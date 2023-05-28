# Keyboard Quantizer
Keyboard Quantizerは一般的なUSBキーボードやマウスを自作キーボード用のファームウェアの定番であるQMKに対応させるためのボードです。キー配列を自由に変えられるだけでなく、キーボード/マウスにレイヤ、マクロ、コンビネーションなどの機能を追加できるようになります。

[キーボードの対応状況を調査しています。ご協力お願いします。](https://forms.gle/qfXvfceP8PH9swBT8)

[集計結果まとめ](keyboard_list.md)

(2021/3/30) USBハブ経由での接続に対応しました。1段4ポートまで認識できます。 (※ハブとの相性によっては動作しないようです) 
(2021/2/5) マウス/トラックボールにも対応しました。ボタンに任意の動作を設定したり、ジェスチャ機能を追加したりできます。  
ファームウェアを開発することによってその他のHID機器も接続できます。

|![rev2](img/rev2.jpg)|![rev3](img/rev3_rear.jpg)|
|-|-|
|rev1(rev2はPro Micro側にLCDを取り付けます)|rev3, rev4|

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
- [rev4(基板にKeyboard Quantize RPのシルクがある)](rev4.md)
- [mini](mini/README.md)

## よくある質問
- xxキーボードで動きますか？
  - [対応状況調査まとめ](keyboard_list.md)
  - xxキーボードが手元にない場合は回答できません
    - HIDキーボードとして認識されるのであれば最終的にはQMKファームウェアを編集することで動作させられると思われます
