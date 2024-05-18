# mutual_subscription_mgmt
A spreadsheet, form, and script that enables cost distribution and bill tracking. It makes keeping track of who owes whom and for what a lot easier.


# Setting up App Scripts
For initial setup you will need to enable Apps Scripts and set up three triggers.
1. Go to the google form, select the settings button, and then Script editor.
2. Select Triggers from the left hand menu, and then Add Trigger.
3. You will be prompted to allow App Script access to your account. You will need to allow this.
4. Create three triggers:
   Trigger One:
     Function to run: update_srv_usr_data
     Which runs at deployment: Head
     Select event source: Time-driven
     Select type of time based trigger: Minutes timer
     Select minute interval: Every minute
   Trigger Two:
     Function to run: srv_metadata
     Which runs at deployment: Head
     Select event source: Time-driven
     Select type of time based trigger: Month timer
     Select day of month: 5th
     Select time of day: Midnight to 1am
   Trigger Three:
     Function to run: populateQuestions
     Which runs at deployment: Head
     Select event source: Time-driven
     Select type of time based trigger: Minutes timer
     Select minute interval: Every minute

# Setting up Members
Add names to column A in the tab named SERVICE_MGMT.

# Setting up Services
Go to the tab named USER_SERVICE_MGMT and edit columns A through H. It is important that each cell have a value excluding B and C (one or both can be filled) and F, G, and H (only one should be marked).

# FAQs
Why don’t I see an entry for the form I just submitted? 
Ensure that on the SERVICE_MGMT tab you have the “Toggle Active / Pending” selected.
Wait at least one minute after your form submission to allow time for the system to update its tables.



