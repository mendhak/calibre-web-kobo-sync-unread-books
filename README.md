Python script to dynamically populate a "Kobo Shelf" in Calibre Web's database by getting the list of unread books from Calibre metadata.db custom column. 
  
It assumes the metadata.db has a boolean custom column called Read. 
The script grabs list of books without a value in this Read column.   
For each book it finds, it is added to the book_shelf_link table in Calibre Web's app.db.  

Assumptions: 

* In Calibre Web (app.db), the Kobo Shelf ID is `1``.   
* In Calibre DB (metadata.db), the Read column is in the table `custom_column_1`  


Worth considering: 

* The Calibre Web db has its own read_status column in the book_read_link. Could combine that, and not add to the Kobo shelf if the book is marked read in Calibre Web. 