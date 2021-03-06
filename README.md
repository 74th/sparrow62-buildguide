# Sparrow 62 Keyboard ビルドガイド

## Sparrow 62 Keyboard とは

Lily58 に触発された @74th が販売する、自作キーボードキットです。

**Kailh Choc V2 キースイッチの場合（キーキャップ: DSA）**
![](img/top_choc.jpg)
![](img/top_choc2.jpg)

以下のような特徴があります。

- 薄型キースイッチ Kailh Choc V1/V2 が使えること。
- Cherry MX 互換キースイッチが使えること。
- 縦に揃ったキー配置(カラムスタッガード)であること。
- 十分キーの数が多いこと。
- Pro Micro をキーの横に配置してキーボード自体を薄くすること。
- キースイッチ交換可能なようにソケットを使うこと。
- ボトムプレート、トッププレートをキットに含まないが、必要であれば別途発注可能であること。

一方、この特徴をシンプルに実現するために、妥協している点は以下のとおりです。

- LED に対応しないこと。
- OLED ディスプレイ に対応しないこと。
- 形が角ばっており、 Lily58 に比べて外見にこだわりがないこと
- 薄さを優先し、ボトムプレートをキットに含まないこと

より作りやすい、完成度の高いキーボードとして、ゆーちさんの頒布されている Lily58 があります。
ぜひ Lily58 の購入も検討ください。

**Kailh Choc V1 キースイッチの場合**
![](img/top_choc_v1.jpg)

**Cherry MX 互換スイッチを使用し、トッププレートを加えた場合（キーキャップ: DSA）**
![](img/top_cherry_mx.jpg)

### 対応、おすすめキースイッチ

Sparrow62 Keyboard では、以下のキースイッチに対応しています。

- MX 互換キースイッチ
- Kailh Low Profile Choc v1 ([遊舎工房](https://yushakobo.jp/shop/pg1350/)): 非常に薄いメカニカルキースイッチです。ただし、専用のキーキャップが必要です。
- Kailh Low Profile Choc v2 ([遊舎工房](https://yushakobo.jp/shop/kailh-choc-v2/)): 非常に薄いメカニカルキースイッチです。MX 軸の一般的なキーキャップが使用可能です。

製作者のおすすめは、以下の順です。

- Durock T1 ... Holy Panda 調の強いタクタイルスイッチ。高品質だが、ちょっとお高め。
  - [TALP KEYBOARD](https://talpkeyboard.stores.jp/items/5fe9830e72eb4624411ad5f9)
- Durock ミディアムタクタイル ... 程よいタクタイル。小指用に使っています。高品質だが、ちょっとお高め。
  - [TALP KEYBOARD](https://talpkeyboard.stores.jp/items/5fe9a5a6da019c0abb3e6fa6)
- Kailh Speed Switch Copper ... 作用点までが 1mm と軽快に使えるゲーマースイッチ。
  - [遊舎工房](https://yushakobo.jp/shop/kailh-speed/)
- Kailh Low Profile Choc v2 ... 薄いキースイッチ。ちょっとお高め。
  - [遊舎工房](https://yushakobo.jp/shop/kailh-choc-v2/)

現在（2021/02/11）製作者が主に使っているのは、Durock T1、Durock ミディアムタクタイルです

## カスタマイズ

作者は主に `Magic Trackpad 2 を快適に使うトッププレート、ボトムプレート` を使用しています。

### Cherry MX 互換スイッチ を使い、トッププレート、ボトムプレートを組み合わせる

アクリルトッププレート、ボトムプレート 1、ボトムプレート 2 を作成することで、挟み込むことができます。トッププレートと、PCB の間にはスペーサー 3mm を使います。

上から順に挙げると以下のようになります。

1. M2 4mm ネジ
2. トッププレート
3. M2 3mm 両雌ねじスペーサー
4. PCB
5. ボトムプレート 1
6. ボトムプレート 2
7. M2 8mm ネジ
8. ゴム足

アクリルトッププレート、ボトムプレートは以下のファイルを使い、遊舎工房で発注することが可能です。

[デザインファイル Sparrow62_set_Laser_450x300.svg](./additional_plate/Sparrow62_set_Laser_450x300.svg)

[遊舎工房 レーザーカットサービス](https://yushakobo.jp/lasercut/)

その他に必要なものは以下になります。

- M2 4mm ネジ x20
  - [モノタロウ SNZF 精密機器用十字穴付き皿小ねじ(微細ねじ) 寸法 m M1.4(mm)、寸法 l 3mm](https://www.monotaro.com/p/4926/2543/)
  - [遊舎工房 スリムヘッド小ねじ M2 黒](https://yushakobo.jp/shop/a0800b2/)
- M2 8mm ネジ x20
  - [モノタロウ SNZF 精密機器用十字穴付き皿小ねじ(微細ねじ) 寸法 m M1.4(mm)、寸法 l 8mm](https://www.monotaro.com/p/4926/2586/)
  - [遊舎工房 トラス小ねじ M2](https://yushakobo.jp/shop/a0800t2/)
- M2 2mm 両雌ねじスペーサー x20
  - [モノタロウ スペーサー(黄銅スペーサー) ASB-2000E シリーズ(M=2 ピッチ 0.4)](https://www.monotaro.com/p/1111/2858/)
  - [遊舎工房 黄銅スペーサー（丸）M2](https://yushakobo.jp/shop/a0800c2/)
  - [遊舎工房 黄銅スペーサー（六角）M2](https://yushakobo.jp/shop/a0800r2/)
- ゴム足
  - [モノタロウ ソフトクッション 直径 × 高さ 8×2.0(mm)](https://www.monotaro.com/p/4891/2353/)
  - [遊舎工房 ウレタンクッション – 丸型 10mm 6 個入り](https://yushakobo.jp/shop/a0800ur-01-6/)

### Kailh Choc v1/v2 スイッチを使い、トッププレート、ボトムプレートを組み合わせる

正直なところ、Choc スイッチを使うのであれば、PCB にゴム足を直接付けたほうが薄さの上で有利であるため、推奨していません。

上から順に挙げると以下のようになります。

1. M2 8mm ネジ
2. トッププレート
3. PCB
4. ボトムプレート 1
5. ボトムプレート 2
6. M2 ナット
7. ゴム足

アクリルトッププレート、ボトムプレートは以下のファイルを使い、遊舎工房で発注することが可能です。

[デザインファイル Sparrow62_set_Laser_450x300.svg](./additional_plate/Sparrow62_set_Laser_450x300.svg)

[遊舎工房 レーザーカットサービス](https://yushakobo.jp/lasercut/)

その他に必要なものは以下になります。

- M2 10mm ネジ
  - [モノタロウ (+)スリムヘッド小ねじ (ステンレス)(パック品) ねじの呼び M2、長さ 10mm、寸法 H 0.5mm、寸法 D 4mm](https://www.monotaro.com/p/4174/6731/?t.q=M2%20%83l%83W%2010mm)
- M2 ナット
  - [モノタロウ 六角ナット 1 種(ステンレス/ブラック)](https://www.monotaro.com/p/4221/6097/?t.q=%83i%83b%83g%20m2)

ボトムプレート 2 を廃止することで、基本セットと同等の薄さになります。

上から順に挙げると以下のようになります。

1. M2 8mm ネジ
2. トッププレート
3. PCB
4. ボトムプレート 1
5. M2 ナット
6. ゴム足

その他に必要なものは以下になります。

- M2 6mm ネジ（8mmの代わり） x20
  - [モノタロウ SNZF 精密機器用十字穴付き皿小ねじ(微細ねじ) 寸法 m M1.4(mm)、寸法 l 8mm](https://www.monotaro.com/p/4926/2586/)
  - [遊舎工房 トラス小ねじ M2](https://yushakobo.jp/shop/a0800t2/)
- ゴム足
  - [モノタロウ ソフトクッション 直径 × 高さ 8×2.0(mm)](https://www.monotaro.com/p/4891/2353/)
  - [遊舎工房 ウレタンクッション – 丸型 10mm 6 個入り](https://yushakobo.jp/shop/a0800ur-01-6/)

### Magic Trackpad 2 を快適に使うトッププレート、ボトムプレート

片手 4 キーを廃し、そこに Magic Trackpad 2 を置くことができます。

![](img/trackpad.jpeg)

アクリルトッププレート、ボトムプレートは以下のファイルを使い、遊舎工房で発注することが可能です。現在右手を Magic Trackpad 2 で操作するためのキットとして提供しています。（左手用が必要でしたら、作成しますので気軽にお声かけください）

[Sparrow62_Right_Magic_Trackpad_Laser_450x300.svg](./additional_plate/Sparrow62_Right_Magic_Trackpad_Laser_450x300.svg)

[テンプレート 遊舎工房 レーザーカットサービス](https://yushakobo.jp/lasercut/)

他に必要なものは以下になります。

- M2 4mm ネジ x34（表から、トッププレートを貫く。裏から、トラックパッドプレートを貫く）
  - [モノタロウ SNZF 精密機器用十字穴付き皿小ねじ(微細ねじ) 寸法 m M1.4(mm)、寸法 l 3mm](https://www.monotaro.com/p/4926/2543/)
  - [遊舎工房 スリムヘッド小ねじ M2 黒](https://yushakobo.jp/shop/a0800b2/)
- M2 6mm ネジ x20（裏から、ボトムプレート、PCBを貫く）
  - [モノタロウ SNZF 精密機器用十字穴付き皿小ねじ(微細ねじ) 寸法 m M1.4(mm)、寸法 l 6mm](https://www.monotaro.com/p/4926/2762/)
  - [遊舎工房 トラス小ねじ M2](https://yushakobo.jp/shop/a0800t2/)
- M2 3mm 両雌ねじスペーサー x18（PCB-トッププレート間、トッププレートセットには付属）
  - [モノタロウ スペーサー(黄銅スペーサー) ASB-2000E シリーズ(M=2 ピッチ 0.4) 3mm](https://www.monotaro.com/p/1111/2858/)
  - [遊舎工房 黄銅スペーサー（丸）M2](https://yushshakobo.jp/shop/a0800c2/)
  - [遊舎工房 黄銅スペーサー（六角）M2](https://yushakobo.jp/shop/a0800r2/)
- M2 7mm 両雌ねじスペーサー x6
  - [モノタロウ スペーサー(黄銅スペーサー) ARB-2000Eシリーズ(M=2 ピッチ0.4) 7mm)](https://www.monotaro.com/p/1113/3657/?t.attr_f2=M2&t.q=M2%20%83X%83y%81%5B%83T%81%5B)
  - [遊舎工房 黄銅スペーサー（六角）M2](https://yushakobo.jp/shop/a0800r2/)
- M2 5.5mm 両雌ねじスペーサー x1（あったほうが良いが、なくても。PCB、トラックパッドトッププレートを接続。すこし空くが5mmや、4mm+ナットを挟んで5.6mmにすることもできる）
  - [モノタロウ スペーサー(黄銅スペーサー) ARB-2000Eシリーズ(M=2 ピッチ0.4) 5.5mm](https://www.monotaro.com/p/1111/2903/)
- 追加のゴム足
  - [モノタロウ ソフトクッション 直径 × 高さ 8×2.0(mm)](https://www.monotaro.com/p/4891/2353/)
  - [遊舎工房 ウレタンクッション – 丸型 10mm 6 個入り](https://yushakobo.jp/shop/a0800ur-01-6/)

## 販売先

- Sparrow62 自作キーボードキット https://booth.pm/ja/items/2525427
- 半組立済 or 完成品 Sparrow62 自作キーボードキット https://booth.pm/ja/items/2565218
  - 半完成品: はんだ付け済み、キーキャップとキースイッチを付けるだけで完成するもの。別途 TRRS ケーブル、Micro USB ケーブルは必要。
  - 完成品: Kailh Speed Switch Copper、DSA キーキャップが付いた完成品キーボード

## キット以外に必要なもの

以下のものが必要です。

- 電子工作用はんだ及び、はんだ付け工具
- 対応キースイッチ x62
- キースイッチ対応キーキャップ x62
- スイッチ用 PCB ソケット x62 （以下のいづれか）
  - MX 互換スイッチ用 ([遊舎工房](https://yushakobo.jp/shop/a01ps/)、[TALP KEYBOARD](https://talpkeyboard.stores.jp/items/5e02c5405b120c792616bcf9))
  - Kailh Low Profile Choc V1/V2 用 ([遊舎工房](https://yushakobo.jp/shop/a01ps/))
- Micro USB ケーブル x1: Pro Micro と PC の接続用
- TRRS ケーブル、もしくは 3.5mm ステレオミニプラグオーディオケーブル x1 ([遊舎工房](https://yushakobo.jp/shop/trrs_cable/)、[Amazon](https://www.amazon.co.jp/dp/B018FPYC78))
- Pro Micro x2 ([遊舎工房](https://yushakobo.jp/shop/promicro-spring-pinheader/)、[TALP KEYBOARD](https://talpkeyboard.stores.jp/items/5b24504ba6e6ee7ec60063e3))
- Pro Micro 用コンスルー x2 (遊舎工房 Pro Micro に付属、[TALP KEYBOARD](https://talpkeyboard.stores.jp/items/5e056626d790db16e2889233))

### おすすめのもの

- Kailh Low Profile Choc v2 タクタイル（茶）([遊舎工房](https://yushakobo.jp/shop/kailh-choc-v2/)): 非常に薄いタクタイルスイッチです。MX 軸の一般的なキーキャップが使用可能で、薄さをキープしたまま良い打ち心地を得ることができます。
- Kailh Speed Switch Copper（茶）([遊舎工房](https://yushakobo.jp/shop/kailh-speed/): 押下点（押されたと判定される深さ）が 1.1mm と非常に小さいタクタイルスイッチです。そこまで押すことなく入力が軽快にでき、指が痛くなりません。
- DSA キーキャップ （[遊舎工房](https://yushakobo.jp/product-category/keycaps/dsa/)、[TALP KEYBOARD](https://talpkeyboard.stores.jp/?category_id=59be1864b1b6195942000732)）: 非常に薄い、かつ全て同型のキーキャップです
- 見つけてよかったキーキャップ https://www.amazon.co.jp/gp/product/B0852YVT71/

## キット同梱物

キットには以下のものを含んでいます。

- PCB x2 （左右の手の PCB は同じものです）
- ダイオード 1N4148W x62
- TRRS ジャック x2
- タクトスイッチ x2
- ゴム足 x20

トッププレート付属の場合には、以下のものを含んでいます。

- トッププレート x2
- スペーサー M2 3mm x20
- M2 ネジ x40

トッププレートは Cherry MX 互換キースイッチ専用とお考えください。 Kailh Choc V1/V2 の場合キーキャップと干渉したり、高さが高すぎたりします。

## キット同梱物が追加で必要な場合

キットに付属している以上の材料が必要になった場合、PCB 以外は秋月電子通商、または遊舎工房で購入することが可能です。

- TRRS ジャック: [秋月電子通商](https://akizukidenshi.com/catalog/g/gC-06070/)、[遊舎工房](https://yushakobo.jp/shop/a0800tr-01-1/)
- ダイオード: [秋月電子通商](https://akizukidenshi.com/catalog/g/gI-07084/)、[遊舎工房](https://yushakobo.jp/shop/a0800di-02-100/)
- タクトスイッチ: [秋月電子通商](https://akizukidenshi.com/catalog/g/gP-08073/)、[遊舎工房](https://yushakobo.jp/shop/a0800ts-01-1/)、[モノタロウ](https://www.monotaro.com/p/0148/6257/)
- ゴム足: [モノタロウ](https://www.monotaro.com/p/4891/2387/)

## 追加であると良いもの

- はんだこて台 [Amazon](https://www.amazon.co.jp/dp/B0016V7JOC/): やすいものでもあると、机の上が煩雑になりません。
- ハンダ吸い取り線 [Amazon](https://www.amazon.co.jp/dp/B002TKEGRM/): はんだ付け失敗時に取り外しできます。あったほうが心強いです。
- フラックス: はんだ付け失敗時に再びはんだ付けをしやすくするのに塗ります。なくても良いです。
- 逆作用ピンセット [Amazon](https://www.amazon.co.jp/dp/B0036RQR4W/): 手が震えずに効率的にはんだ付けできます。ダイオードは非常に小さい部品なのでこの機会に買いましょう。
- マスキングテープ: ダイオード、ソケットなどの仮どめに使用できます。
- デジタルテスター [Amazon](https://www.amazon.co.jp/dp/B003272E48/): 通電不良時の調査用に使えます。
- ルーペ: ダイオードの方向確認に使えます。スマホのカメラの拡大機能でも代用できます。
- エポキシ系接着剤 [Amazon](https://www.amazon.co.jp/dp/B003SL8CBC/): Pro Micro の MicroUSB 端子のもげ防止に使えます。
- ニッパー [Amazon](https://www.amazon.co.jp/dp/B000ICAOE2/): タクトスイッチの足を切ります。
- ラジオペンチ [Amazon](https://www.amazon.co.jp/dp/B00FB92PJY/): ソケットにスイッチを差し込んだ際、スイッチの端子が曲がることがあります。それを伸ばすのに使います。

## 高さ調整に必要なもの

[詳しくはこちらの高さ調整ガイドを確認ください。](./hight_guide/README.md)

## 手順

### Kailh Choc V2 の場合、足を 1 本切断する

Kailh Choc V2 では銅線の足が 3 つ出ていますが、このうち写真赤丸の 1 本をニッパで切断します。
切断した際に発生する小さな破片にご注意ください。
写真青丸の銅線は切断しないように気をつけてください。

![](img/choc_v2.jpg)

ここできれいに切断すると、安定性が増します。
もし少し残ってぐらついてしまう場合、補助的にトッププレートを使うことで安定させることもできます（ただし、Choc スイッチの下の爪と上の爪までの幅が 1.65mm であるため、完全にははまりません）。
[後からトッププレートが必要となった場合、遊舎工房さんで発注することができます。こちらを確認ください。](https://github.com/74th/sparrow62-buildguide#%E8%BF%BD%E5%8A%A0%E3%81%A7%E3%83%88%E3%83%83%E3%83%97%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%83%9C%E3%83%88%E3%83%A0%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%81%8C%E6%AC%B2%E3%81%97%E3%81%84%E5%A0%B4%E5%90%88)

### Pro Micro にもげ防止加工を実施（お好みで）

Pro Micro の Micro USB 端子は非常にもげやすいものになっています。
これを防止するため、端子に エボキシ系接着剤を塗布します。
誤って端子の中に接着剤が入り込まないように気をつけてください。

![](img/pro_micro_connecter.jpg)

### Pro Micro とピンヘッダをはんだ付けする

ピンヘッダには向きがあります。詳しくは、遊舎工房の解説を確認ださい。

https://yushakobo.zendesk.com/hc/ja/articles/360044233974-%E3%82%B3%E3%83%B3%E3%82%B9%E3%83%AB%E3%83%BC-%E3%82%B9%E3%83%97%E3%83%AA%E3%83%B3%E3%82%B0%E3%83%94%E3%83%B3%E3%83%98%E3%83%83%E3%83%80-%E3%81%AE%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91%E6%96%B9%E3%82%92%E6%95%99%E3%81%88%E3%81%A6%E4%B8%8B%E3%81%95%E3%81%84

Sparrow62 キーボードは Pro Micro を写真の向きで使います。

![](img/pro_micro.jpg)

先に、Pro Micro とピンヘッダを PCB に差し込みます。
その上から、 Pro Micro とピンヘッダのみをはんだづけします。
ピンヘッダと PCB ははんだ付けしないようにします。

Pro Micro は脆弱な部品ため、破損した場合交換が可能となります。

### PCB を左右どちらに使うかを決める

部品によって、実装面が異なります。

- 表面に実装: タクトスイッチ、TRRS ジャック
- 裏面に実装: ダイオード、スイッチソケット

誤って反対面に実装しないように、実装する側に印をつけておくとよいでしょう。

### ダイオードを実装する

ダイオードを向きを気をつけて、はんだ付けします。

実装手順については、サリチル酸さんのツイートの動画が非常に良くできているため、こちらを確認いただくと良いと思います。

https://twitter.com/Salicylic_acid3/status/1296494976319315970
https://twitter.com/Salicylic_acid3/status/1108798243142434816

1. 先に PCB の片側にはんだをつける。
2. つけたハンダを溶かして、ダイオードの片側を付ける
3. ダイオードの向きが間違っていないか、虫眼鏡、もしくはスマホカメラの拡大機能で確認する
4. 反対側の足をはんだ付けする

片面のダイオードが全て同じ向きを向くように設計されています。
ダイオードの片側をはんだ付けした時点で、向きの確認を行い、その後反対側の足のはんだ付けをすると良いです。

**1.先に PCB の片側にはんだをつける**

![](img/diode1.jpg)

**2.つけたハンダを溶かして、ダイオードを片側をはんだ付けする**

![](img/diode2.jpg)

**3.ダイオードの向きを確認する**

![](img/diode4.jpg)

**4.反対側の足をはんだ付けする**

![](img/diode2.jpg)

### スイッチソケットを実装する

スイッチソケットを、ダイオードと同じ面に、ハンダ付けします。

実装手順について、こちらもサリチル酸さんのツイートの動画がよくできているため、こちらを確認いただくのが良いと思います。

https://twitter.com/Salicylic_acid3/status/1310253635255717889

私の場合は以下のようにしています。

1. 先に PCB の両側の端子にハンダをつける
2. ソケットを置き、片側を端子の上からハンダごてを当てて、先につけたハンダを溶かして、ソケットの端子と PCB を接着させる。この時、ソケットを上から押してある程度密着させる。
3. 反対側の端子の上からはんだごてを押さえつけるようにあてて、ソケットの端子と基盤を密着させる。このときもソケットを押す。
4. 再度反対側の端子にはんだごてを当てつつ、ソケットを押して、端子と基盤を密着させる。

**1.先に PCB の両側の端子にハンダをつける**

![](img/socket1.jpg)

**2.ソケットを置き、ハンダを溶かしながら押す**

![](img/socket2.jpg)

**3.反対側も同様にする**

![](img/socket3.jpg)

**4.密着するまでくりかえす**

![](img/socket4.jpg)

### タクトスイッチを実装する

タクトスイッチは、**ダイオードとは異なる面に** 実装します。

足が裏面に出るため、はんだ付けを行う面は **ダイオードと同じ面** です。

1. 先にタクトスイッチを差し込み、マスキングテープで固定します。
2. 裏返して、足をはんだ付けします。
3. 余分な足をニッパで切ります

**タクトスイッチ**

![](img/tact_switch.jpg)

### TRRS ジャックを実装する

TRRS ジャックは、**ダイオードとは異なる面に** 実装します。

足が裏面に出るため、はんだ付けを行う面は **ダイオードと同じ面** です。

1. 先に TRRS ジャックを差し込み、マスキングテープで固定します。
2. 裏返して、足をはんだ付けします。
3. 余分な足をニッパで切ります

**TRRS コネクタ**

![](img/trrs.jpg)

### キースイッチを差し込む

キースイッチをソケットに差し込みます。キーキャップはまだしません。

### Pro Micro にファームウェアを書き込む

ファームウェアには、[QMK Firmware](https://docs.qmk.fm/) を使います。

デフォルトのキーマップで良い場合、QMK Toolbox でファームウェアを書き込めば完了です。

キーマップのカスタマイズには、VIA を使うと GUI で変更できます。
更に高度なカスタ合図を行う場合、QMK Firmware のビルド環境を整える必要があります。

#### QMK Toolbox を使ってデフォルトのファームウェアを書き込む

以下のキーマップを、default のファームウェアとして提供しています。

- [Download sparrow62_default.hex](https://github.com/74th/sparrow62-buildguide/raw/master/sparrow62_default.hex)

レイヤ 1

![](./img/keymap_default_layer1.png)

レイヤ 2（レイヤ 1 の`MO(1)`のキーと同時に押すと、動作する）

![](./img/keymap_default_layer2.png)

こちらを [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases) を使って書き込むことができます。

QMK Toolbox の使い方は[サリチル酸さんの記事](https://salicylic-acid3.hatenablog.com/entry/qmk-toolbox)が詳しいため、こちらを確認ください。

左右のキーボードの両方に書き込む必要があります。

#### VIA を使ってキーマップを変更する

GUI でキーマップを変更できる [VIA](https://caniusevia.com/) というツールがあります。

VIA を使うには、VIA のファームウェアを書き込む必要があります。以下からダウンロードし、[QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases)などを使って書き込んでください。

- [Download sparrow62_via.hex](https://github.com/74th/sparrow62-buildguide/raw/master/sparrow62_via.hex)

VIA には、まだ Sparrow62 の設定がマージされていないため、VIA を起動した後に、以下の手順で設定を追加します。

1. **SETTINGS タブ** を開き、**Show Design tab** を有効化する。
2. **DESIGN タブ** を開き、**Load Draft Definition** から[この JSON ファイル(via_sparrow62.json)](https://github.com/74th/sparrow62-buildguide/raw/master/via_sparrow62.json) を読み込ませる。
3. キーボードを接続し、**CONFIGURE タブ**を開く

VIA の使い方は[サリチル酸さんのブログ](https://salicylic-acid3.hatenablog.com/entry/via-manual)が詳しいので、こちら参照ください。

#### 更にカスタマイズするため、QMK Firmware のビルド環境を整える

QMK Firmware のセットアップ手順（[公式英語](https://docs.qmk.fm/#/newbs_getting_started)、[有志日本語](https://github.com/shelaf/qmk_firmware/blob/master/docs/ja/newbs_getting_started.md)）に従い、インストールします。

Ubuntu を使用している場合には、ModemManager が邪魔をすることがあるので、`sudo systemctl stop ModemManager.service`を実行いておくと有効です。

デフォルトのキーマップをインストールするには、PC と Pro Micro を USB ケーブルで接続し、以下を実行します。

```
qmk flash -kb sparrow62 -km default
```

`Detecting USB port, reset your controller now...`と表示されたところで、キーボードのタクトスイッチ（リセット）を押します。
この Firmware の書き込みを、左右 2 つの Pro Micro で両方とも行います。

この default のキーマップは以下のようになっています。 `MO(_FN)`のキーを押すと、キーレイヤが下の`[_FN]`のものに変わり、F1-12 キーや、矢印キーとして動作させることができます。

![](img/default_keymap.png)

新しいキーマップを作成する場合には、以下のように実行します（nnyn が新しいキーマップ名）

```
qmk new-keymap -kb sparrow62 -km nnyn
```

キーマップの設定する C のソースが `~/qmk_firmware/keyboards/sparrow62/keymaps/nnyn/keymap.c` にできます。
こちらを変更して、以下のコマンドで Firmware を書き込みます。

```
qmk flash -kb sparrow62 -km nnyn
```

詳しいファームウェアの実装方法は、公式のドキュメントや Qiita の記事を参照ください。

- [Keymap Overview](https://docs.qmk.fm/#/keymap)
- [はじめての QMK キーマップ編集](https://qiita.com/marksard/items/9317949ce1da327f7436)

### キースイッチのテストをする

QMK Continuator のキーテストを開きます。

https://config.qmk.fm/#/test

キースイッチを押し、キーレイアウトの通りに動作するかを確認します。

### 動作しないキーがある場合

#### 1 キーのみ動作しない場合

まず、キースイッチの足が曲がっていないか確認してください。

左手用のキーの場合、以下の同じ色の部分がつながっています。それぞれテスターなどで疎通しているか確認ください。

![](img/left_hand_debug.jpg)

右手用のキーの場合、以下の同じ色の部分がつながっています。それぞれテスターなどで疎通しているか確認ください。

![](img/right_hand_debug.jpg)

#### 縦一列、横一列が動作しない場合

青丸が COL のラインとなっており、そのまま Pro Micro の COL0-6 につながっています。緑丸が ROW のラインとなっており、そのまま Pro Micro の ROW0-4 につながっています。
Pro Micro の接続を確認ください。

## 追加でトッププレート、ボトムプレートが欲しい場合

追加でトッププレート、ボトムプレートが入り用の場合には、[遊舎工房さんのレーザーカットサービス](https://yushakobo.jp/lasercut/)で利用可能なデータを提供していますので、ご自身で発注ください。
また、データで問題があった場合には、私まで問い合わせください。

- [トッププレート A4 Sparrow62_top_Laser_A4.svg](additional_plate/Sparrow62_top_Laser_A4.svg)
- [ボトムプレート A4 Sparrow62_bottom_Laser_A4.svg](additional_plate/Sparrow62_bottom_Laser_A4.svg)
- [ボトムプレート 450x300 Sparrow62_set_Laser_450x300.svg](additional_plate/Sparrow62_set_Laser_450x300.svg)

## 不明点がある場合

不明点がある場合、作成にあたり相談したいことがある場合には、私のところまでお気軽に問い合わせください。

- Twitter: @74th
- Mail: site@74th.tech
