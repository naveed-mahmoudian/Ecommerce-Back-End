# E-Commerce Back End

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Description

This application is a a backend server for an e-commerce website using Node.js, Express.js, and Sequelize with MySQL.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Credits](#credits)
- [Questions](#questions)

## Installation

[Click Here for GitHub Repo](https://github.com/naveed-mahmoudian/Ecommerce-Back-End)

To install, please ensure you have `node.js` installed on your computer. Then clone the github repo and run `npm i` to install all dependencies.

IMPORTANT: Be sure to create a `.env` file in the main directory with the following contents:

```
DB_NAME='ecommerce_db'
DB_USER='<your mysql username>'
DB_PW='<your mysql password>'
```

This is crucial or else the connection in `config/connection.js` will throw an error and you will not be able to connect the database.

To build and seed the database run the following commands in your terminal:

- Enter the MySQL shell:

```
mysql -u root -p
Enter your password...
```

- Destroy and rebuild the `ecommerce_db` database:

```
source db/schema.sql;
```

- To seed the database, exit the mysql shell and run the following in your terminal:

```
npm run seed
```

Now you can make requests to various endpoints of the application.

## Usage

To make requests to the various endpoints you can use an API client like Insomnia, Postman, etc.

[Click Here for Walkthrough Video](https://app.castify.com/view/ab71c7d6-814c-4651-82e7-2954868af555)

Default Endpoint: `http://localhost:3001/api`

- Product Example Requests:

  - GET all Products

    `GET: /products`

  - GET 1 Product

    `GET: /products/{id}`

  - CREATE a Product

    `POST: /products`

    ```
    body: {
        "product_name": "Football",
        "price": 20.00,
        "stock": 3,
        "tagIds": [1, 2, 3, 4]
    }
    ```

  - UPDATE a Product

    `PUT: /products/{id}`

    ```
    body: {
        "product_name": "Football",
        "price": 30.00,
        "stock": 5,
        "tagIds": [1, 2, 3, 4]
    }
    ```

  - DELETE a Product

    `DELETE: /products/{id}`

- Category Example Requests:

  - GET all Categories

    `GET: /categories`

  - GET 1 Category

    `GET: /categories/{id}`

  - CREATE a Category

    `POST: /categories`

    ```
    body: {
        "category_name": "Outdoors"
    }
    ```

  - UPDATE a Category

    `PUT: /categories/{id}`

    ```
    body: {
        "category_name": "Indoors"
    }
    ```

  - DELETE a Category

    `DELETE: /categories/{id}`

- Tag Example Requests:

  - GET all Tags

    `GET: /tags`

  - GET 1 Tag

    `GET: /tags/{id}`

  - CREATE a Tag

    `POST: /tags`

    ```
    body: {
        tag_name: "Clearance"
    }
    ```

  - UPDATE a Tag

    `PUT: /tags/{id}`

    ```
    body: {
        tag_name: "Sale"
    }
    ```

  - DELETE a Tag

    `DELETE: /tags/{id}`

## License

MIT License

      Copyright (c) 2022 Naveed Mahmoudian

      Permission is hereby granted, free of charge, to any person obtaining a copy
      of this software and associated documentation files (the "Software"), to deal
      in the Software without restriction, including without limitation the rights
      to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
      copies of the Software, and to permit persons to whom the Software is
      furnished to do so, subject to the following conditions:

      The above copyright notice and this permission notice shall be included in all
      copies or substantial portions of the Software.

      THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
      IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
      FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
      AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
      LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
      OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
      SOFTWARE.

## Credits

This application was created by Naveed Mahmoudian

## Questions

GitHub: [naveed-mahmoudian](https://www.github.com/naveed-mahmoudian/)

Email: nmahmoudian@gmail.com
