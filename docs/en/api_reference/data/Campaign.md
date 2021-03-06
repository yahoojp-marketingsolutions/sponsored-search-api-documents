# Campaign
Campaign object describes Campaign information.

### Service
+ [CampaignService](../services/CampaignService.md)

<table>
 <tr>
  <th>Field</th>
  <th>Type</th>
  <th>Description</th>
  <th>response</th>
  <th>get</th>
  <th>add</th>
  <th>set</th>
  <th>remove</th>
 </tr>
 <tr>
  <td>accountId</td>
  <td>xsd:long</td>
  <td>Account ID.</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>campaignId</td>
  <td>xsd:long</td>
  <td>Campaign ID.</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>Requirement<br><i>NotUpdatable</i></td>
  <td>Requirement<br><i>NotUpdatable</i></td>
 </tr>
 <tr>
  <td>campaignTrackId</td>
  <td>xsd:long</td>
  <td>Campaign ID for tracking.<br>* "0" will return in Sandbox.</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>campaignName</td>
  <td>xsd:string</td>
  <td>Campaign name.<br>* Insert limit: Up to 50 characters.</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement</td>
  <td>Optional</td>
  <td>-</td>
 </tr>
 <tr>
  <td>userStatuses</td>
  <td>enum <a href="./UserStatus.md">UserStatus</a></td>
  <td>Status of ad display set by user.</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement</td>
  <td>Optional</td>
  <td>-</td>
 </tr>
 <tr>
  <td>servingStatus</td>
  <td>enum <a href="./CampaignServingStatus.md">CampaignServingStatus</a></td>
  <td>Status of display in Campaign level.<br>Return the campgin status regardless of display status set from user (userStatuses).</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
 </tr>
  <tr>
  <td>startDate</td>
  <td>xsd:string</td>
  <td>Start date of Campaign.<br>* Cannot set the past date.</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional<br>* Default: Current date.</td>
  <td>Optional</td>
  <td>-</td>
 </tr>
 <tr>
  <td>endDate</td>
  <td>xsd:string</td>
  <td>End date of Campaign.<br>* Cannot set the past date and date before the start date.</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional<br>* Default: 20371231</td>
  <td>Optional</td>
  <td>-</td>
 </tr>
 <tr>
  <td>budget</td>
  <td><a href="./Budget.md">Budget</a></td>
  <td>Budget of Campaign.</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement</td>
  <td>Optional</td>
  <td>-</td>
 </tr>
 <tr>
  <td>biddingStrategyConfiguration</td>
  <td><a href="./BiddingStrategy_Campaign.md">BiddingStrategy</a></td>
  <td>Bid setting.<br>* Cannot create or update the BudgetOptimizer (Only referring is available)<br>* If iOS is selected for App Campaign, cannot set "TARGET_CPA" or "TARGET_ROAS".</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement</td>
  <td>Optional</td>
  <td>-</td>
 </tr>
  <tr>
  <td>biddingStrategyFailedReason</td>
  <td>enum <a href="./BiddingStrategyFailedReason.md">BiddingStrategyFailedReason</a></td>
  <td>Reason of Auto Bidding set has failed.<br>* This field shows when setting has actually failed.</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>failedBiddingStrategyConfiguration</td>
  <td><a href="./BiddingStrategy_Campaign.md">BiddingStrategy</a></td>
  <td>Reason of Auto Bidding creation has failed.<br>* This field shows when setting has actually failed.</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>conversionOptimizerEligibility</td>
  <td>enum <a href="./ConversionOptimizerEligibility.md">ConversionOptimizerEligibility</a></td>
  <td>Determines if eligible to use Conversion Optimizer.</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>adServingOptimizationStatus</td>
  <td>enum <a href="./AdServingOptimizationStatus.md">AdServingOptimizationStatus</a></td>
  <td>Setting of Ad display optimization.</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional<br>* Default: OPTIMIZE</td>
  <td>Optional</td>
  <td>-</td>
 </tr>
  <tr>
  <td>settings</td>
  <td><a href="./Settings_Campaign.md">Settings</a><br>inherited <a href="./GeoTargetTypeSetting.md">GeoTargetTypeSetting</a></td>
  <td>Setting of target and matching.</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional<br>* Default: GeoTargetTypeSetting</td>
  <td>Optional</td>
  <td>-</td>
 </tr>
 <tr>
  <td>campaignType</td>
  <td>enum <a href="./CampaignType.md">CampaignType</a></td>
  <td>Type of Campaign.</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional<br>* Default: STANDARD</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>appStore</td>
  <td>enum <a href="./AppStore_Campaign.md">AppStore</a></td>
  <td>Selection of App store.</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement<br>* When the campaign type is Mobile App (MOBILE_APP)</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>appId</td>
  <td>xsd:string</td>
  <td>App ID (for iOS) or Package name (for Android).<br>*Input only the numbers for iOS in Mobile App Campaign.</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement<br>* When Campaign type is Mobile App (MOBILE_APP)</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>trackingUrl</td>
  <td>xsd:string</td>
  <td>Tracking URL.<br>* Cannot set if Mobile App Campaign is in Android.</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>Optional<br>* Cannot update during review.<br>*If there is no change on this field, it will not be reviewed.</td>
  <td>-</td>
 </tr>
 <tr>
  <td>customParameters</td>
  <td><a href="./CustomParameters.md">CustomParameters</a></td>
  <td>Custom Parameter.<br>* Cannot set if Mobile App Campaign is in Android.</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>Optional<br>* Cannot update when Tracking URL is in review.<br>*If there is no change on this field, it will not be reviewed.</td>
  <td>-</td>
 </tr>
 <tr>
  <td>urlReviewData</td>
  <td><a href="./UrlReviewData.md">UrlReviewData</a></td>
  <td>Review status of URL.</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
 </tr>
</table>

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
