# 2. ���Z�q

**���Z�q���g�����ŁA��Ɋ�{�f�[�^�^�̒l�ɑ΂���v�Z���s�����Ƃ��ł��܂��B**
���Z�q�ɂ�**�Z�p���Z�q, �_�����Z�q, ��r���Z�q, ������Z�q, �r�b�g���Z�q**��5������܂�

***

## 2.1 ���Z�q�̎��

### �Z�p���Z�q

�Z�p���Z�q�͐��l����舵���Ƃ��Ɏg�����Z�q�ł�
|���Z�q|�L���� | ����|
|---|---| ---|
|+| x + y | x��y�����Z|
|-| x - y | x��y�����Z|
|*| x * y | x��y����Z|
|%| x % y | x��y�Ŋ������]������߂�|
|++| x++ | x�̒l��1���₵�����a�̒l��Ԃ�|
|++| ++x | x�̒l��Ԃ������a�̒l��1���₷|
|--| y-- | y�̒l��1���炵�����a�̒l��Ԃ�|
|--| --y | y�̒l��Ԃ������a�̒l��1���炷|

++�A--���Z�q�̓C���N�������g�A�f�N�������g���Z�q�Ƃ����܂�
�ϐ��̑O�ɒu������O�u�ƌ����A�ϐ��̌��ɒu��������u�ƌ����܂�

�T���v���R�[�h:

~~~java
int a = 1 + 3; // a = 4
int b = 4 - 2; // b = 2
int c = 2 * 3; // c = 6
int d = 4 / 2; // d = 2
int e = 4 % 3; // e = 1

int f = 5;
f++;
System.out.println(f); //6
~~~

***

### �_�����Z�q

�_�����Z�q��boolean�^�̒l�ɑ΂��鑀����s�����Z�q�ł��B
**�K��boolean�^�̒l��Ԃ��܂��B**
|���Z�q|�L���� | ����|
|---|---| ---|
|!| !a | x��false�ꍇ��true��Ԃ��Ax��true�ꍇ��false��Ԃ�|
|&&| x && y | x��y�̗�����true�̏ꍇ��true��Ԃ�|
| \|\|| x \|\| y | x��y�̂����ꂩ��true�̏ꍇ��true��Ԃ�|
�T���v���R�[�h:

~~~java
boolean x = true;
boolean y = true;
boolean z = false;
System.out.println(x);      //true
System.out.println(!x);     //false
System.out.println(x && y); //true
System.out.println(x && z); //false
System.out.println(x || y); //true
System.out.println(x || z); //true
~~~

***

### ��r���Z�q

|���Z�q|�L���� | ����|
|---|---| ---|
|==| x == y | x��y���������ꍇ��true��Ԃ�|
|!=| x != y | x��y���������Ȃ��ꍇ��true��Ԃ�|
| >| x > y | x��y�����傫���ꍇ��true��Ԃ�|
| <| x < y | x��y�����������ꍇ��true��Ԃ�|
|>=| x >= y| x��y�����傫�����������ꍇ��true��Ԃ�|
|<=| x <= y| x��y�������������������ꍇ��true��Ԃ�|

�T���v���R�[�h:

~~~java
System.out.println(1 == 1); //true
System.out.println(1 == 2); //false
System.out.println(1 != 1); //false
System.out.println(1 >  0); //true
System.out.println(1 <  2); //true
System.out.println(1 <= 1); //true
System.out.println(0 >= 1); //false
~~~

***

### ������Z�q

|���Z�q|�L���� | ����|
|---|---| ---|
|= | x = 100 | x��100���� |
|+=| x += 1  | x��x+1�̒l����|
|-=| x += 2  | x��x-2�̒l����|
|*=| x += 3  | x��x\*3�̒l����|
|/=| x += 4  | x��x/4�̒l����|

�T���v���R�[�h:

~~~java
int a = 100;
System.out.println(a); // 100
a = 200;
System.out.println(a); // 200
a += 50;
System.out.println(a); // 250
~~~

***

### �r�b�g���Z�q

|���Z�q|�L���� | ����|
|---|---| ---|
|& | x & y | x��y�̃r�b�gAND |
|\| | x \| y | x��y�̃r�b�gOR |
|^ | x ^ y | x��y�̃r�b�gXOR |
|~ | ~x  | x�̃r�b�g�𔽓]������ |

�T���v���R�[�h:

~~~java
int a = 0b00011; // 3
int b = 0b01010; //10

System.out.println(a & b); // 2
System.out.println(a | b); //11
System.out.println(a ^ b); // 9
System.out.println(~a);    //-4

~~~

***

## 2.2. ���Z�q�̗D�揇��

�ォ��D�悳��܂�

1. `X++` `X--` ��u�C���N�������g/�f�N�������g

2. `++X` `--X` `~` �O�u�C���N�������g/�f�N�������g  NOT

3. `*` `/` `%`�@��Z ���Z ��]

4. `+` `-`�@���Z ���Z

5. `<<` `>>`�@�r�b�g�V�t�g

6. `<` `>` `<=` `>=`�@��r���Z�q

7. `==` `!=`�@��r���Z�q

8. `&` AND

9. `^` XOR

10. `|` OR

11. `&&` �_�����Z�q(AND)

12. `||`�@�_�����Z�q(OR)

13. `?:` �O�����Z�q

14. ������Z�q�S��

�܂��A`()`�̒��g����D�悳��܂��B

~~~java
System.out.println(3 + 1 * 2);
System.out.println(5.0 / 4.0 >= 2);
System.out.println((10 + 20) / 5);
~~~

~~~java
���s���ʁF
5
false
6
~~~
