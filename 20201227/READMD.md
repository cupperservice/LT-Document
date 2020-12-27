---
marp: true
theme: default
footer: https://github.com/cupperservice/LT-Document/tree/main/20201227
---

# Let's get started with Scala

Unagi.py 忘年 LT大会 2020
2020.12.27

Kawashima Kazuhisa

---
# 自己紹介
* 名前: 川嶋 一寿
* 所属: [株式会社ゆめみ](https://www.yumemi.co.jp/)
* 職業: プログラマー
* 拠点: 静岡県静岡市
* 趣味: 酒、ジョギング、水泳（最近再開）
* 好きな言語: [Scala](https://www.scala-lang.org/)
* その他活動: 専門学校講師、[Scalapedia](https://scalapedia.com/)の記事執筆
* Twitter: [@cupperservice](https://twitter.com/cupperservice)

---
# 本日の内容
## Scalaを始めてみよう

---
# Scalaって難しい？
オブジェクト指向と関数型のマルチバラダイム言語

* オブジェクト指向
* 関数型
  * 文脈がどうたら
  * モナドがどうたら
  * 圏論がどうたら

---
# どの程度、難しいのか？ 
## ScalaはPythonと同じくらい難しい

---
# 環境構築
## 必要なもの
* Java
* sbt
* node(scalajsの場合)

---
## Install SDKMAN
SDKMANをインストールする

* [SDKMAN](https://sdkman.io/)
Java関連のパッケージを管理するツール  
The Software Development Kit Manager

* インストール方法
https://sdkman.io/install

---
# Install Java
Javaをインストールする

* command
  ```
  sdk install java `version`
  ```

* Javaとの互換性
https://docs.scala-lang.org/overviews/jdk-compatibility/overview.html

---
# Install sbt
sbtをインストールする

* command
  ```
  sdk install sbt `version`
  ```
---
# Install Nodejs
1. Install nvm
  ```
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
  source ~/.bash_profile
  ```

2. Install nodejs
  ```
  nvm install `version`
  ```

---
# Create scala project
Scalaのプロジェクトを作成する

* command
  ```
  sbt new scala/scala-seed.g8
  ```

---
# Create scalajs project
## Setting sbt
1. Adding the Scala.js sbt plugin is a one-liner in `project/plugins.sbt
    ```
    addSbtPlugin("org.scala-js" % "sbt-scalajs" % "1.3.1")
    ```

2. Add the follwing settings in `build.sbt`
    ```
    enablePlugins(ScalaJSPlugin)
    ```

    ```
    scalaJSUseMainModuleInitializer := true
    ```

---
# 教材
## Web
* [scalapedia](https://scalapedia.com/)
* [Scala学習テキスト](https://scala-text.github.io/scala_text/)

## 本
* Scalaスケーラブルプログラミング
* Scala関数デザイン&プログラミング

---
# Pythonユーザーに朗報
## Scala3ではインデント構文をサポートする！

* gitter template for scala3
  ```
  sbt new scala/scala3.g8
  ```

---
# 急募
専門学校でPythonの授業をしてみたい方はいますか？

* 場所: 浜松駅から徒歩8分
* 教材: あり
* コマ数: 年間45コマ程度（週1日 - 2日）

興味がある方は以下にDMを送ってください。

* Twitter: [@cupperservice](https://twitter.com/cupperservice)

---
# Thank you for listening!
