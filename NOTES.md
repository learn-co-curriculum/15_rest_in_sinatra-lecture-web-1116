## REST

1. GET '/books'- index action on the books controller - shows all the books
2. POST '/books' - 'create' action on the books controller - creates a book
3. DELETE '/books/:id' - 'destroy' action - deletes that particular book
4. GET '/books/:id' - 'show' action - displays info on one particular book
5. PUT/PATCH '/books/:id' - 'update' action - will update a resource for a particular book

## REST activity

Write out all of the RESTful routes and actions for our 'authors' resource
1. See all the authors
  GET '/authors' -> AuthorsController -> 'index' action -> Author.all -> SELECT * FROM authors
2. See one author
  GET '/authors/:id' -> AuthorsController -> 'show' action -> Author.find(params[:id]) -> SELECT * FROM authors WHERE id = 5
3. Create an author
  GET '/authors/new' -> AuthorsController -> 'new' action -> No SQL fires here
  POST '/authors' -> AuthorsController -> 'create' action -> Author.create(params[:authors]) - INSERT INTO authors (columns) VALUES (values)
4. Delete an author
  DELETE '/authors/:id' -> AuthorsController -> 'destroy' action -> author = Author.find(params[:id]) author.destroy - 'DELETE FROM authors WHERE id = 7'
5. Update an author
  GET '/authors/:id/edit' -> AuthorsController -> 'edit' action -> Author.find(params[:id])
  PATCH '/authors/:id' -> AuthorsController -> 'update' action -> Author.find(params[:id]) , author.update -> UPDATE authors SET values WHERE id = 7





## Edit and Update

1. When the user submits the form, we should update that record in the database
