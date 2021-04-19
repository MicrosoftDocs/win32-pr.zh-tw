---
description: CMSPCallMultiGraph 成員
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: CMSPCallMultiGraph 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987559"
---
# <a name="cmspcallmultigraph-members"></a><span data-ttu-id="33778-103">CMSPCallMultiGraph 成員</span><span class="sxs-lookup"><span data-stu-id="33778-103">CMSPCallMultiGraph Members</span></span>

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

<span data-ttu-id="33778-104">等候區塊會儲存註冊到執行緒集區的等候相關資訊。</span><span class="sxs-lookup"><span data-stu-id="33778-104">The wait blocks store the information about the wait registered to the thread pool.</span></span> <span data-ttu-id="33778-105">它包含 [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) 呼叫所傳回的等候控制碼，以及內容結構的指標。</span><span class="sxs-lookup"><span data-stu-id="33778-105">It includes the wait handles returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) call and a pointer to the context structure.</span></span> <span data-ttu-id="33778-106">陣列中的每個區塊都是針對其中一個資料流程物件中的圖形。</span><span class="sxs-lookup"><span data-stu-id="33778-106">Each block in the array is for a graph in one of the stream objects.</span></span> <span data-ttu-id="33778-107">此陣列中的區塊位移與擁有圖形的資料流程位移相同。</span><span class="sxs-lookup"><span data-stu-id="33778-107">The offset of a block in this array is the same as the offset of the stream that owns the graph.</span></span>

 

 
