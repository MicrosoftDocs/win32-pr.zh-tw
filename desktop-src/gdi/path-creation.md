---
description: 若要建立路徑並將其選取到 DC，首先必須定義描述它的點。
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: 路徑建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191928"
---
# <a name="path-creation"></a><span data-ttu-id="5275b-103">路徑建立</span><span class="sxs-lookup"><span data-stu-id="5275b-103">Path Creation</span></span>

<span data-ttu-id="5275b-104">若要建立路徑並將其選取到 DC，首先必須定義描述它的點。</span><span class="sxs-lookup"><span data-stu-id="5275b-104">To create a path and select it into a DC, it is first necessary to define the points that describe it.</span></span> <span data-ttu-id="5275b-105">這是藉由呼叫 [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) 函式來完成，指定適當的繪圖函式，然後再呼叫 [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) 函數。</span><span class="sxs-lookup"><span data-stu-id="5275b-105">This is done by calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function, specifying the appropriate drawing functions, and then by calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="5275b-106">這種函式組合 (**BeginPath**、繪製函式和 **EndPath**) 構成 *路徑括弧*。</span><span class="sxs-lookup"><span data-stu-id="5275b-106">This combination of functions (**BeginPath**, drawing functions, and **EndPath**) constitute a *path bracket*.</span></span> <span data-ttu-id="5275b-107">以下是可以使用的繪圖函數清單。</span><span class="sxs-lookup"><span data-stu-id="5275b-107">The following is the list of drawing functions that can be used.</span></span>

-   [<span data-ttu-id="5275b-108">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="5275b-108">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [<span data-ttu-id="5275b-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="5275b-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [<span data-ttu-id="5275b-110">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="5275b-110">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [<span data-ttu-id="5275b-111">**和絃**</span><span class="sxs-lookup"><span data-stu-id="5275b-111">**Chord**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [<span data-ttu-id="5275b-112">**CloseFigure**</span><span class="sxs-lookup"><span data-stu-id="5275b-112">**CloseFigure**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [<span data-ttu-id="5275b-113">**橢圓形**</span><span class="sxs-lookup"><span data-stu-id="5275b-113">**Ellipse**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [<span data-ttu-id="5275b-114">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="5275b-114">**ExtTextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="5275b-115">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="5275b-115">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [<span data-ttu-id="5275b-116">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="5275b-116">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [<span data-ttu-id="5275b-117">**圓形圖**</span><span class="sxs-lookup"><span data-stu-id="5275b-117">**Pie**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [<span data-ttu-id="5275b-118">**PolyBezier**</span><span class="sxs-lookup"><span data-stu-id="5275b-118">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [<span data-ttu-id="5275b-119">**PolyBezierTo**</span><span class="sxs-lookup"><span data-stu-id="5275b-119">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [<span data-ttu-id="5275b-120">**PolyDraw**</span><span class="sxs-lookup"><span data-stu-id="5275b-120">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [<span data-ttu-id="5275b-121">**多邊形**</span><span class="sxs-lookup"><span data-stu-id="5275b-121">**Polygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [<span data-ttu-id="5275b-122">**聚合線條**</span><span class="sxs-lookup"><span data-stu-id="5275b-122">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [<span data-ttu-id="5275b-123">**PolylineTo**</span><span class="sxs-lookup"><span data-stu-id="5275b-123">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [<span data-ttu-id="5275b-124">**PolyPolygon**</span><span class="sxs-lookup"><span data-stu-id="5275b-124">**PolyPolygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [<span data-ttu-id="5275b-125">**PolyPolyline**</span><span class="sxs-lookup"><span data-stu-id="5275b-125">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [<span data-ttu-id="5275b-126">**矩形**</span><span class="sxs-lookup"><span data-stu-id="5275b-126">**Rectangle**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [<span data-ttu-id="5275b-127">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="5275b-127">**RoundRect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [<span data-ttu-id="5275b-128">**TextOut**</span><span class="sxs-lookup"><span data-stu-id="5275b-128">**TextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="5275b-129">當應用程式呼叫 [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)時，系統會在指定的 DC 中選取相關聯的路徑。</span><span class="sxs-lookup"><span data-stu-id="5275b-129">When an application calls [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), the system selects the associated path into the specified DC.</span></span> <span data-ttu-id="5275b-130"> (如果先前已在 DC 中選取另一個路徑，系統就會刪除該路徑，而不會儲存該路徑 ) 。當系統選取 DC 中的路徑之後，應用程式就可以使用下列其中一種方式在路徑上操作：</span><span class="sxs-lookup"><span data-stu-id="5275b-130">(If another path had previously been selected into the DC, the system deletes that path without saving it.) After the system selects the path into the DC, an application can operate on the path in one of the following ways:</span></span>

-   <span data-ttu-id="5275b-131">使用目前的畫筆) 繪製路徑 (的大綱。</span><span class="sxs-lookup"><span data-stu-id="5275b-131">Draw the outline of the path (using the current pen).</span></span>
-   <span data-ttu-id="5275b-132">使用目前的筆刷) ，繪製路徑 (的內部。</span><span class="sxs-lookup"><span data-stu-id="5275b-132">Paint the interior of the path (using the current brush).</span></span>
-   <span data-ttu-id="5275b-133">繪製外框並填滿路徑的內部。</span><span class="sxs-lookup"><span data-stu-id="5275b-133">Draw the outline and fill the interior of the path.</span></span>
-   <span data-ttu-id="5275b-134">修改路徑 (將曲線轉換成線段) 。</span><span class="sxs-lookup"><span data-stu-id="5275b-134">Modify the path (converting curves to line segments).</span></span>
-   <span data-ttu-id="5275b-135">將路徑轉換成剪輯路徑。</span><span class="sxs-lookup"><span data-stu-id="5275b-135">Convert the path into a clip path.</span></span>
-   <span data-ttu-id="5275b-136">將路徑轉換成區域。</span><span class="sxs-lookup"><span data-stu-id="5275b-136">Convert the path into a region.</span></span>
-   <span data-ttu-id="5275b-137">將路徑中的每個曲線轉換成一連串的線段，以壓平合併路徑。</span><span class="sxs-lookup"><span data-stu-id="5275b-137">Flatten the path by converting each curve in the path into a series of line segments.</span></span>
-   <span data-ttu-id="5275b-138">抓取組成路徑之線條和曲線的座標。</span><span class="sxs-lookup"><span data-stu-id="5275b-138">Retrieve the coordinates of the lines and curves that compose a path.</span></span>

 

 



