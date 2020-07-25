# task_tathastu
import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

class MyCalFrame extends JFrame implements ActionListener
{
	JButton b1,b2,b3,b4,b5;
	JLabel l1,l2,l3,l4;
	JTextField t1,t2,t3;
	JPanel p1,p2,p3;
	MyCalFrame()
	{


Font ft = new Font("Courier New",Font.BOLD,20);

		setTitle("My First Frame");

		b1 = new JButton("+");b1.setFont(ft);
		b2 = new JButton("-");b2.setFont(ft);
       b3 = new JButton("*");b3.setFont(ft);
       b4 = new JButton("/");b4.setFont(ft);
       b5 = new JButton("Reset");b5.setFont(ft);

       l1 = new JLabel("Basic Calculator");l1.setFont(new Font("Courier New",Font.BOLD,30));
       l2 = new JLabel("Enter First Number");l2.setFont(ft);
       l3 = new JLabel("Enter Second Number");l3.setFont(ft);
       l4 = new JLabel("Result");l4.setFont(ft);


       t1 = new JTextField();t1.setFont(ft);
       t2 = new JTextField();t2.setFont(ft);
       t3= new JTextField();t3.setFont(ft);
       p1 = new JPanel();
       p2 = new JPanel();p2.setLayout(new GridLayout(3,2,10,10));
       p3 = new JPanel();
       p1.add(l1);
       p2.add(l2);p2.add(t1);
       p2.add(l3);p2.add(t2);
       p2.add(l4);p2.add(t3);

       p3.add(b1);p3.add(b2);p3.add(b3);p3.add(b4);p3.add(b5);

       add(p1,"North");
       add(p2);
       add(p3,"South");

       pack();
//setSize(300,300);
 b1.addActionListener(this);
 b2.addActionListener(this);
 b3.addActionListener(this);
 b4.addActionListener(this);
 b5.addActionListener(this);





		}
		public void actionPerformed(ActionEvent ev)
		 {
			 double x = Double.parseDouble(t1.getText());
			 double y = Double.parseDouble(t2.getText());
			 double z;
			 if(ev.getSource()==b1)
			 {
				 z = x+y;
				t3.setText(""+z);

				 }
				 if(ev.getSource()==b2)
				 			 {
					z = x-y;
				t3.setText(""+z);


				 }if(ev.getSource()==b3)
			 {
				 z = x*y;
				 t3.setText(""+z);


				 }if(ev.getSource()==b4)
			 {
				 z = x/y;
				t3.setText(""+z);


				 }if(ev.getSource()==b5)
			 {
				 t1.setText("");
				 t2.setText("");
				 t3.setText("");


				 }
	     }


	}
class SwingTest1
{
public static void main(String args[])
{

MyCalFrame f = new MyCalFrame();
f.setVisible(true);


	}

}
