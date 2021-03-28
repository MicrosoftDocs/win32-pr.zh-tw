---
description: Windows GDI + 的服務分為下列三種廣泛的類別：
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: GDI + 的三個部分
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2021260e9fe3b3d927131c2ba1856aeed0ed07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991314"
---
# <a name="the-three-parts-of-gdi"></a><span data-ttu-id="2878f-103">GDI + 的三個部分</span><span class="sxs-lookup"><span data-stu-id="2878f-103">The Three Parts of GDI+</span></span>

<span data-ttu-id="2878f-104">Windows GDI + 的服務分為下列三種廣泛的類別：</span><span class="sxs-lookup"><span data-stu-id="2878f-104">The services of Windows GDI+ fall into the following three broad categories:</span></span>

-   [<span data-ttu-id="2878f-105">2D 向量圖形</span><span class="sxs-lookup"><span data-stu-id="2878f-105">2-D vector graphics</span></span>](#2-d-vector-graphics)
-   [<span data-ttu-id="2878f-106">建立映像</span><span class="sxs-lookup"><span data-stu-id="2878f-106">Imaging</span></span>](#imaging)
-   [<span data-ttu-id="2878f-107">印刷樣式</span><span class="sxs-lookup"><span data-stu-id="2878f-107">Typography</span></span>](#typography)

## <a name="2-d-vector-graphics"></a><span data-ttu-id="2878f-108">2D 向量圖形</span><span class="sxs-lookup"><span data-stu-id="2878f-108">2-D vector graphics</span></span>

<span data-ttu-id="2878f-109">向量圖形包含繪製基本 (，例如線條、曲線和圖形，) 由座標系統上的點集所指定。</span><span class="sxs-lookup"><span data-stu-id="2878f-109">Vector graphics involves drawing primitives (such as lines, curves, and figures) that are specified by sets of points on a coordinate system.</span></span> <span data-ttu-id="2878f-110">例如，直線可以由它的兩個端點來指定，並可指定矩形的點，提供其左上角的位置，以及提供其寬度和高度的數位配對。</span><span class="sxs-lookup"><span data-stu-id="2878f-110">For example, a straight line can be specified by its two endpoints, and a rectangle can be specified by a point giving the location of its upper-left corner and a pair of numbers giving its width and height.</span></span> <span data-ttu-id="2878f-111">簡單路徑可由點陣列指定，以直線連接。</span><span class="sxs-lookup"><span data-stu-id="2878f-111">A simple path can be specified by an array of points to be connected by straight lines.</span></span> <span data-ttu-id="2878f-112">貝茲曲線是由四個控制點所指定的複雜曲線。</span><span class="sxs-lookup"><span data-stu-id="2878f-112">A Bézier spline is a sophisticated curve specified by four control points.</span></span>

<span data-ttu-id="2878f-113">GDI + 提供的類別會儲存基本型別的相關資訊、儲存基本專案相關資訊的類別，以及實際進行繪製的類別。</span><span class="sxs-lookup"><span data-stu-id="2878f-113">GDI+ provides classes that store information about the primitives themselves, classes that store information about how the primitives are to be drawn, and classes that actually do the drawing.</span></span> <span data-ttu-id="2878f-114">例如， **Rect** 類別會儲存矩形的位置和大小; **Pen** 類別會儲存線條色彩、線條寬度和線條樣式的相關資訊;和 **圖形** 類別具有繪製線條、矩形、路徑和其他圖形的方法。</span><span class="sxs-lookup"><span data-stu-id="2878f-114">For example, the **Rect** class stores the location and size of a rectangle; the **Pen** class stores information about line color, line width, and line style; and the **Graphics** class has methods for drawing lines, rectangles, paths, and other figures.</span></span> <span data-ttu-id="2878f-115">另外還有數個 **筆刷** 類別，可儲存有關如何以色彩或模式填滿封閉的圖形和路徑的資訊。</span><span class="sxs-lookup"><span data-stu-id="2878f-115">There are also several **Brush** classes that store information about how closed figures and paths are to be filled with colors or patterns.</span></span>

## <a name="imaging"></a><span data-ttu-id="2878f-116">建立映像</span><span class="sxs-lookup"><span data-stu-id="2878f-116">Imaging</span></span>

<span data-ttu-id="2878f-117">使用向量圖形的技巧很難或無法顯示特定類型的圖片。</span><span class="sxs-lookup"><span data-stu-id="2878f-117">Certain kinds of pictures are difficult or impossible to display with the techniques of vector graphics.</span></span> <span data-ttu-id="2878f-118">例如，工具列按鈕上的圖片和顯示為圖示的圖片，都很難指定為線條和曲線的集合。</span><span class="sxs-lookup"><span data-stu-id="2878f-118">For example, the pictures on toolbar buttons and the pictures that appear as icons would be difficult to specify as collections of lines and curves.</span></span> <span data-ttu-id="2878f-119">更難使用向量技術來建立擁擠棒球體育場的高解析度數位相片。</span><span class="sxs-lookup"><span data-stu-id="2878f-119">A high-resolution digital photograph of a crowded baseball stadium would be even more difficult to create with vector techniques.</span></span> <span data-ttu-id="2878f-120">此類型的影像會儲存為點陣圖、數位陣列，代表螢幕上的個別點色彩。</span><span class="sxs-lookup"><span data-stu-id="2878f-120">Images of this type are stored as bitmaps, arrays of numbers that represent the colors of individual dots on the screen.</span></span> <span data-ttu-id="2878f-121">儲存點陣圖相關資訊的資料結構，通常比向量圖形所需的更為複雜，因此 GDI + 中有幾個類別專門用於此用途。</span><span class="sxs-lookup"><span data-stu-id="2878f-121">Data structures that store information about bitmaps tend to be more complex than those required for vector graphics, so there are several classes in GDI+ devoted to this purpose.</span></span> <span data-ttu-id="2878f-122">這類類別的範例是 **CachedBitmap**，它是用來將點陣圖儲存在記憶體中，以供快速存取和顯示。</span><span class="sxs-lookup"><span data-stu-id="2878f-122">An example of such a class is **CachedBitmap**, which is used to store a bitmap in memory for fast access and display.</span></span>

## <a name="typography"></a><span data-ttu-id="2878f-123">印刷樣式</span><span class="sxs-lookup"><span data-stu-id="2878f-123">Typography</span></span>

<span data-ttu-id="2878f-124">印刷樣式與各種字型、大小和樣式的文字顯示相關。</span><span class="sxs-lookup"><span data-stu-id="2878f-124">Typography is concerned with the display of text in a variety of fonts, sizes, and styles.</span></span> <span data-ttu-id="2878f-125">GDI + 針對這項複雜的工作提供了令人印象深刻的支援。</span><span class="sxs-lookup"><span data-stu-id="2878f-125">GDI+ provides an impressive amount of support for this complex task.</span></span> <span data-ttu-id="2878f-126">GDI + 中的其中一項新功能是子圖元消除鋸齒，可讓螢幕上呈現的文字變得更平滑。</span><span class="sxs-lookup"><span data-stu-id="2878f-126">One of the new features in GDI+ is subpixel antialiasing, which gives text rendered on an LCD screen a smoother appearance.</span></span>

 

 



