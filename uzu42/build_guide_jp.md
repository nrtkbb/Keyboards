# uzu42ビルドガイド

自作キーボードキット [uzu42](https://nrtkbb.booth.pm/items/1583207) のビルドガイドです。  
組み立てる際は、このビルドガイドを先に読んで理解してから、工具を揃え、環境構築して、実際に作業を行ってください。

## 準備

### 同梱品の確認

1. ProMicro：2個
1. コンスルー：4個
1. TRRSジャック：2個
1. タクトスイッチ：2個
1. スペーサー（6.5mm）：8本
1. スペーサー（8mm）：4本
1. ネジ：24本
1. クッションゴム：8個
1. 表面実装ダイオード：43個（予備1個）
1. MX互換スイッチ用PCBソケット：42個
1. PCB：1枚
1. トッププレート：2枚
1. ボトムプレート：2枚
1. ProMicro保護プレート：2枚
1. LED実装用治具（通称いもけんぴ）：21個

| ![parts list](./img/00_parts/parts_14.jpg) |  ![parts list](./img/00_parts/parts_13.jpg) | ![parts list](./img/00_parts/parts_11.jpg) | ![parts list](./img/00_parts/parts_9.jpg) |
| ---- | ---- | ---- | ---- |
| ProMicro | コンスルー | TRRSジャック | タクトスイッチ |
| ![parts list](./img/00_parts/parts_6.jpg) | ![parts list](./img/00_parts/parts_7.jpg) | ![parts list](./img/00_parts/parts_10.jpg) | ![parts list](./img/00_parts/parts_8.jpg) |
| スペーサー | ネジ | クッションゴム | 表面実装ダイオード |
| ![parts list](./img/00_parts/parts_16.jpg) | ![parts list](./img/00_parts/parts_4.jpg) | ![parts list](./img/00_parts/parts_15.jpg) | ![parts list](./img/00_parts/parts_5.jpg) |
| MX互換スイッチ用PCBソケット | PCB（左）<br>トッププレート（右上）<br>ボトムプレート（右下） | ProMicro保護プレート | LED実装用治具（通称いもけんぴ） |

### 用意するもの

1. MX互換スイッチ：42個
    - [Switches | 遊舎工房](https://yushakobo.jp/product-category/switches/)
    - [TALP KEYBOARD](https://talpkeyboard.stores.jp/?category_id=59cf8860ed05e668db003f5d)
1. 1Uキーキャップ：42個
    - [Keycaps | 遊舎工房](https://yushakobo.jp/product-category/keycaps/)
    - [TALP KEYBOARD](https://talpkeyboard.stores.jp/?category_id=59be183f428f2d49120007b1)
    - [ゆかりキーボードファクトリー](https://eucalyn.shop/)
    - [KBDFans](https://kbdfans.com/)
    - [WASD Keyboards Custom Mechanical Keyboards and Cherry MX Keycaps](http://www.wasdkeyboards.com/)
    - [PIMP MY KEYBOARD](https://pimpmykeyboard.com/)
    - [1UP Keyboards](https://www.1upkeyboards.com/product-category/keycaps/)
    - [NovelKeys__](https://novelkeys.xyz/)
    - uzu42 へのおすすめキーキャップ
        - PIMP MY KEYBOARD の DSA 1 Space(Pack Of 10) で RED(RAR) をセレクトして Quantity を 5 にして購入することです！
        - ショップURL: https://pimpmykeyboard.com/dsa-1-space-pack-of-10/
        - 参考URL: https://twitter.com/nrtkbb/status/1139984729921339392
    - uzu42 へのおすすめキーキャップ2
        - ゆかりキーボードファクトリー様にて uzu42 専用のキーキャップセットを販売してくださっています！
        - オプションから **uzu42セット** をお選びください
        - ショップURL: https://eucalyn.shop/shop/keycaps/taihao-abs-red
        - 参考URL: https://twitter.com/nrtkbb/status/1225423293454241792
1. TRS or TRRSケーブル：1本
    - [Auxケーブル 0.5M オーディオケーブル 赤 | Amazon](https://www.amazon.co.jp/gp/product/B07N36N7YW)
1. OLEDモジュール（ピンソケット付き）：2個（オプション）
    - [OLEDモジュール | 遊舎工房](https://yushakobo.jp/shop/oled/) ※ピンソケット付きを選択してください
1. SK6812MINI：54個（オプション）
    - [SK6812MINI 35個入り | 遊舎工房](https://yushakobo.jp/shop/sk6812mini-35/) ※54個以上になるようにご購入ください
1. USB-A to Micro-USBケーブル：1本
    - [USB micro ケーブル 赤 | Amazon](https://www.amazon.co.jp/s?k=usb+micro+ケーブル+赤&__mk_ja_JP=カタカナ)
    - [USB Cables | ZAP!CABLES](https://zapcables.com/usb-cables/)


## 工具

自分の家で作業される予定の方は以下のページを参考に工具を用意してください。  
一度組み立てが完了しても、初めのうちはちょっと持ち運ぶだけで不具合が出ることもありました。  
自分の自作キーボードを使い続けるにはどうしてもメンテナンスが必要です。  
しっかりとした工具を揃えることで備えましょう。

- [Helix キーボードキットの製作に必要な工具メモ | gist.github.com](https://gist.github.com/mtei/6957107a676ddfa85bde0ae41f8fa849)
- [第8回「自作キーボードのつくりかた #2」組み立てる道具とはんだ付け編 | Youtube](https://youtu.be/LOC53FeU-QM)
- [自作キーボードを作るために必要なもの | 自作キーボード温泉街の歩き方](https://salicylic-acid3.hatenablog.com/entry/2018/11/24/%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89%E3%82%92%E4%BD%9C%E3%82%8B%E3%81%9F%E3%82%81%E3%81%AB%E5%BF%85%E8%A6%81%E3%81%AA%E3%82%82%E3%81%AE#%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89%E3%81%A7%E5%BF%85%E8%A6%81%E3%81%AA%E3%82%82%E3%81%AE)
- [自作キーボードの組み立てに使っている工具 | yfuku blog](https://blog.yfuku.com/entry/keybord_build_tool)


### 自分の使ってる工具

- はんだ [goot リール巻はんだ 100ｇ SE-06008](https://www.amazon.co.jp/dp/B001PR1L2S)
- はんだ吸い取り線 [goot はんだ吸取り線 CP-3015](https://www.amazon.co.jp/dp/B001PR1KPQ)
- はんだこて [白光 ダイヤル式温度制御はんだこて FX600](https://www.amazon.co.jp/dp/B006MQD7M4)
- こて台 [白光(HAKKO) こて台 633-01](https://www.amazon.co.jp/dp/B000TGNWCS)
- テスター [Crenova デジタルマルチメーター 電圧・電流・周波数・抵抗・導通測定テスター](https://www.amazon.co.jp/dp/B00KXX2OYY)
  - テスターは安いので良いのでこっちにしておけばよかった→ [デジタルテスター　マニュアルレンジ　ｈＦＥ測定機能付](http://akizukidenshi.com/catalog/g/gM-12542/)
- ふつうの丈夫なピンセット [タミヤ 精密ピンセット （ツル首タイプ） #74047](https://www.amazon.co.jp/dp/B000J46WZY)
- 逆作用ピンセット [goot 逆作用ピンセット 小 TS-16](https://www.amazon.co.jp/dp/B0036RQR4W)
- ニッパー [goot ニッパー YN-10](https://www.amazon.co.jp/dp/B001VB37RK/)
- マスキングテープ [日東電工 マスキングテープ No.720 15mm×18m J7520](https://www.amazon.co.jp/dp/B005JWNDT4)
- エポキシ系接着剤 [セメダイン 30分硬化型エポキシ系接着剤 ハイスーパー30 6gセット箱 CA-189](https://www.amazon.co.jp/dp/B003SL8CBC)
- フラックス [ホーザン(HOZAN) フラックス 鉛フリーハンダ対応 便利なハケ付きキャップ付 容量30mL H-722](https://www.amazon.co.jp/dp/B000TGJTUW)
- フラックスクリーナー [サンハヤト フラックスクリーナー 15ml FL-L15](https://www.amazon.co.jp/dp/B01GROTPEE)
- ツールクリッパー [TSK ツールクリッパー TX303](https://www.amazon.co.jp/dp/B003SBS4EM)
- キムワイプ [日本製紙クレシア キムワイプ S-200 mini 62015 1個入](https://www.amazon.co.jp/dp/B00CWA23P6)
- 10倍ルーペ [PEAK ルーペ10× 1961 東海産業](https://www.amazon.co.jp/dp/B00VJV37GI)
- 棒ヤスリ [タミヤ クラフトツールシリーズ No.104 ベーシックヤスリセット (細目 ダブルカット) 74104](https://www.amazon.co.jp/dp/B00CE3L96K)
- 作業マット [iMagitek 断熱ワーキングマット耐熱500℃](https://www.amazon.co.jp/gp/product/B07BPJVQQ9)

あと家にあるものでも良いので、爪楊枝と、カッターマットがあれば用意してください。  
オプションのLEDのデバッグには両端がオスのジャンパ線が1本あるととてもはかどります。


## 組み立て手順の確認

1. 動画で確認
1. ProMicro へのファームウェアの書き込み
1. ProMicro のモゲ対策
1. PCB の分割
1. ProMicro へコンスルーのはんだ付け
1. （オプション）LED のはんだ付け
1. ダイオードのはんだ付け
1. タクトスイッチ、TRRS ジャックのはんだ付け
1. ケーブルを繋いで動作確認
1. ソケットのはんだ付け
1. （オプション）OLEDのはんだ付け
1. ネジ止め
1. ゴム足の接着
1. スイッチとキーキャップの装着
1. 完成！

一つずつ、詳しく見ていきます。


### 動画で確認

[![自作キーボード作ってみた uzu42編 in 遊舎工房](https://i.ytimg.com/vi/h2fBtLVtGxc/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLBfOEK7seJuJ_9tmNCbFyDkxOJHLQ)](https://www.youtube.com/watch?v=h2fBtLVtGxc)  
[Daihukuさん](https://twitter.com/Daihuku0015)がYoutubeに[自作キーボード作ってみた uzu42編 in 遊舎工房](https://www.youtube.com/watch?v=h2fBtLVtGxc)というビルドログを公開してくださっています。  
とても丁寧な説明で、初心者が陥りがちなポイントについて詳しくご説明くださっているので、ぜひ初めにご確認いただくことをおすすめします。


#### （初心者向け）はんだ付け動画

はんだ付けは技術力が必要な作業です。  
もりもりにはんだが付いているだけだと不具合の原因になります。  
また、完成までに 444 箇所もはんだ付けするため、はじめは数時間の作業になります。  
動画を見る時間は40分以内のため作業の短縮になると思います。

そのため、はじめての方は少しでも学習されることを強くおすすめします。


はんだ付けの基本動作  
https://youtu.be/ZA-ehWjRfYM

ProMicro、タクトスイッチ、TRRSジャックなどを実装する際にスルーホールをはんだ付けするため、こちらの動画で学習すると効率的です。  
https://youtu.be/oq3Q3n57-B0

表面実装ダイオード、LEDなどをはんだ付けする方法は、こちらの動画で学習すると効率的でした。  
https://youtu.be/vqKKElJ1vw0


### ProMicro へのファームウェアの書き込み

ファームウェアを準備するための手順はこちらに記述されています。  
https://docs.qmk.fm/#/newbs_getting_started  

uzu42 は QMK Configurator や QMK Toolbox や VIA には対応していないため、上記URLを参考にビルド環境の構築を行ってください。  
具体的には `qmk` をインストールし `qmk setup` を行ってください。

正しく qmk_firmware の環境が構築できたら、先に ProMicro にファームウェアを書き込み、正常に書き込める個体かどうかを確認しておきます。  
```
qmk compile -kb uzu42 -kb default
```
とするとビルドが実行されます。
```
$ qmk compile -kb uzu42 -kb default
INFO Compiling keymap with make uzu42:default


QMK Firmware 0.9.46
Making uzu42/rev1 with keymap default

avr-gcc.exe (GCC) 8.3.0
Copyright (C) 2018 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

Compiling: keyboards/uzu42/uzu42.c                                                                  [OK]
Compiling: keyboards/uzu42/rev1/rev1.c                                                              [OK]
Compiling: keyboards/uzu42/keymaps/default/keymap.c                                                 [OK]
Compiling: quantum/quantum.c                                                                        [OK]
Compiling: quantum/keymap_common.c                                                                  [OK]
Compiling: quantum/keycode_config.c                                                                 [OK]
Compiling: quantum/matrix_common.c                                                                  [OK]
Compiling: quantum/split_common/matrix.c                                                            [OK]
Compiling: quantum/debounce/sym_g.c                                                                 [OK]
Compiling: quantum/split_common/split_util.c                                                        [OK]
Compiling: quantum/split_common/transport.c                                                         [OK]
Compiling: quantum/color.c                                                                          [OK]
Compiling: quantum/rgblight.c                                                                       [OK]
Compiling: quantum/process_keycode/process_rgb.c                                                    [OK]
Compiling: drivers/avr/ws2812.c                                                                     [OK]
Compiling: quantum/led_tables.c                                                                     [OK]
Compiling: quantum/process_keycode/process_space_cadet.c                                            [OK]
Compiling: quantum/process_keycode/process_magic.c                                                  [OK]
Compiling: quantum/process_keycode/process_grave_esc.c                                              [OK]
Compiling: drivers/avr/i2c_master.c                                                                 [OK]
Archiving: .build/obj_uzu42_rev1_default/i2c_master.o                                               [OK]
Compiling: drivers/avr/i2c_slave.c                                                                  [OK]
Archiving: .build/obj_uzu42_rev1_default/i2c_slave.o                                                [OK]
Compiling: drivers/avr/serial.c                                                                     [OK]
Archiving: .build/obj_uzu42_rev1_default/serial.o                                                   [OK]
Compiling: tmk_core/common/host.c                                                                   [OK]
Compiling: tmk_core/common/keyboard.c                                                               [OK]
Compiling: tmk_core/common/action.c                                                                 [OK]
Compiling: tmk_core/common/action_tapping.c                                                         [OK]
Compiling: tmk_core/common/action_macro.c                                                           [OK]
Compiling: tmk_core/common/action_layer.c                                                           [OK]
Compiling: tmk_core/common/action_util.c                                                            [OK]
Compiling: tmk_core/common/print.c                                                                  [OK]
Compiling: tmk_core/common/debug.c                                                                  [OK]
Compiling: tmk_core/common/sendchar_null.c                                                          [OK]
Compiling: tmk_core/common/util.c                                                                   [OK]
Compiling: tmk_core/common/eeconfig.c                                                               [OK]
Compiling: tmk_core/common/report.c                                                                 [OK]
Compiling: tmk_core/common/avr/suspend.c                                                            [OK]
Compiling: tmk_core/common/avr/timer.c                                                              [OK]
Compiling: tmk_core/common/avr/bootloader.c                                                         [OK]
Assembling: tmk_core/common/avr/xprintf.S                                                           [OK]
Compiling: tmk_core/common/magic.c                                                                  [OK]
Compiling: tmk_core/protocol/lufa/lufa.c                                                            [OK]
Compiling: tmk_core/protocol/usb_descriptor.c                                                       [OK]
Compiling: tmk_core/protocol/lufa/outputselect.c                                                    [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Class/Common/HIDParser.c                                       [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/AVR8/Device_AVR8.c                                        [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/AVR8/EndpointStream_AVR8.c                                [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/AVR8/Endpoint_AVR8.c                                      [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/AVR8/Host_AVR8.c                                          [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/AVR8/PipeStream_AVR8.c                                    [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/AVR8/Pipe_AVR8.c                                          [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/AVR8/USBController_AVR8.c                                 [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/AVR8/USBInterrupt_AVR8.c                                  [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/ConfigDescriptors.c                                       [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/DeviceStandardReq.c                                       [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/Events.c                                                  [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/HostStandardReq.c                                         [OK]
Compiling: lib/lufa/LUFA/Drivers/USB/Core/USBTask.c                                                 [OK]
Linking: .build/uzu42_rev1_default.elf                                                              [OK]
Creating load file for flashing: .build/uzu42_rev1_default.hex                                      [OK]
Copying uzu42_rev1_default.hex to qmk_firmware folder                                               [OK]
Checking file size of uzu42_rev1_default.hex                                                        [OK]
```
と表示されればビルドは正しく行えています。  
書き込みは、
```
qmk flash -kb uzu42 -kb default
```
というコマンドを実行します。  
すると、以下のようになります。
```
$ qmk flash -kb uzu42 -kb default
INFO Compiling keymap with make uzu42:default:flash


QMK Firmware 0.9.46
Making uzu42/rev1 with keymap default and target flash

avr-gcc.exe (GCC) 8.3.0
Copyright (C) 2018 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

Size before:
   text    data     bss     dec     hex filename
      0   20064       0   20064    4e60 .build/uzu42_rev1_default.hex

Copying uzu42_rev1_default.hex to qmk_firmware folder                                               [OK]
Checking file size of uzu42_rev1_default.hex                                                        [OK]
 * The firmware size is fine - 20064/28672 (69%, 8608 bytes free)
Detecting USB port, reset your controller now.
```
この時、USBでPCに接続している ProMicro の RST と GND をピンセットなどで両方触れてショートさせることで実際に書き込みが開始されます。  

| ![firmware](./img/01_firmware_test/firmware_test_1.jpg) | ![firmware](./img/01_firmware_test/firmware_test_2.jpg) | ![firmware](./img/01_firmware_test/firmware_test_3.jpg) |
| ---- | ---- | ---- |
| PC に ProMicro を接続します | PC で now... と表示されたら、写真の下の左から2番めと3番めの穴に同時に一瞬だけピンセットを当てます。正しく当てると ProMicro の光り方が変わります | すると書き込みが行われます。成功してから PC に ProMicro を接続し直すと 光り方が変わります |

上手くいくと、
```
Device /dev/ttyS12 has appeared; assuming it is the controller.
Remapped MSYS2 USB port to COM13

Connecting to programmer: .
Found programmer: Id = "CATERIN"; type = S
    Software Version = 1.0; No Hardware Version given.
Programmer supports auto addr increment.
Programmer supports buffered memory access with buffersize=128 bytes.

Programmer supports the following devices:
    Device code: 0x44

avrdude.exe: AVR device initialized and ready to accept instructions

Reading | ################################################## | 100% 0.00s

avrdude.exe: Device signature = 0x1e9587 (probably m32u4)
avrdude.exe: NOTE: "flash" memory has been specified, an erase cycle will be performed
             To disable this feature, specify the -D option.
avrdude.exe: erasing chip
avrdude.exe: reading input file ".build/uzu42_rev1_default.hex"
avrdude.exe: input file .build/uzu42_rev1_default.hex auto detected as Intel Hex
avrdude.exe: writing flash (20064 bytes):

Writing | ################################################## | 100% 1.52s

avrdude.exe: 20064 bytes of flash written
avrdude.exe: verifying flash memory against .build/uzu42_rev1_default.hex:
avrdude.exe: load data flash data from input file .build/uzu42_rev1_default.hex:
avrdude.exe: input file .build/uzu42_rev1_default.hex auto detected as Intel Hex
avrdude.exe: input file .build/uzu42_rev1_default.hex contains 20064 bytes
avrdude.exe: reading on-chip flash data:

Reading | ################################################## | 100% 0.19s

avrdude.exe: verifying ...
avrdude.exe: 20064 bytes of flash verified

avrdude.exe done.  Thank you.


```
と表示されて完了します。  
完了した際に ProMicro の赤い LED がつきっぱなしになるのが気になる場合は、一度 USB ケーブルを抜き差しすると赤い LED が消えます。  
上記のように書き込みが出来れば少なくとも書き込みに対して検品ができたことになります。  



### ProMicro のモゲ対策

ProMicro のもげ対策を行います。  
ProMicro の USB を挿す部分はとても脆くなっており、抜き差ししていると簡単にもげてしまいます。  
そこでモゲ対策が必要です。  


| ![moge](./img/02_moge/moge_1.jpg) | ![moge](./img/02_moge/moge_2.jpg) |
| ---- | ---- |
| ProMicro を袋から取り出し | ProMicro の入っていた袋にエポキシ樹脂を出し |
| ![moge](./img/02_moge/moge_3.jpg) | ![moge](./img/02_moge/moge_4.jpg) |
| 爪楊枝の頭で混ぜます | 爪楊枝の頭に適量載せて塗っていきます |
| ![moge](./img/02_moge/moge_5.jpg) | ![moge](./img/02_moge/moge_6.jpg) |
| USBを刺す金属部分の周りに塗ります<br>金属部分の横の穴から入らないように注意して | 盛り上げることなくはんだ付けのようにフィレットを作ると良いです。金属部分の上には盛らないようにします |
| ![moge](./img/02_moge/moge_7.jpg) | ![moge](./img/02_moge/moge_8.jpg) |
| 基板から飛び出してる裏側にも塗ります | このぐらいの範囲に付けていけば頑丈になります |

注意する点は3つ

#### 盛りすぎないこと
盛りすぎてUSBが刺さる金属部分より盛ったエポキシ樹脂の山が高くなると後々はまらなくなります。

#### 金属部分の横の穴
金属部分の横には穴が空いています。ここにエポキシ樹脂が入り込むと USB が刺さらなくなります。

#### スルーホールまで盛らないこと
両脇のスルーホール（両脇にいっぱい空いてる穴）の近くまで盛ってしまうとコンスルーが刺さらなくなります。穴の端から1mm程度は避けて盛るようにしましょう。

エポキシ樹脂は、固まる前ならキムワイプなどでかんたんに拭えますので根気よく量を調整しましょう。  
きちんと盛れたら、一旦放置してエポキシ樹脂が固まるのを待ちます。


### PCBの分割

PCBを2つに分割します。カッターなどで切り目を入れてから折り、断面をヤスリがけします。

| ![pcb](./img/03_pcb/pcb_1.jpg) | ![pcb](./img/03_pcb/pcb_2.jpg) |
| ---- | ---- |
| カッターと定規とPCBをカッターマットに置きます | 定規にカッターをあてながら10〜20回ほど切り込みを入れます |
| ![pcb](./img/03_pcb/pcb_3.jpg) | ![pcb](./img/03_pcb/pcb_4.jpg) |
| 途中まで切り込みが入ったら手で折ると簡単に分割できます | 反対側も切り込みを入れます |
| ![pcb](./img/03_pcb/pcb_5.jpg) | ![pcb](./img/03_pcb/pcb_6.jpg) |
| ここは細かいのでペンチなどでつまんで | 折ります |
| ![pcb](./img/03_pcb/pcb_7.jpg) | ![pcb](./img/03_pcb/pcb_8.jpg) |
| 折った後の断面はヤスリで整えます | 整えました |

定規をあてずにカッターで切り込みを入れようとして、一箇所カッターがズレて切ってしまいました。  
皆さんはそうならないように必ず定規をあててカッターを使われることをおすすめします。


### ProMicro へコンスルーのはんだ付け

ProMicro に付けたエポキシ樹脂が固まっていたら ProMicro にコンスルーをはんだ付けします。  

まず、コンスルーには向きがあります。  
黒い樹脂の部分に穴が空いてる面と、穴がなく真っ黒な面です。  
また、穴が空いている面は、穴が端に近い方と長い方とがあります。  

ProMicro にコンスルーを刺す時は、穴が開いてる面を揃え、穴が端に近い方をProMicroに刺して利用します。  
向きを間違えるとコンスルーが壊れることがあったり、接触不良になることがあります。

| ![promicro](./img/04_promicro/promicro_1.jpg) | ![promicro](./img/04_promicro/promicro_2.jpg) |
| ---- | ---- |
| コンスルーは表（穴が開いてる）と裏（穴が空いていない）があり、上下（穴が近い方と遠い方）とがあります | 穴が開いてる面を揃え、穴が端に近い方をProMicroに刺して利用します |
|![promicro](./img/04_promicro/promicro_3.jpg) | ![promicro](./img/04_promicro/promicro_4.jpg) |
| 裏から見ると両方とも穴が空いていません | ProMicro にコンスルーを刺したら PCB にはめます |

コンスルーを ProMicro にはんだ付けする時は PCB にはめた状態で行います。  
そうするとコンスルーが傾いたままになってしまうミスが発生しづらいです。

| ![promicro](./img/04_promicro/promicro_5.jpg) | ![promicro](./img/04_promicro/promicro_6.jpg) |
| ---- | ---- |
| はんだ付けしました。一方向から見たら良いように見えましたが、、 | 上から確認すると写真上の 3 のスルーホールは反対側にはんだが回っていないことを発見しました。はんだ付け後はいろんな角度から見て確認しましょう |


### （オプション）LEDのはんだ付け


こちらはオプションですが「低いものからはんだ付けする」の原則に従い LED を用意されている方は、はじめに行います。  

**注意**  
SK6812MINI はとても熱に弱いです。  
はんだこての設定温度を220℃～270℃ぐらいにして、あまり長時間はんだこてを当てずに素早くはんだ付けを行わないと壊れます。  
4箇所のはんだ付けはいっぺんに行わず、2箇所ずつはんだ付けし、冷ましながら行います。  
いっぺんにすべての LED をはんだ付けしてから確認するよりも、一つ～数個ずつはんだ付けしてすぐ LED TEST で確認するのがおすすめです。（LED TESTの方法は後述します）  
注意終わり。

はじめに、同梱されているアクリル片（通称：芋けんぴ）を LED のための穴に固定します。  
芋けんぴは LED が穴の丁度いい位置に浮かせるための治具になります。  

| ![led](./img/05_led/led_1.jpg) | ![led](./img/05_led/led_14.jpg) |
| ---- | ---- |
| 芋けんぴの突起部分を PCB のシルクが描いてない面からあてて | 一つずつマスキングテープで固定します |
| ![led](./img/05_led/led_2.jpg) | ![led](./img/05_led/led_4.jpg) |
| LED を試しに載せてみます | すると右の LED のように穴が加工誤差により小さすぎる場合は PCB の表面と LED の表面に段差ができます |
| ![led](./img/05_led/led_3.jpg) |  |
| そんな時は穴を少しだけ削ります<br>LED との段差が多少できていても、はんだをブリッジしてあげれば一応は機能するのでこの辺の作業は好みです | |

LED は ProMicro の LED パッドを出発点にして LED から LED に数珠つなぎにつながっています。  

| ![led](./img/05_led/led_15_annotation.jpg) | ![led](./img/05_led/led_17_annotation.jpg) |
| ---- | ---- |
| 左上の大きい矢印が出発点で 1～6 番までは裏面 Underglow が光り（水色の丸）、7～27 番では表面 Backlight が光る（緑色の丸）ようになります | LED の4つのパッドは電源用の VDD と GND の他に DIN（control Data signal INput）と DOUT（control Data signal OUTput）とがあります。ProMicro の LED ピンから出た線が1つ目の LED の DIN に繋がり、1つ目の LED の DOUT から出た線が2つ目の LED の DIN につながることでデータ（光り方の情報）がすべての LED に伝搬していきます |
| ![led](./img/05_led/led_5.jpg) | ![led](./img/05_led/led_6.jpg) |
| LED の VDD のパッドが PCB の白枠の付いたパッドに来るようにはんだ付けします | Underglow の場合は VDD のパッドにはんだを盛ります |
| ![led](./img/05_led/led_7.jpg) | ![led](./img/05_led/led_9.jpg) |
| 逆作用ピンセットで LED をつまみながら上に載せ、270度に設定したはんだこてで、盛ったはんだを少し熱します | うまくはんだが溶けてくれたら LED を上から押さえつけながらもう一度はんだを熱し直します。フラックスを多めに塗ってから行うとやりやすいです |
| ![led](./img/05_led/led_8.jpg) | |
| はんだ付けができたら横から見て浮いてないことを確認します | |

残りのパッドにもはんだ付けを行います。  
PCB や LED のパッドにフラックスを少し多めに塗りながら行うと、格段にやりやすいのでおすすめです。というかフラックスがないとほとんどの方が無理だと思います。


**LED TEST の方法**

1つ目の LED をはんだ付けできた段階で LED が実際に光るかどうかテストします。  
全部はんだ付けしてからテストすると、なんというか、心が折れる可能性があり、、はじめからテストしつつ進める方法をおすすめします。

ProMicro を PC に接続し以下のコマンドで Helix の LED test Keymap を書き込みます。
```
$ qmk flash -kb helix -km led_test
```
このファームウェアを焼き込んだ状態の ProMicro を PCBに挿して PC に接続すると「赤→緑→青→赤→...」と順番に点灯してくれます。  
正しく「赤→緑→青→赤→...」とすべての LED が点灯しているかどうかではんだ付けが成功してるかどうか確認できます。

PC がスリープ中だと赤くだけ光って色が変わってくれないことがあります。  
PC がスリープしてない普通の時にテストしましょう。
同じようにバッテリーに接続して

**LED が点灯してくれない場合のデバッグ方法**

こちらの記事に詳しく書かれていますので、熟読されることをおすすめします。  
[コルネキーボードを作りました ～LED取り付けに四苦八苦記～ | キオクノロンダリング](https://marksard.github.io/2018/08/04/make-the-crkbd/)  

テスト方法とデバッグ方法を覚えたところで LED の続きのはんだ付けをしていきます。

| ![led](./img/05_led/led_10.jpg) | ![led](./img/05_led/led_11.jpg) |
| ---- | ---- |
| 一つ目の LED のテストを行ってみてるところです。ちゃんと「赤→緑→青→赤→...」と3色光ってました | 1〜6番の Underglow のはんだ付けが終わってテストしてるところです |
| ![led](./img/05_led/led_12.jpg) | ![led](./img/05_led/led_13.jpg) |
| Backlight を4つほどはんだ付けしたところです。LED のパッドを4箇所いっぺんにはんだ付けすると熱で LED がやられやすいので2箇所ずつフラックスを塗って2箇所ずつはんだ付けしていきます | 順調に順番通り付いていくと自信につながりますが、光らない LED があっても冷静にデバッグ方法を見直して修正していきます |
| ![led](./img/05_led/led_15.jpg) | ![led](./img/05_led/led_16.jpg) |
| すべての LED のはんだ付けが完了した図です。自分のはあまり上手ではありませんが、一応全部点灯してるのでなにかの参考になれば… | 1枚分の LED が終わったら反対側も芋けんぴを付けてはんだ付けします。2枚とも終わったら、芋けんぴをチャック付きポリ袋に入れて保管しておくと良いかもしれません |

光らない LED が出てきてしまった場合はデバッグの後に、ダメになった LED を基板から取る必要があります。  
Backlight の LED は、はんだ吸い取り線ではんだを除去すれば比較的簡単に取れます。  
Underglow の LED は、はんだ吸い取り線ではんだを除去しても、ポロッと取れないこともあります。はんだを除去した上で、ラジオペンチなどで横から押さえたまま強い力で潰してしまうか、ニッパーでザクザクにしていくと良いかもしれません。破片が飛ぶ可能性もあるので気をつけてください。破壊してもパッドだけ基板にこびりつく場合は、はんだを多めに足して4つのパッドの全体的にはんだがのるようにするとスルッと取れます。  
もっとスマートな方法もあります → https://www.analog.com/jp/education/landing-pages/003/bbs/bbs_02.html

すべての LED が成功したら ProMicro を uzu42 のファームウェアに戻しておきましょう。  
また、フラックスを大量に塗ったままの基板はベタベタしてしまうので、フラックスクリーナーを塗りキムワイプできれいに拭き取っておくと良いでしょう。


### ダイオードのはんだ付け

表面実装ダイオードをはんだ付けします。  
チップ部品の「|」印が、ダイオードのシルクの「|◁」の「|」の方に向けるように取り付けます。  

| ![diode](./img/06_diode/diode_1.jpg) | ![diode](./img/06_diode/diode_2.jpg) |
| ---- | ---- |
| ダイオードをパッケージから取り出したら、マスキングテープの粘着面を上にして固定したところへ整列させます。表面の `｜ T4` と書かれてる印字をよく見ながら同じ向きにします。（写真には、一つだけ反転してるダイオードがあります。わかりますか？） | 基板の `｜◁` と書かれたところに写真の向きでダイオードをはんだ付けします |
| ![diode](./img/06_diode/diode_3.jpg) | ![diode](./img/06_diode/diode_4.jpg) |
| まず片方のパッドにはんだを盛ります | 逆作用ピンセットでダイオードをつかみ、はんだ付けするところへ載せます |
| ![diode](./img/06_diode/diode_5.jpg) | ![diode](./img/06_diode/diode_6.jpg) |
| そのままはんだこてをあてます。もし浮いてたら、ダイオードを上から押さえつけつつはんだを温めることで基板に密着させます | 多少はんだが多すぎていても、一旦、反対側のはんだ付けを行い、ダイオードを基板に固定します |
| ![diode](./img/06_diode/diode_7.jpg) | ![diode](./img/06_diode/diode_8.jpg) |
| 改めて盛りすぎたはんだにフラックスを塗り、こて先にはんだが付いてないはんだこてをあてることではんだの量を調節します | このように角になってしまったはんだも同様にフラックスを塗ってからはんだが付いてないはんだこてをあてることで、はんだをきれいにすることができます |
| ![diode](./img/06_diode/diode_9.jpg) | |
| まだちょっと盛り過ぎなところもありますが、横から見て浮いてるダイオードがないか確認します |  |

すべてのダイオードのはんだ付けが終わったら、ここでフラックスクリーナーを多めに塗り、キムワイプできれいに拭き取っておくと良いでしょう。

フラックスが残ったままだとベタベタにホコリが付着し、水分を吸ってショートする恐れがあります。  
フラックスがはんだを腐食させることもあります。  
しっかりとキレイにしておきましょう。

### タクトスイッチ、TRRS ジャックのはんだ付け

TRRSジャック、タクトスイッチのはんだ付けします。  
マスキングテープで押さえてからはんだ付けを行うとまっすぐ付けやすいです。  

| ![trrs_tact](./img/07_trrs_tact/trrs_tact_1.jpg) | ![trrs_tact](./img/07_trrs_tact/trrs_tact_2.jpg) |
| ---- | ---- |
| TRRSジャックは TRRS と基板に書かれてるところへ、タクトスイッチは RESET と書かれているところへ挿し込みます。タクトスイッチには向きはありません | 上からパーツを挿したら特にズレやすい TRRSジャックをマスキングテープで固定します |
| ![trrs_tact](./img/07_trrs_tact/trrs_tact_3.jpg) | ![trrs_tact](./img/07_trrs_tact/trrs_tact_4.jpg) |
| 横から見てパーツが直角になってるか確認します | 裏からはんだ付けします。はんだ付けができたら ProMicro の時のようなことがないように色んな角度からみて確認してから完了します |


### ケーブルを繋いで動作確認

2つの基板をTRRSケーブルでつなぎ uzu42 のファームウェアが書き込まれた ProMicro を基板に付け、USBケーブルをPCにつないでみます。ソケットのパッドをピンセットなどでショートさせて正しい文字が入力されているか確認します。  
ダイオードの向きが間違ってたり、どこかにはんだ付けが失敗してるところがあると正常に動作しないので、根気よく探して修正します。

https://www.keyboardtester.com/

こちらのサイトでテストを行うと抜け漏れなくすべてのキーをテストしやすいのでおすすめです。

| ![test](./img/08_test/test_1.jpg) | ![ ](./img/08_test/test_2.png) |
| ---- | ---- |
| ソケットのパッドにピンセットを当ててショートさせてます | KeyboardTester.com でテストしてるところ|


### ソケットのはんだ付け

ソケットのはんだ付けを行います。  
ダイオードと同じく片方のパッドに先にはんだを盛っておいてからパーツを押さえてはんだを付けていきます。

| ![socket](./img/09_socket/socket_1.jpg) | ![socket](./img/09_socket/socket_2.jpg) |
| ---- | ---- |
| 片方のパッドにはんだを盛ります | ソケットを差し込みます |
| ![socket](./img/09_socket/socket_3.jpg) | ![socket](./img/09_socket/socket_4.jpg) |
| はんだがある方をはんだこてで温め、はんだを溶かします | しっかりと基板にソケットが密着したことを確認します |
| ![socket](./img/09_socket/socket_5.jpg) | ![socket](./img/09_socket/socket_6.jpg) |
| 反対側もはんだ付けしながらすべてのソケットをはんだ付けしていきます | まれにこのように、後ろから確認すると浮いたソケットがあるので、きちんと確認しつつはんだ付けを修正して進めます |
| ![socket](./img/09_socket/socket_7.jpg) | |
| すべてのソケットがはんだ付けできたら真横からみて、浮いてるソケットが無いかどうか確認します |  |


### （オプション）OLEDモジュールのはんだ付け

オプションですが OLED モジュールのはんだ付けを行います。  
BETA 版はちょっとひと手間追加になってしまいました。

| ![oled](./img/10_oled/oled_1.jpg) | ![oled](./img/10_oled/oled_2.jpg) |
| ---- | ---- |
| 遊舎工房の「OLED ピンソケット付き」を購入すると上から OLED、ピン、ソケット と3種類ずつのパーツが入っています | ソケットを PCB の OLED と書かれている枠に刺し、マスキングテープで固定します。例によって横から見て、直角になってるか確認します |
| ![oled](./img/10_oled/oled_3.jpg) | ![oled](./img/10_oled/oled_4.jpg) |
| ソケットのはんだ付けを行います | はんだ付け完了して、表から見たところです。ここで ProMicro も挿し込んでおきます |
| ![oled](./img/10_oled/oled_5.jpg) | ![oled](./img/10_oled/oled_6.jpg) |
| ピンを挿し込みます。割と硬いので力を込めてキッチリと挿します | OLEDモジュールを上からかぶせて、はんだ付けを行います |
| ![oled](./img/10_oled/oled_7.jpg) | ![oled](./img/10_oled/oled_8.jpg) |
| はんだ付けができました。ProMicro を挿し込んだ上に OLEDモジュール をかぶせることで、正しい角度のままはんだ付けを行えます | と、BETA版のみここでトラブルです。ProMicro保護プレートを付けるために OLED の隣の穴に 8mm のスペーサーを装着すると OLED の PCB が当たってしまいます |
| ![oled](./img/10_oled/oled_9.jpg) | ![oled](./img/10_oled/oled_10.jpg) |
| 上から確認してみると 1mm 弱干渉してしまっています。しょうがないのでヤスリで少し削ります | ヤスリでの調整が完了して干渉が取れました。次のバージョンからはこんなことがないように修正します |
| ![oled](./img/10_oled/oled_11.jpg) | ![oled](./img/10_oled/oled_12.jpg) |
| 横から確認すると、スペーサーよりもピンが少し上に出てしまっています | ピンをニッパーで切断して完了です。切断面に残った応力が気になる方は、はんだを温め直します |

OLED を付けた方は、ファームウェアを一行だけ修正する必要があります。

[qmk_firmware / keyboards / uzu42 / rules.mk](https://github.com/qmk/qmk_firmware/blob/9b07098dbd63fcd7b69eadfa91b5b01724e80e78/keyboards/uzu42/rules.mk#L40)

`rules.mk` のファイルの下記の部分を
```
OLED_DRIVER_ENABLE = no      # OLED display
```
以下のように修正します。
```
OLED_DRIVER_ENABLE = yes      # OLED display
```
この修正は OLED を取り外した際に `no` に戻す必要がありますのでご注意ください。


### ネジ止め

ネジ止めします。  
ここまで来ると完成も目の前です。

| ![plate](./img/11_plate/plate_1.jpg) | ![plate](./img/11_plate/plate_3.jpg) |
| ---- | ---- |
| まず ProMicro 保護プレート用のスペーサーを PCB にネジ止めします。| トッププレートにスペーサーをネジ止めします。 |
| ![plate](./img/11_plate/plate_4.jpg) | |
|  PCB をスペーサーに通し、ボトムプレートをはめ、ボトムプレートの裏からネジ止めします。 | |


### ゴム足の接着

ゴム足はボトムプレートの四隅に貼り付けます。

| ![plate](./img/11_plate/plate_5.jpg) | ![plate](./img/11_plate/plate_6.jpg) |
| ---- | ---- |
| ゴム足を貼り付ける作業はピンセットで行うときれいにできます | 四隅に貼り付けます |
| ![plate](./img/11_plate/plate_7.jpg) | |
| 貼り付けたらしっかりと上から押さえつけると、透明度が上がってキレイになります | |


### スイッチとキーキャップ

スイッチとキーキャップをはめて完了です

| ![switch keycap](./img/12_switch_keycap/switch_keycap_1.jpg) | ![switch keycap](./img/12_switch_keycap/switch_keycap_2.jpg) |
| ---- | ---- |
| スイッチは、たまに端子が曲がってることがありますので、一つ一つ目視しながら挿していきます | キーキャップもはめたら完成です |


### 完成

PC につないで問題がなければ完成です。  
お疲れさまでした！


## ギャラリー

| ![uzu42](https://i.imgur.com/kwD0vdi.jpg) | ![uzu42](https://i.imgur.com/CQTfebZ.jpg) |
| ---- | ---- |
| ![uzu42](https://i.imgur.com/DDWgKmO.jpg) | ![uzu42](https://i.imgur.com/5xJcRUI.jpg) |
| ![uzu42](https://i.imgur.com/KdEYrO4.jpg) | ![uzu42](https://i.imgur.com/rTMoizZ.jpg) |
| ![uzu42](https://i.imgur.com/CSJjGtR.jpg) |  |

