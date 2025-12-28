# GA4 E-commerce Tracking – Portfolio Project

## Overview
This project demonstrates a complete **GA4 E-commerce tracking implementation** built from scratch for portfolio purposes.  
The goal is to showcase best practices in **event tracking, Google Tag Manager setup, and analytical readiness for Looker Studio dashboards**.

All data, products, and flows were intentionally created to simulate a real-world e-commerce scenario.

---

## Architecture

User  
↓  
Website (HTML + JavaScript)  
↓  
dataLayer.push()  
↓  
Google Tag Manager (GTM)  
↓  
Google Analytics 4 (GA4)  
↓  
Looker Studio (Analytics Layer)

---

## GA4 E-commerce Events Implemented

All events follow the **official GA4 E-commerce specification**, including the `items[]` array.

| Event Name       | Description                               |
|-----------------|-------------------------------------------|
| view_item_list  | Product list visualization                |
| view_item       | Product detail view                       |
| add_to_cart     | Product added to cart                     |
| view_cart       | Cart visualization                        |

---

## Shopping Cart Logic

- Cart persistence implemented using **localStorage**
- Quantity increment logic supported
- Total cart value dynamically calculated
- Cart state restored on page reload

---

## Google Tag Manager (GTM)

### Components Created

**Triggers**
- Custom Events based on `dataLayer` events

**Tags**
- GA4 Configuration Tag
- GA4 Event Tags for:
  - view_item_list
  - view_item
  - add_to_cart
  - view_cart

**Custom JavaScript Variables**
- JS – Ecommerce Items
- JS – Ecommerce Value

All triggers and tags follow GA4 best practices.

---

## Validation & Debugging

The implementation was validated using:

- Google Tag Assistant
- GTM Preview Mode
- GA4 DebugView

### Validations Performed
- Correct firing of all GA4 events
- Validation of `items[]` structure
- Currency and value consistency
- Proper event sequencing

---

## Technologies Used

- HTML5
- JavaScript (Vanilla)
- Google Tag Manager
- Google Analytics 4
- Looker Studio (data-ready)

---

## Portfolio Notes

This project was designed exclusively for **demonstration and portfolio purposes**.  
No real users or transactions are involved.

It reflects a production-like GA4 tracking setup that can be applied to real e-commerce environments.

---

## Author

Daniel Gomes de Oliveira  
Data & Analytics Consultant  
Specialized in GA4, GTM, BI & Data Engineering
