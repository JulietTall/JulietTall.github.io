---
layout: post
title:  "Different Strategies, Same Solution"
date:   2017-08-27 15:15:50 -0400
---


In the education field, there is a curriculum called *Cognitively Guided Instruction*. This curriculum is typically [implemented](http://http://minds-in-bloom.com/implement-cognitively-guided-instruction-classroom/) through the teacher presenting a word problem to the class. The students are not given any guidelines to solve the problem. While the students are using their independent strategies to find a solution, the teacher will observe how different students arrive at their answer. After all students arrive at a solution, the whole class will reconvene. The teacher will select students to present their strategies to the whole class. This way, students are able to discover different strategies to solve a problem.

While working through my Full Stack Web Development course, I have been trying to implement this teaching practice on myself as a way to reflect on my completed labs. After I finish a lab, I like to select a few of my peers' pull requests on GitHub. Unfortunately, since we are not altogether in a classroom, I've been trying to present and describe their strategies to myself on their behalf. I also like to evaluate different strategies - whether the code is simple, eloquent, and nonrepetitive.

In one lab, we were asked to build a simplified version of the display_board method in which:
1. Each cell is presented by a string with 3 spaces:"   "
2. Each row has 3 cells, the middle separated by 2 | (pipe) characters:   |   |    
3. There are 3 rows, with 2 separating lines of 11 - (dash) characters: -----------

This is the method I built:
```
def display_board
puts "   |   |   "
puts "-----------"
puts "   |   |   "
puts "-----------"
puts "   |   |   "
end
```
I think this method is pretty simple and straightforward - Ruby executes each string to output each row of the Tic Tac Toe board. However, I wonder if there is a way I could have made the method less repetitive.

Here is a method built by Peer A:
```
def display_board
  row_1 = ["   ","   ","   "]
  row_2 = ["   ","   ","   "]
  row_3 = ["   ","   ","   "]
  border = ["-----------"]

  print row_1[0]
  print "|"
  print row_1[1]
  print "|"
  puts row_1[2]
  puts border

  print row_2[0]
  print "|"
  print row_2[1]
  print "|"
  puts row_2[2]
  puts border

  print row_3[0]
  print "|"
  print row_3[1]
  print "|"
  puts row_3[2]
end

display_board()
```

In this method, Peer A defined the rows and cells as arrays. When Ruby executes this method, it prints items from the different arrays. Even though this method passed tests and produced the same results, this strategy isn't very simple and is quite repetitive.

Here is a method built by Peer B:

```
def display_board
  puts "   " '|' "   " '|' "   "
  puts "-----------"
  puts "   " '|' "   " '|' "   "
  puts "-----------"
  puts "   " '|' "   " '|' "   "
 end
```

This method built by Peer B is very similar to the method I came up with. Even though this method passed and produced the same results, I think eliminating the ' ' around the |'s would make this code more simple.
 
 Here is a method built by Peer C:
```
 def display_board
  cells = "   |   |   "
  lines = "-----------"
  puts cells
  puts lines
  puts cells
  puts lines
  puts cells
end
```

In this method, Peer C defined two variables. Cells are defined as a string of "   |   |   " and lines are defined as a string of "-----------". When Ruby executes this method, it evaluates and outputs the variables. While this method may not be as simple, I think this one is really cool. Peer C found a way to avoid entering "   |   |   "  and "-----------" multiple times - which has the potential to create typos and causes errors. It's easier to accurately type "puts cells" and "puts lines."

It's so amazing that there are so many different strategies to arrive at the same solution. I hope to continue to merge my two passions for education and web development by using Cognitively Guided Instruction both in the classroom as an early childhood educator and behind the screen as a student.
