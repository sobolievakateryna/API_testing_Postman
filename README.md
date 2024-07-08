# API_testing_Postman

This project aimed to show skills in testing API and working with Postman as a QA Engineer. 

I used free API documentation available at https://dummyapi.io to test an application simulating the functioning of a social network. It allows users to create profiles, make posts, and leave comments.

### Okay, let's get started. 

First, I created a new collection and set up an environment named "QA."

Then I made a set of requests. You can see a flow here:

![Collection](images/collection.png)

You can use variables in Postman to store and access values in different API requests without manual input. 

Let's look at the variables:

![variables](images/variables.png)

And how I’ve created them:

![email,userId](images/set_email_userid.png)
![postId](images/set_postid.png)
![postId2](images/set_postid2.png)
![commentId](images/set_commentid.png)


Let’s look at the request “Create Post” where we can see:
- body of the request;
- using the variable {{userId}} instead of manually writing an IP address;
- status code 200.
  
![Create Post](images/create_post.png)


For User creation, we have required firstName, lastName, and email fields. In the future, when running tests, we will have to change the email data manually for each new test iteration. To minimize manual work, I have set a {{$randomEmail}} so that Postman can generate random email values (also I’ve set {{$randomFirstName}} ).

![Randoms](images/randoms.png)

Some tests:
1.	Test checks the status code (here it should be 200 for passing)
2.	Test checks the body (here it should match string)
3.	Test checks the digits in FirstName field 
4.	Test checks the symbols in FirstName field

![Tests](images/tests.png)

And response:

![Response](images/test_response.png)


Let’s run a collection: 

![Run a collection](images/run_the_collection.png)

And I’ve made a test report using Newman:

![Newman report](images/Newman_report.png)
