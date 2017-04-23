# Interview-Practice-udacity
Project 7 Udacity Project: This file only contains my answers to the interview questions that were listed for this assignment.

## What is the most influential book or blog post you’ve read regarding web development?
The most influential book that I read and helped me out alot when I first started to learn how to do web development was "Head First: PHP & MYSQL". I bought this book back in 2012 a month before I turned 19 after watching 'The Social Network' where it inspired me to make web sites. Head First was a little outdated as it showed mysqli syntax while pdo was considered best practice. At the time I didn't know that however using mysqli taught me alot by showing me the very basic fundamentals on how a website is made and how it is powered by code. After, recreating many of the projects in the book. I absolutely loved how programming can be such a fun tool to use, get and retrieve information from around the world. 

## Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?
When I first started to learn how to code a few years back I mainly worked with the LAMP stack. The reason why I decided to work with the LAMP stack was because that's what Facebook was originally built on along with other applications such as Wordpress. So, the code was heavily tested upon and seemed reliable at the time. During this time my main and only web app that I worked extensively on was this site called Portalhut. It was a job searching site that incorporated google maps to display jobs that were near the users area. It also simplified the job searching process by having your profile as your resume filled with all of the relevent information that an employer would need. I chose to build this web application because filling out job forms was a very repetitive and tedious task that took up so much time doing the same thing over and over again. I knew there was a better way of doing this so I set out to work on it as my first project. I was in over my head when I started working on this because I absolutely did not know where to start but I just looked at other big sites and from there I gathered a list of features that I needed to implement like login/signup,forgot password, upload profile picture and so on.

At the time I also didn't know that there were these things called frameworks which would've helped me out drastically but by doing vanilla code it taught me how the foundation is built and the types of problems you would expect to see. There were many challenges and obstacles that I had to endure like implementing the upload picture feature and connecting mysqli to the google maps api making sure the data and markers loaded on the map. The way I went about with these problems is by doing lots of research on google and reading code from other users that have had similar issues. I couldn't find the right code to solve my problems but after doing considerable brainstorming I managed to create the code myself solving my specific issues. Everytime I faced my challenges and successfuly solved it I was enthusiastically relieved and just felt really accomplished because I solved it on my own without having someone guide me.

## Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?

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

1. XSS - XSS stands for cross site scripting which basically is when javascript code gets run when the page loads. For example, when the sites creators forget to sanitize one of their input fields it allows an attacker to insert their own code and run it as if it were part of the site collecting users sensitive information like credit card numbers etc. You can prevent this attack by sanitizing all users input so all html tags or javascript would be escaped looking something like this: `&lt;script&gt;`

2. SQL Injections - SQL Injections are very similar to XSS but this vulnerability affects the sites database. Normally a user would put in their information onto the input field but an attacker would run a command like: `SELECT * FROM Users; DROP TABLE Suppliers` To delete a table from the database which can drastically delay the company from operational use losing clients and their credibility. The way you prevent this attack from happening is by santizing user input. It is sort of like implementing the solution to xss but there are various ways of implementing this. It depends on the language that you are using but using prepared statements is one of the best ways because it allows the database to distinguish input from code and data. It will look into the database and try to find the following values 'Tom' or '1=1' thus mitigating the attack because the procedure is followed differently from old traditional ways of doing sql queries.

## Here is some starter code for a Flask Web Application. Expand on that and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.

```
  from flask import Flask
  app = Flask(__name__)

  from flask import jsonify
  import random

  @app.route('/')
  def hello_world():
   return 'Hello World!'
   
  @app.route('/dice/json')
  def dice():
    total = 0
    # Creates two instances of a dice
    for i in range(2):
        # Randomly selects a number between 1 through 6 and inserts both values into the total variable ex. (3+4=7)
        total += random.randint(1, 6)
    # Returns the value in json format
    return jsonify({'Roll of 2 dices:': total})
    
  if __name__ == '__main__':
    app.debug = True
    app.run()
```
The dice function creates 2 instances of a dice and for each dice the total variable randomly selects a number between 1 through 6 and inserts both values into the total variable. Lastly the function returns the value in json format using jsonify.

## If you were to start your full-stack developer position today, what would be your goals a year from now?
Their are many things I would like to accomplish one year from now but at the top of my list one that will make me a better programmer is mastering full stack javascript. Why Javascript? It is the forefront of the web industry as it has been around since the inception of the modern internet and it's only getting bigger and better as everything is completely accessible with javascript. Frontend and backend for websites, internet of things, robotics etc. The way that I will be preparing myself is by taking free online courses that are catered to full stack javascript development like Free Code Camp. I also will try to help other peoples issues with Javascript as the best way to learn is to just code and create things. Another aspect of web development that I want to get better on is web design. Ever since Steve Jobs introduced the iphone the world has been keen on design and with all of the other projects that followed from Apple like the iMac and Macbook Pro it's just something that a company needs. An elegant design whether it's software or hardware based it needs to look attractive to attract customers. The way that I will approach this is by taking hands on classes whether at a university or a coding bootcamp located in Chicago.

## Resources Used
1. http://stackoverflow.com/questions/33069476/simulating-rolling-2-dice-in-python
2. https://www.toptal.com/security/10-most-common-web-security-vulnerabilities
