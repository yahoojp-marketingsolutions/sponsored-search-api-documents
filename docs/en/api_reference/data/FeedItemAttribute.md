# FeedItemAttribute
FeedItemAttribute contains the value of FeedItem information.
### Service
+ [FeedItemService](../services/FeedItemService.md)

| Field | Data Type | maxOccurs | minOccurs | response | add | set | remove | Description | 
|---|---|---|---|---|---|---|---|---|
| placeholderField| enum <a href="./PlaceholderField.md">PlaceholderField</a>| 1| 0| yes| Requirement| Requirement| Ignore| FeedItem information type |
| feedAttributeValue| long| 1| 0| yes| Requirement| Requirement| Ignore| FeedItem information value<br>For update, insert value in this field and request set<br>* In request, value of FeedItem information can be inserted from add and set<br>* In response, information will appear when it is in review or in approved status |
| editFeedAttributeValue| enum <a href="./ApprovalStatus.md">ApprovalStatus</a>| 1| 0| yes※| Ignore| Ignore| Ignore| Responded only when FeedItem information is in review<br>Field will not appear after the review is done<br>* In request, this field will not be used<br>* In response, information will appear when it is in disapproved with review or in delivery review. |
<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
