Jeff-s-code-examples-Java
=========================

Examples of code that I have implemented in Java
/* MY GUI.JAVA LAB #2
by JEFF  MARTINEZ
CIST 2372  JAVA 2 */
import javax.swing.JLabel;
import javax.swing.JTextField;
import javax.swing.JFrame;
import java.awt.FlowLayout;
import java.awt.BorderLayout;
import java.awt.*;
import javax.swing.*;
import java.awt.GridLayout;
import javax.swing.border.*;

public class MyGUI extends JFrame {

public MyGUI () {
   
this.setLayout(new BorderLayout());            
     TopPanel tp1 = new TopPanel();  
     tp1.setBackground(Color.YELLOW);         
     MiddlePanel mp1 = new MiddlePanel();           
     BottomPanel bp1 = new BottomPanel();     

this.setLayout(new BorderLayout()); 
     cTopPanel tp2 = new cTopPanel();
     cMiddlePanel mp2 = new cMiddlePanel();
     cBottomPanel bp2 = new cBottomPanel(); 
 
//tpan1     
JTabbedPane tpan = new JTabbedPane ();
     
JPanel p1 = new JPanel();
p1.setLayout(new BorderLayout());
p1.add(tp1,BorderLayout.NORTH);
p1.add(mp1,BorderLayout.CENTER);
p1.add(bp1,BorderLayout.SOUTH);
tpan.addTab("Student",p1);

this.add(tpan);

//tpan2         
JTabbedPane tpan2 = new JTabbedPane (); 
 
JPanel p2 = new JPanel();
p2.setLayout(new BorderLayout());
p2.add(tp2,BorderLayout.NORTH);
p2.add(mp2,BorderLayout.CENTER);
p2.add(bp2,BorderLayout.SOUTH);
tpan.addTab("Course Data",p2);

this.add(tpan);
                      
this.setTitle("MyGUI"); // Title in the frame
this.setSize(600, 500); // Set the frame size
this.setLocationRelativeTo(null); // center a frame
this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
this.setVisible(true); // Display the frame      
} 
public static void  main(String[] args) {
MyGUI mg = new MyGUI(); // Create a frame

}//End main  
}//End class



