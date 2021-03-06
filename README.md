# My Bookshelf App
___

## Table of Contents
* [Overview](#overview)
* [Installation](#installation)
* [File Tree](#file-tree)
* [Backend](#backend-server)
* [Miscellaneous](#important)

## Overview
This is a book organizing app. The main page shows three e-bookshelves('Read', Currently Reading', 'Want to Read') where you can organize your books according to the user selected status. You can also search for a book in the Search Page and then add it to one of the bookshelves. I was provided the starter code and stylesheet and was tasked to make it functional using the React Library. This project passed a code review by a Udacity reviewer.

## Installation

To get started:

* install all project dependencies with `npm install`
* start the development server with `npm start`

## File Tree
```bash
├── CONTRIBUTING.md
├── README.md - This file.
├── SEARCH_TERMS.md # The whitelisted short collection of available search terms for you to use with your app.
├── package.json # npm package manager file. It's unlikely that you'll need to modify this.
├── public
│   ├── favicon.ico # React Icon
│   └── index.html # DO NOT MODIFY
└── src
    ├── App.css # Styles
    ├── App.js # This is the root of the app.
    ├── Main.js # This is the homepage.
    ├── Bookshelf.js # This is the component that renders the different bookshelves.
    ├── SearchPage.js # This is the search page where the search input field and search results are displayed.
    ├── SearchField.js # This file handles the search field component.
    ├── Book.js # This is the file for the component that handels each book.
    ├── App.test.js # Used for testing. Provided with Create React App. Testing is encouraged, but not required.
    ├── BooksAPI.js # A JavaScript API for the provided Udacity backend. Instructions for the methods are below.
    ├── icons # Helpful images for your app. Use at your discretion.
    │   ├── add.svg
    │   ├── arrow-back.svg
    │   └── arrow-drop-down.svg
    ├── index.css # Global styles. You probably won't need to change anything here.
    └── index.js # You should not need to modify this file. It is used for DOM rendering only.
```

## Backend Server

Udacity provided a backend server to develop against. The provided file [`BooksAPI.js`](src/BooksAPI.js) contains the methods that were needed to perform necessary operations on the backend:

* [`getAll`](#getall)
* [`update`](#update)
* [`search`](#search)

### `getAll`

Method Signature:

```js
getAll()
```

* Returns a Promise which resolves to a JSON object containing a collection of book objects.
* This collection represents the books currently in the bookshelves in your app.

### `update`

Method Signature:

```js
update(book, shelf)
```

* book: `<Object>` containing at minimum an `id` attribute
* shelf: `<String>` contains one of ["wantToRead", "currentlyReading", "read"]
* Returns a Promise which resolves to a JSON object containing the response data of the POST request

### `search`

Method Signature:

```js
search(query)
```

* query: `<String>`
* Returns a Promise which resolves to a JSON object containing a collection of a maximum of 20 book objects.
* These books do not know which shelf they are on. They are raw results only. You'll need to make sure that books have the correct state while on the search page.

## Important
The backend API uses a fixed set of cached search results and is limited to a particular set of search terms, which can be found in [SEARCH_TERMS.md](SEARCH_TERMS.md). That list of terms are the _only_ terms that will work with the backend, so don't be surprised if your searches for Basket Weaving or Bubble Wrap don't come back with any results.

## Create React App

This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).

## Contributing

Udacity provided the starter code.
For details, check out [CONTRIBUTING.md](CONTRIBUTING.md).
