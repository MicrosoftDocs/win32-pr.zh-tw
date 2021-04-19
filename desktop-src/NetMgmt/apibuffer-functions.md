---
title: ApiBuffer 函式
description: 網路管理 ApiBuffer 函式可用來管理具有網路管理功能之應用程式所使用的記憶體配置。
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967682"
---
# <a name="apibuffer-functions"></a><span data-ttu-id="13313-103">ApiBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="13313-103">ApiBuffer Functions</span></span>

<span data-ttu-id="13313-104">網路管理 ApiBuffer 函式可用來管理具有網路管理功能之應用程式所使用的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="13313-104">The network management ApiBuffer functions are used to manage memory allocation used by an application with network management functions.</span></span> <span data-ttu-id="13313-105">不過，一般而言，針對應用程式所使用的其他記憶體，您應該使用 [記憶體管理](/windows/desktop/Memory/memory-management-functions) 函式，而不是這些 ApiBuffer 函數。</span><span class="sxs-lookup"><span data-stu-id="13313-105">However, in general, for other memory used by an application you should use the [memory management functions](/windows/desktop/Memory/memory-management-functions) instead of these ApiBuffer functions.</span></span>

<span data-ttu-id="13313-106">ApiBuffer 函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="13313-106">The ApiBuffer functions are listed following.</span></span>



| <span data-ttu-id="13313-107">函式</span><span class="sxs-lookup"><span data-stu-id="13313-107">Function</span></span>                                                 | <span data-ttu-id="13313-108">描述</span><span class="sxs-lookup"><span data-stu-id="13313-108">Description</span></span>                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13313-109">**NetApiBufferAllocate**</span><span class="sxs-lookup"><span data-stu-id="13313-109">**NetApiBufferAllocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | <span data-ttu-id="13313-110">從堆積配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="13313-110">Allocates memory from the heap.</span></span> <span data-ttu-id="13313-111">當您需要與 **NetApiBufferFree** 函數相容時，請呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="13313-111">Call this function when you require compatibility with the **NetApiBufferFree** function.</span></span> |
| [<span data-ttu-id="13313-112">**NetApiBufferFree**</span><span class="sxs-lookup"><span data-stu-id="13313-112">**NetApiBufferFree**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | <span data-ttu-id="13313-113">釋放 **NetApiBufferAllocate** 函式所配置的記憶體和其他網路管理功能。</span><span class="sxs-lookup"><span data-stu-id="13313-113">Frees memory allocated by the **NetApiBufferAllocate** function and other network management functions.</span></span>                   |
| [<span data-ttu-id="13313-114">**NetApiBufferReallocate**</span><span class="sxs-lookup"><span data-stu-id="13313-114">**NetApiBufferReallocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | <span data-ttu-id="13313-115">變更 **NetApiBufferAllocate** 函式的呼叫所配置的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="13313-115">Changes the size of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                                |
| [<span data-ttu-id="13313-116">**NetApiBufferSize**</span><span class="sxs-lookup"><span data-stu-id="13313-116">**NetApiBufferSize**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | <span data-ttu-id="13313-117">傳回對 **NetApiBufferAllocate** 函式的呼叫所配置的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="13313-117">Returns the size, in bytes, of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                     |



 

<span data-ttu-id="13313-118">針對將資訊傳回給呼叫端的可遠端函式，RPC 執行時間程式庫會配置包含傳回信息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="13313-118">For remotable functions that return information to the caller, the RPC run-time library allocates the buffer containing the return information.</span></span> <span data-ttu-id="13313-119">當呼叫端處理完資訊之後，它必須呼叫 [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) 函式來釋放已配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="13313-119">When the caller has finished processing the information, it must call the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function to free the allocated buffer.</span></span>

 

 