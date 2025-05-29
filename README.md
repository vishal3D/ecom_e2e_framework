# ecom_e2e_framework
# E-Commerce E2E Testing Framework (Cypress)

This repository contains an automated end-to-end testing framework for an e-commerce website, built with Cypress and JavaScript.

## Features

  * **End-to-End Testing:** Provides a complete setup for writing and running e2e tests.
  * **Page Object Model (POM):** Organizes the code into a clean and maintainable structure by separating page selectors and actions from the actual test cases.
  * **Cypress Test Runner:** Leverages the interactive Cypress Test Runner for easy debugging, time-traveling through test steps, and viewing real-time execution.
  * **Cross-Browser Support:** Natively supports running tests on Chrome, Firefox, Edge, and Electron.
  * **Custom Commands:** Includes examples of reusable custom commands to simplify test writing.

## Tech Stack

  * **Framework:** [Cypress](https://www.cypress.io/)
  * **Language:** JavaScript
  * **Package Manager:** npm

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

Ensure you have the following software installed:

  * [Node.js](https://nodejs.org/) (which includes npm)

### Installation

1.  **Clone the repository**
    ```sh
    git clone https://github.com/vishal3D/ecom_e2e_framework.git
    ```
2.  **Navigate to the project directory**
    ```sh
    cd ecom_e2e_framework
    ```
3.  **Install project dependencies**
    This command will download all the required packages, including Cypress, defined in `package.json`.
    ```sh
    npm install cypress
    ```

## How to Run Tests

Cypress provides multiple ways to execute your tests.

### 1\. Interactive Test Runner (Recommended for Development)

This command opens the Cypress Test Runner GUI, which allows you to see your tests run in real-time, select specific tests to run, and easily debug.

```sh
npx cypress open
```

### 2\. Command-Line (Headless)

This command runs all tests headlessly in the terminal. This is ideal for CI/CD environments.

```sh
npx cypress run
```

### 3\. Running a Specific Test File

To run a single test file (spec), use the `--spec` flag.

```sh
npx cypress run --spec "cypress/e2e/tests/YourTestFile.cy.js"
```

## Framework Structure

The project follows the standard Cypress 10+ directory structure:

  * **`cypress/`**: The main folder containing all testing-related files.
      * **`e2e/`**: Contains the actual test files (specs).
          * `pages/`: Page Object classes that encapsulate the logic and selectors for each page.
          * `tests/`: The test spec files that use the page objects to perform user actions and assertions.
      * **`fixtures/`**: Stores static test data, such as JSON files, that can be used in your tests.
      * **`support/`**: Contains reusable custom commands and global configurations.
          * `commands.js`: The place to define custom commands (e.g., `cy.login()`).
          * `e2e.js`: This file runs before every single spec file.
  * **`cypress.config.js`**: The main configuration file for Cypress, where you can set the base URL, timeouts, and other project-specific settings.
  * **`package.json`**: Defines project dependencies, scripts, and metadata.
