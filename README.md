# serverless-node-read-restful-api-optimized-aws-lambda-mongodb
restful apis for optimizing read operations - Node.js + AWS Lambda + MongoDB - No Framework or Third part library used
AWS Lambda function :   app.zip
configure lambda handler as:   app.handler
configure environment variable for MongoDB:


Environment Variable in AWS Lambda for MONGODB_URI = "{connection string}" 

MongoDB Atlas is a great option for managed cloud mongodb cluster to start with - Free Tier is available

Environment Variable in AWS Lambda for MONGODB_DATABASE_NAME = "{db name}"

How to configure?: https://docs.aws.amazon.com/lambda/latest/dg/configuration-envvars.html"

E-Route to get the data from any collection from MongoDB Database ( Highly Dynamic)

</BR></BR>
Just upload "app.zip" to AWS Lambda directly via Lambda Code mangement console as function size is just 682.7 kB </BR>

We can use MongoDB Atlas Cloud managed solution - [Free Shared Instance](https://www.mongodb.com/blog/post/free-your-genius-on-mongodb-atlas-free-tier)
</BR></BR>
**e-Route** </BR>
Connect an API gateway with $default stage and only one route GET /{proxy+}: </BR>
Following Routes are available to access the resources from db: </BR>
[ GET ] /api/e/{entity} </BR>
[ GET ] /api/e/{entity}/{id} </BR>
</BR>
**CRUD**: Any Entity as json request can be read from the MongoDB database </BR>


</BR> **Working On** </BR>
- JWT authorization via:
  - APIGateway Authorizer for any specific route
  - Custom implementation is pretty much dynamic. Using JWT Library dependency but it may add an additional cold start time for boot up.
- </BR> CI/CD for one-click/command deploy updates to Lambda func 

</BR>Any Feedback, suggestion, improvisation is welcomed</BR>

</BR></BR>
**Created By**, </BR>
Furqan </BR>
(Software Developer / Solution Architect) </BR></BR>
