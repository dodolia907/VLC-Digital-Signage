## 導入
事前にCLIでLinuxをインストールしておいてください。

1. このリポジトリを任意の場所にクローンします。
2. scpなどでkioskディレクトリに表示する映像や画像を転送します。
3. crontab -eでお好みに設定します。

以下は毎時00分と30分に画像を切り替える設定の例です。
```
@reboot [kiosk-start.shのフルパス]
00 * * * * [kiosk-next.shのフルパス]
30 * * * * [kiosk-next.shのフルパス]
```

## 使い方
設定後は起動するだけで映像が表示されます。
手動で映像を切り替えたい場合は別のマシンから`telnet [サーバーのIPアドレス] [4212]`と入力してtelnet接続を行います。