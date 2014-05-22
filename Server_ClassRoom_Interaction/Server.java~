import javax.swing.*;
import java.awt.*;
import java.awt.image.BufferedImage;

class ServerFrame extends JFrame
{
	JPanel audioPanel,textPanel;
	String ipAddress="127.0.0.1";
	String sessionId="1234";
	JButton addButton,deleteButton;
	ServerFrame()
	{
		addButton=new JButton("\u2714");
		deleteButton=new JButton("X");
		
		JLabel ipLabel=new JLabel("IP Address : ");
		JLabel sessionIdLabel=new JLabel("Session ID : ");
		
		
		JLabel ipValueLabel=new JLabel(ipAddress);
		JLabel sessionIdValueLabel=new JLabel(sessionId);
		
		JComboBox studentNumberComboBox=new JComboBox();
		studentNumberComboBox.addItem("1");
		studentNumberComboBox.addItem("2");
		studentNumberComboBox.addItem("3");
		studentNumberComboBox.addItem("4");
		studentNumberComboBox.addItem("5");
		studentNumberComboBox.addItem("6");
		studentNumberComboBox.addItem("7");
		studentNumberComboBox.addItem("8");
		studentNumberComboBox.addItem("9");
		studentNumberComboBox.addItem("10");
		studentNumberComboBox.addItem("11");
		studentNumberComboBox.addItem("12");
		studentNumberComboBox.addItem("13");
		studentNumberComboBox.addItem("14");
		studentNumberComboBox.addItem("15");
		
		
		setSize(500,500);
		setLocation(100,100);
		
		this.setLayout(new BorderLayout(10,10));
		
		JPanel ipPanel=new JPanel();
		ipPanel.setLayout(new GridLayout(2,2,10,10));
		ipPanel.setBorder(BorderFactory.createTitledBorder(""));
		
		ipPanel.add(ipLabel);
		ipPanel.add(ipValueLabel);
		ipPanel.add(sessionIdLabel);
		ipPanel.add(sessionIdValueLabel);
		
		audioPanel=new JPanel();
		audioPanel.setLayout(new BorderLayout(10,10));
		JPanel listPanel=new JPanel();
		listPanel.setLayout(new GridLayout(1,2,10,10));
	
		listPanel.add(new JLabel("Number of Visible Students"));
		listPanel.add(studentNumberComboBox);
		
		audioPanel.add(listPanel,BorderLayout.NORTH);
		textPanel=new JPanel();
		
		JTabbedPane tabbedPane=new JTabbedPane();
		tabbedPane.addTab("Audio",audioPanel);
		tabbedPane.addTab("Text",textPanel);
		
		JPanel studentPanel=new JPanel();
		for(int i=0;i<Integer.parseInt(studentNumberComboBox.getSelectedItem().toString());i++)
			studentPanel.add(createStudentPanel(new Student("Lavish","123.123.123","/home/lavish/Desktop/a.jpg")));
			
		audioPanel.add(studentPanel,BorderLayout.CENTER);
		
		add(ipPanel,BorderLayout.NORTH);
		add(tabbedPane,BorderLayout.CENTER);
	}
	
	private JPanel createStudentPanel(Student student)
	{
		JPanel studentPanel=new JPanel();
		studentPanel.setLayout(new GridLayout(1,5,10,10));
		
		JPanel studentPicPanel=new StudentPicPanel().getStudentPicPanel(student.studentImage);
		studentPanel.add(studentPicPanel);
		studentPanel.add(new JLabel(student.studentName));
		studentPanel.add(new JLabel(student.doubtSubject));
		studentPanel.add(addButton);
		studentPanel.add(deleteButton);
		return studentPanel;
	}
	public Insets getInsets()
	{
		return new Insets(20,20,20,20);
	}
	
}

class StudentPicPanel extends JPanel
{
	JPanel studentPicPanel;
	BufferedImage studentImage;
	@Override
	public void paintComponent(Graphics g)
	{
		super.paintComponent(g);
		g.drawImage(studentImage,0,0,null);
	} 

	public JPanel getStudentPicPanel(BufferedImage studentImage)
	{
		return this;
	}
	
}

class Main
{
	public static void main(String []args)
	{
		ServerFrame sf=new ServerFrame();
		sf.setVisible(true);
		sf.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	}
}
