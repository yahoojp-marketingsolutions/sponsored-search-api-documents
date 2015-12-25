# リリースノート
スポンサードサーチAPI ver.5.1
## リリースバージョン
5.1 (WSDLバージョン: 5.1.0)
## バージョンアップの種類
メジャーバージョンアップ  
## 本リリースの主な内容

#### 1. 自動入札設定作成機能を追加
アカウント配下に5パターンの自動入札設定が作成できるようになりました。    
* 検索ページの目標掲載位置  
* クリック数の最大化  
* コンバージョン数の最大化
* コンバージョン単価の目標値
* 広告費用対効果の目標値
  
新規のWebサービスは以下となります。
* BiddingStrategyService(自動入札設定の作成・変更・削除・取得)
  
※ManualCPCは作成できません。 ※キャンペーン、広告グループに関連付いている自動入札設定は 削除できません。   
  
* 対象ウェブサービス  
 * [BiddingStrategyService](/docs/ja/api_reference/services/BiddingStrategyService.md)
  
* 対象データオブジェクト  
 * [BiddingStrategySelector](/docs/ja/api_reference/data/BiddingStrategySelector.md)
 * [BiddingStrategyOperation](/docs/ja/api_reference/data/BiddingStrategyOperation.md)
 * [BiddingStrategyPage](/docs/ja/api_reference/data/BiddingStrategyPage.md)
 * [BiddingStrategyReturnValue](/docs/ja/api_reference/data/BiddingStrategyReturnValue.md)
 * [BiddingStrategyValues](/docs/ja/api_reference/data/BiddingStrategyValues.md)
 * [BiddingStrategy](/docs/ja/api_reference/data/BiddingStrategy.md)
 * [BiddingScheme](/docs/ja/api_reference/data/BiddingScheme.md)
 * [EnhancedCpcBiddingScheme](/docs/ja/api_reference/data/EnhancedCpcBiddingScheme.md)
 * [PageOnePromotedBiddingScheme](/docs/ja/api_reference/data/PageOnePromotedBiddingScheme.md)
 * [TargetCpaBiddingScheme](/docs/ja/api_reference/data/TargetCpaBiddingScheme.md)
 * [TargetSpendBiddingScheme](/docs/ja/api_reference/data/TargetSpendBiddingScheme.md)
 * [TargetRoasBiddingScheme](/docs/ja/api_reference/data/TargetRoasBiddingScheme.md)
  
* 対象Enumerations  
 * [BiddingStrategyType](/docs/ja/api_reference/data/BiddingStrategyType.md)
 * [TargetPositionType](/docs/ja/api_reference/data/TargetPositionType.md)
 * [BidChangesForRaisesOnly](/docs/ja/api_reference/data/BidChangesForRaisesOnly.md)
 * [RaiseBidWhenBudgetConstrained](/docs/ja/api_reference/data/RaiseBidWhenBudgetConstrained.md)
 * [RaiseBidWhenLowQualityScore](/docs/ja/api_reference/data/RaiseBidWhenLowQualityScore.md)
  
#### 2. 自動入札設定リリースに伴う機能改善  
アカウント配下に作成した自動入札設定をキャンペーン、広告グループに関連付けることができるようになりました。  
※キーワードには親（キャンペーンまたは広告グループ）の有効な入札 設定が自動的に関連付けられます。  
※「コンバージョン単価の目標値」または「広告費用対効果の目標値」を関連付ける場合には、コンバージョンオプティマイザーが有効で ある必要があります。  
（関連付けるキャンペーン、広告グループにおいて、直近30日間に一定のコンバージョン実績が発生している場合に、コンバージョンオプティマイザーが有効になります。）  
※制限事項として、サンドボックスではコンバージョンオプティマイザ ーが無条件で有効になります。   
（キャンペーンを新規に作成した場合、コンバージョンオプティマイザーが有効になるまでに一定の時間がかかります。）  
また、自動入札設定ごとの実績値を照会できる「自動入札レポート」を新規に提供します。   
  
* 対象ウェブサービス
 * [CampaignService](/docs/ja/api_reference/services/CampaignService.md)
 * [AdGroupService](/docs/ja/api_reference/services/AdGroupService.md)
 * [AdGroupCriterionService](/docs/ja/api_reference/services/AdGroupCriterionService.md)
 * [ReportDefinitionService](/docs/ja/api_reference/services/ReportDefinitionService.md)
 * [CustomerSyncService](/docs/ja/api_reference/services/CustomerSyncService.md)

* 対象データオブジェクト
 * [CampaignSelector](/docs/ja/api_reference/data/CampaignSelector.md)
 * [Campaign](/docs/ja/api_reference/data/Campaign.md)
 * [AdGroupSelector](/docs/ja/api_reference/data/AdGroupSelector.md)
 * [AdGroup](/docs/ja/api_reference/data/AdGroup.md)
 * [AdGroupCriterionSelector](/docs/ja/api_reference/data/AdGroupCriterionSelector.md)
 * [BiddableAdGroupCriterion](/docs/ja/api_reference/data/BiddableAdGroupCriterion.md)
 * [ReportDefinition](/docs/ja/api_reference/data/ReportDefinition.md)
 * [Auditlog](/docs/ja/api_reference/data/Auditlog.md)
 * [BiddingStrategy](/docs/ja/api_reference/data/BiddingStrategy.md)
 * [BiddingScheme](/docs/ja/api_reference/data/BiddingScheme.md)
 * [ManualCpcBiddingScheme](/docs/ja/api_reference/data/ManualCpcBiddingScheme.md)
 * [EnhancedCpcBiddingScheme](/docs/ja/api_reference/data/EnhancedCpcBiddingScheme.md)
 * [PageOnePromotedBiddingScheme](/docs/ja/api_reference/data/PageOnePromotedBiddingScheme.md)
 * [TargetCpaBiddingScheme](/docs/ja/api_reference/data/TargetCpaBiddingScheme.md)
 * [TargetSpendBiddingScheme](/docs/ja/api_reference/data/TargetSpendBiddingScheme.md)
 * [TargetRoasBiddingScheme](/docs/ja/api_reference/data/TargetRoasBiddingScheme.md)
 * [Bid](/docs/ja/api_reference/data/Bid.md)
 * ManualCPC（削除）
 * AdGroupBid（削除）
 * ManualCPCAdGroupBid（削除）
 * AdGroupCriterionBid（削除）
 * ManualCPCAdGroupCriterionBid（削除）

* 対象Enumerations
 * [BiddingStrategyType](/docs/ja/api_reference/data/BiddingStrategyType.md)
 * [TargetPositionType](/docs/ja/api_reference/data/TargetPositionType.md)
 * [BidChangesForRaisesOnly](/docs/ja/api_reference/data/BidChangesForRaisesOnly.md)
 * [RaiseBidWhenBudgetConstrained](/docs/ja/api_reference/data/RaiseBidWhenBudgetConstrained.md)
 * [RaiseBidWhenLowQualityScore](/docs/ja/api_reference/data/RaiseBidWhenLowQualityScore.md)
 * [BiddingStrategyFailedReason](/docs/ja/api_reference/data/BiddingStrategyFailedReason.md)
 * [BiddingStrategySource](/docs/ja/api_reference/data/BiddingStrategySource.md)
 * [ConversionOptimizerEligibility](/docs/ja/api_reference/data/ConversionOptimizerEligibility.md)
 * [BidSource](/docs/ja/api_reference/data/BidSource.md)
 * [ReportType](/docs/ja/api_reference/data/ReportType.md)
 * [EntityType](/docs/ja/api_reference/data/EntityType.md)
 * [ConversionTrackerCategory](/docs/ja/api_reference/data/ConversionTrackerCategory.md)

#### 3. BudgetOptimizerのサポート終了
BudgetOptimizerの登録と変更が行えなくなりました。（照会のみ可能）  
※登録、変更時にBudgetOptimzerを指定した場合は、バリデーション エラーになります。  
※キャンペーン、広告グループに設定できる入札設定一覧   
  
<table class="standard">
<tbody><tr>
<th valign="top">
  <p>Version</p>
</th>
<th valign="top">
  <p>メソッド</p>
</th>
<th valign="top">
  <p>ManualCPC</p>
</th>
<th valign="top">
  <p>BudgetOptimizer</p>
</th>
<th valign="top">
  <p>自動入札設定</p>
</th>
<th valign="top">
  <p>特記事項</p>
</th>
</tr>
<tr>
<td rowspan="3" valign="top">
  <p>旧Version（Ver.5.0以前）</p>
</td>
<td valign="top">
  <p>add</p>
</td>
<td valign="top">
  <p>○</p>
</td>
<td valign="top">
  <p>×</p>
</td>
<td valign="top">
  <p>×</p>
</td>
<td valign="top">
  <p> - </p>
</td>
</tr>
<tr>
<td valign="top">
  <p>set</p>
</td>
<td valign="top">
  <p>○ ※</p>
</td>
<td valign="top">
  <p>×</p>
</td>
<td valign="top">
  <p>×</p>
</td>
<td valign="top">
  <p>下記の変更は可能です。<br>
・BudgetOptimizer⇒ManualCPC<br>
※ ManualCPC⇒BudgetOptimizer の変更は行えません。</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>get</p>
</td>
<td valign="top">
  <p>○</p>
</td>
<td valign="top">
  <p>○</p>
</td>
<td valign="top">
  <p>×</p>
</td>
<td valign="top">
  <p> - </p>
</td>
</tr>
<tr>
<td rowspan="3" valign="top">
  <p>新Version（Ver.5.1）</p>
</td>
<td valign="top">
  <p>add</p>
</td>
<td valign="top">
  <p>○</p>
</td>
<td valign="top">
  <p>×</p>
</td>
<td valign="top">
  <p>○</p>
</td>
<td valign="top">
  <p> - </p>
</td>
</tr>
<tr>
<td valign="top">
  <p>set</p>
</td>
<td valign="top">
  <p>○ ※</p>
</td>
<td valign="top">
  <p>×</p>
</td>
<td valign="top">
  <p>○</p>
</td>
<td valign="top">
  <p>下記の変更は可能です。<br>
・BudgetOptimizer⇒ManualCPC<br>
・BudgetOptimizer⇒自動入札設定<br>
※ ManualCPC⇒BudgetOptimizer の変更は行えません。</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>get</p>
</td>
<td valign="top">
  <p>○</p>
</td>
<td valign="top">
  <p>○</p>
</td>
<td valign="top">
  <p>○</p>
</td>
<td valign="top">
  <p> - </p>
</td>
</tr>
</tbody>
</table>

* 対象ウェブサービス  
 * [CampaignService](/docs/ja/api_reference/services/CampaignService.md)  
 * [AdGroupService](/docs/ja/api_reference/services/AdGroupService.md)  
 * [AdGroupCriterionService](/docs/ja/api_reference/services/AdGroupCriterionService.md)  
  
* 対象データオブジェクト 
 * [Campaign](/docs/ja/api_reference/data/Campaign.md)  
 * [AdGroup](/docs/ja/api_reference/data/AdGroup.md)  
 * BudgetOptimizer（削除）  
 * BudgetOptimizerAdGroupBid（削除）  
 * BudgetOptimizerAdGroupCriterionBid（削除） 
    
* 対象Enumerations    
 * [BiddingStrategyType](/docs/ja/api_reference/data/BiddingStrategyType.md)  
  

#### 4. アプリダウンロード広告の機能改善  

アプリダウンロード広告に優先配信デバイス（スマートフォン）を設定できるようになりました。  
ターゲティング毎のレポートとして新たに3つのレポートタイプが追加されました。  
    
* 対象ウェブサービス  
 * [AdGroupAdService](/docs/ja/api_reference/services/AdGroupAdService.md)  
  
* 対象データオブジェクト  
 * [AppAd](/docs/ja/api_reference/data/AppAd.md)  
  
#### 5. ConversionTrackerの機能改善  
  
アプリコンバージョン専用のカテゴリタイプ（DOWNLOAD）が追加されました。  
　※本バージョンからアプリコンバージョンのカテゴリタイプに「DEFAULT」は設定できません。  
　※広告管理ツールおよびレポート上での表示は「その他」になります。  
また、スポンサードサーチのモバイル向け広告配信の終了に伴い、モバイル用のマークアップ言語「CHTML」と「WML」の登録と更新が行えなくなりました。（照会のみ可能）  
※登録、変更時に「CHTML」または「WML」を指定した場合は、バリデーションエラーになります。  
  
* 対象ウェブサービス
 * [ConversionTrackerService](/docs/ja/api_reference/services/ConversionTrackerService.md)

* 対象データオブジェクト
 * [ConversionTrackerSelector](/docs/ja/api_reference/data/ConversionTrackerSelector.md)
 
* 対象Enumerations
 * [ConversionTrackerCategory](/docs/ja/api_reference/data/ConversionTrackerCategory.md)


#### 6. Serviceの変更による各Versionへの影響  
  
<table class="standard">
<tbody>
<tr>
<th valign="top">
  <p>Service</p>
</th>
<th valign="top">
  <p>Ver.4.2以前</p>
</th>
<th valign="top">
  <p>Ver.5.0</p>
</th>
<th valign="top">
  <p>Ver.5.1</p>
</th>
</tr>
<tr>
<td valign="top">
  <p>AdGroupAd<br>Service</p>
</td>
<td valign="top">
  <p>- APIIF変更なし</p>
</td>
<td valign="top">
  <p>- APIIF変更なし</p>
</td>
<td valign="top">
  <p>- APIIF変更あり<br>
・アプリ向けの広告情報のオブジェクト（AppAd）に「devicePreference」（優先配信デバイス）のフィールドを追加しました。</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>AdGroup<br>CriterionService</p>
</td>
<td valign="top">
  <p>-APIIF変更なし<br>
・親エンティティの有効な<br>入札設定を関連付けるようにしました。<br>
※入札価格は設定可能です。</p>
</td>
<td valign="top">
  <p>-APIIF変更なし<br>
・親エンティティの<br>
有効な入札設定を<br>
関連付けるようにしました。<br>
※入札価格は設定可能です。</p>
</td>
<td valign="top">
  <p>- APIIF変更あり<br>
・親エンティティの有効な入札設定を関連付けるようにしました。<br>
・有効な入札設定をレスポンスするフィールドを追加しました。<br>
・BudgetOptimizerに関する項目を削除しました。<br>
<br>
■Error<br>
・入札タイプと自動入札IDの両方を指定した際に「210500：Double setting in Auto bidding.」を返します。<br>
・編集中（削除を含む）の自動入札を指定した際に「210501：Setting the disabled Auto bidding.」を返します。<br>
・コンバージョン測定タグが発行されていない際に「210502：Invalid conversion tracking.」を返します。<br>
・コンバージョンの実績が十分ではない際に「210503：Not enough conversions.」を返します。<br>
・キャンペーンの入札設定に「コンバージョン数の最大化」、または「コンバージョン単価の目標値」が設定されている際に「210504：Invalid settings in Auto bidding of campaign.」を返します。<br>
・広告グループの入札設定に「コンバージョン数の最大化」、または「コンバージョン単価の目標値」が設定されている際に「210505：Invalid settings in Auto bidding of ad group.」を返します。<br>
・キーワードに指定できない自動入札を指定した際に「210506：Invalid keyword settings.」を返します。<br>
・予算額を超過している際に「210507：Budget has exceeded.」を返します。<br>
・カスタムURLを更新する際に、キーワードが"承認済み"になっていないケースでは「210508：Keyword is not approved yet.」を返します。<br>
・対象外キーワードに登録されているキーワードを入札キーワードとして登録しようとした際に（その逆のケースも同様）「210509：Cannot set the bidding keyword to negative keywords, or vice versa.」を返します。<br>
・指定されたキーワード、マッチタイプが既にキャンペーン/広告グループ内に存在している際に「Setting already exists in campaign/ad group.」を返します。<br>
・コンバージョンオプティマイザーが利用できない際に「210511：Cannot use conversion optimizer.」を返します。<br>
・キャンペーンがACTIVEではないため、入札戦略が利用できない際に「210512：Set campaign active.」を返します。<br>
・キャンペーンがMANUAL_CPCではないため、入札戦略が利用できない際に「210513：Set campaign to Manual CPC.」を返します。</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>AdGroup<br>Service</p>
</td>
<td valign="top">
  <p>- APIIF変更なし<br>
・親エンティティの<br>
有効な入札設定を関連<br>
付けるようにしました。<br>
※入札価格は設定可能です。<br>
（bidをRequirementから<br>Optionalに変更）</p>
</td>
<td valign="top">
  <p>- APIIF変更なし<br>
・親エンティティの<br>
有効な入札設定を関連<br>
付けるようにしました。<br>
※入札価格は設定可能です。<br>
（bidをRequirementから<br>Optionalに変更）</p>
</td>
<td valign="top">
  <p>- APIIF変更あり<br>
・入札設定情報を保持するフィールドを追加しました。<br>
・BudgetOptimizerに関する項目を削除しました。<br>
<br>
■Error<br>
・入札タイプと自動入札IDの両方を指定した際に「210400：Double setting in Auto bidding.」を返します。<br>
・編集中（削除を含む）の自動入札を指定した際に「210401：Setting the disabled Auto bidding.」を返します。<br>
・コンバージョン測定タグが発行されていない際に「210402：Invalid conversion tracking.」を返します。<br>
・コンバージョンの実績が十分ではない際に「210403：Not enough conversions.」を返します。<br>
・キーワードに個別の入札価格または入札設定が指定されている状態で、広告グループに「コンバージョン数の最大化」、または「コンバージョン単価の目標値」の自動入札を設定しようとした際に「210404：Auto bidding is already set.」を返します。<br>
・予算額を超過している際に「210405：Budget has exceeded.」を返します。<br>
・コンバージョンオプティマイザーが利用できない際に「210406：Cannot use conversion optimizer.」を返します。<br>
・キャンペーンがACTIVEではないため、入札戦略が利用できない際に「210407：Set campaign active.」を返します。<br>
・キャンペーンがMANUAL_CPCではないため、入札戦略が利用できない際に「210408：Set campaign to Manual CPC.」を返します。</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>BiddingStrategy<br>Service</p>
</td>
<td valign="top">
  <p>- 提供なし</p>
</td>
<td valign="top">
  <p>- 提供なし</p>
</td>
<td valign="top">
  <p>- 新規公開</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>Campaign<br>Service</p>
</td>
<td valign="top">
  <p>- APIIF変更なし<br>
・自動入札設定は<br>行えません。<br>
・BudgetOptimizerの<br>
登録、変更は行えません。<br>
※照会は行えます。<br>
※BudgetOptimizerから<br>
ManualCPCの変更は行えます。</p>
</td>
<td valign="top">
  <p>- APIIF変更なし<br>
・自動入札設定は<br>行えません。<br>
・BudgetOptimizerの<br>
登録、変更は行えません。<br>
※照会は行えます。<br>
※BudgetOptimizerから<br>
ManualCPCの変更は行えます。</p>
</td>
<td valign="top">
  <p>- APIIF変更あり<br>
・入札設定情報を保持するフィールドを追加しました。<br>
・BudgetOptimizerに関する項目を削除しました。<br>
・コンバージョンオプティマイザーが利用可能であるかを判定する項目をレスポンスに追加しました。<br>
<br>
■Error<br>
・入札タイプと自動入札IDの両方に指定がない、または両方を指定している際に「210300：Double or no settings in Auto bidding.」を返します。<br>
・編集中（削除を含む）の自動入札を指定した際に「210301：Setting the disabled Auto bidding.」を返します。<br>
・コンバージョン関連の自動入札設定を指定した際に「210302：Conversion related settings in Auto bidding.」を返します。<br>
・コンバージョン測定タグが発行されていない際に「210303：Invalid conversion tracking.」を返します。<br>
・コンバージョンの実績が十分ではない際に「210304：Not enough conversions.」を返します。<br>
・キーワードに個別の入札価格または入札設定が指定されている状態で、キャンペーンに「コンバージョン数の最大化」、または「コンバージョン単価の目標値」の自動入札を設定しようとした際に「210305：Auto bidding is already set.」を返します。<br>
・コンバージョンオプティマイザーが利用できない際に「210306：Cannot use conversion optimizer.」を返します。<br>
・キャンペーン内の広告グループ・キーワードに設定されている予算よりも予算額が低く設定された際に「210307：Budget is lower than ad group/keywords.」を返します。<br>
・キャンペーンがACTIVEではないため、入札戦略が利用できない際に「210308：Set campaign active.」を返します。<br>
・キャンペーンがMANUAL_CPCではないため、入札戦略が利用できない際に「210309：Set campaign to Manual CPC.」を返します。</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>CustomerSync<br>Service</p>
</td>
<td valign="top">
  <p>-APIIF変更なし<br>
※入札情報は<br>照会できません。</p>
</td>
<td valign="top">
  <p>-APIIF変更なし<br>
※入札情報は<br>照会できません。</p>
</td>
<td valign="top">
  <p>- APIIF変更あり<br>
・EntityTypeのEnumに「BIDDING_STRATEGY」（自動入札設定）を追加しました。<br>
・操作履歴情報を保持するオブジェクト（Auditlog）に「biddingStrategyId」（自動入札ID）のフィールドを追加しました。</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>ReportDefinition<br>Service</p>
</td>
<td valign="top">
  <p>- APIIF変更なし<br>
※新レポートタイプ<br>
および追加フィールド、<br>
セグメントは指定できません。</p>
</td>
<td valign="top">
  <p>- APIIF変更なし<br>
※新レポートタイプ<br>
および追加フィールド、<br>
セグメントは指定できません。</p>
</td>
<td valign="top">
  <p>- APIIF変更あり<br>
・ReportTypeのEnumに「BID_STRATEGY」（自動入札設定レポート）を追加しました。<br>
・レポート定義情報を保持するオブジェクト（ReportDefinition）に「biddingStrategyIds」（自動入札ID）のフィールドを追加しました。</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>Conversion<br>TrackerService</p>
</td>
<td valign="top">
  <p>- APIIF変更なし<br>
・マークアップ言語<br>
「CHTML」と「WML」の<br>
登録と変更は行えません。<br>
※照会は行えます。<br>
※登録、変更時に<br>
「CHTML」または「WML」を<br>
指定した場合は、バリデーション<br>
エラーになります。</p>
</td>
<td valign="top">
  <p>- APIIF変更なし<br>
※ アプリコンバージョンで<br>
ConversionTrackerCategoryに<br>
「DEFAULT」を指定した場合は、<br>
「DOWNLOAD」に変換します。<br>
　- 登録/変更：DEFAULT⇒DOWNLOAD<br>
　- 照会：DOWNLOAD⇒DEFAULT<br>
<br>
・マークアップ言語「CHTML」と<br>
「WML」の登録と変更は行えません。<br>
　※照会は行えます。<br>
　※登録、変更時に「CHTML」または<br>
「WML」を指定した場合は、<br>
バリデーションエラーになります。</p>
</td>
<td valign="top">
  <p>- APIIF変更あり<br>
・ConversionTrackerCategoryのEnumに「DOWNLOAD」（ダウンロード）を追加しました。<br>
　※アプリコンバージョンでは「DEFAULT」の指定はできません。<br>
　※広告管理ツールおよびレポート上での表示は「その他」になります。<br>
・マークアップ言語「CHTML」と「WML」の登録と変更は行えません。<br>
　※照会は行えます。<br>
　※登録、変更時に「CHTML」または「WML」を指定した場合は、バリデーションエラーになります。</p>
</td>
</tr>
</tbody>
</table>

#### 7. 下位バージョンへの影響
下位バージョンにおいてもBudgetOptimizerの登録と変更は行えなく なりましたのでご注意下さい。  
また、以下のAPIIFにおいては下位バージョンにも修正が行われておりますが、今までと同じリクエスト内容でAPIを使用できます。  

##### AdGroupCriterionService
* operand/bid/type が Requirement 項目（ADD,SET,REMOVE）でし たが、自動的に親のtypeを引き継ぐためIgnore項目に変更しました。

##### AdGroupService
* operand/bid/type が Requirement項目（ADD）でしたが、自動的に 親のtypeを引き継ぐためIgnore項目に変更しました。
* operand/bid/keywordMaxCpc が Requirement項目（ADD）でした が、デフォルト値（1円）を設定したことにより、Optional項目に 変更しました。


#### 8. エラーコードの変更
本バージョンの一部サービスからは返されるエラー内容が変更になりました。  
詳細については以下をご確認ください。  

##### CampaignService

<table class="standard">
<tbody>
<tr>
<th colspan="2" valign="top">
  <p>Ver.5.0以前</p>
</th>
<th colspan="2" valign="top">
  <p>Ver.5.1</p>
</th>
</tr>
<tr>
<th valign="top">
  <p>コード</p>
</th>
<th valign="top">
  <p>メッセージ</p>
</th>
<th valign="top">
  <p>コード</p>
</th>
<th valign="top">
  <p>メッセージ</p>
</th>
</tr>
<tr>
<td valign="top">
  <p>10100</p>
</td>
<td valign="top">
  <p> DEACTIVATED </p>
</td>
<td valign="top">
  <p> 0010 </p>
</td>
<td valign="top">
  <p>not a valid id.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10104</p>
</td>
<td valign="top">
  <p> EXISTS_SAME_NAME </p>
</td>
<td valign="top">
  <p> 0059 </p>
</td>
<td valign="top">
  <p>Same value has already been registered.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10300</p>
</td>
<td valign="top">
  <p> OVER_LIMIT</p>
</td>
<td valign="top">
  <p>0063</p>
</td>
<td valign="top">
  <p>Over limit.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10400</p>
</td>
<td valign="top">
  <p> EXISTS_SAME_NAME </p>
</td>
<td valign="top">
  <p> 0059 </p>
</td>
<td valign="top">
  <p>Same value has already been registered.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20101</p>
</td>
<td valign="top">
  <p> REQUIRED </p>
</td>
<td valign="top">
  <p> 0006 </p>
</td>
<td valign="top">
  <p> required.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20102</p>
</td>
<td valign="top">
  <p> NOT_LIST </p>
</td>
<td valign="top">
  <p> 0014 </p>
</td>
<td valign="top">
  <p>selector is invalid.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20105</p>
</td>
<td valign="top">
  <p> NOT_HASH </p>
</td>
<td valign="top">
  <p> 0001 </p>
</td>
<td valign="top">
  <p>Invalid Request.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20401</p>
</td>
<td valign="top">
  <p> DUPLICATE </p>
</td>
<td valign="top">
  <p> 0058 </p>
</td>
<td valign="top">
  <p> Duplicate values. </p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20601</p>
</td>
<td valign="top">
  <p> INVALID_NUMBER_FORMAT </p>
</td>
<td valign="top">
  <p> 0007 </p>
</td>
<td valign="top">
  <p>invalid number format.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20602</p>
</td>
<td valign="top">
  <p> LOWER_NUMBER </p>
</td>
<td valign="top">
  <p> 0057 </p>
</td>
<td valign="top">
  <p>Too small value.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20603</p>
</td>
<td valign="top">
  <p> OVER_NUMBER </p>
</td>
<td valign="top">
  <p> 0056 </p>
</td>
<td valign="top">
  <p> Too large value.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20604</p>
</td>
<td valign="top">
  <p> INVALID_STEP_NUMBER </p>
</td>
<td valign="top">
  <p> 0065 </p>
</td>
<td valign="top">
  <p>Invalid step value.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20701</p>
</td>
<td valign="top">
  <p> INVALID_STRING_FORMAT </p>
</td>
<td valign="top">
  <p> 0008 </p>
</td>
<td valign="top">
  <p>invalid string format.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20703</p>
</td>
<td valign="top">
  <p> OVER_STRING </p>
</td>
<td valign="top">
  <p> 0054 </p>
</td>
<td valign="top">
  <p>Too long values.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20901</p>
</td>
<td valign="top">
  <p> INVALID_DATE_FORMAT </p>
</td>
<td valign="top">
  <p> 0060 </p>
</td>
<td valign="top">
  <p>Invalid date format.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20902</p>
</td>
<td valign="top">
  <p> LOWER_DATE </p>
</td>
<td valign="top">
  <p> 0066 </p>
</td>
<td valign="top">
  <p>Date set before the available period.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20903</p>
</td>
<td valign="top">
  <p> OVER_DATE </p>
</td>
<td valign="top">
  <p> 0067 </p>
</td>
<td valign="top">
  <p>Date set after the available period.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>21001</p>
</td>
<td valign="top">
  <p> INVALID_ENUM </p>
</td>
<td valign="top">
  <p> 0009 </p>
</td>
<td valign="top">
  <p>invalid enum.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>21401</p>
</td>
<td valign="top">
  <p> INVALID_RELATION </p>
</td>
<td valign="top">
  <p>0063</p>
</td>
<td valign="top">
  <p>Invalid relation.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10602</p>
</td>
<td valign="top">
  <p> LOWER_BUDGET_AMOUNT </p>
</td>
<td valign="top">
  <p> 210307 </p>
</td>
<td valign="top">
  <p>Budget is lower than ad group/keywords.</p>
</td>
</tr>
</tbody>
</table>

##### AdGroupService
<table class="standard">
<tbody>
<tr>
  <th colspan="2" valign="top">
<p>Ver.5.0以前</p>
  </th>
  <th colspan="2" valign="top">
<p>Ver.5.1</p>
  </th>
</tr>
<tr>
  <th valign="top">
<p>コード</p>
  </th>
  <th valign="top">
<p>メッセージ</p>
  </th>
  <th valign="top">
<p>コード</p>
  </th>
  <th valign="top">
<p>メッセージ</p>
  </th>
</tr>
<tr>
  <td valign="top">
<p>10100</p>
  </td>
  <td valign="top">
<p> DEACTIVATED </p>
  </td>
  <td valign="top">
<p> 0010 </p>
  </td>
  <td valign="top">
<p>not a valid id.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>10300</p>
  </td>
  <td valign="top">
<p> OVER_LIMIT</p>
  </td>
  <td valign="top">
<p>0063</p>
  </td>
  <td valign="top">
<p>Over limit.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>10400</p>
  </td>
  <td valign="top">
<p> EXISTS_SAME_NAME </p>
  </td>
  <td valign="top">
<p> 0059 </p>
  </td>
  <td valign="top">
<p>Same value has already been registered.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20101</p>
  </td>
  <td valign="top">
<p> REQUIRED </p>
  </td>
  <td valign="top">
<p> 0006 </p>
  </td>
  <td valign="top">
<p> required.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20102</p>
  </td>
  <td valign="top">
<p> NOT_LIST </p>
  </td>
  <td valign="top">
<p> 0014 </p>
  </td>
  <td valign="top">
<p>selector is invalid.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20105</p>
  </td>
  <td valign="top">
<p> NOT_HASH </p>
  </td>
  <td valign="top">
<p> 0001 </p>
  </td>
  <td valign="top">
<p>Invalid Request.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20401</p>
  </td>
  <td valign="top">
<p> DUPLICATE </p>
  </td>
  <td valign="top">
<p> 0058 </p>
  </td>
  <td valign="top">
<p> Duplicate values. </p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20601</p>
  </td>
  <td valign="top">
<p> INVALID_NUMBER_FORMAT </p>
  </td>
  <td valign="top">
<p> 0007 </p>
  </td>
  <td valign="top">
<p>invalid number format.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20602</p>
  </td>
  <td valign="top">
<p> LOWER_NUMBER </p>
  </td>
  <td valign="top">
<p> 0057 </p>
  </td>
  <td valign="top">
<p>Too small value.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20603</p>
  </td>
  <td valign="top">
<p> OVER_NUMBER </p>
  </td>
  <td valign="top">
<p> 0056 </p>
  </td>
  <td valign="top">
<p> Too large value.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20701</p>
  </td>
  <td valign="top">
<p> INVALID_STRING_FORMAT </p>
  </td>
  <td valign="top">
<p> 0008 </p>
  </td>
  <td valign="top">
<p>invalid string format.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20702</p>
  </td>
  <td valign="top">
<p> LOWER_STRING </p>
  </td>
  <td valign="top">
<p> 0006 </p>
  </td>
  <td valign="top">
<p>required.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>20703</p>
  </td>
  <td valign="top">
<p> OVER_STRING </p>
  </td>
  <td valign="top">
<p> 0054 </p>
  </td>
  <td valign="top">
<p>Too long values.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>21001</p>
  </td>
  <td valign="top">
<p> INVALID_ENUM </p>
  </td>
  <td valign="top">
<p> 0009 </p>
  </td>
  <td valign="top">
<p>invalid enum.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>21401</p>
  </td>
  <td valign="top">
<p> INVALID_RELATION </p>
  </td>
  <td valign="top">
<p>0063</p>
  </td>
  <td valign="top">
<p>Invalid relation.</p>
  </td>
</tr>
<tr>
  <td valign="top">
<p>10601</p>
  </td>
  <td valign="top">
<p> OVER_BUDGET_AMOUNT </p>
  </td>
  <td valign="top">
<p> 210405 </p>
  </td>
  <td valign="top">
<p>Budget has exceeded.</p>
  </td>
</tr>
  </tbody>
</table>

##### AdGroupService

<table class="standard">
<tbody>
<tr>
<th colspan="2" valign="top">
  <p>Ver.5.0以前</p>
</th>
<th colspan="2" valign="top">
  <p>Ver.5.1</p>
</th>
</tr>
<tr>
<th valign="top">
  <p>コード</p>
</th>
<th valign="top">
  <p>メッセージ</p>
</th>
<th valign="top">
  <p>コード</p>
</th>
<th valign="top">
  <p>メッセージ</p>
</th>
</tr>
<tr>
<td valign="top">
  <p>10100</p>
</td>
<td valign="top">
  <p> DEACTIVATED </p>
</td>
<td valign="top">
  <p> 0010 </p>
</td>
<td valign="top">
  <p>not a valid id.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10300</p>
</td>
<td valign="top">
  <p> OVER_LIMIT</p>
</td>
<td valign="top">
  <p>0063</p>
</td>
<td valign="top">
  <p>Over limit.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10400</p>
</td>
<td valign="top">
  <p> EXISTS_SAME_NAME </p>
</td>
<td valign="top">
  <p> 0059 </p>
</td>
<td valign="top">
  <p>Same value has already been registered.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20101</p>
</td>
<td valign="top">
  <p> REQUIRED </p>
</td>
<td valign="top">
  <p> 0006 </p>
</td>
<td valign="top">
  <p> required.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20102</p>
</td>
<td valign="top">
  <p> NOT_LIST </p>
</td>
<td valign="top">
  <p> 0014 </p>
</td>
<td valign="top">
  <p>selector is invalid.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20105</p>
</td>
<td valign="top">
  <p> NOT_HASH </p>
</td>
<td valign="top">
  <p> 0001 </p>
</td>
<td valign="top">
  <p>Invalid Request.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20401</p>
</td>
<td valign="top">
  <p> DUPLICATE </p>
</td>
<td valign="top">
  <p> 0058 </p>
</td>
<td valign="top">
  <p> Duplicate values. </p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20601</p>
</td>
<td valign="top">
  <p> INVALID_NUMBER_FORMAT </p>
</td>
<td valign="top">
  <p> 0007 </p>
</td>
<td valign="top">
  <p>invalid number format.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20602</p>
</td>
<td valign="top">
  <p> LOWER_NUMBER </p>
</td>
<td valign="top">
  <p> 0057 </p>
</td>
<td valign="top">
  <p>Too small value.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20603</p>
</td>
<td valign="top">
  <p> OVER_NUMBER </p>
</td>
<td valign="top">
  <p> 0056 </p>
</td>
<td valign="top">
  <p> Too large value.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20701</p>
</td>
<td valign="top">
  <p> INVALID_STRING_FORMAT </p>
</td>
<td valign="top">
  <p> 0008 </p>
</td>
<td valign="top">
  <p>invalid string format.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20702</p>
</td>
<td valign="top">
  <p> LOWER_STRING </p>
</td>
<td valign="top">
  <p> 0006 </p>
</td>
<td valign="top">
  <p>required.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20703</p>
</td>
<td valign="top">
  <p> OVER_STRING </p>
</td>
<td valign="top">
  <p> 0054 </p>
</td>
<td valign="top">
  <p>Too long values.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>21001</p>
</td>
<td valign="top">
  <p> INVALID_ENUM </p>
</td>
<td valign="top">
  <p> 0009 </p>
</td>
<td valign="top">
  <p>invalid enum.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>21401</p>
</td>
<td valign="top">
  <p> INVALID_RELATION </p>
</td>
<td valign="top">
  <p>0063</p>
</td>
<td valign="top">
  <p>Invalid relation.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10601</p>
</td>
<td valign="top">
  <p> OVER_BUDGET_AMOUNT </p>
</td>
<td valign="top">
  <p> 210405 </p>
</td>
<td valign="top">
  <p>Budget has exceeded.</p>
</td>
</tr>
</tbody>
</table>


##### AdGroupCriterionService

<table class="standard">
<tbody>
<tr>
<th colspan="2" valign="top">
  <p>Ver.5.0以前</p>
</th>
<th colspan="2" valign="top">
  <p>Ver.5.1</p>
</th>
</tr>
<tr>
<th valign="top">
  <p>コード</p>
</th>
<th valign="top">
  <p>メッセージ</p>
</th>
<th valign="top">
  <p>コード</p>
</th>
<th valign="top">
  <p>メッセージ</p>
</th>
</tr>
<tr>
<td valign="top">
  <p>10100</p>
</td>
<td valign="top">
  <p> DEACTIVATED </p>
</td>
<td valign="top">
  <p> 0010 </p>
</td>
<td valign="top">
  <p>not a valid id.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10300</p>
</td>
<td valign="top">
  <p> OVER_LIMIT</p>
</td>
<td valign="top">
  <p>0063</p>
</td>
<td valign="top">
  <p>Over limit.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10400</p>
</td>
<td valign="top">
  <p> EXISTS_SAME_NAME </p>
</td>
<td valign="top">
  <p> 0059 </p>
</td>
<td valign="top">
  <p>Same value has already been registered.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20101</p>
</td>
<td valign="top">
  <p> REQUIRED </p>
</td>
<td valign="top">
  <p> 0006 </p>
</td>
<td valign="top">
  <p> required.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20102</p>
</td>
<td valign="top">
  <p> NOT_LIST </p>
</td>
<td valign="top">
  <p> 0014 </p>
</td>
<td valign="top">
  <p>selector is invalid.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20105</p>
</td>
<td valign="top">
  <p> NOT_HASH </p>
</td>
<td valign="top">
  <p> 0001 </p>
</td>
<td valign="top">
  <p>Invalid Request.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20401</p>
</td>
<td valign="top">
  <p> DUPLICATE </p>
</td>
<td valign="top">
  <p> 0058 </p>
</td>
<td valign="top">
  <p> Duplicate values. </p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20601</p>
</td>
<td valign="top">
  <p> INVALID_NUMBER_FORMAT </p>
</td>
<td valign="top">
  <p> 0007 </p>
</td>
<td valign="top">
  <p>invalid number format.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20602</p>
</td>
<td valign="top">
  <p> LOWER_NUMBER </p>
</td>
<td valign="top">
  <p> 0057 </p>
</td>
<td valign="top">
  <p>Too small value.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20603</p>
</td>
<td valign="top">
  <p> OVER_NUMBER </p>
</td>
<td valign="top">
  <p> 0056 </p>
</td>
<td valign="top">
  <p> Too large value.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20701</p>
</td>
<td valign="top">
  <p> INVALID_STRING_FORMAT </p>
</td>
<td valign="top">
  <p> 0008 </p>
</td>
<td valign="top">
  <p>invalid string format.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20702</p>
</td>
<td valign="top">
  <p> LOWER_STRING </p>
</td>
<td valign="top">
  <p> 0006 </p>
</td>
<td valign="top">
  <p>required.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>20703</p>
</td>
<td valign="top">
  <p> OVER_STRING </p>
</td>
<td valign="top">
  <p> 0054 </p>
</td>
<td valign="top">
  <p>Too long values.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>21001</p>
</td>
<td valign="top">
  <p> INVALID_ENUM </p>
</td>
<td valign="top">
  <p> 0009 </p>
</td>
<td valign="top">
  <p>invalid enum.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>21401</p>
</td>
<td valign="top">
  <p> INVALID_RELATION </p>
</td>
<td valign="top">
  <p>0062</p>
</td>
<td valign="top">
  <p>Invalid relation.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>21601</p>
</td>
<td valign="top">
  <p> INVALID_URL_FORMAT </p>
</td>
<td valign="top">
  <p>0064</p>
</td>
<td valign="top">
  <p>Invalid url format.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10601</p>
</td>
<td valign="top">
  <p> OVER_BUDGET_AMOUNT</p>
</td>
<td valign="top">
  <p> 210507 </p>
</td>
<td valign="top">
  <p>Budget has exceeded.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10200</p>
</td>
<td valign="top">
  <p> INVALID_STATUS </p>
</td>
<td valign="top">
  <p> 210508 </p>
</td>
<td valign="top">
  <p>Keyword is not approved yet.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10701</p>
</td>
<td valign="top">
  <p> EXISTS_DIFFERENT_CRITERION_USE_TYPE </p>
</td>
<td valign="top">
  <p> 210509 </p>
</td>
<td valign="top">
  <p>Cannot set bidding keyword to negative keywords, or vice versa.</p>
</td>
</tr>
<tr>
<td valign="top">
  <p>10702</p>
</td>
<td valign="top">
  <p> EXISTS_SAME_TERM_WITH_MATCH_TYPE </p>
</td>
<td valign="top">
  <p> 210510 </p>
</td>
<td valign="top">
  <p>Setting already exists in campaign/ad group.</p>
</td>
</tr>
</tbody>
</table>


## 技術ドキュメント

本リリースの内容が含まれたドキュメントは、スポンサードサーチ Ver.5.1です。

## SS API Ver.4.0以前のご利用について
SS API Ver.4.0以前のバージョンも引き続きご利用いただけます。

## スポンサードサーチ API Ver.4.0以前のサポート終了予定日
Ver.4.0は、2014年4月以降にサポート終了予定です。  
※決定次第、あらためてお知らせいたします。  
