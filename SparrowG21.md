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

- SparrowG21 PCB x1
- SparrowG21 Top Plate (FR4 PCB) x1
- OLED x1
- ジョイスティックモジュール B10K x2
- SH1.0-4P(Qwiic) ケーブル x1
- ダイオード 1N4148W x60
- RGBLED SK6812-MINI-E x12
- SH1.0-4P(Qwiic) SMD ソケット x1
- M2 2mm スペーサー x4 : StickPointV、PCB間
- M2 8mm 黒 平ネジ x7 : ケースとPCBの間のネジ止め

### PCBに実装済みの部品

- マイコン RP2040 x1
- マイコンプログラム用フラッシュ W25Q32JVS x1
- RP2040 の動作に必要な受動部品（コンデンサ、抵抗、水晶発振器）
- 6x6mm SMD タクタイルスイッチ（RP2040 RESET、BOOTSEL用） x2
- 電源保護用理想ダイオード CH213K x1
- 0805 SMD 青色LED x2
- USB Type-C コネクタ x1

### トッププレートに実装済みの部品

- SH1.0-4P(Qwiic) SMD ソケット x1
- 0805 SMD 抵抗 x2
- 0805 SMD 青色LED x2

## キットの組み立てに必要なもの

### キットの他に必要なもの

本キットは、「MX互換スイッチ」もしくは「Kailh Choc v1 スイッチ/LOFREE x KAILH Full POM Low Profile スイッチ」を排他的に利用します。

#### 共通で必要なもの

- GH60 互換キーボードケース x1
- MX 互換スイッチソケット x21 （MX互換スイッチを用いる場合）
- MX 互換スイッチ x21（MX互換スイッチを用いる場合）
- MX 互換スイッチ用キーキャップ一式 x1（MX互換スイッチを用いる場合）
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

### RGBLED の実装

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

表面からスルーホールに差し込みます。まず、足を1本だけ実装し、奥まで刺さっていることを確認してから、残りの足を実装してください。足の実装後、余分な足の部分をニッパ出切り取ります。

TODO: 写真

### 実装後の確認

本キットのRP2040にはあらかじめGP2040-CEを書き込んでいます。

実際にキーを押して確認してください。

テスト画面の表示の仕方はWindowsであれば以下のサイトを参照してください。

> ゲームパッドとは？／動作確認方法は？／設定方法は？
>
> https://qa.elecom.co.jp/faq_detail.html?id=5432

GP2040-CEを新たにRP2040に書き込んだ場合には、SparrowG21用のキーアサインをやり直す必要があります。

### GP2040-CEのSparrowG21用の設定

本キットのRP2040にはあらかじめ設定したGP2040-CEを書き込んでいます。以下は、GP2040-CEのファームウェアを更新した場合や、設定を変更したい場合に参照してください。

GP2040にはWeb Configuratorがあります。Web Configuratorを起動するには、以下のように操作します。

- GP2040インストール直後: R3キー（IO17）を押しながらRESETを押す
- SparrowG21用の設定を適用後: S2キーを押しながらRESETを押す

その後、ブラウザにて [http://192.168.7.1](http://192.168.7.1)にアクセスすると開けます。

#### Pin Mapping

各スイッチと繋がるピンの設定です。

ヘッダーの「Configuration」から「Pin Mapping」を開いてください。

それぞれのピンを以下のように設定してください。設定後、Saveを押してください。

| GP2040   | Pin |
| -------- | --- |
| Up       | 7   |
| Down     | 5   |
| Left     | 2   |
| Right    | 6   |
| B1       | 14  |
| B2       | 16  |
| B3       | 13  |
| B4       | 15  |
| L1       | 21  |
| R1       | 19  |
| L2       | 22  |
| R2       | 20  |
| S1       | 23  |
| S2       | 3   |
| L3       | 17  |
| R3       | 18  |
| A1       | 8   |
| A2       | 11  |
| Function | 12  |

![](./img/g21/gp2040-pin-mapping.png)

#### LED Configuration

各スイッチのLEDの設定です。

ヘッダーの「Configuration」から「LED Configuration」を開いてください。

以下を設定します。設定後、Saveを押してください。

| Setting Group Name    | Setting Name    | Value           |
| --------------------- | --------------- | --------------- |
| RGB LED Configuration | Data Pin        | 24              |
|                       | LED Format      | RGB             |
|                       | LED Layout      | 8-Button Layout |
|                       | LEDs Per Button | 1               |

![](./img/g21/gp2040-led-configuration.png)

#### Display Configuration

中央のOLEDの設定です。

ヘッダーの「Configuration」から「Display Configuration」を開いてください。

以下を設定します。設定後、Saveを押してください。

| Setting Name   | Value    |
| -------------- | -------- |
| Enabled        | Enabled  |
| I2C Block      | i2c0     |
| SDA Pin        | 0        |
| SCL Pin        | 1        |
| I2C Address    | 0x3C     |
| I2C Speed      | 400000   |
| Flip Display   | None     |
| Invert Display | Disabled |

![](./img/g21/gp2040-display-configuration.png)

#### On-Board LED Configuration

SparrowG21のロゴの右側のLEDの設定です。

ヘッダーの「Configuration」から「Add-Ons Configuration」を開いてください（以降の設定はすべてAdd-Ons Configurationです）。

「On-Board LED COnfiguration」と書かれたパネルの「Enabled」をオンにしてください。LED Modeはお好みのものを設定してください。設定後、最下部のSaveを押してください。

![](./img/g21/gp2040-onboard-led-configuration.png)

#### Analog

2つのジョイスティックの設定です。

ヘッダーの「Configuration」から「Add-Ons Configuration」を開いてください。

「Analog」と書かれたパネルの「Enabled」をオンにして、設定項目に以下の設定をしてください。設定後、最下部のSaveを押してください。

| Setting Name          | Value        |
| --------------------- | ------------ |
| Analog Stick 1 X Pin  | 26           |
| Analog Stick 1 Y Pin  | 27           |
| Analog Stick 1 Mode   | Left Analog  |
| Analog Stick 1 Invert | None         |
| Analog Stick 2 X Pin  | 28           |
| Analog Stick 2 Y Pin  | 29           |
| Analog Stick 2 Mode   | Right Analog |
| Analog Stick 2 Invert | None         |
| Deadzone Size         | 5            |

![](./img/g21/gp2040-analog.png)

#### Turbo

連射機能の設定です。

ヘッダーの「Configuration」から「Add-Ons Configuration」を開いてください。

「Turbo」と書かれたパネルの「Enabled」をオンにして、設定項目に以下の設定をしてください。設定後、最下部のSaveを押してください。

| Setting Name                 | Value    |
| ---------------------------- | -------- |
| Turbo Pin                    | 9        |
| Turbo Pin LED                | 10       |
| Turbo Shot Count（連射速度） | お好みで |
| Turbo Dial                   | none     |

#### Extra Button Configuration

追加ボタン（Down、RIGHT、S2ボタンに挟まれたEXTRAボタン）の設定です。任意のボタンを左手にも割り当てることができます。

ジャンプアクションゲームでDownキーを割り当て、従来のDown（IO5）にUp、従来のUp（IO7）にB1を割り当てたりして、左手親指でジャンプする操作を想定しています。

ヘッダーの「Configuration」から「Add-Ons Configuration」を開いてください。

「Extra Button Configuration」と書かれたパネルの「Enabled」をオンにして、設定項目に以下の設定をしてください。設定後、最下部のSaveを押してください。

| Setting Name | Value |
| Extra Button Pin | 4 |
| Extra Button（機能させるキー）| Downなどお好みで |

## トラブルシューティング

こちらのページを確認ください。

> Trouble Shooting Guide
>
> [./trouble_shooting_guide.md](./trouble_shooting_guide.md)
