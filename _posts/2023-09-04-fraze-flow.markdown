---
layout: post
title: "In Progress...Fraze Flow (JavaScript, Postgresql, Flask, HTML, CSS)"
date: 2023-09-04 10:25:45 -0400
categories: jekyll update
---

This project is currently in progress. Inspired by Wordle and the classic gameshow Chain Reaction, Fraze Flow is a daily word game where players attempt to complete the Fraze Flow by guessing 5 words. Each word make a 2-word phrase with the row above and below it. Players can make 7 mistakes before the game considers it a loss.

This game is written using JavaScript, HTML, CSS, Boostrap, Font Awesome for the front-end. The backend is written in Python using Flask. The user data (not yet implemented) and game data is stored in Postgresql and the session data is being handled with Redis.  In general, JavaScript is responsible for creating the gameboard, handling user input, and managing current game state. The backend is handling user verification (not yet implemented) and all of the game logic (checking validity of words and win/lose conditions). Below are some screenshots of the game in action:

<div align="center">
  <img src="/screenshots/fraze_flow/Fraze_flow_how_to_play.png" alt="How To Play">
  <br>
  How to play popup screen
</div>

<br>
  
<div align="center">
  <img src="/screenshots/fraze_flow/Fraze_flow_guess.png" alt="Guessing Word">
  <br>
  Words can be typed (desktop) or entered using an on-screen keyboard
</div>

<br>

<div align="center">
  <img src="/screenshots/fraze_flow/Fraze_flow_correct_guess.png" alt="Correct Guess">
  <br>
  Correct guesses turn blue, and a new letter is revealed
</div>

<br>

<div align="center">
  <img src="/screenshots/fraze_flow/Fraze_flow_wrong_guess.png" alt="Incorrect Guess">
  <br>
  After an incorrect guess, you lose a heart, and a new letter is revealed
</div>

<br>

<div align="center">
  <img src="/screenshots/fraze_flow/Fraze_flow_victory_screen.png" alt="Victory Screen">
  <br>
  Victory screen
</div>


