---
title: 堆積
description: 堆積會追蹤一組以一個單位來釋放的配置。
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- 適用于 Windows 的堆積 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383349"
---
# <a name="heap"></a><span data-ttu-id="5fd04-106">堆積</span><span class="sxs-lookup"><span data-stu-id="5fd04-106">Heap</span></span>

<span data-ttu-id="5fd04-107">堆積會追蹤一組以一個單位來釋放的配置。</span><span class="sxs-lookup"><span data-stu-id="5fd04-107">A heap tracks a group of allocations that are freed as a unit.</span></span>

<span data-ttu-id="5fd04-108">這可讓您避免在使用 WWSAPI 時，配置和解除配置記憶體的複雜模式。</span><span class="sxs-lookup"><span data-stu-id="5fd04-108">This allows you to avoid complex patterns of allocating and deallocating memory when you use the WWSAPI.</span></span>


<span data-ttu-id="5fd04-109">每個訊息都有相關聯的堆積。</span><span class="sxs-lookup"><span data-stu-id="5fd04-109">There is a heap associated with every message.</span></span> <span data-ttu-id="5fd04-110">傳送訊息或接收訊息時，訊息的堆積會用於任何與該特定訊息相關的配置。</span><span class="sxs-lookup"><span data-stu-id="5fd04-110">As a message is being sent, or as a message is being received, the heap of the message is used for any allocations relating to that particular message.</span></span> <span data-ttu-id="5fd04-111">傳送或接收訊息之後，就會重設堆積 (這會清除與特定訊息) 相關的任何配置。</span><span class="sxs-lookup"><span data-stu-id="5fd04-111">After a message is sent or received, the heap is reset (which cleans up any allocations related to the particular message).</span></span>

<span data-ttu-id="5fd04-112">堆積也可以用來儲存訊息的存留期以外的訊息資料。</span><span class="sxs-lookup"><span data-stu-id="5fd04-112">Heaps can also be used to store message data separately from the lifetime of a message.</span></span> <span data-ttu-id="5fd04-113">許多 API 在讀取資料時所使用的堆積允許規格，可讓您明確控制讀取的任何資料存留期。</span><span class="sxs-lookup"><span data-stu-id="5fd04-113">Many of the API's allow specification of the heap to use when reading data give explicit control over the lifetime of any data read.</span></span>

<span data-ttu-id="5fd04-114">來自堆積的配置保證至少會對齊8個位元組的界限。</span><span class="sxs-lookup"><span data-stu-id="5fd04-114">Allocations from a heap are guaranteed to be aligned on at least an 8 byte boundary.</span></span>

<span data-ttu-id="5fd04-115">零位元組配置會傳回非 Null 指標。</span><span class="sxs-lookup"><span data-stu-id="5fd04-115">Zero byte allocations will return a non-NULL pointer.</span></span>

<span data-ttu-id="5fd04-116">在 Windows 7 中，如果啟用 PageHeap，則會使用從 HeapCreate 傳回的堆積來管理記憶體。</span><span class="sxs-lookup"><span data-stu-id="5fd04-116">In Windows 7, if PageHeap is enabled, a heap returned from HeapCreate is used to manage the memory.</span></span> <span data-ttu-id="5fd04-117">在此情況下， [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) 會直接對應至 HeapAlloc，並將 [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) 對應至 HeapDestroy。</span><span class="sxs-lookup"><span data-stu-id="5fd04-117">In this case, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) maps directly to HeapAlloc and [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) maps to HeapDestroy.</span></span>

<span data-ttu-id="5fd04-118">下列列舉會搭配堆積使用：</span><span class="sxs-lookup"><span data-stu-id="5fd04-118">The following enumeration is used with the heap:</span></span>

-   [<span data-ttu-id="5fd04-119">**WS \_ 堆積 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="5fd04-119">**WS\_HEAP\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

<span data-ttu-id="5fd04-120">下列函式會搭配堆積使用：</span><span class="sxs-lookup"><span data-stu-id="5fd04-120">The following functions are used with the heap:</span></span>

-   [<span data-ttu-id="5fd04-121">**WsAlloc**</span><span class="sxs-lookup"><span data-stu-id="5fd04-121">**WsAlloc**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [<span data-ttu-id="5fd04-122">**WsCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="5fd04-122">**WsCreateHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [<span data-ttu-id="5fd04-123">**WsFreeHeap**</span><span class="sxs-lookup"><span data-stu-id="5fd04-123">**WsFreeHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [<span data-ttu-id="5fd04-124">**WsGetHeapProperty**</span><span class="sxs-lookup"><span data-stu-id="5fd04-124">**WsGetHeapProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [<span data-ttu-id="5fd04-125">**WsResetHeap**</span><span class="sxs-lookup"><span data-stu-id="5fd04-125">**WsResetHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

<span data-ttu-id="5fd04-126">下列控制碼會搭配堆積使用：</span><span class="sxs-lookup"><span data-stu-id="5fd04-126">The following handle is used with the heap:</span></span>

-   [<span data-ttu-id="5fd04-127">WS \_ 堆積</span><span class="sxs-lookup"><span data-stu-id="5fd04-127">WS\_HEAP</span></span>](ws-heap.md)

<span data-ttu-id="5fd04-128">下列結構會搭配堆積使用：</span><span class="sxs-lookup"><span data-stu-id="5fd04-128">The following structures are used with the heap:</span></span>

-   [<span data-ttu-id="5fd04-129">**WS \_ 堆積 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="5fd04-129">**WS\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [<span data-ttu-id="5fd04-130">**WS \_ 堆積 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="5fd04-130">**WS\_HEAP\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




