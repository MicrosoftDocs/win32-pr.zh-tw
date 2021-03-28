---
description: 下列函式可用於矩形。
ms.assetid: b03da8c9-ee6d-4045-8d90-8beceb09ead5
title: 矩形函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5c72812363185217e5cf30ae88447f82edc42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191920"
---
# <a name="rectangle-functions"></a><span data-ttu-id="627c5-103">矩形函數</span><span class="sxs-lookup"><span data-stu-id="627c5-103">Rectangle Functions</span></span>

<span data-ttu-id="627c5-104">下列函式可用於矩形。</span><span class="sxs-lookup"><span data-stu-id="627c5-104">The following functions are used with rectangles.</span></span>



| <span data-ttu-id="627c5-105">函式</span><span class="sxs-lookup"><span data-stu-id="627c5-105">Function</span></span>                               | <span data-ttu-id="627c5-106">描述</span><span class="sxs-lookup"><span data-stu-id="627c5-106">Description</span></span>                                                                                                                                   |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="627c5-107">**CopyRect**</span><span class="sxs-lookup"><span data-stu-id="627c5-107">**CopyRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyrect)           | <span data-ttu-id="627c5-108">將一個矩形的座標複製到另一個矩形。</span><span class="sxs-lookup"><span data-stu-id="627c5-108">Copies the coordinates of one rectangle to another.</span></span>                                                                                           |
| [<span data-ttu-id="627c5-109">**EqualRect**</span><span class="sxs-lookup"><span data-stu-id="627c5-109">**EqualRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-equalrect)         | <span data-ttu-id="627c5-110">藉由比較左上角和右下角的座標，判斷兩個指定的矩形是否相等。</span><span class="sxs-lookup"><span data-stu-id="627c5-110">Determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.</span></span>           |
| [<span data-ttu-id="627c5-111">**InflateRect**</span><span class="sxs-lookup"><span data-stu-id="627c5-111">**InflateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-inflaterect)     | <span data-ttu-id="627c5-112">增加或減少指定矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="627c5-112">Increases or decreases the width and height of the specified rectangle.</span></span>                                                                       |
| [<span data-ttu-id="627c5-113">**IntersectRect**</span><span class="sxs-lookup"><span data-stu-id="627c5-113">**IntersectRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-intersectrect) | <span data-ttu-id="627c5-114">計算兩個來源矩形的交集，並將交集矩形的座標放入目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="627c5-114">Calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle.</span></span> |
| [<span data-ttu-id="627c5-115">**IsRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="627c5-115">**IsRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isrectempty)     | <span data-ttu-id="627c5-116">判斷指定的矩形是否為空白。</span><span class="sxs-lookup"><span data-stu-id="627c5-116">Determines whether the specified rectangle is empty.</span></span>                                                                                          |
| [<span data-ttu-id="627c5-117">**OffsetRect**</span><span class="sxs-lookup"><span data-stu-id="627c5-117">**OffsetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-offsetrect)       | <span data-ttu-id="627c5-118">依據指定的位移移動指定的矩形。</span><span class="sxs-lookup"><span data-stu-id="627c5-118">Moves the specified rectangle by the specified offsets.</span></span>                                                                                       |
| [<span data-ttu-id="627c5-119">**>ptinrect**</span><span class="sxs-lookup"><span data-stu-id="627c5-119">**PtInRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ptinrect)           | <span data-ttu-id="627c5-120">判斷指定的點是否位於指定的矩形內。</span><span class="sxs-lookup"><span data-stu-id="627c5-120">Determines whether the specified point lies within the specified rectangle.</span></span>                                                                   |
| [<span data-ttu-id="627c5-121">**SetRect**</span><span class="sxs-lookup"><span data-stu-id="627c5-121">**SetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrect)             | <span data-ttu-id="627c5-122">設定指定之矩形的座標。</span><span class="sxs-lookup"><span data-stu-id="627c5-122">Sets the coordinates of the specified rectangle.</span></span>                                                                                              |
| [<span data-ttu-id="627c5-123">**SetRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="627c5-123">**SetRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrectempty)   | <span data-ttu-id="627c5-124">建立空的矩形，其中所有座標都設為零。</span><span class="sxs-lookup"><span data-stu-id="627c5-124">Creates an empty rectangle in which all coordinates are set to zero.</span></span>                                                                          |
| [<span data-ttu-id="627c5-125">**SubtractRect**</span><span class="sxs-lookup"><span data-stu-id="627c5-125">**SubtractRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-subtractrect)   | <span data-ttu-id="627c5-126">決定矩形的座標，該矩形是藉由從另一個矩形減去另一個矩形所形成。</span><span class="sxs-lookup"><span data-stu-id="627c5-126">Determines the coordinates of a rectangle formed by subtracting one rectangle from another.</span></span>                                                   |
| [<span data-ttu-id="627c5-127">**UnionRect**</span><span class="sxs-lookup"><span data-stu-id="627c5-127">**UnionRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unionrect)         | <span data-ttu-id="627c5-128">建立兩個矩形的聯集。</span><span class="sxs-lookup"><span data-stu-id="627c5-128">Creates the union of two rectangles.</span></span>                                                                                                          |



 

 

 



