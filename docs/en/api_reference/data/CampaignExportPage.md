# CampaignExportPage
CampaignExportPage object describes the export (download) URL with get results.

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
  <td colspan="8"><a href="./Page.md">Page</a>(inherited)</td>
 </tr>
 <tr>
  <td>totalNumEntries</td>
  <td>xsd:int</td>
  <td>Total number of entries in the result.</td>
  <td colspan="5"></td>
 </tr>
 <tr>
  <td>Page.Type</td>
  <td>xsd:string</td>
  <td>Subtype of Page of this instance.</td>
  <td colspan="5"></td>
 </tr>
 <tr>
  <td colspan="8">CampaignExportPage</td>
 </tr>
 <tr>
  <td>values[]</td>
  <td><a href="./CampaignExportValues.md">CampaignExportValues</a></td>
  <td>List of export (download) URL.<br>Each list includes export (download) URL with result of get process.</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
 </tr>
</table>

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
