# UPI Transaction-Dashboard (2024)

### Dashboard Link : https://suraj-shukla45.github.io/UPI-Transaction-Dashboard-Power-BI/

## Problem Statement

This dashboard helps to understand how money moves through customer accounts over the year 2024. It shows the total transaction amount and the remaining account balance month by month, so patterns like peak months and low months can be identified easily.

Using the 10 common filters (Bank, City, Device Type, Gender, Age Group, Merchant, Payment Method, Purpose, Transaction Type), the data can be sliced from many angles to find which segments contribute more to transactions and balances.

The second page gives a city-wise and month-wise view of Amount and Remaining Balance, along with the currency used in each city, which helps in comparing how different cities perform over the year.

## Tools Used

- Power BI Desktop
- Power BI Service
- DAX

## Report Structure

The report has **2 pages** and **10 common slicers** that work on both pages (slicers are synced). If a filter is applied on one page, the same selection is automatically applied on the other page too.

| Page | Content |
|---|---|
| Page 1 | 4 charts (Transaction line, Transaction column, Balance line, Balance column) switched using bookmarks and buttons |
| Page 2 | Matrix (table) showing Amount and Remaining Balance by City, Currency and Month |

## Steps followed

- Step 1 : Load the dataset into Power BI Desktop.
- Step 2 : Open Power Query Editor and check "column distribution", "column quality" and "column profile" (based on entire dataset) to find errors and empty values.
- Step 3 : Clean the data and set correct data types.
- Step 4 : Create a calculated column for **Age Groups** to group customers by age.
- Step 5 : Add 10 slicers on Page 1: **BankNameSent, BankNameReceived, City, DeviceType, Gender, Age Groups, MerchantName, PaymentMethod, Purpose, TransactionType**.
- Step 6 : Build 4 charts on Page 1 and place them on top of each other in the same area:
  - Transaction by Month (Line) (2024)
  - Transaction by Month (Column) (2024)
  - Balance by Month (Line) (2024)
  - Balance by Month (Column) (2024)
- Step 7 : Create one **bookmark** for each chart (Line Chart (Transaction), Column Chart (Transaction), Line Chart (Balance), Column Chart (Balance)) from the Bookmarks pane, hiding the other 3 charts in each bookmark using the Selection pane.
- Step 8 : Add 4 **buttons** at the top of the chart area and link each button to its bookmark using the Action option, so the user can switch between charts with a click.
- Step 9 : Create Page 2 and add a **matrix** with City and Currency in columns, Month in rows and Amount and RemainingBalance in values. Conditional formatting (background color) was applied to the values.
- Step 10 : Copy the same slicers to Page 2 and use **View → Sync slicers** to sync all 10 slicers across both pages.
- Step 11 : Apply theme and formatting (titles, borders, shadows) for a clean look.
- Step 12 : Publish the report to Power BI Service.

<!-- Add your DAX measures / calculated columns here, for example: -->
<!-- Age Groups = SWITCH(TRUE(), ...) -->

# Snapshot of Dashboard
## Page 1
<img width="400" height="230" alt="Image" src="https://github.com/user-attachments/assets/8659ab3a-fb07-44a3-b374-cac5a2bc7102" />
<img width="400" height="230" alt="Image" src="https://github.com/user-attachments/assets/9adb50dc-55cc-47f2-a1df-fe61af0047b6" />
<img width="400" height="230" alt="Image" src="https://github.com/user-attachments/assets/e62d37d6-a590-4fde-b45e-42ab36158015" />
<img width="400" height="230" alt="Image" src="https://github.com/user-attachments/assets/af2581a0-c412-46d0-a173-be7bb5e399f9" />

## Page 2
<img width="805" height="462" alt="Image" src="https://github.com/user-attachments/assets/bec99a79-7aa0-451f-aca3-6e2382b2cdc4" />

# Insights

## Page 1

### Chart 1 : Transaction by Month (Line) (2024)

| Month | Amount |
|---|---|
| January | 1,679K |
| February | 1,693K |
| March | 1,624K |
| April | 1,663K |
| May | 1,707K |
| June | 1,653K |
| July | 1,610K |
| August | 1,599K |
| September | 1,667K |
| October | 1,691K |
| November | 1,642K |
| December | 1,646K |

- Amount rises from January (1,679K) to February (1,693K), then drops sharply in March (1,624K).
- It recovers in April and reaches the yearly peak in May (1,707K).
- From May it keeps falling and touches the yearly low in August (1,599K).
- It recovers strongly in September (1,667K) and October (1,691K), then dips in November (1,642K) and stays almost flat in December (1,646K).

        thus, the line shows a rise and fall pattern with peaks in February, May and October, and lows in March, August and November.

### Chart 2 : Transaction by Month (Column) (2024)

- January 1.68M, February 1.69M, March 1.62M, April 1.66M, May 1.71M, June 1.65M
- July 1.61M, August 1.60M, September 1.67M, October 1.69M, November 1.64M, December 1.65M

        thus, May (1.71M) is the highest month and August (1.60M) is the lowest.
        All months stay in a narrow range of 1.6M to 1.7M, so transactions are fairly stable through the year.

### Chart 3 : Balance by Month (Line) (2024)

- Balance is highest in May (1,707K) and lowest in August (1,599K).
- Sharp fall in March (1,624K), recovery till May, decline till August, recovery till October (1,691K), then a small dip in November (1,642K).

<!-- NOTE: these values are same as Transaction line chart. Check that this chart uses RemainingBalance, then update this section. -->

### Chart 4 : Balance by Month (Column) (2024)

- January 8.2M, February 8.4M, March 8.3M, April 8.4M, May 8.2M, June 8.5M
- July 8.3M, August 8.4M, September 8.4M, October 8.4M, November 8.3M, December 8.4M

        thus, June (8.5M) has the highest balance, and January and May (8.2M) have the lowest.
        Balance stays between 8.2M and 8.5M, so it is quite stable across the year.

## Page 2

### Matrix : City-wise Amount and Remaining Balance by Month

Each city uses a different currency: Bangalore (EUR), Delhi (USD), Hyderabad (GBP), Mumbai (INR).

| Month | City | Amount | Remaining Balance |
|---|---|---|---|
| January | Mumbai | 1,678,735 | 8,231,686 |
| February | Delhi | 1,692,738 | 8,352,849 |
| March | Bangalore | 1,623,693 | 8,251,925 |
| April | Hyderabad | 1,662,907 | 8,442,456 |
| May | Mumbai | 1,706,786 | 8,222,007 |
| June | Delhi | 1,652,588 | 8,535,972 |
| July | Bangalore | 1,609,833 | 8,330,594 |
| August | Hyderabad | 1,598,709 | 8,433,286 |
| September | Mumbai | 1,667,044 | 8,433,149 |
| October | Delhi | 1,691,413 | 8,421,307 |

- Highest amount: Mumbai in May (1,706,786). Lowest amount: Hyderabad in August (1,598,709).
- Highest remaining balance: Delhi in June (8,535,972). Lowest: Mumbai in May (8,222,007).
- Conditional formatting (color shades) helps to spot high and low values quickly.

## Interactivity

- 10 common slicers are synced on both pages, so a filter applied on one page also changes the other page.
- Buttons with bookmarks let the user switch between the 4 charts on Page 1.

All values will change if different slicers are applied.
