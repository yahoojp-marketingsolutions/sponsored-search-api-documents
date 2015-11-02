# RuleBaseTargetList
RuleBaseTargetListは、ベースターゲットリストの情報を保持するオブジェクトです。

### Service
+ [RetargetingListService](../services/RetargetingListService.md)

| フィールド | データ型 | max<br>Occurs | min<br>Occurs | resp<br>onse | add | set | remove | 説明 | 
|---|---|---|---|---|---|---|---|---|
| TargetingList(inherited)|||||||||
| accountId|long| 1| 1| ○| Req| Req| -| アカウントIDです。 |
| retargetingAccountStatus| <a href="./RetargetingAccountStatus.md">RetargetingAccountStatus</a>| 1| 0| ○| Ignore| Ignore| -| アカウントのリタゲ審査ステータスです。 |
| targetListid| long| 1| 0| ○| Ignore| Req| -| ターゲットリストIDです。 |
| targetListType| enum <a href="./TargetListType.md">TargetListType</a>| 1| 1| ○| Req| Req| -| ターゲットリスト種別です。 |
| targetListName| string| 1| 0| ○| Req| Opt| -| ターゲットリスト名です。 |
| targetListDescription|string| 1| 0| ○| Opt| Opt| -| ターゲットリストの説明です。 |
| reachStorageStatus| enum <a href="./ReachStorageStatus.md">ReachStorageStatus</a>| 1| 0| ○| Optional<br>※Logical TargetListの場合、ignore| Optional<br>※Logica TargetListの場合、ignore| -| Cookieの保持かのステータスです。<br>※Default値：OPEN |
| reachStorageSpan| long| 1| 0| ○| Optional<br>※Logical TargetListの場合、ignore| Optional<br>※Logica TargetListの場合、ignore| -| Cookieを保持する日数です。<br>※Default値：180 |
| reach| long| 1| 0| ○| Ignore| Ignore| -| リストに蓄積されているユーザー数です。 |
| RuleBaseTargetList|||||||
| rules[]|string|20|0|○|Opt|Opt|-|ルール設定です。|
| isAllVisitor|enum <a href="./IsAllVisitorRule.md">IsAllVisitorRule</a>|1|0|○|Req|Req|-|全訪問者ルール設定です。|
| isDateSpecific|enum <a href="./IsDateSpecificRule.md">IsDateSpecificRule</a>|1|0|○|Opt|Ignore|-|期限付きルールです。|
| startDate|string|1|0|○|Opt|Opt|-|ルール適用開始日です。<br>※YYYYMMDD形式<br>※リクエスト日は2037/12/30まで指定可能です。|
| endDate|string|1|0|○|Opt|Opt|-|ルール適用終了日です。<br>※YYYYMMDD形式<br>※リクエスト日は2037/12/30まで指定可能です。||

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>

