# rs_auth_passkey_1

 Version: 0.9.1

 Author  : 

 date    : 2026/11/18
 
 update  :

***

Rust Axum , Passkey Authrize SQLite Example

* SQLite DB
* windows11 , Windows hello
* express
* node22
* Linux

***
* Env-value
```
export RP_ID=localhost
export RP_ORIGIN=http://localhost:3000
```

***
* start
```
cargo build
cargo run
```


***
## 補足

* webauthn-rs は OpenSSL に依存します。Windows でビルドが失敗する場合は、vcpkg で OpenSSL を入れるか、openssl クレートの vendored 機能(Perl と C コンパイラが必要)を使ってください。

* 本番で使うときは、RP_ID と RP_ORIGIN を環境変数で実ドメインに設定し、HTTPS にして Cookie の .secure(true) を有効にしてください。
* チャレンジの状態はメモリ保持なので、再起動すると消えます。TTL(有効期限)付きの管理を足すのがおすすめです。
* index.html では Windows Hello を優先するよう authenticatorAttachment: "platform" を指定しています。スマホや USB キーも許可したい場合は、その1行を削除してください

***
### version
* V_0_9_1: new

***
### blog

https://zenn.dev/knaka0209/scraps/92ae6df120c739
