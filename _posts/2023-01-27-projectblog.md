---
toc: true
layout: post
description: Outline and planning for my individual feature of the trimester 2 CPT project, following CB requirements
categories: [markdown, week20] 
title: CPT Individual Feature Outline
---

## Feature Description
My feature is a period cycle tracker.

### Program Purpose and Function 
The program can help women track periods, for health and education. This period cycle tracker allows users to submit the information of their last period, including date and length, and the program will use the data to display the date of their next period on a calender. The input is the dates and numbers inputted by the user, and the output is the date of their next period, as well it visually displayed on a calender.

## Code Plan
> according to CB requirements

### Data Abstraction
I will use data abstraction in storing the user input. The date, length of period, and lenth of cycle will all be stored in a JavaScript object. This way, the different types of data can all be compiled together, to make the program's data easier to access when calculating dates for every month. 

### Managing Complexity
I would have to create new sets of variables and functions for each month of the year in order to display each period cycle. By keeping the user's data all in an object, each time the calculation runs for a month's output, it will just access the data in the object, instead of the function being written several times. 

### Procedural Abstraction 
My procedure will take the data from the object and calculate and produce the date of the next period. The parameters will be date and length. This procedure is what creates the output.

### Algorithm Implementation
With this output (sequencing), the program can use this new produced date to run again (iteration) to produce the following month's period. The default is to output 6 months of periods, but if the user chooses to display more, or less, then it will output a different output, which is more or less months (selection).

### Testing
The first call will be the user input of January 4th, 5 days, and 28 days. 28 days will be added to January 1st to produce the next period start and 5 days will be added to this date to calculate period end. Result will be that the periods will last from February 1st to 6th, March 1st to 6th, and March 29th to April 3rd. 
The second call will be the user input of January 4th, 5 days, and 28 days, and to display 6 months instead of 3. 28 days will be added to January 1st to produce the next period start and 5 days will be added to this date to calculate period end. Result will be that the periods will last from February 1st to 6th, March 1st to 6th, March 29th to April 3rd, April 26th to May 1st, May 24th to May 29th, and June 26 to July 1st.

## Video Plan
I will input the date January 4th into date of last period, 5 days into length of last period, and 28 days into usual menstrual cycle. Program will output that the periods will last from February 1st to 6th, March 1st to 6th, and March 29th to April 3rd. 