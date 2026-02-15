# Inventory Management System

A simple **object-oriented inventory management system** written in **Python**, designed to manage various types of products, including general, perishable, and electronic items. This project demonstrates Python OOP concepts like inheritance, encapsulation, and polymorphism.

---

## Features

- **Add Products:** Add standard, perishable, and electronic products to inventory.
- **Calculate Product Value:** Automatically calculate the total value of products.
  - Perishable products can have discounts if close to expiry.
  - Electronic products include a fixed tax rate in value calculation.
- **Inventory Summary:** View all products and their calculated values.
- **Search Functionality:** Search for products by name.

---

## Classes Overview

### `Product`
- Base class for all products.
- Attributes: `product_id`, `name`, `price`, `quantity`.
- Methods:
  - `calculate_value()`
  - `get_name()`, `get_id()`, `get_quantity()`
  - `__str__()` for readable display.

### `PerishableProduct` (inherits from `Product`)
- Additional attributes: `expiry_date`, `storage_temperature`.
- Overrides `calculate_value()` to apply a discount if the product is near expiry.

### `ElectronicProduct` (inherits from `Product`)
- Additional attributes: `warranty_period`, `power_consumption`.
- Overrides `calculate_value()` to include a tax rate.

### `Inventory`
- Manages all products in the inventory.
- Methods:
  - `add_product(product)`
  - `get_total_inventory_value()`
  - `find_product_by_name(name)`
  - `show_inventory()`

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/General-Saeed/Hello-Git.git
   cd Hello-Git