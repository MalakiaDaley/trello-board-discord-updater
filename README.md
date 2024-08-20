# trello-board-discord-updater
This will send updates to your discord server when there's a new trello card added to the board you can configure this however you want. I'll maybe edit this in future but right now this is extremely barebones. I believe locking this feature behind paywall is insanely stupid and greedy.

Also for the trello developers I love you but please fix the backend api why is one your requests longer than a paragraph I'd write in an exam. Straight up BULLYING.

endpoints:

https://trello.com/1/board/boardURL?fields=id&cards=visible&card_fields=id,address,badges,cardRole,closed,coordinates,cover,creationMethodError,dateLastActivity,desc,descData,due,dueComplete,dueReminder,idAttachmentCover,idBoard,idLabels,idList,idMembers,idShort,isTemplate,labels,limits,locationName,name,pinned,pos,shortLink,shortUrl,start,subscribed,url&card_attachments=true&card_attachment_fields=id,bytes,date,edgeColor,fileName,idMember,isUpload,mimeType,name,pos,url&card_checklists=all&card_checklist_fields=id,idBoard,idCard,name,pos&card_checklist_checkItems=none&card_customFieldItems=true&card_pluginData=true&card_stickers=true&lists=open&list_fields=id,closed,color,creationMethod,datasource,idBoard,limits,name,pos,softLimit,subscribed,type

Encoded:

https://trello.com/1/board/boardURL?fields=id&cards=visible&card_fields=id%2Caddress%2Cbadges%2CcardRole%2Cclosed%2Ccoordinates%2Ccover%2CcreationMethodError%2CdateLastActivity%2Cdesc%2CdescData%2Cdue%2CdueComplete%2CdueReminder%2CidAttachmentCover%2CidBoard%2CidLabels%2CidList%2CidMembers%2CidShort%2CisTemplate%2Clabels%2Climits%2ClocationName%2Cname%2Cpinned%2Cpos%2CshortLink%2CshortUrl%2Cstart%2Csubscribed%2Curl&card_attachments=true&card_attachment_fields=id%2Cbytes%2Cdate%2CedgeColor%2CfileName%2CidMember%2CisUpload%2CmimeType%2Cname%2Cpos%2Curl&card_checklists=all&card_checklist_fields=id%2CidBoard%2CidCard%2Cname%2Cpos&card_checklist_checkItems=none&card_customFieldItems=true&card_pluginData=true&card_stickers=true&lists=open&list_fields=id%2Cclosed%2Ccolor%2CcreationMethod%2Cdatasource%2CidBoard%2Climits%2Cname%2Cpos%2CsoftLimit%2Csubscribed%2Ctype

This will return card information and labels

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
