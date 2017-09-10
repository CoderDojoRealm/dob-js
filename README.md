# dob-js
An intro project with basic HTML, CSS and JS

# Overview

This project was created in a beginners HTML/CSS/JS workshop at CoderDojo Realm.

It is a basic HTML/CSS page with a JavaScript app that asks the user for their date of birth,
and then calculates the number of hours that person has been alive.

# Technical notes

It purposely avoids using any JavaScript libraries, and keeps everything in one file for 
simplicity.

The function ```submitForm()``` is run when the form is submitted. When run, it uses the 
JavaScript ```Date``` object to set up a date from the input data, which it then turns
into a timestamp integer (which is the number of seconds since epoch). JavaScript handles
dates in microseconds, so we divide by 1000 to get seconds. 

The function then does the same for the current date/time, and then subtracts one from the
other to get the number of seconds the person has been alive.

When outputing the time, it trims off the fraction part by using the ```toFixed()``` method
on the ```Date``` object.

Note also that the function is bound to the form in the HTML with the attribute 
```onsubmit="submitForm(); return false;"```. The ```return false;``` part prevents
the form from refreshing the page.

# Ideas for further work

- Ninjas, try extending this app to display the results back onto the page in HTML rather 
than using the ```alert()``` statement. Hint: You could create an empty ```DIV``` element 
and then replace its ```innerHTML``` with the results. Or you could look to the JQuery
library for fancier special animation effects.
- How about improving the input validation, to ensure the user can only type valid dates.
- Perhaps add extra controls onto the form to allow the user to select whether to show 
  seconds, hours, days, weeks, months or years as the output

