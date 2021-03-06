# RaspberryPi-manual
Note for myself.
現時点で日本語のみの対応としています。

# update 
2021/08/14


# TL;DR
Raspberry Piを運用する上でのあれこれをWikiっぽくまとめています。
GUIを使う初心者/リッチな環境用とCLIでの運用を念頭に置いた軽量版についてまとめている最中です。




# 基礎知識

オンボードPC。SDカードにOSのイメージを書き込むことで動作させることができるLinux。

Raspberry Pi の現行(2021/08/14)は"4"で、初めてRAMが1GB~8GBまで選べるようになった。

それまで(3まで)は1GBのメモリでの運用を念頭に置く必要があったが、サーバしての機能がリッチになった。

インターフェースとしてRaspberry Pi 4 からは電源がTypeCでの3A給電になり、microHDMI端子から同時画面出力などが可能になった。
一方で処理能力の向上とトレードオフで発熱が増しているのでヒートシンクや空冷ファンの購入をおすすめ。

そのため筐体を並列に大量に扱いたい場合、あるいは初心者はRaspberry Pi3B+の購入もおすすめ。
基盤単体で5000円程度で変える上、入力が2.5AのMicroB USBなうえ、HDMIケーブルでの出力が容易で5GHzに乗ることもできる。

ちなみに3B+と同じくよく出回っている2Bまでは**wifiのアンテナが基盤に付いていない**他、Bluetoothのアンテナもない。


## その他の筐体

LTE Pi , 3G pi と言われるsimカードによって単体で基地局とデータ通信を行うことができる拡張基盤タイプもある。


# To Buy

秋月電子通商、千石電商ほか、[ヨドバシカメラ](https://www.yodobashi.com/?word=Raspberry+Pi)や[Amazon](https://www.amazon.co.jp/Raspberry-Pi/s?k=Raspberry+Pi)などで購入できる。

[おすすめは全部入のセット](https://www.amazon.co.jp/%E3%82%AD%E3%83%83%E3%83%88%EF%BC%88%E6%8A%80%E9%81%A9%E3%83%9E%E3%83%BC%E3%82%AF%E5%85%A5%EF%BC%89MicroSDHC%E3%82%AB%E3%83%BC%E3%83%8932G-Raspbian%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0%E3%83%97%E3%83%AA%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB-MicroHDMI-HDMI%E3%82%B1%E3%83%BC%E3%83%96%E3%83%AB%E3%83%A9%E3%82%A4%E3%83%B3-%E6%97%A5%E6%9C%AC%E8%AA%9E%E5%8F%96%E6%89%B1%E8%AA%AC%E6%98%8E%E6%9B%B8%EF%BC%884GB/dp/B099RKY9J9/ref=sr_1_7?dchild=1&keywords=Raspberry+Pi&qid=1628856830&sr=8-7)


[ユーザグループ](https://www.raspi.jp/whatis/buy/)のページが法人には便利か。

## 必要な周辺機器

- キーボード
- モニター (HDMI入力ができるのであればテレビ)
- マウス
- インターネット環境 (いわゆる*普通の*wifiがあればOK)

これらはなくても大丈夫(PCやガジェットに詳しい人ならば代替方法がある)だが、**できれば買おう**。
マウスとキーボードは1000円前後からある。

## その他あると良いもの

- PC Sdカードにイメージを書き込むのに利用する他、SSHやRDPによってRaspberry Piを遠隔で操作することもできる。
- ブレッドボードやジャンパーワイヤー、抵抗



# 使い方

## 実用
- 高級言語(C,Python)を以て電子工作、制御を行う基盤
- LinuxのWebサーバーとして(かんたんなweb工作)
- Windows10 IoTCoreを載せたwindowsの処理環境として

## 学習
- Minecraft、Steamのゲームの最低スペック環境として
- Sonic Pi で作曲

## Advanced
- 監視カメラ
- VPNサーバー
- 入退室管理(Felica)
- センシング(wifiの強度、温湿度、CO2...)
- リモートリポジトリ(Gitlab)
- Kubernetes


# 知っておくと幸せになれること

- タッチパネルからの入力を受け取れるので、寿司チェーンでは注文端末にしてある
- Wifiのモジュールを使って無線Lan(wifi)のアクセスポイントの構築や中継機にもできる
- ベースとなっているDebianはもちろん、ubuntu(あるいはmate)やCent、Archを導入することもできる。

- Dockerも基本的にあまりこまることはないが、armV8用のイメージが提供されていないコンテナもあり、一部フル機能使えないソフトウェアがあったりする
- OSの導入時期によってネットワーク関係のデーモンの推奨される記述方法がちがう

- Raspbian -> Raspberry PiOSと名称が改まったが、実はGUIモードでプリインストールされるゲームが減っていたりする(Minecraft pi とか)

