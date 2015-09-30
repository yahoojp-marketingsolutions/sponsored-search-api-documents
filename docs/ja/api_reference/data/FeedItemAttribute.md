# FeedItemAttribute
FeedItemAttributeオブジェクトは、FeedItem情報の値を格納します。
### Service
+ [FeedItemService](../services/FeedItemService.md)

| フィールド | データ型 | maxOccurs | minOccurs | response | add | set | remove | 説明 | 
|---|---|---|---|---|---|---|---|---|
| placeholderField| enum <a href="./PlaceholderField.md">PlaceholderField</a>| 1| 0| ○| Requirement| Requirement| Ignore| FeedItem情報の種類です。 |
| feedAttributeValue| long| 1| 0| ○| Requirement| Requirement| Ignore| FeedItem情報の値です。 更新するときは、このフィールドに値を入力してmutate(SET)リクエストします。<br>※リクエストでは、mutate(ADD)およびmutate(SET)で指定したFeedItem情報の値が入力されます。<br>※レスポンスでは、審査状況が審査中、または配信中の情報が入力されます。 |
| editFeedAttributeValue| enum <a href="./ApprovalStatus.md">ApprovalStatus</a>| 1| 0| ○※| Ignore| Ignore| Ignore| FeedItem情報が審査中のときのみレスポンスされます。審査が完了するとフィールドが含まれなくなります。<br>※リクエストではこのフィールドは使用しません。<br>※レスポンスでは、審査状況が再審査中か、配信審査中の場合のみ、審査中の情報が設定されます。 |
<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
