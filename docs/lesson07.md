# Lesson 07 : 関数とは？
プログラミングを行う上で、関数は非常に強力な武器になります。  
例えば、全社員の年齢を生年月日から計算したい時どうしますか？毎回同じ計算式を使いますよね。  
共通化できる計算式（処理）を再利用できるように関数で定義したり、処理をわかりやすく関数で分割したりすることでコードを分かりやすく書くことができメンテナンス性もあがります。

まずは関数がどのようなものかを体験してみましょう。   

```
function functionName(引数, 引数,,,,) {
  何かの処理;
}
```

のように書きます。   

function名は自由に定義できます。引数は0個以上を定義できます。   
引数とは、関数実行時に与える変数です。   

以下は、testという関数名で３つの引数をもつ関数です。
test関数は与えられた３つの引数が何だったかを出力してくれる関数です。

```
function test(a, b, c) {
  console.log('第1引数は' + a + '. 第2引数は' + b + '. 第3引数は' + c);
}
test(1, 2, 3);
```

引数名は自由に決めることができ、その関数内で使う変数として宣言していることになります。

```
// 上記で何が怒っているかを分解して説明すると、
// test関数内で
var a = 1;// 第1引数
var b = 2;// 第2引数
var c = 3;// 第3引数
console.log('第1引数は' + a + '. 第2引数は' + b + '. 第3引数は' + c);
//のように実行されていることになります。
```

関数は、何かの処理をひとまとめにする為にあります。  
特定の処理が複数回使用されるならば関数にして利便性・再利用性を高めることができます。  
また、関数は、処理結果を返す(return)ことができます。

```
function multiplicativeFunction(foo, bar) {
  return foo * bar;// foo かける barの結果を返す
}
var result = multiplicativeFunction(5, 10); // 5 * 10の結果をresult変数に返す
console.log(result);// resultの中身を出力する
```


### 練習問題1
- 実行させてみましょう

```
function saySomething(word) {
  console.log(word);
}
saySomething('Hello JavaScript World!!');
saySomething('This lesson is to learn about function.');
// 引数が必要なのに与えずに与えずに実行すると？
saySomething();
```

- 実行させてみましょう

```
var functionCanBeVal = function(){
  console.log('こんな書きできます。');
};

functionCanBeVal();

```

- 実行させてみましょう

```
// 関数の最後の処理として何か値を返してほしいときは、returnを使います
var connectStrings = function(word1, word2) {
  return word1 + word2;
};

console.log('私達は、' + connectStrings('Ebisu.JS', 'です。'));
```

- 足りない何かを書き足して、正しく実行させてみましょう

```
// 2で割った値を出力してくれる関数をかきたいとします
function divideByTwo() {
  var calc = number_val / 2;
  return calc;
}

console.log(divideByTwo(4));
```

### 練習問題2
- 条件分岐が正しく機能するようなthisStringIsEbisu関数を定義してみましょう  
ヒント: 与えられた文字列(引数）が'Ebisu'であれば、trueを返す関数('Ebisu'でなければ、falseを返しましょう)

```
var targetString = 'Ebisu';

if(thisStringIsEbisu(targetString)) {
  console.log('YES!');
}
else {
  console.log('NO!');
}
```

### 練習問題3
- 三角形の面積を出力してくれる関数を定義して実行してみましょう  
ヒント: 底辺と高さを引数として与えて計算結果をconsole.log()で出力する関数
