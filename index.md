---
layout: page
title: Di Wu, Denny (吴迪)<br />
permalink: /
---
*Ph.D. HKU, M.S. CityU(HK), B.Eng. UESTC*<br />
{% include image.html url="images/photo.jpg" caption="" max_width="300px" align="left" %}

**Assistant Professor**<br />   
**Shenzhen University**<br />  

**Tel**: +86-755-12345678<br />  
**Email**: diwu@szu.edu.cn, diwu@eee.hku.hk<br />    
**Office**: Room 999, College of Electronic Science and Technology, Southern Campus, Shenzhen University, Shenzhen,518060,China    

**Biography:**
Dr. Di Wu received the B.Eng. degree in electromagnetic field and microwave technology from the University of Electronic Science and Technology of China (UESTC), Chengdu, China, in 2009, the M.S. degree from the City University of Hong Kong, Hong Kong, in 2013 and the Ph.D. degree from The University of Hong Kong, Hong Kong, in 2018. In 2017, he was supported by the Pilot Scheme of HKU to work as an Honorary Research Associate (Visiting Ph.D.) in the University of Wisconsin-Madison, Madison, WI, USA. 

From 2010 to 2012, he was with MediaTek.Inc (MTK) as a Senior RF Engineer. From  2018 to 2019, he was with the Hong Kong Applied Science and Technology Research Institute (ASTRI), Hong Kong, as a Senior System RF Engineer,  focusing on the R&D of the 5G low cost phased array system for base station application. Since Jan. 2019, he has been with the College of Electronic Science and Technology, Shenzhen University, Shenzhen, China, as an assistant professor. His current research interests include phased array system, phase shifter design, in-band full duplex antenna system, mobile antennas, MIMO antennas, and wearable antennas.

ServletContextappliaton = this.getServletContext();

     //获取当前web应用项目的context对象

     Integer count = (Integer) appliaton.getAttribute("count");

     //获取Context对象的count属性

    

     /*

      *对count属性值进行判断，如果为空值，说明该网站是第一次被访问，count赋值为1

      * 如果不为空值，则进行累加操作

      *

      * */if(count == null) {

       count = 1;

    }else {

       count++;

     }

      //设置编码格式为utf-8

     response.setContentType("text/html;charset=utf-8");

     //创建一个响应流

     PrintWriter out = response.getWriter();

     //输出访问次数

     out.print("该网站共被访问了"+count+"次");

     //保存访问次数

     appliaton.setAttribute("count", count) 
--------------------- 
作者：大尾巴战狼 
来源：CSDN 
原文：https://blog.csdn.net/dawiebazhanlang/article/details/79669481 
版权声明：本文为博主原创文章，转载请附上博文链接！

