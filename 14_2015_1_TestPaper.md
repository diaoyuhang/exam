### 一、单选题（共 10 小题，每题 0.5 分，共 5 分）

1. 我国自行研制的 “曙光 4000A” 计算机是（）

   A. 微型计算机   B. 小型计算机   C. 大型计算机   D. 巨型计算机
2. 下列 PC 机 I/O 接口能同时适用于链接鼠标、键盘、数码相机的是（）

   A. IEEE-1394

   B. IDE

   C. RS-232

   D. USB

3. 为解决内存和 CPU 之间不匹配问题，可采用以下哪种存储器（）

   A. 虚拟存储器

   B. 移动硬盘

   C. 高速缓冲存储器

   D. 优盘

   

4. 最早应用计算机的领域是（）

   A. 科学计算

   B. 实时控制

   C. 信息处理

   D. 辅助设计

   

5. 有线电视接入用户使用的电缆类型是（）

   A. 双绞线

   B. 光缆

   C. 同轴电缆

   D. 微波

   

6. 即时通讯是因特网的一种允许的实时快速地交换信息的通讯服务，下列哪种软件提供该服务（）

   A. Access

   B. Photoshop

   C. QQ

   D. Word

   

7. CD 唱片上记录的高保真全频带立体声数字声音的主要参数有取样频率（44.1kHz）、量化位数（16 位）和声道数（2 声道）等，那么该 CD 唱片上记录的数字声音未压缩前的码率是（）

   A. 705.6kb/s

   B. 141kb/s

   C. 202.14kb/s

   D. 176.4kb/s

   

------

### 二、多项选择题（共 5 小题，每题 1 分，共 5 分）

1. 下列对二进制数不能进行基本逻辑运算和逻辑判断的的有（）

   A. 运算器

   B. 控制器

   C. 存储器

   D. 寄存器

   

2. 使用口令（密码）是目前最简单也是最普遍的身份鉴别方法，但安全性不高，因此用口令作为身份证鉴别时，应采取的防范措施有（）

   A. 定期改变口令

   B. 口令长度要求 6 位及其以上

   C. 严格限制非法登陆次数

   D. 避免使用与用户特征相关的口令（如生日、电话号码）

------

### 三、简答题（两小题，共 20 分）

1. 如果自己动手组装一台家用微型电脑，购买零部件时应考虑哪些因素？
2. 为确保计算机不被计算机病毒侵害，应采取哪些预防措施？

------

### 四、实务题（三小题，共 60 分）

1. email 是 Internet 使用最频繁的应用，采用客户 / 服务器结构，现有邮箱名 nihao，域名[126.com](https://126.com)（20 分）

   (1) 电子邮箱工作原理示意图或步骤

   (2) 请给出上述用户 E-mail 地址

   (3) 给出一封电子邮件的一般组成

   

2. 某公司开发一个通讯录管理程序，包括姓名、电话、家庭住址，姓名（name）定义长度为 20 的字符数组，号码（phone）为 15 的字符数组，家庭（home）为 40 的数组，C 语言编码如下：（20 分）

   

```
#include<stdio.h>
#include<string.h>

typedef struct phone {
    char name[20];
    // ①
    // ②
} phoneInfo;

int search(phoneInfo ph[], char name[], int n) {
    int i=0;
    for (i=0;i<n;i++) {
        if(strcmp(ph[i].name, name)==0)
            return i;
    }
    return -1;
}

void main() {
    int k,n;
    char name[20];
    phoneInfo ph[]= {{"liming"}, "13278967654", "35zhongshanroad",
                    {"fanghai"}, "15687906543", "1yunnan road",
                    {"lifang"}, "13456789876", "5ciafei road",
                    {"wangqiang"}, "17165433456", "10guangzhouroad"};
    n=sizeof(ph)/size of(phoneInfo);
    printf("please input name:\n");
    gets(name);
    k=search(ph, name, n);
    if(k==-1)
        printf("Not Found!\n");
    else {
        printf("searched result:\n");
        printf("%15s%40s\n", ph[k].name, ph[k].phonenum, ph[k].adress);
    }
}
```

要求：

1. 完善 5、6 行
2. 给出 search 函数处理流程
3. 给出 28-34 语句功能
