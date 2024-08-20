
# Returning basic information

https://trello.com/1/board/

This is baseURL for I'm going to assume the backend
after /board/ you put the short url after 
e.g
https://trello.com/b/shortURLCODE/Name-Of-board

When sending a request to the backend you need a cookie known as cloud.session.token
To learn how to get the cookie click <a href=/>Here</a>

# Information Returned

It'll return json data and status of 200 the json structure has the following
<br>
id : "boardID"
name : "Name Of Board"
desc : ""
descData : null
closed : false
idOrganization : "organisationID?"
idEnterprise : null
pinned : false
url : "https://trello.com/b/urlCode/Name-Of-Board"
shortUrl : "https://trello.com/b/urlCode"
prefs : LIST
labelNames : LIST

