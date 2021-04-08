---
title: " (用戶端) 快取結果"
description: 用戶端快取會將結果集儲存在用戶端記憶體中，以提供用戶端的效能增強功能。
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- 快取 (用戶端) ADSI 的結果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931853"
---
# <a name="caching-the-result-client-side"></a><span data-ttu-id="8bf86-104"> (用戶端) 快取結果</span><span class="sxs-lookup"><span data-stu-id="8bf86-104">Caching the Result (Client Side)</span></span>

<span data-ttu-id="8bf86-105">用戶端快取會將結果集儲存在用戶端記憶體中，以提供用戶端的效能增強功能。</span><span class="sxs-lookup"><span data-stu-id="8bf86-105">Client-side caching stores the result set in the client memory, providing performance enhancements for the client side.</span></span> <span data-ttu-id="8bf86-106">用戶端可以重複使用物件，而不需要多次往返伺服器。</span><span class="sxs-lookup"><span data-stu-id="8bf86-106">A client can revisit an object repeatedly without multiple trips to the server.</span></span> <span data-ttu-id="8bf86-107">根據預設，ADSI 會快取用戶端的結果集。</span><span class="sxs-lookup"><span data-stu-id="8bf86-107">By default, ADSI caches the result set for the clients.</span></span> <span data-ttu-id="8bf86-108">這可讓 ADSI 提供用戶端類似 SQL 的資料指標支援。</span><span class="sxs-lookup"><span data-stu-id="8bf86-108">This enables ADSI to provide clients with SQL-like cursor support.</span></span> <span data-ttu-id="8bf86-109">您可以逐一查看指定的結果集數次。</span><span class="sxs-lookup"><span data-stu-id="8bf86-109">You may iterate through a given result set several times.</span></span>

<span data-ttu-id="8bf86-110">ADSI 也可讓用戶端關閉快取，以降低記憶體需求。</span><span class="sxs-lookup"><span data-stu-id="8bf86-110">ADSI also enables clients to turn off the cache to reduce memory requirements.</span></span> <span data-ttu-id="8bf86-111">如果用戶端快取已停用，用戶端就不會在記憶體中維護結果集。</span><span class="sxs-lookup"><span data-stu-id="8bf86-111">If client-side caching is disabled, the client does not maintain the result set in memory.</span></span> <span data-ttu-id="8bf86-112">每個資料列會在應用程式抓取之後釋放。</span><span class="sxs-lookup"><span data-stu-id="8bf86-112">Each row is freed after the application retrieves it.</span></span> <span data-ttu-id="8bf86-113">停用用戶端快取可能有助於減少用戶端記憶體需求，例如，當您只想要透過結果集進行單一傳遞時。</span><span class="sxs-lookup"><span data-stu-id="8bf86-113">Disabling client-side caching can be useful for decreasing the client-side memory requirements in such cases as when you intend only to make a single pass through the result set.</span></span> <span data-ttu-id="8bf86-114">不過，當用戶端選擇不快取結果時，它們會提供資料指標支援。</span><span class="sxs-lookup"><span data-stu-id="8bf86-114">However, when clients elect not to cache the result, they give up cursor support.</span></span>

<span data-ttu-id="8bf86-115">如需有關使用特定搜尋介面的結果快取的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="8bf86-115">For more information about results caching with a specific search interface, see:</span></span>

-   [<span data-ttu-id="8bf86-116">使用 >idirectorysearch 的結果快取</span><span class="sxs-lookup"><span data-stu-id="8bf86-116">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="8bf86-117">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="8bf86-117">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="8bf86-118">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="8bf86-118">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




