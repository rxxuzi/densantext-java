# 7.�W������
**�R�}���h���C������̓��͂��󂯎���ăv���O��������蓮�I�ɂ���ׂɕW�����͂��s���܂��B**

## 7.1. Scanner
Java�ɂ����āA�W�����͂��󂯎�邽�߂ɂ�`java.util.Scanner`�N���X���g�p���܂��BScanner�N���X�́A�R�}���h���C������̓��́A�t�@�C������̓��́A�܂��͕����񂩂�̓��͂��󂯎�邱�Ƃ��ł��܂��B
~~~java
�R�}���h���C�����當������󂯎���āA"Hello (������)"�Əo�͂���R�[�h
~~~
```java
import java.util.Scanner;
public class Main{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Your Name");
        String str = sc.nextLine();
        System.out.println("Hello " + str);
        sc.close();
    }
}
```
~~~
���́F
Java!
�o�́F
Hello Java!
~~~
***
��L�̃T���v���R�[�h�ł͂܂��A`Scanner`�N���X���C���|�[�g���Ă��܂��B
```java
import java.util.Scanner;
```
`Scanner`�N���X��`java.util�p�b�P�[�W`�ɂ���N���X�ŁA�R�}���h���C������̓��͂�t�@�C������̓��͂�ǂݍ��񂾂�A�w�肵���^�̒l���\����͂����肷�邽�߂Ɏg���܂��B
�܂��A
~~~java
import java.util.*;
~~~

�ƃA�X�^���X�N`*`�����邱�ƂŁA`java.util�p�b�P�[�W`�ɂ���S�ẴN���X���C���|�[�g���鎖���ł��܂��B
**Java�̊��K�Ƃ��āAimport���̓\�[�X�R�[�h�̐擪�ɁA�p�b�P�[�W�錾�̉��ɋL�q���܂�**
***
```java
Scanner sc = new Scanner(System.in);
```
���̍s�ł�Scanner�N���X�̃C���X�^���X���쐬���Ă��܂��B

Scanner�N���X�̃C���X�^���X���쐬����Ƃ��ɂ́A`System.in`���R���X�g���N�^�̈����Ɏw�肵�܂��B���̃R�[�h�ł�Scanner�N���X�̃C���X�^���X���Q�Ƃ���ϐ�����`sc`�ɂ��Ă��܂��B

Java��`new`�L�[���[�h�́A�N���X�̃C���X�^���X���쐬����Ƃ��Ɏg���܂��B�܂�A**�V�����I�u�W�F�N�g�̂��߂Ƀ����������蓖�ĂāA���̃������ւ̎Q�Ƃ�Ԃ�**�Ƃ������Ƃł��B
***
~~~java
String str = sc.nextLine();
~~~
���̍s�ł͕�����̕ϐ�`str`�ɓ��͂��ꂽ������������Ă��܂��B


Scanner�N���X�́A���̂悤�Ȉ�A�̃��\�b�h��񋟂��Ă��܂��B

+ `next()`: �X�y�[�X����s�܂ł̎��̃g�[�N����ǂݍ��݂܂��B
+ `nextLine()`: ���̍s�܂ł̕������ǂݍ��݂܂��B
+ `nextInt()`: ���̐�����ǂݍ��݂܂��B
+ `nextDouble()`: ���̕��������_����ǂݍ��݂܂��B
+ `hasNext()`: ���̃g�[�N�������݂��邩�ǂ����𔻒f���܂��B
+ `close()`: ���̓X�g���[������܂��B
***
~~~java
sc.close();
~~~
���̍s�ł�Scanner�N���X��`close()`���\�b�h���Ăяo����Scanner����Ă��܂��B
`close`���\�b�h���Ăяo�����ƂŁB���\�[�X�̉����G���[�̉���Ȃǂ��ł��܂�

���̃��\�b�h�ɂ��Ă�Oracle�����y�[�W���Q�l�ɂ��Ă��������B
[Oracle�����y�[�W Scanner�N���X](https://docs.oracle.com/javase/jp/8/docs/api/java/util/Scanner.html)

