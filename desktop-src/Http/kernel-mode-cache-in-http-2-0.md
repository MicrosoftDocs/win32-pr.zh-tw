---
title: 核心模式快取
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021988"
---
# <a name="kernel-mode-cache"></a><span data-ttu-id="b4c6c-103">核心模式快取</span><span class="sxs-lookup"><span data-stu-id="b4c6c-103">Kernel Mode Cache</span></span>

<span data-ttu-id="b4c6c-104">HTTP 伺服器版本 2.0 API 可讓應用程式以核心模式快取靜態內容的回應。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-104">The HTTP Server version 2.0 API allows applications to cache responses with static content in kernel mode.</span></span> <span data-ttu-id="b4c6c-105">從核心快取提供要求而不轉換為使用者模式時，可以達到更高的效能。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-105">Increased performance is achieved when requests are served from the kernel cache without transitioning to user mode.</span></span>

<span data-ttu-id="b4c6c-106">HTTP 伺服器 API 會將適當的屬性設定套用至從核心快取提供的所有要求，包括記錄回應。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-106">The HTTP Server API applies the appropriate property configurations to all requests served from the kernel cache, including logging responses.</span></span> <span data-ttu-id="b4c6c-107">不過，需要驗證的要求將無法從快取中提供。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-107">Requests that require authentication, however, will not be served from the cache.</span></span>

<span data-ttu-id="b4c6c-108">HTTP 伺服器 API 會將核心模式快取限制為符合下列條件的要求：</span><span class="sxs-lookup"><span data-stu-id="b4c6c-108">The HTTP Server API limits the kernel mode cache to requests that meet the following conditions:</span></span>

-   <span data-ttu-id="b4c6c-109">要求動詞命令為 GET，而且會收到整個要求。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-109">The request verb is GET and the entire request is received.</span></span>
-   <span data-ttu-id="b4c6c-110">要求不能有實體主體。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-110">The request must not have an entity body.</span></span>
-   <span data-ttu-id="b4c6c-111">HTTP 通訊協定是1.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-111">The HTTP protocol is version 1.0 or later.</span></span>
-   <span data-ttu-id="b4c6c-112">"翻譯： f" 標頭不存在。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-112">The "Translate: f " header is not present.</span></span>
-   <span data-ttu-id="b4c6c-113">預期不會出現 "預期： 100-Continue" 以外的標頭。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-113">Expect headers other than "Expect: 100-Continue" are not present.</span></span>
-   <span data-ttu-id="b4c6c-114">授權標頭不存在。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-114">The authorization header is not present.</span></span>
-   <span data-ttu-id="b4c6c-115">範圍和 If-Range 的標頭不存在。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-115">The Range and If-Range headers are not present.</span></span>

<span data-ttu-id="b4c6c-116">除了要求的限制之外，回應也必須符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="b4c6c-116">In addition to the restrictions on the request, the response must also meet the following conditions:</span></span>

-   <span data-ttu-id="b4c6c-117">根據預設，回應大小受限於 256 KB。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-117">Response size is limited to 256 KB, by default.</span></span> <span data-ttu-id="b4c6c-118">若要變更快取回應的大小，請將 **UriMaxUriBytes** 登錄值設定為所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-118">To change the size of the response that is cached, set the **UriMaxUriBytes** registry value to the required number of bytes.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   <span data-ttu-id="b4c6c-119">您必須在 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)的單一呼叫中提供整個回應。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-119">The entire response must be provided in a single call to [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span>
-   <span data-ttu-id="b4c6c-120">回應上的日期標頭不得隱藏。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-120">The date header on the response must not be suppressed.</span></span>
-   <span data-ttu-id="b4c6c-121">如果最後修改的標頭存在，標頭的值必須具有正確的語法。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-121">If the last-modified header is present, the value of the header must have the correct syntax.</span></span> <span data-ttu-id="b4c6c-122">此標頭中的時間值會用於快取控制驗證。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-122">The time value in this header is used for cache control verification.</span></span>
-   <span data-ttu-id="b4c6c-123">核心模式快取有足夠的剩餘空間來儲存回應。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-123">The kernel mode cache has enough space left to store the response.</span></span>

<span data-ttu-id="b4c6c-124">預設會啟用核心模式回應快取。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-124">By default, kernel mode response cache is enabled.</span></span> <span data-ttu-id="b4c6c-125">如果未符合上述要求或回應的任何條件，則會傳送回應，但不會快取。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-125">If any of the conditions for the request or response listed above are not met, the response will be sent, but it will not be cached.</span></span> <span data-ttu-id="b4c6c-126">在 HTTP 伺服器版本 2.0 API 中， [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 包含選擇性的 *pCachePolicy* 參數，可傳遞 HTTP 快取 [**\_ \_ 原則**](/windows/desktop/api/Http/ns-http-http_cache_policy) 結構。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-126">In HTTP Server version 2.0 API, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) includes an optional *pCachePolicy* parameter to pass the [**HTTP\_CACHE\_POLICY**](/windows/desktop/api/Http/ns-http-http_cache_policy) structure.</span></span> <span data-ttu-id="b4c6c-127">應用程式會使用快取原則結構來設定快取。</span><span class="sxs-lookup"><span data-stu-id="b4c6c-127">Applications use the cache policy structure to configure the cache.</span></span>

 

 




