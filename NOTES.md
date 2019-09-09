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

  OR

1. User logs in from home page.
2. User searches a title from logged-in home page.
3. Directed to search results page with possible book matches.
  Clicking on a book will take the user to the similar books page.
  * This will access the Goodreads reviews API, passing in the chosen book's ID
    number: https://www.goodreads.com/api/index#book.show
4. User can click to add any similar book to his/her want-to-read list.
5. User has access to want-to-read list with info and links for each saved book.

- Routes
Root: welcome#home (log-in posts to user#create)
User: create (redirects to user#show), show (has search box, posts to user/books#create)
User/books: create(), index (user's saved searches list)

## Routes

1. searches - only :index and :create (:index will be home page, :create will be
  search results page)
2. books - only :index (similar books page)

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
