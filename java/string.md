在google+上看到一篇面试题，[java面试题，看看输出是什么？][1]，其中涉及到了string
对象的用法。

内容
=======
    public static void swap(String a,String b){
        	 String temp = a;
        	 a = b;
        	 b = temp;
    }
         
    public static void main(String[] args){
        	 String a = "hello,world";
        	 String b = "test";
        	 swap(a,b);
        	 System.out.println(a);
        	 System.out.println(b);
    }
这样输出的结果是什么？

答案
=======
    hello,world
    test

分析
========
[stackoverflow-java pass by reference][2]



> Written with [StackEdit](http://benweet.github.io/stackedit/).


  [1]: http://www.codelect.net/InterviewQuestions/Java%20Junior%20Level%20Test
  [2]: http://stackoverflow.com/questions/40480/is-java-pass-by-reference/40523#40523