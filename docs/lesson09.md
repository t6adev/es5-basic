# Lesson 09 : 配列とループ  
データの格納方法として便利なものに、配列というものがあります。   
これまで、データ（数値や文字列など）を格納するときは１つずつ変数に格納してきました。   
しかし、扱うデータによってはまとめて管理、操作したほうが都合の良い場合が多々あります。   

学級名簿を考えてみましょう。今までの方法であれば、以下の様な方法で表現したかもしれません。   
```
var studentName01 = 'Jun Matsumoto';
var studentName02 = 'Masaki Aiba';
var studentName03 = 'Satoshi Ono';
var studentName04 = 'Kazunari Ninomiya';
var studentName05 = 'Sho Sakurai';
```

数字が出席番号という感じでしょうか。それにしても5人のクラスなんてよっぽど過疎化のすすんだ所の学校ですね。
さて、一般的なクラスの人数というと30人とかでしょうか。この調子で30人分書き続けるってのはスマートではないですね。
配列の仕組みを使うと、以下のように書くことが出来て便利です。
```
var studentNames = ['Jun Matsumoto', 'Masaki Aiba', 'Satoshi Ono', 'Kazunari Ninomiya', 'Sho Sakurai'];
var studentNumbers = [1, 2, 3, 4, 5];
```

javascriptの配列では、データ型をミックスして格納することが出来ます。たとえば、以下の様な感じです。
```
var studentsNameAndNumber = ['Jun Matsumoto', 1, 'Masaki Aiba', 2, 'Satoshi Ono', 3, 'Kazunari Ninomiya', 4, 'Sho Sakurai', 5];
```

これまでに学んだ変数は、自由に書き換えができました。もちろん、配列も書き換え可能です。
```
studentNumbers = [3, 2, 5, 4, 1];
studentNumbers = [1];
studentNumbers = ['1番', '2番', '3番', '4番', '5番'];
```

もし、出席番号の3番と1番を入れ替えたい時など、一つ一つの要素の順番を書き換えたい時、毎回直すのは面倒ですね。
各要素にアクセスするときは、`配列名[要素の番号]`という風に書きます。お気づきのように、最初の要素は0番目です。（0番目から数えます）
```
studentNumbers[0] = 1;
studentNumbers[4] = 3;
```
要素数（配列の長さ）を取得したい場合は、`studentNumbers.length`で取得可能です。

### 練習問題
- 下記のコードでは生徒名を出力しています。出席番号となるような番号も同時に出力できるように、console.log()の中身を変更してみましょう。Jun Matsumoto君から1番になるようにしましょう。  

```
var students = ['Jun Matsumoto', 'Masaki Aiba', 'Satoshi Ono', 'Kazunari Ninomiya', 'Sho Sakurai'];

for(i = 0; i < students.length; i++) {
  console.log(students[i] + '君！');
}
```
