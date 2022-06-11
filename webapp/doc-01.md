# Webアプリ構築に関わるアレコレ

#　静的なファイルを同一LAN内の他の端末から確認したい

`http-server`で任意の階層をルーティングして配信するといいかも
macだとbrew入って楽だが、aptでは入らないので、npmを経由で入れてパスを通すといいかも。

```
#時間かかる
sudo apt install npm
```

```
npm install http-server
```

グローバルでのインストールなので、通常$HOMEの直下のnode_modulesにライブラリが入る

```
ls ~./node_modules/http-server/bin
```

```
tree

node_modules/webpack
├── LICENSE
├── README.md
├── SECURITY.md
├── bin
│   └── http-server
├── ...
...(省略)

```

```
http-server {配信したいディレクトリ}

or
#パスを通しているなら
~./node_modules/http-server/bin/http-server {配信したいディレクトリ}

```

これで配信したいディレクトリのindex.htmlが`192.168.aaa.bbb:8080`で配信される




# 外部にNATを越えてアプリケーションを配信したい場合

- ngrok
- tonnelto
