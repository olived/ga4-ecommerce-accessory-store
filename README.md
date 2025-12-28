GA4 E-commerce Tracking – Accessory Store (Portfolio Project)

This is a portfolio project focused on implementing a complete GA4 e-commerce tracking setup using Google Tag Manager, dataLayer, and advanced debugging, fully prepared for analytical consumption in Looker Studio.

IMPORTANT:
This project uses a fictitious e-commerce store created exclusively for study and portfolio purposes.


PROJECT GOAL

The main objective of this project is to demonstrate, end to end, how to implement a professional GA4 e-commerce tracking setup, covering:

- GA4 standard e-commerce events
- Proper dataLayer structure
- Google Tag Manager configuration (tags, triggers, variables)
- Event validation using Tag Assistant and GA4 DebugView
- Analytics-ready foundation for Looker Studio dashboards


TRACKING ARCHITECTURE

User
  |
  v
Website (HTML + JavaScript)
  |
  v
dataLayer.push()
  |
  v
Google Tag Manager (GTM)
  |
  v
Google Analytics 4 (GA4)
  |
  v
Looker Studio (Analytics Layer)


DEMO STORE OVERVIEW

The project simulates a tech accessories e-commerce store with:

- Product listing page
- Product detail page
- Functional shopping cart flow
- Cart persistence using localStorage

Front-end technologies used:
- HTML5
- CSS3
- Vanilla JavaScript


IMPLEMENTED GA4 EVENTS

All events follow the official GA4 E-commerce specification, including the items[] array.

Event Name        Description
-----------------------------------------------
view_item_list   Product list view
view_item        Product detail view
add_to_cart      Add product to cart
view_cart        Cart view


DATALAYER STRUCTURE EXAMPLE

Example of the dataLayer payload sent to GA4:

dataLayer.push({
  event: "view_cart",
  ecommerce: {
    currency: "USD",
    value: 297,
    items: [
      {
        item_id: "A001",
        item_name: "Wireless Headphones Pro",
        item_category: "Audio",
        price: 99,
        quantity: 3
      }
    ]
  }
});


GOOGLE TAG MANAGER SETUP

Components created:

Triggers:
- Custom events based on dataLayer
  - view_item_list
  - view_item
  - add_to_cart
  - view_cart

Tags:
- GA4 Event Tags
  - One tag per e-commerce event

Custom JavaScript Variables:
- JS – Ecommerce Items
- JS – Ecommerce Value

All triggers and tags were configured following GA4 best practices.


VALIDATION AND DEBUGGING

The project was validated using:

- Google Tag Assistant
- Google Tag Manager Preview Mode
- GA4 DebugView

Validations performed:
- Correct event firing
- Proper e-commerce payload structure
- Variables resolving correctly in GTM
- Events marked as completed in Tag Assistant
- Events visible in GA4 DebugView in real time


LOOKER STUDIO READINESS

The tracking setup is fully prepared for Looker Studio dashboards, enabling analysis such as:

- Product views
- Add to cart actions
- Cart views
- Total cart value
- Navigation funnel (list → product → cart)

The visualization layer can be built directly on top of the implemented GA4 events.


NEXT STEPS (ROADMAP)

- Implement begin_checkout event
- Implement purchase event (simulated checkout)
- Build Looker Studio dashboard
- Add validation screenshots (GA4 and GTM)
- Extend cart to support multiple different products


AUTHOR

This project was developed as a professional analytics portfolio case, focusing on GA4, Google Tag Manager, and Looker Studio best practices.

