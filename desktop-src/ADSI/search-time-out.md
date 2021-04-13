---
title: 搜尋超時
description: 用戶端也可能會強制等候伺服器傳回結果集的時間限制。
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- 搜尋即時 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300059"
---
# <a name="search-time-out"></a><span data-ttu-id="cf7d8-104">搜尋超時</span><span class="sxs-lookup"><span data-stu-id="cf7d8-104">Search Time Out</span></span>

<span data-ttu-id="cf7d8-105">用戶端也可能會強制等候伺服器傳回結果集的時間限制。</span><span class="sxs-lookup"><span data-stu-id="cf7d8-105">A client can also impose a time limit that it will wait for a server to return the result set.</span></span> <span data-ttu-id="cf7d8-106">[搜尋超時] 選項的值會指定此限制。</span><span class="sxs-lookup"><span data-stu-id="cf7d8-106">The value of the "search time out" option specifies this limit.</span></span> <span data-ttu-id="cf7d8-107">當伺服器無法在指定的期間內回應查詢時，用戶端可以停止搜尋，稍後再試一次。</span><span class="sxs-lookup"><span data-stu-id="cf7d8-107">When the server fails to respond to a query within the specified time period, the client can stop the search and try again later.</span></span>

<span data-ttu-id="cf7d8-108">當用戶端要求非同步搜尋時，超時屬性很有用。</span><span class="sxs-lookup"><span data-stu-id="cf7d8-108">The time-out property is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="cf7d8-109">在非同步搜尋中，用戶端會提出要求，然後在等候伺服器傳回結果時，繼續執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="cf7d8-109">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="cf7d8-110">伺服器可能會離線，而不會通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="cf7d8-110">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="cf7d8-111">在此情況下，用戶端無法辨識伺服器是否仍在處理查詢，或是否已停止運作。</span><span class="sxs-lookup"><span data-stu-id="cf7d8-111">In this case, the client has no way of recognizing that the server is still processing the query, or if it has ceased to be live.</span></span> <span data-ttu-id="cf7d8-112">超時屬性可讓用戶端在這類實例中有一些控制權。</span><span class="sxs-lookup"><span data-stu-id="cf7d8-112">The time-out property provides the client some control in such instances.</span></span>

<span data-ttu-id="cf7d8-113">如需有關使用搜尋超時選項搭配特定搜尋介面的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="cf7d8-113">For more information about using the search time-out option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="cf7d8-114">使用 >idirectorysearch 的用戶端時間限制</span><span class="sxs-lookup"><span data-stu-id="cf7d8-114">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="cf7d8-115">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="cf7d8-115">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="cf7d8-116">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="cf7d8-116">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




