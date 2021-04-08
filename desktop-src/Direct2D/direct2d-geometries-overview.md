---
title: 幾何概觀
description: 描述 Direct2D 幾何的基本概念、可用於表示、操作及分析圖形的物件。
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D，幾何總覽
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684175"
---
# <a name="geometries-overview"></a><span data-ttu-id="1edfb-104">幾何概觀</span><span class="sxs-lookup"><span data-stu-id="1edfb-104">Geometries overview</span></span>

<span data-ttu-id="1edfb-105">本總覽說明如何建立和使用 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 物件，以定義和操作2d 圖形。</span><span class="sxs-lookup"><span data-stu-id="1edfb-105">This overview describes how to create and use [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) objects to define and manipulate 2D figures.</span></span> <span data-ttu-id="1edfb-106">包含以下幾節。</span><span class="sxs-lookup"><span data-stu-id="1edfb-106">It contains the following sections.</span></span>

## <a name="what-is-a-direct2d-geometry"></a><span data-ttu-id="1edfb-107">什麼是 Direct2D geometry？</span><span class="sxs-lookup"><span data-stu-id="1edfb-107">What is a Direct2D geometry?</span></span>

<span data-ttu-id="1edfb-108">Direct2D geometry 是 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 物件。</span><span class="sxs-lookup"><span data-stu-id="1edfb-108">A Direct2D geometry is an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object.</span></span> <span data-ttu-id="1edfb-109">這個物件可以是簡單幾何 ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)、 [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)或 [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)) 、路徑幾何 ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) ，或是複合幾何 ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) 和 [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)) 。</span><span class="sxs-lookup"><span data-stu-id="1edfb-109">This object can be a simple geometry ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), or [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), a path geometry ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)), or a composite geometry ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) and [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span></span>

<span data-ttu-id="1edfb-110">Direct2D 幾何可讓您描述二維圖形並提供許多用途，例如定義點擊測試區域、裁剪區域，甚至是動畫路徑。</span><span class="sxs-lookup"><span data-stu-id="1edfb-110">Direct2D geometries enable you to describe two-dimensional figures and offer many uses, such as defining hit-test regions, clip regions, and even animation paths.</span></span>

<span data-ttu-id="1edfb-111">Direct2D 幾何是不可變的，且由 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)建立的裝置獨立資源。</span><span class="sxs-lookup"><span data-stu-id="1edfb-111">Direct2D geometries are immutable and device-independent resources created by [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span> <span data-ttu-id="1edfb-112">一般而言，您應該建立一次幾何，並將其保留在應用程式的存留期內，或直到必須變更為止。</span><span class="sxs-lookup"><span data-stu-id="1edfb-112">Generally, you should create geometries one time and keep them for the life of the application, or until they have to be changed.</span></span> <span data-ttu-id="1edfb-113">如需與裝置無關和裝置相依資源的詳細資訊，請參閱 [資源總覽](resources-and-resource-domains.md)。</span><span class="sxs-lookup"><span data-stu-id="1edfb-113">For more information about device-independent and device-dependent resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="1edfb-114">下列各節說明不同類型的幾何。</span><span class="sxs-lookup"><span data-stu-id="1edfb-114">The following sections describe the different kinds of geometries.</span></span>

## <a name="simple-geometries"></a><span data-ttu-id="1edfb-115">簡單幾何</span><span class="sxs-lookup"><span data-stu-id="1edfb-115">Simple geometries</span></span>

<span data-ttu-id="1edfb-116">簡單幾何包括 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)、 [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)和 [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) 物件，可用來建立基本的幾何圖形，例如矩形、圓角矩形、圓形和省略號。</span><span class="sxs-lookup"><span data-stu-id="1edfb-116">Simple geometries include [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), and [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects, and can be used to create basic geometric figures, such as rectangles, rounded rectangles, circles, and ellipses.</span></span>

<span data-ttu-id="1edfb-117">若要建立簡單幾何，請使用其中一個 [**ID2D1Factory：： create<*GeometryType*>幾何**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 方法。</span><span class="sxs-lookup"><span data-stu-id="1edfb-117">To create a simple geometry, use one of the [**ID2D1Factory::Create<*geometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) methods.</span></span> <span data-ttu-id="1edfb-118">這些方法會建立指定之類型的物件。</span><span class="sxs-lookup"><span data-stu-id="1edfb-118">These methods create an object of the specified type.</span></span> <span data-ttu-id="1edfb-119">例如，若要建立矩形，請呼叫 [**ID2D1Factory：： CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))，它會傳回 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) 物件;若要建立圓角矩形，請呼叫 [**ID2D1Factory：： CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry))，它會傳回 [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) 物件等等。</span><span class="sxs-lookup"><span data-stu-id="1edfb-119">For example, to create a rectangle, call [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), which returns an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object; to create a rounded rectangle, call [**ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), which returns an [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) object, and so on.</span></span>

<span data-ttu-id="1edfb-120">下列程式碼範例會呼叫 [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) 方法，並將 *中央* 設定為 (100、100) 、 *x-半徑* 至100，以及 *y 半徑* 至50的橢圓形結構。</span><span class="sxs-lookup"><span data-stu-id="1edfb-120">The following code example calls the [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) method, passing in an ellipse structure with the *center* set to (100, 100), *x-radius* to 100, and *y-radius* to 50.</span></span> <span data-ttu-id="1edfb-121">然後，它會呼叫 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)，傳入傳回的橢圓形幾何、黑色 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)的指標，以及5的筆觸寬度。</span><span class="sxs-lookup"><span data-stu-id="1edfb-121">Then, it calls [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passing in the returned ellipse geometry, a pointer to a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), and a stroke width of 5.</span></span> <span data-ttu-id="1edfb-122">下圖顯示程式碼範例的輸出。</span><span class="sxs-lookup"><span data-stu-id="1edfb-122">The following illustration shows the output from the code example.</span></span>

![橢圓形的圖例](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



<span data-ttu-id="1edfb-124">若要繪製任何幾何的外框，請使用 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 方法。</span><span class="sxs-lookup"><span data-stu-id="1edfb-124">To draw the outline of any geometry, use the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method.</span></span> <span data-ttu-id="1edfb-125">若要繪製其內部，請使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法。</span><span class="sxs-lookup"><span data-stu-id="1edfb-125">To paint its interior, use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

## <a name="path-geometries"></a><span data-ttu-id="1edfb-126">路徑幾何</span><span class="sxs-lookup"><span data-stu-id="1edfb-126">Path geometries</span></span>

<span data-ttu-id="1edfb-127">路徑幾何會以 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="1edfb-127">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="1edfb-128">這些物件可用來描述由弧線、曲線和線條等線段組成的複雜幾何圖形。</span><span class="sxs-lookup"><span data-stu-id="1edfb-128">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="1edfb-129">下圖顯示使用路徑幾何建立的繪圖。</span><span class="sxs-lookup"><span data-stu-id="1edfb-129">The following illustration shows a drawing created by using path geometry.</span></span>

![河、山脈和 sun 的圖例](images/path-geo-mnts.png)

<span data-ttu-id="1edfb-131">如需詳細資訊和範例，請參閱 [路徑幾何總覽](path-geometries-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1edfb-131">For more information and examples, see the [Path Geometries Overview](path-geometries-overview.md).</span></span>

## <a name="composite-geometries"></a><span data-ttu-id="1edfb-132">複合幾何</span><span class="sxs-lookup"><span data-stu-id="1edfb-132">Composite geometries</span></span>

<span data-ttu-id="1edfb-133">複合幾何是將幾何分組或與另一個幾何物件合併，或與轉換合併。</span><span class="sxs-lookup"><span data-stu-id="1edfb-133">A composite geometry is a geometry grouped or combined with another geometry object, or with a transform.</span></span> <span data-ttu-id="1edfb-134">複合幾何包含 [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) 和 [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) 物件。</span><span class="sxs-lookup"><span data-stu-id="1edfb-134">Composite geometries include [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) and [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) objects.</span></span>

### <a name="geometry-groups"></a><span data-ttu-id="1edfb-135">Geometry 群組</span><span class="sxs-lookup"><span data-stu-id="1edfb-135">Geometry groups</span></span>

<span data-ttu-id="1edfb-136">Geometry 群組是一種方便的方式，可同時將數個幾何分組，讓數個相異幾何的所有圖形都串連成一個。</span><span class="sxs-lookup"><span data-stu-id="1edfb-136">Geometry groups are a convenient way to group several geometries at the same time so all figures of several distinct geometries are concatenated into one.</span></span> <span data-ttu-id="1edfb-137">若要建立 [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup)物件，請在 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)物件上呼叫 [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup)方法，並在 *fillMode* 中傳入 [**D2D1 \_ 填滿 \_ 模式 \_ 替代**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (替代) 和 **D2D1 \_ 填滿 \_ 模式 \_ 繞組**、要加入至 geometry 群組的幾何物件陣列，以及這個陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="1edfb-137">To create a [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) object, call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) method on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in the *fillMode* with possible values of [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternate) and **D2D1\_FILL\_MODE\_WINDING**, an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>

<span data-ttu-id="1edfb-138">下列程式碼範例會先宣告 geometry 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="1edfb-138">The following code example first declares an array of geometry objects.</span></span> <span data-ttu-id="1edfb-139">這些物件是四個具有下列半徑的同心圓：25、50、75和100。</span><span class="sxs-lookup"><span data-stu-id="1edfb-139">These objects are four concentric circles that have the following radii: 25, 50, 75, and 100.</span></span> <span data-ttu-id="1edfb-140">然後，在 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)物件上呼叫 [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) ，傳入 [**D2D1 \_ 填滿 \_ 模式 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode)、要加入至 geometry 群組的 geometry 物件陣列，以及這個陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="1edfb-140">Then call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>


```C++
ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory->CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &m_pGeoGroup_WindingFill
        );
}
```

<span data-ttu-id="1edfb-141">下圖顯示從範例呈現兩個群組幾何的結果。</span><span class="sxs-lookup"><span data-stu-id="1edfb-141">The following illustration shows the results of rendering the two group geometries from the example.</span></span>

![四個同心圓的圖，其中有一組已填滿的交替環形，另一個則填滿所有環形](images/create-geometry-group.png)

### <a name="transformed-geometries"></a><span data-ttu-id="1edfb-143">轉換的幾何</span><span class="sxs-lookup"><span data-stu-id="1edfb-143">Transformed geometries</span></span>

<span data-ttu-id="1edfb-144">有多種方式可以轉換幾何。</span><span class="sxs-lookup"><span data-stu-id="1edfb-144">There are multiple ways to transform a geometry.</span></span> <span data-ttu-id="1edfb-145">您可以使用轉譯目標的 [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) 方法來轉換轉譯目標繪製的所有專案，或者您可以使用 [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) 方法來建立 [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))，直接將轉換與幾何產生關聯。</span><span class="sxs-lookup"><span data-stu-id="1edfb-145">You can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of a render target to transform everything that the render target draws, or you can associate a transform directly with a geometry by using the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) method to create an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span></span>

<span data-ttu-id="1edfb-146">您應該使用的方法取決於您想要的效果。</span><span class="sxs-lookup"><span data-stu-id="1edfb-146">The method that you should use depends on the effect that you want.</span></span> <span data-ttu-id="1edfb-147">當您使用轉譯目標來轉換幾何，然後轉譯幾何時，轉換會影響幾何的所有內容，包括您已套用的任何筆觸寬度。</span><span class="sxs-lookup"><span data-stu-id="1edfb-147">When you use the render target to transform and then render a geometry, the transform affects everything about the geometry, including the width of any stroke that you have applied.</span></span> <span data-ttu-id="1edfb-148">另一方面，當您使用 [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)時，轉換只會影響描述圖形的座標。</span><span class="sxs-lookup"><span data-stu-id="1edfb-148">On the other hand, when you use an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), the transform affects only the coordinates that describe the shape.</span></span> <span data-ttu-id="1edfb-149">繪製幾何時，轉換不會影響筆觸粗細。</span><span class="sxs-lookup"><span data-stu-id="1edfb-149">The transformation will not affect the stroke thickness when the geometry is drawn.</span></span>

> [!Note]  
> <span data-ttu-id="1edfb-150">從 Windows 8 開始，世界轉換並不會影響筆觸粗細的筆觸粗細 [**D2D1 \_ 筆觸 \_ 轉換 \_ 類型 \_ 固定**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)或 [**D2D1 \_ 筆觸 \_ 轉換 \_ 類型 \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)的最細效果。</span><span class="sxs-lookup"><span data-stu-id="1edfb-150">Starting with Windows 8 the world transform will not affect the stroke thickness of strokes with [**D2D1\_STROKE\_TRANSFORM\_TYPE\_FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)or [**D2D1\_STROKE\_TRANSFORM\_TYPE\_HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span></span> <span data-ttu-id="1edfb-151">您應使用這些轉換類型來達成轉換的獨立筆劃</span><span class="sxs-lookup"><span data-stu-id="1edfb-151">You should use these transform types to achieve transform independent strokes</span></span>

 

<span data-ttu-id="1edfb-152">下列範例會建立 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)，然後在不轉換的情況下繪製。</span><span class="sxs-lookup"><span data-stu-id="1edfb-152">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), then draws it without transforming it.</span></span> <span data-ttu-id="1edfb-153">它會產生下圖中顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="1edfb-153">It produces the output shown in the following illustration.</span></span>

![矩形的圖例](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="1edfb-155">下一個範例會使用轉譯目標，將幾何調整為3的因數，然後繪製。</span><span class="sxs-lookup"><span data-stu-id="1edfb-155">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="1edfb-156">下圖顯示在沒有轉換和轉換的情況下繪製矩形的結果。</span><span class="sxs-lookup"><span data-stu-id="1edfb-156">The following illustration shows the result of drawing the rectangle without the transform and with the transform.</span></span> <span data-ttu-id="1edfb-157">請注意，即使筆觸粗細為1，筆劃在轉換後會變寬。</span><span class="sxs-lookup"><span data-stu-id="1edfb-157">Notice that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![具有較粗筆觸的大型矩形內較小矩形的圖例](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="1edfb-159">下一個範例會使用 [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) 方法，將幾何調整為3的因數，然後繪製它。</span><span class="sxs-lookup"><span data-stu-id="1edfb-159">The next example uses the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="1edfb-160">它會產生下圖中顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="1edfb-160">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="1edfb-161">請注意，雖然矩形更大，但其筆觸尚未增加。</span><span class="sxs-lookup"><span data-stu-id="1edfb-161">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![具有相同筆觸粗細之大型矩形內較小矩形的圖例](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a><span data-ttu-id="1edfb-163">以遮罩形式的幾何</span><span class="sxs-lookup"><span data-stu-id="1edfb-163">Geometries as masks</span></span>

<span data-ttu-id="1edfb-164">當您呼叫 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))方法時，您可以使用 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)物件做為幾何遮罩。</span><span class="sxs-lookup"><span data-stu-id="1edfb-164">You can use an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object as a geometric mask when you call the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="1edfb-165">幾何遮罩會指定複合到轉譯目標的圖層區域。</span><span class="sxs-lookup"><span data-stu-id="1edfb-165">The geometric mask specifies the area of the layer that is composited into the render target.</span></span> <span data-ttu-id="1edfb-166">如需詳細資訊，請參閱 [圖層](direct2d-layers-overview.md)的 [幾何遮罩] 區段。</span><span class="sxs-lookup"><span data-stu-id="1edfb-166">For more information, see the Geometric Masks section of the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="geometric-operations"></a><span data-ttu-id="1edfb-167">幾何作業</span><span class="sxs-lookup"><span data-stu-id="1edfb-167">Geometric operations</span></span>

<span data-ttu-id="1edfb-168">[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)介面提供數個幾何運算，可讓您用來操作和測量幾何圖形。</span><span class="sxs-lookup"><span data-stu-id="1edfb-168">The [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) interface provides several geometric operations that you can use to manipulate and measure geometric figures.</span></span> <span data-ttu-id="1edfb-169">例如，您可以使用它們來計算並傳回其界限、比較，以瞭解一個幾何如何在空間上與另一個幾何相關聯 (適用于點擊測試) 、計算區域和長度等等。</span><span class="sxs-lookup"><span data-stu-id="1edfb-169">For example, you can use them to calculate and return their bounds, compare to see how one geometry is spatially related to another (useful for hit testing), calculate the areas and lengths, and more.</span></span> <span data-ttu-id="1edfb-170">下表說明常見的幾何作業。</span><span class="sxs-lookup"><span data-stu-id="1edfb-170">The following table describes the common geometric operations.</span></span>



| <span data-ttu-id="1edfb-171">作業</span><span class="sxs-lookup"><span data-stu-id="1edfb-171">Operation</span></span>                                                   | <span data-ttu-id="1edfb-172">方法</span><span class="sxs-lookup"><span data-stu-id="1edfb-172">Method</span></span>                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1edfb-173">合併</span><span class="sxs-lookup"><span data-stu-id="1edfb-173">Combine</span></span>                                                     | [<span data-ttu-id="1edfb-174">**CombineWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="1edfb-174">**CombineWithGeometry**</span></span>](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| <span data-ttu-id="1edfb-175">界限/加寬界限/抓取界限、變更區域更新</span><span class="sxs-lookup"><span data-stu-id="1edfb-175">Bounds/ Widened Bounds/Retrieve Bounds, Dirty Region update</span></span> | <span data-ttu-id="1edfb-176">[**加寬**](id2d1geometry-widen.md)、 [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds)、 [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span><span class="sxs-lookup"><span data-stu-id="1edfb-176">[**Widen**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span></span>                             |
| <span data-ttu-id="1edfb-177">點擊測試</span><span class="sxs-lookup"><span data-stu-id="1edfb-177">Hit Testing</span></span>                                                 | <span data-ttu-id="1edfb-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md)、 [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span><span class="sxs-lookup"><span data-stu-id="1edfb-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span></span>                                             |
| <span data-ttu-id="1edfb-179">筆勢</span><span class="sxs-lookup"><span data-stu-id="1edfb-179">Stroke</span></span>                                                      | [<span data-ttu-id="1edfb-180">**StrokeContainsPoint**</span><span class="sxs-lookup"><span data-stu-id="1edfb-180">**StrokeContainsPoint**</span></span>](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| <span data-ttu-id="1edfb-181">比較</span><span class="sxs-lookup"><span data-stu-id="1edfb-181">Comparison</span></span>                                                  | [<span data-ttu-id="1edfb-182">**CompareWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="1edfb-182">**CompareWithGeometry**</span></span>](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| <span data-ttu-id="1edfb-183">簡化 (移除弧形和二次方貝茲曲線) </span><span class="sxs-lookup"><span data-stu-id="1edfb-183">Simplification (removes arcs and quadratic Bezier curves)</span></span>   | [<span data-ttu-id="1edfb-184">**簡化**</span><span class="sxs-lookup"><span data-stu-id="1edfb-184">**Simplify**</span></span>](id2d1geometry-simplify.md)                                                                                                                                 |
| <span data-ttu-id="1edfb-185">鑲嵌</span><span class="sxs-lookup"><span data-stu-id="1edfb-185">Tessellation</span></span>                                                | [<span data-ttu-id="1edfb-186">**Tessellate**</span><span class="sxs-lookup"><span data-stu-id="1edfb-186">**Tessellate**</span></span>](id2d1geometry-tessellate.md)                                                                                                                             |
| <span data-ttu-id="1edfb-187"> (移除交集) 外框</span><span class="sxs-lookup"><span data-stu-id="1edfb-187">Outline (remove intersection)</span></span>                               | [<span data-ttu-id="1edfb-188">**外框**</span><span class="sxs-lookup"><span data-stu-id="1edfb-188">**Outline**</span></span>](id2d1geometry-outline.md)                                                                                                                                   |
| <span data-ttu-id="1edfb-189">計算幾何的區域或長度</span><span class="sxs-lookup"><span data-stu-id="1edfb-189">Calculate the area or length of a geometry</span></span>                  | <span data-ttu-id="1edfb-190">[**ComputeArea**](id2d1geometry-computearea.md)、 [**ComputeLength**](id2d1geometry-computelength.md)、 [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span><span class="sxs-lookup"><span data-stu-id="1edfb-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span></span> |



 

> [!Note]  
> <span data-ttu-id="1edfb-191">從 Windows 8 開始，您可以在 [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1)上使用 [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description))方法來計算幾何的區域或長度。</span><span class="sxs-lookup"><span data-stu-id="1edfb-191">Starting in Windows 8, you can use the [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) method on the [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) to calculate the area or length of a geometry.</span></span>

 

### <a name="combining-geometries"></a><span data-ttu-id="1edfb-192">結合幾何</span><span class="sxs-lookup"><span data-stu-id="1edfb-192">Combining geometries</span></span>

<span data-ttu-id="1edfb-193">若要將一個幾何與另一個幾何結合，請呼叫 [**ID2D1Geometry：： CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1edfb-193">To combine one geometry with another, call the [**ID2D1Geometry::CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) method.</span></span> <span data-ttu-id="1edfb-194">當您合併幾何時，可以指定下列四種方式之一來執行合併作業： [**D2D1 合併模式聯 \_ \_ \_ 集**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (聯集) 、 [**D2D1 \_ 合併 \_ 模式 \_ 交集**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (交集) 、 [**D2D1 \_ 合併 \_ 模式 \_ XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor) ，以及 [**D2D1 \_ 合併 \_ 模式 \_ 排除**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (排除) 。</span><span class="sxs-lookup"><span data-stu-id="1edfb-194">When you combine the geometries, you specify one of the four ways to perform the combine operation: [**D2D1\_COMBINE\_MODE\_UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (union), [**D2D1\_COMBINE\_MODE\_INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (intersect), [**D2D1\_COMBINE\_MODE\_XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor), and [**D2D1\_COMBINE\_MODE\_EXCLUDE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (exclude).</span></span> <span data-ttu-id="1edfb-195">下列程式碼範例會示範兩個使用聯集合並模式結合的圓形，其中第一個圓形的中心點是 (75、75) 和半徑50的半徑，而第二個圓圈具有 (125、75) 和50半徑的中心點。</span><span class="sxs-lookup"><span data-stu-id="1edfb-195">The following code example shows two circles that are combined by using the union combine mode, where the first circle has the center point of (75, 75) and the radius of 50, and the second circle has the center point of (125, 75) and the radius of 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}


if (SUCCEEDED(hr))
{
    //
    // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
    //
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

    if (SUCCEEDED(hr))
    {
        hr = m_pPathGeometryUnion->Open(&pGeometrySink);

        if (SUCCEEDED(hr))
        {
            hr = m_pCircleGeometry1->CombineWithGeometry(
                m_pCircleGeometry2,
                D2D1_COMBINE_MODE_UNION,
                NULL,
                NULL,
                pGeometrySink
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pGeometrySink->Close();
        }

        SafeRelease(&pGeometrySink);
    }
}
```



<span data-ttu-id="1edfb-196">下圖顯示結合了 union 模式的兩個圓形。</span><span class="sxs-lookup"><span data-stu-id="1edfb-196">The following illustration shows two circles combined with a combine mode of union.</span></span>

![將兩個重迭的圓形合併為聯集的圖例](images/combine-mode-union.png)

<span data-ttu-id="1edfb-198">如需所有合併模式的圖例，請參閱 [**D2D1 \_ 合併 \_ 模式列舉**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)。</span><span class="sxs-lookup"><span data-stu-id="1edfb-198">For illustrations of all the combine modes, see the [**D2D1\_COMBINE\_MODE enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span></span>

### <a name="widen"></a><span data-ttu-id="1edfb-199">擴大</span><span class="sxs-lookup"><span data-stu-id="1edfb-199">Widen</span></span>

<span data-ttu-id="1edfb-200">[**擴大**](id2d1geometry-widen.md)方法會產生新的幾何，其填滿相當於對現有幾何進行筆劃，然後將結果寫入至指定的 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)物件。</span><span class="sxs-lookup"><span data-stu-id="1edfb-200">The [**Widen**](id2d1geometry-widen.md) method generates a new geometry whose fill is equivalent to stroking the existing geometry, and then writes the result to the specified [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) object.</span></span> <span data-ttu-id="1edfb-201">下列程式碼範例會呼叫 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)物件上的 [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) 。</span><span class="sxs-lookup"><span data-stu-id="1edfb-201">The following code example calls [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) on the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object.</span></span> <span data-ttu-id="1edfb-202">如果 **開啟** 成功，它會對 geometry 物件呼叫 **加寬** 。</span><span class="sxs-lookup"><span data-stu-id="1edfb-202">If **Open** succeeds, it calls **Widen** on the geometry object.</span></span>


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a><span data-ttu-id="1edfb-203">Tessellate</span><span class="sxs-lookup"><span data-stu-id="1edfb-203">Tessellate</span></span>

<span data-ttu-id="1edfb-204">[**Tessellate**](id2d1geometry-tessellate.md)方法會建立一組順向纏繞三角形，以在使用指定的矩陣進行轉換之後，以指定的誤差來轉換幾何。</span><span class="sxs-lookup"><span data-stu-id="1edfb-204">The [**Tessellate**](id2d1geometry-tessellate.md) method creates a set of clockwise-wound triangles that cover the geometry after it is transformed by using the specified matrix and flattened by using the specified tolerance.</span></span> <span data-ttu-id="1edfb-205">下列程式碼範例會使用 **Tessellate** 來建立代表 *pPathGeometry* 的三角形清單。</span><span class="sxs-lookup"><span data-stu-id="1edfb-205">The following code example uses **Tessellate** to create a list of triangles that represent *pPathGeometry*.</span></span> <span data-ttu-id="1edfb-206">三角形會儲存在 [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)、 *pMesh*，然後傳送至類別成員 *m \_ pStrokeMesh*，以供稍後轉譯時使用。</span><span class="sxs-lookup"><span data-stu-id="1edfb-206">The triangles are stored in an [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, then transferred to a class member, *m\_pStrokeMesh*, for later use when rendering.</span></span>


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a><span data-ttu-id="1edfb-207">FillContainsPoint 和 StrokeContainsPoint</span><span class="sxs-lookup"><span data-stu-id="1edfb-207">FillContainsPoint and StrokeContainsPoint</span></span>

<span data-ttu-id="1edfb-208">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md)方法會指出幾何所填滿的區域是否包含指定的點。</span><span class="sxs-lookup"><span data-stu-id="1edfb-208">The [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) method indicates whether the area filled by the geometry contains the specified point.</span></span> <span data-ttu-id="1edfb-209">您可以使用這個方法來進行點擊測試。</span><span class="sxs-lookup"><span data-stu-id="1edfb-209">You can use this method to do hit testing.</span></span> <span data-ttu-id="1edfb-210">下列程式碼範例會在 [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)物件上呼叫 **FillContainsPoint** ，並在 (0、0) 和身分 [**識別**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity)矩陣的點傳入點。</span><span class="sxs-lookup"><span data-stu-id="1edfb-210">The following code example calls **FillContainsPoint** on an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) object, passing in a point at (0,0) and an [**Identity**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) matrix.</span></span>


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



<span data-ttu-id="1edfb-211">[**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)方法會判斷幾何的筆劃是否包含指定的點。</span><span class="sxs-lookup"><span data-stu-id="1edfb-211">The [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) method determines whether the geometry's stroke contains the specified point.</span></span> <span data-ttu-id="1edfb-212">您可以使用這個方法來進行點擊測試。</span><span class="sxs-lookup"><span data-stu-id="1edfb-212">You can use this method to do hit testing.</span></span> <span data-ttu-id="1edfb-213">下列程式碼範例會使用 **StrokeContainsPoint**。</span><span class="sxs-lookup"><span data-stu-id="1edfb-213">The following code example uses **StrokeContainsPoint**.</span></span>


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a><span data-ttu-id="1edfb-214">簡化 </span><span class="sxs-lookup"><span data-stu-id="1edfb-214">Simplify</span></span>

<span data-ttu-id="1edfb-215">[**簡化**](id2d1geometry-simplify.md)方法會從指定的幾何中移除弧形和二次方貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="1edfb-215">The [**Simplify**](id2d1geometry-simplify.md) method removes arcs and quadratic Bezier curves from a specified geometry.</span></span> <span data-ttu-id="1edfb-216">因此，產生的幾何只會包含線條和（選擇性）三次方貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="1edfb-216">So, the resulting geometry contains only lines and, optionally, cubic Bezier curves.</span></span> <span data-ttu-id="1edfb-217">下列程式碼範例使用 **簡化** ，將具有貝茲曲線的幾何轉換成隻包含線段的幾何。</span><span class="sxs-lookup"><span data-stu-id="1edfb-217">The following code example uses **Simplify** to transform a geometry with Bezier curves into a geometry that contains only line segments.</span></span>


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a><span data-ttu-id="1edfb-218">ComputeLength 和 ComputeArea</span><span class="sxs-lookup"><span data-stu-id="1edfb-218">ComputeLength and ComputeArea</span></span>

<span data-ttu-id="1edfb-219">如果每個區段都展開成一行， [**ComputeLength**](id2d1geometry-computelength.md) 方法就會計算指定之幾何的長度。</span><span class="sxs-lookup"><span data-stu-id="1edfb-219">The [**ComputeLength**](id2d1geometry-computelength.md) method calculates the length of the specified geometry if each segment were unrolled into a line.</span></span> <span data-ttu-id="1edfb-220">這包括當幾何關閉時的隱含結尾區段。</span><span class="sxs-lookup"><span data-stu-id="1edfb-220">This includes the implicit closing segment if the geometry is closed.</span></span> <span data-ttu-id="1edfb-221">下列程式碼範例會使用 **ComputeLength** 來計算指定之圓形 (**m \_ pCircleGeometry1**) 的長度。</span><span class="sxs-lookup"><span data-stu-id="1edfb-221">The following code example uses **ComputeLength** to compute the length of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



<span data-ttu-id="1edfb-222">[**ComputeArea**](id2d1geometry-computearea.md)方法會計算指定幾何的區域。</span><span class="sxs-lookup"><span data-stu-id="1edfb-222">The [**ComputeArea**](id2d1geometry-computearea.md) method calculates the area of the specified geometry.</span></span> <span data-ttu-id="1edfb-223">下列程式碼範例會使用 **ComputeArea** 來計算指定之圓形的區域 (**m \_ pCircleGeometry1**) 。</span><span class="sxs-lookup"><span data-stu-id="1edfb-223">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a><span data-ttu-id="1edfb-224">CompareWithGeometry</span><span class="sxs-lookup"><span data-stu-id="1edfb-224">CompareWithGeometry</span></span>

<span data-ttu-id="1edfb-225">[**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md)方法會描述呼叫這個方法的幾何和指定幾何之間的交集。</span><span class="sxs-lookup"><span data-stu-id="1edfb-225">The [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) method describes the intersection between the geometry that calls this method and the specified geometry.</span></span> <span data-ttu-id="1edfb-226">交集的可能值包括 [**D2D1 \_ 幾何 \_ 關聯 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) 性 (不連續的) 、 **D2D1 GEOMETRY (\_ \_ 關聯 \_ \_** 包含) 、 **D2D1 \_ geometry \_ 關聯 \_ 包含** (包含) ，以及 **D2D1 \_ 幾何 \_ 關聯 \_** (重迭) 重迭。</span><span class="sxs-lookup"><span data-stu-id="1edfb-226">The possible values for intersection include [**D2D1\_GEOMETRY\_RELATION\_DISJOINT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disjoint), **D2D1\_GEOMETRY\_RELATION\_IS\_CONTAINED** (is contained), **D2D1\_GEOMETRY\_RELATION\_CONTAINS** (contains), and **D2D1\_GEOMETRY\_RELATION\_OVERLAP** (overlap).</span></span> <span data-ttu-id="1edfb-227">「無交集」表示兩個幾何填滿完全不相交。</span><span class="sxs-lookup"><span data-stu-id="1edfb-227">"disjoint" means that two geometry fills do not intersect at all.</span></span> <span data-ttu-id="1edfb-228">「包含」表示幾何完全由指定的幾何所包含。</span><span class="sxs-lookup"><span data-stu-id="1edfb-228">"is contained" means that the geometry is completely contained by the specified geometry.</span></span> <span data-ttu-id="1edfb-229">「contains」表示幾何完全包含指定的幾何，而「重迭」表示兩個幾何重迭，但不完全包含另一個。</span><span class="sxs-lookup"><span data-stu-id="1edfb-229">"contains" means that the geometry completely contains the specified geometry, and "overlap" means the two geometries overlap but neither completely contains the other.</span></span>

<span data-ttu-id="1edfb-230">下列程式碼範例顯示如何比較兩個半徑為50但位移為50的圓形。</span><span class="sxs-lookup"><span data-stu-id="1edfb-230">The following code example shows how to compare two circles that have the same radius of 50 but are offset by 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a><span data-ttu-id="1edfb-231">外框</span><span class="sxs-lookup"><span data-stu-id="1edfb-231">Outline</span></span>

<span data-ttu-id="1edfb-232">[ [**外框**](id2d1geometry-outline.md) ] 方法會計算幾何的輪廓 (某個幾何的版本，其中沒有任何圖與本身或任何其他圖表) ，並將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)。</span><span class="sxs-lookup"><span data-stu-id="1edfb-232">The [**Outline**](id2d1geometry-outline.md) method computes the outline of the geometry (a version of the geometry in which no figure crosses itself or any other figure) and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="1edfb-233">下列程式碼範例使用 **大綱** 來建立不具任何自我交集的相等幾何。</span><span class="sxs-lookup"><span data-stu-id="1edfb-233">The following code example uses **Outline** to construct an equivalent geometry without any self-intersections.</span></span> <span data-ttu-id="1edfb-234">它會使用預設的簡維容錯。</span><span class="sxs-lookup"><span data-stu-id="1edfb-234">It uses the default flattening tolerance.</span></span>


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a><span data-ttu-id="1edfb-235">GetBounds 和 GetWidenedBounds</span><span class="sxs-lookup"><span data-stu-id="1edfb-235">GetBounds and GetWidenedBounds</span></span>

<span data-ttu-id="1edfb-236">[**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds)方法會捕獲幾何的界限。</span><span class="sxs-lookup"><span data-stu-id="1edfb-236">The [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) method retrieves the bounds of the geometry.</span></span> <span data-ttu-id="1edfb-237">下列程式碼範例會使用 **GetBounds** 來取出指定之圓形 (**m \_ pCircleGeometry1**) 的界限。</span><span class="sxs-lookup"><span data-stu-id="1edfb-237">The following code example uses **GetBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



<span data-ttu-id="1edfb-238">[**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)方法會在指定的筆觸寬度和樣式（由指定的矩陣轉換）加寬之後，抓取幾何的範圍。</span><span class="sxs-lookup"><span data-stu-id="1edfb-238">The [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) method retrieves the bounds of the geometry after it is widened by the specified stroke width and style and transformed by the specified matrix.</span></span> <span data-ttu-id="1edfb-239">下列程式碼範例會使用 **GetWidenedBounds** 來抓取指定之圓形的範圍 (**m \_ pCircleGeometry1**) 在以指定的筆觸寬度加寬之後。</span><span class="sxs-lookup"><span data-stu-id="1edfb-239">The following code example uses **GetWidenedBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**) after it is widened by the specified stroke width.</span></span>


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a><span data-ttu-id="1edfb-240">ComputePointAtLength</span><span class="sxs-lookup"><span data-stu-id="1edfb-240">ComputePointAtLength</span></span>

<span data-ttu-id="1edfb-241">[**ComputePointAtLength**](id2d1geometry-computepointatlength.md)方法會在幾何的指定距離計算點和正切向量。</span><span class="sxs-lookup"><span data-stu-id="1edfb-241">The [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) method calculates the point and tangent vector at the specified distance along the geometry.</span></span> <span data-ttu-id="1edfb-242">下列程式碼範例會使用 **ComputePointAtLength**。</span><span class="sxs-lookup"><span data-stu-id="1edfb-242">The following code example uses **ComputePointAtLength**.</span></span>


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a><span data-ttu-id="1edfb-243">相關主題</span><span class="sxs-lookup"><span data-stu-id="1edfb-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1edfb-244">路徑幾何總覽</span><span class="sxs-lookup"><span data-stu-id="1edfb-244">Path Geometries Overview</span></span>](path-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="1edfb-245">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="1edfb-245">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 