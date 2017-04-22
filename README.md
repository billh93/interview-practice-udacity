# interview-practice-udacity
Project 7 Udacity Project: This file only contains my answers to the interview questions that were listed for this assignment.

## What is the most influential book or blog post you’ve read regarding web development?
The most influential book that I read and helped me out alot when I first started to learn how to do web development was "Head First: PHP & MYSQL". I bought this book back in 2012 a month before I turned 19 after watching 'The Social Network' where it inspired me to make web sites. Head First was a little outdated as it showed mysqli syntax while pdo was considered best practice. At the time I didn't know that however using mysqli taught me alot by showing me the very basic fundamentals on how a website is made and how it is powered by code. After, recreating many of the projects in the book. I absolutely loved how programming can be such a fun tool to use, get and retrieve information from around the world.

## Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?
When I first started to learn how to code a few years back I mainly worked with the LAMP stack. My main and only web app that I worked extensively on was this site called Portalhut. It was a job searching site that incorporated google maps to display jobs that were near the users area. It also simplified the job searching process by having your profile as your resume filled with all of the relevent information that an employer would need. I chose to build this web application because filling out job forms was a very repetitive and tedious task that took up so much time doing the same thing over and over again. I knew there was a better way of doing this so I set out to work on it as my first project. I was in over my head when I started working on this because I absolutely did not know where to start but I just looked at other big sites and from there I gathered a list of features that I needed to implement like login/signup,forgot password, upload profile picture and so on. At the time I also didn't know that there were these things called frameworks which would've helped me out drastically but by doing vanilla code it taught me how the foundation is built and the types of problems you would expect to see. There were many challenges and obstacles that I had to endure like implementing the upload picture feature and connecting mysqli to the google maps api making sure the data and markers loaded on the map. The way I went about with these problems is by doing lots of research on google and reading code from other users that have had similar issues. I couldn't find the right code to solve my problems but after doing considerable brainstorming I managed to create the code myself solving my specific issues. Everytime I faced my challenges and successfuly solved it I was enthusiastically relieved and just felt really accomplished because I solved it on my own without having someone guide me.

## Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list (<ul>...</ul>) of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?

```
  def disp_str(list):
    string = "<ul>\n"
    # Goes through each item in the list
    for s in list:
    # Appends each item inside the unordered list 
      string += "<li>" + str(s) +"</li>\n"
    string += "</ul>"
    # Returns the final string 
    return string
    
  # Static variable  
  food = ['chicken','cheeseburger','sandwich','pizza']
  # Prints out the function output
  print(disp_str(food))
```
If the list is provided by user input I would insert in an if statement to check to see if it is indeed a list and if the values are strings.
`if isinstance(list, basestring)` and `if isinstance(string, basestring)`

## List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks?
There are various attacks that web applications are susceptible to. The two most common ones are xss and sql injections.
1.) XSS - XSS stands for cross site scripting which basically is when javascript code gets run when the page loads. 
