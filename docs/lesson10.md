# Lesson 10 : Object（オブジェクト）で表現の幅を広げる
いよいよJavaScriptの基本の最終段階とも言ってよいObjectを学ぶ時が来ました。  
前回、配列によってまとまった情報を表現することが出来ました。  
が、少しスッキリしない感覚を覚えませんでしたか？  
前回、以下のように生徒名と出席番号を無理矢理に表現しました。   
```
// 生徒名と出席番号を別々に定義してみた例
var studentNames = ['Jun Matsumoto', 'Masaki Aiba', 'Satoshi Ono', 'Kazunari Ninomiya', 'Sho Sakurai'];
var studentNumbers = [1, 2, 3, 4, 5];

// 1つの配列に生徒名と出席番号をまとめた例
var studentsNameAndNumber = ['Jun Matsumoto', 1, 'Masaki Aiba', 2, 'Satoshi Ono', 3, 'Kazunari Ninomiya', 4, 'Sho Sakurai', 5];
```

変数名から、「生徒の名前と番号を表してるんだなぁ」とか、[]内の記述から、「名前と番号を順番に書いて表現しているのか」などがわかるかと思います。  
では、生年月日を追加したい場合、どのようにデータを表現したらよいでしょう。さらに性別や趣味、得意科目などを追加したい時はどうしましょう。  
studentsNameNumberBirthdayGender...の様に変数名を書いて、配列の中身を['生徒名', 出席番号, '性別',,,]などとしますか？これは流石にひどいですね。  
そこで便利なものが、Object(オブジェクト)です。まずは以下を見てみましょう。   
```
var student = {
  name: 'Jun Matsumoto',
  number: 1,
  gender: 'male',
};
```

Objectは、`{ property: value }`のように表現します。propertyは、任意の名前。valueは、propertyに該当する値を意味します。（propertyのことをkeyとも呼びます）  
valueには、配列や関数も定義することができます。今は頭の片隅においておいてください。  
ここでなんとなく、配列にオブジェクトも入れることが出来るのかな？と思えたら、良い傾向です。  
とりあえず、まずはオブジェクトにアクセスする方法を体験してみましょう。  
```
console.log(student.name); // 変数名.プロパティー名でアクセス可能です
console.log(student['name']); // 変数名['プロパティー名の文字列']でもアクセス可能です。なんだか配列みたいですね。
```

## 記法
if文や関数で使った`{}`をオブジェクトでも使います。  
0個以上のプロパティ数で定義が可能で、複数のプロパティを書く際は、`,`で区切ります。  
プロパティの値を変えたい場合、`oneProp.something = 'changed something';`のように書くことが出来ます。さらに、新たなプロパティを任意のタイミングで追加することも出来ます。
```
var blankObj = {};
var oneProp = { something: 'something' };
var twoProps = { one: 1, two: 2 };

console.log(blankObj);
console.log(oneProp);
console.log(twoProps);

blankObj.addedProp = 'added';
console.log(blankObj);
```


### 練習問題1
- student変数自体を出力してみましょう
- student変数の各プロパティをすべて出力してみましょう

```
var student = {
  name: 'Jun Matsumoto',
  number: 1,
  gender: 'male',
};
```

## オブジェクトと配列の組み合わせ
早速、学生名簿をObjectと配列(Array)で表現してみましょう。
```
var students = [{
  name: 'Jun Matsumoto',
  number: 1,
  gender: 'male',
}, {
  name: 'Gro Inagaki',
  number: 2,
  gender: 'male',
}, {
  name: 'Satoshi Ono',
  number: 3,
  gender: 'male',
}, {
  name: 'Kazunari Ninomiya',
  number: 4,
  gender: 'male',
}, {
  name: 'Sho Sakurai',
  number: 5,
  gender: 'male',
}];
```

### 練習問題2
- 何かの情報をObjectで表現してみましょう。(例：朝昼晩の天気と気温)

### 練習問題3
- students配列の誰かの情報１つを出力してみましょう  
ヒント: Arrayは、変数名[要素番号], Objectは、変数名.プロパティ名(または、変数名[プロパティ名の文字列])でアクセスできました。

```
var students = [{
  name: 'Jun Matsumoto',
  number: 1,
  gender: 'male'
}, {
  name: 'Gro Inagaki',
  number: 2,
  gender: 'male'
}, {
  name: 'Satoshi Ono',
  number: 3,
  gender: 'male'
}, {
  name: 'Kazunari Ninomiya',
  number: 4,
  gender: 'male'
}, {
  name: 'Sho Sakurai',
  number: 5,
  gender: 'male'
}];
```
