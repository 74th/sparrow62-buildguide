# SparrowDial Keyboard Kit Build Guide

このビルドガイドには他のキーボードの写真が含まれていますのでご注意ください。

また、作成中に疑問点等質問がありましたら、74th（Twitter(X): [@74th](https://twitter.com/74th)、email:`site@74th.tech`、本リポジトリのissue）まで問い合わせください。

## 販売先

- booth(準備中)

## SparrowDial の注意点

- マイコンRP2040が直接PCBに実装されています。
- GH60互換キーボードケース対応のPCBですが、必ずしもすべてのケースに対応するわけではありません。
- キットのPCBにはRP2040を動作させるためのマイコン及び受動部品が実装されています。

## キットの内容

### キーボード PCB

- SparrowDial PCB x1
- ダイオード 1N4148W x56
- RGBLED SK6812-MINI-E x1
- 表面実装 Grove(HY2.0) コネクタ（アイボリー色） x2

### M5Stack Core2 PortA 底面引き出しモジュール

- M5Stack Core2 ProtA 底面引き出し PCB x1
- スルーホール Grove(HY2.0) コネクタ（白色） x1
- 表面実装 2x15P ピンヘッダ x1

### ケーブル

- Grove(HY2.0) 互換 ケーブル 10cm x1
- Grove(HY2.0) - USB-C Daughter ケーブル 10cm x1

### ケース組み込み部品

- SparrowDial Top Plate (FR4 PCB) x1
- M2 2mm スペーサー x6 : ケースとPCBの間のスペーサー
- M2 8mm 黒 平ネジ x6 : ケースとPCBの間のネジ止め

## PCB に実装済みの部品

- マイコン RP2040 x1
- マイコンプログラム用フラッシュ W25Q32JVS x1
- RP2040 の動作に必要な受動部品（コンデンサ、抵抗、水晶発振器）
- 電源保護用理想ダイオード CH213K x1
- USB Type-C コネクタ x1
- 表面実装 6x6mm タクタイルスイッチ（RESET/BOOTSEL用） x2

## キットの組み立てに必要なもの

### キットの他に必要なもの

- GH60互換キーボードケース x1
- MX互換スイッチソケット x56
- MX互換スイッチ x56
- MX互換スイッチ用キーキャップ一式 x1
- PC接続用USBType-Cケーブル x1
- Trackpad用M5Stackどちらか
  - M5Stack Core2 x1
  - M5Stack Dial x1

### 組み立てに必要な機材

- はんだごて、はんだ
- ニッパ（キーボードケースの加工用）
- ピンセット（表面実装部品を抑えるのに利用します）
- PC（Windows、Linux、MacOS の動作するもの。ファームウェアの作成に必要）

### あるとよいもの

- フラックス
  - はんだにはフラックスが含まれていて、端子に広がるようにできていますが、熱を加えすぎるとすべてのフラックスが蒸発します。その場合、追加のフラックスを入れて使います
- フラックス洗浄液（はんだや、フラックスが無洗浄タイプでない場合）
- ルーペ（スマートフォンカメラでも代用できます）
- ラジオペンチ（ネジ止めの他、スイッチの足が曲がってしまった場合に、つまんで伸ばします）

## how to build / 作成方法

このキーボードには、RP2040の動作に必要な部品は既に実装されています。

### M5StackCore2 PortA 底面引き出しモジュールの組み立て

M5StackCore2を利用する場合、モジュールを組み立てます。

JP1ジャンパがありますが、ここは真ん中とBATをショートさせます。

<img src="img/dial/m5stack_bottom_jumper.jpeg" width="300px">

次に表面実装2x15Pピンヘッドを実装します。スルーホールと異なり、はんだがピンヘッダにのみに回り、PCBのランドに届いていないことがあります。ランドまで加熱するようにしてください。ピンヘッダはずれやすいため、対角端の1ピンずつを先に実装して位置合わせの上、残りを実装すると良いでしょう。

Grove(HY2.0)コネクタを実装します。このコネクタは、PortAの記述がある面に実装します。

<img src="img/dial/m5stack_bottom_grove.jpeg" width="300px">

### ケースの加工

遊舎工房や、TalpKeyboard で販売されているプラスチック GH60互換ケースでは、干渉が発生するためケースの加工が必要です。

#### 共通

TODO: 写真

写真の印の部分の仕切りをニッパで切り取ります。

#### M5Dial 使用時のみ

TODO: 写真

まず、写真のネジ止め部分を、ニッパで切り取ります。

TODO: 写真

次に、写真の印の部分の仕切りをニッパで切り取ります。

#### M5Dial がどうしても収まらないとき

コードの整理などでぎりぎり収まりますが、収まらないときは、はんだごてで、写真の箇所のプラスチックを溶かし、空間を広げます。

TODO: 写真

主に障害になるのは、M5Dial の底部の下の方です。

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

### Soldering switch sockets / スイッチソケットを実装する

We recommend soldering the socket as shown in the video. With the latest Kailh switch sockets, it is no longer possible to insert the soldering iron from the top, but you should still insert it from the open side.
🇯🇵 ソケットのはんだ付けは動画のようにすることをおすすめしています。最新のKailh社製スイッチソケットでは、上面からはんだごてを差し込むことはできなくなりましたが、それでも横の空いている面からはんだごてを差し込む様にします。

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

### Soldering Grove(HY2.0) sockets / Grove(HY2.0) ソケットの実装

2箇所あるGrove(HY2.0)ソケットを実装します。

まず、1本のピンのみを実装し、はんだごてを更にあてながらPCBのシルクの位置になるように調整します。その後、残りのピンも実装します。ケーブルを差し込む面にも下部に固定用の金属部分があるため、こちらも忘れずに実装します。

TODO:

### M5StackCore2、M5Dialへのファームウェアの書き込み

ファームウェアは以下の方法でマイコンにアップロードできます。

- 1. https://74th.github.com/sparrow62-buildguide/firmware/index.html にて、ファームウェアをアップロードする
- 2. esptool.py等ファームウェアアップロードツールを用いる

M5StackCore2、M5DialはUSBで接続します。M5Dialについてはケースに組み込む前にファームウェアをアップロードする必要があります。

TODO:

### ケースへの組み込みの前の実装確認

ケースへの組み込むと、はんだ実装に不具合があっても、キーキャップ、スイッチ、ネジなどのすべてを外さないとPCBの実装面にはアクセスできません。なるべく、ケースに組み込む前に、一度はんだ実装不良がないか確認すると良いでしょう。

#### M5StackCore2を使う場合

M5StackCore2のM-Bus PCB（底面のCore2と書かれた白いPCB）を外します。このPCBには、ピンヘッダとピンソケットで本体PCBに接続されており、垂直に抜く必要があります。

TODO: 写真

M5StackCore2の底面の4つのネジを外し、ボトムケースを取り外します。ボトムケース部分には、バッテリーが搭載されており、本体PCBとソケットとケーブルで接続されています。このソケットを外して下さい。

TODO: 写真

M-BusにM5StackCore2 PortA 底面引き出しモジュールを写真の向きで接続します。

TODO: 写真

なお、必ずバッテリーを外した状態で行ってください。

M5StackCore2 PortA底面引き出しモジュールのGroveソケットと、SparrowDial PCBのI2C Groveと書かれたGroveソケットを、HY2.0(Grove)ケーブルで接続してください。

#### M5Dialを使う場合

M5Dialの裏面のPortAのGroveソケット（赤色）と、SparrowDial PCBのI2C Groveと書かれたGroveソケットを、HY2.0(Grove)ケーブルで接続してください。

M5DialのUSBと、SparrowDial PCBのPower Groveと書かれたGroveソケットを、Grove USBドーターケーブルで接続してください。

#### キーの確認

PCBをUSBに接続します。出荷時点でキーボードとして動作するファームウェアが書き込まれています。

M5StackCore2、M5DialにI2C Connection Errorと書かれている場合、I2C通信に失敗していることがあります。ソケットの実装を見直してください。また、ファームウェア書き込み後にもこの表示が消えない場合には、一度USBを抜き差しして電源を入れ直してみてください（USBの抜き差しで、RP2040とM5StackCore2/M5Dialの両方の再起動を同じタイミングで行えます）。

M5StackCore2/M5Dialを操作し、マウスカーソルが動作することを各員してください。

QMK Configuratorのテスト画面を呼び出します。この画面では、キー入力に対して、どのキーが押されたのかを表示します。

> QMK Configurator
>
> https://config.qmk.fm/#/test

スイッチソケットの2箇所の金属部をジャンパ線や、ピンセットなどをあてて、通電させます。すると、キースイッチが動作していれば、キー入力として反応します。キー入力として認識されない場合には、そのキーのダイオード、スイッチソケットの実装をやり直します。

縦一列や、横一列反応しない場合には、RP2040のピンの実装が外れてしまった可能性があります。フラックスを塗った上で、RP2040の対応するピンにはんだごてを当てて、再実装します。どのキーがどのピンに対応しているかは、回路図を参照ください。

また、このキーボードはレイアウト変更時に、LEDの色が変わるようになっています。初期状態でLEDが点灯することを確認してください。

### SparrowDial PCB上のRP2040へのファームウェアの書き込み

始めからVIA、Remap用のファームウェアが書き込まれた状態になっています。

VIA、Remapを利用しない利用しない場合は、別途ファームウェアを用意してください。RP2040はBOOTSELボタンを押しながらRESETを行うと、USBマスストレージデバイスがPCに認識され、その中にuf2ファイルをドラッグドロップすることで、ファームウェアを書き込むことができます。

#### VIA、Remapを利用する場合

VIA、RemapはWebサイトや、ツール上からキーマップの書き換えができるサイトです。VIA対応のファームウェアをRP2040にアップロードすると、利用できるようになります。

- Remap https://remap-keys.app/
- VIA https://caniusevia.com/

ファームウェアは以下からダウンロードできます。

- VIA、Remap 用ファームウェア [firmware/sparrowdial_via.uf2](https://github.com/74th/sparrow62-buildguide/raw/master/firmware/sparrowdial_via.uf2)

#### QMK Firmwareでファームウェアをビルドする場合

現在、SparrowDialキーボードはQMK Firmwareの本体には取り込まれていません。下記リポジトリに作成したファームウェアのコードがあります。

https://github.com/74th/qmk_firmware_sparrow_keyboard

QMK Firmwareの環境のセットアップについては[公式のドキュメント https://docs.qmk.fm/#/newbs_getting_started](https://docs.qmk.fm/#/newbs_getting_started)を確認ください。[日本語のドキュメント https://docs.qmk.fm/#/ja/newbs_getting_started](https://docs.qmk.fm/#/ja/newbs_getting_started)もあります

まず、リポジトリをチェックアウトしてください。QMK Firmwareのフォークとなっているため、QMK Firmwareのセットアップでチェックアウトされたgitリポジトリのremoteとして登録できます。

```sh
cd ~/qmk_firmware
git remote add sparrow https://github.com/74th/qmk_firmware_sparrow_keyboard.git
git fetch sparrow
git checkout sparrow
```

このリポジトリ上では、キーボード名`sparrowdial`として登録されています。新しいキーマップを作成するには以下を実行します。

```
qmk new-keymap -kb sparrowdial -km <keymap_name>
```

`~/qmk_firmware/keyboards/sparrowdial/keymaps/<keymap_name>`というフォルダに作成されるため、キーマップを作成します。

キーマップ作成後は、以下のコマンドでコンパイルします。

```
qmk compile -kb sparrowdial -km <keymap_name>
```

すると、`~/qmk_firmware/.build/sparrowdial_<keymap_name>.uf2`にビルドされるため、これをRP2040に書き込みます。

### ケースへの組み込み

ケースへの組み込みは以下の手順で行います。

1. ケース底面の加工（まだの場合）
2. SparrowDial PCBへGroveケーブルを接続
3. （M5Dialを用いる場合のみ）ケース底面のネジ穴に対して、2mm中空スペーサーを置く
4. SparrowDial PCBをケースに配置する
5. SparrowDial PCBとケースのネジ止め
6. SparrowDial Top PlateへのM5StackCore2、M5Dialの組み込み
7. SparrowDial Top Plateを重ねる
8. スイッチの差し込み
9. キーの動作テスト
10. キーキャップの差し込み

#### 1. ケース底面の加工（まだの場合）

前述のケース底面の加工を行ってください。

#### 2. SparrowDial PCBへGroveケーブルを接続

HY2.0(Grove)ケーブルをSparrowDial PCBのI2C Groveポートに接続してください。

M5Dialを用いる場合、追加でGrove USBドーターケーブルをSparrowDial PCBのPower Groveポートに接続してください。

コードの先端を、SparrowDial PCBの中央の円形ホールを通すようにしてください。

TODO: 写真

#### 3. （M5Dialを用いる場合のみ）ケース底面のネジ穴に対して、2mm中空スペーサーを置く

ケース底面の、各ネジ穴のところに、M2 2mm中空スペーサーを置きます。

TODO: 写真

#### 4. SparrowDial PCBをケースに配置する

SparrowDial PCBを載せます。

M5Dialを用いる場合、ケースの上の中空スペーサーを落とさないように気をつけてください。

M5StackCore2を用いる場合、若干ダイオードがケースに干渉しますが、少しPCBをずらすと干渉を避けて、ケースのネジ穴に密着させることができます。

TODO: 写真

#### 5. SparrowDial PCBとケースのネジ止め

付属のネジを用いて、M2 8mmネジで6箇所を留めます。M5Dialを用いる場合、中空スペーサーを落とさない様にしてください。

TODO: 写真

#### 6. SparrowDial Top PlateへのM5StackCore2、M5Dialの組み込み

SparrowDial Top Plateは、SparrowDialの名前が入っている方が、上面になります。上面がタッチパネルになるように取り付けます。

##### 6.1. M5StackCore2を用いる場合

M5StackCore2のM-busのPCBは取り外してください。

M5StackCore2の、ボトムケースを外してください。ボトムケースにはバッテリーが取り付けられており、PCBとはケーブルとソケットで繋がれています。このケーブルは取り外してください。

そして、

M5StackCore2のM-Bus PCB（底面のCore2と書かれた白いPCB）を外します。このPCBには、ピンヘッダとピンソケットで本体PCBに接続されており、垂直に抜く必要があります。

TODO: 写真

M5StackCore2の底面の4つのネジを外し、ボトムケースを取り外します。ボトムケース部分には、バッテリーが搭載されており、本体PCBとソケットとケーブルで接続されています。このソケットを外して下さい。

TODO: 写真

M-BusにM5StackCore2 PortA 底面引き出しモジュールを写真の向きで接続します。

TODO: 写真

M5StackCore2のタッチボタンが左側になるように、Top Plateの裏面からM3ネジで留めます。

TODO: 写真

なお、必ずバッテリーを外した状態で行ってください。

M5StackCore2 PortA底面引き出しモジュールのGroveソケットと、SparrowDial PCBのI2C Groveと書かれたGroveソケットを、HY2.0(Grove)ケーブルで接続してください。

##### 6.2. M5Dialを用いる場合

M5Dialの、オレンジ色の大きなナット部品を使って、Top Plateを挟み込むように固定します。この時、上面のM5の文字が下になるようにしてください。

TODO: 写真

M5DialのPortA Groveソケット（赤茶色）に、SparrowDial PCBのI2C Groveと接続されたHY2.0ケーブルを接続します。

M5DialのUSBソケットに、SparrowDial PCBのPower Groveと接続されたGrove USBドーターケーブルを接続します。

TODO: 写真

#### 7. SparrowDial Top Plateを重ねる

SparrowDial Top Plateを、ケースに重ねます。SparrowDialは、PCBとTop Plate間の固定は、スイッチのみで行います。

TODO: 写真

#### 8. スイッチの差し込み

SparrowDial Top Plateの穴から、SparrowDial PCBに向かってスイッチを差し込みます。MX互換スイッチには、Top Plateを挟み込む溝が付いています。この溝にTop Plateが挟まれるようにTop Plateを持ち上げてください。

この時、M5Dial、M5StackCore2のまわりのスイッチと、左右外側のスイッチから、順に固定していくと、高さをキープしやすくなります。

TODO: 写真

M5Dialは結構干渉し、十分に刺さらない場合があります。その場合、M5Dialのケーブルが干渉していないか確認して、ケーブルをずらしたり、前述の「M5Dial がどうしても収まらないとき」の対策を行ってみてください。

#### 9. キーの動作テスト

USBをPCに接続し、QMK Configuratorを開き、キーをタイプしてすべてのキーが動作するかを確認します。

動作しないキーがある場合、一度すべてをケースから取り外し、該当キーのダイオードとスイッチソケットの実装をやり直します。取り外す必要があるため、一度すべてのキーを挿してみることをお勧めします。

#### 10. キーキャップの差し込み

すべてのキーが動作することを確認できたならば、キーキャップを付けて完成です！
