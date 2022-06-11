# Webアプリ構築に関わるアレコレ

#　静的なファイルを同一LAN内の他の端末から確認したい

常套作としてはApatchやNGINXをインストールして、`www/html`などを配信するパターンなどもあるが、もう少し簡単にもできる。

## `http-server`で任意の階層をルーティングして配信するといいかも。
やっていることはReact使うときのnpm startでlocalhost:3000の配信するときと概ね同じ。

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
#パスを通しているなら
http-server {配信したいディレクトリ}

or
#パスを通してない場合
~./node_modules/http-server/bin/http-server {配信したいディレクトリ}

```

これで配信したいディレクトリのindex.htmlが`192.168.aaa.bbb:8080`で配信される



# お家からインターネットを介してアプリケーションやNASの入り口を提供したい場合

必要なものやあると良いもの
- webサーバ(Apache,NGINX,envoy)
- ダイナミックDNS
- ドメイン


# 外部にNATを越えてアプリケーションを配信したい場合

- ngrok
- tonnelto
