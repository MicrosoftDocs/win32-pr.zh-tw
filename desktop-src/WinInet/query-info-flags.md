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
# <a name="query-info-flags-winineth"></a><span data-ttu-id="531dc-103">查詢資訊旗標 (Wininet. h) </span><span class="sxs-lookup"><span data-stu-id="531dc-103">Query Info Flags (Wininet.h)</span></span>

<span data-ttu-id="531dc-104">下列清單包含 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 和 [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))所使用的屬性和修飾詞。</span><span class="sxs-lookup"><span data-stu-id="531dc-104">The following lists contain the attributes and modifiers used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) and [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span></span>

<span data-ttu-id="531dc-105">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (或 [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) 使用屬性旗標來指出要取出的資料。</span><span class="sxs-lookup"><span data-stu-id="531dc-105">The attribute flags are used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) to indicate what data to retrieve.</span></span> <span data-ttu-id="531dc-106">大部分的屬性旗標會直接對應至特定的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="531dc-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="531dc-107">另外還有一些特殊旗標（例如 [HTTP \_ 查詢 \_ 原始 \_ 標頭](/windows)）與特定標頭無關。</span><span class="sxs-lookup"><span data-stu-id="531dc-107">There are also some special flags, such as [HTTP\_QUERY\_RAW\_HEADERS](/windows), that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="531dc-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP \_ 查詢 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="531dc-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-109">24</span><span class="sxs-lookup"><span data-stu-id="531dc-109">24</span></span>
</dt> <dt>



<span data-ttu-id="531dc-110">抓取回應可接受的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="531dc-110">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP \_ 查詢 \_ 接受 \_ 字元集**</span><span class="sxs-lookup"><span data-stu-id="531dc-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-112">25</span><span class="sxs-lookup"><span data-stu-id="531dc-112">25</span></span>
</dt> <dt>



<span data-ttu-id="531dc-113">捕獲回應的可接受字元集。</span><span class="sxs-lookup"><span data-stu-id="531dc-113">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP \_ 查詢 \_ 接受 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="531dc-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-115">26</span><span class="sxs-lookup"><span data-stu-id="531dc-115">26</span></span>
</dt> <dt>



<span data-ttu-id="531dc-116">抓取回應可接受的內容編碼值。</span><span class="sxs-lookup"><span data-stu-id="531dc-116">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP \_ 查詢 \_ 接受 \_ 語言**</span><span class="sxs-lookup"><span data-stu-id="531dc-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-118">27</span><span class="sxs-lookup"><span data-stu-id="531dc-118">27</span></span>
</dt> <dt>



<span data-ttu-id="531dc-119">抓取回應的可接受自然語言。</span><span class="sxs-lookup"><span data-stu-id="531dc-119">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**HTTP \_ 查詢 \_ 接受 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="531dc-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**HTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-121">42</span><span class="sxs-lookup"><span data-stu-id="531dc-121">42</span></span>
</dt> <dt>



<span data-ttu-id="531dc-122">抓取資源所接受範圍要求的類型。</span><span class="sxs-lookup"><span data-stu-id="531dc-122">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP \_ 查詢 \_ 存留期**</span><span class="sxs-lookup"><span data-stu-id="531dc-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-124">48</span><span class="sxs-lookup"><span data-stu-id="531dc-124">48</span></span>
</dt> <dt>



<span data-ttu-id="531dc-125">抓取 Age 回應標頭欄位，其中包含寄件者在源伺服器上產生回應以來的預估時間量。</span><span class="sxs-lookup"><span data-stu-id="531dc-125">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP \_ 查詢 \_ 允許**</span><span class="sxs-lookup"><span data-stu-id="531dc-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-127">7</span><span class="sxs-lookup"><span data-stu-id="531dc-127">7</span></span>
</dt> <dt>



<span data-ttu-id="531dc-128">接收伺服器所支援的 HTTP 動詞命令。</span><span class="sxs-lookup"><span data-stu-id="531dc-128">Receives the HTTP verbs supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP \_ 查詢 \_ 授權**</span><span class="sxs-lookup"><span data-stu-id="531dc-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-130">28</span><span class="sxs-lookup"><span data-stu-id="531dc-130">28</span></span>
</dt> <dt>



<span data-ttu-id="531dc-131">抓取用於要求的授權認證。</span><span class="sxs-lookup"><span data-stu-id="531dc-131">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP \_ 查詢快取 \_ \_ 控制**</span><span class="sxs-lookup"><span data-stu-id="531dc-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-133">49</span><span class="sxs-lookup"><span data-stu-id="531dc-133">49</span></span>
</dt> <dt>



<span data-ttu-id="531dc-134">抓取快取控制指示詞。</span><span class="sxs-lookup"><span data-stu-id="531dc-134">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP \_ 查詢 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="531dc-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-136">23</span><span class="sxs-lookup"><span data-stu-id="531dc-136">23</span></span>
</dt> <dt>



<span data-ttu-id="531dc-137">抓取任何針對特定連接指定的選項，且不能透過其他連接的 proxy 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="531dc-137">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**HTTP \_ 查詢 \_ 內容 \_ 基底**</span><span class="sxs-lookup"><span data-stu-id="531dc-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**HTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-139">50</span><span class="sxs-lookup"><span data-stu-id="531dc-139">50</span></span>
</dt> <dt>



<span data-ttu-id="531dc-140">抓取基底 URI， (統一資源識別項) 來解析實體內的相對 Url。</span><span class="sxs-lookup"><span data-stu-id="531dc-140">Retrieves the base URI (Uniform Resource Identifier) for resolving relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**HTTP \_ 查詢 \_ 內容 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="531dc-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**HTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-142">4</span><span class="sxs-lookup"><span data-stu-id="531dc-142">4</span></span>
</dt> <dt>



<span data-ttu-id="531dc-143">已過時。</span><span class="sxs-lookup"><span data-stu-id="531dc-143">Obsolete.</span></span> <span data-ttu-id="531dc-144">僅針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="531dc-144">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP \_ 查詢 \_ 內容 \_ 處置**</span><span class="sxs-lookup"><span data-stu-id="531dc-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-146">47</span><span class="sxs-lookup"><span data-stu-id="531dc-146">47</span></span>
</dt> <dt>



<span data-ttu-id="531dc-147">已過時。</span><span class="sxs-lookup"><span data-stu-id="531dc-147">Obsolete.</span></span> <span data-ttu-id="531dc-148">僅針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="531dc-148">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**HTTP \_ 查詢 \_ 內容 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="531dc-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**HTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-150">29</span><span class="sxs-lookup"><span data-stu-id="531dc-150">29</span></span>
</dt> <dt>



<span data-ttu-id="531dc-151">抓取已套用至整個資源的任何其他內容 codings。</span><span class="sxs-lookup"><span data-stu-id="531dc-151">Retrieves any additional content codings that have been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**HTTP \_ 查詢 \_ 內容 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="531dc-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**HTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-153">3</span><span class="sxs-lookup"><span data-stu-id="531dc-153">3</span></span>
</dt> <dt>



<span data-ttu-id="531dc-154">抓取內容識別。</span><span class="sxs-lookup"><span data-stu-id="531dc-154">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**HTTP \_ 查詢 \_ 內容 \_ 語言**</span><span class="sxs-lookup"><span data-stu-id="531dc-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**HTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-156">6</span><span class="sxs-lookup"><span data-stu-id="531dc-156">6</span></span>
</dt> <dt>



<span data-ttu-id="531dc-157">抓取內容所在的語言。</span><span class="sxs-lookup"><span data-stu-id="531dc-157">Retrieves the language that the content is in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**HTTP \_ 查詢 \_ 內容 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="531dc-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**HTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-159">5</span><span class="sxs-lookup"><span data-stu-id="531dc-159">5</span></span>
</dt> <dt>



<span data-ttu-id="531dc-160">抓取資源的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="531dc-160">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**HTTP \_ 查詢 \_ 內容 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="531dc-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**HTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-162">51</span><span class="sxs-lookup"><span data-stu-id="531dc-162">51</span></span>
</dt> <dt>



<span data-ttu-id="531dc-163">抓取訊息中所包含之實體的資源位置。</span><span class="sxs-lookup"><span data-stu-id="531dc-163">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP \_ 查詢 \_ 內容 \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="531dc-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-165">52</span><span class="sxs-lookup"><span data-stu-id="531dc-165">52</span></span>
</dt> <dt>



<span data-ttu-id="531dc-166">抓取實體主體的 MD5 摘要，以提供實體主體 (MIC) 的端對端訊息完整性檢查。</span><span class="sxs-lookup"><span data-stu-id="531dc-166">Retrieves an MD5 digest of the entity-body for the purpose of providing an end-to-end message integrity check (MIC) for the entity-body.</span></span> <span data-ttu-id="531dc-167">如需詳細資訊，請參閱 RFC1864，內容-MD5 標頭欄位，位於 [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) 。</span><span class="sxs-lookup"><span data-stu-id="531dc-167">For more information, see RFC1864, The Content-MD5 Header Field, at [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**HTTP \_ 查詢 \_ 內容 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="531dc-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**HTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-169">53</span><span class="sxs-lookup"><span data-stu-id="531dc-169">53</span></span>
</dt> <dt>



<span data-ttu-id="531dc-170">抓取完整實體主體中應插入部分實體內文的位置，以及完整實體主體的總大小。</span><span class="sxs-lookup"><span data-stu-id="531dc-170">Retrieves the location in the full entity-body where the partial entity-body should be inserted and the total size of the full entity-body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**HTTP \_ 查詢 \_ 內容 \_ 傳輸 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="531dc-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**HTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-172">2</span><span class="sxs-lookup"><span data-stu-id="531dc-172">2</span></span>
</dt> <dt>



<span data-ttu-id="531dc-173">接收已套用至資源的其他內容編碼。</span><span class="sxs-lookup"><span data-stu-id="531dc-173">Receives the additional content coding that has been applied to the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**HTTP \_ 查詢 \_ 內容 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="531dc-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**HTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-175">1</span><span class="sxs-lookup"><span data-stu-id="531dc-175">1</span></span>
</dt> <dt>



<span data-ttu-id="531dc-176">接收資源 (的內容類型，例如 text/html) 。</span><span class="sxs-lookup"><span data-stu-id="531dc-176">Receives the content type of the resource (such as text/html).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP \_ 查詢 \_ COOKIE**</span><span class="sxs-lookup"><span data-stu-id="531dc-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-178">44</span><span class="sxs-lookup"><span data-stu-id="531dc-178">44</span></span>
</dt> <dt>



<span data-ttu-id="531dc-179">抓取任何與要求相關聯的 cookie。</span><span class="sxs-lookup"><span data-stu-id="531dc-179">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**HTTP \_ 查詢 \_ 成本**</span><span class="sxs-lookup"><span data-stu-id="531dc-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**HTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-181">15</span><span class="sxs-lookup"><span data-stu-id="531dc-181">15</span></span>
</dt> <dt>



<span data-ttu-id="531dc-182">不再支援。</span><span class="sxs-lookup"><span data-stu-id="531dc-182">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_ \_ 自訂 HTTP 查詢**</span><span class="sxs-lookup"><span data-stu-id="531dc-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**HTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-184">65535</span><span class="sxs-lookup"><span data-stu-id="531dc-184">65535</span></span>
</dt> <dt>



<span data-ttu-id="531dc-185">使 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 搜尋 *lpvBuffer* 中指定的標頭名稱，並將標頭資料儲存在 *lpvBuffer* 中。</span><span class="sxs-lookup"><span data-stu-id="531dc-185">Causes [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to search for the header name specified in *lpvBuffer* and store the header data in *lpvBuffer*.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**HTTP \_ 查詢 \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="531dc-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**HTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-187">9</span><span class="sxs-lookup"><span data-stu-id="531dc-187">9</span></span>
</dt> <dt>



<span data-ttu-id="531dc-188">接收發出訊息的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="531dc-188">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_ \_ 衍生 \_ 自的 HTTP 查詢**</span><span class="sxs-lookup"><span data-stu-id="531dc-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**HTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-190">14</span><span class="sxs-lookup"><span data-stu-id="531dc-190">14</span></span>
</dt> <dt>



<span data-ttu-id="531dc-191">不再支援。</span><span class="sxs-lookup"><span data-stu-id="531dc-191">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**HTTP \_ 查詢 \_ 回應 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="531dc-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**HTTP\_QUERY\_ECHO\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-193">73</span><span class="sxs-lookup"><span data-stu-id="531dc-193">73</span></span>
</dt> <dt>



<span data-ttu-id="531dc-194">目前未實作。</span><span class="sxs-lookup"><span data-stu-id="531dc-194">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP \_ 查詢 \_ 回應 \_ 標頭 \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="531dc-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP\_QUERY\_ECHO\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-196">74</span><span class="sxs-lookup"><span data-stu-id="531dc-196">74</span></span>
</dt> <dt>



<span data-ttu-id="531dc-197">目前未實作。</span><span class="sxs-lookup"><span data-stu-id="531dc-197">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP \_ 查詢 \_ 回應 \_ 回復**</span><span class="sxs-lookup"><span data-stu-id="531dc-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP\_QUERY\_ECHO\_REPLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-199">72</span><span class="sxs-lookup"><span data-stu-id="531dc-199">72</span></span>
</dt> <dt>



<span data-ttu-id="531dc-200">目前未實作。</span><span class="sxs-lookup"><span data-stu-id="531dc-200">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP \_ 查詢 \_ 回應 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="531dc-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP\_QUERY\_ECHO\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-202">71</span><span class="sxs-lookup"><span data-stu-id="531dc-202">71</span></span>
</dt> <dt>



<span data-ttu-id="531dc-203">目前未實作。</span><span class="sxs-lookup"><span data-stu-id="531dc-203">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP \_ 查詢 \_ ETAG**</span><span class="sxs-lookup"><span data-stu-id="531dc-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-205">54</span><span class="sxs-lookup"><span data-stu-id="531dc-205">54</span></span>
</dt> <dt>



<span data-ttu-id="531dc-206">抓取相關聯實體的實體標記。</span><span class="sxs-lookup"><span data-stu-id="531dc-206">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP \_ 查詢 \_ 預期**</span><span class="sxs-lookup"><span data-stu-id="531dc-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-208">68</span><span class="sxs-lookup"><span data-stu-id="531dc-208">68</span></span>
</dt> <dt>



<span data-ttu-id="531dc-209">抓取預期的標頭，指出用戶端應用程式是否應該預期100系列回應。</span><span class="sxs-lookup"><span data-stu-id="531dc-209">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP \_ 查詢 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="531dc-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-211">10</span><span class="sxs-lookup"><span data-stu-id="531dc-211">10</span></span>
</dt> <dt>



<span data-ttu-id="531dc-212">接收應將資源視為過期的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="531dc-212">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**轉送的 HTTP \_ 查詢 \_**</span><span class="sxs-lookup"><span data-stu-id="531dc-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**HTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-214">30</span><span class="sxs-lookup"><span data-stu-id="531dc-214">30</span></span>
</dt> <dt>



<span data-ttu-id="531dc-215">已過時。</span><span class="sxs-lookup"><span data-stu-id="531dc-215">Obsolete.</span></span> <span data-ttu-id="531dc-216">僅針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="531dc-216">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP \_ 查詢 \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="531dc-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-218">31</span><span class="sxs-lookup"><span data-stu-id="531dc-218">31</span></span>
</dt> <dt>



<span data-ttu-id="531dc-219">如果指定 From 標頭，則抓取控制提出要求之使用者代理程式的人類使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="531dc-219">Retrieves the email address for the human user who controls the requesting user agent if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP \_ 查詢 \_ 主機**</span><span class="sxs-lookup"><span data-stu-id="531dc-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-221">55</span><span class="sxs-lookup"><span data-stu-id="531dc-221">55</span></span>
</dt> <dt>



<span data-ttu-id="531dc-222">抓取所要求資源的網際網路主機和埠號碼。</span><span class="sxs-lookup"><span data-stu-id="531dc-222">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**符合的 HTTP \_ 查詢 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="531dc-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-224">56</span><span class="sxs-lookup"><span data-stu-id="531dc-224">56</span></span>
</dt> <dt>



<span data-ttu-id="531dc-225">抓取 If-Match 要求標頭欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="531dc-225">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**\_ \_ \_ 自從之後修改 HTTP \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="531dc-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-227">32</span><span class="sxs-lookup"><span data-stu-id="531dc-227">32</span></span>
</dt> <dt>



<span data-ttu-id="531dc-228">抓取已修改-自標頭的內容。</span><span class="sxs-lookup"><span data-stu-id="531dc-228">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**\_ \_ 如果 \_ 沒有 \_ 相符的 HTTP 查詢**</span><span class="sxs-lookup"><span data-stu-id="531dc-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-230">57</span><span class="sxs-lookup"><span data-stu-id="531dc-230">57</span></span>
</dt> <dt>



<span data-ttu-id="531dc-231">抓取 If-match 要求標頭欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="531dc-231">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP \_ 查詢（ \_ 如果 \_ 範圍）**</span><span class="sxs-lookup"><span data-stu-id="531dc-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-233">58</span><span class="sxs-lookup"><span data-stu-id="531dc-233">58</span></span>
</dt> <dt>



<span data-ttu-id="531dc-234">抓取 If-Range 要求標頭欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="531dc-234">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="531dc-235">此標頭可讓用戶端應用程式確認與用戶端應用程式快取中實體部分複本相關的實體尚未更新。</span><span class="sxs-lookup"><span data-stu-id="531dc-235">This header enables the client application to verify that the entity related to a partial copy of the entity in the client application cache has not been updated.</span></span> <span data-ttu-id="531dc-236">如果實體尚未更新，請傳送缺少用戶端應用程式的元件。</span><span class="sxs-lookup"><span data-stu-id="531dc-236">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="531dc-237">如果實體已更新，請傳送整個更新的實體。</span><span class="sxs-lookup"><span data-stu-id="531dc-237">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**未 \_ 修改的 HTTP 查詢（ \_ \_ \_ 自**</span><span class="sxs-lookup"><span data-stu-id="531dc-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-239">59</span><span class="sxs-lookup"><span data-stu-id="531dc-239">59</span></span>
</dt> <dt>



<span data-ttu-id="531dc-240">從要求標頭欄位開始，抓取（如果不修改）的內容。</span><span class="sxs-lookup"><span data-stu-id="531dc-240">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ 上次修改 HTTP \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="531dc-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**HTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-242">11</span><span class="sxs-lookup"><span data-stu-id="531dc-242">11</span></span>
</dt> <dt>



<span data-ttu-id="531dc-243">接收伺服器認為資源上次修改的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="531dc-243">Receives the date and time at which the server believes the resource was last modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP \_ 查詢 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="531dc-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-245">16</span><span class="sxs-lookup"><span data-stu-id="531dc-245">16</span></span>
</dt> <dt>



<span data-ttu-id="531dc-246">已過時。</span><span class="sxs-lookup"><span data-stu-id="531dc-246">Obsolete.</span></span> <span data-ttu-id="531dc-247">僅針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="531dc-247">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP \_ 查詢 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="531dc-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-249">33</span><span class="sxs-lookup"><span data-stu-id="531dc-249">33</span></span>
</dt> <dt>



<span data-ttu-id="531dc-250">抓取在位置回應標頭中使用的絕對統一資源識別項 (URI) 。</span><span class="sxs-lookup"><span data-stu-id="531dc-250">Retrieves the absolute Uniform Resource Identifier (URI) used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP \_ 查詢 \_ 最大值**</span><span class="sxs-lookup"><span data-stu-id="531dc-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-252">78</span><span class="sxs-lookup"><span data-stu-id="531dc-252">78</span></span>
</dt> <dt>



<span data-ttu-id="531dc-253">不是查詢旗標。</span><span class="sxs-lookup"><span data-stu-id="531dc-253">Not a query flag.</span></span> <span data-ttu-id="531dc-254">指出 HTTP 查詢值的最大 \_ 值 \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="531dc-254">Indicates the maximum value of an HTTP\_QUERY\_\* value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**HTTP \_ 查詢 \_ 最大 \_ 轉寄**</span><span class="sxs-lookup"><span data-stu-id="531dc-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**HTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-256">60</span><span class="sxs-lookup"><span data-stu-id="531dc-256">60</span></span>
</dt> <dt>



<span data-ttu-id="531dc-257">抓取可將要求轉送至下一個輸入伺服器的 proxy 或閘道數目。</span><span class="sxs-lookup"><span data-stu-id="531dc-257">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**HTTP \_ 查詢 \_ 訊息 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="531dc-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**HTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-259">12</span><span class="sxs-lookup"><span data-stu-id="531dc-259">12</span></span>
</dt> <dt>



<span data-ttu-id="531dc-260">不再支援。</span><span class="sxs-lookup"><span data-stu-id="531dc-260">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP \_ 查詢 \_ MIME \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="531dc-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-262">0</span><span class="sxs-lookup"><span data-stu-id="531dc-262">0</span></span>
</dt> <dt>



<span data-ttu-id="531dc-263">接收用來建立訊息的 MIME 通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="531dc-263">Receives the version of the MIME protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**HTTP \_ 查詢 \_ TOASTPKG.ORIG \_ URI**</span><span class="sxs-lookup"><span data-stu-id="531dc-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**HTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-265">34</span><span class="sxs-lookup"><span data-stu-id="531dc-265">34</span></span>
</dt> <dt>



<span data-ttu-id="531dc-266">已過時。</span><span class="sxs-lookup"><span data-stu-id="531dc-266">Obsolete.</span></span> <span data-ttu-id="531dc-267">僅針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="531dc-267">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP \_ 查詢 \_ PRAGMA**</span><span class="sxs-lookup"><span data-stu-id="531dc-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-269">17</span><span class="sxs-lookup"><span data-stu-id="531dc-269">17</span></span>
</dt> <dt>



<span data-ttu-id="531dc-270">接收可能會在要求/回應鏈中套用至任何收件者的特定執行指示詞。</span><span class="sxs-lookup"><span data-stu-id="531dc-270">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP \_ 查詢 \_ PROXY \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="531dc-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-272">41</span><span class="sxs-lookup"><span data-stu-id="531dc-272">41</span></span>
</dt> <dt>



<span data-ttu-id="531dc-273">抓取 proxy 傳回的驗證配置和領域。</span><span class="sxs-lookup"><span data-stu-id="531dc-273">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP \_ 查詢 \_ PROXY \_ 授權**</span><span class="sxs-lookup"><span data-stu-id="531dc-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-275">61</span><span class="sxs-lookup"><span data-stu-id="531dc-275">61</span></span>
</dt> <dt>



<span data-ttu-id="531dc-276">抓取用來將使用者識別為需要驗證之 proxy 的標頭。</span><span class="sxs-lookup"><span data-stu-id="531dc-276">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="531dc-277">只有在將要求傳送到伺服器之前，才能抓取此標頭。</span><span class="sxs-lookup"><span data-stu-id="531dc-277">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP \_ 查詢 \_ PROXY \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="531dc-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-279">69</span><span class="sxs-lookup"><span data-stu-id="531dc-279">69</span></span>
</dt> <dt>



<span data-ttu-id="531dc-280">抓取 Proxy-Connection 標頭。</span><span class="sxs-lookup"><span data-stu-id="531dc-280">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**公用的 HTTP \_ 查詢 \_**</span><span class="sxs-lookup"><span data-stu-id="531dc-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**HTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-282">8</span><span class="sxs-lookup"><span data-stu-id="531dc-282">8</span></span>
</dt> <dt>



<span data-ttu-id="531dc-283">接收此伺服器提供的方法。</span><span class="sxs-lookup"><span data-stu-id="531dc-283">Receives methods available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP \_ 查詢 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="531dc-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-285">62</span><span class="sxs-lookup"><span data-stu-id="531dc-285">62</span></span>
</dt> <dt>



<span data-ttu-id="531dc-286">捕獲實體的位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="531dc-286">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**HTTP \_ 查詢 \_ 原始 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="531dc-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**HTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-288">21</span><span class="sxs-lookup"><span data-stu-id="531dc-288">21</span></span>
</dt> <dt>



<span data-ttu-id="531dc-289">接收伺服器傳回的所有標頭。</span><span class="sxs-lookup"><span data-stu-id="531dc-289">Receives all the headers returned by the server.</span></span> <span data-ttu-id="531dc-290">每個標頭都以 " \\ 0" 結束。</span><span class="sxs-lookup"><span data-stu-id="531dc-290">Each header is terminated by "\\0".</span></span> <span data-ttu-id="531dc-291">額外的 " \\ 0" 會終止標頭清單。</span><span class="sxs-lookup"><span data-stu-id="531dc-291">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP \_ 查詢 \_ 原始 \_ 標頭 \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="531dc-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-293">22</span><span class="sxs-lookup"><span data-stu-id="531dc-293">22</span></span>
</dt> <dt>



<span data-ttu-id="531dc-294">接收伺服器傳回的所有標頭。</span><span class="sxs-lookup"><span data-stu-id="531dc-294">Receives all the headers returned by the server.</span></span> <span data-ttu-id="531dc-295">每個標頭都會以換行字元（ (CR/LF) 序列）來分隔。</span><span class="sxs-lookup"><span data-stu-id="531dc-295">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP \_ 查詢 \_ 推薦者**</span><span class="sxs-lookup"><span data-stu-id="531dc-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-297">35</span><span class="sxs-lookup"><span data-stu-id="531dc-297">35</span></span>
</dt> <dt>



<span data-ttu-id="531dc-298">接收取得所要求 URI 之資源 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="531dc-298">Receives the Uniform Resource Identifier (URI) of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**HTTP \_ 查詢重新整理 \_**</span><span class="sxs-lookup"><span data-stu-id="531dc-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**HTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-300">46</span><span class="sxs-lookup"><span data-stu-id="531dc-300">46</span></span>
</dt> <dt>



<span data-ttu-id="531dc-301">已過時。</span><span class="sxs-lookup"><span data-stu-id="531dc-301">Obsolete.</span></span> <span data-ttu-id="531dc-302">僅針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="531dc-302">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP \_ 查詢 \_ 要求 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="531dc-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-304">45</span><span class="sxs-lookup"><span data-stu-id="531dc-304">45</span></span>
</dt> <dt>



<span data-ttu-id="531dc-305">接收在要求中使用的 HTTP 動詞命令，通常是 GET 或 POST。</span><span class="sxs-lookup"><span data-stu-id="531dc-305">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP \_ 查詢 \_ 之後重試 \_**</span><span class="sxs-lookup"><span data-stu-id="531dc-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-307">36</span><span class="sxs-lookup"><span data-stu-id="531dc-307">36</span></span>
</dt> <dt>



<span data-ttu-id="531dc-308">捕獲服務預期無法使用的時間量。</span><span class="sxs-lookup"><span data-stu-id="531dc-308">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP \_ 查詢 \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="531dc-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-310">37</span><span class="sxs-lookup"><span data-stu-id="531dc-310">37</span></span>
</dt> <dt>



<span data-ttu-id="531dc-311">抓取源伺服器用來處理要求之軟體的相關資料。</span><span class="sxs-lookup"><span data-stu-id="531dc-311">Retrieves data about the software used by the origin server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP \_ 查詢 \_ 設定 \_ COOKIE**</span><span class="sxs-lookup"><span data-stu-id="531dc-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-313">43</span><span class="sxs-lookup"><span data-stu-id="531dc-313">43</span></span>
</dt> <dt>



<span data-ttu-id="531dc-314">接收要求的 cookie 集合值。</span><span class="sxs-lookup"><span data-stu-id="531dc-314">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**HTTP \_ 查詢 \_ 狀態 \_ 代碼**</span><span class="sxs-lookup"><span data-stu-id="531dc-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**HTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-316">19</span><span class="sxs-lookup"><span data-stu-id="531dc-316">19</span></span>
</dt> <dt>



<span data-ttu-id="531dc-317">接收伺服器所傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="531dc-317">Receives the status code returned by the server.</span></span> <span data-ttu-id="531dc-318">如需詳細資訊和可能的值清單，請參閱 [**HTTP 狀態碼**](http-status-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="531dc-318">For more information and a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**HTTP \_ 查詢 \_ 狀態 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="531dc-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**HTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-320">20</span><span class="sxs-lookup"><span data-stu-id="531dc-320">20</span></span>
</dt> <dt>



<span data-ttu-id="531dc-321">接收回應行上伺服器傳回的任何其他文字。</span><span class="sxs-lookup"><span data-stu-id="531dc-321">Receives any additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP \_ 查詢 \_ 標題**</span><span class="sxs-lookup"><span data-stu-id="531dc-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-323">38</span><span class="sxs-lookup"><span data-stu-id="531dc-323">38</span></span>
</dt> <dt>



<span data-ttu-id="531dc-324">已過時。</span><span class="sxs-lookup"><span data-stu-id="531dc-324">Obsolete.</span></span> <span data-ttu-id="531dc-325">僅針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="531dc-325">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP \_ 查詢 \_ 傳輸 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="531dc-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-327">63</span><span class="sxs-lookup"><span data-stu-id="531dc-327">63</span></span>
</dt> <dt>



<span data-ttu-id="531dc-328">抓取已套用至訊息主體的轉換類型，以便在傳送者與收件者之間安全地傳輸。</span><span class="sxs-lookup"><span data-stu-id="531dc-328">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP \_ 查詢 \_ （ \_ 除非 \_ 自從之後修改）**</span><span class="sxs-lookup"><span data-stu-id="531dc-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-330">70</span><span class="sxs-lookup"><span data-stu-id="531dc-330">70</span></span>
</dt> <dt>



<span data-ttu-id="531dc-331">抓取，除非修改-自標頭。</span><span class="sxs-lookup"><span data-stu-id="531dc-331">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**HTTP \_ 查詢 \_ 升級**</span><span class="sxs-lookup"><span data-stu-id="531dc-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**HTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-333">64</span><span class="sxs-lookup"><span data-stu-id="531dc-333">64</span></span>
</dt> <dt>



<span data-ttu-id="531dc-334">抓取伺服器所支援的其他通訊協定。</span><span class="sxs-lookup"><span data-stu-id="531dc-334">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP \_ 查詢 \_ URI**</span><span class="sxs-lookup"><span data-stu-id="531dc-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-336">13</span><span class="sxs-lookup"><span data-stu-id="531dc-336">13</span></span>
</dt> <dt>



<span data-ttu-id="531dc-337">接收 (uri) 的部分或所有統一資源識別項，其可識別要求 URI 資源。</span><span class="sxs-lookup"><span data-stu-id="531dc-337">Receives some or all of the Uniform Resource Identifiers (URIs) by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**HTTP \_ 查詢 \_ 使用者 \_ 代理程式**</span><span class="sxs-lookup"><span data-stu-id="531dc-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**HTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-339">39</span><span class="sxs-lookup"><span data-stu-id="531dc-339">39</span></span>
</dt> <dt>



<span data-ttu-id="531dc-340">抓取提出要求之使用者代理程式的相關資料。</span><span class="sxs-lookup"><span data-stu-id="531dc-340">Retrieves data about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP \_ 查詢 \_ 不同**</span><span class="sxs-lookup"><span data-stu-id="531dc-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-342">65</span><span class="sxs-lookup"><span data-stu-id="531dc-342">65</span></span>
</dt> <dt>



<span data-ttu-id="531dc-343">使用伺服器驅動的協商，抓取表示已從回應的許多可用表示中選取實體的標頭。</span><span class="sxs-lookup"><span data-stu-id="531dc-343">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP \_ 查詢 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="531dc-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-345">18</span><span class="sxs-lookup"><span data-stu-id="531dc-345">18</span></span>
</dt> <dt>



<span data-ttu-id="531dc-346">接收伺服器傳回的最後一個回應碼。</span><span class="sxs-lookup"><span data-stu-id="531dc-346">Receives the last response code returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP \_ 查詢 \_ VIA**</span><span class="sxs-lookup"><span data-stu-id="531dc-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-348">66</span><span class="sxs-lookup"><span data-stu-id="531dc-348">66</span></span>
</dt> <dt>



<span data-ttu-id="531dc-349">抓取使用者代理程式與伺服器上要求之間的中繼通訊協定和收件者，以及源伺服器與用戶端的回應之間的收件者。</span><span class="sxs-lookup"><span data-stu-id="531dc-349">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP \_ 查詢 \_ 警告**</span><span class="sxs-lookup"><span data-stu-id="531dc-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-351">67</span><span class="sxs-lookup"><span data-stu-id="531dc-351">67</span></span>
</dt> <dt>



<span data-ttu-id="531dc-352">抓取回應狀態碼可能不會反映之回應狀態的其他相關資料。</span><span class="sxs-lookup"><span data-stu-id="531dc-352">Retrieves additional data about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP \_ 查詢 \_ WWW \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="531dc-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-354">40</span><span class="sxs-lookup"><span data-stu-id="531dc-354">40</span></span>
</dt> <dt>



<span data-ttu-id="531dc-355">抓取伺服器傳回的驗證配置和領域。</span><span class="sxs-lookup"><span data-stu-id="531dc-355">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**HTTP \_ QUERY \_ X \_ 內容 \_ 類型 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="531dc-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**HTTP\_QUERY\_X\_CONTENT\_TYPE\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-357">79</span><span class="sxs-lookup"><span data-stu-id="531dc-357">79</span></span>
</dt> <dt>



<span data-ttu-id="531dc-358">抓取 X-Content-type 選項的標頭值。</span><span class="sxs-lookup"><span data-stu-id="531dc-358">Retrieves the X-Content-Type-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP \_ 查詢 \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="531dc-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP\_QUERY\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-360">80</span><span class="sxs-lookup"><span data-stu-id="531dc-360">80</span></span>
</dt> <dt>



<span data-ttu-id="531dc-361">抓取 P3P 標頭值。</span><span class="sxs-lookup"><span data-stu-id="531dc-361">Retrieves the P3P header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP \_ 查詢 \_ X \_ P2P \_ PEERDIST**</span><span class="sxs-lookup"><span data-stu-id="531dc-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP\_QUERY\_X\_P2P\_PEERDIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-363">81</span><span class="sxs-lookup"><span data-stu-id="531dc-363">81</span></span>
</dt> <dt>



<span data-ttu-id="531dc-364">抓取 X-P2P-PeerDist 標頭值。</span><span class="sxs-lookup"><span data-stu-id="531dc-364">Retrieves the X-P2P-PeerDist header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP \_ 查詢 \_ 轉譯**</span><span class="sxs-lookup"><span data-stu-id="531dc-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP\_QUERY\_TRANSLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-366">82</span><span class="sxs-lookup"><span data-stu-id="531dc-366">82</span></span>
</dt> <dt>



<span data-ttu-id="531dc-367">捕獲轉譯標頭值。</span><span class="sxs-lookup"><span data-stu-id="531dc-367">Retrieves the translate header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP \_ QUERY \_ X \_ UA \_ 相容**</span><span class="sxs-lookup"><span data-stu-id="531dc-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP\_QUERY\_X\_UA\_COMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-369">83</span><span class="sxs-lookup"><span data-stu-id="531dc-369">83</span></span>
</dt> <dt>



<span data-ttu-id="531dc-370">抓取 X-UA 相容的標頭值。</span><span class="sxs-lookup"><span data-stu-id="531dc-370">Retrieves the X-UA-Compatible header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**HTTP \_ 查詢 \_ 預設 \_ 樣式**</span><span class="sxs-lookup"><span data-stu-id="531dc-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**HTTP\_QUERY\_DEFAULT\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-372">84</span><span class="sxs-lookup"><span data-stu-id="531dc-372">84</span></span>
</dt> <dt>



<span data-ttu-id="531dc-373">抓取 Default-Style 標頭值。</span><span class="sxs-lookup"><span data-stu-id="531dc-373">Retrieves the Default-Style header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP \_ 查詢 \_ X \_ 畫面格 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="531dc-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP\_QUERY\_X\_FRAME\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-375">85</span><span class="sxs-lookup"><span data-stu-id="531dc-375">85</span></span>
</dt> <dt>



<span data-ttu-id="531dc-376">抓取 X 框架選項的標頭值。</span><span class="sxs-lookup"><span data-stu-id="531dc-376">Retrieves the X-Frame-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP \_ 查詢 \_ X \_ XSS \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="531dc-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP\_QUERY\_X\_XSS\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-378">86</span><span class="sxs-lookup"><span data-stu-id="531dc-378">86</span></span>
</dt> <dt>



<span data-ttu-id="531dc-379">抓取 X-XSS 保護標頭值。</span><span class="sxs-lookup"><span data-stu-id="531dc-379">Retrieves the X-XSS-Protection header value.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="531dc-380">修飾詞旗標會與屬性旗標搭配使用，以修改要求。</span><span class="sxs-lookup"><span data-stu-id="531dc-380">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="531dc-381">修飾詞旗標可修改傳回的資料格式，或指出 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (或 [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) 應該搜尋資料的位置。</span><span class="sxs-lookup"><span data-stu-id="531dc-381">Modifier flags either modify the format of the data returned or indicate where [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) should search for the data.</span></span>

<dl> <dt>

<span data-ttu-id="531dc-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP \_ 查詢 \_ 旗標 \_ 聯合**</span><span class="sxs-lookup"><span data-stu-id="531dc-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP\_QUERY\_FLAG\_COALESCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-383">0x10000000</span><span class="sxs-lookup"><span data-stu-id="531dc-383">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="531dc-384">未實作。</span><span class="sxs-lookup"><span data-stu-id="531dc-384">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP \_ 查詢 \_ 旗標 \_ 編號**</span><span class="sxs-lookup"><span data-stu-id="531dc-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-386">0x20000000</span><span class="sxs-lookup"><span data-stu-id="531dc-386">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="531dc-387">針對值為數字的標頭，以32位數位的形式傳回資料，例如狀態碼。</span><span class="sxs-lookup"><span data-stu-id="531dc-387">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP \_ 查詢 \_ 旗 \_ \_ 標要求標頭**</span><span class="sxs-lookup"><span data-stu-id="531dc-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-389">0x80000000</span><span class="sxs-lookup"><span data-stu-id="531dc-389">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="531dc-390">只查詢要求標頭。</span><span class="sxs-lookup"><span data-stu-id="531dc-390">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="531dc-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP \_ 查詢 \_ 旗標 \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="531dc-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="531dc-392">0x40000000</span><span class="sxs-lookup"><span data-stu-id="531dc-392">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="531dc-393">傳回標頭值作為 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構，而不需要應用程式剖析資料。</span><span class="sxs-lookup"><span data-stu-id="531dc-393">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="531dc-394">用於其值為日期/時間字串的標頭，例如「上次修改時間」。</span><span class="sxs-lookup"><span data-stu-id="531dc-394">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="531dc-395">備註</span><span class="sxs-lookup"><span data-stu-id="531dc-395">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="531dc-396">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="531dc-396">WinINet does not support server implementations.</span></span> <span data-ttu-id="531dc-397">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="531dc-397">In addition, it should not be used from a service.</span></span> <span data-ttu-id="531dc-398">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="531dc-398">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="531dc-399">規格需求</span><span class="sxs-lookup"><span data-stu-id="531dc-399">Requirements</span></span>



| <span data-ttu-id="531dc-400">需求</span><span class="sxs-lookup"><span data-stu-id="531dc-400">Requirement</span></span> | <span data-ttu-id="531dc-401">值</span><span class="sxs-lookup"><span data-stu-id="531dc-401">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="531dc-402">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="531dc-402">Minimum supported client</span></span><br/> | <span data-ttu-id="531dc-403">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="531dc-403">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="531dc-404">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="531dc-404">Minimum supported server</span></span><br/> | <span data-ttu-id="531dc-405">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="531dc-405">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="531dc-406">標頭</span><span class="sxs-lookup"><span data-stu-id="531dc-406">Header</span></span><br/>                   | <dl> <span data-ttu-id="531dc-407"><dt>Wininet</dt></span><span class="sxs-lookup"><span data-stu-id="531dc-407"><dt>Wininet.h</dt></span></span> </dl> |



 

