[TOC]

## First Part: Test Design

##### A. Application Coverage sorted by business impact: 

This section provides prioritization of areas in the application that have the biggest business impact. Each area has been classified to its sub-modules that should be tested. 

1. Tracking expenses
   1. Income
   2. Expenses
   3. Spending Chart
      1. Categories
   4. Calculator
2. Managing accounts
   1. Add account
   2. Transfer from account-account.
3. Settings
   1. Balance.
      1. Budget Mode.
      2. Carry-over.
      3. Future recurring records.
   2. General settings:
      1. First day of week .
      2. First day of month.
      3. Export to file.
      4. Language.
      5. Change Currency.
      6. About Monefy.
      7. Privacy Policy.
   3. Synchronization. 
   4. Data backup.
      1. Create data backup.
      2. Restore data.
      3. Clear data.
4. Premium Features:
   1. Multiple currencies.
   2. Pass code protection.
   3. Synchronization
      1. Dropbox.
      2. Google drive.
5. Tracking filter
6. UI Components
   1. Color
   2. Size

##### B. Test Case Design:

The test cases in the following section provide coverage for the above areas and sub-modules.

| TC Name                                                      | Description                                                  | Steps                                                        | Expected Results                                             |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| TC 1.1 - Tracking Expenses - Checking Entry of Income/Expenses | This test case is to check that process of entering income and expenses are done successfully and reflect in the spending chart. | 1. Open Monefy Application. 2. Click on the Plus icon. 3. Enter in the calculator 100. 4. Press on choose category to proceed. 5. Click on any source (e.g: savings). 6. Click on the Minus icon. 7. Enter in the calculator 50. 8. Click on choose category to proceed. 9. Choose any category available. 10. Repeat Steps 1- 9. 11. Check the spending chart. 12. Click on any category to add expense. | 1. Income should be added successfully and should update the balance and spending chart. 2. Expenses should be added successfully and should update the balance and spending chart. 3. Spending chart should indicate the expenses and their percentages. |
| TC 1.2 - Tracking Expenses - Balance record tracking Drawer  | This test case is to check that the balance record tracking drawer is updated correctly with all the transactions that occur. | 1. Execute TC 1.1. Slide up the balance drawer to check the transactions' details. | 1. Transactions should be listed based on their type whether Expense/Income, their category and the amounts. |
| TC 2.1 - Manage Accounts - Adding New Account                | This test case is to check the process of adding a new account whether cash/payment card. | 1. Open Monefy application. 2. Click on the Options button on the top right. 3. Click on Accounts. 4. Click on the Plus button to add a new account. 5. Change currency to Egyptian Pounds. 6. Give a name and select an icon. 7. In the tab of accounts, access the new account and add an income. 8. Repeat step 7 for expenses. | 1. A new account should be created under the tab of Accounts. 2. New account should now be accessible and can have expenses and income. |
| TC 2.2 - Manage Accounts - Transfer From Account To Account  | This test case is to check the process of  transferring funds from one account to another whether cash/payment card | 1. Open Monefy application. 2. Click on the right-left button in the top right corner **OR** open the options button and click on Account tab, then click on Transfer icon. 3. Choose a date for the transfer. 4. Enter an amount to be transferred from cash to card. 5. Repeat step 4 for card to cash. 6. Add payment. | 1. A message should be shown indicating the successful transfer. 2. The accounts' balance should be affected based on that transfer. |
| TC 3.1 - Settings - Balance Tab                              | This test case is to check the balance settings.             | 1. Open Monefy application. 2. Click on the Options button on the top right corner. 3. Click on Settings Tab. 4. Under Balance tab, click on Budget Mode. 5. Under Balance tab, click on Carry-over. 6. Under Balance tab, click on future-recurring records. | 1. User should be allowed to add budget to be spent for the month. Same for carry-over and future-recurring records. |
| TC 3.2 - Settings - General Settings                         | This test case is to check the general settings              | 1. Open Monefy application. 2. Click on the Options button on the top right corner. 3. Click on Settings Tab. 4. Under General Settings tab, click on First day of the week. 5. Choose a day. 6. Under General settings tab, click on First day of the month. 7. Choose a day. 8. Under General settings tab, click on About us then the privacy policy. | 1. Choices made should update the fields. 2. About us and privacy policy should open successfully. |
| TC 3.3 - Settings - Data Backup                              | This test case is to check the Data backup.                  | 1. Open Monefy application. 2. Click on the Options button on the top right corner. 3. Click on Settings Tab. 4. Under Data Backup tab, click on Create data backup. 5. Under Data backup tab, click on Restore Data. 6. Under Data backup tab, click on Clear Data. | 1. A confirmation message should be shown to create a data backup. 2. A list should appear to choose a restoration point. 3. Clearing data should clear all current information. |
| TC 4 - Records' Date Filter                                  | This test case is to check the records' date filter.         | 1. Open Monefy application. 2. Click on the Options button on the top left corner. 3. Click on the Options button on the top left corner. 3. Try each of these tabs: Day, month, week, year and all. 3. Click on Choose Date. 4. Repeat steps 2 and 3 for cash/payment card. | 1. Records should be fetched based on the filter selected.   |
| TC 5 - Premium Features                                      | This test case is to check the premium features.             | 1. Open Monefy application. 2. Check that each of the following items navigate to the premium page activity. A. Adding new categories. B. Clicking on the Currencies Tab. C. Dark theme under General Settings tab. D. Pass code protection under General Settings tab. E. Synchronization tab. | 1. These elements should navigate to the Premium features activity successfully. |

 



## Second Part: Bug Reporting

##### A. Bugs:

Severity has the following options:

	1. Critical 
 	2. Major 
 	3. Average
 	4. Minor

Priority has the following options:

1. Urgent
2. High
3. Medium 
4. Low

Impact has the following options:

	1. Functionality
 	2. User Interface
 	3. User Experience

| Title                                                        | Reproducible Steps                                           | Attachments/ Actual Result                                   | Affected Devices    | Network | Severity | Priority | Impact          |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------- | ------- | -------- | -------- | --------------- |
| Options Drawer - Back-Button-Opens-Filter-Drawer             | 1. Open Monefy application. 2. Press Options button on the top right corner. 3. Click on the back button on the top left corner. | *Could not capture transition*. The left side drawer opens while the right side drawer is still open. They overlap on each other. instead of closing the left side drawer only. | Android, HTC one M9 | WiFi    | Low      | Low      | User Experience |
| Manage Accounts - Add New Account - Currency - Changing-currency-from-New-account-Navigates -to-multiple-currencies-premium-features | 1. Open Monefy. 2. Press on the Options button on the top right corner. 3. Press on Accounts. 4. Press on the Plus button of  Add tab. 5. Press on USD from the activity of New account to change currency | *could not capture transition*. The activity navigates to premium features when it should have listed the options of the currencies, giving a confirmation message that this will change the default currency of all accounts. | Android, HTC one M9 | WiFi    | Average  | Medium   | Functionality   |
| Settings - General Settings - First Day of Week/Month - Component-accepts-text | 1. Open Monefy. 2. Press on the Options button on the top right corner. 3. Press on Settings. 4. Under General settings tab, press on First day of the Month/Week. 5. Double click on the selected option to edit. 6. Type in any number/day to auto-complete. | ![img](https://scontent-hbe1-1.xx.fbcdn.net/v/t1.15752-9/80042288_445321572800106_4381170764259262464_n.png?_nc_cat=102&_nc_ohc=bHBSzBcbPyQAQnX8M7wwrHUdIUmbCp2cEgzMsxuSoYzbUxO4Le1hFjrEw&_nc_ht=scontent-hbe1-1.xx&oh=3d293424ed2832cdb807e9a0ea12b1e1&oe=5EAEC7C9)This element should not be text-enabled. | Android, HTC one M9 | WiFi    | Average  | High     | Functionality   |
| Manage Accounts - Transfer transaction - Adding_Note_Keyboard_Overlaps_Adding_Fund_keyboard | 1. Open Monefy application. 2.  Press on the transfer button on the top right section. 3. Type any input in the add note field. 4. Press on the fund field. Repeat for tool tip of transfer icon that appears after opening the application for the first time. | ![img](https://scontent-hbe1-1.xx.fbcdn.net/v/t1.15752-9/79792403_1732022753589326_1404548279676436480_n.png?_nc_cat=108&_nc_ohc=BuJr-iy9W90AQmC99v4ZCcI-13CteOfD_0PnBZCuI0ev_maCYUNac-Kpw&_nc_ht=scontent-hbe1-1.xx&oh=a6b78fe68a3625ba7fe986994673417a&oe=5EB0C35C)1. After clicking on the fund field, the keyboard should disappear. This happens in expenses and income activities as well. 2. Tool tip overlaps the right side drawer when opened. (This could have been written in a seperate bug report) | Android, HTC one M9 | WiFi    | Average  | Medium   | User experience |
| Filter Drawer - Design - Elements_Do_Not_Fit_Correctly       | 1. Open Monefy application. 2. Press on the drawer in the top left corner. 3. Check the design spacing. | ![img](https://scontent-hbe1-1.xx.fbcdn.net/v/t1.15752-9/79502587_2996654797026130_6257370224710909952_n.png?_nc_cat=105&_nc_ohc=NLRHeFE504EAQmlCbP-rXcGVHt_FGHsTDzGhvF5PFcD3lvnO1viw8rEEg&_nc_ht=scontent-hbe1-1.xx&oh=7f976dfcfd60a2474f32141b020d3cff&oe=5EB123B1)Choose date element is not allowed sufficient spacing. | Android, HTC one M9 | WiFi    | Minor    | Low      | User Interface  |
| Filter Drawer - Filters - Future_Filtering_of_records_Is_Allowed | 1. Open Monefy application. 2. Press on the drawer in the top left corner. 3. Press on Choose Date. 4. Choose any date in the future. | Calendar should stop at current date as there will be no future records to ever filter. | Android, HTC one M9 | WiFi    | Major    | Medium   | Functionality   |

##### B. UX Comments:

	1. The app does not highlight the premium features. User will learn about the premium features by stumbling upon areas that are not included in the free version.
 	2. There is insufficient instructions regarding how to use the app. Only after opening the app for the first time, tool tips appear to show the user the location of the important areas of the app. Example: To add expense, user must enter fund then choose category. User will be confused regarding how to submit the expense until they understand that they can only proceed by choosing a category.
 	3. Currency field in the settings can have a search bar that will give the user the option to search immediately instead of scrolling the whole list.
 	4. About and privacy policy can be merged together under a different section than the General settings.
 	5. The tab categories is useless as a name as it merely allows the user to change the icon of a category or merge it with another or delete it. It can be renamed to "display" to indicate that it is not related to any functionality but rather only the look of the app.
 	6. The filter of tracking the records are mostly useless in the beginning of the user's journey in using the app. This space could be used to allow the user to insert short term goals or otherwise.
 	7. Linking the app with a Gmail account could be more useful regarding the default currency that should be used and can be fetched according to the user's location. Also this would make saving any related information and restoring it easier.

## Third Part: Test Automation

##### Test Cases:

My chosen website will be Youtube. In this case, I assumed that only the test data can be changed to produce more test cases.

| Test Case Name                  | Steps                                                        | Expected Result                   |
| ------------------------------- | ------------------------------------------------------------ | --------------------------------- |
| TC 1 - Testing the search field | 1. Open www.youtube.com. 2. Write in the search bar any of the following test data then press Enter: a. Liverpool vs. Barcelona. b. 123456. c. 1264!@#. d. تعلم . | 1. Related results should appear. |
| TC 2 - Testing the search icon  | 1. Open www.youtube.com. 2. Write in the search bar any of the following test data then press on the search icon on the right: a. Liverpool vs. Barcelona. b. 123456. c. 1264!@#. d. تعلم . | 1. Related results should appear. |



##### Automated Tests:

##### TC 1 - Testing the search field 

Repeat this test case for each of the test data given above in the test case.

###### Using Selenium Web driver:

`import java.util.concurrent.TimeUnit;`

`import org.openqa.selenium.WebDriver;`
`import org.openqa.selenium.chrome.ChromeDriver;`

`public class FirstTestInSelenium {`

`public static void main(String[] args) {`
`// TODO Auto-generated method stub`

`//setting the driver executable`
`System.setProperty("webdriver.chrome.driver", "C:\\Users\\Downloads\\chromedriver.exe");`

`//Initiating your chromedriver`
`WebDriver driver=new ChromeDriver();`

`//Applied wait time`
`driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);`
`//maximize window`
`driver.manage().window().maximize();`

`//open browser with desried URL`
`driver.get("https://www.youtube.com");`

`WebElement elem = wd.findElement(By.id("search")); //finding the web element using name locator`
`elem.sendKeys(new String[]{"Testing User interface of search field "});`
`elem.submit();`

`//closing the browser`
`driver.close();`

`}`

`}`

##### TC 2 - Testing the search icon

###### Using Selenium Web driver:

`import java.util.concurrent.TimeUnit;`

`import org.openqa.selenium.WebDriver;`
`import org.openqa.selenium.chrome.ChromeDriver;`

`public class FirstTestInSelenium {`

`public static void main(String[] args) {`
`// TODO Auto-generated method stub`

`//setting the driver executable`
`System.setProperty("webdriver.chrome.driver", "C:\\Users\\Downloads\\chromedriver.exe");`

`//Initiating your chromedriver`
`WebDriver driver=new ChromeDriver();`

`//Applied wait time`
`driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);`
`//maximize window`
`driver.manage().window().maximize();`

`//open browser with desried URL`
`driver.get("https://www.youtube.com");`

`WebElement searchElem = wd.findElement(By.id("search")); //finding the web element using name locator`

`WebElement SearchIconElem = wd.findElement(By.id("search_icon_legacy")); //finding the web element using name locator`
`searchElem.sendKeys(new String[]{"Testing User interface of search icon"});`
`SearchIconElem.submit();`

`//closing the browser`
`driver.close();`

`}`

`}`