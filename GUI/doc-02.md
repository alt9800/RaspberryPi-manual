# やりたいこと逆引きセッティング
ここにIndex of Contentsを記載。


# カメラモジュールを使いたい
ラズパイの設定(RaspiConfiguration or Raspi-config)より「camera」を有効にしたあと再起動。


## 写真を取りたい
`raspistill -o ./output.jpg`

起動後モニターを見ながら

## 動画を取りたい
`raspivid -o ./output.mp4`

動画を

注意点として、raspividやRaspistillはHDMI出力先にデモウインドウを表示する信号を送る仕様になっているので、RDP時など画面にデモが表示されないという問題がある。
これを解消するためには実画面(HDMI出力先)をつないだ上でのミラーリング、もしくはUSBカメラの項目を参照のこと。



# 監視カメラにしたい


# USBカメラを使いたい


# wifiサーバにしたい

# 遠隔地からアクセスしたい

## Linuxとしてsshをしたい

## Remote Desktopしたい






