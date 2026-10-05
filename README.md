# Lusaka City Council Market Management System

A working prototype of a digital system for managing public markets in Lusaka. It brings market registration, stall allocation, rent collection, incident alerts and an online marketplace into one place, with separate views for the Council and for each market manager.

The whole prototype is a single file (`index.html`), so it opens in any modern browser with no installation.

## Markets in the prototype

- Simon Mwewa Lane Market
- City Market
- Town Center Market

Stall counts, facilities and manager names are sample values to be replaced with official records.

## Features

### Council dashboard
- Markets registered, stalls allocated, rent paid to the Council today, incident alerts today and people on waiting lists
- Table of every market with its manager, assistant, allocation rate, rent due, daily collections and security status
- Latest alerts from all markets
- Registration form for new markets: name, location, number of stalls, enclosed shops, toilets, showers, manager, assistant and security status
- Emergency contact directory and alert dispatch log
- Council logo upload

### Market manager dashboard
- Colour-coded stall map: green for rent paid, orange for rent due, grey for vacant
- Stall types: **Open stall** and **Shop**
- Trader profile for each stall: photo, name, age, national ID (NRC) and verification status, phone, mobile network, mobile money number, items sold and rent status
- **One person per stall**: an NRC number can hold only one stall in a market
- **Change ownership** with a reason and a dated ownership history
- **Applications and waiting list**: applicants are queued in order of application and **allocated automatically** when the stall type (or specific stall) they applied for becomes available
- Daily incident reporting with type and severity
- Security status updates

### Rent payments and QR codes
- Pay rent **daily, monthly or yearly**, for one or several periods ahead (up to 365 days, 12 months or 3 years)
- Live preview of the amount and the date the stall is covered until
- A QR code for every stall linking the stall, the trader and the payment
- Sample rates (to be replaced with the official tariff):

| Stall type | Daily | Monthly | Yearly |
|---|---|---|---|
| Open stall | K10 | K200 | K2,200 |
| Shop | K25 | K500 | K5,500 |

### Incident alerts to emergency services
Alerts are routed by severity and incident type:

| Severity | Who is notified |
|---|---|
| Low | Council control room |
| Medium | Council plus the matching service (Fire, Police, or Ambulance and Hospital) |
| High | Council plus every listed emergency contact |

Each recipient gets ready-to-send SMS and email buttons. Contacts in the prototype are samples and can be edited in the Council dashboard.

### Online market
- Marketeers list the day's items with a **photo**, price, unit and **available quantity**; stock reduces with every purchase
- **Fast selling** tags and **Bargains of the day** (normal price versus selling price), each with its own filter
- Buyers pay by Airtel Money, MTN MoMo, Zamtel Kwacha or Visa debit card
- **Delivery tracking** with the assigned transport, driver, stage, a moving route icon and an expected arrival time
- **Ratings** for sellers and transporters, shown as a star average and the percentage of satisfied customers
- Delivery agents and coordinators can be registered with their transport: **Vehicle, Motorbike, 3-wheeler or Bicycle**

## Getting started

1. Download `index.html` from this repository.
2. Open it in a browser.
3. Use the three tabs at the top: **Council dashboard**, **Market manager** and **Online market**.

### Publish with GitHub Pages
1. Open **Settings**, then **Pages**.
2. Under **Branch**, choose `main` and the root folder, then **Save**.
3. The site goes live at `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

## How data is stored

The prototype keeps its data in each person's own browser (local storage), which makes it ideal for demonstrations and testing. To reset the sample data, clear the site data in your browser.

## Roadmap to a live system

| Area | Planned step |
|---|---|
| Shared records | Central database so Council officers and managers see the same live data |
| Access | Secure logins and roles for Council officers, market managers, marketeers and buyers |
| Payments | Gateway integration for Airtel Money, MTN MoMo, Zamtel Kwacha and Visa, with automatic reconciliation to stall QR codes |
| Alerts | SMS and email gateway for fully automatic dispatch to emergency services |
| Tracking | Live GPS feed from delivery vehicles, motorbikes and 3-wheelers |
| Verification | NRC verification against official records |
| Notifications | SMS to applicants when a waiting-list allocation is made, and rent reminders to traders |

## Technology

- Plain HTML, CSS and JavaScript in one file
- [qrcodejs](https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js) for stall QR codes
- Light and dark colour themes, responsive for phones, tablets and desktops

## Project status

Prototype for demonstration and requirements validation. All names, numbers, rates and contacts shown are sample data.

## Licence

To be confirmed by the Lusaka City Council.
