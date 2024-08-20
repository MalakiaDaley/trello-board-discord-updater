
https://trello.com/1/board/boardURL?fields=id&cards=visible&card_fields=id%2Caddress%2Cbadges%2CcardRole%2Cclosed%2Ccoordinates%2Ccover%2CcreationMethodError%2CdateLastActivity%2Cdesc%2CdescData%2Cdue%2CdueComplete%2CdueReminder%2CidAttachmentCover%2CidBoard%2CidLabels%2CidList%2CidMembers%2CidShort%2CisTemplate%2Clabels%2Climits%2ClocationName%2Cname%2Cpinned%2Cpos%2CshortLink%2CshortUrl%2Cstart%2Csubscribed%2Curl&card_attachments=true&card_attachment_fields=id%2Cbytes%2Cdate%2CedgeColor%2CfileName%2CidMember%2CisUpload%2CmimeType%2Cname%2Cpos%2Curl&card_checklists=all&card_checklist_fields=id%2CidBoard%2CidCard%2Cname%2Cpos&card_checklist_checkItems=none&card_customFieldItems=true&card_pluginData=true&card_stickers=true&lists=open&list_fields=id%2Cclosed%2Ccolor%2CcreationMethod%2Cdatasource%2CidBoard%2Climits%2Cname%2Cpos%2CsoftLimit%2Csubscribed%2Ctype

This will return information about cards, limits, members etc

boardURL = is before the boards name
Encoded = the url safe one which you can send requests to

You'll also need a cookie by the name of cloud.session.token= you can find this on the requests tab in the request headers
Look for a request under the specified endpoint using the filter on the network tab on inspect element
Scroll down it's headers until you can see "Cookie" you'll also see cloud.session.token use this as it acts as authorization

OR

Go to inspect element while on the board
Go to application
Go to cookies
Go to trello.com cookie
And copy cloud.session.token from there

<hr>

The data returned will be in a json format put it into jsonviewer and you'll see the structure and understand it

Data returned

```
datePluginDisable : null
desc : ""
descData : null
enterpriseOwned : false
idEnterprise : null
idMemberCreator : "id"
idOrganization : "id"
idTags
labelNames
limits
name : "name-of-board"
nodeId : "ari:cloud:trello::board/workspace/id/id"
powerUps
prefs
premiumFeatures
shortLink : "url"
shortUrl : "https://trello.com/b/url"
subscribed : false
templateGallery : null
url : "https://trello.com/b/url/name-of-board"
boardPlugins
enterprise
labels
members
customFields
memberships
myPrefs
pluginData
organization
```
