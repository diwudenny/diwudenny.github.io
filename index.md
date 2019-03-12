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

import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class ShowTimesServlet extends HttpServlet {
	private static final long serialVersionUID = 1L;
	protected void doGet(HttpServletRequest request,
       HttpServletResponse response) throws ServletException, IOException {
		ServletContext context = getServletContext();
		Integer times = (Integer) context.getAttribute("times");
		if (times == null) {
			times = new Integer(1);
		} else {
			times = new Integer(times.intValue() + 1);
		}
		response.setContentType("text/html;charset=utf-8");
     PrintWriter out= response.getWriter();
     out.println("<html><head><title>");
     out.println("页面访问统计");
        out.println("</title></head><body>");
        out.println("当前页面被访问了");
        out.println("<font color=red size=20>"+times+"</font>次");
        context.setAttribute("times",times);
	}
	protected void doPost(HttpServletRequest request,
       HttpServletResponse response) throws ServletException, IOException {
		this.doGet(request, response);
	}
}
 
