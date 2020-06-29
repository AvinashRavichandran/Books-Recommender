# Books-Recommender

# Tech stack
A full stack application built using GRAM Stack.
The Stack includes GraphQL, React, Apollo and Mongo DB

![Architecture](https://github.com/AvinashRavichandran/Books-Recommender/blob/master/Architecture.png)

# Idea
A book recommendation system to suggest books based on the selected book or the author. Recommends books with similar genre or author.

# Methodology
### Mongo Database

We'll make use of the MLab of MongoDB, which is populated with the data.

![DB](https://github.com/AvinashRavichandran/Books-Recommender/blob/master/DB.png)

The above is MongoDB DB Engine. The below connection string is used to connect to the application.

![Connection](https://github.com/AvinashRavichandran/Books-Recommender/blob/master/Connection.png)

# GraphQL

We have used apollo graphql server and client to connect with the database and REST API endpoints.

![Graph](https://github.com/AvinashRavichandran/Books-Recommender/blob/master/Graph.png)

### Mutations
```
GetBook($id: ID){
        book(id: $id) {
            id
            name
            genre
            author {
                id
                name
                age
                books {
                    name
                    id
                }
            }
        }
    }
    
AddBook($name: String!, $genre: String!, $authorId: ID!){
        addBook(name: $name, genre: $genre, authorId: $authorId){
            name
            id
        }
    }
```

# React
The React app allows us to add more books to the author. 
The user can choose a book which displays the author name, genre of the book and recommends some of the books written by the author.

![Output](https://github.com/AvinashRavichandran/Books-Recommender/blob/master/Output.png)

### Running locally
```
cd graphql/frontend/
npm install
npm start
```

This might start the dev web server at http://localhost:3001 or at http://localhost:3000 depending on your system port availability.
