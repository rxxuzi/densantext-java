#0. �͂��߂�
���̃e�L�X�g��java�ɏ����ł��������������l���C�y�ɐG�����悤�ɂ����e�L�X�g�ł�
����C�����G�ꂽ���Ƃ�����l��A�d�Z�e�L�X�g��ǔj�����l�Ȃ瑽���]�T�ł��B

***
## 0.1. Hello World!
�܂���java�𓮂����Ă݂܂��傤
�܂�```Main.java```�Ƃ����t�@�C��������āA����``Main.java``�̃t�@�C���̒��Ɏ��̃R�[�h�������Ă݂܂��傤
~~~java
class Main{
    public static void main(String args[]){
        System.out.println("Hello World");//java
    }
}
~~~
���ɐ�قǏ������R�[�h���R���p�C������ƁA�R�}���h���C����
~~~
Hello World
~~~
�Ǝ��s���ʂ��o��Ǝv���܂��B
���ꂪ��������Ƃ���java�ł�Hello World�̂����ɂȂ�܂��B
***
## 0.2. �\��
���̍��ł͐�قǏ������R�[�h�̈Ӗ���������Ă��������Ǝv���܂��B
`package`�ɂ��Ă͌�قǐ������܂��B

~~~java
class Main{

}
~~~
����``class ���O{}``�ň͂܂ꂽ�����̎���**�N���X**�Ƃ����܂��B
~~~java
public static void main(String args[]){
    
}
~~~
����``public static ~ ``�ň͂܂ꂽ������**���\�b�h**�Ƃ����A
���\�b�h�ň͂܂ꂽ�����ɂ�肽�������������܂�
*���̌�̓��e�ł̓N���X�����ƃ��\�b�h�����͏ȗ����܂��B

��L�̃R�[�h�ł�``System.out.println("Hello World");``�������ɂ�����܂�
�܂��A�R�[�h�̒��� ``//``�ƃo�b�N�X���b�V����2����邱�Ƃɂ���āA**�R�����g**���邱�Ƃ��ł��܂��B
(�R�����g�Ƃ̓v���O�����ɉe����^�����ɂ����钍�߂̂��Ƃł�)

**�܂��Ajava�̌��܂�Ƃ��ĕ����ɂ͕K���Z�~�R����``;``���K�v�ƂȂ�܂�**

```System.out.println()```��``()``�̒��g���o�͂���Ƃ����Ӗ��ł��BC�����``printf()``�Ǝ����悤�ȕ��ƍl���Ă����ł��B
()�̒��́A������ł����``""``�_�u���R�[�e�[�V�����ň͂݁A���l�Ȃ炻�̂܂ܓ���邱�Ƃ��ł��܂��B�܂��A`()`�̒��ɕ����񂪓����Ă����``+``�L�����g���ĘA�����邱�Ƃ��ł��܂��B
������``()``�̒��ł͌v�Z�����邱�Ƃ��ł��܂��B

`System.out.print()`�ƋL�q���鎖�ŁA���s�����ɏo�͂����邱�Ƃ��ł��܂��B

�T���v���R�[�h�F
~~~java
System.out.print("Hello ");
System.out.println("world");
System.out.println("Hello " + "Java!");
System.out.println("Number :" + 10);
System.out.println("20" + "23");
System.out.println(20 + 23);
~~~
�o�́F
~~~
Hello world
Hello Java!
Number : 10
2023
43
~~~
��L�̃R�[�h��5�s�ڂ�6�s�ڂ̈Ⴂ��20��23�������񂩐��l�ł��邩�̈Ⴂ�ł��B
5�s�ڂ͐�����``""``�ň͂܂�Ă���̂ŕ�����ƂȂ�܂��B�����``()``�̒��ł͕�����̘A���Ƃ��ď�������܂��B
6�s�ڂ͐��������̂܂܏�����Ă���̂Ő��l�����ƂȂ�܂��B�����``()``�̒��ł͐��l�̌v�Z�������s���܂��B
���l�ƕ�����̈Ⴂ�͏�Ɉӎ����ăR�[�h�������Ă����܂��傤�B
***
## 0.3. main���\�b�h�̍\��
���̍���main���\�b�h�̍\���ɂ��Đ������܂��B
~main���\�b�h�͂��܂��Ȃ��̂悤�Ȃ��̂Ȃ̂ŁA�ŏ��͂��̍\���̎�������Ȃ��Ă��ǂ��Ǝv���܂�~
~~~java
public static void main(String args[]){
}
~~~
Java�� main���\�b�h�̐錾�ł́A�����̏��������ׂĖ������Ă���K�v������܂��B

+ �A�N�Z�X�C���q
+ static�C���q
+ �߂�l
+ ���\�b�h��
+ ����


### �A�N�Z�X�C���q
**<span style="color: red; ">public</span>** _static void main(String[] args)_
�����͕K��``public``�ł���K�v������Apublic�̓v���O�����̌��J�͈͂��Ӗ����Ă�����Apublic�C���q��t�������\�b�h�́A���\�b�h�̒�`���̃N���X�̊O���A�O���̃R�[�h����A�N�Z�X�ł���悤�ɂȂ�܂��B

### static�C���q
_public_ **<span style="color: red; ">static</span>** _void main(String[] args)_
static�C���q��t�������\�b�h�́A�N���X��**�C���X�^���X��**[^1]���邱
�ƂȂ��A�N�Z�X�ł���悤�ɂȂ�܂��B
static�C���q���t���Ă��郁�\�b�h�̎���ÓI���\�b�h�ƌ����܂�

### �߂�l
_public static_ **<span style="color: red; ">void</span>** _main(String[] args)_
main���\�b�h�̖߂�l�͕K��**void**[^2]�łȂ���΂Ȃ�܂���B

### ���\�b�h��
_public static void_ **<span style="color: red; ">main</span>** _(String[] args)_
���\�b�h���͕K���S��������`main`�łȂ���΂Ȃ�܂���B
JVM���Q�Ƃ��鎯�ʎq�ł��B
### ����
_public static void main_ **<span style="color: red; ">(String[] args)</span>** 
���\�b�h�̈����ɂ�`String�^�̔z��`�A�܂���`String�^�̉ϒ�����`�ł��邱�Ƃ��K�v�ł��B
�܂��A`args`�̓v���O���������s�����Ƃ��ɓn���������Ӗ����Ă��܂��B
***

## 0.4. java�t�@�C����class�t�@�C��
�O�̍���`Main.java`����`helloworld`�����s�����Ǝv���܂����A�R���p�C���������ۂ�`Main.java`���쐬�����t�H���_�̒���`Main.class`���쐬���ꂽ���Ǝv���܂��BJava�̃v���O���������s���邽�߂ɕK�v�ȏ���������ł��B
**Java��<span style="color: #ff00ff; ">�I�u�W�F�N�g�w���v���O���~���O����</span>�ŁA�I�u�W�F�N�g�Ƃ������̂��`���Ďg���܂��B�I�u�W�F�N�g��class�Œ�`����܂��B**

***
**Java�̃v���O���~���O�̊�{�I�ȗ���͈ȉ��̂悤�ɂȂ�܂��B**

1. �\�[�X�t�@�C���i`.java`�j���쐬����
2. �R���p�C���i`javac`�j���g���ă\�[�X�t�@�C�����o�C�g�R�[�h�i`.class`�j�ɕϊ�����
3. JVM[^3]���g���ăo�C�g�R�[�h(`.class`)�����s����



[^1]: new���Z�q�Ȃǂ��g���C���X�^���X�𐶐����邱��
[^2]: ���\�b�h�̏������ʂ��Ăяo�����֕Ԃ��K�v���Ȃ��ꍇ�ɂ���߂�l�̌^
[^3]: JavaVirtualMachine�̗��ŁAJava�ō쐬���ꂽ�A�v���P�[�V������Windows��MacOS�Ȃǂœ��������߂ɕK�v�ƂȂ�A�v���P�[�V�����ł��B
