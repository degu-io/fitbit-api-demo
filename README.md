# FitBit API Demo

An annotated demo of how to access the FitBit OAuth 2.0 library 
using Node.js, Redis and Express.js

In this demo we will:
  1. Request access to a user's data from FitBit
  2. Acquire the user's `access token` and other key details
  3. Use the `access token` to acquire a food log from a specific date

Requirements:
  - Node.js (This demo was developed using Node 4.1.1 it should work with 
    most recent versions.)
  - Redis
  - A FitBit API Client ID, Key and Secret - see https://dev.fitbit.com/apps/new
  - Specify a callback in when setting up you FitBit app `http://localhost:3000/auth/fitbit/callback`

To run the app:
  - create a text file `.env` based on the `env-sample` file 
  - populate the `.env` with your FitBit app details
  - run `npm install`
  - from the command line run `node index.js`
  - visit `http://localhost:3000/auth`

You will be asked by FitBit to login and grant access to this app. 
Should you accept you will be redirected to the `/user/:user_id` page where you 
will see the JSON of the date specified food log.

## More info

FitBit API: https://dev.fitbit.com

Redis: https://www.npmjs.com/package/redis & http://redis.io/commands

Express.JS: http://expressjs.com/en/4x/api.html

