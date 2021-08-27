---
title: HTTP 伺服器 API 錯誤記錄檔的格式
description: 一般而言，HTTP 伺服器 API 錯誤記錄檔的格式與 W3C 錯誤記錄檔相同，不同之處在于 HTTP 伺服器 API 錯誤記錄檔不包含欄標題。
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- HTTP 伺服器 API，錯誤記錄檔格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e666e29178695482b05cfef6bdd252fb35072b7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477774"
---
# <a name="format-of-the-http-server-api-error-logs"></a>HTTP 伺服器 API 錯誤記錄檔的格式

一般而言，HTTP 伺服器 API 錯誤記錄檔的格式與 W3C 錯誤記錄檔相同，不同之處在于 HTTP 伺服器 API 錯誤記錄檔不包含欄標題。 HTTP 伺服器 API 錯誤記錄檔中的每一行都會以特定順序來記錄欄位的一個錯誤。 每個欄位都會以單一空白字元分隔 (0x0020) 。 在每個欄位中，空白字元、索引標籤和不可列印的控制字元會以加號取代 (0x002B) 。

下表會識別欄位以及錯誤記錄檔中欄位的順序。




| 欄位 | 描述 | 
|-------|-------------|
| <span id="Date"></span><span id="date"></span><span id="DATE"></span>日期<br /> | 日期欄位會遵循 W3C 格式，而且是以國際標準時間 (UTC) 為基礎。日期欄位一律為 "YYYY-MM-DD" 格式的10個字元。 例如，2003 5 月1日表示為 "2003-05-01"。<br /> | 
| <span id="Time"></span><span id="time"></span><span id="TIME"></span>時間<br /> | 時間欄位會遵循 W3C 格式，而且是以 UTC 為基礎。 Time 欄位一律為8個字元，格式為 "MM： HH： SS"。 例如，5:30 PM (UTC) 會表示為 "17:30:00"。<br /> | 
| <span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>用戶端 IP 位址<br /> | 受影響用戶端的 IP 位址可以是 IPv4 位址或 IPv6 位址。 如果用戶端 IP 位址是 IPv6 位址，則 [ScopeId] 欄位也會包含在位址中。<br /> | 
| <span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>用戶端埠<br /> | 受影響用戶端的埠號碼。<br /> | 
| <span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>伺服器 IP 位址<br /> | 受影響伺服器的 IP 位址可以是 IPv4 位址或 IPv6 位址。 如果伺服器 IP 位址是 IPv6 位址，則 [ScopeId] 欄位也會包含在位址中。<br /> | 
| <span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>伺服器埠<br /> | 受影響之伺服器的埠號碼。<br /> | 
| <span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>通訊協定版本<br /> | 所使用的通訊協定版本。 <br /><ul><li>如果連接未剖析足夠的來判斷通訊協定版本，則會使用連字號 (0x002D) 作為空白欄位的預留位置。</li><li>如果剖析的主要或次要版本號碼大於或等於10，則會將版本記錄為 "HTTP/?.?"。</li></ul> | 
| <span id="Verb"></span><span id="verb"></span><span id="VERB"></span>動詞<br /> | 上次剖析的要求所傳遞的動詞狀態。 包含了未知的動詞，但超過255個位元組的任何動詞將會截斷為此長度。 如果無法使用動詞，則會使用連字號 (0x002D) 作為空白欄位的預留位置。<br /> | 
| <span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + 查詢<br /> | URL 和與其相關聯的任何查詢都會記錄為一個欄位，以問號分隔 (0x3F) 。 此欄位的長度上限為4096個位元組。<ul><li>如果已將此 URL 剖析 ( "處理後" ) ，則會使用本機字碼頁轉換進行記錄，並將它視為 Unicode 欄位。</li><li>如果未將此 URL 剖析 ( "處理後" ) 在記錄時，它會完全複製，而不需要任何 Unicode 轉換。</li><li>如果 HTTP 伺服器 API 無法剖析此 URL，則會使用連字號 (0x002D) 作為空白欄位的預留位置。</li></ul><br /> | 
| <span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>通訊協定狀態<br /> | 通訊協定狀態不能超過999。 <br /><ul><li>如果要求的回應的通訊協定狀態為 [可用]，則會記錄在此欄位中。</li><li>如果無法使用通訊協定狀態，則會使用連字號 (0x002D) 作為空白欄位的預留位置。</li></ul> | 
| <span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId<br /> | 未在此版本的 HTTP 伺服器 API 中使用。 預留位置連字號 (0x002D) 一律會出現在此欄位中。<br /> | 
| <span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>原因片語<br /> | 此欄位包含可識別正在記錄之錯誤類型的字串。 絕不會保留空白。<br /> | 




 

下列範例程式碼來自 HTTP 伺服器 API 錯誤記錄檔：

``` syntax
2002-07-05 18:45:09 172.31.77.6 2094 172.31.77.6 80 
                    HTTP/1.1 GET /qos/1kbfile.txt 503 - ConnLimit
2002-07-05 19:51:59 127.0.0.1 2780 127.0.0.1 80 
                    HTTP/1.1 GET /ThisIsMyUrl.htm 400 - Hostname
2002-07-05 19:53:00 127.0.0.1 2894 127.0.0.1 80 
                    HTTP/2.0 GET / 505 - Version_N/S
2002-07-05 20:06:01 172.31.77.6 64388 127.0.0.1 80 
                    - - - - - Timer_MinBytesPerSecond
```

 

 





