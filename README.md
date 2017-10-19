# mathmodel
A course in TJU Grade 2 
## team member:ZMY,YFQ,LRS.
## First task
A  检索系统  http://math.tongji.edu.cn/model/misc20.html
Deadline:201701023
Discussion: 20171018 17:50 Library Floor 1.
### idea 1
这个检索系统分为两步，第一步，分类。第二步，给出一组词，直接搜出相关文章。
我通过查阅有关北京大学2001数学建模比赛的文章，
https://wenku.baidu.com/view/5057af96dd88d0d233d46aba.html

有一篇文章说用三种方法：
第一种是AI自动根据文本进行分类
第二种是首字母分类，然后构造一个树状的模型
第三种是按照关键词长度分类

我觉得按照首字母分类是比较合理的

过程：
1.把文本导入excel，或者进一步导入mysql
2.导入后按首字母排序，然后用 group by进行分组，可以分成26组。
3.进行匹配

sql中分组的方法
http://www.studyofnet.com/news/247.html
python正则
https://docs.python.org/2.7/library/re.html
sql中构建树状结构的方法
http://www.cnblogs.com/zplutor/archive/2009/07/31/1536146.html
按首字母分组的语句
select count(*),left(a, 1) from table group by left(a, 1)
SQL语句与正则表达式
http://www.cnblogs.com/renzaijianghu/p/5666750.html

书本标题聚类分析的一个教程 
https://ad1m.github.io/Book_Title_Clustering/
