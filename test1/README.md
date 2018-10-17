实验一  
实验日期 ：2018/10/17  
实验内容：对Oracle12c中的HR人力资源管理系统中的表进行查询与分析  
学生姓名：刘成  
学号 ：201610414311  
对 两个查询示例代码运行结果如下  
示例 2  
![Image text](https://github.com/201610414311/Oracle/blob/master/raw/search2.png)
   
  示例2的解释计划:   
 ![Image text](https://github.com/201610414311/Oracle/blob/master/raw/explain%20plan1.png)
  示例1  
![Image text](https://github.com/201610414311/Oracle/blob/master/raw/search1.png)  
  示例1的解释计划：  
  ![Image text](https://github.com/201610414311/Oracle/blob/master/raw/explain%20plan2.png)  
  从示例1和示例2的脚本运行时间来看，示例1比示例2的运行时间要长一点。所以，单从代码执行效率来看，示例2的代码显得更加好一些。  
  但是，当我们再看示例1和示例2各自的解释计划中的cost栏时，我们会发现，示例1的成本会比示例2的成本低一半以上。  
  综合以上因素，我觉得示例1的代码更优，理由如下：  
  一：两段示例代码在运行的时间上相差不是太多，在不是很紧急的情况下，两段代码都是很适用的。  
  二：示例2的成本要比示例1高出一倍多，查询数据较少，勉强还能使用示例2的代码，但如果查询数据量非常大，示例2的代码就有点不理性了。  
  
 示例1优化指导如下图：  
 
