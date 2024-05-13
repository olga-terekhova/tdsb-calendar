# tdsb-calendar
Utilities to manage calendars and schedules for TDSB (Toronto District School Board) students.

## TDSB_Calendar_Elementary.ipynb
An utility that marks up a list of dates in a school year with labels "Day 1", "Day 2", "Day 3", "Day 4", "Day 5" and shares it as iCalendar files.  

This labeling is a consecutive day numbering system employed by TDSB which cannot be derived directly from dates or days of week.  
The TDSB day numbers start with "Day 1" on the 1st day of school and cycle through 1-5 until the end of a school year.  
The numbers shift each time there is a holiday, a school break, or a PA day, so there's never a gap in the consecutive pattern.  
The numbers might also shift due to some force majeure days, like snow days. We've had none so far in 2024, so I'm not sure how they're handled.   

TDSB does not publish this numbering cycle for wide access and does not provide the way to easily and quickly look up the day number.  
Individual schools or teachers can send out this info in a form of a locally prepared PDF with a calendar view of a year or an upcoming month.   
However, TDSB provides all input data on the calendar page at https://www.tdsb.on.ca/About-Us/School-Year-Calendar.   

This utility uses the TDSB data as a source, generates the list of labeled dates and exports it.  
When there's a daily schedule associated with each of the five days, the utility can propagate it to all days in a selected timeframe.    

The script generates .ics files which can be uploaded into calendars that support iCalendar.  
I recommend creating a separate calendar for each file:  
- it's easier to toggle off a calendar from view so that the main calendar view doesn't become cluttered
- it's easier to update the calendars, just delete a calendar, create a new one with the same name and re-import the .ics file

The result in Google Calendar:  
<img src="pics/tdsb-schedule-example.png" width="252">


