# Tour-Balance for Traveling with Friends
**Tour-Balance** is a tool for traveling with friends. Most of traveling cases, when you guys need to pay something together(such as hostel fee, lunch...), it's very annoying to share money everytime. Even nowadays we have many electronic payment, it still exhausts people. **Tour-Balance** is based on Google service. Everyone keys in the items on website-browser and views the final result on Google-Sheet. It's easy for all. (If using a mobile app, it needs people to install the app. It's also tiring.)

## Build a Tour-Balance

### Step1: Copy a Google-Sheet
1. Open https://tinyurl.com/tour-balance-user
2. Press "File/Make a copy"

### Step2: Build a Google-Form
1. Create a new Google-Form.
2. Set the 1st question "`Who Paid`" with "Dropdown" type. Put the names into the list
3. Set the 2nd question "`Amount`" with "Short answer" type
4. Set the 3rd question "`Item`" with "Short answer" type
5. Set the 4th question "`Who needs to share`" with "Checkboxs" type. Put the names into the list
6. Set the 5th qeustion "`Comment`" with "Short answer" type
7. Click "Responses/Create Spreadsheet/Select existing spreadsheet", then select the sheet we copy at Step1

```
* Please make sure the members' names are absolutely correct and not the same with any others.
```

### Step3: Set the Google-Sheet
1. Rename the linked-form sheet to "`xList`"
2. Choose "xList" sheet and add "`Invalid`" at G1 cell
3. Choose "Person" sheet and edit member name
4. Choose "Final" sheet and delete the null column
5. Click "Edit/Find and replace"
    * Find: `List!`
    * Replace with: `xList!`
    * Select "All sheets"
    * Check "Match case", "Search using regular expressions", "Also search within formulas"
    * Finally, click "Replace all", wait for a while, then click "Done"
6. Delete original "List" sheet

## Run Tour-Balance
* Share the form link with others, so eveyone can fill in
* In "Final" sheet, you will know how to share the money.
* If you want to cancel the specific item, type "`v`" into the cell below "Invalid" column in "List" sheet.

