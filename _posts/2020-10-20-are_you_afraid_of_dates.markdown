---
layout: post
title:      "Are you afraid of dates?"
date:       2020-10-20 12:42:21 -0400
permalink:  are_you_afraid_of_dates
---


I was afraid of dates. I wanted to stay away from them, but we are web developers and it is very important to have a good understanding about how to use Date objects.

For my final project I decided to build a car rental app and the most important part of my app is to avoid double bookings. Now I want to talk about how I found the solution.
Lets think about what we need to make this work. We have to select dates, select the Start day and the End day.
Ok, now what do we have to do? 
We have to find all the days between the Start date and End date. Lets define a function that is going to do that for us.
 
```
  const getSearchDates = (stDate, endDate ) => {
      let std = new Date(stDate)
      let end = new Date(endDate)
      let days = []
      let daysInTime = end.getTime() - std.getTime();
      let totalDays = daysInTime / (1000 * 3600 * 24);
      
      for (let i = 0; i < Math.ceil(totalDays); i++){
        let nextDay = new Date(stDaye)
          nextDay.setDate(nextDay.getDate() + i)
          days = [...days, nextDay]
      }
      return days
   }
```
Lets break the code down.  `let std = new Date(stDaye)` and `let end = new Date(endDate)` are the selected dates.
`let days = []` array is where we want to populate our dates. Now we want to find how many days are between the start date and the end date. 
`let daysInTime = end.getTime() - std.getTime();` The `getTime()` method returns the number of milliseconds. 
  `const date = new Date();` `console.log(date.getTime());` and output: 1603205407144.  This means if we take out from our  `end.getTime()` the `std.getTime()` will find the amount of selected days in milliseconds. Now lets return milliseconds to total days. `   let totalDays = daysInTime / (1000 * 3600 * 24);`Cool. We are doing good, we have everything we need for our `for loop`.
	
	     for (let i = 0; i < Math.ceil(totalDays); i++){
        let nextDay = new Date(stDaye)
          nextDay.setDate(nextDay.getDate() + i)
          days = [...days, nextDay]
      }
			
Here we have the code` let nextDay = new Date(stDaye)` is representing the selected start day. `nextDay.setDate(nextDay.getDate() + i)` will create the next day for us and  `days = [...days, nextDay]` populates the days array with the new date.
Now you have an array with a selected date. All you have to do is use the same function for booking dates and compare 2 arrays and check for availability.  Here is how I’m comparing two arrays for the same days.

```
 const compare = (arr1, arr2) => {
   const finalArray = []
   arr1.forEach(e1 => arr2.forEach(e2 =>
     {if (e1.getTime() === e2){
       finalArray.push(e1)
     } 
   } 
) )
     return finalArray
}
```
 If the compare returns an empty array, it means that we can display that item for rent for the selected dates. If not, it's already booked.
We have two functions, now it's up to you where you want to use them. I hope you found this article helpful.


 
