---
title: 路徑幾何總覽
description: 描述如何使用路徑幾何來定義複雜的圖形。
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104568766"
---
# <a name="path-geometries-overview"></a><span data-ttu-id="e831f-103">路徑幾何總覽</span><span class="sxs-lookup"><span data-stu-id="e831f-103">Path Geometries Overview</span></span>

<span data-ttu-id="e831f-104">本主題說明如何使用 Direct2D 路徑幾何來建立複雜的繪圖。</span><span class="sxs-lookup"><span data-stu-id="e831f-104">This topic describes how to use Direct2D path geometries to create complex drawings.</span></span> <span data-ttu-id="e831f-105">包含以下幾節。</span><span class="sxs-lookup"><span data-stu-id="e831f-105">It contains the following sections.</span></span>

-   [<span data-ttu-id="e831f-106">先決條件</span><span class="sxs-lookup"><span data-stu-id="e831f-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="e831f-107">Direct2D 中的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-107">Path Geometries in Direct2D</span></span>](#path-geometries-in-direct2d)
-   [<span data-ttu-id="e831f-108">使用 ID2D1GeometrySink 來填入路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-108">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [<span data-ttu-id="e831f-109">範例：建立複雜的繪圖</span><span class="sxs-lookup"><span data-stu-id="e831f-109">Example: Create a Complex Drawing</span></span>](#example-create-a-complex-drawing)
    -   [<span data-ttu-id="e831f-110">建立左方山地的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-110">Create a Path Geometry for the Left Mountain</span></span>](#create-a-path-geometry-for-the-left-mountain)
    -   [<span data-ttu-id="e831f-111">建立適用于右山地的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-111">Create a Path Geometry for the Right Mountain</span></span>](#create-a-path-geometry-for-the-right-mountain)
    -   [<span data-ttu-id="e831f-112">建立 Sun 的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-112">Create a Path Geometry for the Sun</span></span>](#create-a-path-geometry-for-the-sun)
    -   [<span data-ttu-id="e831f-113">建立河的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-113">Create a Path Geometry for the River</span></span>](#create-a-path-geometry-for-the-river)
    -   [<span data-ttu-id="e831f-114">將路徑幾何轉譯至顯示</span><span class="sxs-lookup"><span data-stu-id="e831f-114">Render the Path Geometries onto the Display</span></span>](#render-the-path-geometries-onto-the-display)
-   [<span data-ttu-id="e831f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e831f-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="e831f-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="e831f-116">Prerequisites</span></span>

<span data-ttu-id="e831f-117">本總覽假設您已經熟悉如何建立基本的 Direct2D 應用程式，如 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e831f-117">This overview assumes that you are familiar with creating basic Direct2D applications, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span> <span data-ttu-id="e831f-118">它也假設您已熟悉 Direct2D 幾何的基本功能，如 [幾何總覽](direct2d-geometries-overview.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e831f-118">It also assumes that you are familiar with the basic features of Direct2D geometries, as described in the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="path-geometries-in-direct2d"></a><span data-ttu-id="e831f-119">Direct2D 中的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-119">Path Geometries in Direct2D</span></span>

<span data-ttu-id="e831f-120">路徑幾何會以 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="e831f-120">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="e831f-121">若要具現化路徑幾何，請呼叫 [**ID2D1Factory：： CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) 方法。</span><span class="sxs-lookup"><span data-stu-id="e831f-121">To instantiate a path geometry, call the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span> <span data-ttu-id="e831f-122">這些物件可用來描述由弧線、曲線和線條等線段組成的複雜幾何圖形。</span><span class="sxs-lookup"><span data-stu-id="e831f-122">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="e831f-123">若要在路徑幾何中填入圖表和區段，請呼叫 [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) 方法來取出 [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) ，並使用 geometry 接收器的方法將圖形和區段加入至路徑幾何。</span><span class="sxs-lookup"><span data-stu-id="e831f-123">To populate a path geometry with figures and segments, call the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) and use the geometry sink's methods to add figures and segments to the path geometry.</span></span>

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a><span data-ttu-id="e831f-124">使用 ID2D1GeometrySink 來填入路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-124">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>

<span data-ttu-id="e831f-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) 描述的幾何路徑可以包含線條、弧線、三次方貝茲曲線，以及二次方貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="e831f-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) describes a geometric path that can contain lines, arcs, cubic Bezier curves, and quadratic Bezier curves.</span></span>

<span data-ttu-id="e831f-126">幾何接收器是由一或多個圖表所組成。</span><span class="sxs-lookup"><span data-stu-id="e831f-126">A geometry sink consists of one or more figures.</span></span> <span data-ttu-id="e831f-127">每個圖表都是由一或多個線條、曲線或弧線區段所組成。</span><span class="sxs-lookup"><span data-stu-id="e831f-127">Each figure is made up of one or more line, curve, or arc segments.</span></span> <span data-ttu-id="e831f-128">若要建立圖表，請呼叫 [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) 方法，並傳入圖表的起點，然後使用其 add 方法 (例如 [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) 和 [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 來加入區段。</span><span class="sxs-lookup"><span data-stu-id="e831f-128">To create a figure, call the [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) method, passing in the figure's starting point, and then use its Add methods (such as [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) and [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to add segments.</span></span> <span data-ttu-id="e831f-129">當您完成加入區段時，請呼叫 [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) 方法。</span><span class="sxs-lookup"><span data-stu-id="e831f-129">When you are finished adding segments, call the [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) method.</span></span> <span data-ttu-id="e831f-130">您可以重複此順序來建立其他圖形。</span><span class="sxs-lookup"><span data-stu-id="e831f-130">You can repeat this sequence to create additional figures.</span></span> <span data-ttu-id="e831f-131">當您完成建立圖表時，請呼叫 [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) 方法。</span><span class="sxs-lookup"><span data-stu-id="e831f-131">When you are finished creating figures, call the [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) method.</span></span>

## <a name="example-create-a-complex-drawing"></a><span data-ttu-id="e831f-132">範例：建立複雜的繪圖</span><span class="sxs-lookup"><span data-stu-id="e831f-132">Example: Create a Complex Drawing</span></span>

<span data-ttu-id="e831f-133">下圖顯示具有線條、弧形和貝茲曲線的複雜繪圖。</span><span class="sxs-lookup"><span data-stu-id="e831f-133">The following illustration shows a complex drawing with lines, arcs, and Bezier curves.</span></span> <span data-ttu-id="e831f-134">接下來的程式碼範例會示範如何使用四個路徑幾何物件（一個用於左方的山區）來建立繪圖、將一個用於右山地、一個用於一張，以及一個適用于 sun 的光暈。</span><span class="sxs-lookup"><span data-stu-id="e831f-134">The code example that follows shows how to create the drawing by using four path geometry objects, one for the left mountain, one for the right mountain, one for the river, and one for the sun with flares.</span></span>

![使用路徑幾何的河、山脈和 sun 圖例](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a><span data-ttu-id="e831f-136">建立左方山地的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-136">Create a Path Geometry for the Left Mountain</span></span>

<span data-ttu-id="e831f-137">此範例會先建立左方山地的路徑幾何，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="e831f-137">The example first creates a path geometry for the left mountain as shown in the following illustration.</span></span>

![顯示表示山地的多邊形複雜繪圖。](images/path-geo-leftmnt.png)

<span data-ttu-id="e831f-139">為了建立左方的山，此範例會呼叫 [**ID2D1Factory：： CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) 方法來建立 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)。</span><span class="sxs-lookup"><span data-stu-id="e831f-139">To create the left mountain, the example calls the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



<span data-ttu-id="e831f-140">然後，此範例會使用 [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) 方法從 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 取得幾何接收器，並將其儲存在 *pSink* 變數中。</span><span class="sxs-lookup"><span data-stu-id="e831f-140">The example then uses the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to obtain a geometry sink from an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and stores it in the *pSink* variable.</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



<span data-ttu-id="e831f-141">然後，此範例會呼叫 [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure)，並在 [**D2D1 \_ 圖中 \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) 傳入，指出此圖表已填滿，然後呼叫 [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines)，傳入 [**D2D1 \_ 點 \_**](d2d1-point-2f.md) 的陣列、 (267、177) 、 (236、192) 、 (212、160) 、 (156、255) 和 (346、255) 。</span><span class="sxs-lookup"><span data-stu-id="e831f-141">The example then calls [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passing in [**D2D1\_FIGURE\_BEGIN\_FILLED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) that indicates this figure is filled, then calls [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passing in an array of [**D2D1\_POINT\_2F**](d2d1-point-2f.md) points, (267, 177), (236, 192), (212, 160), (156, 255) and (346, 255).</span></span>

<span data-ttu-id="e831f-142">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="e831f-142">The following code shows how to do this.</span></span>


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a><span data-ttu-id="e831f-143">建立適用于右山地的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-143">Create a Path Geometry for the Right Mountain</span></span>

<span data-ttu-id="e831f-144">接著，此範例會為右山建立另一個路徑幾何，其點為 (481、146) 、 (449、181) 、 (433、159) 、 (401、214) 、 (381、199) 、 (323、263) 和 (575、263) 。</span><span class="sxs-lookup"><span data-stu-id="e831f-144">The example then creates another path geometry for the right mountain with points (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263), and (575, 263).</span></span> <span data-ttu-id="e831f-145">下圖顯示如何顯示右邊的山地。</span><span class="sxs-lookup"><span data-stu-id="e831f-145">The following illustration shows how the right mountain is displayed.</span></span>

![顯示山地的多邊形圖例](images/path-geo-rightmnt.png)

<span data-ttu-id="e831f-147">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="e831f-147">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a><span data-ttu-id="e831f-148">建立 Sun 的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-148">Create a Path Geometry for the Sun</span></span>

<span data-ttu-id="e831f-149">然後，此範例會將另一個路徑幾何填入至太陽，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="e831f-149">The example then populates another path geometry for the sun as shown in the following illustration.</span></span>

![顯示太陽的弧形和貝茲曲線圖例](images/path-geo-sun.png)

<span data-ttu-id="e831f-151">若要這樣做，路徑幾何會建立一個接收，然後將每個光暈的曲線和一個圖表加入至接收器。</span><span class="sxs-lookup"><span data-stu-id="e831f-151">To do this, the path geometry creates a sink, and adds a figure for the arc and a figure for each flare to the sink.</span></span> <span data-ttu-id="e831f-152">藉由重複 [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure)順序，其 Add (例如 [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) 方法和 [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure)，會將多個資料新增至接收器。</span><span class="sxs-lookup"><span data-stu-id="e831f-152">By repeating the sequence of [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), its Add (such as [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) methods, and [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), multiple figures are added to the sink.</span></span>

<span data-ttu-id="e831f-153">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="e831f-153">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a><span data-ttu-id="e831f-154">建立河的路徑幾何</span><span class="sxs-lookup"><span data-stu-id="e831f-154">Create a Path Geometry for the River</span></span>

<span data-ttu-id="e831f-155">然後，此範例會為包含貝茲曲線的河建立另一個幾何路徑。</span><span class="sxs-lookup"><span data-stu-id="e831f-155">The example then creates another geometry path for the river that contains Bezier curves.</span></span> <span data-ttu-id="e831f-156">下圖顯示的是如何顯示中的。</span><span class="sxs-lookup"><span data-stu-id="e831f-156">The following illustration shows how the river is displayed.</span></span>

![顯示河的貝茲曲線圖例](images/path-geo-river.png)

<span data-ttu-id="e831f-158">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="e831f-158">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a><span data-ttu-id="e831f-159">將路徑幾何轉譯至顯示</span><span class="sxs-lookup"><span data-stu-id="e831f-159">Render the Path Geometries onto the Display</span></span>

<span data-ttu-id="e831f-160">下列程式碼示範如何在顯示上呈現已填入的路徑幾何。</span><span class="sxs-lookup"><span data-stu-id="e831f-160">The following code shows how to render the populated path geometries on the display.</span></span> <span data-ttu-id="e831f-161">它會先繪製和繪製 sun 幾何、左方的山地幾何、下出的幾何，最後是右邊的山地幾何。</span><span class="sxs-lookup"><span data-stu-id="e831f-161">It first draws and paints the sun geometry, next the left mountain geometry, then the river geometry, and finally the right mountain geometry.</span></span>


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



<span data-ttu-id="e831f-162">完整的範例會輸出下圖。</span><span class="sxs-lookup"><span data-stu-id="e831f-162">The complete example outputs the following illustration.</span></span>

![使用路徑幾何的河、山脈和 sun 圖例](images/path-geo-mnts.png)

## <a name="related-topics"></a><span data-ttu-id="e831f-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="e831f-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e831f-165">建立簡單的 Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="e831f-165">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> <dt>

[<span data-ttu-id="e831f-166">幾何概觀</span><span class="sxs-lookup"><span data-stu-id="e831f-166">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> </dl>

 

 