# Paradise Nursery Shopping Application

A modern, responsive e-commerce application for purchasing house plants, built with React and Redux Toolkit.

## Project Overview

Paradise Nursery is a shopping cart application that offers a variety of house plants across different categories. The application provides a seamless shopping experience with features like product browsing, cart management, and dynamic quantity updates.

## Features

### Core Functionality
- **Landing Page**: Welcoming homepage with "Get Started" button that navigates to the product listing
- **Navigation Bar**: Persistent navbar with links to:
  - Paradise Nursery (Home)
  - Plants (Product Listing)
  - Cart Icon with live item count badge

### Product Catalog
- **Multiple Categories**: Plants organized into distinct sections:
  - Air Purifying Plants
  - Aromatic Fragrant Plants
  - Insect Repellent Plants
  - Medicinal Plants
  - Low Maintenance Plants

- **Product Cards**: Each plant displayed with:
  - High-quality image
  - Plant name
  - Detailed description
  - Price
  - "Add to Cart" button

### Shopping Cart
- **Cart Management**:
  - View all items added to cart
  - Display product thumbnail, name, and unit cost
  - Show quantity for each product
  - Calculate and display total cost per product type
  - Calculate and display overall cart total

- **Quantity Controls**:
  - Increment button (+) to increase quantity
  - Decrement button (-) to decrease quantity
  - Automatic removal when quantity reaches zero
  - Delete button for immediate removal

- **Navigation Buttons**:
  - Continue Shopping: Returns to product listing
  - Checkout: Proceed to checkout (ready for future integration)

### Dynamic Features
- **Live Cart Count**: Real-time update of total items in cart badge
- **Automatic Total Calculation**: Cart total updates instantly when quantities change
- **State Management**: Powered by Redux Toolkit for reliable state handling

## Technology Stack

- **React 18.2.0**: Modern UI library with functional components
- **Redux Toolkit 2.2.3**: State management with simplified Redux setup
- **React-Redux 9.1.1**: Official React bindings for Redux
- **Vite 5.2.0**: Fast build tool and development server
- **ESLint**: Code quality and consistency

## Project Structure

```
e-plantShopping/
├── src/
│   ├── App.jsx              # Main application component
│   ├── App.css              # Main application styles
│   ├── ProductList.jsx      # Product catalog component
│   ├── ProductList.css      # Product listing styles
│   ├── CartItem.jsx         # Shopping cart component
│   ├── CartItem.css         # Cart styles
│   ├── CartSlice.jsx        # Redux slice for cart state
│   ├── AboutUs.jsx          # About section component
│   ├── AboutUs.css          # About section styles
│   ├── store.js             # Redux store configuration
│   ├── main.jsx             # Application entry point
│   └── index.css            # Global styles
├── public/                  # Static assets
├── package.json             # Project dependencies
└── README.md               # Project documentation
```

## Installation & Setup

1. **Clone the repository**
```bash
git clone <your-forked-repo-url>
cd e-plantShopping
```

2. **Install dependencies**
```bash
npm install
```

3. **Run development server**
```bash
npm run dev
```

4. **Build for production**
```bash
npm run build
```

5. **Preview production build**
```bash
npm run preview
```

## Key Components

### CartSlice.jsx
Redux slice managing cart state with three actions:
- `addItem`: Adds new item or increments quantity if exists
- `removeItem`: Removes item from cart
- `updateQuantity`: Updates item quantity

### ProductList.jsx
Displays product catalog with:
- Category sections
- Product cards with images and details
- Add to Cart functionality
- Navigation between product view and cart

### CartItem.jsx
Shopping cart interface with:
- Item list with thumbnails
- Quantity controls (+/- buttons)
- Individual and total cost calculations
- Delete functionality
- Continue Shopping and Checkout buttons

## Redux State Structure

```javascript
{
  cart: {
    items: [
      {
        name: "Plant Name",
        image: "image-url",
        cost: "$XX",
        quantity: number
      }
    ]
  }
}
```

## Learning Objectives Demonstrated

✅ React functional components with hooks (useState, useEffect)
✅ Component composition and nesting
✅ Redux integration (actions, reducers, store)
✅ State management with Redux Toolkit
✅ Dynamic data rendering from arrays
✅ Event handling and conditional rendering
✅ Responsive design principles

## Future Enhancements

- User authentication
- Checkout and payment integration
- Order history
- Product search and filtering
- User reviews and ratings
- Wishlist functionality

## Author

Created as part of the IBM Developer Skills Network course project.

## License

This project is licensed under the Apache License 2.0 - see the LICENSE file for details.
