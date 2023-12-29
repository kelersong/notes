# 期末考试复习

## 指针处理字符串

## 结构体+链表 链表的插入和删除
+ 一些注意事项
  - c语言中的结构体要用typedef 否则需要struct SNode 这样子
  - c语言中没有引用传参，对于链表的一些操作，需要将链表直接返回。
  - 代码部分
    ~~~~
    typedef struct Node{
        ElemType data;   //数据域
        struct Node* next; //指针域
    } Node, *p_Node;

      typedef struct Link{
      p_Node head;
      p_Node tail;
      int length;

    };
    ~~~~

  - 链表销毁，从头结点开始逐个销毁后面的结点，但是销毁前，要把next赋给head->next 因为要保存一下结点的信息。
  - 结构体指针使用之前要开辟空间，并且错误提醒
    ~~~~
    L.head = (SNode*)malloc(sizeof(SNode));
    if(L.head == NULL){
        exit(OVERFLOW);
    }
    ~~~~
  - malloc 函数需要引入头文件<stdlib.h>
## 文件加结构体

## 文件的读写
+ 文件的读写主要考察一些函数的使用
  ~~~~
  fgetc(FILE*);                 //读取一个字符
  fgets(FILE*);                 //读取一行
  fscanf(FILE*,"%d",&a);        //格式化读取
  fprintf(FILE*,"%d",a);        //格式化输出

  ~~~~
  
+ 文件的打开和关闭
  ~~~~
  FILE* fp;
  fp = fp.open("文件名","打开方式");
  if(fp == NULL){
    纠错机制
  }
  fp.close();
  ~~~~
## 二维数组存储矩阵，矩阵的一系列操作


