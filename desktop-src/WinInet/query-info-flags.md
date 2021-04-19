---
title: '查詢資訊旗標 (Wininet. h) '
description: 下列清單包含 HttpQueryInfo 和 QueryInfo 所使用的屬性和修飾詞。
ms.assetid: b1613193-ae03-411e-bf05-de42f471cd8c
topic_type:
- apiref
api_name:
- HTTP_QUERY_ACCEPT
- HTTP_QUERY_ACCEPT_CHARSET
- HTTP_QUERY_ACCEPT_ENCODING
- HTTP_QUERY_ACCEPT_LANGUAGE
- HTTP_QUERY_ACCEPT_RANGES
- HTTP_QUERY_AGE
- HTTP_QUERY_ALLOW
- HTTP_QUERY_AUTHORIZATION
- HTTP_QUERY_CACHE_CONTROL
- HTTP_QUERY_CONNECTION
- HTTP_QUERY_CONTENT_BASE
- HTTP_QUERY_CONTENT_DESCRIPTION
- HTTP_QUERY_CONTENT_DISPOSITION
- HTTP_QUERY_CONTENT_ENCODING
- HTTP_QUERY_CONTENT_ID
- HTTP_QUERY_CONTENT_LANGUAGE
- HTTP_QUERY_CONTENT_LENGTH
- HTTP_QUERY_CONTENT_LOCATION
- HTTP_QUERY_CONTENT_MD5
- HTTP_QUERY_CONTENT_RANGE
- HTTP_QUERY_CONTENT_TRANSFER_ENCODING
- HTTP_QUERY_CONTENT_TYPE
- HTTP_QUERY_COOKIE
- HTTP_QUERY_COST
- HTTP_QUERY_CUSTOM
- HTTP_QUERY_DATE
- HTTP_QUERY_DERIVED_FROM
- HTTP_QUERY_ECHO_HEADERS
- HTTP_QUERY_ECHO_HEADERS_CRLF
- HTTP_QUERY_ECHO_REPLY
- HTTP_QUERY_ECHO_REQUEST
- HTTP_QUERY_ETAG
- HTTP_QUERY_EXPECT
- HTTP_QUERY_EXPIRES
- HTTP_QUERY_FORWARDED
- HTTP_QUERY_FROM
- HTTP_QUERY_HOST
- HTTP_QUERY_IF_MATCH
- HTTP_QUERY_IF_MODIFIED_SINCE
- HTTP_QUERY_IF_NONE_MATCH
- HTTP_QUERY_IF_RANGE
- HTTP_QUERY_IF_UNMODIFIED_SINCE
- HTTP_QUERY_LAST_MODIFIED
- HTTP_QUERY_LINK
- HTTP_QUERY_LOCATION
- HTTP_QUERY_MAX
- HTTP_QUERY_MAX_FORWARDS
- HTTP_QUERY_MESSAGE_ID
- HTTP_QUERY_MIME_VERSION
- HTTP_QUERY_ORIG_URI
- HTTP_QUERY_PRAGMA
- HTTP_QUERY_PROXY_AUTHENTICATE
- HTTP_QUERY_PROXY_AUTHORIZATION
- HTTP_QUERY_PROXY_CONNECTION
- HTTP_QUERY_PUBLIC
- HTTP_QUERY_RANGE
- HTTP_QUERY_RAW_HEADERS
- HTTP_QUERY_RAW_HEADERS_CRLF
- HTTP_QUERY_REFERER
- HTTP_QUERY_REFRESH
- HTTP_QUERY_REQUEST_METHOD
- HTTP_QUERY_RETRY_AFTER
- HTTP_QUERY_SERVER
- HTTP_QUERY_SET_COOKIE
- HTTP_QUERY_STATUS_CODE
- HTTP_QUERY_STATUS_TEXT
- HTTP_QUERY_TITLE
- HTTP_QUERY_TRANSFER_ENCODING
- HTTP_QUERY_UNLESS_MODIFIED_SINCE
- HTTP_QUERY_UPGRADE
- HTTP_QUERY_URI
- HTTP_QUERY_USER_AGENT
- HTTP_QUERY_VARY
- HTTP_QUERY_VERSION
- HTTP_QUERY_VIA
- HTTP_QUERY_WARNING
- HTTP_QUERY_WWW_AUTHENTICATE
- HTTP_QUERY_X_CONTENT_TYPE_OPTIONS
- HTTP_QUERY_P3P
- HTTP_QUERY_X_P2P_PEERDIST
- HTTP_QUERY_TRANSLATE
- HTTP_QUERY_X_UA_COMPATIBLE
- HTTP_QUERY_DEFAULT_STYLE
- HTTP_QUERY_X_FRAME_OPTIONS
- HTTP_QUERY_X_XSS_PROTECTION
- HTTP_QUERY_FLAG_COALESCE
- HTTP_QUERY_FLAG_NUMBER
- HTTP_QUERY_FLAG_REQUEST_HEADERS
- HTTP_QUERY_FLAG_SYSTEMTIME
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f3a6166c59e158d041e730d2198f6e1b066a8b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979696"
---
# <a name="query-info-flags-winineth"></a>查詢資訊旗標 (Wininet. h) 

下列清單包含 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 和 [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))所使用的屬性和修飾詞。

[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (或 [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) 使用屬性旗標來指出要取出的資料。 大部分的屬性旗標會直接對應至特定的 HTTP 標頭。 另外還有一些特殊旗標（例如 [HTTP \_ 查詢 \_ 原始 \_ 標頭](/windows)）與特定標頭無關。

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP \_ 查詢 \_ 接受**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



抓取回應可接受的媒體類型。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP \_ 查詢 \_ 接受 \_ 字元集**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



捕獲回應的可接受字元集。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP \_ 查詢 \_ 接受 \_ 編碼**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



抓取回應可接受的內容編碼值。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP \_ 查詢 \_ 接受 \_ 語言**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



抓取回應的可接受自然語言。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**HTTP \_ 查詢 \_ 接受 \_ 範圍**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



抓取資源所接受範圍要求的類型。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP \_ 查詢 \_ 存留期**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



抓取 Age 回應標頭欄位，其中包含寄件者在源伺服器上產生回應以來的預估時間量。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP \_ 查詢 \_ 允許**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



接收伺服器所支援的 HTTP 動詞命令。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP \_ 查詢 \_ 授權**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



抓取用於要求的授權認證。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP \_ 查詢快取 \_ \_ 控制**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



抓取快取控制指示詞。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP \_ 查詢 \_ 連接**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



抓取任何針對特定連接指定的選項，且不能透過其他連接的 proxy 進行通訊。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**HTTP \_ 查詢 \_ 內容 \_ 基底**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



抓取基底 URI， (統一資源識別項) 來解析實體內的相對 Url。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**HTTP \_ 查詢 \_ 內容 \_ 描述**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



已過時。 僅針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP \_ 查詢 \_ 內容 \_ 處置**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



已過時。 僅針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**HTTP \_ 查詢 \_ 內容 \_ 編碼**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



抓取已套用至整個資源的任何其他內容 codings。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**HTTP \_ 查詢 \_ 內容 \_ 識別碼**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



抓取內容識別。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**HTTP \_ 查詢 \_ 內容 \_ 語言**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



抓取內容所在的語言。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**HTTP \_ 查詢 \_ 內容 \_ 長度**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



抓取資源的大小（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**HTTP \_ 查詢 \_ 內容 \_ 位置**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



抓取訊息中所包含之實體的資源位置。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP \_ 查詢 \_ 內容 \_ MD5**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



抓取實體主體的 MD5 摘要，以提供實體主體 (MIC) 的端對端訊息完整性檢查。 如需詳細資訊，請參閱 RFC1864，內容-MD5 標頭欄位，位於 [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) 。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**HTTP \_ 查詢 \_ 內容 \_ 範圍**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



抓取完整實體主體中應插入部分實體內文的位置，以及完整實體主體的總大小。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**HTTP \_ 查詢 \_ 內容 \_ 傳輸 \_ 編碼**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



接收已套用至資源的其他內容編碼。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**HTTP \_ 查詢 \_ 內容 \_ 類型**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



接收資源 (的內容類型，例如 text/html) 。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP \_ 查詢 \_ COOKIE**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



抓取任何與要求相關聯的 cookie。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**HTTP \_ 查詢 \_ 成本**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



不再支援。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_ \_ 自訂 HTTP 查詢**
</dt> <dd> <dl> <dt>

65535
</dt> <dt>



使 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 搜尋 *lpvBuffer* 中指定的標頭名稱，並將標頭資料儲存在 *lpvBuffer* 中。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**HTTP \_ 查詢 \_ 日期**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



接收發出訊息的日期和時間。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_ \_ 衍生 \_ 自的 HTTP 查詢**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



不再支援。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**HTTP \_ 查詢 \_ 回應 \_ 標頭**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



目前未實作。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP \_ 查詢 \_ 回應 \_ 標頭 \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



目前未實作。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP \_ 查詢 \_ 回應 \_ 回復**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



目前未實作。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP \_ 查詢 \_ 回應 \_ 要求**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



目前未實作。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP \_ 查詢 \_ ETAG**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



抓取相關聯實體的實體標記。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP \_ 查詢 \_ 預期**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



抓取預期的標頭，指出用戶端應用程式是否應該預期100系列回應。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP \_ 查詢 \_ 過期**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



接收應將資源視為過期的日期和時間。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**轉送的 HTTP \_ 查詢 \_**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



已過時。 僅針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP \_ 查詢 \_ 來源**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



如果指定 From 標頭，則抓取控制提出要求之使用者代理程式的人類使用者的電子郵件地址。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP \_ 查詢 \_ 主機**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



抓取所要求資源的網際網路主機和埠號碼。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**符合的 HTTP \_ 查詢 \_ \_**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



抓取 If-Match 要求標頭欄位的內容。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**\_ \_ \_ 自從之後修改 HTTP \_ 查詢**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



抓取已修改-自標頭的內容。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**\_ \_ 如果 \_ 沒有 \_ 相符的 HTTP 查詢**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



抓取 If-match 要求標頭欄位的內容。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP \_ 查詢（ \_ 如果 \_ 範圍）**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



抓取 If-Range 要求標頭欄位的內容。 此標頭可讓用戶端應用程式確認與用戶端應用程式快取中實體部分複本相關的實體尚未更新。 如果實體尚未更新，請傳送缺少用戶端應用程式的元件。 如果實體已更新，請傳送整個更新的實體。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**未 \_ 修改的 HTTP 查詢（ \_ \_ \_ 自**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



從要求標頭欄位開始，抓取（如果不修改）的內容。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ 上次修改 HTTP \_ 查詢**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



接收伺服器認為資源上次修改的日期和時間。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP \_ 查詢 \_ 連結**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



已過時。 僅針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP \_ 查詢 \_ 位置**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



抓取在位置回應標頭中使用的絕對統一資源識別項 (URI) 。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP \_ 查詢 \_ 最大值**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



不是查詢旗標。 指出 HTTP 查詢值的最大 \_ 值 \_ \* 。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**HTTP \_ 查詢 \_ 最大 \_ 轉寄**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



抓取可將要求轉送至下一個輸入伺服器的 proxy 或閘道數目。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**HTTP \_ 查詢 \_ 訊息 \_ 識別碼**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



不再支援。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP \_ 查詢 \_ MIME \_ 版本**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



接收用來建立訊息的 MIME 通訊協定版本。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**HTTP \_ 查詢 \_ TOASTPKG.ORIG \_ URI**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



已過時。 僅針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP \_ 查詢 \_ PRAGMA**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



接收可能會在要求/回應鏈中套用至任何收件者的特定執行指示詞。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP \_ 查詢 \_ PROXY \_ 驗證**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



抓取 proxy 傳回的驗證配置和領域。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP \_ 查詢 \_ PROXY \_ 授權**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



抓取用來將使用者識別為需要驗證之 proxy 的標頭。 只有在將要求傳送到伺服器之前，才能抓取此標頭。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP \_ 查詢 \_ PROXY \_ 連接**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



抓取 Proxy-Connection 標頭。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**公用的 HTTP \_ 查詢 \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



接收此伺服器提供的方法。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP \_ 查詢 \_ 範圍**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



捕獲實體的位元組範圍。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**HTTP \_ 查詢 \_ 原始 \_ 標頭**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



接收伺服器傳回的所有標頭。 每個標頭都以 " \\ 0" 結束。 額外的 " \\ 0" 會終止標頭清單。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP \_ 查詢 \_ 原始 \_ 標頭 \_ CRLF**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



接收伺服器傳回的所有標頭。 每個標頭都會以換行字元（ (CR/LF) 序列）來分隔。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP \_ 查詢 \_ 推薦者**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



接收取得所要求 URI 之資源 (URI) 的統一資源識別項。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**HTTP \_ 查詢重新整理 \_**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



已過時。 僅針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP \_ 查詢 \_ 要求 \_ 方法**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



接收在要求中使用的 HTTP 動詞命令，通常是 GET 或 POST。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP \_ 查詢 \_ 之後重試 \_**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



捕獲服務預期無法使用的時間量。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP \_ 查詢 \_ 伺服器**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



抓取源伺服器用來處理要求之軟體的相關資料。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP \_ 查詢 \_ 設定 \_ COOKIE**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



接收要求的 cookie 集合值。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**HTTP \_ 查詢 \_ 狀態 \_ 代碼**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



接收伺服器所傳回的狀態碼。 如需詳細資訊和可能的值清單，請參閱 [**HTTP 狀態碼**](http-status-codes.md)。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**HTTP \_ 查詢 \_ 狀態 \_ 文字**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



接收回應行上伺服器傳回的任何其他文字。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP \_ 查詢 \_ 標題**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



已過時。 僅針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP \_ 查詢 \_ 傳輸 \_ 編碼**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



抓取已套用至訊息主體的轉換類型，以便在傳送者與收件者之間安全地傳輸。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP \_ 查詢 \_ （ \_ 除非 \_ 自從之後修改）**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



抓取，除非修改-自標頭。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**HTTP \_ 查詢 \_ 升級**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



抓取伺服器所支援的其他通訊協定。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP \_ 查詢 \_ URI**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



接收 (uri) 的部分或所有統一資源識別項，其可識別要求 URI 資源。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**HTTP \_ 查詢 \_ 使用者 \_ 代理程式**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



抓取提出要求之使用者代理程式的相關資料。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP \_ 查詢 \_ 不同**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



使用伺服器驅動的協商，抓取表示已從回應的許多可用表示中選取實體的標頭。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP \_ 查詢 \_ 版本**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



接收伺服器傳回的最後一個回應碼。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP \_ 查詢 \_ VIA**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



抓取使用者代理程式與伺服器上要求之間的中繼通訊協定和收件者，以及源伺服器與用戶端的回應之間的收件者。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP \_ 查詢 \_ 警告**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



抓取回應狀態碼可能不會反映之回應狀態的其他相關資料。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP \_ 查詢 \_ WWW \_ 驗證**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



抓取伺服器傳回的驗證配置和領域。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**HTTP \_ QUERY \_ X \_ 內容 \_ 類型 \_ 選項**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



抓取 X-Content-type 選項的標頭值。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP \_ 查詢 \_ P3P**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



抓取 P3P 標頭值。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP \_ 查詢 \_ X \_ P2P \_ PEERDIST**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



抓取 X-P2P-PeerDist 標頭值。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP \_ 查詢 \_ 轉譯**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



捕獲轉譯標頭值。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP \_ QUERY \_ X \_ UA \_ 相容**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



抓取 X-UA 相容的標頭值。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**HTTP \_ 查詢 \_ 預設 \_ 樣式**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



抓取 Default-Style 標頭值。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP \_ 查詢 \_ X \_ 畫面格 \_ 選項**
</dt> <dd> <dl> <dt>

85
</dt> <dt>



抓取 X 框架選項的標頭值。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP \_ 查詢 \_ X \_ XSS \_ 保護**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



抓取 X-XSS 保護標頭值。


</dt> </dl> </dd> </dl>

修飾詞旗標會與屬性旗標搭配使用，以修改要求。 修飾詞旗標可修改傳回的資料格式，或指出 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (或 [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) 應該搜尋資料的位置。

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP \_ 查詢 \_ 旗標 \_ 聯合**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



未實作。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP \_ 查詢 \_ 旗標 \_ 編號**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



針對值為數字的標頭，以32位數位的形式傳回資料，例如狀態碼。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP \_ 查詢 \_ 旗 \_ \_ 標要求標頭**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



只查詢要求標頭。


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP \_ 查詢 \_ 旗標 \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



傳回標頭值作為 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構，而不需要應用程式剖析資料。 用於其值為日期/時間字串的標頭，例如「上次修改時間」。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wininet</dt> </dl> |



 

