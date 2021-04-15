---
description: 記憶體配置器
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: 記憶體配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510212"
---
# <a name="memory-allocator"></a><span data-ttu-id="eeb81-103">記憶體配置器</span><span class="sxs-lookup"><span data-stu-id="eeb81-103">Memory Allocator</span></span>

<span data-ttu-id="eeb81-104">記憶體配置器物件會配置媒體範例的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="eeb81-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="eeb81-105">篩選器可以使用此物件來配置共用記憶體緩衝區;不過，具有特殊需求的篩選也可以執行它自己的記憶體配置器物件。</span><span class="sxs-lookup"><span data-stu-id="eeb81-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="eeb81-106">藉由呼叫 **CoCreateInstance** 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="eeb81-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="eeb81-107">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="eeb81-107">Class Identifier</span></span> | <span data-ttu-id="eeb81-108">CLSID \_ MemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="eeb81-108">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="eeb81-109">介面</span><span class="sxs-lookup"><span data-stu-id="eeb81-109">Interfaces</span></span>       | [<span data-ttu-id="eeb81-110">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="eeb81-110">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="eeb81-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="eeb81-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb81-112">DirectShow 物件</span><span class="sxs-lookup"><span data-stu-id="eeb81-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



