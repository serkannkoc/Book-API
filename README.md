# Book Relationship Management
![alt text](https://media.istockphoto.com/photos/collection-of-old-books-in-library-picture-id1299842132?k=20&m=1299842132&s=612x612&w=0&h=YTvSQ1fdSrpLWmq2Tr2Z7W_YUjFSWUyBn3ZtnaZjB2w=)


Coded this project to learn ASP.Net Core 5.0 Web Api development when I was
intern at DGPays.

## Project Summary  

* Design the relationships between books, publishers and authors.
* CRUD operations on relational data.
* Custom global error handling.
* Sorting, filtering and paging data.
* Different types of API versioning.
* Logging to database.
* Unit tests on controllers and services.

## Used Technologies  

* ASP.Net Core 5.0
* Microsoft Sql Server
* Entity Framework Core
* Serilog
* NUnit
* Postman

## Database Diagram
![alt text](https://github.com/serkannkoc/Book-API/blob/main/screenshots/Screenshot_1.png?raw=true)
## File Structure
The project is 2 tier architecture. Which are the project and testing.  

Project structure is below
* Action Results
* Controllers
* Data
    * Models
    * Paging
    * Services
    * View Models
* Exceptions
* Logs
* Tests

    
## Endpoints
To get all publishers use the below endpoint.
| Type | Method |
| ------ | ------ |
| GET | localhost:44368/api/publishers/get-all-publishers |  

You can add parameters to this endpoint to sort, filter and page. Such as  
| Type | Method |
| ------ | ------ |
| GET | localhost:44368/api/publishers/get-all-publishers?sortBy=name_desc |  

Try to add a book with its authors this endpoint.
| Type | Method |
| ------ | ------ |
| POST | localhost:44368/api/books/add-book-with-authors |  

Request body 
```
{
    "Title":"The Metamorphosis",
    "Description":"The Metamorphosis is a short novel by Franz Kafka, 
    first published in 1915.",
    "IsRead":true,
    "DateRead":"2018-07-12",
    "Rate" : 7,
    "Genre" : "Fiction",
    "CoverUrl":"https...",
    "PublisherId" : 3,
    "AuthorIds" : [2,3]
}
```



* Other endpoints can be reached from the below link.
[![Run in Postman](https://run.pstmn.io/button.svg)](https://god.postman.co/run-collection/e03e21df83eb5352aec9?action=collection%2Fimport)


