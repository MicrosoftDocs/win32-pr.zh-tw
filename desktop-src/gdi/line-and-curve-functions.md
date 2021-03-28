---
description: 下列函式可用於線條和曲線。
ms.assetid: 90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b
title: Line 和 Curve 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bf04160e8b9cc0a5c2fb28378bce82a1c7650a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991195"
---
# <a name="line-and-curve-functions"></a><span data-ttu-id="6758c-103">Line 和 Curve 函數</span><span class="sxs-lookup"><span data-stu-id="6758c-103">Line and Curve Functions</span></span>

<span data-ttu-id="6758c-104">下列函式可用於線條和曲線。</span><span class="sxs-lookup"><span data-stu-id="6758c-104">The following functions are used with lines and curves.</span></span>



| <span data-ttu-id="6758c-105">函式</span><span class="sxs-lookup"><span data-stu-id="6758c-105">Function</span></span>                                   | <span data-ttu-id="6758c-106">描述</span><span class="sxs-lookup"><span data-stu-id="6758c-106">Description</span></span>                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6758c-107">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="6758c-107">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)               | <span data-ttu-id="6758c-108">繪製線段和弧形。</span><span class="sxs-lookup"><span data-stu-id="6758c-108">Draws a line segment and an arc.</span></span>                                                                              |
| [<span data-ttu-id="6758c-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="6758c-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)                         | <span data-ttu-id="6758c-110">繪製橢圓形弧線。</span><span class="sxs-lookup"><span data-stu-id="6758c-110">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="6758c-111">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="6758c-111">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)                     | <span data-ttu-id="6758c-112">繪製橢圓形弧線。</span><span class="sxs-lookup"><span data-stu-id="6758c-112">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="6758c-113">**GetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="6758c-113">**GetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) | <span data-ttu-id="6758c-114">抓取指定之裝置內容的目前弧線方向。</span><span class="sxs-lookup"><span data-stu-id="6758c-114">Retrieves the current arc direction for the specified device context.</span></span>                                         |
| [<span data-ttu-id="6758c-115">**LineDDA**</span><span class="sxs-lookup"><span data-stu-id="6758c-115">**LineDDA**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-linedda)                 | <span data-ttu-id="6758c-116">決定哪些圖元應針對指定的起始點和結束點所定義的線條反白顯示。</span><span class="sxs-lookup"><span data-stu-id="6758c-116">Determines which pixels should be highlighted for a line defined by the specified starting and ending points.</span></span> |
| [<span data-ttu-id="6758c-117">**LineDDAProc**</span><span class="sxs-lookup"><span data-stu-id="6758c-117">**LineDDAProc**</span></span>](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)         | <span data-ttu-id="6758c-118">搭配 LineDDA 函式使用的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="6758c-118">An application-defined callback function used with the LineDDA function.</span></span>                                      |
| [<span data-ttu-id="6758c-119">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="6758c-119">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)                   | <span data-ttu-id="6758c-120">從目前的位置（但不包含指定的點）繪製線條。</span><span class="sxs-lookup"><span data-stu-id="6758c-120">Draws a line from the current position up to, but not including, the specified point.</span></span>                         |
| [<span data-ttu-id="6758c-121">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="6758c-121">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)               | <span data-ttu-id="6758c-122">將目前的位置更新為指定的點，並選擇性地傳回先前的位置。</span><span class="sxs-lookup"><span data-stu-id="6758c-122">Updates the current position to the specified point and optionally returns the previous position.</span></span>             |
| [<span data-ttu-id="6758c-123">**PolyBezier**</span><span class="sxs-lookup"><span data-stu-id="6758c-123">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)           | <span data-ttu-id="6758c-124">繪製一或多個貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="6758c-124">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="6758c-125">**PolyBezierTo**</span><span class="sxs-lookup"><span data-stu-id="6758c-125">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)       | <span data-ttu-id="6758c-126">繪製一或多個貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="6758c-126">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="6758c-127">**PolyDraw**</span><span class="sxs-lookup"><span data-stu-id="6758c-127">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)               | <span data-ttu-id="6758c-128">繪製一組直線線段和貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="6758c-128">Draws a set of line segments and Bézier curves.</span></span>                                                               |
| [<span data-ttu-id="6758c-129">**聚合線條**</span><span class="sxs-lookup"><span data-stu-id="6758c-129">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)               | <span data-ttu-id="6758c-130">藉由連接指定陣列中的點，繪製一連串的線段。</span><span class="sxs-lookup"><span data-stu-id="6758c-130">Draws a series of line segments by connecting the points in the specified array.</span></span>                              |
| [<span data-ttu-id="6758c-131">**PolylineTo**</span><span class="sxs-lookup"><span data-stu-id="6758c-131">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)           | <span data-ttu-id="6758c-132">繪製一或多個直條。</span><span class="sxs-lookup"><span data-stu-id="6758c-132">Draws one or more straight lines.</span></span>                                                                             |
| [<span data-ttu-id="6758c-133">**PolyPolyline**</span><span class="sxs-lookup"><span data-stu-id="6758c-133">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)       | <span data-ttu-id="6758c-134">繪製多個連接線線段的序列。</span><span class="sxs-lookup"><span data-stu-id="6758c-134">Draws multiple series of connected line segments.</span></span>                                                             |
| [<span data-ttu-id="6758c-135">**SetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="6758c-135">**SetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) | <span data-ttu-id="6758c-136">設定要用於弧線和矩形函數的繪製方向。</span><span class="sxs-lookup"><span data-stu-id="6758c-136">Sets the drawing direction to be used for arc and rectangle functions.</span></span>                                        |



 

 

 



