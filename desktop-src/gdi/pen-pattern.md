---
description: Pattern 屬性指定幾何畫筆的模式。
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: 畫筆模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512860"
---
# <a name="pen-pattern"></a><span data-ttu-id="9ce84-103">畫筆模式</span><span class="sxs-lookup"><span data-stu-id="9ce84-103">Pen Pattern</span></span>

<span data-ttu-id="9ce84-104">Pattern 屬性指定幾何畫筆的模式。</span><span class="sxs-lookup"><span data-stu-id="9ce84-104">The pattern attribute specifies the pattern of a geometric pen.</span></span>

<span data-ttu-id="9ce84-105">下圖顯示使用不同幾何筆繪製的線條。</span><span class="sxs-lookup"><span data-stu-id="9ce84-105">The following illustration shows lines drawn with different geometric pens.</span></span> <span data-ttu-id="9ce84-106">每個畫筆都是使用不同的模式屬性來建立。</span><span class="sxs-lookup"><span data-stu-id="9ce84-106">Each pen was created using a different pattern attribute.</span></span>

![顯示四行的圖，每個線條都以不同的畫筆填滿](images/cspen-02.png)

<span data-ttu-id="9ce84-108">上圖中的第一行會使用六個可用的影線圖樣之一來繪製;如需影線模式的詳細資訊，請參閱 [畫筆影線](pen-hatch.md)。</span><span class="sxs-lookup"><span data-stu-id="9ce84-108">The first line in the previous illustration is drawn using one of the six available hatch patterns; for more information about hatch patterns, see [Pen Hatch](pen-hatch.md).</span></span> <span data-ttu-id="9ce84-109">下一行使用空心模式繪製，與 null 模式相同。</span><span class="sxs-lookup"><span data-stu-id="9ce84-109">The next line is drawn using the hollow pattern, identical to the null pattern.</span></span> <span data-ttu-id="9ce84-110">第三行則是使用從 8 x 8 圖元的點陣圖建立的自訂模式來繪製。</span><span class="sxs-lookup"><span data-stu-id="9ce84-110">The third line is drawn using a custom pattern created from an 8-by-8-pixel bitmap.</span></span> <span data-ttu-id="9ce84-111"> (如需有關點陣圖及其建立方式的詳細資訊，請參閱 [點陣圖](bitmaps.md)。 ) 使用穩固模式繪製最後一行。</span><span class="sxs-lookup"><span data-stu-id="9ce84-111">(For more information about bitmaps and their creation, see [Bitmaps](bitmaps.md).) The last line is drawn using a solid pattern.</span></span> <span data-ttu-id="9ce84-112">建立筆刷並將其控制碼傳遞至 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) 函式，會建立一個模式。</span><span class="sxs-lookup"><span data-stu-id="9ce84-112">Creating a brush and passing its handle to the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function creates a pattern.</span></span>

 

 



