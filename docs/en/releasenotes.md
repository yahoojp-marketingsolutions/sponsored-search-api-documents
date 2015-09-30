# Release Notes
Sponsored Search API ver.5.1
## Release version
5.1 (WSDL Version: 5.1.0)
## Types of Version update
Minor version up
## Main contents of this release

#### 1. Added Auto bidding setting function
Five types of auto bidding can be set on each account.    
* Target position in search results  
* Maximize clicks  
* Maximize conversions
* Target CPA
* Target ROAS (Return On Average Spend)
  
New Web Service is as follows.
* BiddingStrategyService (Create, Update, Delete, Acquire the Auto bidding)
  
*Cannot create ManualCPC. <br>
*Cannot delete the auto bidding that has been set to Campaign, and Ad group. 
  
* Target Web Service  
 * [BiddingStrategyService](/docs/en/api_reference/services/BiddingStrategyService.md)
  
* Target Data Object  
 * [BiddingStrategySelector](/docs/en/api_reference/data/BiddingStrategySelector.md)
 * [BiddingStrategyOperation](/docs/en/api_reference/data/BiddingStrategyOperation.md)
 * [BiddingStrategyPage](/docs/en/api_reference/data/BiddingStrategyPage.md)
 * [BiddingStrategyReturnValue](/docs/en/api_reference/data/BiddingStrategyReturnValue.md)
 * [BiddingStrategyValues](/docs/en/api_reference/data/BiddingStrategyValues.md)
 * [BiddingStrategy](/docs/en/api_reference/data/BiddingStrategy.md)
 * [BiddingScheme](/docs/en/api_reference/data/BiddingScheme.md)
 * [EnhancedCpcBiddingScheme](/docs/en/api_reference/data/EnhancedCpcBiddingScheme.md)
 * [PageOnePromotedBiddingScheme](/docs/en/api_reference/data/PageOnePromotedBiddingScheme.md)
 * [TargetCpaBiddingScheme](/docs/en/api_reference/data/TargetCpaBiddingScheme.md)
 * [TargetSpendBiddingScheme](/docs/en/api_reference/data/TargetSpendBiddingScheme.md)
 * [TargetRoasBiddingScheme](/docs/en/api_reference/data/TargetRoasBiddingScheme.md)
  
* Target Enumerations  
 * [BiddingStrategyType](/docs/en/api_reference/data/BiddingStrategyType.md)
 * [TargetPositionType](/docs/en/api_reference/data/TargetPositionType.md)
 * [BidChangesForRaisesOnly](/docs/en/api_reference/data/BidChangesForRaisesOnly.md)
 * [RaiseBidWhenBudgetConstrained](/docs/en/api_reference/data/RaiseBidWhenBudgetConstrained.md)
 * [RaiseBidWhenLowQualityScore](/docs/en/api_reference/data/RaiseBidWhenLowQualityScore.md)
  
#### 2. Function improvement from Auto bidding release  
Can associate created auto bidding to each Campaigns and Ad groups.   
Start offering the report for performance of each auto bidding.  
*Keywords will automatically relate to the valid bid setting from Campaign or Ad group.  
*To relate the "Target CPA" or "Target ROAS", conversion optimizer have to be valid.  
(Conversion optimizer will be valid when there are a conversion performance in the recent 30 days in Campaign and Ad group)  
*Conversion optimizer will be valid without any conditions.  
(When Campaign is created, it may take time to have the conversion optimizer valid)  
Also, "Auto bidding report" will be available, to confirm the performance of Auto bidding.  
  
* Target Web Service
 * [CampaignService](/docs/en/api_reference/services/CampaignService.md)
 * [AdGroupService](/docs/en/api_reference/services/AdGroupService.md)
 * [AdGroupCriterionService](/docs/en/api_reference/services/AdGroupCriterionService.md)
 * [ReportDefinitionService](/docs/en/api_reference/services/ReportDefinitionService.md)
 * [CustomerSyncService](/docs/en/api_reference/services/CustomerSyncService.md)

* Target Data Object
 * [CampaignSelector](/docs/en/api_reference/data/CampaignSelector.md)
 * [Campaign](/docs/en/api_reference/data/Campaign.md)
 * [AdGroupSelector](/docs/en/api_reference/data/AdGroupSelector.md)
 * [AdGroup](/docs/en/api_reference/data/AdGroup.md)
 * [AdGroupCriterionSelector](/docs/en/api_reference/data/AdGroupCriterionSelector.md)
 * [BiddableAdGroupCriterion](/docs/en/api_reference/data/BiddableAdGroupCriterion.md)
 * [ReportDefinition](/docs/en/api_reference/data/ReportDefinition.md)
 * [Auditlog](/docs/en/api_reference/data/Auditlog.md)
 * [BiddingStrategy](/docs/en/api_reference/data/BiddingStrategy.md)
 * [BiddingScheme](/docs/en/api_reference/data/BiddingScheme.md)
 * [ManualCpcBiddingScheme](/docs/en/api_reference/data/ManualCpcBiddingScheme.md)
 * [EnhancedCpcBiddingScheme](/docs/en/api_reference/data/EnhancedCpcBiddingScheme.md)
 * [PageOnePromotedBiddingScheme](/docs/en/api_reference/data/PageOnePromotedBiddingScheme.md)
 * [TargetCpaBiddingScheme](/docs/en/api_reference/data/TargetCpaBiddingScheme.md)
 * [TargetSpendBiddingScheme](/docs/en/api_reference/data/TargetSpendBiddingScheme.md)
 * [TargetRoasBiddingScheme](/docs/en/api_reference/data/TargetRoasBiddingScheme.md)
 * [Bid](/docs/en/api_reference/data/Bid.md)
 * ManualCPC（Deleted）
 * AdGroupBid（Deleted）
 * ManualCPCAdGroupBid（Deleted）
 * AdGroupCriterionBid（Deleted）
 * ManualCPCAdGroupCriterionBid（Deleted）

* Target Enumerations
 * [BiddingStrategyType](/docs/en/api_reference/data/BiddingStrategyType.md)
 * [TargetPositionType](/docs/en/api_reference/data/TargetPositionType.md)
 * [BidChangesForRaisesOnly](/docs/en/api_reference/data/BidChangesForRaisesOnly.md)
 * [RaiseBidWhenBudgetConstrained](/docs/en/api_reference/data/RaiseBidWhenBudgetConstrained.md)
 * [RaiseBidWhenLowQualityScore](/docs/en/api_reference/data/RaiseBidWhenLowQualityScore.md)
 * [BiddingStrategyFailedReason](/docs/en/api_reference/data/BiddingStrategyFailedReason.md)
 * [BiddingStrategySource](/docs/en/api_reference/data/BiddingStrategySource.md)
 * [ConversionOptimizerEligibility](/docs/en/api_reference/data/ConversionOptimizerEligibility.md)
 * [BidSource](/docs/en/api_reference/data/BidSource.md)
 * [ReportType](/docs/en/api_reference/data/ReportType.md)
 * [EntityType](/docs/en/api_reference/data/EntityType.md)
 * [ConversionTrackerCategory](/docs/en/api_reference/data/ConversionTrackerCategory.md)

#### 3. End of Support for BudgetOptimizer
End the support for create and update of BudgetOptimizer (Reference supports will continue).<br>
　*Error will return when create and update request are sent to BudgetOptimizer. <br>
　*Auto bidding comparison for Version 4.2/5.0 and Version 5.1.<br>

<table class="standard">
<tbody><tr>
<th valign="top">
   <p>Version</p>
</th>
<th valign="top">
   <p>method</p>
</th>
<th valign="top">
   <p>ManualCPC</p>
</th>
<th valign="top">
   <p>BudgetOptimizer</p>
</th>
<th valign="top">
   <p>Auto bidding</p>
</th>
<th valign="top">
   <p>Notes</p>
</th>
</tr>
<tr>
<td rowspan="3" valign="top">
   <p>Ver.4.2/5.0</p>
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
   <p>○*</p>
</td>
<td valign="top">
   <p>×</p>
</td>
<td valign="top">
   <p>×</p>
</td>
<td valign="top">
   <p>Update procedure as below is possible.<br>
・BudgetOptimizer ⇒ ManualCPC<br>
*ManualCPC ⇒ BudgetOptimizer is not possible</p>
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
   <p>Ver.5.1</p>
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
   <p>○*</p>
</td>
<td valign="top">
   <p>×</p>
</td>
<td valign="top">
   <p>○</p>
</td>
<td valign="top">
   <p>Update procedure as below is possible.<br>
・BudgetOptimizer ⇒ ManualCPC<br>
・BudgetOptimizer ⇒ Autobidding setting<br>
*ManualCPC ⇒ BudgetOptimizer is not possible</p>
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


* Target Web Service  
 * [CampaignService](/docs/en/api_reference/services/CampaignService.md)  
 * [AdGroupService](/docs/en/api_reference/services/AdGroupService.md)  
 * [AdGroupCriterionService](/docs/en/api_reference/services/AdGroupCriterionService.md)  
  
* Target Data Object 
 * [Campaign](/docs/en/api_reference/data/Campaign.md)  
 * [AdGroup](/docs/en/api_reference/data/AdGroup.md)  
 * BudgetOptimizer（Deleted）  
 * BudgetOptimizerAdGroupBid（Deleted）  
 * BudgetOptimizerAdGroupCriterionBid（Deleted） 
    
* Target Enumerations    
 * [BiddingStrategyType](/docs/en/api_reference/data/BiddingStrategyType.md)  
  

#### 4. Function improvement for App Ads  

Can set Priority device (Smartphone) from App Ads.
    
* Target Web Service  
 * [AdGroupAdService](/docs/en/api_reference/services/AdGroupAdService.md)  
  
* Target Data Object  
 * [AppAd](/docs/en/api_reference/data/AppAd.md)  
  
#### 5. Function improvement for ConversionTracker  
  
Category type (DOWNLOAD) for App conversion has been added.  
　*From this version, “DEFAULT” setting will not be possible to category type of App conversion.   
　*Report from Campaign Management Tool will be displayed as "Others".  
From the closing of Sponsored Search API for Mobile (feature phone) Ads, creation and updates of markup language for Mobile, "CHTML" and "WML" will not be available. (Reference supports will continue).  
　*Error will return if "CHTML" or "WML" is selected.  
  
* Target Web Service
 * [ConversionTrackerService](/docs/en/api_reference/services/ConversionTrackerService.md)

* Target Data Object
 * [ConversionTrackerSelector](/docs/en/api_reference/data/ConversionTrackerSelector.md)
 
* Target Enumerations
 * [ConversionTrackerCategory](/docs/en/api_reference/data/ConversionTrackerCategory.md)


#### 6. Impact on each Version from the change of Services  
  
<table class="standard">
<tbody>
<tr>
<th valign="top">
   <p>Service</p>
</th>
<th valign="top">
   <p>Ver.4.2 and before</p>
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
   <p>AdGroupAdService</p>
</td>
<td valign="top">
   <p>- No change in APIIF</p>
</td>
<td valign="top">
   <p>- No change in APIIF</p>
</td>
<td valign="top">
   <p>- APIIF changed<br>
・”devicePreference” (Focus device) has been added to the field of App ad object</p>
</td>
</tr>
<tr>
<td valign="top">
   <p>AdGroupCriterionService</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
・Cannot set for Auto bidding.<br>
・Cannot create and/or update BudgetOptimizer.<br>
　*Reference is possible.<br>
　*Change from BudgetOptimizer to ManualCPC is possible.</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
・Cannot set for Auto bidding.<br>
・Cannot create and/or update BudgetOptimizer.<br>
　*Reference is possible.<br>
　*Change from BudgetOptimizer to ManualCPC is possible.</p>
</td>
<td valign="top">
   <p>- APIIF changed
・Field to set Auto bidding been added. (Only from ManualCpc）<br>
・BudgetOptimizeritem is deleted.
<br>
<br>
■Error messages<br>
・”210500：Doublesetting in bidding strategy.” will return if Auto bidding type and Auto bidding ID are set.<br>
・”210501：Settingthe disabled bidding strategy.” will return if Auto bidding is set when editing (or delete).<br>
・”210502：Invalidconversion tracking.” will return if conversion tag is not created<br>
・”210503：Notenough conversions.” Will return if conversion performance is not enough.<br>
・”210504：Invalidsettings in bidding strategy of campaign.” will return if “Maximize conversion” and/or “Target CPA” are set when setting Auto bidding of Campaign.<br>
・”210505：Invalidsettings in bidding strategy of ad group.” will return if “Maximize conversion” and/or “Target CPA” are set when setting Auto bidding of Ad group.<br>
・”210506：Invalidkeyword settings.” will return if Auto bidding is set to the Keyword that cannot be set.<br>
・”210507：Budgethas exceeded.” will return if the budget exceeds.<br>
・”210508：is not approved yet.“will return if　non-approved Keyword is used during the update of Custom URL.<br>
・”210509：Cannotset the bidding keyword to negative keywords, or vice versa.” will return if bidding keywords are set as negative keywords (and/or vice versa)<br>
・”210510：Settingalready exists in Campaign/Ad group.” will return if designated Keyword and/or match type already exists in Campaign and/or Ad group.<br>
・”210511：Cannotuse conversion optimizer.” will return if conversion optimizer cannot be used.</p>
</td>
</tr>
<tr>
<td valign="top">
   <p>AdGroupService</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
・Cannot set for Auto bidding.<br>
・Cannot create  and/or update BudgetOptimizer<br>
　*Reference is possible.<br>
　*Change from BudgetOptimizer to ManualCPC is possible.<br>
<br>
・If Auto bidding is not set, the upper entity’s Auto bidding will be applied as a default. </p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
・Cannot set for Auto bidding.<br>
・Cannot create and/or update BudgetOptimizer<br>
　*Reference is possible.<br>
　*Change from BudgetOptimizer to ManualCPC is possible.<br>
<br>
・If Auto bidding is not set, the upper entity’s Auto bidding will be applied as a default. </p>
</td>
<td valign="top">
   <p>- APIIF changed<br>
・Added field for Auto bidding setting.<br>
・BudgetOptimizer item has been deleted.<br>
<br>
■Error messages<br>
・”210400：Doublesetting in bidding strategy.” will return if both Auto bidding type and Auto bidding ID are set.<br>
・”210401：Settingthe disabled bidding strategy.” will return if Auto bidding is set during the update (including delete).<br>
・”210402：Invalid conversion tracking.” will return if conversion tag is not created.<br>
・”210403：Not enough conversions.” will return if conversion performance is not enough.<br>
・”210404：Biddingstrategy is already set.” will return if “Maximize conversions” and/or “Target CPA” are set to Campaign when bid or auto bidding is already set to Keyword.<br>
・”210405：Budget has exceeded.” Will return if the budget exceeds.<br>
・”210406：Cannot use conversion optimizer.” will return if conversion optimizer cannot be used.</p>
</td>
</tr>
<tr>
<td valign="top">
   <p>BiddingStrategyService</p>
</td>
<td valign="top">
   <p>- Not supported</p>
</td>
<td valign="top">
   <p>- Not supported</p>
</td>
<td valign="top">
   <p>- New Service</p>
</td>
</tr>
<tr>
<td valign="top">
   <p>CampaignService</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
・Cannot set for Auto bidding.<br>
・Cannot create and/or update BudgetOptimizer.<br>
　*Reference is possible.<br>
　*Change from BudgetOptimizer to ManualCPC is possible.</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
・Cannot set for Auto bidding.<br>
・Cannot create and/or update BudgetOptimizer.<br>
　*Reference is possible.<br>
　*Change from BudgetOptimizer to ManualCPC is possible.</p>
</td>
<td valign="top">
   <p>- APIIF changed<br>
・Added field for Auto bidding setting.<br>
・BudgetOptimizer item has been deleted.<br>
<br>
■Error messages<br>
・”210300：Double or no settings in bidding strategy.”  will return if Auto bidding type and Auto bidding ID both were set, or not set (need one setting).<br>
・”210301：Setting the disabled bidding strategy.” will return if Auto bidding is set when editing (or delete).<br>
・”210302：Conversion related settings in bidding strategy.” will return if Auto  bidding set the items that are conversion related.<br>
・”210303：Invalid conversion tracking.” will return if conversion tag is not created.<br>
・”210304：Not enough conversions.” will return if conversion performance is not enough.<br>
・”210305：Biddingstrategy is already set.” will return if “Maximize conversions” and/or “Target CPA” are set to Campaign when bid or auto bidding is already set to Keyword.<br>
・”210306：Cannot use conversion optimizer.” will return if conversion optimizer cannot be used.<br>
・”210307：Budget is lower than ad group/keywords.” will return if Campaign budget is lower than the budget of Ad group and/or Keyword</p>
</td>
</tr>
<tr>
<td valign="top">
   <p>CustomerSyncService</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
　*Cannot reference the bid information.</p>
</td>
<td valign="top">
   <p>-No change in APIIF<br>
　*Cannot reference the bid information.</p>
</td>
<td valign="top">
   <p>- APIIF changed.<br>
・”BIDDING_STRATEGY” (Auto bidding setting) has been added to EntityType.<br>
・”biddingStrategyId“ (Autobidding ID) field has been added to Auditlog.</p>
</td>
</tr>
<tr>
<td valign="top">
   <p>ReportDefinitionService</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
　*Cannot designate the new report type and added field and segments</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
　*Cannot designate the new report type and added field and segments</p>
</td>
<td valign="top">
   <p>- APIIF changed<br>
・”BID_STRATEGY” (Auto bidding setting report) has been added to ReportType.<br>
・”biddingStrategyIds” (Auto bidding ID) field been added to ReportDefinition.</p>
</td>
</tr>
<tr>
<td valign="top">
   <p>ConversionTrackerService</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
・Cannot create or update the markup language "CHTML" and "WML".<br>
　*Reference is possible.<br>
　*Error will occur if "CHTML" or "WML" is selected in create or update.</p>
</td>
<td valign="top">
   <p>- No change in APIIF<br>
*If “DEFAULT” is set, it will change to “DOWNLOAD” in ConversionTrackerCategory<br>
　-Create/Upload: DEFAULT to DOWNLOAD<br>
　-Reference: DOWNLOAD to DEFAULT<br>
<br>
・Cannot create or update the markup language "CHTML" and "WML".<br>
　*Reference is possible.<br>
　*Error will occur if "CHTML" or "WML" is selected in create or update.</p>
</td>
<td valign="top">
   <p>- APIIF changed<br>
・”DOWNLOAD” been added to ConversionTrackerCategory.<br>
　*Cannot “DEFAULT” in App conversion.<br>
　*From Campaign Management Tool and report, it will display as "Others".<br>
・Cannot create or update the markup language "CHTML" and "WML".<br>
　*Reference is possible.<br>
　*Error will occur if "CHTML" or "WML" is selected in create or update.</p>
</td>
</tr>
</tbody>
</table>

#### 7. Compatibility with version before
The change below will also be effective with version before. <br>However, there will be no problem or effect in using the same request as before.  
##### AdGroupCriterionService
* operand/bid/type was a Requirement for ADD,SET, and REMOVE, but it has changed to Ignore to have the relation with upper class. 

##### AdGroupService
* operand/bid/type was a Requirement for ADD but it has changed to Ignore to have the relation with upper class
* operand/bid/keywordMaxCpc was a Requirement for ADD, but it has changed to Optional, because the default (one yen) has been set.


#### 8. Change of Error Code
There are some changed in error code from this version.  
Please confirm the details below.  
  

##### CampaignService

<table class="standard">
<tbody>
<tr>
<th colspan="2" valign="top">
  <p>Ver.5.0 or before</p>
</th>
<th colspan="2" valign="top">
  <p>Ver.5.1</p>
</th>
</tr>
<tr>
<th valign="top">
  <p>Code</p>
</th>
<th valign="top">
  <p>Message</p>
</th>
<th valign="top">
  <p>Code</p>
</th>
<th valign="top">
  <p>Message</p>
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
  <p>Ver.5.0 or before</p>
</th>
<th colspan="2" valign="top">
  <p>Ver.5.1</p>
</th>
</tr>
<tr>
<th valign="top">
  <p>Code</p>
</th>
<th valign="top">
  <p>Message</p>
</th>
<th valign="top">
  <p>Code</p>
</th>
<th valign="top">
  <p>Message</p>
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
<p>Ver.5.0 or before</p>
  </th>
  <th colspan="2" valign="top">
<p>Ver.5.1</p>
  </th>
</tr>
<tr>
  <th valign="top">
<p>Code</p>
  </th>
  <th valign="top">
<p>Message</p>
  </th>
  <th valign="top">
<p>Code</p>
  </th>
  <th valign="top">
<p>Message</p>
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
  <p>Ver.5.0 or before</p>
</th>
<th colspan="2" valign="top">
  <p>Ver.5.1</p>
</th>
</tr>
<tr>
<th valign="top">
  <p>Code</p>
</th>
<th valign="top">
  <p>Message</p>
</th>
<th valign="top">
  <p>Code</p>
</th>
<th valign="top">
  <p>Message</p>
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

