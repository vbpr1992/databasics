## Explorer Mode:

1.How many users are there?
  - `SQL:` SELECT COUNT ("asterisk") FROM users

  - `ANSWER:`50


2.What are the titles of the 5 most expensive items?
 - `SQL:` SELECT title, price FROM items ORDER BY price DESC LIMIT 5;

 - `ANSWER:` Small Cotton Gloves, Small Wooden Computer, Awesome Granite Pants, Sleek Wooden Hat, Ergonomic Steel Car


3.What's the cheapest item in the `Books` category?
 - `SQL:`SELECT title, category, price FROM items WHERE category LIKE 'Books' ORDER BY price LIMIT 1;

 - `ANSWER:`Ergonomic Granite Chair


4.Who lives at 6439 Zetta Hills, Willmouth, WY?
 - `SQL:`SELECT users.first_name, users.last_name, addresses.street FROM users, addresses WHERE user.id = addresses.user_id AND street = '6439 Zetta Hills' AND city = 'Willmouth' and state = 'WY';

 - `ANSWER:`Corrine Little


5.Correct Virginie Mitchell's address to "New York, NY, 10108".
  - `SQL:`UPDATE addresses SET city = 'New York', state = 'NY', zip = 10108 WHERE user_id = 39;

  - `ANSWER:`Done

6.How much would it cost to buy one of each item in the `Tools` category?
  - `SQL:`SELECT sum(price) FROM items WHERE category = 'Tools';

  - `ANSWER:` 7383

7.How many total items did we sell?
  - `SQL:`SELECT sum(quantity) FROM orders

  - `ANSWER:`2125

8.How much was spent on `Books`?
   - `SQL:`SELECT sum(quantity), sum(price) FROM orders, items WHERE orders.item_id = items.id and items.category = 'Books';

   - `ANSWER:`Quantity Total: 72 and Price Total: 68982

9.Simulate buying an item by inserting a User for yourself and an Order for yourself.
  - `SQL:`PART 1: INSERT INTO users VALUES (51, 'Valeria', 'Benetti','vbenetti46@gmail.com')
          PART 2: INSERT INTO orders VALUES (377, 51, 90, 4,'2017-02-09 00:40:31.307668')

  - `ANSWER:`Done and Done
