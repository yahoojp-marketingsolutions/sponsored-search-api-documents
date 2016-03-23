# ExportSetting
ExportSetting object describes the condition for exports.

### Service
+ [CampaignExportService](../services/CampaignExportService.md)

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
  <td>-</td>
  <td>-</td>
  <td>Requirement</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>campaignIds</td>
  <td>xsd:long</td>
  <td>Campaign ID of export objective.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>campaignCriterionIds</td>
  <td>xsd:long</td>
  <td>Campaign criteria ID.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>adGroupIds</td>
  <td>xsd:long</td>
  <td>Ad group ID of export objective.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>adIds</td>
  <td>xsd:long</td>
  <td>Ad ID of export objective.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>adGroupCriterionIds[0..2]</td>
  <td>enum <a href="./UserStatus.md">UserStatus</a></td>
  <td>Ad group criteria ID.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>campaignUserStatuses[0..2]</td>
  <td>enum <a href="./UserStatus.md">UserStatus</a></td>
  <td>Distribution status in campaign of export objective.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>adGroupUserStatuses[0..2]</td>
  <td>enum <a href="./UserStatus.md">UserStatus</a></td>
  <td>Distribution status in ad group of export objective.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>adGroupAdUserStatuses[0..2]</td>
  <td>enum <a href="./UserStatus.md">UserStatus</a></td>
  <td>Distribution status in ad of export objective.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>adGroupCriterionUserStatuses[0..2]</td>
  <td>enum <a href="./ApprovalStatus.md">ApprovalStatus</a></td>
  <td>Distribution status in ad group criteria of export objective.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>adGroupAdApprovalStatuses[]</td>
  <td>enum <a href="./ApprovalStatus.md">ApprovalStatus</a></td>
  <td>Status in ad approval of export objective.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>entityTypes</td>
  <td>enum <a href="./EntityType_CampaignExport.md">EntityType</a></td>
  <td>Entity type to download.</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>job</td>
  <td><a href="./Job.md">Job</a></td>
  <td>Job information for export.<br>*Default: NULL</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>lang</td>
  <td>enum <a href="./Lang.md">Lang</a></td>
  <td>Language setting for export.<br>*Default: JA</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>output</td>
  <td>enum <a href="./Output.md">Output</a></td>
  <td>Output format for export.</td>
  <td>-</td>
  <td>-</td>
  <td>Requirement</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>encoding</td>
  <td>enum <a href="./Encoding.md">Encoding</a></td>
  <td>Encoding setting of export.</td>
  <td>-</td>
  <td>-</td>
  <td>Requirement</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>advanced</td>
  <td>enum <a href="./Advanced.md">Advanced</a></td>
  <td>Select which object to export.<br>*Default: TRUE</td>
  <td>-</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
</table>

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
