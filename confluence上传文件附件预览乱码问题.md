# confluence
confluence安装文档

1) 先安装想要的字体, 如微软雅黑, 宋体等, 从windows/font下拷到linux的/usr/share/fonts下,
新建个目录比如windowsfonts放进去, 请自行搜索linux下新字体的安装方法（附上一个别人的链接http://www.linuxidc.com/Linux/2016-09/135548.html


2) 在confluence的安装目录, 如/opt/atlassian/confluence/bin下找到setenv.sh, 找到CATALINA_OPTS, 加入一行

CATALINA_OPTS=”-Dconfluence.document.conversion.fontpath=/usr/share/fonts/windowsfonts/ ${CATALINA_OPTS}”


3) 清空confluence的home下viewfile目录和shared-home/dcl-document目录里的所有缓存文档文件,

   不清空的话, confluence预览旧文件时还是会显示方框,只有新文件才会正常.
   
   
 4)重启confluence就OK了
 
 
 
 通过以上几部就可以解决中文文档乱码问题，顺便说一句，confluence对数据库的编码格式要求是utf-8，所以请把数据库编码格式设置正确，以免其他地方出现乱码。
 
 
 
 一般上传的中文字符  msyhbd.ttc  msyhl.ttc  msyh.ttc

