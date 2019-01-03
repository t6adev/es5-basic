# Lesson 03 : Boolean(bool型)と比較演算子と論理演算子

プログラミングにおいて、型というものが重要になってきます。   
Lesson01, 02では、文字列(string型)と数値(Number型)を学習しました。   
Boolean(bool型)とは、`true`(真), `false`(偽)の2つを表現する型になります。   
以下は、文字列ではなくBooleanです。
```
console.log(true);
console.log(false);
```

## 比較演算子
比較演算子とは、2つの値を比べる為の記号（演算子）で、比較結果（演算結果）を`true`または`false`で返してくれます。   
例えば、  
- 1と1を比較した場合、正しいので`true`
- 1と2を比較した場合、間違っているので`false`
となります。  
比較演算子には、 `===`, `<`, `<=`, `>`, `>=` があります。
```
console.log(1 === 1); // -> true
console.log(1 === 2); // -> false
console.log(1 < 1); // -> false
console.log(2 >= 1); // -> true
```

## 論理演算子
### `&&` は、「〜かつ〜」(AND)
`true`同士を `&&` で演算した場合、`true`になりますが、どちらかが`false`である場合、`false`になります。

### `||` は、「〜または〜」(OR)
何かbooleanなものを `||` で演算した場合、１つでも`true`であれば`true`になり、全て`false`であれば`false`になります。

### `!` は、「〜ではない」(NOT)
booleanなものの先頭に `!` を付与すると逆の値を返します。`false`なものを`true`で表現したい場合、`!false`とすれば`true`を返します。

実際に書くと以下のようになります。
```
console.log(true && true); // -> true
console.log(true && false); // -> false
console.log(true || false); // -> true
console.log(!!!true); // -> false
```

## 条件（三項）演算子
条件演算子は、何かの演算した結果、正しい場合と間違った場合で任意の結果を得たい場合に使うことができます。  
記法として、 `[演算] ? [正しい場合の値] : [間違った場合の値]` のように、`?`と`:`で表現できます。  
```
console.log('js' === 'j' + 's' ? 'this is js' : 'this is not js');
```

### 練習問題   
- 「100は、99より大きい」(100 > 99)
- 「100は、99以下」(100 <= 99)
- 「100は、100以上」(100 >= 100)

### 練習問題2   
- 以下の実行結果がどうなるか想像した上で実行させてみましょう。  
演算子（記号）には、処理される優先順位が決まっています。  
また、丸括弧()で部分をくくると、全体の中でその中身がまず処理されます。  

```
console.log('===は、厳密に等しい' === '===は、厳密に等しい'); // true or false?

console.log(3 !== 3.0001); // true or false?

console.log(5 > 4); // true or false?

console.log(5 * 2  >= 5.0 + 5.0); // true or false?

console.log((5 <= 6) === (4 <= 4)); // true or false?

console.log(5 > 4); // true or false?

// 論理演算子の効果を体験してみましょう。
console.log(true && true); // true or false?

console.log(3 === 3 || true === false); // true or false?

console.log(!(true || false)); // true or false?


// 条件（三項）演算子
console.log(!true ? 'こちらではなく' : 'こちらが出力される'); // どちらが出力される？
```

### 練習問題3 論理演算子の腕試し
- 以下を実行してみましょう。実行する前にどのような結果になるか予想してみましょう  

```
// 3-1
console.log(false && true);
// 3-2
console.log(true && false);
// 3-3
console.log(false || true);
// 3-4
console.log(true || false);
// 3-5
console.log(true && true && true);
// 3-6
console.log(true && false && true);
// 3-7
console.log((true || false) && true);
```

## 論理演算子の発展
論理演算子の項目ではBoolean型同士の演算でしたが、実はBoolean型以外も論理演算子で演算することができます。  
型を統一して演算する必要はなく、どんな型同士であっても演算可能になります。

- 下記の結果はどうなるか試してみましょう。

```
console.log(true && '文字列');
console.log(true || '文字列');
console.log(false && '文字列');
console.log(false || '文字列');

console.log('文字列' && true);
console.log('文字列' || true);
console.log('文字列' && false);
console.log('文字列' || false);
```
