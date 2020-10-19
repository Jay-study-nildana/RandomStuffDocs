# QuoteIdentifier

This is a unique ID string used to identify each and every Quote. 

Ulilized in the class QuoteHistory. Look at file QuoteHistory.md

# Formula

This is the formula I came up with to generate this.

    QuoteIdentifier = Title + Date + Time + RandomNumber1000 + RandomStringFive

* Title - - The title portion of the quote. This is actually the person name to whom the quote is said by.
* Date - I will take the date in the form October172020
* Time - I will take the time in the 24 hour format. 1155410 (HourHourMinuteMinuteSecondSecond)
* RandomNumber1000 - A Random Number under 1000. 
* RandomStringFive - Here, this is a little complex. I want a string like xxxxx, for example, abefz. Each character is generated randomly, each time, five times.

# Other Thoughts

Ideally, I would like to use the Guid Generator available in .NET. It creates unique identifiers which are just awesome. However, I wanted the IDs to be more personal. 

# important note 

This code is provided as is without any warranties. It's primarily meant for my own personal use, and to make it easy for me share code with my students. Feel free to use this code as it pleases you.

I can be reached through my website - [Jay's Developer Profile](https://jay-study-nildana.github.io/developerprofile)