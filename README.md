# Github-Issue-Tracker

Live Application

Website is live at Heroku

Explanation to Solution

When the user inputs the url, it's matched using regex. Follwing patterns are allowed
If the input is matched then the [user]/[repository] part is used to send the ajax request to api.github.com/. Since Github API by default sends 30 result per request so to minimize the no. of requests we are also sending an additional parameter per_page = 100 which is maximum that is allowed.

Since the no. of Issues can be more than 100, so we have to make multiple requests. This can be achived by sending an additional parameter page = x where x is the page number.

We keep sending the requests until we receive less than 100 items.
