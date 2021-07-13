Alchemy Notify Tutorial
============
***
dApps on Ethereum have come a long way over the last several years, both in popularity and in complexity. Unfortunately, the user experience of most dApps is still lacking in comparison to web2 applications.

One key piece missing is real-time notifications of events. Users need to know immediately when their trades execute, when their transactions fail, when their auction bid has been accepted, or when a wallet of interest has aped into some new token. Without these notifications, trades can be missed, critical actions are forgotten, and ultimately users end up abandoning your dApp.

Unfortunately, building these real-time notifications into your dApp has traditionally been complicated, time-consuming, and error-prone. But now with Alchemy Notify, sending real-time push notifications to your users for critical events such as dropped transactions, mined transactions, wallet activity, and even gas price changes is straightforward, easy, and dependable.
***

Let’s look at an example of how, with just a few lines of code, your dApp can integrate the power of Alchemy Notify.

For this example, we’ll create a dApp that notifies users, in real-time, when activity happens on a specific Ethereum address. For our architecture, we’ll use Express for our server, WebSockets to communicate between the client and server, and Alchemy Notify to monitor an address and send a push notification when there is activity on that address.

***
For ease of user experience, we configured this particular tutorial to run on Heroku, but you are more than welcome to use other service providers!
***

> To get up and running, change line 37 and 43 in `server.js` to reflect your particular Alchemy webhook id and auth token!
 
### Luanching with Heroku ###

 1. Get the repo!

      * `git clone https://github.com/pileofscraps/alchemy_notify.git`

 2. Install Heroku-CLI and verify/install dependencies.
 
      * Download Heroku-CLI based on your OS
      * After installation, open your terminal and run `heroku login`; follow the commands that follow to login to your Heroku account.  **If you don't have an account you can sign up for one!
      * Run `node --version`.  You may have any version of Node greater than 10.  If you don’t have it or have an older version, install a more recent version of Node.
      * Run `npm --version`.  `npm` is installed with Node, so check that it’s there. If you don’t have it, install a more recent version of Node:
      * Run `git --version`   Check to make sure you have git installed.  
 
 3. Launch Heroku.
 
      * Download Heroku-CLI based on your OS
      * After installation, open your terminal and run `heroku login`; follow the commands that follow to login to your Heroku account.  **If you don't have an account you can sign up for one!
      * Run `node --version`.  You may have any version of Node greater than 10.  If you don’t have it or have an older version, install a more recent version of Node.
      * Run `npm --version`.  `npm` is installed with Node, so check that it’s there. If you don’t have it, install a more recent version of Node:
      * Run `git --version`   Check to make sure you have git installed.  

 3. Launch Heroku

        find wooden spoon
        uncover pot
        stir
        cover pot
        balance wooden spoon precariously on pot handle
        wait 10 minutes
        goto first step (or shut off burner when done)

    Do not bump wooden spoon or it will fall.
