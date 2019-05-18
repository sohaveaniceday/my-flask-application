# Games Science Technical Test (Back End/Python)

## Instructions for Use

#### Post Request

In terminal:

```
curl -H "Content-Type: application/json" -X POST https://unevo7lf61.execute-api.us-east-1.amazonaws.com/dev/users -d '{"userId": "user1", "name": "James Bond"}'
```

#### Get Request

In terminal:

```
curl -H "Content-Type: application/json" -X GET https://unevo7lf61.execute-api.us-east-1.amazonaws.com/dev/users/user1
```

## Approach Walk-through

* Whilst I had built Flask apps using SQL and Heroku deployment, I had never used AWS Lambda before, so I took it upon my self to research the platform before starting the task. 

* I watched the below YouTube video, which gave a good overview of the platform, as well as looking at the official AWS documents.

    * https://www.youtube.com/watch?v=97q30JjEq9Y

    * https://aws.amazon.com/lambda/

* After this, I decided to create an initial AWS Lambda function using the below tutorial. This taught me how to create my function through the official portal, create an Amazon AWS Lambda Zip file using Make, create a virtual environment, plus edit and test the functions.

    * https://www.youtube.com/watch?v=hzlxWBs1Qt4 

    * GitHub Repo: https://github.com/sohaveaniceday/lambda-test

* I then proceeded with the task by creating my Flask App in a similar approach to some of my previous projects. Whilst I was able to deploy the app (thanks to Zappa) and achieve 'Hello World' from a basic Lambda function, I quickly realised that I was struggling to implement SQL as the main database in order to make my get/post requests.

    * GitHub Repo: https://github.com/sohaveaniceday/flask-app 

* Having done some research online, I found the best way of implement a database on AWS Lambda was through DynamoDB, Amazon's own NoSQL database service. With the the accumulated knowledge I had obtained and the below tutorial which incorporated DynamoDB, I started the task from scratch and proceeded in this direction.

    * https://serverless.com/blog/flask-python-rest-api-serverless-lambda-dynamodb/

* I was able to achieve 'Hello World' from a basic Lambda function very quickly. I also found the implementation of DynamoDB extremely painless, showing me the best systems to use are often the ones that work synchronously together. Once I had achieved a successful POST and GET request, I was happy that I had achieved the task's objective.

## Further Improvements & Key Learnings

If I had more time with the task I would definitely add elements like error handling, authentication, and path-specific routing. These are the cornerstone for any REST API and vital for any fully-fledged apps.

I learnt a huge amount doing this task. I didn't realise it was possible to deploy and use AWS functionality all from the terminal, for instance. The biggest learning, however, was when approaching a task with a lot of unknown components it's best to start with the base fundamentals before jumping straight into a task. I found challenges a lot easier once I had built up my knowledge and was able to tackle them with hard-earned logic. A programmer should also not be afraid to start again if they find themselves reaching a dead end with a particualar piece of technology.


## Brief

### Approach

You should treat this test as much about solving problems as the code you should write. You should spend no more than a half-day on the test, but should document resources you use, searches you do to find answers and should commit as you go along in GitHub or a similar source management product, to show your working process.

### Task

Games Science wishes to create a new API for a new feature of our product. We use Flask for the majority of our back end services, hosted on AWS using AWS Lambda as serverless compute. Please create a simple Flask application (or similar in Python) running on AWS Lambda which takes a JSON body input via an HTTP POST method (using the correct headers for accepting a JSON body). This application should persist its data to AWS S3. Please also provide code for a GET method which retrieves the data from S3.
