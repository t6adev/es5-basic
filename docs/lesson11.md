# Lesson 11 : JavaScriptとは  
これまで、プログラミングに必要となる基本を学んできました。  
その過程で、JavaScriptのルール（規約や文法）を体験してきたと思います。  
変数の宣言時には、`var`をつける。1つの処理の終わりには`;`(セミコロン)をつける。  
`function`や`for`、`while`、`if`などは`{}`で括る。Objectを表現する際も`{}`を使う。配列は`[]`。などなど。  
しかしこれらはJavaScriptの基礎の一部であり、他にも仕様は多くあります。  

何かのプログラミング言語を完全に習得するには時間が必要です。プログラミング言語は手段であり目的ではありません。何かを作るための道具を完全に理解し、使いこなせないとスタートラインにたてないなんてことはなく、使いながら自分のものにすれば良いと思います。是非、これからもJavaScriptを使いながら習得していただければと思います。  

## ドキュメント
プログラミング言語を学ぶ上で、分からないことがあればドキュメントや信頼性のおけるサイトで調べることが基本となります。  
個人ブログや書籍でも情報が古かったりするので注意が必要です。  
Mozillaが提供してくれているこちらのサイトが常にメンテナンスされており、JavaScriptに関してわからないことがあればリファレンスとして利用してください。  
[https://developer.mozilla.org/ja/docs/Web/JavaScript](https://developer.mozilla.org/ja/docs/Web/JavaScript "https://developer.mozilla.org/ja/docs/Web/JavaScript")   

## 他の文法などについて
上記で話したように、まだまだ多くの文法などがJavaScriptには存在します。ここで1つ1つを細かく紹介することはやめて、概要について述べたいと思います。  

### 標準オブジェクト
標準オブジェクトとは、JavaScriptが言語として持っている値や関数などのことを言います。  
どこにも定義してないのに急に出てきたこいつはなんだ？と思ったらそれはたいてい標準オブジェクトです。  
こちらでどのようなものがあるか眺めてみましょう。  
[https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects)  

いくつか紹介すると、
- 値が存在しないことを表すための値の`null`
- 日付や時刻を扱うことの出来る`Date`
- 文字の正規表現を扱うことのできる`RegExp`
などがあります。

徐々に学んでいきましょう。

## バージョンについて
JavaScriptにはバージョンが存在します。過去の経緯やプログラミング界の流れなどを考慮し、Ecma Internationalという標準化団体がJavaScriptの仕様となるECMAScriptを策定しています。  
ECMAScriptを略してESと呼びます。`var`を使って変数を宣言する方法は、ES5の仕様になります。  
2015年からリリースサイクルは1年に1回となり、その年の新たな仕様を西暦をとってES2015などと呼びます。ES5とはES2015以前のものであり、最も世に普及した仕様でありどの環境でも動作します。ES2015は、ES6と呼ばれることもあります。  
さて、JavaScriptはブラウザで動作する言語として普及してきましたが、ブラウザにも種類やバージョンがあります。最新のECMAScriptがすべてのブラウザで動作するかどうかはそのブラウザのサポート次第となります。  
もし最新の仕様を使いたい場合は、そのコードの動作保証環境を限定するかトランスパイラを利用する必要があります。

徐々に学んでいきましょう。