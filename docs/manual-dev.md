# Tour-Balance-Dev

## Build a Tour-Balance

### Step1: Copy a Google-Sheet
1. Log in Google account
2. Open https://tinyurl.com/balance-template
3. Press "File" -> "Make a copy"

### Step2: Build a Google-Form
1. Create a new Google-Form.
2. Set the 1st question "`Who Paid`" with "Dropdown" type. Put your friends' names into the list
3. Set the 2nd question "`Amount`" with "Short answer" type
4. Set the 3rd question "`Item`" with "Short answer" type
5. Set the 4th question "`Who needs to share`" with "Checkboxs" type. Put your friends' names into the list
6. Set the 5th qeustion "`Comment`" with "Paragraph" type
7. Click "Responses" -> Icon "Create Spreadsheet" -> "Select existing spreadsheet", then select the Google-Sheet you copied at Step1
8. Back to the form and click "Preview", key in a demo set, then send it
    * Who Paid: Amy
    * Amount: 200
    * Item: Lunch
    * Who needs to share: Amy, Claire
    * Comment: At a steak restaurant
```
* Please make sure the members' names are definitely correct and not the same with any others.
```

### Step3: Set the Google-Sheet
1. Rename the linked-form sheet-page to "`List`"
2. Choose "List" sheet-page and add "`Invalid`" at G1 cell
3. For all sheet-page except "List"
    1. Change or extend the names and columns
    2. Except "Final" sheet-page, add a number for more rows at bottom(the number is for form content)
4. Choose "Pre" sheet-page
    1. @A2 enter and type `=List!$D2&""`
    2. @B2 enter and type `=ISBLANK(List!$G2)*1`
    3. @C2 enter and type `=List!$B2&""`
    4. @D2 enter and type `=($B2)*List!$C2*1`
    5. @E2 enter and type `=List!$E2&""`
    6. @F2 enter and type `=SUM(H2:2)`
    7. @G2 enter and type `=IF(F2, D2/F2, 0)`
    8. @H2 enter and type `=($B2)*IF(REGEXMATCH($E2&",", H$1&","), 1, 0)` and extend it to other names
    9. Extend Row-2 to all row bellow
5. Choose "Paid" sheet-page
    3. @B2 enter and type `=(Pre!$B2)*(Pre!$D2)*IF(REGEXMATCH(Pre!$C2&",", B$1&","), 1, 0)` and extend it to other names
    4. Extend Row-2 to all row bellow
6. Choose "Share" sheet-page
    3. @B2 enter and type `=(Pre!$B2)*(Pre!H2)*(Pre!$G2)` and extend it to other names
    4. Extend Row-2 to all row bellow
7. Choose "Final" sheet-page, extend column content to other names
8. Execute replace coding, Click "Edit" -> "Find and replace"
    * Find: `(.+)(List!\$[B-G][0-9]*)(.+)`
    * Replace with: `$1INDIRECT("$2")$3`
    * Select "All sheets"
    * Check "Match case", "Search using regular expressions", "Also search within formulas"
    * Finally, click "Replace all" and wait for a long time if you add many rows

## Run Tour-Balance
* Share the form link with others, so eveyone can fill in
* In "Final" sheet-page, you will know how to share the money
* If you want to cancel the specific item, type "`v`" into the cell below "Invalid" column in "List" sheet-page

---

```
* Technical Note
    * Only one grep-key can be in a cell
    * There are something word before and after the grep-key
```
