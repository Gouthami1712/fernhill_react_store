# Fernhill – React Plant Store

A small e-commerce front end built with React + Vite.

## Run it
```bash
npm install
npm run dev        # http://localhost:5173
npm run build      # production build in /dist
```

## Features
- Search, category filter, sort
- Product detail modal (Esc to close)
- Cart with quantity controls, shipping rules, fake checkout
- Cart persisted in localStorage
- Light/dark theme, responsive, keyboard accessible

## Structure
```
src/
  main.jsx                 entry, wraps App in CartProvider
  App.jsx                  page state: filters, modal, drawer, toast
  index.css                styles and theme tokens
  data/products.js         product list and constants
  context/CartContext.jsx  useReducer + Context + derived totals
  hooks/useLocalStorage.js reusable persistence hook
  components/              Header, Filters, ProductCard, ProductModal, CartDrawer
  utils/format.js          money()
```

## Interview talking points
- Why `useReducer` + Context for the cart (related actions, shared across components)
- `useMemo` for filtered list and cart totals
- `useEffect` cleanup (Esc key listener, toast timer)
- Controlled inputs, conditional rendering, lifting state up
- Next steps: React Router for `/product/:id`, fetch products from an API, tests with Vitest
