# MATLAB Notes by WENQI
## Collected tricks

MATLAB导出高清晰图片：http://blog.sina.com.cn/s/blog_56d5b3b00102w4x4.html

### MATLAB 读取记事本中的数据
1. load：当记事本中记录的全部是数据时，运行此函数后就会将记事本中的数据按矩阵形式放入名为filename的变量中。
2. textread：当记事本中的数据结构复杂时使用。其中，A,B,C..为每一列数据将要保存的变量名；format为读取格式；N为读取次数
3. fscanf：功能更强大。
> load('filename.***')
