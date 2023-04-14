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

---

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

        // �v�f�̒ǉ� (�v�f�� = 4)
        set.add("java");
        set.add("c++");
        set.add("python");
        set.add("html");
        
        // �v�f�̎擾
        String element = "c++";
        boolean contains = set.contains(element);  // true
        if(contains) { //true
            System.out.println("Elements include");
        }

        // �v�f�̍폜
        set.remove("python");

        // �v�f�̐����擾
        int size = set.size();  // remove�����̂�3
        System.out.println(size);
        
        boolean isE = set.isEmpty(); //false
        
        if(!isE) { // !false -> true
            // �v�f�̃��[�v(�g��for��)
            for (String s : set) {
                System.out.println(s);
            }
        }
        
    }
}

~~~

~~~text
Elements include
3
c++
java
html

~~~

---

## 9.3. Map

Java��`Map`�́A�L�[�ƒl�̃y�A���i�[����f�[�^�\���ł���A�L�[���g���Ēl�ɃA�N�Z�X���邱�Ƃ��ł��܂��B
`Map`�́A`java.util�p�b�P�[�W`�Ɋ܂܂��N���X�ł���A`HashMap`�A`TreeMap`�A`LinkedHashMap`�Ȃǂ�����܂��B
���ꂼ��̃N���X�ɂ́A`Map�C���^�[�t�F�[�X`���������Ă��邽�߁A�����悤�ȕ��@�Ŏg�p���邱�Ƃ��ł��܂��B

�ȉ���`HashMap`���g�p����Map�̗�ł��BHashMap�́A**�L�[�ƒl�̒ǉ��A�擾�A�폜�������ɍs���܂��B**

~~~java

import java.util.HashMap;
import java.util.Map;

public class Example {
    public static void main(String[] args) {
        // Map�̍쐬
        Map<String, Integer> map = new HashMap<String, Integer>();

        // �v�f�̒ǉ�
        map.put("A", 100);
        map.put("B", 200);
        map.put("C", 300);

        // �v�f�̎擾
        int value = map.get("A");  // 100

        // �v�f�̍폜
        map.remove("B");

        // �v�f�̐����擾
        int size = map.size();  // 2

        // �L�[�̃��[�v
        for (String key : map.keySet()) {
            System.out.println(key + " : " + map.get(key));
        }
    }
}

~~~
