  * 利用java.util.Properties可以非常方便的读取ini配置文件。这里给一个简单例子。 首先，需要一个ini配置文件。myconfig.ini:
    
    	para1=anels
    	para2=ruilinliu.com\
    	path=c:/anels/test/
  
  * 然后是程序：
   
    	import java.io.FileInputStream;
    	import java.util.Properties;
    	public class IniReader {
    	public static void main(String args[]) {
    	  Properties ppt = new Properties();
    	  try {
    	    ppt.load(new FileInputStream(“myconfig.ini”));
    	  }catch (Exception e) {}
    	    //get properties
    	    String p1 = ppt.getProperty(“para1″);
    	    String p2 = ppt.getProperty(“para2″);
    	    String pa = ppt.getProperty(“path”);
    	    System.out.println(“p1: “+p1);
    	    System.out.println(“p2: “+p2);
    	    System.out.println(“pa: “+pa);
    	  }
    	}
