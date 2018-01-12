## Heroku How-To

1) [Download and install Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)
2) Create `.env` file with environment variables (see `.env.example` for reference) -
**don't forget to set the proxy server, or Instagram will treat it as a suspicious login attempt!**
3) run `./init_heroku.sh`
4) run `git push heroku <your-local-branch-name>:master`
5) run `heroku ps:scale worker=1`

And you're gramming 24/7 in the cloud!

## Useful Heroku Commands

* Anytime you need to upload your updated code to Heroku, make sure to commit them, and run step 4.

* You can see the logs either in the web interface or by running:

    `heroku logs --tail`

* To stop the worker, either go to the web interface or run:

    `heroku ps:scale worker=0`

* To push the changes in your environment file to Heroku, run:

    `heroku config:push -f .env -o`
