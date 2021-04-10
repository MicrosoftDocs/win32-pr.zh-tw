---
title: HTTP 伺服器 API 錯誤記錄檔的格式
description: 一般而言，HTTP 伺服器 API 錯誤記錄檔的格式與 W3C 錯誤記錄檔相同，不同之處在于 HTTP 伺服器 API 錯誤記錄檔不包含欄標題。
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- HTTP 伺服器 API，錯誤記錄檔格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2eb914251a809178adef28c8a61b1a174c6e86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183202"
---
# <a name="format-of-the-http-server-api-error-logs"></a><span data-ttu-id="b33c8-104">HTTP 伺服器 API 錯誤記錄檔的格式</span><span class="sxs-lookup"><span data-stu-id="b33c8-104">Format of the HTTP Server API Error Logs</span></span>

<span data-ttu-id="b33c8-105">一般而言，HTTP 伺服器 API 錯誤記錄檔的格式與 W3C 錯誤記錄檔相同，不同之處在于 HTTP 伺服器 API 錯誤記錄檔不包含欄標題。</span><span class="sxs-lookup"><span data-stu-id="b33c8-105">In general, HTTP Server API error log files have the same format as W3C error logs except that HTTP Server API error log files do not contain column headings.</span></span> <span data-ttu-id="b33c8-106">HTTP 伺服器 API 錯誤記錄檔中的每一行都會以特定順序來記錄欄位的一個錯誤。</span><span class="sxs-lookup"><span data-stu-id="b33c8-106">Each line of an HTTP Server API error log records one error with fields in a specific order.</span></span> <span data-ttu-id="b33c8-107">每個欄位都會以單一空白字元分隔 (0x0020) 。</span><span class="sxs-lookup"><span data-stu-id="b33c8-107">Each field is separated from the preceding field by a single space character (0x0020).</span></span> <span data-ttu-id="b33c8-108">在每個欄位中，空白字元、索引標籤和不可列印的控制字元會以加號取代 (0x002B) 。</span><span class="sxs-lookup"><span data-stu-id="b33c8-108">Within each field, space characters, tabs, and unprintable control characters are replaced by plus signs (0x002B).</span></span>

<span data-ttu-id="b33c8-109">下表會識別欄位以及錯誤記錄檔中欄位的順序。</span><span class="sxs-lookup"><span data-stu-id="b33c8-109">The following table identifies the fields and the order of the fields in an error log record.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b33c8-110">欄位</span><span class="sxs-lookup"><span data-stu-id="b33c8-110">Field</span></span></th>
<th><span data-ttu-id="b33c8-111">描述</span><span class="sxs-lookup"><span data-stu-id="b33c8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b33c8-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>日期</span><span class="sxs-lookup"><span data-stu-id="b33c8-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date</span></span><br/></td>
<td><span data-ttu-id="b33c8-113">日期欄位會遵循 W3C 格式，而且是以國際標準時間 (UTC) 為基礎。日期欄位一律為10個字元，格式為 &quot; yyyy-mm-dd &quot; 。</span><span class="sxs-lookup"><span data-stu-id="b33c8-113">The Date field follows the W3C format and is based on Coordinated Universal Time (UTC).The Date field is always 10 characters in the form of &quot;YYYY-MM-DD&quot;.</span></span> <span data-ttu-id="b33c8-114">例如，2003 5 月1日表示為 &quot; 2003-05-01 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="b33c8-114">For example, May 1, 2003 is expressed as &quot;2003-05-01&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b33c8-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>時間</span><span class="sxs-lookup"><span data-stu-id="b33c8-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Time</span></span><br/></td>
<td><span data-ttu-id="b33c8-116">時間欄位會遵循 W3C 格式，而且是以 UTC 為基礎。</span><span class="sxs-lookup"><span data-stu-id="b33c8-116">The Time field follows the W3C format and is based on UTC.</span></span> <span data-ttu-id="b33c8-117">Time 欄位一律是8個字元，格式為 &quot; MM： HH： SS &quot; 。</span><span class="sxs-lookup"><span data-stu-id="b33c8-117">The time field is always 8 characters in the form of &quot;MM:HH:SS&quot;.</span></span> <span data-ttu-id="b33c8-118">例如，5:30 PM (UTC) 會以17:30:00 表示 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="b33c8-118">For example, 5:30 PM (UTC) is expressed as &quot;17:30:00&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b33c8-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>用戶端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="b33c8-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client IP Address</span></span><br/></td>
<td><span data-ttu-id="b33c8-120">受影響用戶端的 IP 位址可以是 IPv4 位址或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="b33c8-120">The IP address of the affected client that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="b33c8-121">如果用戶端 IP 位址是 IPv6 位址，則 [ScopeId] 欄位也會包含在位址中。</span><span class="sxs-lookup"><span data-stu-id="b33c8-121">If the client IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b33c8-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>用戶端埠</span><span class="sxs-lookup"><span data-stu-id="b33c8-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Client Port</span></span><br/></td>
<td><span data-ttu-id="b33c8-123">受影響用戶端的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b33c8-123">The port number for the affected client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b33c8-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>伺服器 IP 位址</span><span class="sxs-lookup"><span data-stu-id="b33c8-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server IP Address</span></span><br/></td>
<td><span data-ttu-id="b33c8-125">受影響伺服器的 IP 位址可以是 IPv4 位址或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="b33c8-125">The IP address of the affected server that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="b33c8-126">如果伺服器 IP 位址是 IPv6 位址，則 [ScopeId] 欄位也會包含在位址中。</span><span class="sxs-lookup"><span data-stu-id="b33c8-126">If the server IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b33c8-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>伺服器埠</span><span class="sxs-lookup"><span data-stu-id="b33c8-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Server Port</span></span><br/></td>
<td><span data-ttu-id="b33c8-128">受影響之伺服器的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b33c8-128">The port number of the affected server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b33c8-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>通訊協定版本</span><span class="sxs-lookup"><span data-stu-id="b33c8-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protocol Version</span></span><br/></td>
<td><span data-ttu-id="b33c8-130">所使用的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="b33c8-130">The version of the protocol that is being used.</span></span> <br/>
<ul>
<li><span data-ttu-id="b33c8-131">如果連接未剖析足夠的來判斷通訊協定版本，則會使用連字號 (0x002D) 作為空白欄位的預留位置。</span><span class="sxs-lookup"><span data-stu-id="b33c8-131">If the connection has not been parsed enough to determine the protocol version, then a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
<li><span data-ttu-id="b33c8-132">如果剖析的主要或次要版本號碼大於或等於10，則會將版本記錄為 &quot; HTTP/?.? &quot; 。</span><span class="sxs-lookup"><span data-stu-id="b33c8-132">If either the major or minor version number parsed is greater than or equal to 10, the version is logged as &quot;HTTP/?.?&quot;.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b33c8-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>動詞</span><span class="sxs-lookup"><span data-stu-id="b33c8-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span><br/></td>
<td><span data-ttu-id="b33c8-134">上次剖析的要求所傳遞的動詞狀態。</span><span class="sxs-lookup"><span data-stu-id="b33c8-134">The verb state passed by the last request parsed.</span></span> <span data-ttu-id="b33c8-135">包含了未知的動詞，但超過255個位元組的任何動詞將會截斷為此長度。</span><span class="sxs-lookup"><span data-stu-id="b33c8-135">Unknown verbs are included, but any verb that is more than 255 bytes is truncated to this length.</span></span> <span data-ttu-id="b33c8-136">如果無法使用動詞，則會使用連字號 (0x002D) 作為空白欄位的預留位置。</span><span class="sxs-lookup"><span data-stu-id="b33c8-136">If a verb is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b33c8-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + 查詢</span><span class="sxs-lookup"><span data-stu-id="b33c8-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Query</span></span><br/></td>
<td><span data-ttu-id="b33c8-138">URL 和與其相關聯的任何查詢都會記錄為一個欄位，以問號分隔 (0x3F) 。</span><span class="sxs-lookup"><span data-stu-id="b33c8-138">The URL and any query associated with it are logged as one field, separated by a question mark (0x3F).</span></span> <span data-ttu-id="b33c8-139">此欄位的長度上限為4096個位元組。</span><span class="sxs-lookup"><span data-stu-id="b33c8-139">This field is truncated at its length limit of 4096 bytes.</span></span>
<ul>
<li><span data-ttu-id="b33c8-140">如果已將此 URL 剖析 (&quot; 處理後 &quot;) ，則會使用本機字碼頁轉換進行記錄，並將它視為 Unicode 欄位。</span><span class="sxs-lookup"><span data-stu-id="b33c8-140">If this URL has been parsed (&quot;cooked&quot;), it is logged with local code page conversion, and is treated as a Unicode field.</span></span></li>
<li><span data-ttu-id="b33c8-141">如果此 URL 尚未經過剖析 (&quot; 處理後 &quot; 在記錄時) ，則會完全複製，而不需要任何 Unicode 轉換。</span><span class="sxs-lookup"><span data-stu-id="b33c8-141">If this URL has not been parsed (&quot;cooked&quot;) at the time of logging, it is copied exactly, without any Unicode conversion.</span></span></li>
<li><span data-ttu-id="b33c8-142">如果 HTTP 伺服器 API 無法剖析此 URL，則會使用連字號 (0x002D) 作為空白欄位的預留位置。</span><span class="sxs-lookup"><span data-stu-id="b33c8-142">If the HTTP Server API cannot parse this URL, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b33c8-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>通訊協定狀態</span><span class="sxs-lookup"><span data-stu-id="b33c8-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protocol Status</span></span><br/></td>
<td><span data-ttu-id="b33c8-144">通訊協定狀態不能超過999。</span><span class="sxs-lookup"><span data-stu-id="b33c8-144">The protocol status cannot exceed 999.</span></span> <br/>
<ul>
<li><span data-ttu-id="b33c8-145">如果要求的回應的通訊協定狀態為 [可用]，則會記錄在此欄位中。</span><span class="sxs-lookup"><span data-stu-id="b33c8-145">If the protocol status of the response to a request is available, it is logged in this field.</span></span></li>
<li><span data-ttu-id="b33c8-146">如果無法使用通訊協定狀態，則會使用連字號 (0x002D) 作為空白欄位的預留位置。</span><span class="sxs-lookup"><span data-stu-id="b33c8-146">If the protocol status is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b33c8-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span><span class="sxs-lookup"><span data-stu-id="b33c8-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span></span><br/></td>
<td><span data-ttu-id="b33c8-148">未在此版本的 HTTP 伺服器 API 中使用。</span><span class="sxs-lookup"><span data-stu-id="b33c8-148">Not used in this version of the HTTP Server API.</span></span> <span data-ttu-id="b33c8-149">預留位置連字號 (0x002D) 一律會出現在此欄位中。</span><span class="sxs-lookup"><span data-stu-id="b33c8-149">A placeholder hyphen (0x002D) always appears in this field.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b33c8-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>原因片語</span><span class="sxs-lookup"><span data-stu-id="b33c8-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Reason Phrase</span></span><br/></td>
<td><span data-ttu-id="b33c8-151">此欄位包含可識別正在記錄之錯誤類型的字串。</span><span class="sxs-lookup"><span data-stu-id="b33c8-151">This field contains a string that identifies the kind of error that is being logged.</span></span> <span data-ttu-id="b33c8-152">絕不會保留空白。</span><span class="sxs-lookup"><span data-stu-id="b33c8-152">It is never left empty.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b33c8-153">下列範例程式碼來自 HTTP 伺服器 API 錯誤記錄檔：</span><span class="sxs-lookup"><span data-stu-id="b33c8-153">The following sample lines are from an HTTP Server API error log:</span></span>

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

 

 





