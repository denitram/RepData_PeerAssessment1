# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data
1. Load the data (i.e. `read.csv()`)

```r
unzip("activity.zip", exdir = "./data")
data <- read.csv("./data/activity.csv", sep=",", na.strings = "NA")
```
2. Process/transform the data (if necessary) into a format suitable for your analysis

```r
# Convert date to date format
data$date <- as.Date(as.character(data$date), "%Y-%m-%d")
```

## What is mean total number of steps taken per day?
For this part of the assignment, you can ignore the missing values in the dataset.  
1. Make a histogram of the total number of steps taken each day

```r
tot.steps.day <- tapply(data$steps, data$date, sum)
hist(tot.steps.day, main = "Histogram of Total Steps by Day", xlab = "Steps by Day")
```

![](./PA1_template_files/figure-html/totalStepsDay-1.png) 


## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
