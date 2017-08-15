---
layout: post
title:  "Spaces Are Important!"
date:   2017-08-15 18:16:42 -0400
---

Can you tell the difference between these strings of code? Look very closely.

```
def display_board(board)
puts " #{board[0]}  | #{board[1]} | #{board[2]} "
puts "-----------"
puts " #{board[3]} | #{board[4]} | #{board[5]} "
puts "-----------"
puts " #{board[6]} | #{board[7]} | #{board[8]} "
end
```

```
def display_board(board)
puts " #{board[0]} | #{board[1]} | #{board[2]} "
puts "-----------"
puts " #{board[3]} | #{board[4]} | #{board[5]} "
puts "-----------"
puts " #{board[6]} | #{board[7]} | #{board[8]} "
end
```

Last night, I was working through a lab in which I needed to:
1. define a method that accepts an argument.
2. use the argument within the method.
3. read data from an array.
4. print out a multi-line dynamic string using Interpolation.

After creating this string of code, it should have:
1. displayed a Tic Tac Toe board.
2. passed through the test suite.

Pretty simple, right? I already built most of this string in a previous lab:
```
def display_board
 puts "   |   |   "
 puts "-----------"
 puts "   |   |   "
 puts "-----------"
 puts "   |   |   "
 end
```
It just needed a few changes.

After playing around with the string for about an hour, proceeded by watching an hour long Youtube tutorial walking through the lab, followed by another hour of Googling for more information relating to this lab, and even self admittedly peeking through some of my peers' GitHub pull requests and self indulgently stress crying for 10 minutes, my string was still not passing through the test suite.

Why is that, you ask? Because of one little extra space I had in there! Wow.

Spaces are important. Punctuation is important. Grammar is important.

I feel slightly embarassed for myself both as an educator and as an aspiring software programmer.

Lesson learned. Noted for the future.
