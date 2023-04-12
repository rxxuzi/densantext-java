# 6�@�z��

**�z��Ƃ́A�����^�̗v�f�𕡐��܂Ƃ߂Ĉ������Ƃ̂ł���f�[�^�\���ł��B**

## 6.1.�@��`, �錾

~~~java
�v�f�^[] �ϐ��� = new �v�f�^[�z��T�C�Y];
�v�f�^[] �ϐ��� = new �v�f�^[]{�v�f0,�v�f1,�v�f2....};
~~~

�z��Ɋ܂܂��v�f��0���珇�Ԃɕ��ׂ��Ă��܂��B���̔ԍ���**�C���f�b�N�X**�Ƃ����܂��B���̃C���f�b�N�X��p���Ĕz�񒆂̗v�f�̎擾��X�V���s���܂��B�����A**�z��̃T�C�Y�͈�x��������ƌォ��ύX���邱�Ƃ��ł��܂���**

�܂��A���ׂĂ̗v�f�͓����^�ł���K�v������܂��B
�z��̗v�f�̌^�́A**��{�f�[�^�^�ƎQ�ƌ^�ǂ�����g�����Ƃ��ł��܂�**�B

~~~java

int[] a = {1,2,3,4,5};

int[] b = new int[5];//�z��̐錾
for (int i = 0; i < b.length; i++) {
    b[i] = i+1; // �C���f�b�N�Xi���Ƃ�i+1�̒l����
}
int[] c = new int[]{1,2,3,4,5};

System.out.println(a[0]);
System.out.println(b[1]);
System.out.println(c[2]);
~~~

~~~java
���s���ʁF
1
2
3
~~~

�z��͐錾�E���������i�K�ŁA�z��̊e�v�f�ɗ\�ߏ����l���ݒ肳��܂��B���̂��߃R���p�C���G���[�ɂȂ�܂���B�����l�́A�z��̌^�ɂ��قȂ�܂��B

|�z��^|�����l|
|--|--|
|int�Ȃǂ̐��l�^|0|
|boolean|false|
|�Q�ƌ^|null|

~~~java
int[] a = new int[10];
System.out.println(a[9]);
String[] b = new String[10];
System.out.println(b[9]);
~~~

~~~java
���s���ʁF
0
null
~~~

���̂悤�ɁA�z��ɑ΂��ėv�f�����傫���C���f�b�N�X�ɃA�N�Z�X���悤�Ƃ����
`ArrayIndexOutOfBoundsException`���������܂�

~~~java
int[] a = new int[]{1,2,3,4,5};
System.out.println(a[5]);
~~~

~~~
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 5 out of bounds for length 5 
~~~

�܂��A�z��̗v�f�̐�����**length�t�B�[���h**����擾���邱�Ƃ��ł��܂��B

~~~java
String[] str = new String[]{"Red" , "Green" , "Blue"};
System.out.println(str.length);
int a[] arr = new int[10];
System.out.println(arr.length);
~~~

~~~java
���s���ʁF
3
10
~~~

## 6.2. �������z��

�z��̗v�f�Ƃ��Ĕz����������Ƃ��ł��܂��B
2�����z��̏ꍇ��

~~~java
�v�f�^[][] �ϐ��� = new �v�f�^[�z��T�C�Y][�z��T�C�Y];
�v�f�^[][] �ϐ��� = new �v�f�^[][]{�v�f0,�v�f1..}{�v�f0,�v�f1..};
~~~

�Ɛ錾���܂�

~~~java

int[][] p = new int[][]{
    { 0, 1, 2, 3},
    { 4, 5, 6, 7},
    { 8, 9,10,11},
    {12,13,14,15}
};

System.out.println(p[0][3]);
System.out.println(p[3][2]);
~~~

~~~java
���s���ʁF
3
14
~~~

## 6.3. ArrayList


