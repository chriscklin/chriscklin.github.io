---
layout: post
title: "Microblog (Flask, Bootstrap, Jinja, Javascript)"
date: 2023-07-27 10:25:45 -0400
categories: jekyll update
---

[Git Repo](https://github.com/chriscklin/microblog)<br>
This is my first Flask project. It's a microblog site build with flask, bootstrap, jinja and javascript.

Upon entering the site, the user will be redirected to the Login's page. If the user doesn't have an account, clicking the 'Sign Up' button in the navigation bar.
![Login Page](/screenshots/microblog/login_page_empty.png)

This is the Sign Up page. The form checks if the email or username exists, if the password is at least 8 characters, and if the passwords match upon submission. An error message will flash if any of the criteria fail.
![Sign Up Page](/screenshots/microblog/sign_up_page_empty.png)
<br><br>
![Sign Up Page Error](/screenshots/microblog/sign_up_page_error.png)

Once a new user has been successfully created, the user is automatically logged in and redirected to the Home page where all posts are displayed in reverse chronological order. Once logged in, the navigation bar changes to having 'Home'and 'Logout' options and user's username is displayed on the far right. From the Home page, there are several options. Users can:

- Add a new post using the 'Create a Post' button
- View all posts from a user by clicking any username
- Like a post by clicking the thumbs up icon
- View comments by clicking 'View <#> Comments'
- Leave a comment

![Home Page New User](/screenshots/microblog/new_user_created_home.png)

This is the 'Make a Post' page. Simply enter text in the text post and click post. After the post is created, the user will be redirected back to the Home page.

![Make a Post](/screenshots/microblog/make_a_post_page.png)

When a user name is clicked, all the posts for that user are displayed in reverse chronological order.

![User's Post](/screenshots/microblog/user_post_view.png)

User's have the option to delete their own posts, their own comments, and comments on their post.

![Delete Post](/screenshots/microblog/delete_post.png)
