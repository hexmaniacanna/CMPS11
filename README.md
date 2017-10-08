# CMPS11
* Annabel Maokhamphiou 
 * TimeConverter
 * changes standard time to military time 
 */

import java.util.*; // use Scanner class for readying input 

class TimeConverter {
	public static void main (String[] args) {	
	
		int hour;
		int minute;
		int amOrPm; 
		String hourString = ""; 
		String minuteString = "";
		
		Scanner timeReader = new Scanner(System.in); // timeReader reads user input  
		
		hour = timeReader.nextInt(); // saves first integer that the user inputs in the variable hour
		minute = timeReader.nextInt(); // saves second integer that the user inputs in the variable minute
		amOrPm = timeReader.nextInt(); // saves third integer that the user inputs in the variable amOrPm
		
		if(amOrPm == 1) { // for hours in the am 
			if(hour == 12) {
				hourString = "00"; //changes 12 am to military time
			}
			else if(hour < 10) {
				hourString = "0" + hour; // hours less than ten in the am have a 0 in front of it in military time 
			}
			else {
				hourString = "" + hour; // if hour is 10 or 11 save to hour string variable 
			}
			
		}
		else if(amOrPm == 2) {
			if (hour == 12) {
				hourString = "" + hour; //saves 12 to the hour string
			}
			else {
				hourString = "" + (hour + 12);
			}
		}
		
		if (minute < 10 ) {
			minuteString = "0" + minute;
		}
		else {
			minuteString = "" + minute; 
		}
		System.out.println(hourString + ":" + minuteString); //print hour 
		
	}
} 
