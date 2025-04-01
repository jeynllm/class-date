# Date Class Documentation

The `Date` class in Java represents a calendar date with day, month, and year.

## Class Overview

Provides functionality for date creation, validation, modification, comparison, day-of-week retrieval, and difference calculation. Implements `Comparable` for sorting.

## Constructor

### `Date(int day, int month, int year)`

Creates a new `Date` object.

**Parameters:** `day`, `month` (1-12), `year`.

## Methods

### `boolean isValidDate(int day, int month, int year)`

Checks if the date is valid. Updates the object's date if valid.

**Returns:** `true` if valid, `false` otherwise.

### `void updateDate(int d, int m, int y)`

Updates the date if the new date is valid. Prints update status.

### `void printDate()`

Prints the date in "Month Day, Year" format if valid.

### `int compareTo(Date date)`

Compares this date to another for chronological order (for sorting).

**Returns:** Negative, zero, or positive integer.

### `String getDayOfWeek()`

Returns the day of the week as a `String`.

### `String calculateDifference(Date subtrahend)`

Calculates the absolute difference in days between this date and `subtrahend`.

**Returns:** "Difference is : [days]" or "Date is not valid".

## Usage Example

```java
ArrayList<Date> dates = new ArrayList<Date>();
dates.add(new Date(25, 3, 2025));
// ... (add more dates)

for (Date d : dates) {
    System.out.println(d.isValidDate(d.day, d.month, d.year));
    d.printDate();
}

Collections.sort(dates);
// ... (other operations like updateDate, getDayOfWeek, calculateDifference)
