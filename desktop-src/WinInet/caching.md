---
title: " (Windows 網際網路) 快取"
description: WinINet 函數具有簡單但彈性的內建快取支援。
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093631"
---
# <a name="caching-windows-internet"></a><span data-ttu-id="50880-103"> (Windows 網際網路) 快取</span><span class="sxs-lookup"><span data-stu-id="50880-103">Caching (Windows Internet)</span></span>

<span data-ttu-id="50880-104">WinINet 函數具有簡單但彈性的內建快取支援。</span><span class="sxs-lookup"><span data-stu-id="50880-104">The WinINet functions have simple, yet flexible, built-in caching support.</span></span> <span data-ttu-id="50880-105">從網路取出的任何資料都會快取在硬碟上，並針對後續的要求進行取出。</span><span class="sxs-lookup"><span data-stu-id="50880-105">Any data retrieved from the network is cached on the hard disk and retrieved for subsequent requests.</span></span> <span data-ttu-id="50880-106">應用程式可以控制每個要求的快取。</span><span class="sxs-lookup"><span data-stu-id="50880-106">The application can control the caching on each request.</span></span> <span data-ttu-id="50880-107">若為來自伺服器的 HTTP 要求，也會快取大部分接收到的標頭。</span><span class="sxs-lookup"><span data-stu-id="50880-107">For http requests from the server, most headers received are also cached.</span></span> <span data-ttu-id="50880-108">從快取滿足 HTTP 要求時，快取的標頭也會傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="50880-108">When an http request is satisfied from the cache, the cached headers are also returned to the caller.</span></span> <span data-ttu-id="50880-109">這可讓您順暢地下載資料，無論資料是來自快取或網路。</span><span class="sxs-lookup"><span data-stu-id="50880-109">This makes data download seamless, whether the data is coming from the cache or from the network.</span></span>

<span data-ttu-id="50880-110">應用程式必須適當地配置緩衝區，才能在使用持續性 URL 快取函式時取得所需的結果。</span><span class="sxs-lookup"><span data-stu-id="50880-110">Applications must properly allocate a buffer in order to get the desired results when using the persistent URL caching functions.</span></span> <span data-ttu-id="50880-111">如需詳細資訊，請參閱 [使用緩衝區](appendix-b-using-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="50880-111">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>

## <a name="cache-behavior-during-response-processing"></a><span data-ttu-id="50880-112">回應處理期間的快取行為</span><span class="sxs-lookup"><span data-stu-id="50880-112">Cache Behavior During Response Processing</span></span>

<span data-ttu-id="50880-113">WinINet 快取符合 RFC 2616 中所述的 HTTP 快取控制指示詞。</span><span class="sxs-lookup"><span data-stu-id="50880-113">The WinINet cache is compliant with the HTTP cache-control directives described in RFC 2616.</span></span> <span data-ttu-id="50880-114">快取控制指示詞和應用程式集旗標會決定可快取的內容;但是，WinINet 會根據下列準則來判斷實際快取的內容：</span><span class="sxs-lookup"><span data-stu-id="50880-114">The cache-control directives and application set flags determine what may be cached; however, WinINet determines what is actually cached based on the following criterion:</span></span>

-   <span data-ttu-id="50880-115">WinINet 只會快取 HTTP 和 FTP 回應。</span><span class="sxs-lookup"><span data-stu-id="50880-115">WinINet only caches HTTP and FTP responses.</span></span>
-   <span data-ttu-id="50880-116">快取只會儲存效能良好的回應，並在後續要求的回復中使用。</span><span class="sxs-lookup"><span data-stu-id="50880-116">Only well behaved responses may be stored by a cache and used in a reply to a subsequent Request.</span></span> <span data-ttu-id="50880-117">效能良好的回應會定義為成功傳回的回應。</span><span class="sxs-lookup"><span data-stu-id="50880-117">Well behaved responses are defined as responses that return successfully.</span></span>
-   <span data-ttu-id="50880-118">根據預設，WinINet 會快取成功的回應，除非伺服器的快取控制指示詞，或應用程式定義的旗標明確表示回應可能不會被快取。</span><span class="sxs-lookup"><span data-stu-id="50880-118">By default, WinINet will cache successful responses unless either a cache-control directive from the server, or an application-defined flag specifically denote that the response may not be cached.</span></span>
-   <span data-ttu-id="50880-119">一般來說，如果符合上述需求，則會快取 GET 動詞命令的回應。</span><span class="sxs-lookup"><span data-stu-id="50880-119">In general, responses to the GET verb are cached if the requirements listed above are met.</span></span> <span data-ttu-id="50880-120">在任何情況下，都不會快取 PUT 和 POST 動詞命令的回應。</span><span class="sxs-lookup"><span data-stu-id="50880-120">Responses to PUT and POST verbs are not cached under any circumstances.</span></span>
-   <span data-ttu-id="50880-121">即使快取已滿，也會快取專案。</span><span class="sxs-lookup"><span data-stu-id="50880-121">Items will be cached even when the cache is full.</span></span> <span data-ttu-id="50880-122">如果加入的專案會將快取置於大小限制，則會排程快取清除程式。</span><span class="sxs-lookup"><span data-stu-id="50880-122">If an added item is puts the cache over the size limit, the cache scavenger is scheduled.</span></span> <span data-ttu-id="50880-123">依預設，不保證專案在快取中保持超過10分鐘。</span><span class="sxs-lookup"><span data-stu-id="50880-123">By default, items are not guaranteed to remain more than 10 minutes in the cache.</span></span> <span data-ttu-id="50880-124">如需詳細資訊，請參閱 [下面的快](#cache-scavenger) 取清除程式一節。</span><span class="sxs-lookup"><span data-stu-id="50880-124">For more information, see the [Cache Scavenger](#cache-scavenger) section below.</span></span>
-   <span data-ttu-id="50880-125">預設會快取 Https。</span><span class="sxs-lookup"><span data-stu-id="50880-125">Https is cached by default.</span></span> <span data-ttu-id="50880-126">這是由應用程式定義的快取指示詞無法覆寫的全域設定所管理。</span><span class="sxs-lookup"><span data-stu-id="50880-126">This is managed by a global setting that cannot be overridden by application-defined cache directives.</span></span> <span data-ttu-id="50880-127">若要覆寫全域設定，請在 [控制台] 中選取 [網際網路選項] 小程式，然後移至 [advanced] 索引標籤。核取 [安全性] 區段下的 [不要將加密的頁面儲存到磁片] 方塊。</span><span class="sxs-lookup"><span data-stu-id="50880-127">To override the global setting, select the Internet Options applet in the control panel, and go to the advanced tab. Check the "Do not save encrypted pages to disk" box under the "Security" section.</span></span>

## <a name="cache-scavenger"></a><span data-ttu-id="50880-128">快取清除</span><span class="sxs-lookup"><span data-stu-id="50880-128">Cache Scavenger</span></span>

<span data-ttu-id="50880-129">快取清除清理會定期從快取中清除專案。</span><span class="sxs-lookup"><span data-stu-id="50880-129">The cache scavenger periodically cleans items from the cache.</span></span> <span data-ttu-id="50880-130">如果將專案新增至快取，且快取已滿，則會將專案新增至快取，並排程快取清除程式。</span><span class="sxs-lookup"><span data-stu-id="50880-130">If an item is added to the cache and the cache is full, the item is added to the cache and the cache scavenger is scheduled.</span></span> <span data-ttu-id="50880-131">如果快取清除程式完成一輪清除，而且快取尚未達到快取限制，則在另一個專案加入至快取時，會將清除程式排定為另一個四捨五入。</span><span class="sxs-lookup"><span data-stu-id="50880-131">If the cache scavenger completes a round of scavenging and the cache has not reached the cache limit, the scavenger is scheduled for another round when another item is added to the cache.</span></span> <span data-ttu-id="50880-132">一般情況下，清除程式會在新增的專案將快取置於其大小限制時進行排程。</span><span class="sxs-lookup"><span data-stu-id="50880-132">In general, the scavenger is scheduled when an added item puts the cache over its size limit.</span></span> <span data-ttu-id="50880-133">根據預設，快取中的最短存留時間會設定為10分鐘，除非在快取控制指示詞中另有指定。</span><span class="sxs-lookup"><span data-stu-id="50880-133">By default, the minimum time to live in the cache is set to 10 minutes unless otherwise specified in a cache-control directive.</span></span> <span data-ttu-id="50880-134">快取清除程式啟動時，不保證最舊的專案是要從快取中刪除的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="50880-134">When the cache scavenger is initiated, there is no guarantee that the oldest items are the first to be deleted from the cache.</span></span>

<span data-ttu-id="50880-135">快取會在電腦上的所有 WinINet 應用程式中，針對相同的使用者共用。</span><span class="sxs-lookup"><span data-stu-id="50880-135">The cache is shared across all WinINet applications on the computer for the same user.</span></span> <span data-ttu-id="50880-136">從 Windows Vista 和 Windows Server 2008 開始，快取大小設定為 1/第32磁片的大小，最小大小為8MB，大小上限為50MB。</span><span class="sxs-lookup"><span data-stu-id="50880-136">Starting with Windows Vista and Windows Server 2008 the cache size is set to 1/32nd the size of the disk, with a minimum size of 8MB and a maximum size of 50MB.</span></span>

## <a name="using-flags-to-control-caching"></a><span data-ttu-id="50880-137">使用旗標來控制快取</span><span class="sxs-lookup"><span data-stu-id="50880-137">Using Flags to Control Caching</span></span>

<span data-ttu-id="50880-138">快取旗標可讓應用程式控制其使用快取的時機和方式。</span><span class="sxs-lookup"><span data-stu-id="50880-138">The caching flags allow an application to control when and how it uses the cache.</span></span> <span data-ttu-id="50880-139">這些旗標可以單獨使用，也可以與存取網際網路上的資訊或資源的函式中的 *dwFlags* 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="50880-139">These flags can be used alone or in combination with the *dwFlags* parameter in functions that access information or resources on the Internet.</span></span> <span data-ttu-id="50880-140">根據預設，這些函式會儲存從網際網路下載的所有資料。</span><span class="sxs-lookup"><span data-stu-id="50880-140">By default, the functions store all data downloaded from the Internet.</span></span>

<span data-ttu-id="50880-141">您可以使用下列旗標來控制快取。</span><span class="sxs-lookup"><span data-stu-id="50880-141">The following flags can be used to control caching.</span></span>



| <span data-ttu-id="50880-142">值</span><span class="sxs-lookup"><span data-stu-id="50880-142">Value</span></span>                                                                                                                                                  | <span data-ttu-id="50880-143">意義</span><span class="sxs-lookup"><span data-stu-id="50880-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50880-144">**網際網路旗標快取 \_ \_ \_ 非同步**</span><span class="sxs-lookup"><span data-stu-id="50880-144">**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>](api-flags.md)                                                                            | <span data-ttu-id="50880-145">此旗標無效。</span><span class="sxs-lookup"><span data-stu-id="50880-145">This flag has no effect.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="50880-146">**\_ \_ \_ \_ 網路 \_ 失敗時的網際網路旗標快取**</span><span class="sxs-lookup"><span data-stu-id="50880-146">**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>](api-flags.md)                                                              | <span data-ttu-id="50880-147">如果資源的網路要求因 [ \_ 網際網路連線 \_ \_ 重設錯誤](wininet-errors.md) 或 [ \_ 網際網路 \_ 無法 \_ 連線](wininet-errors.md) 錯誤而失敗，則會從快取傳回資源。</span><span class="sxs-lookup"><span data-stu-id="50880-147">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="50880-148">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="50880-148">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                                                                              |
| [<span data-ttu-id="50880-149">**網際網路旗標不快取 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="50880-149">**INTERNET\_FLAG\_DONT\_CACHE**</span></span>](api-flags.md)                                                                              | <span data-ttu-id="50880-150">不會快取資料，無論是在本機或任何閘道中。</span><span class="sxs-lookup"><span data-stu-id="50880-150">Does not cache the data, either locally or in any gateways.</span></span> <span data-ttu-id="50880-151">與慣用值相同， [**網際網路 \_ 旗標 \_ 無 \_ \_**](api-flags.md)快取寫入。</span><span class="sxs-lookup"><span data-stu-id="50880-151">Identical to the preferred value, [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | <span data-ttu-id="50880-152">表示這是表單提交。</span><span class="sxs-lookup"><span data-stu-id="50880-152">Indicates that this is a Forms submission.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="50880-153">[**網際網路 \_\_ \_ 來自**](api-flags.md)快取 [**網際網路 \_ 旗標 \_ 表單 \_ 提交** 的旗標](api-flags.md)</span><span class="sxs-lookup"><span data-stu-id="50880-153">[**INTERNET\_FLAG\_FROM\_CACHE**](api-flags.md)[**INTERNET\_FLAG\_FORMS\_SUBMIT**](api-flags.md)</span></span> | <span data-ttu-id="50880-154">不會發出網路要求。</span><span class="sxs-lookup"><span data-stu-id="50880-154">Does not make network requests.</span></span> <span data-ttu-id="50880-155">所有實體都會從快取傳回。</span><span class="sxs-lookup"><span data-stu-id="50880-155">All entities are returned from the cache.</span></span> <span data-ttu-id="50880-156">如果要求的專案不在快取中， \_ \_ 則會傳回適當的錯誤，例如找不到錯誤檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="50880-156">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="50880-157">只有 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函式會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="50880-157">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>                                                                                                                                                                                                       |
| [<span data-ttu-id="50880-158">**網際網路 \_ 旗標 \_ FWD \_ 回**</span><span class="sxs-lookup"><span data-stu-id="50880-158">**INTERNET\_FLAG\_FWD\_BACK**</span></span>](api-flags.md)                                                                                  | <span data-ttu-id="50880-159">指出函式應使用目前在網際網路快取中的資源複本。</span><span class="sxs-lookup"><span data-stu-id="50880-159">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="50880-160">不會檢查資源的到期日和其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-160">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="50880-161">如果在網際網路快取中找不到要求的專案，系統會嘗試找出網路上的資源。</span><span class="sxs-lookup"><span data-stu-id="50880-161">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="50880-162">此值是在 Microsoft Internet Explorer 5 中引進，並與 Internet Explorer 的 [ **向前** ] 和 [ **上一頁** ] 按鈕作業相關聯。</span><span class="sxs-lookup"><span data-stu-id="50880-162">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span> |
| [<span data-ttu-id="50880-163">**網際網路 \_ 旗標 \_ 超連結**</span><span class="sxs-lookup"><span data-stu-id="50880-163">**INTERNET\_FLAG\_HYPERLINK**</span></span>](api-flags.md)                                                                                 | <span data-ttu-id="50880-164">如果資源儲存在快取中，則會強制應用程式重載資源（如果沒有過期時間），而且不會傳回上次修改時間。</span><span class="sxs-lookup"><span data-stu-id="50880-164">Forces the application to reload a resource if no expire time and no last-modified time were returned when the resource was stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="50880-165">**網際網路 \_ 旗標 \_ 設為 \_ 持續**</span><span class="sxs-lookup"><span data-stu-id="50880-165">**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>](api-flags.md)                                                                    | <span data-ttu-id="50880-166">不再支援。</span><span class="sxs-lookup"><span data-stu-id="50880-166">No longer supported.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="50880-167">**網際網路 \_ 旗標必須快取 \_ \_ \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="50880-167">**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>](api-flags.md)                                                             | <span data-ttu-id="50880-168">如果無法快取檔案，則會建立暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-168">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="50880-169">這與慣用的值相同，也就是 [**網際網路 \_ 旗標 \_ 需要 \_**](api-flags.md)的檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-169">This is identical to the preferred value, [**INTERNET\_FLAG\_NEED\_FILE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="50880-170">**網際網路 \_ 旗標 \_ 需要檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="50880-170">**INTERNET\_FLAG\_NEED\_FILE**</span></span>](api-flags.md)                                                                                | <span data-ttu-id="50880-171">如果無法快取檔案，則會建立暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-171">Causes a temporary file to be created if the file cannot be cached.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="50880-172">**網際網路 \_ 旗標無快取 \_ \_ \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="50880-172">**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>](api-flags.md)                                                                     | <span data-ttu-id="50880-173">拒絕函數嘗試在快取中儲存從網際網路下載的資料。</span><span class="sxs-lookup"><span data-stu-id="50880-173">Rejects any attempt by the function to store data downloaded from the Internet in the cache.</span></span> <span data-ttu-id="50880-174">如果應用程式不想將任何下載的資源儲存在本機，則需要此旗標。</span><span class="sxs-lookup"><span data-stu-id="50880-174">This flag is necessary if the application does not want any downloaded resources to be stored locally.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="50880-175">**網際網路 \_ 旗標 \_ 無 \_ UI**</span><span class="sxs-lookup"><span data-stu-id="50880-175">**INTERNET\_FLAG\_NO\_UI**</span></span>](api-flags.md)                                                                                        | <span data-ttu-id="50880-176">停用 cookie 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="50880-176">Disables the cookie dialog box.</span></span> <span data-ttu-id="50880-177">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)只可使用此旗標 (HTTP 要求) 。</span><span class="sxs-lookup"><span data-stu-id="50880-177">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="50880-178">**網際網路 \_ 旗標 \_ 離線**</span><span class="sxs-lookup"><span data-stu-id="50880-178">**INTERNET\_FLAG\_OFFLINE**</span></span>](api-flags.md)                                                                                     | <span data-ttu-id="50880-179">防止應用程式將要求傳送至網路。</span><span class="sxs-lookup"><span data-stu-id="50880-179">Prevents the application from sending requests to the network.</span></span> <span data-ttu-id="50880-180">所有要求都是使用儲存在快取中的資源來解決。</span><span class="sxs-lookup"><span data-stu-id="50880-180">All requests are resolved using the resources stored in the cache.</span></span> <span data-ttu-id="50880-181">如果資源不在快取中， \_ \_ 則會傳回適當的錯誤，例如找不 \_ 到錯誤檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-181">If the resource is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="50880-182">**網際網路 \_ 旗標 \_ PRAGMA \_ NOCACHE**</span><span class="sxs-lookup"><span data-stu-id="50880-182">**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>](api-flags.md)                                                                      | <span data-ttu-id="50880-183">強制源伺服器解析要求，即使 proxy 上有快取的複本也一樣。</span><span class="sxs-lookup"><span data-stu-id="50880-183">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="50880-184">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)函式只 (HTTP 和 HTTPS 要求) 且 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)函式使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="50880-184">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="50880-185">**網際網路 \_ 旗標 \_ 重載**</span><span class="sxs-lookup"><span data-stu-id="50880-185">**INTERNET\_FLAG\_RELOAD**</span></span>](api-flags.md)                                                                                       | <span data-ttu-id="50880-186">強制函式直接從網際網路取出要求的資源。</span><span class="sxs-lookup"><span data-stu-id="50880-186">Forces the function to retrieve the requested resource directly from the Internet.</span></span> <span data-ttu-id="50880-187">所下載的資訊會儲存在快取中。</span><span class="sxs-lookup"><span data-stu-id="50880-187">The information that is downloaded is stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="50880-188">**網際網路 \_ 旗標重新 \_ 同步處理**</span><span class="sxs-lookup"><span data-stu-id="50880-188">**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>](api-flags.md)                                                                         | <span data-ttu-id="50880-189">讓應用程式從網際網路執行資源的條件式下載。</span><span class="sxs-lookup"><span data-stu-id="50880-189">Causes an application to perform a conditional download of the resource from the Internet.</span></span> <span data-ttu-id="50880-190">如果儲存在快取中的版本是最新的，則會從快取下載資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-190">If the version stored in the cache is current, the information is downloaded from the cache.</span></span> <span data-ttu-id="50880-191">否則，就會從伺服器重載資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-191">Otherwise, the information is reloaded from the server.</span></span>                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a><span data-ttu-id="50880-192">持續性快取函數</span><span class="sxs-lookup"><span data-stu-id="50880-192">Persistent Caching Functions</span></span>

<span data-ttu-id="50880-193">需要持續性快取服務的用戶端會使用持續性快取功能，讓其應用程式將資料儲存在本機檔案系統中，以供後續使用，例如在低頻寬連結限制資料存取的情況下，或完全無法使用存取。</span><span class="sxs-lookup"><span data-stu-id="50880-193">Clients that need persistent caching services use the persistent caching functions to allow their applications to save data in the local file system for subsequent use, such as in situations where a low-bandwidth link limits access to the data, or the access is not available at all.</span></span>

<span data-ttu-id="50880-194">快取功能可提供持續性快取和離線流覽。</span><span class="sxs-lookup"><span data-stu-id="50880-194">The cache functions provide persistent caching and offline browsing.</span></span> <span data-ttu-id="50880-195">除非 [**網際網路 \_ 旗標 \_ 沒有 \_ \_**](api-flags.md) 明確指定快取的快取寫入旗標，否則函數會快取從網路下載的所有資料。</span><span class="sxs-lookup"><span data-stu-id="50880-195">Unless the [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md) flag explicitly specifies no caching, the functions cache all data downloaded from the network.</span></span> <span data-ttu-id="50880-196">不會快取張貼資料的回應。</span><span class="sxs-lookup"><span data-stu-id="50880-196">The responses to POST data are not cached.</span></span>

## <a name="using-the-persistent-url-cache-functions"></a><span data-ttu-id="50880-197">使用持續性 URL 快取函數</span><span class="sxs-lookup"><span data-stu-id="50880-197">Using the Persistent URL Cache Functions</span></span>

<span data-ttu-id="50880-198">下列持續性 URL 快取功能可讓應用程式存取和操作儲存在快取中的資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-198">The following persistent URL cache functions allow an application to access and manipulate information stored in the cache.</span></span>



| <span data-ttu-id="50880-199">函式</span><span class="sxs-lookup"><span data-stu-id="50880-199">Function</span></span>                                                           | <span data-ttu-id="50880-200">描述</span><span class="sxs-lookup"><span data-stu-id="50880-200">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50880-201">**CommitUrlCacheEntryA**</span><span class="sxs-lookup"><span data-stu-id="50880-201">**CommitUrlCacheEntryA**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | <span data-ttu-id="50880-202">快取儲存體中指定檔案的資料，並將其與指定的 URL 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="50880-202">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="50880-203">**CommitUrlCacheEntryW**</span><span class="sxs-lookup"><span data-stu-id="50880-203">**CommitUrlCacheEntryW**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | <span data-ttu-id="50880-204">快取儲存體中指定檔案的資料，並將其與指定的 URL 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="50880-204">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="50880-205">**CreateUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="50880-205">**CreateUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | <span data-ttu-id="50880-206">配置要求的快取儲存體，並建立本機檔案名以儲存對應于來源名稱的快取專案。</span><span class="sxs-lookup"><span data-stu-id="50880-206">Allocates the requested cache storage and creates a local file name for saving the cache entry that corresponds to the source name.</span></span>                           |
| [<span data-ttu-id="50880-207">**CreateUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="50880-207">**CreateUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | <span data-ttu-id="50880-208">產生快取群組識別。</span><span class="sxs-lookup"><span data-stu-id="50880-208">Generates a cache group identification.</span></span>                                                                                                                       |
| [<span data-ttu-id="50880-209">**DeleteUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="50880-209">**DeleteUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | <span data-ttu-id="50880-210">如果檔案存在，則從快取中移除與來源名稱相關聯的檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-210">Removes the file associated with the source name from the cache, if the file exists.</span></span>                                                                          |
| [<span data-ttu-id="50880-211">**DeleteUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="50880-211">**DeleteUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | <span data-ttu-id="50880-212">釋放在快取索引檔中的 **GROUPID** 和任何相關聯的狀態。</span><span class="sxs-lookup"><span data-stu-id="50880-212">Releases a **GROUPID** and any associated state in the cache index file.</span></span>                                                                                      |
| [<span data-ttu-id="50880-213">**FindCloseUrlCache**</span><span class="sxs-lookup"><span data-stu-id="50880-213">**FindCloseUrlCache**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | <span data-ttu-id="50880-214">關閉指定的列舉控制碼。</span><span class="sxs-lookup"><span data-stu-id="50880-214">Closes the specified enumeration handle.</span></span>                                                                                                                      |
| [<span data-ttu-id="50880-215">**FindFirstUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="50880-215">**FindFirstUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | <span data-ttu-id="50880-216">開始快取的列舉。</span><span class="sxs-lookup"><span data-stu-id="50880-216">Begins the enumeration of the cache.</span></span>                                                                                                                          |
| [<span data-ttu-id="50880-217">**FindFirstUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="50880-217">**FindFirstUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | <span data-ttu-id="50880-218">開始已篩選的快取列舉。</span><span class="sxs-lookup"><span data-stu-id="50880-218">Begins a filtered enumeration of the cache.</span></span>                                                                                                                   |
| [<span data-ttu-id="50880-219">**FindNextUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="50880-219">**FindNextUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | <span data-ttu-id="50880-220">抓取快取中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="50880-220">Retrieves the next entry in the cache.</span></span>                                                                                                                        |
| [<span data-ttu-id="50880-221">**FindNextUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="50880-221">**FindNextUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | <span data-ttu-id="50880-222">抓取已篩選快取列舉中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="50880-222">Retrieves the next entry in a filtered cache enumeration.</span></span>                                                                                                     |
| [<span data-ttu-id="50880-223">**GetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="50880-223">**GetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | <span data-ttu-id="50880-224">抓取快取專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-224">Retrieves information about a cache entry.</span></span>                                                                                                                    |
| [<span data-ttu-id="50880-225">**GetUrlCacheEntryInfoEx**</span><span class="sxs-lookup"><span data-stu-id="50880-225">**GetUrlCacheEntryInfoEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | <span data-ttu-id="50880-226">在轉譯任何會以離線模式套用的快取重新導向（ [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)）之後，搜尋 URL。</span><span class="sxs-lookup"><span data-stu-id="50880-226">Searches for the URL after translating any cached redirections that would be applied in offline mode by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>           |
| [<span data-ttu-id="50880-227">**ReadUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="50880-227">**ReadUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | <span data-ttu-id="50880-228">從使用 [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)開啟的資料流程讀取快取的資料。</span><span class="sxs-lookup"><span data-stu-id="50880-228">Reads the cached data from a stream that has been opened using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                            |
| [<span data-ttu-id="50880-229">**RetrieveUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="50880-229">**RetrieveUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | <span data-ttu-id="50880-230">從快取中，以檔案的形式抓取快取專案。</span><span class="sxs-lookup"><span data-stu-id="50880-230">Retrieves a cache entry from the cache in the form of a file.</span></span>                                                                                                 |
| [<span data-ttu-id="50880-231">**RetrieveUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="50880-231">**RetrieveUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | <span data-ttu-id="50880-232">提供最有效率、獨立執行的方式來存取快取資料。</span><span class="sxs-lookup"><span data-stu-id="50880-232">Provides the most efficient and implementation-independent way of accessing the cache data.</span></span>                                                                   |
| [<span data-ttu-id="50880-233">**SetUrlCacheEntryGroup**</span><span class="sxs-lookup"><span data-stu-id="50880-233">**SetUrlCacheEntryGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | <span data-ttu-id="50880-234">從快取群組新增或移除專案。</span><span class="sxs-lookup"><span data-stu-id="50880-234">Adds or removes entries from a cache group.</span></span>                                                                                                                   |
| [<span data-ttu-id="50880-235">**SetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="50880-235">**SetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | <span data-ttu-id="50880-236">設定網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構的指定成員。</span><span class="sxs-lookup"><span data-stu-id="50880-236">Sets the specified members of the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span>                                                |
| [<span data-ttu-id="50880-237">**UnlockUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="50880-237">**UnlockUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | <span data-ttu-id="50880-238">從 [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)抓取檔案時鎖定的快取專案解除鎖定，以供快取使用。</span><span class="sxs-lookup"><span data-stu-id="50880-238">Unlocks the cache entry that was locked when the file was retrieved for use from the cache by [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span></span> |
| [<span data-ttu-id="50880-239">**UnlockUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="50880-239">**UnlockUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | <span data-ttu-id="50880-240">關閉使用 [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)取出的資料流程。</span><span class="sxs-lookup"><span data-stu-id="50880-240">Closes the stream that has been retrieved using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                                           |



 

### <a name="enumerating-the-cache"></a><span data-ttu-id="50880-241">列舉快取</span><span class="sxs-lookup"><span data-stu-id="50880-241">Enumerating the Cache</span></span>

<span data-ttu-id="50880-242">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)和 [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)函數會列舉儲存在快取中的資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-242">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) and [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) functions enumerate the information stored in the cache.</span></span> <span data-ttu-id="50880-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) 會藉由採用搜尋模式、緩衝區和緩衝區大小來建立控制碼，並傳回第一個快取專案，來啟動列舉。</span><span class="sxs-lookup"><span data-stu-id="50880-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) starts the enumeration by taking a search pattern, a buffer, and a buffer size to create a handle and return the first cache entry.</span></span> <span data-ttu-id="50880-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) 會採用 [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)、緩衝區和緩衝區大小所建立的控制碼，以傳回下一個快取專案。</span><span class="sxs-lookup"><span data-stu-id="50880-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) takes the handle created by [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), a buffer, and a buffer size to return the next cache entry.</span></span>

<span data-ttu-id="50880-245">這兩個函數都會將網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構儲存在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="50880-245">Both functions store an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure in the buffer.</span></span> <span data-ttu-id="50880-246">此結構的大小會因每個專案而有所不同。</span><span class="sxs-lookup"><span data-stu-id="50880-246">The size of this structure varies for each entry.</span></span> <span data-ttu-id="50880-247">如果傳遞給其中一個函式的緩衝區大小不足，則函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤的 \_ \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="50880-247">If the buffer size passed to either function is insufficient, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="50880-248">緩衝區大小變數包含取出該快取專案所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="50880-248">The buffer size variable contains the buffer size that was needed to retrieve that cache entry.</span></span> <span data-ttu-id="50880-249">應配置緩衝區大小變數所表示之大小的緩衝區，並使用新的緩衝區再次呼叫該函式。</span><span class="sxs-lookup"><span data-stu-id="50880-249">A buffer of the size indicated by the buffer size variable should be allocated, and the function should be called again with the new buffer.</span></span>

<span data-ttu-id="50880-250">[**網際網路快 \_ 取 \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)結構包含結構大小、快取資訊的 URL、本機檔案名、快取專案類型、使用計數、命中率、大小、上次修改時間、到期日、上次存取、上次同步處理時間、標頭資訊、標頭資訊大小和副檔名。</span><span class="sxs-lookup"><span data-stu-id="50880-250">The [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="50880-251">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)函式會採用搜尋模式、儲存網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)結構的緩衝區，以及緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="50880-251">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) function takes a search pattern, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="50880-252">目前，只會執行預設搜尋模式，它會傳回所有快取專案。</span><span class="sxs-lookup"><span data-stu-id="50880-252">Currently, only the default search pattern, which returns all cache entries, is implemented.</span></span>

<span data-ttu-id="50880-253">列舉快取之後，應用程式應該呼叫 [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) 來關閉快取列舉控制碼。</span><span class="sxs-lookup"><span data-stu-id="50880-253">After the cache is enumerated, the application should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) to close the cache enumeration handle.</span></span>

<span data-ttu-id="50880-254">下列範例會在清單方塊中顯示每個快取專案的 URL （ **IDC \_ CacheList**）。</span><span class="sxs-lookup"><span data-stu-id="50880-254">The following example displays each cache entry's URL in a list box, **IDC\_CacheList**.</span></span> <span data-ttu-id="50880-255">它會使用最大快取 \_ \_ 專案 \_ 資訊 \_ 大小來初始配置緩衝區，因為較早版本的 WinINet API 不會正確地列舉快取。</span><span class="sxs-lookup"><span data-stu-id="50880-255">It uses MAX\_CACHE\_ENTRY\_INFO\_SIZE to initially allocate a buffer, since early versions of the WinINet API do not enumerate the cache properly otherwise.</span></span> <span data-ttu-id="50880-256">較新的版本會正確地列舉快取，而且沒有快取大小的限制。</span><span class="sxs-lookup"><span data-stu-id="50880-256">Later versions do enumerate the cache properly and there is no cache size limit.</span></span> <span data-ttu-id="50880-257">在具有 Internet Explorer 4.0 之 WinINet API 版本的電腦上執行的所有應用程式，都必須配置所需大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="50880-257">All applications that run on computers with the version of the WinINet API from Internet Explorer 4.0 must allocate a buffer of the required size.</span></span> <span data-ttu-id="50880-258">如需詳細資訊，請參閱 [使用緩衝區](appendix-b-using-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="50880-258">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a><span data-ttu-id="50880-259">正在抓取快取專案資訊</span><span class="sxs-lookup"><span data-stu-id="50880-259">Retrieving Cache Entry Information</span></span>

<span data-ttu-id="50880-260">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)函式可讓您針對指定的 URL 取得網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)結構。</span><span class="sxs-lookup"><span data-stu-id="50880-260">The [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) function lets you retrieve the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure for the specified URL.</span></span> <span data-ttu-id="50880-261">此結構包含結構大小、快取資訊的 URL、本機檔案名、快取專案類型、使用計數、命中率、大小、上次修改時間、到期日、上次存取、上次同步處理時間、標頭資訊、標頭資訊大小和副檔名。</span><span class="sxs-lookup"><span data-stu-id="50880-261">This structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="50880-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) 接受 URL、網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構的緩衝區，以及緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="50880-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accepts a URL, a buffer for an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="50880-263">如果找到 URL，則會將資訊複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="50880-263">If the URL is found, the information is copied into the buffer.</span></span> <span data-ttu-id="50880-264">否則，函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 \_ \_ \_ 找不到的錯誤檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-264">Otherwise, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="50880-265">如果緩衝區大小不足以儲存快取專案資訊，則函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤的 \_ \_ 緩衝區不足。</span><span class="sxs-lookup"><span data-stu-id="50880-265">If the buffer size is insufficient to store the cache entry information, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="50880-266">取得資訊所需的大小會儲存在緩衝區大小變數中。</span><span class="sxs-lookup"><span data-stu-id="50880-266">The size required to retrieve the information is stored in the buffer size variable.</span></span>

<span data-ttu-id="50880-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) 不會進行任何 URL 剖析，因此在快取中找不到包含錨點 () 的 url \# ，即使資源已快取也是一樣。</span><span class="sxs-lookup"><span data-stu-id="50880-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="50880-268">例如，如果傳遞 URL " https://example.com/example.htm\#sample "，則函式會傳回錯誤檔案 \_ ， \_ \_ 即使 " https://example.com/example.htm " 在快取中也是一樣。</span><span class="sxs-lookup"><span data-stu-id="50880-268">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="50880-269">下列範例會針對指定的 URL 抓取快取專案資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-269">The following example retrieves the cache entry information for the specified URL.</span></span> <span data-ttu-id="50880-270">然後，此函式會在 **IDC \_ CacheDump** 編輯方塊中顯示標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-270">The function then displays the header information in the **IDC\_CacheDump** edit box.</span></span>


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a><span data-ttu-id="50880-271">建立快取專案</span><span class="sxs-lookup"><span data-stu-id="50880-271">Creating a Cache Entry</span></span>

<span data-ttu-id="50880-272">應用程式會使用 [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) 和 [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) 函數來建立快取專案。</span><span class="sxs-lookup"><span data-stu-id="50880-272">An application uses the [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) and [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) functions to create a cache entry.</span></span>

<span data-ttu-id="50880-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) 接受 URL、預期的檔案大小和副檔名。</span><span class="sxs-lookup"><span data-stu-id="50880-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accepts the URL, expected file size, and file name extension.</span></span> <span data-ttu-id="50880-274">然後，此函式會建立本機檔案名，以儲存對應至 URL 和副檔名的快取專案。</span><span class="sxs-lookup"><span data-stu-id="50880-274">The function then creates a local file name for saving the cache entry that corresponds to the URL and file name extension.</span></span>

<span data-ttu-id="50880-275">使用本機檔案名，將資料寫入本機檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-275">Using the local file name, write the data into the local file.</span></span> <span data-ttu-id="50880-276">將資料寫入本機檔案之後，應用程式應該呼叫 [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)。</span><span class="sxs-lookup"><span data-stu-id="50880-276">After the data has been written to the local file, the application should call [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>

<span data-ttu-id="50880-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) 接受 URL、本機檔案名、到期日、上次修改時間、快取專案類型、標頭資訊、標頭資訊大小和副檔名。</span><span class="sxs-lookup"><span data-stu-id="50880-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accepts the URL, local file name, expiration, last modified time, cache entry type, header information, header information size, and file name extension.</span></span> <span data-ttu-id="50880-278">然後，此函式會將資料快取在快取儲存體中指定的檔案中，並將其與指定的 URL 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="50880-278">The function then caches data in the file specified in the cache storage and associates it with the given URL.</span></span>

<span data-ttu-id="50880-279">下列範例會使用先前呼叫 [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)所建立的本機檔案名（儲存在 [ **\_ LocalFile**] 文字方塊中），在快取專案中儲存文字方塊中的文字（ **idc \_ CacheDump**）。</span><span class="sxs-lookup"><span data-stu-id="50880-279">The following example uses the local file name, created by a previous call to [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), stored in the text box, **IDC\_LocalFile**, to store the text from the text box, **IDC\_CacheDump**, in the cache entry.</span></span> <span data-ttu-id="50880-280">使用 **fopen**、 **fprintf** 和 **fclose** 將資料寫入檔案之後，會使用 [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)來認可該專案。</span><span class="sxs-lookup"><span data-stu-id="50880-280">After the data has been written to the file using **fopen**, **fprintf**, and **fclose**, the entry is committed using [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a><span data-ttu-id="50880-281">刪除快取專案</span><span class="sxs-lookup"><span data-stu-id="50880-281">Deleting a Cache Entry</span></span>

<span data-ttu-id="50880-282">[**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)函式會使用 URL 並移除與其相關聯的快取檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-282">The [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) function takes a URL and removes the cache file associated with it.</span></span> <span data-ttu-id="50880-283">如果快取檔案不存在，此函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會 \_ 傳回 \_ \_ 找不到的錯誤檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-283">If the cache file does not exist, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="50880-284">如果快取檔案目前已鎖定或正在使用中，則函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 \_ 拒絕存取錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="50880-284">If the cache file is currently locked or in use, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="50880-285">解除鎖定時，會刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-285">The file is deleted when unlocked.</span></span>

### <a name="retrieving-cache-entry-files"></a><span data-ttu-id="50880-286">正在抓取快取專案檔</span><span class="sxs-lookup"><span data-stu-id="50880-286">Retrieving Cache Entry Files</span></span>

<span data-ttu-id="50880-287">如果應用程式需要資源的檔案名，請使用 [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) 和 [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) 函數。</span><span class="sxs-lookup"><span data-stu-id="50880-287">For applications that require the file name of a resource, use the [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) and [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) functions.</span></span> <span data-ttu-id="50880-288">不需要檔案名的應用程式應該使用 [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)、 [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)和 [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) 函式來取得快取中的資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-288">Applications that do not require the file name should use the [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream), and [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) functions to retrieve the information in the cache.</span></span>

<span data-ttu-id="50880-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) 不會進行任何 URL 剖析，因此在快取中找不到包含錨點 () 的 url \# ，即使資源已快取也是一樣。</span><span class="sxs-lookup"><span data-stu-id="50880-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="50880-290">例如，如果傳遞 URL " https://example.com/example.htm\#sample "，則函式會傳回錯誤檔案 \_ ， \_ \_ 即使 " https://example.com/example.htm " 在快取中也是一樣。</span><span class="sxs-lookup"><span data-stu-id="50880-290">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="50880-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) 接受 URL、儲存網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構的緩衝區，以及緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="50880-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accepts a URL, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="50880-292">函式會針對呼叫端取得和鎖定。</span><span class="sxs-lookup"><span data-stu-id="50880-292">The function is retrieved and locked for the caller.</span></span>

<span data-ttu-id="50880-293">使用檔案中的資訊之後，應用程式應該呼叫 [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) 來解除鎖定檔案。</span><span class="sxs-lookup"><span data-stu-id="50880-293">After the information in the file has been used, the application should call [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) to unlock the file.</span></span>

### <a name="cache-groups"></a><span data-ttu-id="50880-294">快取群組</span><span class="sxs-lookup"><span data-stu-id="50880-294">Cache Groups</span></span>

<span data-ttu-id="50880-295">若要建立快取群組，必須呼叫 [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) 函數來產生快取群組的 **GROUPID** 。</span><span class="sxs-lookup"><span data-stu-id="50880-295">To create a cache group, the [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) function must be called to generate a **GROUPID** for the cache group.</span></span> <span data-ttu-id="50880-296">您可以藉由提供快取專案的 URL 和網際網路快取 \_ \_ 群組，將旗標新增 \_ 至 [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) 函式，將專案新增至快取群組。</span><span class="sxs-lookup"><span data-stu-id="50880-296">Entries can be added to the cache group by supplying the cache entry's URL and the INTERNET\_CACHE\_GROUP\_ADD flag to the [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) function.</span></span> <span data-ttu-id="50880-297">若要從群組中移除快取專案，請將快取專案的 URL 和 INTERNET \_ cache \_ group remove 旗標傳遞 \_ 給 [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)。</span><span class="sxs-lookup"><span data-stu-id="50880-297">To remove a cache entry from a group, pass the cache entry's URL and the INTERNET\_CACHE\_GROUP\_REMOVE flag to [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span></span>

<span data-ttu-id="50880-298">[**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)和 [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)函數可用來列舉指定之快取群組中的專案。</span><span class="sxs-lookup"><span data-stu-id="50880-298">The [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) and [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) functions can be used to enumerate the entries in a specified cache group.</span></span> <span data-ttu-id="50880-299">列舉完成之後，函式應該呼叫 [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)。</span><span class="sxs-lookup"><span data-stu-id="50880-299">After the enumeration is complete, the function should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span></span>

## <a name="handling-structures-with-variable-size-information"></a><span data-ttu-id="50880-300">處理具有變數大小資訊的結構</span><span class="sxs-lookup"><span data-stu-id="50880-300">Handling Structures with Variable Size Information</span></span>

<span data-ttu-id="50880-301">快取可包含每個儲存的 URL 的變數大小資訊。</span><span class="sxs-lookup"><span data-stu-id="50880-301">The cache can contain variable size information for each URL stored.</span></span> <span data-ttu-id="50880-302">這會反映在 [**網際網路快 \_ 取 \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構中。</span><span class="sxs-lookup"><span data-stu-id="50880-302">This is reflected in the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span> <span data-ttu-id="50880-303">當快取函式傳回此結構時，會建立一律為網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 大小加上任何變數大小資訊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="50880-303">When the cache functions return this structure, they create a buffer that is always the size of [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) plus any variable size information.</span></span> <span data-ttu-id="50880-304">如果指標成員不是 **Null**，它會指向緊接在結構後面的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="50880-304">If a pointer member is not **NULL**, it points to the memory area immediately after the structure.</span></span> <span data-ttu-id="50880-305">將函式所傳回的緩衝區複製到另一個緩衝區時，指標成員應固定為指向新緩衝區中的適當位置，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="50880-305">While copying the buffer returned by a function into another buffer, the pointer members should be fixed to point to the appropriate place in the new buffer, as the following example shows.</span></span>

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

<span data-ttu-id="50880-306">\_ \_ 如果您指定的緩衝區太小而無法包含函式所抓取的快取專案資訊，某些快取函數會失敗，並出現錯誤緩衝區錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="50880-306">Some cache functions fail with the ERROR\_INSUFFICIENT\_BUFFER error message if you specify a buffer that is too small to contain the cache entry information retrieved by the function.</span></span> <span data-ttu-id="50880-307">在此情況下，函式也會傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="50880-307">In this case, the function also returns the required size of the buffer.</span></span> <span data-ttu-id="50880-308">然後，您可以配置適當大小的緩衝區，然後再次呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="50880-308">You can then allocate a buffer of the appropriate size and call the function again.</span></span>

> [!Note]  
> <span data-ttu-id="50880-309">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="50880-309">WinINet does not support server implementations.</span></span> <span data-ttu-id="50880-310">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="50880-310">In addition, it should not be used from a service.</span></span> <span data-ttu-id="50880-311">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="50880-311">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
