---
description: 記憶體配置器
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: 記憶體配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909417"
---
# <a name="memory-allocator"></a><span data-ttu-id="66296-103">記憶體配置器</span><span class="sxs-lookup"><span data-stu-id="66296-103">Memory Allocator</span></span>

<span data-ttu-id="66296-104">記憶體配置器物件會配置媒體範例的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="66296-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="66296-105">篩選器可以使用此物件來配置共用記憶體緩衝區;不過，具有特殊需求的篩選也可以執行它自己的記憶體配置器物件。</span><span class="sxs-lookup"><span data-stu-id="66296-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="66296-106">藉由呼叫 **CoCreateInstance** 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="66296-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="66296-107">標籤</span><span class="sxs-lookup"><span data-stu-id="66296-107">Label</span></span> | <span data-ttu-id="66296-108">值</span><span class="sxs-lookup"><span data-stu-id="66296-108">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="66296-109">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="66296-109">Class Identifier</span></span> | <span data-ttu-id="66296-110">CLSID \_ MemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="66296-110">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="66296-111">介面</span><span class="sxs-lookup"><span data-stu-id="66296-111">Interfaces</span></span>       | [<span data-ttu-id="66296-112">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="66296-112">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="66296-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="66296-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66296-114">DirectShow 物件</span><span class="sxs-lookup"><span data-stu-id="66296-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



