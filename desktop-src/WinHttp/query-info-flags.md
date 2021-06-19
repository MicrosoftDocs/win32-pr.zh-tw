---
description: WinHttpQueryHeaders 會使用這些屬性和修飾詞。
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: " (WinHTTP. h) 的查詢資訊旗標"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8a7f95f0e093f175901e4bed30f4055a04b8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396623"
---
# <a name="query-info-flags-winhttph"></a> (WinHTTP. h) 的查詢資訊旗標

[**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders)會使用這些屬性和修飾詞。

[**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders)會使用屬性旗標來指出要取出的資訊。 大部分的屬性旗標會直接對應至特定的 HTTP 標頭。 另外還有一些特殊旗標（例如 WINHTTP \_ 查詢 \_ 原始 \_ 標頭）與特定標頭無關。

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP \_ 查詢 \_ 接受**
</dt> <dd> <dl> <dt>



抓取回應可接受的媒體類型。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ 查詢 \_ 接受 \_ 字元集**
</dt> <dd> <dl> <dt>



捕獲回應的可接受字元集。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP \_ 查詢 \_ 接受 \_ 編碼**
</dt> <dd> <dl> <dt>



抓取回應可接受的內容編碼值。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP \_ 查詢 \_ 接受 \_ 語言**
</dt> <dd> <dl> <dt>



抓取回應的可接受自然語言。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP \_ 查詢 \_ 接受 \_ 範圍**
</dt> <dd> <dl> <dt>



抓取資源所接受範圍要求的類型。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP \_ 查詢 \_ 存留期**
</dt> <dd> <dl> <dt>



抓取 Age 回應標頭欄位，其中包含寄件者在源伺服器上產生回應以來的預估時間量。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP \_ 查詢 \_ 允許**
</dt> <dd> <dl> <dt>



接收伺服器所支援的 [**HTTP 動詞**](glossary.md) 命令。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP \_ 查詢 \_ 驗證 \_ 資訊**
</dt> <dd> <dl> <dt>



抓取 Authentication-Info 標頭。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP \_ 查詢 \_ 授權**
</dt> <dd> <dl> <dt>



抓取用於要求的授權認證。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP \_ 查詢快取 \_ \_ 控制**
</dt> <dd> <dl> <dt>



抓取快取控制指示詞。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP \_ 查詢 \_ 連接**
</dt> <dd> <dl> <dt>



抓取任何針對特定連接指定的選項，且不能透過其他連接的 proxy 進行通訊。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 基底**
</dt> <dd> <dl> <dt>



抓取基底統一資源識別項 (URI) 來解析實體內的相對 Url。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 描述**
</dt> <dd> <dl> <dt>



已過時。 針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 處置**
</dt> <dd> <dl> <dt>



已過時。 針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 編碼**
</dt> <dd> <dl> <dt>



抓取已套用至整個資源的其他內容編碼。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 識別碼**
</dt> <dd> <dl> <dt>



抓取內容識別。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 語言**
</dt> <dd> <dl> <dt>



抓取內容撰寫的語言。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 長度**
</dt> <dd> <dl> <dt>



抓取資源的大小（以位元組為單位）。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 位置**
</dt> <dd> <dl> <dt>



抓取訊息中所包含之實體的資源位置。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP \_ 查詢 \_ 內容 \_ MD5**
</dt> <dd> <dl> <dt>



針對提供實體主體端對端訊息完整性檢查的目的，抓取實體主體的 MD5 摘要。 如需詳細資訊，請參閱 [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt)。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 範圍**
</dt> <dd> <dl> <dt>



抓取完整實體主體中應插入部分實體內容的位置，以及完整實體主體的總大小。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 傳輸 \_ 編碼**
</dt> <dd> <dl> <dt>



捕獲適用于實體主體的編碼轉換。 它可能已經套用、可能需要套用，或可能會選擇性地套用。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 類型**
</dt> <dd> <dl> <dt>



接收資源的內容類型，例如文字或 html。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP \_ 查詢 \_ COOKIE**
</dt> <dd> <dl> <dt>



抓取任何與要求相關聯的 cookie。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP \_ 查詢 \_ 成本**
</dt> <dd> <dl> <dt>



不支援。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP \_ 查詢 \_ 自訂**
</dt> <dd> <dl> <dt>



使 [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) 搜尋 *pwszName* 參數中指定的標頭名稱，並將標頭資訊儲存在 *lpBuffer* 中。 應用程式可以使用 **WINHTTP \_ 選項 \_ 接收 \_ 回應 \_ 超時** ，來限制此查詢等候接收所有標頭的時間上限。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP \_ 查詢 \_ 日期**
</dt> <dd> <dl> <dt>



接收發出訊息的日期和時間。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_ \_ \_ 繼承自的 WINHTTP 查詢**
</dt> <dd> <dl> <dt>



不支援。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP \_ 查詢 \_ ETAG**
</dt> <dd> <dl> <dt>



抓取相關聯實體的實體標記。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP \_ 查詢 \_ 預期**
</dt> <dd> <dl> <dt>



抓取預期的標頭，指出用戶端應用程式是否應該預期100系列回應。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP \_ 查詢 \_ 過期**
</dt> <dd> <dl> <dt>



接收應將資源視為過期的日期和時間。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**轉送的 WINHTTP \_ 查詢 \_**
</dt> <dd> <dl> <dt>



已過時。 針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP \_ 查詢 \_ 來源**
</dt> <dd> <dl> <dt>



如果指定 From 標頭，則抓取控制提出要求之 [*使用者代理程式*](glossary.md) 之使用者的電子郵件地址。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP \_ 查詢 \_ 主機**
</dt> <dd> <dl> <dt>



抓取所要求資源的網際網路主機和埠號碼。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**符合的 WINHTTP \_ 查詢 \_ \_**
</dt> <dd> <dl> <dt>



抓取 If-Match 要求標頭欄位的內容。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_ \_ \_ \_ 自從之後修改的 WINHTTP 查詢**
</dt> <dd> <dl> <dt>



抓取已修改-自標頭的內容。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_ \_ 如果 \_ 沒有 \_ 相符的 WINHTTP 查詢**
</dt> <dd> <dl> <dt>



抓取 If-match 要求標頭欄位的內容。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP \_ 查詢 \_ \_ 範圍**
</dt> <dd> <dl> <dt>



抓取 If-Range 要求標頭欄位的內容。 此標頭可讓用戶端應用程式檢查與用戶端應用程式快取中實體部分複本相關的實體是否尚未更新。 如果實體尚未更新，請傳送缺少用戶端應用程式的元件。 如果實體已更新，請傳送整個更新的實體。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP \_ 查詢 \_ （ \_ \_ 自之後）**
</dt> <dd> <dl> <dt>



從要求標頭欄位開始，抓取（如果不修改）的內容。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP \_ 查詢 \_ 連結**
</dt> <dd> <dl> <dt>



已過時。 針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ 上次 \_ 修改的 WINHTTP 查詢**
</dt> <dd> <dl> <dt>



接收上次修改資源的日期和時間。 日期和時間是由伺服器決定。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP \_ 查詢 \_ 位置**
</dt> <dd> <dl> <dt>



抓取位置回應標頭中使用的絕對 URI。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP \_ 查詢 \_ 最大值**
</dt> <dd> <dl> <dt>



表示 WINHTTP 查詢值的最大 \_ 值 \_ \* 。 不是查詢旗標。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP \_ 查詢 \_ 最大 \_ 轉寄**
</dt> <dd> <dl> <dt>



抓取可將要求轉送至下一個輸入伺服器的 proxy 或閘道數目。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP \_ 查詢 \_ 訊息 \_ 識別碼**
</dt> <dd> <dl> <dt>



不支援。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP \_ 查詢 \_ MIME \_ 版本**
</dt> <dd> <dl> <dt>



接收用來建立訊息之多用途網際網路郵件延伸 (MIME) 通訊協定的版本。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP \_ 查詢 \_ TOASTPKG.ORIG \_ URI**
</dt> <dd> <dl> <dt>



已過時。 針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP \_ 查詢 \_ PRAGMA**
</dt> <dd> <dl> <dt>



接收可能會在要求/回應鏈中套用至任何收件者的特定執行指示詞。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP \_ 查詢 \_ PROXY \_ 驗證**
</dt> <dd> <dl> <dt>



抓取 proxy 傳回的驗證配置和領域。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP \_ 查詢 \_ PROXY \_ 授權**
</dt> <dd> <dl> <dt>



抓取用來將使用者識別為需要驗證之 proxy 的標頭。 只有在將要求傳送到伺服器之前，才能抓取此標頭。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP \_ 查詢 \_ PROXY \_ 連接**
</dt> <dd> <dl> <dt>



抓取 Proxy-Connection 標頭。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP \_ 查詢 \_ PROXY \_ 支援**
</dt> <dd> <dl> <dt>



抓取 Proxy-Support 標頭。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**公開的 WINHTTP \_ 查詢 \_**
</dt> <dd> <dl> <dt>



接收此伺服器提供的 HTTP 指令動詞。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP \_ 查詢 \_ 範圍**
</dt> <dd> <dl> <dt>



捕獲實體的位元組範圍。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP \_ 查詢 \_ 原始 \_ 標頭**
</dt> <dd> <dl> <dt>



接收伺服器傳回的所有標頭。 每個標頭都以 " \\ 0" 結束。 額外的 " \\ 0" 會終止標頭清單。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP \_ 查詢 \_ 原始 \_ 標頭 \_ CRLF**
</dt> <dd> <dl> <dt>



接收伺服器傳回的所有標頭。 每個標頭都會以換行字元（ (CR/LF) 序列）來分隔。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP \_ 查詢 \_ 推薦者**
</dt> <dd> <dl> <dt>



接收取得所要求 URI 之資源的 URI。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP \_ 查詢重新整理 \_**
</dt> <dd> <dl> <dt>



已過時。 針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP \_ 查詢 \_ 要求 \_ 方法**
</dt> <dd> <dl> <dt>



接收在要求中使用的 HTTP 動詞命令，通常是 GET 或 POST。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP \_ 查詢 \_ 之後重試 \_**
</dt> <dd> <dl> <dt>



捕獲服務預期無法使用的時間量。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP \_ 查詢 \_ 伺服器**
</dt> <dd> <dl> <dt>



抓取源伺服器用來處理要求之軟體的相關資訊。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP \_ 查詢 \_ 設定 \_ COOKIE**
</dt> <dd> <dl> <dt>



接收要求的 cookie 集合值。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP \_ 查詢 \_ 狀態 \_ 代碼**
</dt> <dd> <dl> <dt>



接收伺服器所傳回的狀態碼。 如需可能值的清單，請參閱 [**HTTP 狀態碼**](http-status-codes.md)。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP \_ 查詢 \_ 狀態 \_ 文字**
</dt> <dd> <dl> <dt>



接收回應行上伺服器所傳回的其他文字。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP \_ 查詢 \_ 標題**
</dt> <dd> <dl> <dt>



已過時。 針對舊版應用程式相容性進行維護。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP \_ 查詢 \_ 傳輸 \_ 編碼**
</dt> <dd> <dl> <dt>



抓取已套用至訊息主體的轉換類型，以便在傳送者與收件者之間安全地傳輸。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_ \_ 除非 \_ \_ 自從之後修改，否則 WINHTTP 查詢**
</dt> <dd> <dl> <dt>



抓取，除非修改-自標頭。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP \_ 查詢 \_ 升級**
</dt> <dd> <dl> <dt>



抓取伺服器所支援的其他通訊協定。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP \_ 查詢 \_ URI**
</dt> <dd> <dl> <dt>



接收可識別要求 URI 資源的部分或所有 URI。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP \_ 查詢 \_ 使用者 \_ 代理程式**
</dt> <dd> <dl> <dt>



抓取提出要求之使用者代理程式的相關資訊。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP \_ 查詢 \_ 不同**
</dt> <dd> <dl> <dt>



使用伺服器驅動的協商，抓取表示已從回應的許多可用表示中選取實體的標頭。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP \_ 查詢 \_ 版本**
</dt> <dd> <dl> <dt>



抓取存在於狀態行中的 HTTP 版本。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP \_ 查詢 \_ VIA**
</dt> <dd> <dl> <dt>



抓取使用者代理程式與伺服器上要求之間的中繼通訊協定和收件者，以及源伺服器與用戶端的回應之間的收件者。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP \_ 查詢 \_ 警告**
</dt> <dd> <dl> <dt>



抓取回應狀態碼可能不會反映之回應狀態的其他相關資訊。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP \_ 查詢 \_ WWW \_ 驗證**
</dt> <dd> <dl> <dt>



抓取伺服器傳回的驗證配置和領域。


</dt> </dl> </dd> </dl>

修飾詞旗標會與屬性旗標搭配使用，以修改要求。 修飾詞旗標可修改傳回的資料格式，或指出 [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) 函式應該搜尋資訊的位置。

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP \_ 查詢 \_ 旗標 \_ 編號**
</dt> <dd> <dl> <dt>



針對值為數字的標頭，以32位數位的形式傳回資料，例如狀態碼。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP \_ 查詢 \_ 旗 \_ \_ 標要求標頭**
</dt> <dd> <dl> <dt>



只查詢要求標頭。


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP \_ 查詢 \_ 旗標 \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>



傳回標頭值作為 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構，而不需要應用程式剖析資料。 用於其值為日期/時間字串的標頭，例如「上次修改時間」。


</dt> </dl> </dd> </dl>

<span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**WINHTTP \_ 查詢 \_ 旗標 \_ 尾端**
</dt> <dd> <dl> <dt>


查詢回應尾端。 在查詢回應尾端之前，您必須先呼叫 [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) ，直到它傳回0個位元組。


</dt> </dl> </dd> </dl>

<span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**WINHTTP \_ 查詢 \_ 旗標 \_ 網路 \_ 編碼**
</dt> <dd> <dl> <dt>


根據預設， [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) 會先執行 Unicode 轉換，再傳回所查詢的標頭。 如果設定此旗標，WinHttp 會將標頭傳回給呼叫端，而不會執行這項轉換。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]      |
| 最低支援的伺服器 | Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]   |
| 標頭                   | <dl> <dt>WinHTTP. h</dt> </dl> |

## <a name="see-also"></a>另請參閱

* [WinHTTP 版本](winhttp-versions.md)
