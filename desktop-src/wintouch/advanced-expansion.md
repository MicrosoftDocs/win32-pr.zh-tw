---
title: Advanced 擴充
description: Advanced 擴充
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows Touch，擴充
- Windows Touch，advanced 擴充
- Windows Touch，操作
- 操作，擴充
- 操作，advanced 擴充
- 展開，advanced
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81a3a395da053b7d0e8f79a115a2489f3e63190
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183071"
---
# <a name="advanced-expansion"></a><span data-ttu-id="a7f59-109">Advanced 擴充</span><span class="sxs-lookup"><span data-stu-id="a7f59-109">Advanced Expansion</span></span>

<span data-ttu-id="a7f59-110">下圖顯示可展開物件的兩種方式。</span><span class="sxs-lookup"><span data-stu-id="a7f59-110">The following illustration shows two ways that an object can be expanded.</span></span>

![圖例顯示物件中心點周圍的簡單展開，以及圍繞操作中心點的先進展開](images/expansion.png)

<span data-ttu-id="a7f59-112">例如，簡單的展開範例中，物件會圍繞其中心點展開。</span><span class="sxs-lookup"><span data-stu-id="a7f59-112">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="a7f59-113">在 B 範例中，物件是在操作中心點周圍展開。</span><span class="sxs-lookup"><span data-stu-id="a7f59-113">In example B, the object is expanded around the center point of the manipulation.</span></span> <span data-ttu-id="a7f59-114">若要啟用此功能，您必須在展開時轉譯物件。</span><span class="sxs-lookup"><span data-stu-id="a7f59-114">To enable this, you must translate the object while it is being expanded.</span></span> <span data-ttu-id="a7f59-115">您將轉譯物件的數量，與從物件中央到手勢中心點的距離相同。</span><span class="sxs-lookup"><span data-stu-id="a7f59-115">The amount that you will translate the object is the same as the distance from the center of the object to the center point of the gesture.</span></span> <span data-ttu-id="a7f59-116">很直覺地，它就像是從展開筆勢的中心點展開物件，然後將它移動，使其仍位於與其初始位置相同的中心點。</span><span class="sxs-lookup"><span data-stu-id="a7f59-116">Intuitively, it is as though you are expanding the object from the center point of your expansion gesture and then moving it so that it is still at the same center as its initial position.</span></span> <span data-ttu-id="a7f59-117">下列程式碼示範如何套用這個概念，以啟用中心點周圍的擴充。</span><span class="sxs-lookup"><span data-stu-id="a7f59-117">The following code shows one way that this concept can be applied to enable expansion around a center point.</span></span>


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a><span data-ttu-id="a7f59-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7f59-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7f59-119">操作</span><span class="sxs-lookup"><span data-stu-id="a7f59-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




