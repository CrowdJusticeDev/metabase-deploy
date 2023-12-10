[![Metabase Logo](http://www.metabase.com/images/logo.svg)](http://www.metabase.com/)

[Metabase](http://www.metabase.com/) is the easy, open source way for everyone in your company to ask questions and learn from data.

# How to update Metabase

Update the version in this file: https://github.com/CrowdJusticeDev/metabase-buildpack/blob/master/bin/version

Clone the metabase-deploy repo to your local machine:

```bash
git clone https://github.com/CrowdJusticeDev/metabase-deploy
cd metabase-deploy
```

Add a git remote for our Metabase instance (replace <metabase-app-name> with the name of the Heroku app):

```bash
git remote add heroku https://git.heroku.com/<metabase-app-name>.git
```

Add an empty commit to the repo to force a re-deploy:

```bash
git commit --allow-empty -m "empty commit"
git push heroku master
```

Wait for the deploy to finish
