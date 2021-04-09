---
title: OLE 記憶體配置器
description: OLE 記憶體配置器
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093356"
---
# <a name="the-ole-memory-allocator"></a><span data-ttu-id="7d5e0-103">OLE 記憶體配置器</span><span class="sxs-lookup"><span data-stu-id="7d5e0-103">The OLE Memory Allocator</span></span>

<span data-ttu-id="7d5e0-104">COM 程式庫提供記憶體配置器的實作為安全線程。</span><span class="sxs-lookup"><span data-stu-id="7d5e0-104">The COM library provides an implementation of a memory allocator that is thread-safe.</span></span> <span data-ttu-id="7d5e0-105"> (也就是說，在多執行緒情況下，它不會造成問題 ) 。每當配置的記憶體區塊擁有權透過 COM 介面或在用戶端與 COM 程式庫之間傳遞時，您就必須使用這個 COM 配置器來配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="7d5e0-105">(That is, it cannot cause problems in multithreaded situations.) Whenever ownership of an allocated chunk of memory is passed through a COM interface or between a client and the COM library, you must use this COM allocator to allocate the memory.</span></span> <span data-ttu-id="7d5e0-106">物件的內部配置可以使用任何所需的配置配置，但是 COM 記憶體配置器是一個方便、有效率且安全線程的配置器。</span><span class="sxs-lookup"><span data-stu-id="7d5e0-106">Allocation internal to an object can use any allocation scheme desired, but the COM memory allocator is a handy, efficient, and thread-safe allocator.</span></span>

<span data-ttu-id="7d5e0-107">對 API 函式 [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) 的呼叫會提供 OLE 配置器的指標，這是 [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) 介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="7d5e0-107">A call to the API function [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) provides a pointer to the OLE allocator, which is an implementation of the [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) interface.</span></span> <span data-ttu-id="7d5e0-108">不過，呼叫 helper 函式 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)、 [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)和 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)會更有效率，這會包裝取得工作記憶體配置器的指標、呼叫對應的 **IMalloc** 方法，然後釋放配置器的指標。</span><span class="sxs-lookup"><span data-stu-id="7d5e0-108">However, it is more efficient to call the helper functions [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc), and [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), which wrap getting a pointer to the task memory allocator, calling the corresponding **IMalloc** method, and then releasing the pointer to the allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d5e0-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d5e0-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d5e0-110">管理記憶體配置</span><span class="sxs-lookup"><span data-stu-id="7d5e0-110">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> <dt>

[<span data-ttu-id="7d5e0-111">COM 程式庫</span><span class="sxs-lookup"><span data-stu-id="7d5e0-111">The COM Library</span></span>](the-com-library.md)
</dt> </dl>

 

 