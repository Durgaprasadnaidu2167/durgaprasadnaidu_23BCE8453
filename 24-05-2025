package Connection;

import java.sql.*;
public class DBConection {
	public static void main(String [] args){
		try{
			Class.forName("com.mysql.cj.jdbc.Driver");
			Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/vit", "root", "rao@2167");
			
			Statement stmt=con.createStatement();
			
			ResultSet rs=stmt.executeQuery("select * from cont");
			
			while(rs.next())
				System.out.println(rs.getString(1)+" "+rs.getString(2)+" "+rs.getString(3)+" "+rs.getInt(4));
			con.close();
		}
		catch(Exception e){
			System.out.println("Sorry for inconvinence");

			
		}
	}


package curd_operations;

public class CURD_Operations {

	public static void main(String[] args) {
		CRUD_Operations objTest=new CRUD_Operations();
		  
		objTest.create_data("103", "manoj");
		objTest.create_data("104", "karthick");
	    
	}

	public void create_data(String sl_no,String name,int mark){
		DB_Connection obj_DB_Connection=new DB_Connection();
		Connection connection=obj_DB_Connection.get_connection();
		PreparedStatement ps=null;
		try {
			String query="insert into student values (?,?)";
			ps=connection.prepareStatement(query);
			ps.setString(1, sl_no);
			ps.setString(2, name);
			System.out.println(ps);
			ps.executeUpdate();
		} catch (Exception e) {
			System.out.println(e);
		}


	}

}


package curd_operations;

import java.sql.Connection;
import java.sql.DriverManager;

public class DB_Connection {

	public static void main(String[] args) {
		DB_Connection obj_DB_Connection=new DB_Connection();
		System.out.println(obj_DB_Connection.get_connection());
		
	}
	public Connection get_connection() {
		Connection connection=null;
	try {
		Class.forName("com.mysql.cj.jdbc.Driver");
		Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/vit", "root", "rao@2167");
		
	}
	catch(Exception e) {
		return connection;
	}
	}

}
