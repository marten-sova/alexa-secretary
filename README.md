# alexa-secretary
A simple Alexa voice assistant. Simulates a secretary who schedules events for you.

## Intents
1. AddEventIntent. *This intent will create a new calendar event by asking the user for a date, time, and event name.*
2. DeleteEventIntent *This intent will delete a calendar event, identified by asking for an event name and date.*
## Sample Utterances

### AddEventIntent
1. Create an event
2. New event on {Date}
3. Schedule an event for {Date} at {Time}
4. Add an event
5. I want to make a new event on {Date}
6. Can you add a new event?
7. I have an {EventName} on {Date} at {Time}
8. Schedule an {EventName}
9. I want to add an event
10. I have a {EventName} at {Time}

### DeleteEventIntent
1. Cancel my {EventName} on {Date}
2. Delete my {EventName} on {Date}
3. Cancel my {EventName}
4. Delete my {EventName}
5. I want to delete an event
6. Delete an event
7. Cancel my {Time}
8. Can you delete the event called {EventName}
9. Delete the event on {Date} at {Time}
10. Cancel the event on {Date}

## Slots and Slot Types
"name": "EventName" "type": "EventName"  
"name": "Date" "type": "AMAZON.DATE"  
"name": "Time" "type": "AMAZON.TIME"  
## Logic for Each Intent
### AddEvent Algorithm
[Requires EventName, Time, and Date for successful completion]  
Get intent and detect any provided slot values  
Loop: if missing a slot's value:  
&nbsp;	Ask user for required info  
&nbsp;	If previous response was invalid:  
&nbsp;&nbsp;		Ask user for info with explicit format requirements  
Confirm event creation  
### DeleteEvent Algorithm  
[Requires EventName, Time, and Date for successful completion]  
Get intent and detect any provided slot values  
Loop: if missing a slot's value:  
&nbsp;	Ask user for required info
&nbsp;	If response was invalid:  
&nbsp;&nbsp;		Ask user for info with explicit format requirements  
Confirm event creation
### Test phrases
- Add an event
- Schedule an appointment
- Add an event at 3pm on August 1st called meeting
- I have an appointment at 5pm
- Cancel my 3 o'clock
- Delete the appointment on July 23rd
- Cancel the meeting later
- I want to delete an event
- Cancel my 11am meeting on Sunday
- Cancel my appointment