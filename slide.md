class: center, middle, inverse

# Android Studioのススメ

---

.left-column[
  ## Why Android Studio?
]

.right-column[
1. お客さん「miyazaki君、とりあえずAndroidの方やっといてよ」
1. Google先生「Eclipseはもう捨てたわ」
1. 「えっ、君Android Studio使えるの？！いいね！」
1. 新しいことやっときたい
]

--
.right-column[
# 不純
]

---

.left-column[
  ## Why Android Studio?
  ## Eclipse -> Android Studio
]

.right-column[
## 手段は2つ

1. ローカルのEclipseプロジェクトをインポート
1. gitリポジトリからクローン
]
--
.right-column[
## まあgit cloneでしょ
]

---

.left-column[
  ## Why Android Studio?
  ## Eclipse -> Android Studio
  ## clone
]

--

.right-column[
## index-pack failed
]

--

.right-column[
# んっ？
]

--

.right-column[
インストールされてるgit自動検出して設定してくれてるじゃん
]

--

.right-column[
Google先生「Cygwinのgitじゃ動かねえから」
]

---
class: center, middle

# 憎らしくてキーボードに爪を立ててみる

---
name: ira
class: center, middle

# イラッ⭐︎

![ira](http://www.trust5.jp/wp-content/uploads/1226.jpg)

---
.left-column[
  ## Why Android Studio?
  ## Eclipse -> Android Studio
  ## clone
  ## Settings
]
.right-column[
とにもかくにもWindowsのgitをインストール
]

--
.right-column[
IDEの左にsrcとかlibとかbinとか出てこない
]

--

.right-column[
探す
]

--
.right-column[
探す
探す
]

--
.right-column[
探す
探す
探す
]

---

.left-column[
  ## Why Android Studio?
  ## Eclipse -> Android Studio
  ## clone
  ## Settings
]
.right-column[
![staff](http://stamp.bokete.jp/5873813.png)
]

---
.left-column[
  ## Why Android Studio?
  ## Eclipse -> Android Studio
  ## clone
  ## Settings
]
.right-column[
* File>Project Structureより、これがソースフォルダ、これがリソースフォルダだよと指定してく
* 全部指定したらとりあえず左側に出てきた
]

---
class: center, middle

# んっ？

---
class: center, middle

# これってGradleの仕事じゃないの？

--

* でもなんかビルドできるし、動くし。。。
--

* まあでもせっかくだし、デファクトスタンダード(にしたい)らしいし

---
.left-column[
# What is gradle?
]
.right-column[
* ビルドツール
* GroovyベースのDSL
* Ant -> Maven -> Gradle
* Google先生激推し
]

---
.left-column[
# What is gradle?
# How-to
]
.right-column[
* build.gradleというビルドスクリプトに設定書くだけ
]

--

.right-column[
# ﾀﾞﾄﾖｶｯﾀﾉﾆﾈ
]

---

* プロジェクトルートにbuild.gradle置く

--

* 書く

--

* エラー出る

--

* でもビルドできる

--

* 実行もできる

--

* ﾅﾆｺﾚ

---
class: center, middle

## ソースなどと同じく認識されてないから設定してあげなきゃならないんじゃ？

--

## でもどうやって？

---

![staff](http://stamp.bokete.jp/5873813.png)

---

.left-column[
## Settings
]
.right-column[
* File>Project Structure>Project Settings>Facets>Detection

* Android-Gradleを追加
]

--

.right-column[
* 「これはGradleでビルドするプロジェクトだから検出してね」ってことか
]

---
template: ira

---

.left-column[
## Settings
]
.right-column[
File>Project Structureより、これがソースフォルダ、これがリソースフォルダだよと指定してく
## あっ、これ要らないんすね。。。
]

---
class: center, middle, inverse

## 心が怒りの矢を放つ☆(うろ覚え)

---

.left-column[
## Settings
]
.right-column[
* 検出してね設定を行うと、Project Structureより設定できる項目が大幅に減る

* 減った設定は全てbuild.gradleに任せるってことね

* これでプロジェクトがbuild.gradleと紐付いたってことか
]

--

.right-column[
# 勝った
]

---
class: center, middle, inverse

## その後・・・

---
class: center, middle

# 私はEclipseを使っています！

---

class: center, middle, inverse

# 以上！
