---
description: SetRect 函式會建立矩形，CopyRect 函式會建立指定矩形的複本，而 SetRectEmpty 函式會建立空的矩形。
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: 矩形作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318832"
---
# <a name="rectangle-operations"></a><span data-ttu-id="8e73d-103">矩形作業</span><span class="sxs-lookup"><span data-stu-id="8e73d-103">Rectangle Operations</span></span>

<span data-ttu-id="8e73d-104">[**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect)函式會建立矩形， [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect)函式會建立指定矩形的複本，而 [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty)函式會建立空的矩形。</span><span class="sxs-lookup"><span data-stu-id="8e73d-104">The [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) function creates a rectangle, the [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) function makes a copy of a given rectangle, and the [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) function creates an empty rectangle.</span></span> <span data-ttu-id="8e73d-105">空的矩形是任何寬度為零的矩形、零高度或兩者。</span><span class="sxs-lookup"><span data-stu-id="8e73d-105">An empty rectangle is any rectangle that has zero width, zero height, or both.</span></span> <span data-ttu-id="8e73d-106">[**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty)函式會判斷指定的矩形是否為空白。</span><span class="sxs-lookup"><span data-stu-id="8e73d-106">The [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) function determines whether a given rectangle is empty.</span></span> <span data-ttu-id="8e73d-107">[**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect)函式會判斷兩個矩形是否相同，也就是它們是否具有相同的座標。</span><span class="sxs-lookup"><span data-stu-id="8e73d-107">The [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) function determines whether two rectangles are identical that is, whether they have the same coordinates.</span></span>

<span data-ttu-id="8e73d-108">[**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect)函式會增加或減少矩形的寬度或高度，或兩者。</span><span class="sxs-lookup"><span data-stu-id="8e73d-108">The [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) function increases or decreases the width or height of a rectangle, or both.</span></span> <span data-ttu-id="8e73d-109">它可以新增或移除矩形兩端的寬度;它可以新增或移除矩形頂端和底部的高度。</span><span class="sxs-lookup"><span data-stu-id="8e73d-109">It can add or remove width from both ends of the rectangle; it can add or remove height from both the top and bottom of the rectangle.</span></span>

<span data-ttu-id="8e73d-110">[**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect)函式會以指定的數量移動矩形。</span><span class="sxs-lookup"><span data-stu-id="8e73d-110">The [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) function moves a rectangle by a given amount.</span></span> <span data-ttu-id="8e73d-111">它會藉由將指定的 x 數量、y 金額或 x 和 y 數量新增至邊角座標來移動矩形。</span><span class="sxs-lookup"><span data-stu-id="8e73d-111">It moves the rectangle by adding the given x-amount, y-amount, or x- and y-amounts to the corner coordinates.</span></span>

<span data-ttu-id="8e73d-112">[**>ptinrect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect)函式會判斷指定的點是否位於指定的矩形內。</span><span class="sxs-lookup"><span data-stu-id="8e73d-112">The [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) function determines whether a given point lies within a given rectangle.</span></span> <span data-ttu-id="8e73d-113">如果該點位於左邊或上方，或完全在矩形內，則該點位於矩形內。</span><span class="sxs-lookup"><span data-stu-id="8e73d-113">The point is in the rectangle if it lies on the left or top side or is completely within the rectangle.</span></span> <span data-ttu-id="8e73d-114">如果這個點位於右邊或底部，則不在矩形中。</span><span class="sxs-lookup"><span data-stu-id="8e73d-114">The point is not in the rectangle if it lies on the right or bottom side.</span></span>

<span data-ttu-id="8e73d-115">[**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect)函數會建立新的矩形，這是兩個現有矩形的交集，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8e73d-115">The [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) function creates a new rectangle that is the intersection of two existing rectangles, as shown in the following figure.</span></span>

![<span data-ttu-id="8e73d-116">顯示兩個重迭矩形的圖例，以較深的陰影來指出交集</span><span class="sxs-lookup"><span data-stu-id="8e73d-116">illustration showing two overlapping rectangles, with darker shading to indicate the intersection</span></span> ](images/csrec-01.png)

<span data-ttu-id="8e73d-117">[**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect)函式會建立一個新的矩形，其為兩個現有矩形的聯集，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8e73d-117">The [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) function creates a new rectangle that is the union of two existing rectangles, as shown in the following figure.</span></span>

![兩個重迭矩形的圖例，以較深的陰影表示等位內的區域，但不在任一矩形內](images/csrec-02.png)

<span data-ttu-id="8e73d-119">如需繪製橢圓形和多邊形之函式的詳細資訊，請參閱 [填滿的圖形](filled-shapes.md)。</span><span class="sxs-lookup"><span data-stu-id="8e73d-119">For information about functions that draw ellipses and polygons, see [Filled Shapes](filled-shapes.md).</span></span>

 

 



