This is repo contains a automation script to automate [https://www.douglas.com/de/de ]


# Playwright Automation – Douglas.de (Perfume Filters)

## Project Overview

This project contains **Playwright automation scripts written in TypeScript** for testing the **Douglas.de** website, a cosmetic and fashion e-commerce platform offering **luxury perfumes and beauty products**.

The automation focuses on **validating product listing behavior after applying filters** in the **Perfume (Parfum)** section. The goal is to ensure that **all product cards load correctly** after each filter is applied.

---

## Test Scenario Description

The automated test covers the following steps:

1. Navigate to **[https://www.douglas.de/de](https://www.douglas.de/de)**
2. Handle the **cookie consent pop-up**
3. Hover over the **"Parfum"** category in the main navigation
4. Select and apply the following filters:

   * **Sale**
   * **Neu**
5. After applying each filter:

   * Verify that the **filtered product list is displayed**
   * Ensure that **all product cards are loaded successfully**
   * Validate that no empty or partially loaded results are shown

The tests are implemented as **data-driven tests**, allowing the same validation logic to run for multiple filter values.

---

## Filters Covered

The following filter categories are validated:

* **Criteria (Highlights)**: Sale, Neu
* **Marke**
* **Produktart**
* **Geschenk für**
* **Für Wen**

Each filter is applied individually to ensure correct product rendering.

---

## Tech Stack

* **Automation Tool**: Playwright
* **Language**: TypeScript
* **Test Design**: Data-driven testing
* **Browser Support**: Chromium, Firefox, WebKit
* **Wait Strategy**: Explicit waits to ensure all product cards load after filter application

---

## Project Setup

### Prerequisites

* Node.js (LTS version recommended)
* npm (comes with Node.js)

### Install Node Modules

```bash
npm install
```

### Install Playwright (Latest Version)

```bash
npm install playwright@latest
```

### Install Browsers

```bash
npx playwright install
```

---

## Running the Tests

Run all Playwright tests:

```bash
npx playwright test
```

Run tests in headed mode:

```bash
npx playwright test --headed
```

Run tests with Playwright UI:

```bash
npx playwright test --ui
```

---

## Test Design Approach

* **Hover actions** are used to access the *Parfum* menu.
* **Reusable methods** are created for applying filters.
* **Data-driven testing** is implemented to validate multiple filter options.
* Explicit assertions ensure:

  * Product cards are visible
  * Product count is greater than zero
  * Page updates correctly after each filter selection

