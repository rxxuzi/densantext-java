# 8.メソッドとクラス

**メソッド**とは処理をまとめて汎用的に使えるようにする仕組みです
他のプログラミング言語でいう関数のようなものです。

**クラス**とは、オブジェクト指向プログラミングにおいて、複数のオブジェクトが共通して持つデータ構造とメソッドを定義するためのテンプレートのようなものです。

**パッケージ**とは、関連するクラスやインタフェースをまとめ、同じパッケージに属する**クラス**や**インタフェース**をグループ化するための仕組みです。
**パッケージ**は、Javaプログラムの構成要素の1つであり、パッケージ内には複数のJavaクラスを含むことができます。

## 8.1. メソッドとは

メソッドにはインスタンスメソッドとクラスメソッドと呼ばれるものがあり、ここではクラスメソッドをについて説明します。

メソッドの宣言例:

~~~java
修飾子 戻り型 メソッド名 (引数型　引数名){
    メソッド本体
    return 戻り値;
}

修飾子 void メソッド名 (引数型　引数名){
    メソッド本体
}
~~~

メソッド本体は、メソッドが実際に実行するコードであり、波かっこで囲まれたブロックで表されます。
メソッドは、戻り値を返すことができ、戻り値の型はメソッドの宣言に合わせます。戻り値がない場合は、戻り値の型は`void`となります。

メソッドは、プログラムの可読性を高め、重複するコードを避けることができます。
また、メソッドは、プログラムの機能を単一のブロックにカプセル化し、再利用可能なモジュールとして抽象化することができます。

~~~java

int sa = a + b / 2 - ( 100 * a + 10 * b );
int sb = b + c / 2 - ( 100 * b + 10 * c );
int sc = c + d / 2 - ( 100 * c + 10 * d );
~~~

メソッドを使う事で上のコードを以下のように書き換えることができます。

~~~java

private int calculate(int x, int y){
    return x + y / 2 - ( 100 * x + 10 * y );
}

int sa = calculate(a,b);
int sb = calculate(b,c);
int sc = calculate(c,d);
~~~

## 8.2. classとは

Javaにおけるクラスとは、オブジェクト指向プログラミングにおいて、複数のオブジェクトが共通して持つデータ構造とメソッドを定義するためのテンプレートのようなものです。

クラスは、オブジェクトの設計図として機能し、同じクラスから複数のオブジェクトを作成することができます。
クラスは、オブジェクトが持つ属性（データメンバーまたはフィールド）や、オブジェクトに対して行われる操作（メソッド）を定義します。

~~~java

アクセス修飾子 class クラス名 {
    フィールド定義
    メソッド定義
}

~~~

`アクセス修飾子`はクラスの可視性を指定します。
`クラス名`は、クラスの名前を指定します。
`フィールド定義`は、クラスが持つ属性を定義します。
`メソッド定義`は、クラスが持つ操作を定義します。

classは以下のように使用します

~~~java

クラス名　オブジェクト名　= new クラス名();

~~~

ここで、`クラス名`は、作成するオブジェクトのクラスを指定します。`オブジェクト名`は、作成されたオブジェクトを参照するための変数名です。
`newキーワード`は、オブジェクトを作成するために使用されます。このことを**インスタンス化**といいます

クラスは、プログラムの機能を単一の単位に分割し、プログラムの構造を明確化するために使用されます。
クラスを使用することで、コードの再利用性や保守性が向上し、プログラムの開発をより効率的に行うことができます。
また、クラスは、異なるオブジェクトの間でデータを共有するための手段として機能し、オブジェクト指向プログラミングの主要な概念の1つとして重要です。