---
description: 每個進程都有系統提供的預設堆積。 從堆積進行頻繁配置的應用程式，可以使用私用堆積來改善效能。
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: 堆積函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e591c1e349ed6806cbebe00a178a99e63bb412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849162"
---
# <a name="heap-functions"></a>堆積函數

每個進程都有系統提供的預設堆積。 從堆積進行頻繁配置的應用程式，可以使用私用堆積來改善效能。

私用堆積是呼叫進程的位址空間中一或多個頁面的區塊。 建立私用堆積之後，進程會使用 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) 和 [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) 等函數來管理該堆積中的記憶體。

堆積函數也可以用來使用 [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) 函式所傳回的控制碼，在進程的預設堆積中管理記憶體。 新的應用程式應該使用堆積函式，而不是使用 [全域和區域](global-and-local-functions.md) 函式來進行這項工作。

從私用堆積配置的記憶體與使用其他記憶體配置函數配置的記憶體之間沒有任何差異。 如需函式的完整清單，請參閱 [記憶體管理函數](memory-management-functions.md)中的資料表。

> [!Note]  
> 執行緒應該只針對進程的預設堆積以及執行緒所建立和管理的私用堆積呼叫堆積函數，並使用 [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) 或 [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) 函數所傳回的控制碼。

 

[**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate)函式會建立私用堆積物件，呼叫進程可以使用 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)函數來配置記憶體區塊。 **HeapCreate** 指定堆積的初始大小和大小上限。 初始大小會決定一開始為堆積配置的認可、讀取/寫入頁面數目。 大小上限決定了保留的頁面總數。 這些頁面會在堆積可以成長的進程的虛擬位址空間中建立連續區塊。 如果 **HeapAlloc** 要求超過目前認可的頁面大小，則會自動從這個保留的空間認可其他頁面，但前提是它的實體儲存體可供使用。 一旦頁面認可之後，就不會已取消認可這些頁面，直到進程終止，或呼叫 [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) 函數來終結堆積為止。

私用堆積物件的記憶體只能由建立它的進程存取。 如果動態連結程式庫 (DLL) 建立私用堆積，則會在呼叫 DLL 之進程的位址空間中執行此動作。 只有該進程可以存取它。

[**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)函式會從私用堆積配置指定的位元組數，並將指標傳回給配置的區塊。 此指標可以用於 [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree)、 [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc)、 [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)和 [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) 函數。

[**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)配置的記憶體不是可移動的。 在釋放或重新配置記憶體區塊之前， **HeapAlloc** 傳回的位址是有效的;記憶體區塊不需要鎖定。

因為系統無法壓縮私用堆積，所以它可能會分散。 以各種配置大小配置大量記憶體的應用程式，可以使用 [低片段堆積](low-fragmentation-heap.md) 來減少堆積片段。

堆積函式的可能用途是在進程啟動時建立私用堆積，指定足夠的初始大小來滿足進程的記憶體需求。 如果對 [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) 函式的呼叫失敗，進程可以終止或通知使用者記憶體不足;但是，如果成功，進程就能確保記憶體需要。

[**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate)要求的記憶體不一定是連續的。 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)在堆積內配置的記憶體是連續的。 您不應該寫入或讀取堆積中的記憶體（除了由 **HeapAlloc** 所配置），也不應該假設 **HeapAlloc** 所配置的兩個記憶體區域之間有任何關聯性。

您不應該以任何方式參考 [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree)已釋放的記憶體。 釋放記憶體之後，其中可能存在的任何資訊都會永久消失。 如果您需要資訊，請勿釋放包含資訊的記憶體。 傳回記憶體 (資訊的函式呼叫，例如 [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)) 可能無法搭配釋出的記憶體使用，因為它們可能會傳回假的資料。

[**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy)函式會終結私用堆積物件。 它會解除和釋放堆積物件的所有頁面，並使堆積的控制碼失效。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[比較記憶體配置方法](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



