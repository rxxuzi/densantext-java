# 3�@���䕶

���䕶�̓v���O�����̓������R���g���[�����邽�߂̂��̂ł�

---

## 3.1 if��

~~~java
if(����){
    ����1;
}else{
    ����2;
}
~~~

if�����g���Ƃ���**��������������Ă��邩�ǂ����ɂ���ď����𕪊򂳂��邱�Ƃ��ł��܂�**�B
��������������Ă���Ώ���1���s���A��������������Ă��Ȃ���Ώ���2���s���܂��B

~~~java
if(����1){
    ����1;
}else if(����2){
    ����2;
}
~~~

`else if`�͍ŏ��̏�������������Ă��Ȃ��ꍇ�A�ʂ̂������(�����ł͏���2)����������Ă���ꍇ�A�������s�����Ƃ��ł��܂��B
�܂��Aif���̏��������ɂ�`boolean�^`��Ԃ����������܂��B���̐^�U�l�ɂ���Ď��s����镶��؂�ւ��邱�Ƃ��ł��܂��B

~~~java
boolean result = true;
int x = 3; 
int y = 3;
if(result){
    System.out.println("result��true�ł�");
}else{
    System.out.println("result��false�ł�");
}

if(x > 5){
    System.out.println("x��5���傫���ł�");
}else{
    System.out.println("x��5��菬�����ł�");
}

if(x > y){
    System.out.println("x��y���傫���ł�");
}else if(x == y){
    System.out.println("x��y��蓙�����ł�");
}else{
    System.out.println("x��y��菬�����ł�");
}
~~~

~~~
���s����:
result��true�ł�
x��5��菬�����ł�
x��y��蓙�����ł�
~~~

***

## 3.2. switch��

~~~java
swicth(��){
    case �l1:
        �l1�Ƀ}�b�`�������̏���
        break;
    case �l2:
        �l2�Ƀ}�b�`�������̏���
        break;
    case �l3:
        �l3�Ƀ}�b�`�������̏���
        break;
    case default:
        �ǂ̒l�Ƃ���v���Ȃ������Ƃ��ɏ���
        break;
}
~~~

switch���͏�����**�l**�ŕ��򂳂��邱�Ƃ��ł��܂��B
switch���Ń}�b�`���邱�Ƃ��ł���l�̌^�͈ȉ��̒ʂ�ł�

+ char
+ byte
+ short
+ int
+ Integer
+ String

`default:`��switch���ɑ���ꂽ������`case`�̂ǂ̒l�Ƃ���v���Ȃ������Ƃ��ɏ�������܂��B
�܂��Acase�̍Ō��`break;`���L�q���Ȃ��ꍇ�A����`case`�̒����������Ă��܂��܂��B

~~~java
int medal = 2;
switch(medal){
    case 1:
        System.out.println("Gold");
        break;
    case 2:
        System.out.println("Silver");
        break;
    case 3:
        System.out.println("Bronze");
        break;
    case default:
        System.out.println("None");
        break;
}
~~~

~~~
���s����:
Silver
~~~

��L�̃R�[�h�ł͕ϐ�`medal`�̒l�ɂ���ďo�͂�ς��Ă��܂��B
�T���v���R�[�h�ł�`medal = 2`�Ȃ̂ŁA`case 2`�̒���`System.out.println("Silver");`�̏������s���܂�

#### <span style="color: red; ">NullPointerException</span>

switch���Ń}�b�`������l��`Null`�������ꍇ�A`NullPointerException`���������܂��B

***

## 3.3. �O�����Z�q

```java
������ ? �}�b�`�����ꍇ�̒l : �}�b�`���Ȃ������ꍇ�̒l;
```

�O�����Z�q�̓}�b�`���邩�ǂ����𔻒肷��������ƃ}�b�`�����ꍇ�̒l�A�}�b�`���Ȃ������ꍇ�̒l���w�肷�鉉�Z�q�ł��B
if-else�����ȗ��������L�q���@�ł��B

if-else����p�����R�[�h:

```java
int a ;
int b = 20
if(b > 15){
    a = 10;
}else{
    a = -10;
}
System.out.println(a);
```

~~~java
���s���ʁF
10
~~~

�O�����Z�q��p�����R�[�h:

```java
int b = 20
int a = b > 15 ? 10 : -10;
System.out.println(a);
```

~~~java
���s���ʁF
10
~~~
