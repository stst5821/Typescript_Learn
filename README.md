## 配列に型をつける

`const numArr: number[] = [1, 2, 3];`
　　ジェネリクス(※)の書き方
`const strArr:Array<string> = ['one', 'two', 'three'];`

※ジェネリクスとは
データ型の定義とそれを参照する式の一部にパラメータを渡すことで、類似した構造を持つ複数のデータ型を一括定義できるしくみのこと。
一般的には、ジェネリクスより前者の方式（number[ ]のほう）をよく使うらしい。

## interface とは

オブジェクトの型を定義する際は、以下のようにプロパティのキー名と値の型を明記する。
`const red: {rgb:string, opacity:number} = {rgb:'ff0000', opacity:1 };`

しかし、これでは毎回インラインで型定義を書くのが大変なので
以下のように型定義をまとめることができる。

```
interface Color {
 readonly rgb:string;
 opacity:number;
 name?:string;
}

const turquoise:Color = {rgb:'00afcc', opacity:1 };
```
