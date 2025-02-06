# One-Card Calendar

## Overview
This project provides a compact, one-page calendar for the entire year of 2025. It is designed to give a quick overview of the dates and days of the week for each month in a single view.

## Features
- **Single View Layout**: All months are displayed on a single card, making it easy to see the entire year at a glance.
- **Dynamic Date Calculation**: Utilizes Excel formulas to accurately display the correct dates and corresponding days of the week for each month.
- **Highlighting Weekends**: Weekends are formatted differently for easy visibility.
- **Optimized Print Area**: The calendar layout is specifically optimized for printing on a 63.5mm x 88mm poker size card, making it portable and convenient for physical use.

## Formulas Used
- **Dynamic Date Array Formula**:
  - `IFERROR(INDEX($O:$O, SMALL(IF($Q:$Q=$H2, ROW($Q:$Q)-MIN(ROW($Q:$Q))+1), ""), ""))`
    - This array formula is used to calculate the n-th occurrence of days in each month, where `$Q:$Q` contains weekday numbers, `$H2` is the target weekday, and `$O:$O` includes all the dates in the year. `SMALL` with `IF` fetches the nth smallest row number that meets the condition, adjusted by `ROW() - MIN(ROW()) + 1` to get the correct position in the list.
- **IFERROR and INDEX**: These functions are used together to pull and display the correct dates in each cell dynamically based on the year 2025.
- **SMALL and ROW**: These functions help in calculating which dates to display where, ensuring that each month aligns correctly according to the days of the week.

## Customization
Users can easily adjust the year by modifying the base date formulas to create similar calendars for other years.

## Usage
This calendar is ideal for anyone needing a quick year-at-a-glance tool to oversee project timelines, personal events, or any other long-term planning.

## Software Requirements
- **LibreOffice Calc**: Designed for use in LibreOffice Calc, ensuring compatibility across different operating systems without the need for specific software purchases.

## How to Get Started
1. Download the ODS file.
2. Open it with LibreOffice Calc.
3. Modify as needed for personal customization.
