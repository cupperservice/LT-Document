---
marp: true
theme: gaia
header: "**All in Scala!**"
footer: "**K.Kawasima 2020**"
---

# All in Scala

Team-Q 2020 LT大会
2020.12.25

Kawashima Kazuhisa

---

# 自己紹介
* 名前: 川嶋 一寿
* 職業: プログラマー
* 拠点: 静岡県静岡市
* 趣味: 酒、ジョギング、水泳（最近再開）
* 好きな言語: [Scala](https://www.scala-lang.org/)
* その他活動: 専門学校講師、[Scalapedia](https://scalapedia.com/)の記事執筆
* Twitter: [@cupperservice](https://twitter.com/cupperservice)

---

# 今日のお話
サーバサイドもフロントエンドもすべて __Scala__ で書いてみた話

---

# Scala使ってますか？

![width:1200px; height:450px](./img/icon-scala.png)

---

# [Scala](https://www.scala-lang.org/)とは
「オブジェクト指向」と「関数型」を統合した __マルチパラダイム__ 言語

__マルチパラダイム言語？__

---

# 要するに

オブジェクト指向と関数型の両方の良いとこ取りの言語
Simpleに記述できることが特徴

JavaVM上で動作する言語の一つ
Java言語とは相互に利用可能
JavaVM上で動作する言語は他に以下がある
* Groovy
* JRuby
* Kotlin

---

# フロントエンドの Scala?

私達には [Scala.js](https://www.scala-js.org/) がある！

![ScalaJS](./img/ScalaJS.png)

---

# Scala.jsとは？

AltJSの一つ

ScalaのプログラムをJavaScriptに変換して動作させるもの  
Scalaなのでもちろんコンパイラによる型チェックあり

---

![bg 85%](./img/CompTBL.png)

---

# 作ってみた

https://github.com/cupperservice/mydic2

---

# システム構成

![width:1100px height:250px](./img/sys.png)

---

# ディレクトリ構成

```
dev-res     // アプリケーション
+-- client    // フロントエンドのコード
+-- server    // サーバサイドのコード
+-- shared    // フロントエンドとサーバサイドの共通コード
services    // Docker
+-- appsvr    // Applicationサーバ
+-- db        // Databaseサーバ
+-- websvr    // Webサーバ
```

---

# サーバサイドの構成
* Framework: [Playframework](https://www.playframework.com/)
* DIコンテナ: [Guice](https://github.com/google/guice)
* DBアクセス: JDBC

![width:600px](./img/server.png)

---

# フロントエンドの構成
* Framework: なし
* DOM操作: [scala-js-dom](https://scala-js.github.io/scala-js-dom/)
* [View](https://github.com/cupperservice/mydic2/blob/master/dev-res/server/app/views/index.scala.html)
* [コード](https://github.com/cupperservice/mydic2/tree/master/dev-res/client/src/main/scala/cupper/mydic2)

---

# 共通コード
サーバとフロントエンドで共通のコードが使える
[コード](https://github.com/cupperservice/mydic2/tree/master/dev-res/shared/src/main/scala/cupper/mydic2)

---

# DOM操作を書くのはめんどくさい
今どきDOMを直接操作する？

モダンなWebフレームワークを使いたい
Reactとか
![width:100px height:100px](./img/icon-react.png)

Vue.jsとか
![width:100px height:100px](./img/icon-vue.png)

---
# Scalaで Reactするなら

* [Slinky](https://slinky.dev/)
* [scalajs-react](https://github.com/japgolly/scalajs-react)

---
# Scalaで Vue.jsするなら

ScalaでVue.jsは厳しい。

---

# Airframe?

サーバサイドもフロントエンドの両方をScalaで開発できる[Airframe](https://wvlet.org/airframe/)というものがあるらしい。

![width:500px height:200px](./img/icon-airframe.png)

---

# Airframeとは

Scalaで開発するための軽量ライブラリの集まり
* Designed for Scala and Scala.js
* RPC Framework
* MessagePack-based Object Serialization
* REST Services
...

---

# 作ってみた

https://github.com/cupperservice/mydic3

---

# ディレクトリ構成
```
app         // アプリケーション
+-- api       // サーバサイドのAPIインターフェース & Valueオブジェクト
+-- sercer    // サーバサイドのコード
+-- ui        // フロントエンドのコード
services    // Docker
+-- appsvr    // Applicationサーバ
+-- db        // Databaseサーバ
+-- websvr    // Webサーバ
```

---

# 

---

# 

---

# Thank you for listening!
