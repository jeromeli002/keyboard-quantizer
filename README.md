# Keyboard Quantizer
Keyboard Quantizerは一般的なUSBキーボードを自作キーボード用のファームウェアの定番であるQMKに対応させるためのボードです。キー配列を自由に変えられるだけでなく、キーボードにレイヤ、マクロ、コンビネーションなどの機能を追加できるようになります。

(2021/2/5) マウス/トラックボールにも対応しました。ボタンに任意の動作を設定したり、ジェスチャ機能を追加したりできます。  
ファームウェアを開発することによってその他のHID機器も接続できます。

|![rev2](img/rev2.jpg)|![rev3](img/rev3_rear.jpg)|
|-|-|
|rev1(rev2はPro Micro側にLCDを取り付けます)|rev3|

## 販売リンク
- [BOOTH](https://nogikes.booth.pm/items/2256612)
- [遊舎工房](https://yushakobo.jp/shop/keyboard-quantizer/)

## 制約事項
簡単な仕組みとしては、
1. USBホスト用のマイコンがUSB機器と通信し
1. 受け取ったレポートをボード上のPro Microに送信
1. Pro Microはレポートから押されたキーを判定してQMK上の処理をする

といった流れになっています。

そのため、Fnキーなどのレポートとしては送信されないキーに反応することはできません。Fnキーと他のキーの組み合わせにより入力されるキー/音量調整などのレポートは受け取ることができます。

NKROやポインティングデバイス付きのキーボードについては認識できる場合とできない場合があります。  
一般的なプロトコル(モディファイア+予約(1byte)+6キー分のデータを送信する)のキーボードやマウス(8ボタン、スクロール、パン)であれば安定して認識できます。  

既存のファームウェアで認識できないデバイスについてはファームウェアを改造して頂く必要があります。

## ビルドガイド
- [rev2以前(Pro Microを乗せるタイプ)](rev2.md)
- [rev3(ケースに入ったタイプ)](rev3.md)
