# Salim Blog API

A Simple Blog Service created with Fast API and Redis-OM

![image](https://user-images.githubusercontent.com/64667212/186480200-6d4d01d1-886d-4e72-91fd-61430a5bfed6.png)

![image](https://user-images.githubusercontent.com/64667212/186480270-0b4e1fcb-973f-48a0-ae6e-e40f69a6ddea.png)

![image](https://user-images.githubusercontent.com/64667212/186480338-c1832cea-6527-4ba6-9343-9fe97b01cfd7.png)

![image](https://user-images.githubusercontent.com/64667212/186480601-c3b89d36-7a11-4116-a5d8-cc7758ffe4fb.png)

# Overview video

Here's a short video that explains the project and how it uses Redis:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/eLC8isM7iCE/0.jpg)](https://www.youtube.com/watch?v=eLC8isM7iCE)


## How it works

The blog is pretty simple. It has the following API's;

- A `GET` method at the home page that displays the message `Hello world, I am Salim from Africa!`. 

- Two `POST` methods [to create authors and blogs respectively] that users can use to create a new blog and register as an author. 

The author method collects the pk, first name, last name, email address, bio of the author and the date the author joined. The schema is shown below. 
```
"pk": "string",
  "first_name": "string",
  "last_name": "string",
  "email": "string",
  "bio": "string",
  "date_joined": "2022-08-24T16:59:09.222111"
  ```

- A `GET` method that retrieves the created blogs. 

- A `PUT` method that is capable of updating blogs. 

- A `DELETE` method that makes users able to delete blogs.

### How the data is stored:

![image](https://user-images.githubusercontent.com/64667212/186483903-dc3ad327-37d4-4269-a210-08cca05a7beb.png)

### How the data is accessed:

Data is accessed using a pk i.e. a keyword that is assigned to each author. 

![image](https://user-images.githubusercontent.com/64667212/186484928-dc66bc92-8d59-4b7f-979c-80329707281e.png)

## How to run it locally?

Step 1: Clone the repository locally to a location of your choice. 

Step 2: Create and activate a virtual environment. 

For windows
```
$ python  -m venv env 
$ cd env\Scripts\activate
```

For MacOS
```
$ python3 -m venv env 
$ source env/bin/activate
```

Step 3: Install all the needed dependencies in the virtual environment
```
pip install -r requirements.txt
```

Step 4: Go to the blog directory and run the server

```
$ cd blog
$ uvicorn main:app --reload
```

Navigate to http://127.0.0.1:8000/docs in your browser

### Prerequisites

- A python interpreter
- A code editor



## Deployment

To make deploys work, you need to create free account on [Redis Cloud](https://redis.info/try-free-dev-to)

### Google Cloud Run

To run on Google button, check [here](https://cloud.google.com/blog/products/serverless/introducing-cloud-run-button-click-to-deploy-your-git-repos-to-google-cloud)

### Heroku

To deploy on Heroku button, check [here](https://devcenter.heroku.com/articles/heroku-button)

### Netlify

To deploy on Netlify button, check [here](https://www.netlify.com/blog/2016/11/29/introducing-the-deploy-to-netlify-button/)

### Vercel

To deploy on Vercel button,check [here](https://vercel.com/docs/deploy-button)

## More Information about Redis Stack

Here some resources to help you quickly get started using Redis Stack. If you still have questions, feel free to ask them in the [Redis Discord](https://discord.gg/redis) or on [Twitter](https://twitter.com/redisinc).

### Getting Started

1. Sign up for a [free Redis Cloud account using this link](https://redis.info/try-free-dev-to) and use the [Redis Stack database in the cloud](https://developer.redis.com/create/rediscloud).
1. Based on the language/framework you want to use, you will find the following client libraries:
    - [Redis OM .NET (C#)](https://github.com/redis/redis-om-dotnet)
        - Watch this [getting started video](https://www.youtube.com/watch?v=ZHPXKrJCYNA)
        - Follow this [getting started guide](https://redis.io/docs/stack/get-started/tutorials/stack-dotnet/)
    - [Redis OM Node (JS)](https://github.com/redis/redis-om-node)
        - Watch this [getting started video](https://www.youtube.com/watch?v=KUfufrwpBkM)
        - Follow this [getting started guide](https://redis.io/docs/stack/get-started/tutorials/stack-node/)
    - [Redis OM Python](https://github.com/redis/redis-om-python)
        - Watch this [getting started video](https://www.youtube.com/watch?v=PPT1FElAS84)
        - Follow this [getting started guide](https://redis.io/docs/stack/get-started/tutorials/stack-python/)
    - [Redis OM Spring (Java)](https://github.com/redis/redis-om-spring)
        - Watch this [getting started video](https://www.youtube.com/watch?v=YhQX8pHy3hk)
        - Follow this [getting started guide](https://redis.io/docs/stack/get-started/tutorials/stack-spring/)

The above videos and guides should be enough to get you started in your desired language/framework. From there you can expand and develop your app. Use the resources below to help guide you further:

1. [Developer Hub](https://redis.info/devhub) - The main developer page for Redis, where you can find information on building using Redis with sample projects, guides, and tutorials.
1. [Redis Stack getting started page](https://redis.io/docs/stack/) - Lists all the Redis Stack features. From there you can find relevant docs and tutorials for all the capabilities of Redis Stack.
1. [Redis Rediscover](https://redis.com/rediscover/) - Provides use-cases for Redis as well as real-world examples and educational material
1. [RedisInsight - Desktop GUI tool](https://redis.info/redisinsight) - Use this to connect to Redis to visually see the data. It also has a CLI inside it that lets you send Redis CLI commands. It also has a profiler so you can see commands that are run on your Redis instance in real-time
1. Youtube Videos
    - [Official Redis Youtube channel](https://redis.info/youtube)
    - [Redis Stack videos](https://www.youtube.com/watch?v=LaiQFZ5bXaM&list=PL83Wfqi-zYZFIQyTMUU6X7rPW2kVV-Ppb) - Help you get started modeling data, using Redis OM, and exploring Redis Stack
    - [Redis Stack Real-Time Stock App](https://www.youtube.com/watch?v=mUNFvyrsl8Q) from Ahmad Bazzi
    - [Build a Fullstack Next.js app](https://www.youtube.com/watch?v=DOIWQddRD5M) with Fireship.io
    - [Microservices with Redis Course](https://www.youtube.com/watch?v=Cy9fAvsXGZA) by Scalable Scripts on freeCodeCamp
