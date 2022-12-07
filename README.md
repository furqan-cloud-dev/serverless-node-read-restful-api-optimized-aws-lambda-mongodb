# serverless-node-read-restful-api-optimized-aws-lambda-mongodb
restful apis for optimizing read operations - Node.js + AWS Lambda + MongoDB - No Framework or Third part library used </BR>
AWS Lambda function :   app.zip </BR>
configure lambda handler as:   app.handler. </BR>
configure environment variable for MongoDB: </BR>

Configure Environment Variable in AWS Lambda for MONGODB_URI = "{connection string}" 

MongoDB Atlas is a great option for managed cloud mongodb cluster to start with - Free Tier is available

Configure Environment Variable in AWS Lambda for MONGODB_DATABASE_NAME = "{db name}"

How to configure?: https://docs.aws.amazon.com/lambda/latest/dg/configuration-envvars.html"

E-Route to get the data from any collection from MongoDB Database ( Highly Dynamic) with minimum latancy. both for Cold Start Time + Init Time. Execution time is also optimized to return the data from database in minimum time. No Express Framework OR Any Third party libray is used. MongoDB Integration is added using mongodb native driver for javascript. Complete pagination, filter and specific returned fields options for dynamic read e-Route without any changes to backend.

[ GET ] /api/e/{entity}?page=1&limit=10 </BR>
json body:   { "filter": { "name": "furqan" }, "sort": { "_id": "desc" }, "fields": ["name", "tech_stack"] }


</BR></BR>
Just upload "app.zip" to AWS Lambda directly via Lambda Code mangement console as function size is just 682.7 kB </BR>
This will result towards minimum cold start time for Node.js runtime for new Node.js 18.x runtime on arm64 architecture ( AWS Graviton Processor for minimum pricing of Lambda function )</BR>

We can use MongoDB Atlas Cloud managed solution - [Free Shared Instance](https://www.mongodb.com/blog/post/free-your-genius-on-mongodb-atlas-free-tier)
</BR></BR>
**e-Route** </BR>
Connect an API gateway with $default stage and only one route GET /{proxy+}: </BR>
Following Routes are available to access the resources from db: </BR>
[ GET ] /api/e/{entity} </BR>
[ GET ] /api/e/{entity}/{id} </BR>
</BR>
**READ**: Any Entity as json request can be read from the MongoDB database </BR>


</BR> **Working On** </BR>
- JWT authorization via:
  - APIGateway Authorizer for generic proxy route
  - Custom implementation is pretty much dynamic. Using JWT Library dependency but it may add an additional cold start time for boot up.
- </BR> CI/CD for one-click/command deploy updates to Lambda func 

</BR>Any Feedback, suggestion, improvisation is welcomed</BR>

</BR></BR>
**Created By**, </BR>
Furqan </BR>
(Software Developer / Solution Architect) </BR></BR>
