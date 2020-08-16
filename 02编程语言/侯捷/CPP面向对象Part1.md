# C++面向對象編程 (C++Object-Oriented Programming) Part I 

## Introduction of C++98, TR1, C++11, C++14 

### Bibliography 
### Data and Functions, from C to C++ 
* C
  * Data，Functions 》》variables
* C++
  * Data Members， MemeberFuntions 》》objects
### Basic forms of C++ programs 
### About output 
### Guard declarations of header files 
* 防卫式声明
### Layout of headers 
* forward declarations 前置声明
* class declaration 类声明
* class definition 类定义
### Object Based 
* 基于对象，OO 面向对象

### Class without pointer member (complex 复数)

* Class declarations 
* Class template, introductions and overviews 简介
* What is 'this' 
* Inline functions 内联函数
* Access levels 
* Constructor (ctor) 
  * 默认实参
  * 初值列，初始列。不要赋值
  * 重载
  * singleton 单例模式，放在 private 区
* Const member functions 
* Parameters : pass by value vs. pass by reference 
* Return values : return by value vs. return by reference 
  * 不能返回局部变量的引用
* Friend 
  * 相同 class 的各个 objects 互为 friends 友元
* Definitions outside class body 
* Operator overloading, as member function 
  * 便于使用级联 << xxx <<
* Return by reference, again 
* Operator overloading, as non-member function 
  * 无 this
* Temporary objects 
  * 不可以 return by reference
* Expertise 
* Code demonstration

### class with pointer members (string 字符串)

* The "Big Three" ，`class with pointer members 必须要有`
  * Copy Constructor 
  * Copy Assignment Operator 
  * Destructor
* Ctor and Dtor, in our String class
* "MUST HAVE" in our String class 
  * Copy Constructor 
  * Copy assignment operator
* Deal with "self assignment" 
  * `一定要在 operator= 中检查`
* Another way to deal with "self assignment" : Copy and Swap 
* Overloading output operator (<<) 
* Expertise 
* Code demonstration

### Objects from stack vs. objects from heap 

* Objects lifetime 
  * stack objects 在作用域 scope 结束之际结束，又称为 auto object，会被自动清理
  * static objects 作用域结束后仍然存在，直到整个程序结束
  * global objects，在整个程序结束之后才结束，可视为一种 static object
  * heap objects，deleted 之际结束，内存泄漏 memory leak
* new expression : allocate memory and then invoke ctor 
  * 先分配 memory 再调用 ctor
    ```cpp
    void* mem = operator new(sizeof(Complex));  // 分配内存，内部调用 malloc
    pc = static_cast<Complex*>(mem);    // 转型
    pc->Complex::Complex(1, 2); // 构造函数
    ```
* delete expression : invoke dtor and then free memory 
  * 先调用 dtor，再释放 memory
  ```cpp
  Complex::~Complex(pc);    // 析构函数
  operator delete(pc);  // 释放内存
  ```
* Anatomy ofmemory blocks from heap 
  * 编译器内存管理，头尾各 4 位的标志
  * 内存对齐
* Allocate an array dynamically 
  * 标志位
  * 内存对齐
* new[] and delete[]

### MORE ISSUES : 

* static 
* private ctors 
* cout 
* Class template 
* Function template 
* namespace 
* Standard Library : Introductions and Overviews

### Object Oriented 

* Composition means "has-a" 
  * Construction : from inside to outside 
  * Destruction : from outside to inside
* Delegation means "Composition by reference" 
* Inheritance means "is-a" 
  * Construction : from inside to outside 
  * Destruction : from outside to inside
* Construction and Destruction, when Inheritance+Composition 
* Inheritance with virtual functions 
  * non-vitual 函数，不希望子类重新定义（override 覆写）它
  * vitual 函数，希望子类 override 它，且对它已有默认定义。
  * pure vitual 函数 = 0，希望子类 override，且没有默认定义。
* Virtual functions typical usage 1 : Template Method 
* Virtual functions typical usage 2 : Polymorphism 
* Virtual functions inside out : vptr, vtbl, and dynamic binding 
* Delegation + Inheritance : Observer 
* Delegation + Inheritance : Composite
* Delegation + Inheritance : Prototype