## はじめに

これはテキスト音声合成ソフトウェア「VOICEVOX」の使い方を紹介するドキュメントを「ITVOICE」向けに書き換えたものです。

最初に[ITVOICE利用規約](http://itvoice.starfree.jp/terms.html)をご確認ください。

## 起動方法

起動しようとすると「Windows によって PC が保護されました」というダイアログが表示されるかもしれません。その際は「詳細情報」をクリックし、「実行」を選んでください。

<img src="res/image14.png" style="max-height: 16rem" alt="「Windows によって PC が保護されました」というダイアログ" /> → <img src="res/image15.png" style="max-height: 16rem" alt="「詳細情報」をクリックし、「実行」を選んでいる様子。" />

## 音声合成エンジンの起動

最初に音声合成エンジンが起動します。
GPU をお持ちの方は、音声の生成がずっと速い GPU モードを快適にご利用いただけます。

<img src="res/image4.png" style="max-height: 8rem" alt="音声合成エンジンを起動している様子。" />

## 音声の生成

キャラクターアイコンの右にある空白をクリックしてテキストを入力してみてください。

<img src="res/image19.png" style="max-height: 12rem" alt="キャラクターアイコンの右にある空白。" />

エンターボタンを押して文章を確定すると、画面の下の方に読みとアクセントが表示されます。（１回目は反映まで数秒ほど時間がかかることがあります。）

<img src="res/image6.png" style="max-height: 14rem" alt="画面の下の方に読みとアクセントが表示された様子。" />

再生ボタンを押すと音声が生成され、音声が再生されます。

## 文章の追加・削除

右下の＋ボタンを押すとテキスト欄が増え、複数の文章を並べることができます。

<img src="res/image10.png" style="max-height: 14rem" alt="テキスト欄が増えた様子。" />

## キャラクターの変更

テキスト入力欄の左にあるアイコンをクリックすると、テキストを読み上げてくれるキャラクターを変更することができます。

<img src="res/image7.png" style="max-height: 12rem" alt="左にあるアイコンをクリックしてほかのキャラクターアイコンが表示されている様子。" />

キャラクターの表示順序は「キャラクター並び替え」で変更できます。

## テキスト欄の並び替え

テキスト欄周辺をドラッグすることで、テキスト欄の順番を並び替えられます。

## 単語の接続変更

意図しない箇所で単語が分離していた場合や、意図しない形で結合してしまっている場合は、アクセント項目で文字の間をクリックすることで修正できます。

例えば「ディープラーニング」がこのように分かれてしまった場合は、

<img src="res/image9.png" style="max-height: 16rem" alt="「ディープラーニング」が「ディープ」と「ラーニング」に分かれた様子。" />

２つの隙間をクリックすると

<img src="res/image3.png" style="max-height: 8rem" alt="「ディープ」と「ラーニング」の間にマウスカーソルを合わせている様子。マウスカーソルが当たっている部分が青色になります。" />

このように１語にまとめることができます

<img src="res/image8.png" style="max-height: 7rem" alt="「ディープ」と「ラーニング」が「ディープラーニング」の１語にまとまった様子。" />

逆に切り離したい場合は、文字の間をクリックして切り離すことができます。

<img src="res/image13.png" style="max-height: 8rem" alt="「ディープ」と「ラーニング」の間にマウスカーソルを合わせている様子。マウスカーソルが当たっている部分が青色になります。"/>

## アクセントの変更

音声の抑揚が意図しないものだった場合に、抑揚を変える方法が２つあります。まずはアクセント箇所を変えてみることをおすすめします。

アクセント箇所を変えるには、読みの上にあるバーを左右に動かします。
例えば「ディープラーニング」を「↑ ディープラ ↓ アニング」と読んでほしい場合は、「ラ」の位置まで丸をスライドします。

<img src="res/image8.png" style="max-height: 8rem" alt="「ディープラーニング」" /> → <img src="res/image1.png" style="max-height: 8rem" alt="「↑ ディープラ ↓ アニング」" />

## 読みの修正

読みが思っているものと違う場合は、アクセント欄で読みをクリックすることで後から修正することもできます。テキスト欄と同様に、ひらがなや句読点、漢字も入力できます。

<img src="res/image20.png" style="max-height: 12rem" alt="アクセント欄で読みをクリックした様子。修正したいテキストが表示されたテキストボックスが表示されています。テキストボックスの内容を書き換えることで読みを修正できます。" />

修正箇所以外の調整結果はそのままなので、調整結果を維持したままテキストを修正したいときにも便利です。

## スタイルの変更

キャラクターによっては複数のスタイル（喋り方）を変えることができます。キャラクターの変更と同様に、テキスト欄左のアイコンから選択できます。

<img src="res/image21.png" style="max-height: 12rem" alt="キャラクターのアイコンをクリックすると別のキャラクターアイコンが表示されている様子。" />

キャラクターを選択したときに適用されるスタイルは、設定の「デフォルトスタイル」で変更できます。

## 音声ファイルの書き出し

メニューにある「ファイル」の「音声書き出し」ボタンを押すと、全テキスト欄の音声が WAV ファイルとして書き出されます。
ファイル保存時、ファイル名は `[何行目]_[キャラ名]_[テキスト冒頭].wav` として保存されます。設定でテキストファイルも一緒に書き出すこともできます。

## テキストファイルの読み込み

読み込みボタンを押すとテキストファイルを読み込めます。テキストは改行または半角コンマ（,）で区切ることで分割できます。また、キャラクター名だけで区切ることで、そのキャラクターとして読み込むことができます。

例えばこのようなテキストを読み込むと、

```txt
四国めたん,おはようございます,こんにちは
ずんだもん,こんばんは
四国めたん(あまあま),さようなら
```

このように読み込まれます。

<img src="res/image17.png" style="max-height: 12rem" alt="テキストが読み込まれた様子。四国めたん「おはようございます」、四国めたん「こんにちは」、ずんだもん「こんばんは」、四国めたん「さようなら」のように、キャラクターと文章が読み込まれています。" />

スタイル名が指定されていない場合は、デフォルトスタイルのスタイルが適用されます。

## テキストを繋げて書き出し

メニュー「ファイル」の「テキストを繋げて書き出し」ボタンで、すべてのテキストを書き出すことができます。
テキストはキャラクター名も一緒に保存され、上の「テキストファイルの読み込み」で読み込むこともできます

## プロジェクトファイルの保存・読み込み

入力したテキストやキャラクター、アクセント修正やイントネーションの調整結果は、プロジェクトファイルとして保存し、ソフトウェアを起動し直した後で読み込むことができます。プロジェクトファイルの拡張子は`.ivproj`です。

## ショートカットキー

「設定」の「キー割り当て」で変更することができます。

- 上下キー
  - 上下のテキスト欄に移動
- Space
  - 音声を再生
- Shift + Enter
  - テキスト欄を追加
- Shift + Delete
  - テキスト欄を消去
- Ctrl + S
  - プロジェクトの保存
- Ctrl + E
  - 音声を書き出し
- Ctrl + Z
  - 元に戻す
- Ctrl + Y
  - やり直す
- Esc
  - テキスト欄からカーソルを外す
- 1
  - アクセント欄を表示
- 2
  - イントネーション欄を表示
- 3
  - 長さ欄を表示
- スライダーの上でマウスホイール
  - スライダーの値を変更します（スライダー →<img src="res/image16.png" style="max-height: 1rem" alt="スライダー、緑色の棒。" />）
  - Ctrl キーを押しながらマウスホイールを使うと更に細かく調整できます
  - Alt キーを押しながらイントネーションや長さを調整することで、同じアクセント区間内を同時に調整できます
- Ctrl + G
  - 全体のイントネーションをリセット
- R
  - 選択中のイントネーションをリセット

## ツールバーのカスタマイズ

画面上部にあるツールバーのボタンの種類や配置を変更することができます。

<img src="res/toolbar-customize.png" style="max-height: 12rem" alt="ツールバーカスタマイズ画面。" />

## キャラクターの並び替え・試聴

「設定」の「キャラクターの並び替え」で、キャラクターの表示順序を変更することができます。
また、キャラクターごとのサンプルボイスを試聴することもできます。

## デフォルトスタイル

「設定」の「デフォルトスタイル」で、キャラクターごとのデフォルトのスタイルを変更することができます。

## 読み方＆アクセント辞書

難しい単語や新しい単語は正しい読みにならないことがありますが、辞書機能を使って読み方を登録しておくことができます。
辞書機能は「設定」の「読み方＆アクセント辞書」で利用できます。

読み方＆アクセント辞書画面を開くと、左に登録した単語のリストが表示されます。
「追加」ボタンで新規に単語を登録できます。

<img src="res/dict01.png" style="max-height: 12rem" alt="読み方＆アクセント辞書の単語リスト画面。" />

「単語」に登録したいテキストを、「読み」にそのテキストの読み方をひらがなかカタカナで入力してください。
「アクセント調整」で自然になるアクセントを登録できます。
もし登録した単語が反映されない場合は、「単語優先度」を上げてみてください。

<img src="res/dict02.png" style="max-height: 15rem" alt="単語と読みとアクセントの登録画面。" />

## オプション

「設定」の「オプション」でいろいろな設定を変更することができます。

### 「エンジン」項目

エンジンの起動モードの起動モードを変更できます。

GPU モードを利用するには、GPU が必要です。
Linux は Nvidia 製 GPU のみに対応しています。

### 「操作」項目

#### パラメータの引き継ぎ

テキスト欄を追加する際、話速や抑揚といったパラメータを引き継ぐようになります。

#### 再生位置を追従

再生中の単語が画面内に収まるよう、自動的にスクロールして追従するようになります。

#### テキスト分割の挙動

テキストを貼り付け時、句点や改行でテキストを分割するかの挙動を変更できます。

### 「保存」項目

#### 文字コード

読み込み・書き込み用の文字コードを選択できます。

#### 書き出し先を固定

音声ファイルを書き出すフォルダを固定し、毎回フォルダを選択しなくても同じフォルダに書き出し続けるようにします。

#### 書き出しファイル名パターン

音声やテキストファイルなどを書き出す際のファイル名をカスタマイズできます。

#### 上書き防止

同じファイル名のファイルがあった場合に連番として保存します。

#### txt ファイルを書き出し

テキスト内容を一緒に保存します。

#### lab ファイルを書き出し

リップシンクなどに便利な、音声の音素情報とそのタイミング情報が書かれたラベルファイルを一緒に保存します。

### 「高度な設定」項目

#### 音声をステレオ化

音声をモノラルからステレオに変換して再生・保存します。

#### 再生デバイス

音声を再生するデバイスを変更できます。

#### 音声のサンプリングレート

音声のサンプリングレートを変更して再生・保存します。
サンプリングレートを高くしても音声の品質は上がりません。

### 「実験的機能」項目

開発中の便利機能を利用することができます。

#### テーマ変更

デフォルトのライトテーマと、暗めのダークテーマを切り替えることが出来ます。

#### プリセット機能

話速や抑揚などのパラメータをまとめて登録できる機能です。
ソフトウェアが終了しても設定したプリセットは残ります。

#### 疑問文自動調整

疑問文のときに自動的に語尾の音を上げて、疑問文っぽい音声を生成するようになります。
#### モーフィング機能

対応している音声を混ぜてモーフィングした音声を合成できるようになります。
２つの音声を一度生成してから、音声を機械的に分析・再合成する後処理を行うことで実現しています。
#### マルチエンジン機能

VOICEVOX 以外の VOICEVOX API 準拠エンジンを VOICEVOX 内で利用できるようになります。
マルチエンジン機能をオンにしたあと、メニューにある「エンジン」の「エンジンの管理」に移動し、VOICEVOX API 準拠エンジンの VVPP ファイルをインストールするか、VOICEVOX 系ソフトウェア内のエンジンのパスを指定することで利用できます。

## その他

右上のピンボタンでウィンドウを最前面に固定できます。

## ヘルプ

利用規約などを確認することができます。

## アンインストール方法

ダウンロードした ZIP ファイルと、展開したフォルダを消去すればアンインストール完了です。

## よくあるご質問

[Q&A](https://voicevox.hiroshiba.jp/qa) をご参照ください。

## ご感想・ご要望・バグ報告など

ご感想・ご要望は、ぜひ Twitter にてハッシュタグ `#ITVOICE` を付けてツイートしてください。開発の励みになります。

うまく動かない場合や不具合を見つけられた方は、Twitter にて不具合をハッシュタグ `#ITVOICE` を付けてツイートしていただくか、ITVOICE 公式（[@Itvoiceofficial](https://twitter.com/Itvoiceofficial)）までご報告ください。

その他、 Q&A に掲載されていないご質問があれば ITVOICE 公式（[@Itvoiceofficial](https://twitter.com/Itvoiceofficial)）にお問い合わせください。
