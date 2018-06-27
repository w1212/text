package dao;
import java.sql.*;
public class DBConn {
     public static Connection getConnection(){
    	 Connection conn=null;
    	 try {
		    Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");
		    conn=DriverManager.getConnection("jdbc:sqlserver://localhost:1433;DataBaseName=tb_diancan","sa","123");
		} catch (Exception e) {
			e.printStackTrace();
		}
		 return conn;
     }
}
