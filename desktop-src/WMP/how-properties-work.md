---
title: 屬性的運作方式
description: 屬性的運作方式
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性
- 外掛程式，Echo 範例屬性
- 數位信號處理外掛程式，Echo 範例屬性
- DSP 外掛程式，Echo 範例屬性
- Echo DSP 外掛程式範例，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673908"
---
# <a name="how-properties-work"></a><span data-ttu-id="b91fd-108">屬性的運作方式</span><span class="sxs-lookup"><span data-stu-id="b91fd-108">How Properties Work</span></span>

<span data-ttu-id="b91fd-109">屬性值會儲存在成員變數中。</span><span class="sxs-lookup"><span data-stu-id="b91fd-109">Property values are stored in member variables.</span></span>

<span data-ttu-id="b91fd-110">屬性可透過方法配對來存取。</span><span class="sxs-lookup"><span data-stu-id="b91fd-110">Properties are made accessible by method pairs.</span></span> <span data-ttu-id="b91fd-111">其中一個方法會提供執行來指定屬性值;其名稱開頭為 put \_ 。</span><span class="sxs-lookup"><span data-stu-id="b91fd-111">One method provides the implementation to specify the property value; its name starts with put\_.</span></span> <span data-ttu-id="b91fd-112">另一個方法會提供實作為抓取屬性值的實值;其名稱開頭為 get \_ 。</span><span class="sxs-lookup"><span data-stu-id="b91fd-112">The other method provides the implementation to retrieve the property value; its name starts with get\_.</span></span> <span data-ttu-id="b91fd-113">介面定義位於 Echo 中。</span><span class="sxs-lookup"><span data-stu-id="b91fd-113">The interface definition is in Echo.idl.</span></span> <span data-ttu-id="b91fd-114">屬性方法原型位於 Echo. h 中。</span><span class="sxs-lookup"><span data-stu-id="b91fd-114">The property method prototypes are in Echo.h.</span></span> <span data-ttu-id="b91fd-115">它們會在 Echo 中實作為。</span><span class="sxs-lookup"><span data-stu-id="b91fd-115">They are implemented in Echo.cpp.</span></span>

<span data-ttu-id="b91fd-116">接下來的三個章節將示範如何修改現有的屬性方法，以符合您的需求，以及如何新增其他屬性的方法。</span><span class="sxs-lookup"><span data-stu-id="b91fd-116">The next three sections will show you how to modify the existing property methods to suit your needs and how to add the methods for an additional property.</span></span>

-   [<span data-ttu-id="b91fd-117">用來儲存屬性的變數</span><span class="sxs-lookup"><span data-stu-id="b91fd-117">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="b91fd-118">修改尺規屬性</span><span class="sxs-lookup"><span data-stu-id="b91fd-118">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="b91fd-119">新增濕混合屬性</span><span class="sxs-lookup"><span data-stu-id="b91fd-119">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="b91fd-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b91fd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b91fd-121">**Echo 範例屬性**</span><span class="sxs-lookup"><span data-stu-id="b91fd-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




