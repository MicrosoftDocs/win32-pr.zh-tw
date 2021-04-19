---
title: 'API 旗標 (Wininet. h) '
description: 許多 WinINet 函數都會接受旗標陣列作為參數。 以下是已定義旗標的簡短描述。
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966326"
---
# <a name="api-flags"></a><span data-ttu-id="5ae3d-104">API 旗標</span><span class="sxs-lookup"><span data-stu-id="5ae3d-104">API Flags</span></span>

<span data-ttu-id="5ae3d-105">許多 WinINet 函數都會接受旗標陣列作為參數。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-105">Many of the WinINet functions accept an array of flags as a parameter.</span></span> <span data-ttu-id="5ae3d-106">以下是已定義旗標的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-106">The following is a brief description of the defined flags.</span></span>

<dl> <dt>

<span data-ttu-id="5ae3d-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**網際網路 \_ COOKIE \_ 評估 \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**INTERNET\_COOKIE\_EVALUATE\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-108">0x80</span><span class="sxs-lookup"><span data-stu-id="5ae3d-108">0x80</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-109">指出隱私權保護的平臺 (P3P) 標頭與 cookie 相關聯。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-109">Indicates that a Platform for Privacy Protection (P3P) header is to be associated with a cookie.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**網際網路 \_ COOKIE \_ 第三 \_ 方**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**INTERNET\_COOKIE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-111">0x10</span><span class="sxs-lookup"><span data-stu-id="5ae3d-111">0x10</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-112">指出正在設定或抓取協力廠商 cookie。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-112">Indicates that a third-party cookie is being set or retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**網際網路 \_ 旗標 \_ 非同步**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**INTERNET\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-114">0x10000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-114">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-115">只會在從這個函式傳回之控制碼的控制碼上進行非同步要求。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-115">Makes only asynchronous requests on handles descended from the handle returned from this function.</span></span> <span data-ttu-id="5ae3d-116">只有 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函式會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-116">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**網際網路旗標快取 \_ \_ \_ 非同步**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-118">0x00000080</span><span class="sxs-lookup"><span data-stu-id="5ae3d-118">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-119">允許延遲快取寫入。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-119">Allows a lazy cache write.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**\_ \_ \_ \_ 網路 \_ 失敗時的網際網路旗標快取**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-121">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-121">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-122">如果資源的網路要求因 [ \_ 網際網路連線 \_ \_ 重設錯誤](wininet-errors.md) 或 [ \_ 網際網路 \_ 無法 \_ 連線](wininet-errors.md) 錯誤而失敗，則會從快取傳回資源。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-122">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="5ae3d-123">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-123">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**網際網路旗標不快取 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**INTERNET\_FLAG\_DONT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-125">0x04000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-125">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-126">不會將傳回的實體新增至快取。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-126">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="5ae3d-127">這與慣用的值相同，也就是 [網際網路旗標無快取 \_ \_ \_ \_ 寫入](/windows)。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-127">This is identical to the preferred value, [INTERNET\_FLAG\_NO\_CACHE\_WRITE](/windows).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**網際網路 \_ 旗標 \_ 現有的 \_ CONNECT**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**INTERNET\_FLAG\_EXISTING\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-129">0x20000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-129">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-130">嘗試使用現有的 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 物件（如果有的話），其屬性必須與提出要求所需的屬性相同。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-130">Attempts to use an existing [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) object if one exists with the same attributes required to make the request.</span></span> <span data-ttu-id="5ae3d-131">這僅適用于 FTP 作業，因為 FTP 是唯一的通訊協定，通常會在同一個會話期間執行多個作業。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-131">This is useful only with FTP operations, since FTP is the only protocol that typically performs multiple operations during the same session.</span></span> <span data-ttu-id="5ae3d-132">WinINet 會針對 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所產生的每個 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼，快取單一連接控制碼。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-132">WinINet caches a single connection handle for each [**HINTERNET**](appendix-a-hinternet-handles.md) handle generated by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="5ae3d-133">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)和 **InternetConnect** 函式會將此旗標用於 Http 和 Ftp 連接。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-133">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and **InternetConnect** functions use this flag for Http and Ftp connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**網際網路 \_ 旗標 \_ 表單 \_ 提交**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**INTERNET\_FLAG\_FORMS\_SUBMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-135">0x00000040</span><span class="sxs-lookup"><span data-stu-id="5ae3d-135">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-136">表示這是表單提交。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-136">Indicates that this is a Forms submission.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**來自快取 \_ 的網際網路旗標 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**INTERNET\_FLAG\_FROM\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-138">0x01000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-138">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-139">不會發出網路要求。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-139">Does not make network requests.</span></span> <span data-ttu-id="5ae3d-140">所有實體都會從快取傳回。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-140">All entities are returned from the cache.</span></span> <span data-ttu-id="5ae3d-141">如果要求的專案不在快取中， \_ \_ 則會傳回適當的錯誤，例如找不到錯誤檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-141">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="5ae3d-142">只有 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函式會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-142">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**網際網路 \_ 旗標 \_ FWD \_ 回**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**INTERNET\_FLAG\_FWD\_BACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-144">0x00000020</span><span class="sxs-lookup"><span data-stu-id="5ae3d-144">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-145">指出函式應使用目前在網際網路快取中的資源複本。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-145">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="5ae3d-146">不會檢查資源的到期日和其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-146">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="5ae3d-147">如果在網際網路快取中找不到要求的專案，系統會嘗試找出網路上的資源。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-147">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="5ae3d-148">此值是在 Microsoft Internet Explorer 5 中引進，並與 Internet Explorer 的 [ **向前** ] 和 [ **上一頁** ] 按鈕作業相關聯。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-148">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**網際網路 \_ 旗標 \_ 超連結**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**INTERNET\_FLAG\_HYPERLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-150">0x00000400</span><span class="sxs-lookup"><span data-stu-id="5ae3d-150">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-151">如果沒有過期時間，而且在決定是否要從網路重載專案時，不會從伺服器傳回任何 LastModified 時間，則會強制執行重載。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-151">Forces a reload if there is no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.</span></span> <span data-ttu-id="5ae3d-152">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)都可使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-152">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="5ae3d-153">**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-153">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**網際網路 \_ 旗標 \_ 忽略 \_ CERT \_ CN \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-155">0x00001000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-155">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-156">停用根據要求中指定的主機名稱，從伺服器傳回的 SSL/PCT 憑證檢查。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-156">Disables checking of SSL/PCT-based certificates that are returned from the server against the host name given in the request.</span></span> <span data-ttu-id="5ae3d-157">WinINet 使用簡單的憑證檢查，方法是比較相符的主機名稱和簡單萬用字元規則。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-157">WinINet uses a simple check against certificates by comparing for matching host names and simple wildcarding rules.</span></span> <span data-ttu-id="5ae3d-158">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-158">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**網際網路 \_ 旗標 \_ 忽略憑證 \_ \_ 日期 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-161">停用 SSL/PCT 憑證的檢查，以取得適當的有效日期。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-161">Disables checking of SSL/PCT-based certificates for proper validity dates.</span></span> <span data-ttu-id="5ae3d-162">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-162">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**網際網路 \_ 旗標 \_ 忽略重新 \_ 導向 \_ 至 \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-164">0x00008000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-164">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-165">停用此特殊重新導向類型的偵測。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-165">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="5ae3d-166">使用這個旗標時，WinINet 會以透明的方式允許從 HTTPS 重新導向至 HTTP Url。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-166">When this flag is used, WinINet transparently allows redirects from HTTPS to HTTP URLs.</span></span> <span data-ttu-id="5ae3d-167">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-167">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**網際網路 \_ 旗標 \_ 忽略重新 \_ 導向 \_ 至 \_ HTTPS**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-169">0x00004000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-169">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-170">停用此特殊重新導向類型的偵測。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-170">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="5ae3d-171">使用這個旗標時，WinINet 會以透明的方式允許從 HTTP 重新導向至 HTTPS Url。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-171">When this flag is used, WinINet transparently allow redirects from HTTP to HTTPS URLs.</span></span> <span data-ttu-id="5ae3d-172">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-172">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**網際網路 \_ 旗標 \_ 保持 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**INTERNET\_FLAG\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-174">0x00400000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-174">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-175">針對連接使用 keep-alive 語義（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-175">Uses keep-alive semantics, if available, for the connection.</span></span> <span data-ttu-id="5ae3d-176">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (會針對 HTTP 要求) 使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-176">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span> <span data-ttu-id="5ae3d-177">Microsoft Network (MSN) 、NTLM 和其他類型的驗證都需要此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-177">This flag is required for Microsoft Network (MSN), NTLM, and other types of authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**網際網路 \_ 旗標 \_ 設為 \_ 持續**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-179">0x02000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-179">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-180">不再支援。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-180">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**網際網路 \_ 旗標必須快取 \_ \_ \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ae3d-182">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-183">與慣用值相同， **網際網路 \_ 旗標 \_ 需要 \_** 檔案。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-183">Identical to the preferred value, **INTERNET\_FLAG\_NEED\_FILE**.</span></span> <span data-ttu-id="5ae3d-184">如果無法快取檔案，則會建立暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-184">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="5ae3d-185">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)都可使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-185">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="5ae3d-186">**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-186">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**網際網路 \_ 旗標 \_ 需要檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**INTERNET\_FLAG\_NEED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-188">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ae3d-188">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-189">如果無法快取檔案，則會建立暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-189">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="5ae3d-190">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)都可使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-190">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="5ae3d-191">**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-191">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**網際網路 \_ 旗標 \_ 無 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**INTERNET\_FLAG\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-193">0x00040000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-193">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-194">不會自動嘗試驗證。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-194">Does not attempt authentication automatically.</span></span> <span data-ttu-id="5ae3d-195">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-195">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**網際網路 \_ 旗標 \_ 沒有 \_ 自動重新 \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**INTERNET\_FLAG\_NO\_AUTO\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-197">0x00200000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-197">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-198">不會自動處理 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)中的重新導向。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-198">Does not automatically handle redirection in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="5ae3d-199">此旗標也可供 HTTP 要求的 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-199">This flag can also be used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) for HTTP requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**網際網路 \_ 旗標無快取 \_ \_ \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-201">0x04000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-201">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-202">不會將傳回的實體新增至快取。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-202">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="5ae3d-203">、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)會使用這個旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-203">This flag is used by , [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="5ae3d-204">**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-204">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**網際網路 \_ 旗標 \_ 無 \_ COOKIE**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**INTERNET\_FLAG\_NO\_COOKIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-206">0x00080000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-206">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-207">不會自動將 cookie 標頭新增至要求，也不會自動將傳回的 cookie 新增至 cookie 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-207">Does not automatically add cookie headers to requests, and does not automatically add returned cookies to the cookie database.</span></span> <span data-ttu-id="5ae3d-208">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (可針對 HTTP 要求) 使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-208">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**網際網路 \_ 旗標 \_ 無 \_ UI**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**INTERNET\_FLAG\_NO\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="5ae3d-210">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-211">停用 cookie 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-211">Disables the cookie dialog box.</span></span> <span data-ttu-id="5ae3d-212">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)只可使用此旗標 (HTTP 要求) 。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-212">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**網際網路 \_ 旗標 \_ 離線**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**INTERNET\_FLAG\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-214">0x01000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-214">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-215">與來自快取 **\_ \_ 的 \_ 網際網路旗** 標相同。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-215">Identical to **INTERNET\_FLAG\_FROM\_CACHE**.</span></span> <span data-ttu-id="5ae3d-216">不會發出網路要求。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-216">Does not make network requests.</span></span> <span data-ttu-id="5ae3d-217">所有實體都會從快取傳回。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-217">All entities are returned from the cache.</span></span> <span data-ttu-id="5ae3d-218">如果要求的專案不在快取中， \_ \_ 則會傳回適當的錯誤，例如找不到錯誤檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-218">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="5ae3d-219">只有 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函式會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-219">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**網際網路 \_ 旗標 \_ 被動式**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**INTERNET\_FLAG\_PASSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-221">0x08000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-221">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-222">使用被動 FTP 語義。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-222">Uses passive FTP semantics.</span></span> <span data-ttu-id="5ae3d-223">只有 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-223">Only [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) use this flag.</span></span> <span data-ttu-id="5ae3d-224">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 會對 ftp 要求使用此旗標，而 [**INTERNETOPENURL**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 會針對 ftp 檔案和目錄使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-224">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses this flag for FTP requests, and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses this flag for FTP files and directories.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**網際網路 \_ 旗標 \_ PRAGMA \_ NOCACHE**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-226">0x00000100</span><span class="sxs-lookup"><span data-stu-id="5ae3d-226">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-227">強制源伺服器解析要求，即使 proxy 上有快取的複本也一樣。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-227">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="5ae3d-228">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)函式只 (HTTP 和 HTTPS 要求) 且 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)函式使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-228">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**網際網路 \_ 旗標 \_ 原始 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**INTERNET\_FLAG\_RAW\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-230">0x40000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-230">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-231">在抓取 FTP 目錄資訊時，以 [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) 結構的形式傳回資料。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-231">Returns the data as a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure when retrieving FTP directory information.</span></span> <span data-ttu-id="5ae3d-232">如果未指定此旗標，或透過 CERN proxy 進行呼叫， [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 會傳回 HTML 版本的目錄。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-232">If this flag is not specified or if the call is made through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) returns the HTML version of the directory.</span></span> <span data-ttu-id="5ae3d-233">只有 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函式會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-233">Only the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function uses this flag.</span></span>

<span data-ttu-id="5ae3d-234">**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：** 在抓取 Gopher 目錄資訊時，也會傳回 [**gopher \_ 尋找 \_ 資料**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) 結構。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-234">**Windows XP and Windows Server 2003 R2 and earlier:** Also returns a [**GOPHER\_FIND\_DATA**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) structure when retrieving Gopher directory information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**網際網路 \_ 旗標 \_ 讀取預先 \_ 提取**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**INTERNET\_FLAG\_READ\_PREFETCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-236">0x00100000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-236">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-237">此旗標目前已停用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-237">This flag is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**網際網路 \_ 旗標 \_ 重載**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**INTERNET\_FLAG\_RELOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-239">0x80000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-239">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-240">強制從源伺服器下載所要求的檔案、物件或目錄清單，而不是從快取。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-240">Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.</span></span> <span data-ttu-id="5ae3d-241">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)函數會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-241">The [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) functions use this flag.</span></span>

<span data-ttu-id="5ae3d-242">**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-242">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**網際網路 \_ 旗標 \_ 受限 \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**INTERNET\_FLAG\_RESTRICTED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-244">0x00020000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-244">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-245">指出所設定的 cookie 與不受信任的網站相關聯。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-245">Indicates that the cookie being set is associated with an untrusted site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**網際網路 \_ 旗標重新 \_ 同步處理**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-247">0x00000800</span><span class="sxs-lookup"><span data-stu-id="5ae3d-247">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-248">如果資源自上一次下載以來已經過修改，就會重載 HTTP 資源。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-248">Reloads HTTP resources if the resource has been modified since the last time it was downloaded.</span></span> <span data-ttu-id="5ae3d-249">所有 FTP 資源都會重載。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-249">All FTP resources are reloaded.</span></span> <span data-ttu-id="5ae3d-250">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)都可使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-250">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="5ae3d-251">**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：**[**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)和 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)也會使用，並重載 Gopher 資源。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-251">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), and Gopher resources are reloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**網際網路 \_ 旗標 \_ 安全**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**INTERNET\_FLAG\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-253">0x00800000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-253">0x00800000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-254">使用安全的交易語義。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-254">Uses secure transaction semantics.</span></span> <span data-ttu-id="5ae3d-255">這會轉譯成使用安全通訊端層/私用通訊技術 (SSL/PCT) 而且只有在 HTTP 要求中有意義。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-255">This translates to using Secure Sockets Layer/Private Communications Technology (SSL/PCT) and is only meaningful in HTTP requests.</span></span> <span data-ttu-id="5ae3d-256">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)會使用此旗標，但如果 URL 中出現 HTTPs://，則這是多餘的。[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函式會使用此旗標來進行 HTTP 連接;在此連接下建立的所有要求控制碼都會繼承此旗標。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-256">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), but this is redundant if https:// appears in the URL.The [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function uses this flag for HTTP connections; all the request handles created under this connection will inherit this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**網際網路 \_ 旗標 \_ 轉換 \_ ASCII**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**INTERNET\_FLAG\_TRANSFER\_ASCII**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-258">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5ae3d-258">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-259">將檔案以 ASCII 的形式傳輸 (FTP 僅) 。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-259">Transfers file as ASCII (FTP only).</span></span> <span data-ttu-id="5ae3d-260">此旗標可供 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)和 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-260">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**網際網路 \_ 旗標 \_ 傳輸 \_ 二進位**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**INTERNET\_FLAG\_TRANSFER\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-262">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5ae3d-262">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-263">將檔案以二進位格式傳輸 (僅) 的 FTP。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-263">Transfers file as binary (FTP only).</span></span> <span data-ttu-id="5ae3d-264">此旗標可供 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)和 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-264">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**網際網路 \_ 無 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ae3d-266">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-267">指出該 API 不應進行任何回呼。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-267">Indicates that no callbacks should be made for that API.</span></span> <span data-ttu-id="5ae3d-268">這會用於允許非同步作業之函式的 *dxCoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-268">This is used for the *dxContext* parameter of the functions that allow asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**網際網路 \_ 選項 \_ 抑制 \_ 伺服器 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-270">104</span><span class="sxs-lookup"><span data-stu-id="5ae3d-270">104</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-271">設定 HTTP 要求物件，使其不會登入源伺服器，但會對 HTTP proxy 伺服器執行自動登入。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-271">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="5ae3d-272">此選項與「要求旗標網際網路 \_ 旗標 \_ 無驗證」不同 \_ ，這會防止對 proxy 伺服器和源伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-272">This option differs from the Request flag INTERNET\_FLAG\_NO\_AUTH, which prevents authentication to both proxy servers and origin servers.</span></span> <span data-ttu-id="5ae3d-273">設定此模式將會抑制使用任何認證材質 (先前提供的使用者名稱/密碼或用戶端 SSL 憑證) 在與源伺服器通訊時使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-273">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="5ae3d-274">但是，如果要求必須透過驗證 proxy 傳輸，WinINet 仍會根據使用者的內部網路區域設定，對 HTTP proxy 執行自動驗證。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-274">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="5ae3d-275">預設內部網路區域設定是允許使用使用者的預設認證進行自動登入。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-275">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span> <span data-ttu-id="5ae3d-276">為了確保隱藏所有識別資訊，呼叫端應該將 [網際網路 \_ 選項 \_ 抑制 \_ 伺服器 \_ 驗證] 與 [網際網路 \_ 旗標 \_ 無 \_ cookie 要求] 旗標合併。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-276">To ensure suppression of all identifying information, the caller should combine INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH with the INTERNET\_FLAG\_NO\_COOKIES request flag.</span></span> <span data-ttu-id="5ae3d-277">此選項只能在要求物件上設定，然後才會傳送。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-277">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="5ae3d-278">在傳送要求之後嘗試設定此選項，將會傳回錯誤的 \_ 網際網路 \_ 錯誤 \_ 控制碼 \_ 狀態。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-278">Attempts to set this option after the request has been sent will return ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE.</span></span> <span data-ttu-id="5ae3d-279">此選項不需要任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-279">No buffer is required for this option.</span></span> <span data-ttu-id="5ae3d-280">InternetSetOption 只會在 HttpOpenRequest 所傳回的控制碼上使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-280">This is used by InternetSetOption on handles returned by HttpOpenRequest only.</span></span> <span data-ttu-id="5ae3d-281">版本：需要 Internet Explorer 8.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-281">Version: Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WININET \_ API \_ 旗標 \_ 非同步**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WININET\_API\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5ae3d-283">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-284">強制執行非同步作業。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-284">Forces asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**WININET \_ API \_ 旗標 \_ 同步**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**WININET\_API\_FLAG\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-286">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5ae3d-286">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-287">強制執行同步作業。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-287">Forces synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ae3d-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**WININET \_ API \_ 旗標 \_ 使用 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**WININET\_API\_FLAG\_USE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5ae3d-289">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="5ae3d-290">強制 API 使用內容值，即使它設定為零也一樣。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-290">Forces the API to use the context value, even if it is set to zero.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ae3d-291">備註</span><span class="sxs-lookup"><span data-stu-id="5ae3d-291">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ae3d-292">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-292">WinINet does not support server implementations.</span></span> <span data-ttu-id="5ae3d-293">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-293">In addition, it should not be used from a service.</span></span> <span data-ttu-id="5ae3d-294">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="5ae3d-294">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ae3d-295">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ae3d-295">Requirements</span></span>



| <span data-ttu-id="5ae3d-296">需求</span><span class="sxs-lookup"><span data-stu-id="5ae3d-296">Requirement</span></span> | <span data-ttu-id="5ae3d-297">值</span><span class="sxs-lookup"><span data-stu-id="5ae3d-297">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae3d-298">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ae3d-298">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae3d-299">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ae3d-299">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5ae3d-300">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ae3d-300">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae3d-301">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ae3d-301">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5ae3d-302">標頭</span><span class="sxs-lookup"><span data-stu-id="5ae3d-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ae3d-303"><dt>Wininet</dt></span><span class="sxs-lookup"><span data-stu-id="5ae3d-303"><dt>Wininet.h</dt></span></span> </dl> |



 

