This is currently hosted on google app engine.

I don't know much about app engine, except for that this simple project
it is a good fit. As we only update this app every year or so it is easy
to forgot how to do it. Below are instructions (these probably are extremely
obvious to anyone who knows about app engine).

The app is found at http://metcouncilny.appspot.com/

We setup metcouncilny@gmail.com Gmail Account for the purposes of hosting the App Engine site. Put username/password for metcouncilny into Trevor's LassPack account.

Created App Engine app "metcouncilny". Added trevorsummerssmith@gmail.com and khwilson@gmail.com as Owners of the app (most permissive permission).

To deploy:
1) bump app.yml version number
2) commit to git (not required but do this)
3) appcfg.py update .
   # you will be asked to enter creds
4) # it is now deployed but traffic has not been cut over
   # to the new version
   # theres definitely a way to do the following from the cmdline
   # however I have not taken the time to figure out how
   go to the app console http://console.cloud.google.com
   Click on Versions. Redirect all traffic to new version.

This allows us to rollback if we screw something up.