import javax.imageio.*;
import java.util.*;
import java.io.*;
import java.awt.image.BufferedImage;
class Student
{
	// this class stores the student information
	BufferedImage studentImage;
	String studentName,macAddress,pic,doubtSubject;
	
	static LinkedList<Student> studentList=new LinkedList<Student>();
	
	Student(String studentName,String macAddress,String pic)
	{
		this.doubtSubject=doubtSubject;
		this.studentName=studentName;
		this.macAddress=macAddress;
		this.pic=pic;
		studentList.add(this);
		try 
		{                
          	studentImage = ImageIO.read(new File(pic));
       	} 
       	catch (IOException ex) {
            // handle exception...
       }
	}
	
	public static LinkedList getStudentList()
	{
		return studentList;
	}
}

