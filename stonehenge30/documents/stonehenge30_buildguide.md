# Stonehenge30 ビルドガイド

- [Stonehenge30 ビルドガイド](#stonehenge30-%E3%83%93%E3%83%AB%E3%83%89%E3%82%AC%E3%82%A4%E3%83%89)
  - [パーツ一覧](#%E3%83%91%E3%83%BC%E3%83%84%E4%B8%80%E8%A6%A7)
    - [キット付属品](#%E3%82%AD%E3%83%83%E3%83%88%E4%BB%98%E5%B1%9E%E5%93%81)
    - [キット以外に必要なもの](#%E3%82%AD%E3%83%83%E3%83%88%E4%BB%A5%E5%A4%96%E3%81%AB%E5%BF%85%E8%A6%81%E3%81%AA%E3%82%82%E3%81%AE)
    - [補足](#%E8%A3%9C%E8%B6%B3)
      - [OLEDとOLED用ピンソケット](#oled%E3%81%A8oled%E7%94%A8%E3%83%94%E3%83%B3%E3%82%BD%E3%82%B1%E3%83%83%E3%83%88)
      - [OLEDの取り付け](#oled%E3%81%AE%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91)
  - [組み立て](#%E7%B5%84%E3%81%BF%E7%AB%8B%E3%81%A6)
  - [Pro Microの準備](#pro-micro%E3%81%AE%E6%BA%96%E5%82%99)
    - [ファームウェアを書き込む](#%E3%83%95%E3%82%A1%E3%83%BC%E3%83%A0%E3%82%A6%E3%82%A7%E3%82%A2%E3%82%92%E6%9B%B8%E3%81%8D%E8%BE%BC%E3%82%80)
  - [ダイオードをはんだ付けする](#%E3%83%80%E3%82%A4%E3%82%AA%E3%83%BC%E3%83%89%E3%82%92%E3%81%AF%E3%82%93%E3%81%A0%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B)
  - [基板の裏と表について](#%E5%9F%BA%E6%9D%BF%E3%81%AE%E8%A3%8F%E3%81%A8%E8%A1%A8%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)
    - [ダイオードの脚を曲げる](#%E3%83%80%E3%82%A4%E3%82%AA%E3%83%BC%E3%83%89%E3%81%AE%E8%84%9A%E3%82%92%E6%9B%B2%E3%81%92%E3%82%8B)
    - [ダイオードのはんだ付け](#%E3%83%80%E3%82%A4%E3%82%AA%E3%83%BC%E3%83%89%E3%81%AE%E3%81%AF%E3%82%93%E3%81%A0%E4%BB%98%E3%81%91)
  - [*(オプション)OLED用のピンソケット・ピンヘッダをはんだ付けする*](#%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3oled%E7%94%A8%E3%81%AE%E3%83%94%E3%83%B3%E3%82%BD%E3%82%B1%E3%83%83%E3%83%88%E3%83%BB%E3%83%94%E3%83%B3%E3%83%98%E3%83%83%E3%83%80%E3%82%92%E3%81%AF%E3%82%93%E3%81%A0%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B)
  - [TRRSコネクタ、タクトスイッチをはんだ付けする](#trrs%E3%82%B3%E3%83%8D%E3%82%AF%E3%82%BF%E3%82%BF%E3%82%AF%E3%83%88%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81%E3%82%92%E3%81%AF%E3%82%93%E3%81%A0%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B)
  - [スイッチをはんだ付けする](#%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81%E3%82%92%E3%81%AF%E3%82%93%E3%81%A0%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B)
  - [*(オプション)UnderglowLEDをはんだ付けする*](#%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3underglowled%E3%82%92%E3%81%AF%E3%82%93%E3%81%A0%E4%BB%98%E3%81%91%E3%81%99%E3%82%8B)
  - [保護パネルの取り付け](#%E4%BF%9D%E8%AD%B7%E3%83%91%E3%83%8D%E3%83%AB%E3%81%AE%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91)
  - [*(オプション)OLEDの取り付け*](#%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3oled%E3%81%AE%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91)
    - [OLED基板のカット](#oled%E5%9F%BA%E6%9D%BF%E3%81%AE%E3%82%AB%E3%83%83%E3%83%88)
  - [キーキャップの取り付け](#%E3%82%AD%E3%83%BC%E3%82%AD%E3%83%A3%E3%83%83%E3%83%97%E3%81%AE%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91)
  - [完成！](#%E5%AE%8C%E6%88%90)
  - [トラブルシューティング](#%E3%83%88%E3%83%A9%E3%83%96%E3%83%AB%E3%82%B7%E3%83%A5%E3%83%BC%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0)

## パーツ一覧

### キット付属品

| 名前 | 数 | 備考 |
| ---- | ---- | --- |
| PCB | 1枚 | |

### キット以外に必要なもの

| 名前 | 数 | 備考 |
| ---- | ---- | --- |
| ダイオード | 30個 |  |
| タクトスイッチ | 1個 | |
| キースイッチ | 30個 | MX、たぶんLowProfile(choc)、たぶんAlps、たぶんぎりぎりKailh Mid-height(MX以外は未検証です) |
| キーキャップ | 30個 | スイッチにあった規格のもの |
| Pro Micro | 1個 | |
| スプリングピンヘッダ 12P | 2個 | 交換や確認にも便利なので必須と言っていいくらい推奨 |
| *LEDストリップ（WS2812B 6個付き）* | *2個* | *Underglow用（オプション）* |
| *OLEDモジュール* | *1個* | *OLED用（オプション）取り付け高難易度のため非推奨* |
| *ピンソケット 4P* | *1個* | *OLED用（オプション）取り付け高難易度のため非推奨* |
| *ピンヘッダ 4P* | *1個* | *OLED用（オプション）取り付け高難易度のため非推奨* |
| MicroUSBケーブル | 1本 | キーボードとPC接続用 |

### 補足

#### OLEDとOLED用ピンソケット

#### OLEDの取り付け

　Treadstone48と同じくPro microの周辺に余裕がなく、OLEDの基板の一部をカットして取り付ける必要があります。どっちかというと余白を埋める存在です。

OLEDのソケットは、  

- 2.54mmピッチ  
- ロープロファイル（低背）基板取り付け高さ3.5mm  
- ピンソケット  
- 1x4(4P)  

　のものが必要です。

　また、OLEDを取り付けた場合は、使用するキーマップフォルダのrules.mkのOLED_ENABLEをyesにしてmakeする必要がありますのでご注意ください。

## 組み立て

　組み立ての時間ですが、1～3時間くらいが目安です。  

## Pro Microの準備

### ファームウェアを書き込む

　Pro Microに先にファームを書き込んでしまいます。はやる気持ちを抑えて最初にソフトウェアの準備と書き込みをしてしまえば、完成後すぐ使用できます。  

  Stonehenge30は本家QMKにマージしておりませんので、私のフォークリポジトリの**my_customize**ブランチにあるものをお使いください。  
  [marksard/qmk_firmware](https://github.com/marksard/qmk_firmware/tree/my_customize)

　Stonehenge30のキーマップのmakeは ```make stonehenge:like_jis``` で可能です。（Linux、Mac、MSYS2環境上なら ```make stonehenge:like_jis:avrdude``` で書き込みも出来ます）  
　キーマップについての解説は[ここにあります](https://github.com/marksard/qmk_firmware/blob/my_customize/keyboards/stonehenge30/keymaps/like_jis/readme_jp.md)。  

## ダイオードをはんだ付けする

## 基板の裏と表について

　キースイッチが乗り、通常使用する際上を向く面を表、逆を裏とします。  
　stonehenge30の場合、stonehenge30と印刷の入ったほうが表になります。  

### ダイオードの脚を曲げる

　基板に付ける前にダイオードの脚を全部曲げてしまいます。基板の穴の間隔を見極めて曲げるための冶具を探してみてください。繋がったままの割りばしなどでも良いと思います。  
　私はUSB-C to USB-Aの変換コネクタが丁度いい感じに使えたので、ダイオードを2,3個いっぺんに曲げていきました。  

![img](../../treadstone48/documents/_image/20181216-PC160164.jpg)  

### ダイオードのはんだ付け

　ダイオードの実装はオモテ面がデフォルトにしています。  

![img](../../treadstone48/documents/_image/diode.png)  

## *(オプション)OLED用のピンソケット・ピンヘッダをはんだ付けする*

　オモテ面に取り付けます。ラクにまっすぐ取り付けるため、マスキングテープでまっすぐつくように仮押さえしてから裏返してはんだ付けします。  

![img](../../treadstone48/documents/_image/20181216-PC160171.jpg)  

## TRRSコネクタ、タクトスイッチをはんだ付けする

　リセット用のタクトスイッチをオモテ面に取り付けてください。  

## スイッチをはんだ付けする

　プレートがないのでスイッチが斜めにつかないように注意して取り付けます。5ピンあるPCBマウント用スイッチを使用してください。

## *(オプション)UnderglowLEDをはんだ付けする*

　テープLEDの剥離紙の両端数cmだけハサミなどでカットします。  

![img](../../treadstone48/documents/_image/20181216-PC160176.jpg)  

## 保護パネルの取り付け

　Pro Micro周りの目隠しとOLEDを保護するためのプレートを取り付けます。8mmスペーサー2つを5mmのネジでPro Microの下にある穴に取り付けます。  
　プレートの保護紙を両方剥がして、黒の4mmネジでPCBに付けたスペーサーに取り付けてください。  
　少し遊びがありますので、キーキャップを取り付けた時にキーキャップと干渉する場合は少しずらしてください。  

## *(オプション)OLEDの取り付け*

### OLED基板のカット

　Pro Micro直下に取り付けるスペーサーと、OLEDの基板が左右1mm x 3mmくらい干渉しますので、写真のようにカットしてください。左が加工後です。
![img](../../treadstone48/documents/_image/20181223-PC230003.jpg)  

　スペーサーをゆるく仮止めしつつ現物合わせで削り込んでいってください。  
![img](../../treadstone48/documents/_image/20181223-PC230004.jpg)  

## キーキャップの取り付け

　お好みのキーキャップを取り付けてください。  

## 完成！

　チェックして問題なさそうなら完成です！あなただけの一台に仕上げてください！

![img](_image/)  

## トラブルシューティング

[トラブルシューティング](../../troubleshooting.md)ページを参考にしてください。  