# Overview

A CLI app created to help the user log and track delivery orders for their pop-up cafe.


## Goals

As a business:
- I want to maintain a collection of products & couriers
- When a customer makes a new order, I need to create it on the system
- I need to be able to update the status of an order
- When I exit the app, I need all data to be persisted
- When I start the app, I need to load all persisted data
- I want to be sure the app has been tested & proven to work well


## Further Details

All data is persisted in MySQL. Whenever a change is made in-app, the databse is immediately updated. A back-up is also stored in .csv format upon exiting the app. (Note: new files will be written if they do not yet exist!)


## Run

To run:
1. Install the requirements by running 'pip install -r requirements.txt'
2. Make a .env file
3. Run 'python ./mini_project.py' & follow the instructions!


## Key Take-Aways

1. Creating something robust! Handling all sorts of errors to avoid crashes.
2. How to fetch and cache values such as auto_incrementing IDs from the database.
3. Using an ID checking function to cross-reference input versus valid IDs while handling invalid input. The same function is used when dealing with products, couriers or orders (see 'id_check_returns_dict()' on line 144).
4. When storing data in the database, the list of items/products of orders are stored as strings. I thoroughly enjoyed the challenge of having to convert this back into a list (see 'convert_item_values_to_list()' on line 79).