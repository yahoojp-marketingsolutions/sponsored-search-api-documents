# FeedItem
FeedItem is a container of FeedItem information.
### Service
+ [FeedItemService](../services/FeedItemService.md)

| Field | Data Type | maxOccurs | minOccurs | response | add | set | remove | Description | 
|---|---|---|---|---|---|---|---|---|
| accountId| long| 1| 1| yes| Requirement| RequirementNot updatable| RequirementNot updatable| Account ID |
| feedItemId| long| 1| 0| yes| Ignore| RequirementNot updatable| RequirementNot updatable| FeedItem ID |
| approvalStatus| enum <a href="./ApprovalStatus.md">ApprovalStatus</a>| 1| 0| yes| Ignore| Ignore| Ignore| Approval status |
| disapprovalReasonCodes| string| unbounded| 0| yes| Ignore| Ignore| Ignore| Reason for disapproval |
| feedItemAttribute| <a href="./FeedItemAttribute.md">FeedItemAttribute</a>| unbounded| 0| yes| Requirement| RequirementUpdatable| Ignore| FeedItem information |
| placeholderType| enum <a href="./PlaceholderType.md">PlaceholderType</a>| 1| 0| yes| Requirement| RequirementNot updatable| RequirementNot updatable| FeedItem type |
| devicePreference| enum <a href="./DevicePreference.md">DevicePreference</a>| 1| 0| yes| OptionalUpdatable| OptionalUpdatable| Ignore| Device preference |
| startDate| string| 1| 0| yes| OptionalUpdatable| OptionalUpdatable| Ignore| Start date of displaySetting will be canceled by leaving here blank on set |
| endDate| string| 1| 0| yes| OptionalUpdatable| OptionalUpdatable| Ignore| End date of displaySetting will be canceled by leaving here blank on set |
| scheduling| <a href="./FeedItemScheduling.md">FeedItemScheduling</a>| 1| 0| yes| OptionalUpdatable| OptionalUpdatable| Ignore| Schedule of displaySetting will be canceled by leaving here blank on set |
<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
