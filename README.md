# book-recommender
This is a recommender for books that uses collaborative filtering.

The dataset is taken from the Book-Crossing community. It contains more than 270,000 users, with 1.14 million ratings about more than 270,000 books.

The model is built user TensorFlow.
Aside from using a MinMaxScaler on ratings, the data has not been transformed in any other way.

Steps:
1. The datasets are first merged to create:
  - dataset with number of ratings for each book
  - dataset with number of ratings for each user

2. Then users and books with fewer than 15 ratings are removed.

3. This leaves us with 
Number of unique books:  5854
Number of unique users:  4121

4. The ratings are scaled with MinMaxScaler.

5. The model is built using TensorFlow - output: recommendation of top 10 books for user.



p.s. I have reservations about this model. It seems to recommend the same set of books for users I have tested this on. 
Granted the books recommended are hugely popular (Harry Potter, To Kill a Mockingbird etc), and are likely to be well-received by most users.
Perhaps the model works as it should, but it also makes most users read the same things in the end.
Will be useful for the mainstream reader, but not so useful for any self-respecting hipster it seems.
