background-image: url(https://lh3.ggpht.com/embNgl_sfBmFB-5PslsKRmmlRrMIJCOzrI0kPFm5dOFYz9IPvG7T9B8CgdD3GpuOzv30=w300)
class: center, middle, inverse

# Android Studioのススメ
## 〜Groovyソースを添えて〜


---
background-image: url(https://lh3.ggpht.com/embNgl_sfBmFB-5PslsKRmmlRrMIJCOzrI0kPFm5dOFYz9IPvG7T9B8CgdD3GpuOzv30=w300)
# Caution

* 今回の発表はAndroid Studio以外で作成された、既存のAndroidプロジェクトをAndroid Studioにインポートして開発しようという、
極めて対象が限られるものです

* いわば茨の道を征く方々の道標になればいいかなと思って発表します

---
.left-column[
  ## Why Android Studio?
]

--
.right-column[
* お客さん「miyazaki君、とりあえずAndroidの方やっといてよ」
]

--
.right-column[
* Google先生「Eclipseはもう捨てたわ」
]

--
.right-column[
* 「えっ、君Android Studio使えるの？！いいね！」
]

--
.right-column[
* 新しいことやっときたい
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
### まあgit cloneでしょ
### そもそもローカルでソース持ってないし
### 何よりディレクトリ構成がAndroid Studio調にガラリと変わるんですよ
]

---

.left-column[
  ## Why Android Studio?
  ## Eclipse -> Android Studio
  ## clone
]

--

.right-column[
# "index-pack failed"
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
## Google先生「Cygwinのgitじゃ動かねえからｗｗｗｗ」
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
class: center, middle, inverse
background-image: url(http://www.wallpapersonly.net/wallpapers/android-3-gingerbread-1280x960.jpg)

# これってGradleの仕事じゃないの？

--

* でもなんかビルドできるし、動くし。。。
--

* まあでもせっかくだし、デファクトスタンダード(にしたい)らしいし

---
.left-column[
## What is Gradle?
]
.right-column[
* ビルドツール
* GroovyベースのDSL
* Ant -> Maven -> Gradle
* Google先生激推し
]

---
.left-column[
## What is Gradle?
## What is Groovy?
]
.right-column[
* JVM上で動作するスクリプト言語。Javaとの親和性パない。
* 簡潔な記法も可
* コンパイルも可
]

---
.left-column[
## What is Gradle?
## What is Groovy?
]
.right-column[
### ハロワ

* Java
```java
public class Main {
      public static void main(String[] args) {
          System.out.println("Hello World");
      }
}
```
* Groovy
```groovy
println "Hello"
```
]

---
.left-column[
## What is Gradle?
## What is Groovy?
]
.right-column[
### List

* Java
```java
List<String> list = Arrays.asList("a", "b", "c", "d");
for (String str : list) {
      System.out.println(str);
}
```
* Groovy
```groovy
list = ["a", "b", "c", "d"]
list.each {str->
      println str
}
```
]

---
.left-column[
## What is Gradle?
## What is Groovy?
]
.right-column[
### ファイル書き込み

* Java
```java
File file = new File(file_name);
FileWriter filewriter = new FileWriter(file);
BufferedWriter bw = new BufferedWriter(filewriter);
PrintWriter pw = new PrintWriter(bw);
pw.print("Hello World")
```
* Groovy
```groovy
new File(file_name).text = "Hello Groovy world!"
```
]


---
.left-column[
## What is Gradle?
## What is Groovy?
## Gradle How-to
]
.right-column[
* build.gradleというビルドスクリプトに設定書くだけ
]

--

.right-column[
# ﾀﾞﾄﾖｶｯﾀﾉﾆﾈ
]

---

.left-column[
## What is Gradle?
## What is Groovy?
## Gradle How-to
]

.right-column[
* プロジェクトルートにbuild.gradle置く
]

--

.right-column[
* 書く
]

--

.right-column[
* エラー出る
]

--

.right-column[
* でもビルドできる
]

--

.right-column[
* 実行もできる
]

--

.right-column[
* ﾅﾆｺﾚ
]

---
class: center, middle, inverse
background-image: url(http://www.wallpapersonly.net/wallpapers/android-3-gingerbread-1280x960.jpg)

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
]

--
.right-column[
## あっ、やっぱこれ要らないんすね。。。
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

# まとめ

### **Android開発をするなら**Eclipseを捨ててAndroid Studioを選択しよう
### 実はGradle検出設定してbuild.gradle書くだけで問題ないです
### 今回大して触れてないですが、Groovyいい感じです。実はAndroidアプリもGroovyで書けます。

---
class: center, middle, inverse

## その後・・・

---
class: center, middle

# 私はEclipseを使っています！

---

class: center, middle, inverse

# 以上！

---
class: center, middle

# というのもなんなので言い訳

---

.left-column[
## 言い訳
]

--

.right-column[
* 今回お客さんに頼まれたのは計算部分+いずれ消える運命にあるUI(作成ま○ださん)
]

--
.right-column[
* いわばAndroid関係ない部分
]

--
.right-column[
* そして何よりAndroidエミュレータマジ重い(ボタン押下後数分でブレイクポイントに)
]

--
.right-column[
* 計算結果検証してグラフに正しく表示できるか見るにはもうAndroidなくていいじゃん
]

---
class: center, middle, inverse

# ご清聴ありがとうございました
#### そもそも今回の件は、Android Studio一本で開発する方には関係ない話でした
#### とはいえこんな悲しい事態に陥った方のために<br>設定方法をgitlabにまとめてありますので、知りたい方はチェックしてみてください
#### Android Studioをディスってるわけではなく、<br>実際かなり使いやすいIDEだと思います
