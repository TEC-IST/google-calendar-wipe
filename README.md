# google-calendar-wipe
Google Apps Script to delete Google Calendar events in a specified date range

To use, go to: https://script.google.com/ and create a new project, pasting in the following and filling in your calendar name and the dates (from/to in YYYY,M,D,H,M,S format)
```
function wipe(){
CalendarApp.getCalendarsByName('your_calendar_name_here')[0].getEvents(new Date(2021,1,1,0,0,0),new Date(2021,12,31,0,0,0)).forEach(x => {x.deleteEvent();Logger.log(x.getTitle());});
}
```
