# 🛍️ JavaScript Shop — IndexedDB

A fully client-side e-commerce shop demo built with pure HTML, CSS, and JavaScript. Products and cart data are stored in **IndexedDB**, so your basket persists across page refreshes — no backend, no server needed.

---

## ✨ Features

- 🛒 **Persistent Cart** — Basket survives page refresh using IndexedDB
- ➕ **Add to Cart** — Add any product with quantity tracking
- ➖➕ **Qty Controls** — Increase or decrease item quantity directly in cart
- 🗑️ **Remove Items** — Remove individual items or clear the entire basket
- ✍️ **Custom Orders** — Add your own products with name, description, image, and price
- 💰 **Live Total** — Cart total updates instantly on every change
- 🧾 **Checkout Page** — Separate page showing basket summary and order confirmation
- 📱 **Responsive** — Works on mobile and desktop

---

## 🚀 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/Adnan-Ghiyath/Certificate-generator.git
   ```
2. Open `shop.html` in your browser — no server needed
3. Browse products and click **Add to Basket**
4. Adjust quantities in the cart panel on the right
5. Click **Checkout →** to go to the order summary page
6. On the checkout page, confirm or clear your order

---

## 🗄️ Database Structure (IndexedDB)

| Property | Value |
|----------|-------|
| Database Name | `ShopDB` |
| Version | `1` |
| Store 1 | `products` — seeded on first run |
| Store 2 | `cart` — updated on every add/remove |

Both pages (`shop.html` and `checkout.html`) share the **same database**.

---

## 📁 Project Structure

```
shop.html        # Main shop page (products + cart)
checkout.html    # Checkout page (basket summary + confirm)
shop.css         # All styles for both pages
shop.js          # IndexedDB logic, product rendering, cart management
```

---

## ⚙️ How It Works

```
Page loads
    ↓
Open ShopDB (IndexedDB)
    ↓
Seed products (first run only)
    ↓
Render product cards + cart items
    ↓
User adds/removes items → cart store updates → UI re-renders
    ↓
Checkout → reads same cart store → shows summary
```

**Key IndexedDB operations used:**
- `getAll()` — load all products / cart items
- `get()` — check if item already in cart
- `put()` — add or update cart item
- `delete()` — remove item from cart
- `clear()` — empty entire cart

---

## 🛠️ Built With

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

- Pure Vanilla JavaScript
- IndexedDB (browser-native database)
- Zero dependencies — no npm, no frameworks

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

> Made with ❤️ by [Adnan-Ghiyath](https://github.com/Adnan-Ghiyath)
