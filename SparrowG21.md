# SparrowG21 Build Guide

このビルドガイドには他のキーボードの写真が含まれていますのでご注意ください。

また、作成中に疑問点等質問がありましたら、74th （twitter: [@74th](https://twitter.com/74th) 、email: site@74th.tech 、 本リポジトリの issue）まで問い合わせください。

## 販売先

- booth(準備中)

## Sparrow60C の注意点

- マイコン RP2040 が直接 PCB に実装されています。
- GH60 互換キーボードケース対応の PCB ですが、必ずしもすべてのケースに対応するわけではありません。
- キットの PCB には RP2040 を動作させるためのマイコン及び受動部品が実装されています。

## キットの内容

- Sparrow60C PCB x1
- Sparrow60C Top Plate (FR4 PCB) x1
- ジョイスティックモジュール StickPointV x1
- HY2.0 ケーブル x1
- ダイオード 1N4148W x60
- RGBLED SK6812-MINI-E x1
- 0805 SMD 抵抗 x2
- 0805 SMD 青色LED x2

### PCB に実装済みの部品

- マイコン RP2040 x1
- マイコンプログラム用フラッシュ W25Q32JVS x1
- RP2040 の動作に必要な受動部品（コンデンサ、抵抗、水晶発振器）
- 電源保護用理想ダイオード CH213K x1
- USB Type-C コネクタ x1

## キットの組み立てに必要なもの

### キットの他に必要なもの

- GH60 互換キーボードケース x1
- MX 互換スイッチソケット x60
- MX 互換スイッチ x60
- MX 互換スイッチ用キーキャップ一式 x1
- PC 接続用 USB Type-C ケーブル x1

### 組み立てに必要な機材

- はんだごて、はんだこて台、スポンジ
- はんだ
- ピンセット（表面実装部品を抑えるのに利用します）
- 両面テープ（ゴムシートとボトムプレートを接着します）
- PC（Windows、Linux、MacOS の動作するもの。ファームウェアの作成に必要。）

### あるとよいもの

- フラックス
  - はんだにはフラックスが含まれていて、端子に広がるようにできていますが、熱を加えすぎるとすべてのフラックスが蒸発します。その場合、追加のフラックスを入れて使います
- フラックス洗浄液
- ルーペ（スマートフォンカメラでも代用できます）
- ラジオペンチ（ネジ止めの他、スイッチの足が曲がってしまった場合に、つまんで伸ばします）

## how to build / 作成方法

### Solder Diodes / ダイオードのはんだ付け

Solder the diode, paying attention to the orientation of the diode.
🇯🇵 ダイオードを向きを気をつけて、はんだ付けします。

The video by @Salicylic_acid3 is very good, so I think you can check here.
🇯🇵 実装手順については、サリチル酸さんのツイートの動画が非常に良くできているため、こちらを確認いただくと良いと思います。

https://twitter.com/Salicylic_acid3/status/1296494976319315970
https://twitter.com/Salicylic_acid3/status/1108798243142434816

Solder one side of the PCB first.
🇯🇵 先に PCB の片側にはんだをつけます。

![](img/v1/diode1.jpg)

Melt the solder you have applied and solder one side of the diode.
🇯🇵 つけたハンダを溶かして、ダイオードを片側をはんだ付けします。

![](img/v2/diode_1.jpg)

First, solder all the diodes **only one side**.
Once one side is soldered, check that all diodes are facing the same way.
🇯🇵 まず、すべてのダイオードを**片側だけ**はんだ付けをしましょう。
片側のはんだ付けが済んだところで、一度すべてのダイオードが同じ向きを向いているか確認します。

![](img/v1/diode4.jpg)

Once you have checked and it is ok, solder the other leg as well.
🇯🇵 確認が済んで大丈夫であれば、反対側の足もはんだ付けします。

![](img/v1/diode2.jpg)

### Soldering the switch socket / スイッチソケットを実装する

> [!CAUTION]
> MX互換キー用ソケットを取り付けた場合には、Kailh Chocスイッチを利用することはできません。Kailh Chocスイッチを利用する場合には、ソケットを実装しないでください。

We recommend soldering the socket as shown in the video.
🇯🇵 ソケットのはんだ付けは動画のようにすることをおすすめしています。

[Movie（Google Drive）](https://drive.google.com/file/d/1VQYtKHCZkTQwoi6JiOMwTrHwYhy1caux/view?usp=sharing)

[Movie（Twitter）](https://twitter.com/74th/status/1514942328900775938)

[Movie file switch_socket.mp4](./img/v2/switch_socket.mp4)

1. Set the socket in the correct orientation.
2. Apply heat with a soldering iron from the inside of the socket's terminals.
3. From the outside of the socket, apply solder with the soldering iron and pour the solder into the socket.
4. Remove the solder and hold the socket with tweezers.
5. remove the soldering iron

🇯🇵

1. ソケットを正しい方向にセットします。
2. ソケットの端子の内側から、はんだごてで熱を加えます
3. ソケットの外側から、はんだごてを当ててはんだを流し込みます
4. はんだを外してから、ピンセットなどでソケットを抑えます
5. はんだごてを抜きます

### Kailh Chocスイッチの実装

> [!CAUTION]
> Kailh Chocスイッチを取り付けた場合には、MX互換スイッチを利用することはできません。MX互換スイッチを利用する場合には、Kailh Chocスイッチを実装しないでください。

表面から、Kailh Chocスイッチを差し込み、裏面から実装します。かならず、写真のようにLEDのランドが見えている面ではんだ付けをするようにしてください。

TODO: 写真

### RGBLED を実装する

RGBLED SK6812MINI-E の方向を注意してください。

RGBLED の実装は、PCB 裏面に裏向きにセットして実装します。
PCB 表向きから見ると、発光面が見える形になります。

また、RGBLED の 4 本の足の 1 つ GND には切れ込みが入っています。切れ込みとシルクの斜め線を合わせるようにしてください。

![](./img/v2/led_1.jpg)

![](./img/v2/led_4.png)

向きを確認できたら、一方の足をマスキングテープで留めます。

![](./img/v2/led_2.jpg)

すべての足を実装します。

![](./img/v2/led_3.jpg)

### Soldering Grove(HY2.0) sockets / Grove(HY2.0) ソケットの実装

Grove(HY2.0)ソケットを実装します。

まず、1本のピンのみを実装し、はんだごてを更にあてながらPCBのシルクの位置になるように調整します。その後、残りのピンも実装します。ケーブルを差し込む面にも下部に固定用の金属部分があるため、こちらも忘れずに実装します。

TODO:

### OLEDの実装

OLEDにはVCCとGNDの位置の違いで、2種類あり、それに応じてジャンパを実装するようになっています。キットでは、同梱したOLEDによって、すでにジャンパがなされています。

以下の手順で実装します。

![](img/g21/solder_oled.svg)

実装後は以下のようになります。

TODO: 写真

### ジョイスティックの実装

表面からスルーホールに差し込み、実装します。実装後、余分な足を切り取ります。

TODO: 写真

### トッププレートのLEDと抵抗の実装

> [!NOTE]
> トッププレートは、MX互換スイッチを使用する場合のみ利用可能です。Kailh Chocスイッチの場合は利用できません。

青色LEDと抵抗を実装します。実装の仕方は、ダイオードの時と同じで、まず片方のランドに

青色LEDは、裏面から、表面に向かって光を届けます。実装面では、矢印や記号が見える状態にしてください。以下の様になっていれば正しい向きとなります。

![](img/common/led_direction.svg)

TODO: 写真

### トッププレートとPCBのQwiicソケットの実装

> [!NOTE]
> トッププレートを使わないChocスイッチを使う場合は実装は不要です。
