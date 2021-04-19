---
title: 流覽點擊測試和螢幕位置
description: 若要找出物件的子系，或判斷物件的大小，用戶端可以點擊螢幕上的測試點。
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967615"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a><span data-ttu-id="b6e19-103">流覽點擊測試和螢幕位置</span><span class="sxs-lookup"><span data-stu-id="b6e19-103">Navigation Through Hit Testing and Screen Location</span></span>

<span data-ttu-id="b6e19-104">若要找出物件的子系，或判斷物件的大小，用戶端可以點擊螢幕上的測試點。</span><span class="sxs-lookup"><span data-stu-id="b6e19-104">To locate an object's children or to determine an object's size, clients can hit test points on the screen.</span></span> <span data-ttu-id="b6e19-105">有兩種方法可用：</span><span class="sxs-lookup"><span data-stu-id="b6e19-105">Two methods are available:</span></span>

-   [<span data-ttu-id="b6e19-106">**IAccessible：： accHitTest**</span><span class="sxs-lookup"><span data-stu-id="b6e19-106">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="b6e19-107">**IAccessible：： accLocation**</span><span class="sxs-lookup"><span data-stu-id="b6e19-107">**IAccessible::accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a><span data-ttu-id="b6e19-108">使用 IAccessible：： accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6e19-108">Using IAccessible::accHitTest</span></span>

<span data-ttu-id="b6e19-109">若要識別某個點是否在物件內、其子系內或兩者皆非，用戶端會呼叫父物件的 [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 方法，並傳遞要進行點擊測試之點的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="b6e19-109">To identify whether a point is within an object, within its child, or neither, clients call the [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) method of the parent object, passing the screen coordinates of the point to be hit tested.</span></span> <span data-ttu-id="b6e19-110">下列清單描述一些一般案例：</span><span class="sxs-lookup"><span data-stu-id="b6e19-110">The following list describes some typical scenarios:</span></span>

-   <span data-ttu-id="b6e19-111">如果物件的子系在指定點重迭， [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 會抓取以視覺化方式呈現空間的最上層子系。</span><span class="sxs-lookup"><span data-stu-id="b6e19-111">If the object's children overlap at a specified point, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) retrieves the topmost child that visually appears to occupy the space.</span></span>
-   <span data-ttu-id="b6e19-112">如果視窗涵蓋子系，或如果父代已裁剪子系，則點擊測試會抓取子系，即使看不到子系也是一樣。</span><span class="sxs-lookup"><span data-stu-id="b6e19-112">If a window covers a child, or if the child is clipped by the parent, hit testing the covered point retrieves the child even though it is not visible.</span></span>
-   <span data-ttu-id="b6e19-113">如果在指定點找到的子系是可存取的物件，而不是子項目，則方法會傳回子系的 [**IDispatch**](idispatch-interface.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="b6e19-113">If the child found at the specified point is an accessible object, as opposed to a child element, the method returns the child's [**IDispatch**](idispatch-interface.md) interface.</span></span>

## <a name="using-iaccessibleacclocation"></a><span data-ttu-id="b6e19-114">使用 IAccessible：： accLocation</span><span class="sxs-lookup"><span data-stu-id="b6e19-114">Using IAccessible::accLocation</span></span>

<span data-ttu-id="b6e19-115">若要取得物件或其中一個物件子系的螢幕位置，用戶端會呼叫 [**IAccessible：： accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)。</span><span class="sxs-lookup"><span data-stu-id="b6e19-115">To get the screen location of an object or one of the object's children, clients call [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span></span> <span data-ttu-id="b6e19-116">這個方法會傳回指定物件之周框的座標。</span><span class="sxs-lookup"><span data-stu-id="b6e19-116">This method returns the coordinates of the specified object's bounding rectangle.</span></span> <span data-ttu-id="b6e19-117">如果物件不像矩形，則方法會傳回包含整個物件的最小矩形座標。</span><span class="sxs-lookup"><span data-stu-id="b6e19-117">If the object is not shaped like a rectangle, the method returns the coordinates of the smallest rectangle that encompasses the entire object.</span></span>

<span data-ttu-id="b6e19-118">下圖說明非矩形物件的區域和其週框之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="b6e19-118">The following illustration shows the relationship between a non-rectangular object's region and its bounding rectangle.</span></span>

![圖例顯示非矩形物件的區域 (圓形) 和其周框。](images/region.gif)

> [!Note]  
> <span data-ttu-id="b6e19-120">[**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 比 [**IAccessible：： accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) 更為精確，因為它可讓用戶端以圖元為單位來決定物件的位置，而不是使用周框矩形。</span><span class="sxs-lookup"><span data-stu-id="b6e19-120">[**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) is more precise than [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because it enables clients to determine the location of objects on a pixel-by-pixel basis rather than with bounding rectangles.</span></span> <span data-ttu-id="b6e19-121">此精確度很有用，例如，當應用程式透過追蹤滑鼠指標的位置來收集資訊時。</span><span class="sxs-lookup"><span data-stu-id="b6e19-121">This precision is useful, for example, when an application is gathering information by tracking the location of the mouse pointer.</span></span>

 

 

 




