Python script to dynamically populate a "Kobo Shelf" in Calibre Web's database by getting the list of unread books from Calibre metadata.db custom column. 
  
It assumes the metadata.db has a boolean custom column called Read. 
The script grabs list of books without a value in this Read column.   
For each book it finds, it is added to the book_shelf_link table in Calibre Web's app.db.  
