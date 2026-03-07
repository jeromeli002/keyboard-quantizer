# Keyboard Quantizer Mini (キット版)　ビルドガイド

## 必要なもの

* はんだごて、はんだ
* ラジオペンチ

## キットに入っているもの

* 基板
* USBコネクタ（オス・メス）
* ケース

## 組み立て手順

### ハンダ付け

* 基板にタブがついている場合は折る
  |![](../img/mini-pcb-1.JPG)|![](../img/mini-pcb-2.JPG)|
  |-|-|
* USBコネクタ（オス）を基板に差し込む
  * 基板から浮かないように奥までしっかり押し込んでください

  ![](../img/mini-plug-side.JPG)
* USBコネクタ（オス）をハンダ付けする

  ![](../img/mini-plug-top.JPG)
* USBコネクタ（オス）のタブ部分をラジオペンチで軽く折り曲げる
  |![](../img/mini-plug-bottom.JPG)|![](../img/mini-plug-side-2.JPG)|
  |-|-|
* USBコネクタ（メス）を基板に差し込む
  * 基板から浮かないように奥までしっかり押し込んでください
* USBコネクタ（メス）をハンダ付けする
  * ハンダを盛りすぎてほかの部分とショートしないように気を付けてください
* USBコネクタ（オス）のタブ部分をハンダ付けする
  * USBコネクタ全体が熱くなるので火傷しないように注意してください
  ![](../img/mini-receptacle-bottom.JPG)
* USBコネクタ（オス）が冷めるのを待つ

### 動作確認

* Keyboard Quantizerにキーボードを接続する
* Keyboard QuantizerをPCに差し込む
* RPI-RP2ドライブが表示されたら[vial用ファームウェアのUF2ファイル](https://github.com/sekigon-gonnoc/keyboard-quantizer-doc/releases/download/mini-6/sekigon_keyboard_quantizer_mini_vial.uf2)を書き込む
* Keyboard Quantizer MiniのLEDが点灯するのを待つ
  * 初回書き込みは起動まで数十秒、そこからキー入力を認識できるようになるまで10秒くらいかかります
* キーボードからキー入力できることを確認する

### ケースの取り付け

* Keyboard Quantizerのオスコネクタ側からケースに差し込む
 ![](../img/mini-case-1.JPG)
* ケースのタブとオスコネクタを持ち上げながらさらに押し込む
  * メスコネクタとケースが引っかかる場合があります。その場合はメスコネクタ側のケースを軽く持ち上げながら押し込んでください

 |![](../img/mini-case-2.JPG)|![](../img/mini-case-3.JPG)|
 |-|-|
 |押し込んでいる途中をオス側から見た図|押し込んでいる途中を横から見た図（右がオス側）|

 ![](../img/cut-model.png)
