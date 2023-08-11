---
layout: post
title: "Library Backend (Go, MongoDB)"
date: 2023-08-08 10:25:45 -0400
categories: jekyll update
---

[Git Repo](https://github.com/chriscklin/library_backend)<br>
This is my first Go project. It's a backend system for a library using Go and MongoDB. In practice, this type of system would work better with a relational database; however, I chose MongoDB because I wanted to learn how to use Go with MongoDB. I'll be showing the functionality using Postman. My database consists of multiple copies of 10 unqiue books. The system allows for the following endpoints:

![All Endpoints](/screenshots/library_backend/all_endpoints.png)

The next three endpoints are used to get all books, checked out books, and overdue books:

<img src="/screenshots/library_backend/get_all_books.png" alt="Get All Books" style="border: 2px solid  gray; margin-bottom: 10px">
<img src="/screenshots/library_backend/get_checked_out_books.png" alt="Get Checked Out Books" style="border: 2px solid  gray; margin-bottom: 10px">
<img src="/screenshots/library_backend/get_overdue_books.png" alt="Get Overdue Books" style="border: 2px solid  gray; margin-bottom: 10px">

Books and users can be retreived by ID:

<style>
* {
  box-sizing: border-box;
}

.column {
  float: left;
  width: 50%;
  padding: 5px;
}

/* Clearfix (clear floats) */
.row::after {
  content: "";
  clear: both;
  display: table;
}
</style>
<div class="row">
  <div class="column">
    <img src="/screenshots/library_backend/get_book_id.png" alt="Get Book by ID" style="width:100%; border: 2px solid  gray">
  </div>
  <div class="column">
    <img src="/screenshots/library_backend/get_user_id.png" alt="Get Users by ID" style="width:100%; border: 2px solid  gray">
  </div>
</div>

Here are the login and logout function for users. Logout endpoint requires user to be logged in to use:

<img src="/screenshots/library_backend/login.png" alt="Login" style="border: 2px solid  gray;">
<div class="row">
  <div class="column">
    <img src="/screenshots/library_backend/logout_successful.png" alt="Logout" style="width:100%; border: 2px solid  gray">
  </div>
  <div class="column">
    <img src="/screenshots/library_backend/logout_unauthorized.png" alt="Logout Unauthorized" style="width:100%; border: 2px solid  gray">
  </div>
</div>

This is the book checkout endpoint. Books are checked out by id in the body and returns the book and user checked out. If the book has already been checked out, it will return an expected return date:

<img src="/screenshots/library_backend/checkout_book.png" alt="Checkout Book" style="border: 2px solid  gray; margin-bottom: 10px">
<img src="/screenshots/library_backend/checkout_book_unavailable.png" alt="Checkout Book Unavailable" style="border: 2px solid  gray; margin-bottom: 10px">

This is the book check in endpoint. It will check if the book has been checked out.

<div class="row">
  <div class="column">
    <img src="/screenshots/library_backend/checkin_book.png" alt="Checkin Book" style="width:100%; border: 2px solid  gray">
  </div>
  <div class="column">
    <img src="/screenshots/library_backend/checkin_book_no_need.png" alt="Checkin Book No Need" style="width:100%; border: 2px solid  gray">
  </div>
</div>

The final four endpoints are three POSTs  and a DELETE. These endpoints require Basic Auth to use. These endpoints are used to register a user, delete user, and add a book (or books) to the library.

<div class="row">
  <div class="column">
    <img src="/screenshots/library_backend/create_new_user.png" alt="Register New User" style="width:100%; border: 2px solid  gray">
  </div>
  <div class="column">
    <img src="/screenshots/library_backend/delete_user.png" alt="Delete User" style="width:100%; border: 2px solid  gray">
  </div>
</div>
<div class="row">
  <div class="column">
    <img src="/screenshots/library_backend/add_new_book.png" alt="Add New Book" style="width:100%; border: 2px solid  gray">
  </div>
  <div class="column">
    <img src="/screenshots/library_backend/add_books.png" alt="Add New Books" style="width:100%; border: 2px solid  gray">
  </div>
</div>
