# Moviemanor

The movie recommendation app recommends movies to users based on their current mood. Users will be asked to select their current mood and based on their selection, a list of movies will be displayed. The users can also search for movies, view a particular movie's description, cast, and overall rating. Only logged-in users can comment, and upVote or downVote a particular user’s comments.  

Group project repository for CS 554 - Web Programming II @ Stevens Institute of Technology

![License](https://img.shields.io/github/license/vatsalshah007/Moviemanor)
![GitHub language count](https://img.shields.io/github/languages/count/vatsalshah007/Moviemanor)
![Stars](https://img.shields.io/github/stars/vatsalshah007/Moviemanor)
---
Team Members :-

  Mehul Savaliya
  
  Niyati Bavishi
  
  Pallavi Jaiswal
  
  Vatsal Shah

---
# Instuctions to Run Application

You can run our application either by cloning this using CLI or run the Docker images using Docker CLI.

## Using CLI

For this guide you need to have [Git](https://git-scm.com/downloads) installed as well as [Node.js](https://nodejs.dev/download) installed on your local machine. 

> ### Step 1:- Clone the repository
To clone project -
```
 git clone "https://github.com/vatsalshah007/Moviemanor.git"
```
You can skip this step if you have the source code and go to the next steps.

> ### Step 2:- Server

  Make sure you have the .env file for the server, placed in the root directory of the server otherwise the application won't work.
  
  To start Server -
 ```
 cd Moviemanor
 cd Server
 npm i
 npm start
```

> ### Step 3:- Client

  Make sure you have the .env file for the client, placed in the root directory of the client otherwise the application won't work.
  
  To start Client -
 ```
 cd Moviemanor
 cd Client
 npm i
 npm start
```  

## Using Docker CLI

You can even run Docker images directly from step 2 if you do not wish to pull the images from the Docker registry. For this guide you need to have [Docker](https://docs.docker.com/get-docker/) installed on your local machine. 

**All the Environment variables are provided in the .env file**

If you want to check out our application on Docker, simply follow the steps below:

> ### Step 1:- Pulling the Server and Client Images from the Docker registry (optional)
To pull the Server image run
```
docker pull marksman007/moviemanor-server
```

To pull the Client image run 
```
docker pull marksman007/moviemanor-client
```

> ### Step 2:- Run the Server Image (required)
Type this command to run the server image and replace the environment variables values with the values provided in the server's .env file

```
docker run -p 4000:4000 --env ATLAS_DATABASE="<ATLAS_DATABASE_VALUE>" --env ATLAS_MOVIE_COLLECTION="<ATLAS_MOVIE_COLLECTION_VALUE>" --env ATLAS_SAVE_MOVIE_COLLECTION="<ATLAS_SAVE_MOVIE_COLLECTION_VALUE>" --env ATLAS_COMMENTS_COLLECTION="<ATLAS_COMMENTS_COLLECTION_VALUE>" --env ATLAS_USERIMAGE_COLLECTION="<ATLAS_USERIMAGE_COLLECTION_VALUE>" --env TMDB_API_KEY="<TMDB_API_KEY_VALUE>" --env ATLAS_PASSWORD="<ATLAS_PASSWORD_VALUE>" --env ATLAS_USERNAME="<ATLAS_USERNAME_VALUE>" --env ATLAS_DATABASE_NO_CAPS="<ATLAS_DATABASE_NO_CAPS_VALUE>" --rm marksman007/moviemanor-server:latest
```
Please enter the correct key values <ins>**without**</ins> "" from the server's .env file. Also keep the port numbers as they are and make sure no other task is running on this port

> ### Step 3:- Run the Client Image (required)
Type this command to run the server image and replace the environment variables values with the values provided in the client's .env file

```
docker run -p 3000:3000 --env REACT_APP_FIREBASE_KEY="<REACT_APP_FIREBASE_KEY_VALUE>" --env REACT_APP_FIREBASE_DOMAIN="<REACT_APP_FIREBASE_DOMAIN_VALUE>" --env REACT_APP_FIREBASE_DATABASE="<REACT_APP_FIREBASE_DATABASE_VALUE>" --env REACT_APP_FIREBASE_PROJECT_ID="<REACT_APP_FIREBASE_PROJECT_ID_VALUE>" --env REACT_APP_FIREBASE_STORAGE_BUCKET="<REACT_APP_FIREBASE_STORAGE_BUCKET_VALUE>" --env REACT_APP_FIREBASE_SENDER_ID="<REACT_APP_FIREBASE_SENDER_ID_VALUE>" --env REACT_APP_FIREBASE_APP_ID="<REACT_APP_FIREBASE_APP_ID_VALUE>" --env REACT_APP_AWS_ACCESS_KEY="<REACT_APP_AWS_ACCESS_KEY_VALUE>" --env REACT_APP_AWS_SECRET_KEY="<REACT_APP_AWS_SECRET_KEY_VALUE>" --env REACT_APP_S3_BUCKET="<REACT_APP_S3_BUCKET_VALUE>" --env REACT_APP_REGION="<REACT_APP_REGION_VALUE>" --rm marksman007/moviemanor-client:latest
```
Please enter the correct key values <ins>**without**</ins> "" from the client's .env file. Also keep the port numbers as they are and make sure no other task is running on this port

> ### Step 4:- For Server (optional)
Type `localhost:4000` in your browser to test the server.

> ### Step 5:- For Client
Type `localhost:3000` in your browser to see and test the application
