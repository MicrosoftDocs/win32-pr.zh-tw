---
description: 有兩種方式可以決定要使用的診斷程式。
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: 使用 WSDAPI 進行疑難排解的開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12396ea656423772d35dbd4ca237c7c536dcdaf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192175"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a>使用 WSDAPI 進行疑難排解的開始使用

這份疑難排解指南包含一組 [診斷](wsdapi-diagnostic-procedures.md) 程式，可用來協助找出應用程式問題的原因。 一旦成功識別出問題的原因，就可以套用診斷程式中的建議解決方案，以便解決問題。

有兩種方式可以決定要使用的診斷程式。 其中一種方式是移至用戶端類型的 [疑難排解] 頁面，以查看用來對用戶端進行疑難排解的診斷程式逐步清單。 另一種方式是移至下方的疑難排解快速參考，以查看顯示 WSDAPI 應用程式常見問題的摘要資料表，以及用來診斷問題的程式。

## <a name="troubleshooting-by-type-of-client"></a>依用戶端類型進行疑難排解

下列主題依用戶端類型顯示相關的診斷程式。 這些主題也會顯示與用戶端類型相關聯的訊息模式。

-   [使用導向探索針對 WSDAPI 應用程式進行疑難排解](troubleshooting-applications-using-directed-discovery.md)
-   [針對函數探索用戶端進行疑難排解](troubleshooting-function-discovery-clients.md)
-   [疑難排解近端分享/會議近端分享](troubleshooting-people-near-me-meetings-near-me.md)
-   [針對新增印表機嚮導進行疑難排解](troubleshooting-the-add-printer-wizard.md)
-   [疑難排解網路總管](troubleshooting-the-network-explorer.md)
-   [針對投影機 Wizard 進行疑難排解](troubleshooting-the-projector-wizard.md)
-   [針對其他 WSDAPI 應用程式進行疑難排解](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a>疑難排解快速參考

下表顯示一些問題，可防止 WSDAPI 用戶端和主機在網路上看到彼此，以及交換裝置中繼資料。 這些表格也會顯示要執行的診斷程式，以及用來評估應用程式是否受到特定問題的準則。

### <a name="network-environment-problems"></a>網路環境問題



| 問題                                                                                                                                                                                              | 診斷程式                                                                                                                                                                                                                             | 問題識別                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 防火牆會封鎖網路探索流量。                                                                                                                                                       | [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | 啟用防火牆上的網路探索例外可解決問題。                                                                                                                      |
| 應用程式特定的防火牆例外狀況會封鎖訊息。                                                                                                                               | [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | 停用防火牆可解決問題。 WF 會顯示應用程式特定的防火牆規則。                                                                                                      |
| 裝置不會以及時的方式傳送 [ProbeMatches](probematches-message.md) 或 [ResolveMatches](resolvematches-message.md) 訊息， (小於4秒的) 來回應 UDP 要求。 | [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | 停用防火牆可解決此問題，而且在4秒內回應的一般主機會順利運作。                                                                            |
| 應用程式的安全性內容不正確 (亦即，用戶端和主機沒有網路) 的足夠許可權。                                                                 | [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md) ，或 [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md) | 裝置位址不會顯示在 WSD Debug 用戶端輸出中。 以系統管理員身分執行應用程式可解決問題。                                                                          |
| IPSec 原則正在封鎖訊息。                                                                                                                                                                | [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md) ，或 [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md) | 裝置位址不會顯示在 WSD Debug 用戶端輸出中。 停用防火牆無法解決此問題。 無法在不受任何 IPSec 原則的電腦上重現問題。 |



 

### <a name="discovery-traffic-problems"></a>探索流量問題



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>問題</th>
<th>診斷程式</th>
<th>問題識別</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>因為應用程式未正確列舉多播網路介面，所以不會在網路上傳輸<a href="hello-message.md">Hello</a>、<a href="probe-message.md">探查</a>或<a href="resolve-message.md">解析</a>訊息。</td>
<td><a href="using-wsddebug-client-to-verify-multicast-traffic.md">使用 WSD Debug 用戶端來驗證多播流量</a></td>
<td>Hello、探查或解析訊息不會出現在 WSD Debug 用戶端輸出中。 封包不會出現在網路上。 未針對回送介面或其他介面產生封包。</td>
</tr>
<tr class="even">
<td>針對未使用導向探索) 的應用程式，UDP 多播不會將<a href="probe-message.md">探查</a>訊息傳送到埠 3702 (。</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS-探索的網路追蹤</a></td>
<td>訊息的檢查顯示其已傳送至錯誤的埠。</td>
</tr>
<tr class="odd">
<td><a href="probe-message.md">探查</a>訊息未包含<strong>類型</strong>元素，或<strong>類型</strong>元素是空的。</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></td>
<td>訊息的檢查會顯示 <strong>類型</strong> 元素不存在或空白。</td>
</tr>
<tr class="even">
<td><a href="probe-message.md">探查</a>訊息的<strong>types</strong>元素不包含主機將回應的類型。</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></td>
<td>訊息的檢查會顯示 <strong>類型</strong> 元素包含格式錯誤或不正確的值。</td>
</tr>
<tr class="odd">
<td><a href="probematches-message.md">ProbeMatches</a>訊息未傳送單播給傳送<a href="probe-message.md">探查</a>的 UDP 埠。</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></td>
<td>檢查輸出會顯示未傳送任何 <a href="probematches-message.md">ProbeMatches</a>) 訊息，或訊息傳送至錯誤的埠。
<blockquote>
[!Note]<br />
針對使用導向探索的應用程式， <a href="probematches-message.md">ProbeMatches</a> 必須透過 HTTP 或 HTTPS 傳送以回應 <a href="probe-message.md">探查</a> 訊息。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="probematches-message.md">ProbeMatches</a>訊息未包含<strong>relatesto</strong>元素，或<strong>relatesto</strong>元素是空的。</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></td>
<td>訊息的檢查會顯示 <strong>RelatesTo</strong> 元素不存在或空白。</td>
</tr>
<tr class="odd">
<td><a href="probematches-message.md">ProbeMatches</a>訊息中的<strong>RelatesTo</strong>元素值與對應的<a href="probe-message.md">探查</a>訊息中的<strong>MessageId</strong>元素值不相符。</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></td>
<td>訊息的檢查會顯示 <strong>RelatesTo</strong> 元素包含格式錯誤或不正確的值。</td>
</tr>
<tr class="even">
<td><a href="probematches-message.md">ProbeMatches</a>訊息中包含的<strong>XAddrs</strong>元素不符合<a href="xaddr-validation-rules.md">XAddr 驗證規則</a>。</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></td>
<td>訊息的檢查會顯示 <strong>XAddrs</strong> 無效。</td>
</tr>
<tr class="odd">
<td>針對未使用導向探索) 的應用程式，UDP 多播不會將<a href="resolve-message.md">解決</a>訊息傳送到埠 3702 (。</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></td>
<td>檢查輸出會顯示 <a href="resolve-message.md">解析</a> 訊息已傳送至錯誤的埠。</td>
</tr>
<tr class="even">
<td><a href="resolvematches-message.md">ResolveMatches</a>訊息未傳送給傳送了<a href="resolve-message.md">解析</a>訊息的 UDP 通訊埠。</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></td>
<td>檢查輸出會顯示未傳送任何 <a href="resolvematches-message.md">ResolveMatches</a> 訊息，或訊息已傳送至錯誤的埠。</td>
</tr>
</tbody>
</table>



 

### <a name="metadata-exchange-problems"></a>中繼資料交換問題



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>問題</th>
<th>診斷程式</th>
<th>問題識別</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>主機所公告的傳輸位址錯誤。</td>
<td><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">使用泛型主機和用戶端進行 HTTP 中繼資料交換</a></td>
<td>在 WSD Debug 用戶端輸出中檢查 XAddrs，會顯示傳輸位址錯誤或格式不正確。</td>
</tr>
<tr class="even">
<td>無法建立中繼資料交換的 TCP 連接。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>封包分析器的輸出不會顯示下列封包交換：
<ul>
<li>從用戶端傳送的 TCP SYN 封包</li>
<li>從主機傳送的 TCP SYN/ACK 封包</li>
<li>從用戶端傳送的 TCP ACK 封包</li>
</ul></td>
</tr>
<tr class="odd">
<td>用戶端未傳送有效的 HTTP GET 要求。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>封包分析器輸出中沒有 HTTP GET 要求，或要求的格式不正確。</td>
</tr>
<tr class="even">
<td>用戶端未傳送有效的 WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">取得</a> 訊息。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>封包分析器輸出中沒有 WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">取得</a> 訊息，或訊息的格式不正確。</td>
</tr>
<tr class="odd">
<td>主機未接聽 HTTP GET 要求中指定的 URL 路徑。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>封包分析器輸出中沒有 HTTP 回應。</td>
</tr>
<tr class="even">
<td>WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> 訊息未包含 <strong>to</strong> 元素，或 <strong>to</strong> 專案是空的。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>訊息的檢查會顯示 <strong>To</strong> 元素不存在或空白。</td>
</tr>
<tr class="odd">
<td>WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a>訊息的<strong>To</strong>元素值不符合其中一個主機端點位址。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>訊息的檢查會顯示 <strong>To</strong> 專案的值不符合主機 <a href="probematches-message.md">ProbeMatches</a> 或 <a href="resolvematches-message.md">ResolveMatches</a> 訊息中通告的其中一個端點位址。</td>
</tr>
<tr class="even">
<td>主機未傳送有效的 HTTP 回應標頭。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>封包分析器輸出中沒有 HTTP 回應，或要求的格式不正確。</td>
</tr>
<tr class="odd">
<td>主機傳送的 HTTP 回應標頭表示無法完成要求。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>回應標頭具有 HTTP/1.1 200 以外的狀態碼。</td>
</tr>
<tr class="even">
<td>主機未傳送有效的 <a href="getresponse--metadata-exchange--message.md">GetResponse</a> 訊息。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>封包分析器輸出中沒有 <a href="getresponse--metadata-exchange--message.md">GetResponse</a> 訊息，或訊息的格式不正確。</td>
</tr>
<tr class="odd">
<td><a href="getresponse--metadata-exchange--message.md">GetResponse</a>訊息未包含<strong>relatesto</strong>元素，或<strong>relatesto</strong>元素是空的。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>訊息的檢查會顯示 <strong>RelatesTo</strong> 元素不存在或空白。</td>
</tr>
<tr class="even">
<td><a href="getresponse--metadata-exchange--message.md">GetResponse</a>訊息中的<strong>RelatesTo</strong>元素值與對應的<a href="get--metadata-exchange--http-request-and-message.md">Get</a>訊息中的<strong>MessageId</strong>元素值不相符。</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></td>
<td>訊息的檢查會顯示 <strong>RelatesTo</strong> 元素包含格式錯誤或不正確的值。</td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 疑難排解指南](wsdapi-troubleshooting-guide.md)
</dt> </dl>
