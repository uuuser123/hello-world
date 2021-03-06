C和C++的区别
从C到C++
C语言是1972年由美国贝尔实验室研制成功的，在当时算是高级语言，它的很多新特性都让汇编程序员羡慕不已，就像今天的Go语言，刚出生就受到追捧。C语言也是”时髦“的语言，后来的很多软件都用C语言开发，包括 Windows、Linux 等。但是随着计算机性能的飞速提高，硬件配置与几十年前已有天壤之别，软件规模也不断增大，很多软件的体积都超过 1G，例如 PhotoShop、Visual Studio 等，用C语言开发这些软件就显得非常吃力了，这时候C++就应运而生了。

     C++ 主要在C语言的基础上增加了面向对象的机制，以适用于大中型软件的编写。在C语言中，我们会把重复使用或具有某项功能的代码封装成一个函数，将具有相似功能的函数放在一个源文件；调用函数时，引入对应的头文件就可以。而在C++中，多了一层封装，就是类（Class）。类由一组相关联的函数、变量组成。你可以将一个类或多个类放在一个源文件，使用时引入对应的类就可以。不要小看这一层封装，它让C++多了很多特性，成为面向对象的编程语言。
C和C++的关系：就像是win98跟winXP的关系。C++是在C的基础上增加了新的理论，玩出了新的花样。所以叫C++。
C是一个结构化语言，它的重点在于算法和数据结构。C程序的设计首要考虑的是如何通过一个过程，对输入（或环境条件）进行运算处理得到输出（或实现过程（事务）控制）。
C++，首要考虑的是如何构造一个对象模型，让这个模型能够契合与之对应的问题域，这样就可以通过获取对象的状态信息得到输出或实现过程（事务）控制。 所以C与C++的最大区别在于它们的用于解决问题的思想方法不一样。之所以说C++比C更先进，是因为“ 设计这个概念已经被融入到C++之中 ”。 
一、类，类对于初学者，它是一个累赘。类的封装使得初学者对程序产生厌倦，感到不适和麻烦。
二、引用，引用是C++中最好尽量不要用它，除非万不得已。引用对于初学者就更容易产生混淆，不知道哪个是引用，哪个是变量。
三、函数的重载，初学者学函数的重载好像没什么坏处，但是，这会使初学者潜意识里对C语言的变量类型的重要性产生淡化，要记住C语言是对变量类型最敏感了的，变量的类型在C语言里的重要性是不言而喻的。
四、流操作符，和上面同样的道理，使得对变量类型的重要性产生淡化，有时会产生使初学者莫名其妙的结果。
五、操作符重载，典型的高级应用，初学者可能根本用不着，这个东东会让他们觉得C++很难，门槛高，看不懂。
六、继承，以及虚函数，看起来深奥，实用价值很低。还有些东东我就不发表评论了，如：new,delete操作符等
七、误区： 
C++并非完全面向对象化，真正的面向对象化的语言恐怕只有Java才算得上。
C与C++的最大区别：在于它们的用于解决问题的思想方法不一样。之所以说C++比C更先进，是因为“ 设计这个概念已经被融入到C++之中 ”，而就语言本身而言，在C中更多的是算法的概念。算法是程序设计的基础，好的设计如果没有好的算法，一样不行。而且，“C加上好的设计”也能写出非常好的东西。
对语言本身而言，C是C++的子集，那么是什么样的一个子集？从上文可以看出， C实现了C++中过程化控制及其它相关功能，而在C++中的C（我称它为“C+”），相对于原来的C还有所加强，引入了重载、内联函数、异常处理等等玩艺儿，C++更是拓展了面向对象设计的内容，如类、继承、虚函数、模板和包容器类等等。 再提高一点，在C++中，数据封装、类型这些东东已不是什么新鲜事了，需要考虑的是诸如：对象粒度的选择、对象接口的设计和继承、组合与继承的使用等等问题。
所以相对于C，C++包含了更丰富的“设计”的概念，但C是C++的一个自洽子集，也具有强大的功能，同样值得学习
C和C++是两门不同的语言，在平常使用中经常出现混编的情况，因此，搞清楚C和C++语法的某些差别很重要，使得我们清楚哪些语句是可以写在c文件里，哪些只能写在cpp文件里的。
1，在C++中局部变量可以在一个程序块内在任何地方声明,在C中局部变量必须在程序块的开始部分,即在所有"操作"语句之前声明,请注意,C99标准中取消了这种限制。例如：在C++中，for语句中可以出现for(int i=0;i<5;i++)，即定义i的同时使用它；但在C中不能这样，只能先定义，然后再使用。int i;for(i=0;i<5;i++)。
2，在C中,按如下方式声明的函数没有对函数参数进行任何说明;
    int func();
也就是说,如果没有在函数后面的括孤内指定任何参数,这在C中就意味着对函数参数未做任何声明,该函数可能有参数,也可能没有参数,然而,在C++中,这样的函数声明意味着该函数没有参数,也就是说,在C++中,下面这两个函数声明具有同样的作用:
    int func();
    int func(void);
    在C++中,参数列表中的void是任选的.许多C++程序员使用它们是为了表明函数没有任何参数的,以便于他人理解程序.但是,从技术上说,void不是必须的。
3，在C++中,所有函数均必须被设计成原型,但这在C中只是一种选择.编程经验表明,在程序中也应该给函数采用原型设计方法。
4，在C与C++之间还存在一个重要而又细微的差别,即字符常数在C中被自动作为整形来处理,但在C++中则不然.
5，在C中,多次声明一个全局变量虽然不可取,但不算错.在C++中,多次声明同一个全局变量会引发错误.
6，在C中,一个标识符可以至少31个有效的组成字符.在C++中,一个标识符的所有组成字符均是有效的.可是,从实用角度看,过长的标识符没有太大的用处,不仅不便于记忆,而且还会增加出现打字错误的可能性.
7，在C中,在程序内部调用main()函数的情形不常见,但这种做法是容许的,在C++中,这种做法是不容许的. 
8，在C中,无法获得register型的地址,在C++中则可以获得这种地址.
9，在C中,如果类型声明语句中没有指定类型名,该类型被假定成int,这种隐式转型在C99与C++中是不允许的.
10，标准C++所定义的新式头部文件,新式C++头部文件不再使用.h扩展名。如：
#include <iostream>
#include <cmath>
11，类与结构体的区别:类与结构体是相互关联的
   结构是C的一部分,C++从C中继承了结构,在语法上,类与结构十分相似,在关系上,这两者也很接近,在C++中,结构的作用被拓宽了,进而使结构成为了类的一种替代方法.实际上,类与结构的惟一区别在于:在默认状态下,结构的所有成员均是公有的,而类的所有成员是私有的.除此之外,类与结构是等价的,也就是说,一个结构定义了一个类的类型.
   C++同时包含这两个等价的关键字struct与class基于3个方面的原因.第一,加强结构的能力.在C中,结构提供了一种数据分组方法,因而让结构包含成员函数是一个小小的改进.第二,由于类与结构是相互关联的,所有现有C代码到C++的移植变得更容易.第三,由于类与结构的等价性,提供两个不同的关键字可以使类定义自由发展,为了保持C++与C的兼容性,结构定义必须始终受它的C定义的结束.
   即使在有些地方可以使用结构来代替类,但尽量不要这么做,为了清楚起见,该用类的地方就用class关键字,该用C结构的地方就用struct关键字.
12，类与联合是相互关联的
联合也可以用来定义类.在C++中,联合包含成员函数,变量以及构造与析构函数.C++联合保留了C联合的全部特征,其中最重要的特征是所有数据元素共享内存的相同地址.与结构类似,联合的成员在默认状态下也是公有的,并且完全兼容于C.与结构一样,C++中的联合声明定义了一种特殊的类,进而意味着保持了类的封装原则.
    C++的联合有几个必须遵守的使用限制.第一,联合不能继承其他任何类型的类.第二,联合不能是基类,不能包含有虚函数成员.静态变量不能是联合的成员.联合不能使用引用成员,而且不能有任何作为成员的重载赋值运算符的对象.第三,如果一个对象包含明确的构造或析构函数,该对象不能成为联合的成员.
    C++有一个叫做匿名联合的特殊联合.匿名联合没有类型名,也不声明任何变量,只是告诉编译程序它的成员变量共享一个内存地址.但是,变量本身无需要使用常规的点运算符语法即可直接引用.
    上述联合的使用限制也适用于匿名联合,但下面这两个限制除外,第一,匿名联合所包含的元素只能是数据,不能包含成员函数,也不能包含私有或受保护元素;第二,全局匿名联合必须声明成静态的.
13，在C++中定义struct，union和enum类型的变量时，关键字struct，union和enum可以省略；在C中不能忽略。
14，在C++中，可以用const类型的整数作为数组的大小，而在C中不可以。
15，在C中，const类型的变量是对外可见的，所以只能出现在源文件中；而在C++中，const类型的变量只有内部可见，所以可以出现在头文件中。例如：在C源文件中通过语句const int i = 2;定义i，因为它是对外可见的，所以在其它的模块中可以通过声明extern const int i;来引用它；而在C++中，因为const类型的变量默认只有内部可见，如果想定义对外部可见的变量，必须用extern修饰，例如用extern const int i = 2;定义变量i，如果是在C++文件中定义一个在C中使用的变量，可以用extern "C" const int x=10;语句。
16，动态开辟内存 C中用malloc 和free，C++中用new和delete或者delete []
C语言是结构化和模块化的面向过程的语言，C++语言是面向对象的程序设计语言。C++语言是C语言的超集，也就是说学会了C++，你其实已经把C语言学会了。至于说有什么区别，应该说是编程思想的区别吧，C是基于过程的，强调的是程序的功能，以函数（功能）为中心。C++是面向对象的，强调程序的分层、分类，以抽象为基础，进行对象的定义与展示，即程序设计。具体说来话长。建议你学习C++的时候，学会用面向对象的方式思考和编程。现在在开发大项目的时候，都是应用面向对象的分析和设计的技术。

C和C++调用编译的区别
大家看WIN32 SDK的头文件，总是可以看到
ifdef __cplusplus
    extern "C"
endif
ifdef __cplusplus
endif
  这个就是直接能够体现实际编程时区别的地方. 在WIN系列下.所有的WIN32 SDK提供的LIB都是以C的形式存在的.当然，C和C++同样都支持C,STDCALL,FASTCALL调用.为什么系统提供C编译器编译的LIB而不是C++编译的LIB呢？这里其实就是C和C++编译器不同的地方.
  所有的函数名称只有在汇编编译器下才最清楚.因为经汇编编译器编译的函数不经过任何修饰.
C 的编译器编译出来的函数名称如果在汇编编译器看来一个C调用将在函数名前家下划线('_').而一个STDCALL的函数将是_FUNC@NUMBER的形式.如FUNC(void)经过编译器后成为_FUNC@0.一个FASTCALL调用的函数被编译成@FUNC@0.顺便提一下.在WIN32的编译器里不再需要PASCALL调用.VC6已经取消了对PASCALL的支持.
光看C的编译还不够，看一下C++编译器是怎么干的.在缺省情况下.一个C++的函数经过C++编译器后编译出的函数名包括函数名，所属的类，参数类型，调用约定，返回类型.而且更要命的是这么多的信息，只有函数名和类名在编译后还依稀可见.其他就是一长串的ABCD字母，根本就是无法辨认其意义的.我们在VC手册里可以看到

一个例子:

void __stdcall b::c(float)； -----------> ？c@b@@QAGXM@Z
  一个函数被编译得连名字也不知道怎么样了.这么一来.如果SDK提供的是C++编译器提供了LIB.那么可以说就无法编译任何一个完整的WIN程序.更加不用说什么混合语言编程.
  现在，VC编译器提供了个extern语句.当出现extern 'C'语句，括号里的函数将以C方式经过编译器.从而使提供库程序方便那么点. 

1，全新的程序程序思维，C语言是面向过程的，而C＋＋是面向对象的。 
2，C语言有标准的函数库，它们松散的，只是把功能相同的函数放在一个头文件中；而C++对于大多数的函数都是有集成的很紧密，特别是C语言中没有的C++中的API是对Window系统的大多数API有机的组合，是一个集体。但你也可能单独调用API。 
3，特别是C++中的图形处理，它和语言的图形有很大的区别。C语言中的图形处理函数基本上是不能用在中C++中的。C语言标准中不包括图形处理。 
4，C和C++中都有结构的概念，但是在C语言中结构只有成员变量，而没成员方法，而在C++中结构中，它可以有自己的成员变量和成员函数。但是在C语言中结构的成员是公共的，什么想访问它的都可以访问；而在VC++中它没有加限定符的为私有的。 
4，C语言可以写很多方面的程序，但是C++可以写得更多更好，C++可以写基于DOSr程序，写DLL，写控件，写系统。 
5，C语言对程序的文件的组织是松散的，几乎是全要程序处理；而c++对文件的组织是以工程，各文件分类明确。 
6，C++中的IDE很智能，和VB一样，有的功能可能比VB还强。 
7，C++对可以自动生成你想要的程序结构使你可以省了很多时间。有很多可用的工具如加入MFC中的类的时候，加入变量的时候等等。 
8，C++中的附加工具也有很多，可以进行系统的分析，可以查看API；可以查看控件。 
9，调试功能强大，并且方法多样。
面向对象三个基本特征：封装，继承，多态。
多态性相对于前二者而言是最灵活的，也是面向对象比较核心的部分。
很多重要的系统及应用，考虑到性能及开发流程，使用机构化语言（C）的更多。
只能说，使用了多态，能让某些功能的实现看起来更“优雅”。
当年C++的作者劝说UNIX的作者用C++编写系统时，后者只是微笑沉默拒绝。这其中有自己的哲学。
C语言的特点：
1）C语言是结构化语言，层次清晰，调试和维护比较容易
2）表现能力和处理能力比较强，可直接访问内存的物理地址
3）c语言实现对硬件的编辑，c语言课用语系统软件的开发，也可用语应用软件的开发，是集高级语言和低级语言的功能一体。
4）C语言效率高，可移植性强。

C++语言特点：
1、在C语言的基础上进行扩充和完善，使C++兼容了C语言的面向过程特点，又成为了一种面向对象的程序设计语言；
2、可以使用抽象数据类型进行基于对象的编程；
3、可以使用多继承、多态进行面向对象的编程；
4、可以担负起以模版为特征的泛型化编程。

