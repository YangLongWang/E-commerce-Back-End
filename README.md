# E-commerce-Back-End

## Table of Contents 

<details>
<summary>Table of Contents</summary>

- [Overview](#overview)
  - [Description](#description)
  - [Installation](#installation)
  - [Usage](#usage)
  - [The challenge](#the-challenge)
  - [Video](#video)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

</details>

## Overview

### Description

A back end for an e-commerce website that uses the latest technologies so that it can compete with other e-commerce companies.


### Installation

Because this is a back end application that runs from a machine and not a browser, it can't be deployed to GitHub pages. If anyone ever wants to look at the application, you have to clone it to your own local machine and run it from there.


### Usage

Create a .env file in root directory, and enter your own DB_NAME, DB_USER, and DB_PW. After that running npm run seed in terminal, and the application will be invoked by using the following command: node server.js. Using Insomnia to check results.

### The challenge

Users should be able to:

- check the CRUD operation of the products, tags, and categories

### Video

- Video link(Categories): [https://drive.google.com/file/d/1SRKfPGSTyXIOD7u9TAOq6n4Q0OYZqvPr/view](https://drive.google.com/file/d/1SRKfPGSTyXIOD7u9TAOq6n4Q0OYZqvPr/view)

- Video link(Products): [https://drive.google.com/file/d/1kBmeYQhkGBXDsX9WjW2MCpSEUM3yVGYT/view](https://drive.google.com/file/d/1kBmeYQhkGBXDsX9WjW2MCpSEUM3yVGYT/view)

- Video link(Tags): [https://drive.google.com/file/d/1Z7tgF0pyTxKz9MfJYeyl4ab_i8UJunNr/view](https://drive.google.com/file/d/1Z7tgF0pyTxKz9MfJYeyl4ab_i8UJunNr/view)

### Links

- Solution URL: [https://github.com/YangLongWang/E-commerce-Back-End](https://github.com/YangLongWang/E-commerce-Back-End)

## My process

### Built with

- JavaScript

### What I learned

- create one to one, one to many, and many to many associations

To see how I add code snippets, see below:

```JS
Product.belongsTo(Category, {
  foreignKey: 'category_id',
});

Category.hasMany(Product, {
  foreignKey: 'category_id'
});

Product.belongsToMany(Tag, {
  through: ProductTag,
  foreignKey: 'product_id',
  onDelete: 'cascade'
});

Tag.belongsToMany(Product, {
  through: ProductTag,
  foreignKey: 'tag_id',
  onDelete: 'cascade'
});
```

## Author

- Github - [Longyang Wang](https://github.com/YangLongWang)
