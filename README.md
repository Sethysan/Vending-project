# Vending Machine Vue.js App

This is a Vue.js-based web application that simulates a vending machine where users can add funds and purchase items. The application uses Vuex for state management and is hosted on [Netlify](https://zingy-puffpuff-1c267c.netlify.app/).

## Live Demo

Check out the live demo of the project here: [Vending Machine App](https://zingy-puffpuff-1c267c.netlify.app/)

## Features

- **Products Display:** Shows a list of products available for purchase, including name, price, type, and quantity.
- **Funds Management:** Users can add funds in increments of $1, $5, and $10.
- **Product Purchase:** Users can purchase items if they have sufficient funds and the product is in stock. Each purchase decreases the funds and product inventory.
- **Responsive UI:** A simple and responsive interface to manage funds and make purchases.

## Tech Stack

- **Vue.js**: JavaScript framework used to build the user interface.
- **Vuex**: State management pattern used to handle the application's state, such as funds and product inventory.
- **Vite**: Build tool for fast development.
- **Netlify**: Hosting service for deploying the app.

## Project Structure

```plaintext
├── public
│   └── vite.svg         # Entry point of the app
├── src
│   ├── assets             # Image assets for products
│   ├── components
│   │   ├── FeedComponent.vue   # Component to add funds
│   │   ├── FundsComponent.vue  # Component to display current funds
│   │   ├── ItemComponent.vue   # Component to display individual product
│   │   ├── ProductsComponent.vue # Component to display all products
│   ├── store
│   │   └── index.js         # VueX store for state management
│   ├── App.vue              # Main Vue app component
│   └── main.js              # App entry point and Vue initialization
├── vite.config.js           # Vite configuration file
├── package.json             # Project dependencies and scripts
└── README.md                # Project documentation


How to Run the Project
Clone the repository:

bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

Install dependencies:

bash
npm install

Run the app:

bash
npm run dev

Build for production:

bash
npm run build

VueX Store
The state of the application is managed using VueX, with the following key components:

State:
funds: The amount of money the user has.
products: An array of product objects, each with id, name, price, type, quantity, and img.

Mutations:
DECREASE_FUNDS: Deducts funds when a product is purchased.
INCREASE_FUNDS: Adds funds when a user clicks the "ADD FUNDS" button.
DECREASE_INVENTORY: Reduces product quantity when an item is purchased.

Getters:
getProduct: Retrieves product information by id.

Components
ProductsComponent.vue: Displays a list of products using the ItemComponent.
ItemComponent.vue: Handles individual product information and purchase logic.
FundsComponent.vue: Displays the current balance of funds.
FeedComponent.vue: Provides buttons to add funds to the user's balance.

License
This project is licensed under the MIT License.
