# GPT_SQL_Query
ABSTRACT: Using OpenAI &amp; SQL Queries with a Chatbot Assistant

Source: https://www.oreilly.com/library/view/developing-apps-with/9781098152475/

- Very similar to the previous chatbot assistant project (https://github.com/mdbromhal/GPT_Assistant.git)
- However, here, we're asking this chatbot to make an SQL query based on our request
- And then receive the appropriate information
- - - 
Example:
1. Give it some data it can search through
```
results = [
        {"name": "pen", "color": "blue", "price": 2.99}, # Dictionary, json database
        {"name": "pencil", "color": "purple", "price": 1.99},
        {"name": "tape", "color": "light blue", "price": 5.99},
        {"name": "nickel", "color": "silver", "price": 0.05}
    ]
```
2. Give it the prompt: "I need the top 3 products where the price is greater than 2.00"
3. SQL Query the chatbot assistant produces:
```
SELECT * FROM products WHERE price > 2.00 ORDER BY price DESC LIMIT 3
```
5. Retreives the response with that SQL Query:
```
The top 3 products with a price greater than $2.00 are:
1. Tape - Price: $5.99
2. Pen - Price: $2.99
3. Pencil - Price: $1.99
```
