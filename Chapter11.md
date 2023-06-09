# 11. 抽象クラスとインターフェース

## 11.1. 抽象クラス

抽象クラスとは、インターフェースと通常のクラスの中間のようなクラスで、「抽象メソッド（処理の記述がないメソッド）が１つ以上持つクラス」のことです

抽象メソッドは継承先のサブクラスで`Override`して実装します。

以下は抽象クラスと抽象メソッドの宣言例です

~~~java
abstract class クラス名 {
    abstract 戻り値の型名 メソッド名(引数);
}
~~~

抽象クラスで抽象メソッドを持つ利点とは、開発者側にメソッドのオーバーライドを強制するということができることです。

### 11.1.2.使う際の注意点

抽象クラスはインスタンス化ができません。使うときは必ず継承しましょう。

また、抽象クラスの抽象メソッドは、必ず全てオーバーライドする必要があります。

例：

~~~java

class Oval extends Area{
   @Override
   public double f(int v, int h) {
      return v * h * Math.PI; //楕円の面積
   }
}

class Rect extends Area{
   @Override
   public double f(int v, int h) {
      return v * h; //長方形の面積
   }
   public double square(int v){
      return vh(v); //class Areaのvh()が実行される
   }
}

class Triangle extends Area{
   @Override
   double f(int v, int h) {
      return v * h >> 1; //三角形の面積
   }
}

abstract class Area{ //面積を求める抽象クラス
   abstract double f(int v,int h); //抽象メソッド
   double vh(int r){//普通のメソッドなのでoverride無しで継承できる
      return r * r;
   }
}

Oval o = new Oval();
Rect r = new Rect();
Triangle t = new Triangle();
Area a = new Area(); // これはエラーが出る
System.out.println(o.f(20, 20));
System.out.println(r.f(20, 40));
System.out.println(r.square(30));
System.out.println(t.f(50, 20));
~~~

出力：

~~~text
1256.6370614359173
800.0
900.0
500.0
~~~

## 11.2. インターフェース

インターフェースは参照型の一種です。クラスと同じ様にフィールドとメソッドを持ち、スーパーインターフェースやサブインターフェースなども存在します。しかし以下の点がクラスとは異なります。

+ **インターフェースのフィールドは必ず定数**
+ **インターフェースが持つメソッドは必ず抽象メソッド**
+ **インターフェースはインスタンスを作れない**

### 11.2.1. 実装方法

以下はインターフェースの宣言例です

~~~java
interface インターフェース名{
    //フィールド定義 (定数)
    //メソッド定義  (抽象メソッド)
}
~~~

以下はインターフェースの実装例です

~~~java
class クラス名 implements インターフェース名{
}
~~~

クラスの継承では`extends`を使い、インターフェースの実装では`implemntes`を使います。


