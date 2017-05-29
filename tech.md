# Tech
Decisions on how to implement this thing

# Arch
Serverless, because this is a learning project and I want to find out its limitations. Also it's cheaper for the usage I'll have.

# Cloud Platform
Which cloud platform to choose. Freeness is important, because I don't expect anyone to use this but me.

I'll easily fit in the free tier for all of the cloud platforms for the foreseeable future

- https://aws.amazon.com/s/dm/optimization/server-side-test/free-tier/free_nc/#details
- https://cloud.google.com/free/docs/always-free-usage-limits

### AWS
- Experience
- Mature
- Apex
- Chalice
- Most Lambda languages

##### Free forever
- Lambda
- Dynamodb

##### Free 12 Months
- API Gateway, but cheap after

### GCE
- New to me, in a good way
- Only supports node for functions
- No API gateway for functions, auth is manual, boo
- Can maybe do something with firebase, yay. Is it free?
- Need to find out if their DynamoDB equivalent is any good

##### Free forever
- Everything I need (except firebase?)

##### Links
- https://stackoverflow.com/questions/37178919/google-cloud-datastore-vs-firebase
- https://cloud.google.com/free/docs/map-aws-google-cloud-platform

### Azure
Not free that I know of for what I want

# Language
- Go if Apex?
- Python if Chalice?
- Node

### Go
- Working wity Dynamodb directly is shit
- Not portable to other platform
- Middling experience, maximum interest
- Dependency management hell

### Python
- Slow, but probably doesn't matter
- Not portable to other platform
- I know it better, so prefer to work on something new

### Node
- Easy to work with JSON and define custom graphql object types
- Portable, but what versions?
- I have less experience

# Back End

### Graphql + NoSQL
Graphql is any idea for implementing the metrics side of things (the query endpoint to the API). More traditional REST could then create users and events as necessary.

This would be backed by a NoSQL DB, with NoSQL in this case being something like Dynamodb

##### Why
- Something new and cool to learn
- Looks like it could actually work well
- Library with flexible back end

##### Notes
- Static types is really nice for dynamically typed languages
- Seems like every language has pretty good libraries that match up to spec
- I don't know much about all this, but that's a good thing

##### Links
- https://github.com/chentsulin/awesome-graphql
-  https://stackoverflow.com/questions/33819658/dynamic-unique-objects-in-graphql
- https://gitter.im/graphql-go/graphql
- https://www.youtube.com/watch?v=srfaKA2wJ0s
- https://github.com/graphql/graphql-js/issues/290
- https://github.com/graphql/graphql-js/issues/405
- https://github.com/serverless/serverless-graphql-blog

### Graphite
Probably less flexibile by faster to just do what I want with less faffing. A good falllback option, but a couple of reasons not to use it:
 
- Might want to do more than metrics in the future
- No way to run a free instance forever that I know of, not available as a cloud service
- Good fallback

##### Links
- http://obfuscurity.com/2014/01/Graphite-Tip-A-Better-Way-to-Store-Events