# 5.��O����

**��O�����Ƃ̓v���O�����̎��s���ɑz��O�̎��Ԃ⎖�ۂ����������Ƃ��ɁA���̑Ή����L�q�����R�[�h�̂��Ƃł�**
������s�����Ńv���O�����̈��S�������߂邱�Ƃ��ł��܂�

## 5.0. ��O

Java�̗�O��**Throwable�N���X**���p������**Error�N���X**�ƁA**Exception�N���X**�ɕ��ނ���܂��B

+ **Error�N���X**�́A**�v���O�����őΏ��ł��Ȃ��d��ȃG���[**��\���܂��B
�Ⴆ�΁A`OutOfMemoryError`��`ClassFormatError`�Ȃǂ�����܂��B

+ **Exception�N���X**�́A**�v���O�����őΏ��ł���\���̂���G���[**��\���܂��B
�Ⴆ�΁AIOException��NullPointerException�Ȃǂ�����܂�

**Exception�N���X**�͂���ɁA**������O**��**�񌟍���O**�ɕ������܂��B

+ **������O**��**�R���p�C�����Ƀ`�F�b�N������O**�ŁAtry-catch����throws�錾�ŏ������Ȃ���΂Ȃ�܂���B
+ **�񌟍���O**��**�R���p�C�����Ƀ`�F�b�N����Ȃ���O**�ŁARuntimeException�N���X�̃T�u�N���X�ł�

**�悭�g���錟����O**
| ��O | ������P�[�X |
| ----|----|
|IOException|�t�@�C�����o�͂Ɋւ���G���[����������P�[�X|
|SQLException| �f�[�^�x�[�X����Ɋւ���G���[����������P�[�X|

**�悭�g����񌟍���O**
| ��O | ������P�[�X |
| ----|----|
|IllegalArgumentException| ���\�b�h���Ăяo���ꂽ�ۂɈ����̒l���������Ȃ��P�[�X|
|NullPointerException| null���֎~����Ă��������null���n�����P�[�X|
|IndexOutOfBoundsException|�z��⃊�X�g�Ȃǂ̃R���N�V��������͈͊O�̗v�f���擾���悤����P�[�X|
|ArithmeticException| �Z�p���Z�ŕs���Ȓl�����������P�[�X|

## 5.1. throw

**throw�Ƃ́A�G���[�𔭐������邽�߂̃L�[���[�h�ł��B**
��O�N���X�̃C���X�^���X���쐬����`throw`���邱�ƂŁA�G���[��\���ł��܂��B

~~~java
throw new ��O�N���X(���b�Z�[�W);
~~~

***

## 5.2. try catch

**try-catch�Ƃ́A�G���[����������\���̂���R�[�h�u���b�N��try�ň͂݁Acatch�̒��ŃG���[�����������ꍇ�ɍs�������������s���ׂ̕��ł�**

~~~java
try {
  // ��O����������\���̂��鏈��
} catch (��O�N���X �ϐ���) {
  // ��O�������������̏���
}

try {
  // ��O����������\���̂��鏈��
} catch (��O�N���X �ϐ���) {
  // ��O�������������̏���
} finally {
    //�K�����s����鏈��
}
~~~

`try`�u���b�N�ɂ͗�O����������\���̂���R�[�h���L�q���A
`catch`�u���b�N�ɂ͗�O�����������Ƃ��Ɏ��s����R�[�h���L�q���Ă��܂��B
`finally`�u���b�N�ɂ́A�Ō�ɕK�����s����R�[�h���L�q���Ă��܂��B
�����̃u���b�N�́A�v���O�����̈��S����ǐ������߂邽�߂ɏd�v�ł�

~~~java
int person = 0;
int candy = 100;
try {
    candy = 100 / person; //�[�����Z�G���[
    System.out.println("candy / person : " + candy);
} catch (ArithmeticException e) {
    System.out.println("��O���������܂���");
    System.out.println(e);
} finally {
    System.out.println("person : " + person);
}
~~~

~~~java
���s���ʁF
��O���������܂���
java.lang.ArithmeticException: / by zero
person : 0
~~~

��L�̃R�[�h�����Ă݂܂��傤�B
�ϐ�`candy`��`100 / 0`�����悤�Ƃ��Ă��܂��ˁB���w�ɂ�����0�Ŋ����Ă͂����Ȃ��Ƃ������[��������ׁA`100/0`�����悤�Ƃ���ƃG���[���N���Ă��܂��܂��B
�����ŁA�G���[�̉\��������`candy = 100 / person`��`try`�ň͂݁A`catch`�ɃG���[���N���Ă��܂������̏����������܂��B��L�̃R�[�h�ł̓G���[���N�������ɃX���[���ꂽ`java.lang.ArithmeticException: / by zero`�Ƃ�����O���o�͂��Ă��܂��B
`finally`�ň͂܂ꂽ�����͗�O���������Ă����Ȃ��Ă��K�����s����܂��B��Ƀt�@�C����close���������ȂǂɎg���܂��B

## 5.3. throws

**throws�́A���\�b�h�̐錾�̌�ɋL�q����L�[���[�h�ŁA���̃��\�b�h������������\���̂����O��񋓂��邱�Ƃ��ł��܂��B**
`throws`���g���ƁA���̃��\�b�h���Ăяo�����ɗ�O������C���邱�Ƃ��ł��܂��B

~~~java
void something() throws Exception {
  // ��O����������\���̂���R�[�h
}
~~~

�܂��A`throws`�L�[���[�h�͕��������܂��B���\�b�h������������\���̂����O�̎�ނ���������ꍇ�́A�J���}`,`�ŋ�؂��ė񋓂��邱�Ƃ��ł��܂�

~~~java
import java.io.FileNotFoundException;
import java.io.FileReader;
public class Main {
    public static void main(String[] args) {
    String fpath = "Sample.txt";//�ǂݍ��݂����t�@�C���p�X
    try {
        readFile(fpath);//readFile���\�b�h�Ƀp�X�𓊂���
    } catch (Exception e) {
        //�@�t�@�C�������������ꍇ�̏���
    }

    }
    public static void readFile(String path) throws FileNotFoundException {
        FileReader r = new FileReader(path);
        /* 
        *�t�@�C���ǂݍ��ݏ���
        */

    }   
}
~~~

��L�̃R�[�h��main���\�b�h����`readFile`���\�b�h��`FileReader`�N���X���g�p���Ă���̂ŃG���[���������{����K�v������܂��B

��O������`throws`���g���ČĂяo�����̃N���X�ɓ����Ă��܂��B
throws�ŌĂяo�����̃N���X�ɗ�O�����𓊂�����̏����͒��~����A��O������main���\�b�h��catch���Ă��̌㏈�������Ă��܂��B

## 5.4. ��O�̓ǂݕ�

`Main.java`�ňȉ��̃R�[�h�����s���悤�Ƃ���ƃG���[���������܂��B

~~~java
public class Main {
    public static void main(String[] args) {
        String str = null;
        System.out.println(str.length());
    }
}
~~~

~~~java
���s���ʁF
Exception in thread "main" java.lang.NullPointerException: Cannot invoke "String.length()" because "str" is null at Main.main(Main.java:4)
~~~

��L�̃R�[�h�́A������`str`�̒������o��`.length()`���\�b�h���Ăяo�����Ƃ��Ă��܂����A`str`��`null`�Ȃ̂ŁA�G���[���o�Ă��܂��Ă��܂��B

`Exception in thread "main" java.lang.NullPointerException: ~~`
���̕����ł�`NullPointerException`�Ƃ����G���[�̓��e���킩��܂��B
`at Main.main(Main.java:4)`
���ɁA���̕����ł̓G���[���N�����ӏ��𖾎����Ă��܂��B�T���v���̏ꍇ���ƁA
�u`Main`�Ƃ����N���X��`main`���\�b�h�̒��ŃG���[���������Ă܂��B�܂����̃G���[��`Main.java`�Ƃ����t�@�C����4�s�ڂɂ���܂��B�v�Ƃ����Ӗ��ł�

�G���[���b�Z�[�W�͎��̂悤�Ȍ`�����܂��B

``at �N���X��.���\�b�h��(�t�@�C����.java: �G���[���N�����s)``

``at �p�b�P�[�W��.�N���X��.���\�b�h��(�t�@�C����.java: �G���[���N�����s)``
