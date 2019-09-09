# Planning and notes

## Basic operation

1. User will enter a search term (book title) on the home page.
  * This will access the Goodreads search API:
    https://www.goodreads.com/api/index#search.books
2. Directed to search results page that will list possible book matches.
  Clicking on a book will take the user to the similar books page.
  * This will access the Goodreads reviews API, passing in the chosen book's ID
    number: https://www.goodreads.com/api/index#book.show
3. The similar books page will list similar books found by the API with a link
  to each book's Goodreads page.

## Models

1. Search
2. Book

## Views

1. Root - home page
2. Search results
3. Similar books

## Controllers

1. Search controller
2. Book controller
