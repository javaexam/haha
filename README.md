import java.applet.*;
import java.awt.*;
import java.awt.event.*;
import java.text.SimpleDateFormat;
import java.util.*;
import javax.swing.*;
import java.applet.*;

public class Buttonset extends JApplet implements Runnable {
	 private JPanel[] jp = new JPanel[3]; 
	private JLabel  []lb=new JLabel[3];
	public void init(){
		for(int i=0;i<3;i++){
			jp[i]=new JPanel();
		}
		lb[0]=new JLabel("1");
		lb[1]=new JLabel("2");
		lb[2]=new JLabel("3");
		setLayout(new GridLayout(3,1));
		jp[0].setLayout(new GridLayout(1,1));
		jp[1].setLayout(new GridLayout(1,1));
		jp[2].setLayout(new GridLayout(1,1));
		jp[0].setBackground(Color.BLUE);
		jp[1].setBackground(Color.WHITE);
		jp[2].setBackground(Color.BLACK);
		jp[0].add(lb[0]);
		jp[1].add(lb[1])
		;jp[2].add(lb[2]);
		add(jp[0]);
		add(jp[1]);
		add(jp[2]);
	}
	
	public void run() {
		
		
	}
}
//這是JPanel 排版的  可以參考
