package webserver;
import java.io.BufferedReader;
import java.io.File;
import java.io.FileFilter;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.PrintStream;
import java.lang.reflect.Field;
import java.net.Socket;

public class Processor extends Thread {//添加框架代码
	private Socket socket;
	public InputStream in;
	public PrintStream out;
	public final static String WEB_ROOT="c:\\eclipse\\workspace\\webserver\\htdocs";//不可能让用户访问所有目录 所以这里定义一个常量 限定只能访问这个目录之下的资源
	public Processor(Socket socket) {
		this.socket=socket;
		try {
			in=socket.getInputStream();//获得一个输入流
		    out=new PrintStream(socket.getOutputStream());//获得输出流
		}catch (Exception e) {
			e.printStackTrace();
			// TODO: handle exception
		}
	};
	public void run() { 
		String filename=parse(in);
		sendFile(filename);
	}
	public String parse(InputStream in) {
		BufferedReader br = new BufferedReader(new InputStreamReader(in));//将in这种字节流封装为br这种字符流
		String filename=null;//new不要丢 声明不要丢
		try {
			String httpMessage=br.readLine();
			String[] content=httpMessage.split(" ");
			if(content.length!=3) {//发过来的应该是三部分
				SendErrorMessage(400, "Client query error");//这就是那个状态码啊
				return filename;
			}
			System.out.println("code:"+content[0]+",filename"+content[1]+"http version:"+content[2]);
		}catch (Exception e) {
			e.printStackTrace();
			// TODO: handle exception
		}
		return filename;
	}
	public void SendErrorMessage(int errorcode,String errorMessage) {
		out.println("HTTP/1.0"+errorcode+" "+errorMessage);
		out.println();
		out.println("<html>");
		out.println("<title>Error Message");
		out.println("</title>");
		out.println("<body>");
		out.println("<h1>ErrorCode:"+errorcode+",Message:"+errorMessage+"</h1>");
		out.println("</body>");
		out.println("</html>");
		}
	
	public void sendFile(String filename) {//先根据文件名找到硬盘上的资源位置 然后返回给用户
		File file = new File(Processor.WEB_ROOT+filename);
		if(file.exists()) {
			SendErrorMessage(404, "File Not Found");
			return;
		}
		try {
			InputStream in = new FileInputStream(file);
			byte content[]=new byte[(int)file.length()];
			in.read(content);
			out.println("HTTP/1.0 200 ");
			out.println("content-length:"+content.length);
			out.println();
			out.write(content);
			out.flush();
			out.close();
			in.close();
		}catch(FileNotFoundException e) {
			e.printStackTrace();//有文件就要写文件异常
		}catch(IOException e) {
			e.printStackTrace();//有输入流就要写输入流异常
		}
	}
}
