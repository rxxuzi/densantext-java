# 9. �R���N�V����

List, Set, Map�ɂ��Đ������܂�

## 9.1. List

Java�ɂ�����`List`�́A�����̗v�f��ێ����邱�Ƃ��ł���I�u�W�F�N�g�ł��B
`List`�́A�z��Ɏ����f�[�^�\���ŁA**���I**�ɗv�f����ύX���邱�Ƃ��ł��܂��B
`List`�Ɋi�[�����v�f�́A�C���f�b�N�X�ɂ���ăA�N�Z�X���邱�Ƃ��ł��܂��B

List�́A`java.util�p�b�P�[�W`�ɑ����Ă���̂ŁA�g�p����ۂɂ̓C���|�[�g����K�v������܂��B``List``�ɂ�`ArrayList`�A`LinkedList`�A`Vector`�Ȃǂ̃N���X����������Ă��܂��B
���ꂼ��̃N���X�ɂ́A`List�C���^�[�t�F�[�X`���������Ă��邽�߁A�����悤�ȕ��@�Ŏg�p���邱�Ƃ��ł��܂��B

�ȉ��́A`ArrayList`���g�p����List�̗�ł��B
ArrayList�́A**�ϒ��̔z��Ƃ��Ď�������Ă���**�A**�v�f�̒ǉ���폜�������ɍs���܂��B**

~~~java

import java.util.ArrayList;
import java.util.List;

public class Example {
    public static void main(String[] args) {
        // List�̍쐬
        List<String> language = new ArrayList<String>();

        // �v�f�̒ǉ�
        language.add("java");
        language.add("c++");
        language.add("python");
        language.add("scala");

        // �v�f�̎擾
        String item = language.get(1);  // item �� "c++" ����
        System.out.println(item);   

        // �v�f�̍폜
        language.remove(2);  // "python"���폜

        // �v�f�����擾
        int size = language.size();  // 3

        // �v�f�̃��[�v (�g��for��)
        for (String s : language) {
            System.out.println("Hello " + s);
        }

        // �v�f�̏�������
        language.set(2,"kotlin"); // �v�f(2)��scala��kotolin�ɏ�������
        System.out.println(language);
    }
}

~~~

�o�́F

~~~text
c++
Hello java
Hello c++
Hello scala
[java, c++, kotlin]

~~~


�錾�̎d��

~~~java

List<String> list = new ArrayList<String>();
~~~

��L�̗�ł́AList�̓C���^�[�t�F�[�X�ł���AArrayList��List�C���^�[�t�F�[�X����������**�N���X**�ł��B`<String>`�́A**List�Ɋi�[�����v�f�̌^**�������Ă��܂��B
���̏ꍇ�A��������i�[���邽�߂�`String`���g�p���Ă��܂��B

## 9.2. Set

Java�ɂ�����`Set`�́A�d���̂Ȃ���ӂȗv�f�̃R���N�V������\�����߂̃f�[�^�\���ł��B
`Set`�́A�W���_�̊T�O�Ɋ�Â��Ă���A�v�f�̏����͕ۏ؂���܂���B
�܂��A`Set`�́A�v�f�̏d���������Ȃ����߁A�����l�𕡐���i�[���邱�Ƃ͂ł��܂���B

Java��Set�ɂ́A`java.util�p�b�P�[�W`�Ɋ܂܂��`HashSet`�A`TreeSet`�A`LinkedHashSet`�Ȃǂ�����܂��B
���ꂼ��̃N���X�ɂ́A`Set�C���^�[�t�F�[�X`���������Ă��邽�߁A�����悤�ȕ��@�Ŏg�p���邱�Ƃ��ł��܂��B

�ȉ��́A`HashSet`���g�p����Set�̗�ł��B`HashSet`�́A**�v�f�̒ǉ���폜�������ɍs���܂��B**

~~~java
import java.util.HashSet;
import java.util.Set;

public class Example {
    public static void main(String[] args) {
        // Set�̍쐬
        Set<String> set = new HashSet<String>();

        // �v�f�̒ǉ�
        set.add("apple");
        set.add("banana");
        set.add("orange");

        // �v�f�̎擾
        boolean contains = set.contains("banana");  // true

        // �v�f�̍폜
        set.remove("orange");

        // �v�f�̐����擾
        int size = set.size();  // 2

        // �v�f�̃��[�v
        for (String s : set) {
            System.out.println(s);
        }
        // "apple"
        // "banana"
    }
}

~~~
