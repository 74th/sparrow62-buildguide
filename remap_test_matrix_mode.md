# RemapのTest Matrix modeを使ったキーマトリックスのテスト方法

Remap には、キーマトリックスをテストする機能があります。
こちらを使うことで、各キーのダイオードやソケットの実装が正常かどうか確認することができます。

それにはまず、VIA、Remap対応のファームウェアをキーボードに書き込みます。Sparrow60C、SparrowDialにおいてはあらかじめ対応ファームウェアが書き込まれています。

まず、RemapのWebサイトを開き、「CUSTOMIZE YOUR KEYBOARD」を押します。

https://remap-keys.app/

![](./img/common/remap_top.png)

キーボードの接続が表示されるため、「+ KEYBOARD」を押します。

![](./img/common/remap_configure_top.png)

既にUSB接続している場合には、左上のメニューから追加を行ってください。

![](./img/common/remap_add_connected_keyboard.png)

キーマップの設定画面になりましたら、図のメニューから「Test Matrix mode」を選んでください。

![](./img/common/remap_open_test_matrix.png)

この画面では、キーを押すとこのように色が変わって表示されます。この状態ですべてのキーが動作することを確認してください。

![](./img/common/remap_test_matrix.png)

キーが押されるとスイッチの2つのピンが通電した状態になります。スイッチを実際に刺さなくても、「金属ピンセットでソケットの2つの金属部分に触れる」ことや「ジャンパワイヤーでソケットの2つうの金属部分に触れること」で通電させることもできます。
