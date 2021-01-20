# java笔记

## 泛型

### why?

https://www.cnblogs.com/gxyjava/p/11790987.html

```java
public class Stack

{

   private int Age;

   public int getAge();

   public Stack(int i)

   {

       this.Age = i;

   }

}

/*这个栈只能处理int数据类型
我们需要一个栈来保存String类型时，该怎么办呢
*/
```

```java
public class Stack

{

   private Object Age;

   public Object getAge();

   public Stack(Object i)

   {

       this.Age = i;

   }

}
/*
解决了为不同类型的数据创建大量相似类的情况。
但是：
1.放入对象很随意，往int堆里放string

2.拿出对象默认拿出Object，需要进行类型转换，编译时可能不报错，因为Object必定是int的父类，但类型转换时，int强制转化为string是必定会出错的。
int x =6;
Stack a=new Stack(x);
string y = (string)stack.getAge();
3.对象类类型不统一，难以启用增强for循环，
for(String s :list)
{
System.out.println(s);
}
*/

*/
```



```java
public class Stack<T>

{
   private T Age;

   public T getAge();

   public Stack(T i)
   {
       this.Age = i;
   }
}
/*
类的写法不变，知识引入了通用类型T就可以适用于任何数据类型
*/
```



### what?



### how?

