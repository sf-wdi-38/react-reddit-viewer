# React Reddit Viewer

Your goal is to to use AJAX to consume Reddit's JSON api and display it using React. You will not create a backend or use a database (reddit _is_ our database).

(Reddit is like the armpit of the internet, so we're so sorry about that).

## Requirements
At a minium your site should have:

* a landing page that displays a list of possible subreddits
* a page for each subreddit, showing the 20 or so top posts
  * a title
  * a vote count
  * a link to the original thread
  * an image
 
**Bonus**: Allow a user to navigate to *any* subreddit by typing the (correct) name into a "search" box. E.g. if I type "funny" into the box, I see the top results for the [r/funny subreddit](https://www.reddit.com/r/funny.json).

**Super-Bonus**: Active subreddits will change quickly! Can you check for updates and automatically re-render the page when there are changes? This pattern is often called "polling" (i.e. checking for changes every 20 seconds).

## Client Routes & Reddit Endpoints

| Client Route | description           | JSON Endpoint  |
| -------------|-------------| -----|
| `/`      | subreddits#index      |  n/a (just hardcode a list of subreddits) |
| `/programmerhumor` | subreddits#show     |  GET `https://www.reddit.com/r/programmerhumor.json` |
| `/reactjs` | subreddits#show   |  GET `https://www.reddit.com/r/reactjs.json` |

> Please note that all reddit endpoints use **HTTPS**. You will get an error if you use just unsecured HTTP.

## Setup
Please use `create-react-app` to generate your project.

```bash
create-react-app react-viewer
cd react-viewer
npm install # <-- not needed, already done for us
npm start # <-- launches the server, opens the browser to http://localhost:3000
```

Dependencies you may eventually need:

* `react-router@3.0.0`
* `jquery-ajax`

## Good Luck!
<img max-width=400 src="https://media3.giphy.com/media/goiauJeRxagM/giphy.gif">
