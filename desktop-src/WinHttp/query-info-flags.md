---
description: WinHttpQueryHeaders 會使用這些屬性和修飾詞。
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: " (WinHTTP. h) 的查詢資訊旗標"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9ffc8f4ba4a947fe6fb277617c99460c43ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026967"
---
# <a name="query-info-flags-winhttph"></a><span data-ttu-id="d4d8d-103"> (WinHTTP. h) 的查詢資訊旗標</span><span class="sxs-lookup"><span data-stu-id="d4d8d-103">Query Info Flags (Winhttp.h)</span></span>

<span data-ttu-id="d4d8d-104">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)會使用這些屬性和修飾詞。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-104">These attributes and modifiers are used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

<span data-ttu-id="d4d8d-105">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)會使用屬性旗標來指出要取出的資訊。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-105">The attribute flags are used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) to indicate what information to retrieve.</span></span> <span data-ttu-id="d4d8d-106">大部分的屬性旗標會直接對應至特定的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="d4d8d-107">另外還有一些特殊旗標（例如 WINHTTP \_ 查詢 \_ 原始 \_ 標頭）與特定標頭無關。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-107">There are also some special flags, such as WINHTTP\_QUERY\_RAW\_HEADERS, that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="d4d8d-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP \_ 查詢 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-109">抓取回應可接受的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-109">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ 查詢 \_ 接受 \_ 字元集**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-111">捕獲回應的可接受字元集。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-111">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP \_ 查詢 \_ 接受 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-113">抓取回應可接受的內容編碼值。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-113">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP \_ 查詢 \_ 接受 \_ 語言**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-115">抓取回應的可接受自然語言。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-115">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP \_ 查詢 \_ 接受 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-117">抓取資源所接受範圍要求的類型。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-117">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP \_ 查詢 \_ 存留期**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-119">抓取 Age 回應標頭欄位，其中包含寄件者在源伺服器上產生回應以來的預估時間量。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-119">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP \_ 查詢 \_ 允許**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-121">接收伺服器所支援的 [*HTTP 動詞*](glossary.md)命令。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-121">Receives the [*HTTP verb*](glossary.md)s supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP \_ 查詢 \_ 驗證 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP\_QUERY\_AUTHENTICATION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-123">抓取 Authentication-Info 標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-123">Retrieves the Authentication-Info header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP \_ 查詢 \_ 授權**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-125">抓取用於要求的授權認證。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-125">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP \_ 查詢快取 \_ \_ 控制**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-127">抓取快取控制指示詞。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-127">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP \_ 查詢 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-129">抓取任何針對特定連接指定的選項，且不能透過其他連接的 proxy 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-129">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 基底**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-131">抓取基底統一資源識別項 (URI) 來解析實體內的相對 Url。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-131">Retrieves the base Uniform Resource Identifier (URI) to resolve relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-133">已過時。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-133">Obsolete.</span></span> <span data-ttu-id="d4d8d-134">針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-134">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 處置**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-136">已過時。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-136">Obsolete.</span></span> <span data-ttu-id="d4d8d-137">針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-137">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-139">抓取已套用至整個資源的其他內容編碼。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-139">Retrieves additional content coding that has been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-141">抓取內容識別。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-141">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 語言**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-143">抓取內容撰寫的語言。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-143">Retrieves the language that the content is written in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-145">抓取資源的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-145">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-147">抓取訊息中所包含之實體的資源位置。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-147">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP \_ 查詢 \_ 內容 \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-149">針對提供實體主體端對端訊息完整性檢查的目的，抓取實體主體的 MD5 摘要。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-149">Retrieves an MD5 digest of the entity body for the purpose of providing an end-to-end message integrity check for the entity body.</span></span> <span data-ttu-id="d4d8d-150">如需詳細資訊，請參閱 [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt)。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-150">For more information, see [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-152">抓取完整實體主體中應插入部分實體內容的位置，以及完整實體主體的總大小。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-152">Retrieves the location in the full entity body where the partial entity body should be inserted and the total size of the full entity body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 傳輸 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-154">捕獲適用于實體主體的編碼轉換。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-154">Retrieves an encoding transformation applicable to an entity-body.</span></span> <span data-ttu-id="d4d8d-155">它可能已經套用、可能需要套用，或可能會選擇性地套用。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-155">It may already have been applied, may need to be applied, or may be optionally applicable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP \_ 查詢 \_ 內容 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-157">接收資源的內容類型，例如文字或 html。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-157">Receives the content type of the resource, such as text or html.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP \_ 查詢 \_ COOKIE**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-159">抓取任何與要求相關聯的 cookie。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-159">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP \_ 查詢 \_ 成本**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-161">不支援。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-161">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP \_ 查詢 \_ 自訂**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-163">使 [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) 搜尋 *pwszName* 參數中指定的標頭名稱，並將標頭資訊儲存在 *lpBuffer* 中。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-163">Causes [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) to search for the header name specified in the *pwszName* parameter and store the header information in *lpBuffer*.</span></span> <span data-ttu-id="d4d8d-164">應用程式可以使用 **WINHTTP \_ 選項 \_ 接收 \_ 回應 \_ 超時** ，來限制此查詢等候接收所有標頭的時間上限。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-164">An application can use **WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT** to limit the maximum time this query waits for all headers to be received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP \_ 查詢 \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-166">接收發出訊息的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-166">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_ \_ \_ 繼承自的 WINHTTP 查詢**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**WINHTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-168">不支援。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-168">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP \_ 查詢 \_ ETAG**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-170">抓取相關聯實體的實體標記。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-170">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP \_ 查詢 \_ 預期**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-172">抓取預期的標頭，指出用戶端應用程式是否應該預期100系列回應。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-172">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP \_ 查詢 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-174">接收應將資源視為過期的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-174">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**轉送的 WINHTTP \_ 查詢 \_**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**WINHTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-176">已過時。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-176">Obsolete.</span></span> <span data-ttu-id="d4d8d-177">針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-177">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP \_ 查詢 \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-179">如果指定 From 標頭，則抓取控制提出要求之 [*使用者代理程式*](glossary.md) 之使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-179">Retrieves the e-mail address for the user who controls the requesting [*user agent*](glossary.md) if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP \_ 查詢 \_ 主機**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-181">抓取所要求資源的網際網路主機和埠號碼。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-181">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**符合的 WINHTTP \_ 查詢 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-183">抓取 If-Match 要求標頭欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-183">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_ \_ \_ \_ 自從之後修改的 WINHTTP 查詢**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WINHTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-185">抓取已修改-自標頭的內容。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-185">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_ \_ 如果 \_ 沒有 \_ 相符的 WINHTTP 查詢**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WINHTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-187">抓取 If-match 要求標頭欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-187">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP \_ 查詢 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-189">抓取 If-Range 要求標頭欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-189">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="d4d8d-190">此標頭可讓用戶端應用程式檢查與用戶端應用程式快取中實體部分複本相關的實體是否尚未更新。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-190">This header allows the client application to check if the entity related to a partial copy of the entity in the client application's cache has not been updated.</span></span> <span data-ttu-id="d4d8d-191">如果實體尚未更新，請傳送缺少用戶端應用程式的元件。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-191">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="d4d8d-192">如果實體已更新，請傳送整個更新的實體。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-192">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP \_ 查詢 \_ （ \_ \_ 自之後）**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-194">從要求標頭欄位開始，抓取（如果不修改）的內容。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-194">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP \_ 查詢 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-196">已過時。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-196">Obsolete.</span></span> <span data-ttu-id="d4d8d-197">針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-197">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ 上次 \_ 修改的 WINHTTP 查詢**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**WINHTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-199">接收上次修改資源的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-199">Receives the date and time at which the resource was last modified.</span></span> <span data-ttu-id="d4d8d-200">日期和時間是由伺服器決定。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-200">The date and time are determined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP \_ 查詢 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-202">抓取位置回應標頭中使用的絕對 URI。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-202">Retrieves the absolute URI used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP \_ 查詢 \_ 最大值**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-204">表示 WINHTTP 查詢值的最大 \_ 值 \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-204">Indicates the maximum value of a WINHTTP\_QUERY\_\* value.</span></span> <span data-ttu-id="d4d8d-205">不是查詢旗標。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-205">Not a query flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP \_ 查詢 \_ 最大 \_ 轉寄**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-207">抓取可將要求轉送至下一個輸入伺服器的 proxy 或閘道數目。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-207">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP \_ 查詢 \_ 訊息 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-209">不支援。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-209">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP \_ 查詢 \_ MIME \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-211">接收用來建立訊息之多用途網際網路郵件延伸 (MIME) 通訊協定的版本。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-211">Receives the version of the Multipurpose Internet Mail Extensions (MIME) protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP \_ 查詢 \_ TOASTPKG.ORIG \_ URI**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-213">已過時。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-213">Obsolete.</span></span> <span data-ttu-id="d4d8d-214">針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-214">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP \_ 查詢 \_ PRAGMA**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-216">接收可能會在要求/回應鏈中套用至任何收件者的特定執行指示詞。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-216">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP \_ 查詢 \_ PROXY \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-218">抓取 proxy 傳回的驗證配置和領域。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-218">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP \_ 查詢 \_ PROXY \_ 授權**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-220">抓取用來將使用者識別為需要驗證之 proxy 的標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-220">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="d4d8d-221">只有在將要求傳送到伺服器之前，才能抓取此標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-221">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP \_ 查詢 \_ PROXY \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-223">抓取 Proxy-Connection 標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-223">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP \_ 查詢 \_ PROXY \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP\_QUERY\_PROXY\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-225">抓取 Proxy-Support 標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-225">Retrieves the Proxy-Support header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**公開的 WINHTTP \_ 查詢 \_**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-227">接收此伺服器提供的 HTTP 指令動詞。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-227">Receives HTTP verbs available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP \_ 查詢 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-229">捕獲實體的位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-229">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP \_ 查詢 \_ 原始 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-231">接收伺服器傳回的所有標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-231">Receives all the headers returned by the server.</span></span> <span data-ttu-id="d4d8d-232">每個標頭都以 " \\ 0" 結束。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-232">Each header is terminated by "\\0".</span></span> <span data-ttu-id="d4d8d-233">額外的 " \\ 0" 會終止標頭清單。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-233">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP \_ 查詢 \_ 原始 \_ 標頭 \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-235">接收伺服器傳回的所有標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-235">Receives all the headers returned by the server.</span></span> <span data-ttu-id="d4d8d-236">每個標頭都會以換行字元（ (CR/LF) 序列）來分隔。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-236">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP \_ 查詢 \_ 推薦者**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-238">接收取得所要求 URI 之資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-238">Receives the URI of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP \_ 查詢重新整理 \_**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-240">已過時。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-240">Obsolete.</span></span> <span data-ttu-id="d4d8d-241">針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-241">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP \_ 查詢 \_ 要求 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-243">接收在要求中使用的 HTTP 動詞命令，通常是 GET 或 POST。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-243">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP \_ 查詢 \_ 之後重試 \_**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-245">捕獲服務預期無法使用的時間量。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-245">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP \_ 查詢 \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-247">抓取源伺服器用來處理要求之軟體的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-247">Retrieves information about the software used by the originating server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP \_ 查詢 \_ 設定 \_ COOKIE**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-249">接收要求的 cookie 集合值。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-249">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP \_ 查詢 \_ 狀態 \_ 代碼**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-251">接收伺服器所傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-251">Receives the status code returned by the server.</span></span> <span data-ttu-id="d4d8d-252">如需可能值的清單，請參閱 [**HTTP 狀態碼**](http-status-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-252">For a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP \_ 查詢 \_ 狀態 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-254">接收回應行上伺服器所傳回的其他文字。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-254">Receives additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP \_ 查詢 \_ 標題**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-256">已過時。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-256">Obsolete.</span></span> <span data-ttu-id="d4d8d-257">針對舊版應用程式相容性進行維護。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-257">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP \_ 查詢 \_ 傳輸 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-259">抓取已套用至訊息主體的轉換類型，以便在傳送者與收件者之間安全地傳輸。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-259">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_ \_ 除非 \_ \_ 自從之後修改，否則 WINHTTP 查詢**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WINHTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-261">抓取，除非修改-自標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-261">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP \_ 查詢 \_ 升級**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-263">抓取伺服器所支援的其他通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-263">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP \_ 查詢 \_ URI**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-265">接收可識別要求 URI 資源的部分或所有 URI。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-265">Receives some or all of the URI by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP \_ 查詢 \_ 使用者 \_ 代理程式**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-267">抓取提出要求之使用者代理程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-267">Retrieves information about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP \_ 查詢 \_ 不同**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-269">使用伺服器驅動的協商，抓取表示已從回應的許多可用表示中選取實體的標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-269">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP \_ 查詢 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-271">抓取存在於狀態行中的 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-271">Retrieves the HTTP version that is present in the status line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP \_ 查詢 \_ VIA**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-273">抓取使用者代理程式與伺服器上要求之間的中繼通訊協定和收件者，以及源伺服器與用戶端的回應之間的收件者。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-273">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP \_ 查詢 \_ 警告**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-275">抓取回應狀態碼可能不會反映之回應狀態的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-275">Retrieves additional information about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP \_ 查詢 \_ WWW \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-277">抓取伺服器傳回的驗證配置和領域。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-277">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="d4d8d-278">修飾詞旗標會與屬性旗標搭配使用，以修改要求。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-278">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="d4d8d-279">修飾詞旗標可修改傳回的資料格式，或指出 [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) 函式應該搜尋資訊的位置。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-279">Modifier flags either modify the format of the data returned or indicate where the [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function should search for the information.</span></span>

<dl> <dt>

<span data-ttu-id="d4d8d-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP \_ 查詢 \_ 旗標 \_ 編號**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-281">針對值為數字的標頭，以32位數位的形式傳回資料，例如狀態碼。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-281">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP \_ 查詢 \_ 旗 \_ \_ 標要求標頭**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-283">只查詢要求標頭。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-283">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4d8d-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP \_ 查詢 \_ 旗標 \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="d4d8d-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4d8d-285">傳回標頭值作為 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構，而不需要應用程式剖析資料。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-285">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="d4d8d-286">用於其值為日期/時間字串的標頭，例如「上次修改時間」。</span><span class="sxs-lookup"><span data-stu-id="d4d8d-286">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4d8d-287">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4d8d-287">Requirements</span></span>



| <span data-ttu-id="d4d8d-288">需求</span><span class="sxs-lookup"><span data-stu-id="d4d8d-288">Requirement</span></span> | <span data-ttu-id="d4d8d-289">值</span><span class="sxs-lookup"><span data-stu-id="d4d8d-289">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d8d-290">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4d8d-290">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d8d-291">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4d8d-291">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="d4d8d-292">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4d8d-292">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d8d-293">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="d4d8d-293">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="d4d8d-294">標頭</span><span class="sxs-lookup"><span data-stu-id="d4d8d-294">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d8d-295"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d8d-295"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d8d-296">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4d8d-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d8d-297">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="d4d8d-297">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

