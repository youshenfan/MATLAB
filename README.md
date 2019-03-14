# MATLAB Notes by WENQI
该笔记记录本人在科研过程中所学到的MATLAB实用操作，为方便查阅总结如下，代码都经过本人验证实用，由于来源广泛，未能列全参考文献。


## 与系统交互
### 直接使用bat命令
> system()

例如，调用LS-DYNA软件对trugrdo.k文件进行求解：
> system('"D:\Program Files\ANSYS Inc\v172\ansys\bin\winx64\LSDYNA.exe" I=trugrdo.k MEMORY=200000000')




## 实用快捷键
1. CTRL+I：自动对齐代码

## 文件读取与图像保存

### 导出高清晰图片：
http://blog.sina.com.cn/s/blog_56d5b3b00102w4x4.html

### 读取记事本中的数据
1. load：当记事本中记录的全部是数据时，运行此函数后就会将记事本中的数据按矩阵形式放入名为filename的变量中。
2. textread：当记事本中的数据结构复杂时使用。其中，A,B,C..为每一列数据将要保存的变量名；format为读取格式；N为读取次数
3. fscanf：功能更强大。
> load('filename.***')

> [A,B,C,...]=textread('filename','format',N)

### 将数据写入记事本中
1. save：保存为.mat文件
2. fprintf：保存为txt文件
> save file obj1 obj2 ...

### 传递数据常用命令
1. fopen
2. fprintf
4. load
5. fscanf
4. textread


### 绘制函数图形
> fplot(@(x)x+10.*sin(5.*x)+7.*cos(4.*x))

或
> fplot('x + 10*sin(5*x)+7*cos(4*x)',[0 9])


### **数据拟合**
#### 多项式拟合
1. polyfit(X,Y,N):多项式拟合，返回降幂排列的多项式系数
2. polyval(P,xi)：计算多项式的值。

x = 1:10;
y = [9 7 6 3 -1 2 5 7 20 25];
P = polyfit(x,y,3);
xi= 0:.2:10;
yi=polyval(P,xi);
plot(xi,yi,x,y,'r*');

#### 指定函数拟合
1. fittype
2. fit

#### 可以用曲线拟合工具箱进行曲线拟合 


