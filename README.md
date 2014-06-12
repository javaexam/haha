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


6/12 google 環境
=========================================================================================

/* INSTRUCTION: This is a command line application. So please execute this template with the following arguments:

		arg	0 = username
		arg	1 = password
*/

/**
 * @author (Your Name Here)
 *
 */
 
import com.google.gdata.client.calendar.CalendarService;
import com.google.gdata.data.calendar.CalendarEntry;
import com.google.gdata.data.calendar.CalendarFeed;
import com.google.gdata.util.AuthenticationException;
import com.google.gdata.util.ServiceException;

import java.io.IOException;
import java.net.MalformedURLException;
import java.net.URL;
import java.util.List;

/**
 * This is a test template
 */

  public class Calendar {
    
    public static void main(String[] args) {
      
      try {
        
        // Create a new Calendar service
        CalendarService myService = new CalendarService("My Application");
        myService.setUserCredentials("bboy_wei@ymail.com","128401864");
        
        
        // Get a list of all entries
        URL metafeedUrl = new URL("http://www.google.com/calendar/feeds/default/allcalendars/full");
        System.out.println("Getting Calendar entries...\n");
        CalendarFeed resultFeed = myService.getFeed(metafeedUrl, CalendarFeed.class);
        List<CalendarEntry> entries = resultFeed.getEntries();
        for(int i=0; i<entries.size(); i++) {
          CalendarEntry entry = entries.get(i);
          System.out.println("\t" + entry.getTitle().getPlainText());
        }
        System.out.println("\nTotal Entries: "+entries.size());
      }
      catch(AuthenticationException e) {
        e.printStackTrace();
      }
      catch(MalformedURLException e) {
        e.printStackTrace();
      }
      catch(ServiceException e) {
        e.printStackTrace();
      }
      catch(IOException e) {
        e.printStackTrace();
      }
    }
  }
 =====================================================================================================================
