
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
```
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
```

To get other information it's like querying a database at the end you want to have ? this is used as query in URL's <br>
All query Paramaters 

```
fields=id
cards=visible
card_fields=id, address,badges,cardRole,closed,coordinates,cover,creationMethodError,dateLastActivity,desc,descData,due,dueComplete,dueReminder,idAttachmentCover,idBoard,idLabels,idList,idMembers,idShort,isTemplate,labels,limits,locationName,name,pinned,pos,shortLink,shortUrl,start,subscribed,url&card_attachments=true&card_attachment_fields=id,bytes,date,edgeColor,fileName,idMember,isUpload,mimeType,name,pos,url&card_checklists=all&card_checklist_fields=id,idBoard,idCard,name,pos&card_checklist_checkItems=none&card_customFieldItems=true&card_pluginData=true&card_stickers=true&lists=open&list_fields=id,closed,color,creationMethod,datasource,idBoard,limits,name,pos,softLimit,subscribed,type
```

Card_fields has it's own set of paramaters what can be customized
```
id
address
badges
cardRole
closed
coordinates
cover
creationMethodError
dateLastActivity
desc
descData
due
dueComplete
dueReminder
idAttachmentCover
idBoard
idLabels
idList
idMembers
idShort
isTemplate
labels
limits
locationName
name
pinned
pos
shortLink
shortUrl
start
subscribed
url
card_attachments=true
card_attachment_fields=id
bytes
date
edgeColor
fileName
idMember
isUpload
mimeType
name
pos
url
card_checklists=all
card_checklist_fields=id
idBoard
idCard
name
pos
card_checklist_checkItems=none
card_customFieldItems=true
card_pluginData=true
card_stickers=true
lists=open
list_fields=id
closed
color
creationMethod
datasource
idBoard
limits
name
pos
softLimit
subscribed
type
```
