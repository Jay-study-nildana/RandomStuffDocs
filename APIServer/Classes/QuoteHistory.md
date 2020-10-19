# Class - QuoteHistory

This is where everything related to a specific Quote is store. Each Quote is essentially a collection of 'QuoteHistory' instances that are stored in the database. The most recent entry in the collection will have the latest information about the Quote.

Note : actual implemented, types and such technical details, leave it in the code. Here, its a general, non-code, guideline only.

# Properties

* CreatedTime - Time when the quote was created. 
* CreatedBy - The user who created it.
* Approved - Time when quote was approved.
* ApprovedBy - The user who approved it.
* Deleted - Time when quote was deleted. This is actually what might be called as a soft delete. The Quote History continues to be maintained. That also means, once a quote is created, it never actually leaves the system.
* DeletedBy - The user who deleted it.
* LastModifiedTime - The last time any of the properties were changed.
* HistoryCounter - The current entry, which is, like an incremental number. The first quote history item starts at 1. From there, it becomes +1 of the previous entry.
* QuoteTitle - The Quote Title as per the current instance.
* QuoteContent - The Quote Content. 
* QuoteIdentifier - an unique identifier that acts as a common link across all Quote related tables. Look at file QuoteIdentifier.md for more details.

# important note 

This code is provided as is without any warranties. It's primarily meant for my own personal use, and to make it easy for me share code with my students. Feel free to use this code as it pleases you.

I can be reached through my website - [Jay's Developer Profile](https://jay-study-nildana.github.io/developerprofile)