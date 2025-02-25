<template>
  <q-dialog
    :model-value="props.openDialog"
    @update:model-value="updateOpenDialog"
  >
    <q-card class="setting-card q-pa-md dialog-card">
      <q-card-section>
        <div class="text-h5">プリセット管理</div>
      </q-card-section>
      <q-card-actions class="q-px-md q-py-sm">
        <div class="full-width row wrap justify-between">
          <q-list bordered separator class="col-sm-grow">
            <draggable
              :modelValue="previewPresetList"
              @update:modelValue="reorderPreset"
              item-key="key"
            >
              <template v-slot:item="{ element: item }">
                <q-item>
                  <q-item-section>{{ item.name }}</q-item-section>
                  <q-space />
                  <q-item-section avatar>
                    <q-btn
                      icon="delete"
                      flat
                      color="display"
                      @click="deletePreset(item.key)"
                    ></q-btn>
                  </q-item-section>
                </q-item>
              </template>
            </draggable>
            <q-item v-if="presetList.length === 0">
              <q-item-section class="display">
                プリセットがありません
              </q-item-section>
            </q-item>
          </q-list>
        </div>
      </q-card-actions>
    </q-card>
  </q-dialog>
</template>

<script setup lang="ts">
import { computed, ref } from "vue";
import { useQuasar } from "quasar";
import draggable from "vuedraggable";
import { useStore } from "@/store";

import { Preset, PresetKey } from "@/type/preload";

const props =
  defineProps<{
    openDialog: boolean;
  }>();
const emit =
  defineEmits<{
    (e: "update:openDialog", val: boolean): void;
  }>();

const updateOpenDialog = (isOpen: boolean) => emit("update:openDialog", isOpen);

const store = useStore();
const $q = useQuasar();

const presetItems = computed(() => store.state.presetItems);
const presetKeys = computed(() => store.state.presetKeys);

const presetList = computed(() =>
  presetKeys.value
    .filter((key) => presetItems.value[key] != undefined)
    .map((key) => ({
      key,
      ...presetItems.value[key],
    }))
);

const isPreview = ref(false);
const previewPresetKeys = ref(store.state.presetKeys);

const previewPresetList = computed(() =>
  isPreview.value
    ? previewPresetKeys.value
        .filter((key) => presetItems.value[key] != undefined)
        .map((key) => ({
          key,
          ...presetItems.value[key],
        }))
    : presetList.value
);

const reorderPreset = (featurePresetList: (Preset & { key: PresetKey })[]) => {
  const newPresetKeys = featurePresetList.map((item) => item.key);
  previewPresetKeys.value = newPresetKeys;
  isPreview.value = true;
  store
    .dispatch("SAVE_PRESET_ORDER", {
      presetKeys: newPresetKeys,
    })
    .finally(() => (isPreview.value = false));
};

const deletePreset = (key: PresetKey) => {
  $q.dialog({
    title: "プリセット削除の確認",
    message: `プリセット "${presetItems.value[key].name}" を削除してもよろしいですか？`,
    cancel: true,
  }).onOk(async () => {
    await store.dispatch("DELETE_PRESET", {
      presetKey: key,
    });
  });
};
</script>

<style>
.dialog-card {
  width: 700px;
  max-width: 80vw;
}
</style>
