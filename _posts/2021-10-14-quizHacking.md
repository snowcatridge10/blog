# Hacking quizzes

Example: Bob is playing a quiz game at example.com. He installs an extension to make him get all the answers right. How?

The extension is getting the game ID and then getting the question ID. Then it is accessing api.example.com/gameID/questionID

Example: api.example.com/456295/3

Then it gets this content

{

  possibleAnswers {
  
    1 : true
    2 : false
    3 : false
    4 : false
  
  }

}

It parses it

CorrectAnswer = 1

Then it gets all the game divs

getElementById("possibleAnswer1")
getElementById("possibleAnswer2")
getElementById("possibleAnswer3")
getElementById("possibleAnswer4")

It styles the correct answer 

getElementById("possibleAnswer1").style.border = "3px solid green"


# How do we stop that from happening

## Option 1

We switch from an API to a database

## Option 2

We make it so only we can access the API
