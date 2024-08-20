# trello-api-understanding

Hello this was originally going to be discord auto-updater for trello but I'll do that in another repo once I've set things up. This is some of trello's backend API and give's brief understanding to returning key information
Also for the trello developers I love you but please fix the backend api why is one your requests longer than a paragraph I'd write in an exam. Straight up BULLYING.

<h2>Endpoints</h2>
<ul>
  <li><a href=/basic>Querying Information</a></li>
  <li><a href=#cookie>Get Your Cookies</a></li>
</ul>

# Cookie

To get the cookie by the name of cloud.session.token= you can find this on the requests tab in the request headers
Look for a request under the specified endpoint using the filter on the network tab on inspect element
Scroll down it's headers until you can see "Cookie" you'll also see cloud.session.token use this as it acts as authorization

OR

Go to inspect element while on the board
Go to application
Go to cookies
Go to trello.com cookie
And copy cloud.session.token from there

<hr>
