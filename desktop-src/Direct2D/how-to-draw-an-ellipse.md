---
title: 如何繪製和填滿基本圖形
description: 本主題說明如何繪製基本圖形。
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 93d8f3a3ddeb06c9168971789dff3ac8c9222d22
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826997"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a><span data-ttu-id="3c064-103">如何繪製和填滿基本圖形</span><span class="sxs-lookup"><span data-stu-id="3c064-103">How to Draw and Fill a Basic Shape</span></span>

<span data-ttu-id="3c064-104">本主題說明如何繪製基本圖形。</span><span class="sxs-lookup"><span data-stu-id="3c064-104">This topic describes how to draw a basic shape.</span></span> <span data-ttu-id="3c064-105">[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)介面提供了用來大綱和填滿省略號、矩形和線條的方法。</span><span class="sxs-lookup"><span data-stu-id="3c064-105">The [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface provides methods for outlining and filling ellipses, rectangles, and lines.</span></span> <span data-ttu-id="3c064-106">下列範例示範如何建立和繪製橢圓形。</span><span class="sxs-lookup"><span data-stu-id="3c064-106">The following examples show how to create and draw an ellipse.</span></span>

<span data-ttu-id="3c064-107">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="3c064-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3c064-108">以實心筆觸繪製橢圓形的外框</span><span class="sxs-lookup"><span data-stu-id="3c064-108">Draw the Outline of an Ellipse with a Solid Stroke</span></span>](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [<span data-ttu-id="3c064-109">使用虛線筆觸繪製橢圓形</span><span class="sxs-lookup"><span data-stu-id="3c064-109">Draw an Ellipse with a Dashed Stroke</span></span>](#draw-an-ellipse-with-a-dashed-stroke)
-   [<span data-ttu-id="3c064-110">繪製和填滿橢圓形</span><span class="sxs-lookup"><span data-stu-id="3c064-110">Draw and Fill an Ellipse</span></span>](#draw-and-fill-an-ellipse)
-   [<span data-ttu-id="3c064-111">繪製更複雜的圖形</span><span class="sxs-lookup"><span data-stu-id="3c064-111">Drawing More Complex Shapes</span></span>](#drawing-more-complex-shapes)
-   [<span data-ttu-id="3c064-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c064-112">Related topics</span></span>](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a><span data-ttu-id="3c064-113">以實心筆觸繪製橢圓形的外框</span><span class="sxs-lookup"><span data-stu-id="3c064-113">Draw the Outline of an Ellipse with a Solid Stroke</span></span>

<span data-ttu-id="3c064-114">若要繪製橢圓形的輪廓，您可以定義筆刷 (例如 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 或 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) 來繪製外框，並使用 [**D2D1 \_ 橢圓形**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) 來描述橢圓形的位置和維度，然後將這些物件傳遞給 [**ID2D1RenderTarget：:D rawellipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c064-114">To draw the outline of an ellipse, you define a brush (such as a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) for painting the outline and a [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) for describing the ellipse's position and dimensions, then pass these objects to the [**ID2D1RenderTarget::DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="3c064-115">下列範例會建立黑色純色筆刷，並將其儲存在 m \_ spBlackBrush 類別成員中。</span><span class="sxs-lookup"><span data-stu-id="3c064-115">The following example creates a black solid color brush and stores it in the m\_spBlackBrush class member.</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



<span data-ttu-id="3c064-116">下一個範例會定義 [**D2D1 \_ 橢圓形**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) ，並使用它與前一個範例中定義的筆刷來繪製橢圓形的輪廓。</span><span class="sxs-lookup"><span data-stu-id="3c064-116">The next example defines an [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) and uses it with the brush defined in the previous example to draw the outline of an ellipse.</span></span> <span data-ttu-id="3c064-117">此範例會產生下圖所示的輸出。</span><span class="sxs-lookup"><span data-stu-id="3c064-117">This example produces the output shown in the following illustration.</span></span>

![具有實心筆觸的橢圓形圖例](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a><span data-ttu-id="3c064-119">使用虛線筆觸繪製橢圓形</span><span class="sxs-lookup"><span data-stu-id="3c064-119">Draw an Ellipse with a Dashed Stroke</span></span>

<span data-ttu-id="3c064-120">上述範例使用了純筆劃。</span><span class="sxs-lookup"><span data-stu-id="3c064-120">The preceding example used a plain stroke.</span></span> <span data-ttu-id="3c064-121">您可以藉由建立 [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)，以數種方式修改筆劃的外觀。</span><span class="sxs-lookup"><span data-stu-id="3c064-121">You can modify the look of a stroke in several ways by creating an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span></span> <span data-ttu-id="3c064-122">**ID2D1StrokeStyle** 可讓您在筆劃的開頭和結尾指定圖形（不論是否有虛線模式），依此類推。</span><span class="sxs-lookup"><span data-stu-id="3c064-122">The **ID2D1StrokeStyle** lets you specify the shape at the beginning and end of a stroke, whether it has a dash pattern, and so on.</span></span> <span data-ttu-id="3c064-123">下列範例會建立描述虛線筆劃的 **ID2D1StrokeStyle** 。</span><span class="sxs-lookup"><span data-stu-id="3c064-123">The following example creates an **ID2D1StrokeStyle** that describes a dashed stroke.</span></span> <span data-ttu-id="3c064-124">這個範例會使用預先定義的虛線模式 [**D2D1 \_ 虛線 \_ 樣式 \_ 虛線 \_ 點 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)，但是您也可以指定自己的虛線樣式。</span><span class="sxs-lookup"><span data-stu-id="3c064-124">This example uses a predefined dash pattern, [**D2D1\_DASH\_STYLE\_DASH\_DOT\_DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), but you can also specify your own.</span></span>


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



<span data-ttu-id="3c064-125">下一個範例會使用筆觸樣式搭配 [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c064-125">The next example uses the stroke style with the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="3c064-126">此範例會產生下圖所示的輸出。</span><span class="sxs-lookup"><span data-stu-id="3c064-126">This example produces the output shown in the following illustration.</span></span>

![具有虛線筆觸的橢圓形圖例](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a><span data-ttu-id="3c064-128">繪製和填滿橢圓形</span><span class="sxs-lookup"><span data-stu-id="3c064-128">Draw and Fill an Ellipse</span></span>

<span data-ttu-id="3c064-129">若要繪製橢圓形的內部，請使用 [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c064-129">To paint the interior of an ellipse, you use the [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method.</span></span> <span data-ttu-id="3c064-130">下列範例會使用 [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) 方法來勾勒出橢圓形，然後使用 **FillEllipse** 方法來繪製其內部。</span><span class="sxs-lookup"><span data-stu-id="3c064-130">The following example uses the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method to outline the ellipse, then uses the **FillEllipse** method to paint its interior.</span></span> <span data-ttu-id="3c064-131">此範例會產生下圖所示的輸出。</span><span class="sxs-lookup"><span data-stu-id="3c064-131">This example produces the output shown in the following illustration.</span></span>

![橢圓形的圖例，其中含有虛線筆觸，然後以純灰色色彩填滿](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



<span data-ttu-id="3c064-133">下一個範例會先填滿橢圓形，然後繪製其輪廓。</span><span class="sxs-lookup"><span data-stu-id="3c064-133">The next example fills the ellipse first, then draws its outline.</span></span> <span data-ttu-id="3c064-134">此範例會產生下圖所示的輸出。</span><span class="sxs-lookup"><span data-stu-id="3c064-134">This example produces the output shown in the following illustration.</span></span>

![以純色筆觸填滿的橢圓形圖例，然後以虛線筆觸表示](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



<span data-ttu-id="3c064-136">這些範例中已省略程式碼。</span><span class="sxs-lookup"><span data-stu-id="3c064-136">Code has been omitted from these examples.</span></span>

## <a name="drawing-more-complex-shapes"></a><span data-ttu-id="3c064-137">繪製更複雜的圖形</span><span class="sxs-lookup"><span data-stu-id="3c064-137">Drawing More Complex Shapes</span></span>

<span data-ttu-id="3c064-138">若要繪製更複雜的圖形，您可以定義 ID2D1Geometry 物件，並使用這些物件搭配 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 和 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c064-138">To draw more complex shapes, you define ID2D1Geometry objects and use them with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods.</span></span> <span data-ttu-id="3c064-139">如需詳細資訊，請參閱 [幾何總覽](direct2d-geometries-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="3c064-139">For more information, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c064-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c064-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c064-141">幾何概觀</span><span class="sxs-lookup"><span data-stu-id="3c064-141">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="3c064-142">筆刷概觀</span><span class="sxs-lookup"><span data-stu-id="3c064-142">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

 

 
