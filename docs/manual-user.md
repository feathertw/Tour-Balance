# Tour-Balance for Traveling with Friends
**Tour-Balance** is a tool for traveling with friends. Most of traveling cases, when you guys need to pay something together(such as hostel fee, lunch...), it's very annoying to share money everytime. Even nowadays we have many electronic payment, it still exhausts people. **Tour-Balance** is based on Google service. Everyone keys in the items on website-browser and views the final result on Google-Sheet. It's easy for all. (If using a mobile app, it needs people to install the app. It's also tiring.)

## Build a Tour-Balance

### Step1: Copy a Google-Sheet
1. Log in Google account
2. Open https://tinyurl.com/tour-balance-user
3. Press "File" -> "Make a copy"

### Step2: Build a Google-Form
1. Create a new Google-Form.
2. Set the 1st question "`Who Paid`" with "Dropdown" type. Put your friends' names into the list
3. Set the 2nd question "`Amount`" with "Short answer" type
4. Set the 3rd question "`Item`" with "Short answer" type
5. Set the 4th question "`Who needs to share`" with "Checkboxs" type. Put your friends' names into the list
6. Set the 5th qeustion "`Comment`" with "Paragraph" type
7. Click "Responses" -> Icon "Create Spreadsheet" -> "Select existing spreadsheet", then select the Google-Sheet you copied at Step1

### Step3: Configure the Google-Sheet
1. Open the Google-Sheet you copied at Step1
2. Rename the linked-form sheet-page to "`xList`"
3. Choose "Person" sheet-page and edit your friends' names
4. Choose "Final" sheet-page and delete the null columns
5. Click "Edit" -> "Find and replace"
    * Find: `List!`
    * Replace with: `xList!`
    * Select "All sheets"
    * Check "Match case"
    * Check "Search using regular expressions"
    * Check "Also search within formulas"
    * Finally, click "Replace all"
    > Note: This step should be operated on the web-browser verison of Google-Sheet
6. Delete original "List" sheet-page

## Run Tour-Balance
* Share the form link with others, so eveyone can fill in on mobile or laptop browser
* In "Final" sheet-page, you will know how to balance the money
