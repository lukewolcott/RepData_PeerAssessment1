# Reproducible Research: Peer Assessment 1
By Luke Wolcott

This file describes a data analysis of step counting data.  An anonymous subject walked around with a tracker during October and November of 2012.  The tracker recorded the number of steps in each 5 minute interval during the day.  How many steps were taken each day, on average? How did the steps change throughout the day?  How does weekend and weekday activity compare?  We will try to answer these questions.


## Loading and preprocessing the data

We assume that the file "activity.csv" is in the working directory.

Each hour has 12 5-minute intervals, so there are 24 x 12 = 288 entries per day.  There are 61 days of recorded data, giving 61 x 288=17568 entries total.  

The first column is the number of steps, the second is the date, and the third is the interval (given as an integer, so 835 means the interval starting at 8:35am).  We can load the data frame and add a column that treats the intervals as times, using the following code.


```r
      d <- read.csv("activity.csv", stringsAsFactors = FALSE)
      int_as_time <- formatC(d$interval, width=4, flag="0")
      int_as_time <- strptime(int_as_time, "%H%M")
      d <- cbind(d, int_as_time)
```


## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
