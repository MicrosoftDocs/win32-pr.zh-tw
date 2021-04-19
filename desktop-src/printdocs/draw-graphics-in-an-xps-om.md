---
description: 此頁面說明如何在 XPS OM 中繪製圖形。
ms.assetid: 2384b522-208a-48db-ae0d-f82fa0214d09
title: 在 XPS OM 中繪製圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabbf8cfb821c80dfff43e2e7844331c8920f726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989384"
---
# <a name="draw-graphics-in-an-xps-om"></a><span data-ttu-id="2195f-103">在 XPS OM 中繪製圖形</span><span class="sxs-lookup"><span data-stu-id="2195f-103">Draw Graphics in an XPS OM</span></span>

<span data-ttu-id="2195f-104">此頁面說明如何在 XPS OM 中繪製圖形。</span><span class="sxs-lookup"><span data-stu-id="2195f-104">This page describes how to draw graphics in an XPS OM.</span></span>

<span data-ttu-id="2195f-105">若要在頁面中繪製以向量為基礎的圖形，請將 [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) 介面具現化，並在其中填入所需的內容，並將它加入至頁面的視覺物件清單或畫布。</span><span class="sxs-lookup"><span data-stu-id="2195f-105">To draw vector-based graphics in a page, instantiate an [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface, populate it with the desired content, and add it to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="2195f-106">**IXpsOMPath** 介面包含以向量為基礎之圖形的屬性，例如大綱、填滿色彩、線條樣式和線條色彩。</span><span class="sxs-lookup"><span data-stu-id="2195f-106">An **IXpsOMPath** interface contains such properties of a vector-based shape as the outline, fill color, line style, and line color.</span></span> <span data-ttu-id="2195f-107">路徑的圖形是由 [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) 介面所指定，其中包含 [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) 介面的集合，以及選擇性的 [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) 介面。</span><span class="sxs-lookup"><span data-stu-id="2195f-107">The path's shape is specified by an [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface, which contains a collection of [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interfaces and, optionally, an [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) interface.</span></span> <span data-ttu-id="2195f-108">您可以使用任何繼承自 [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) 介面的介面來填滿路徑的周邊，以及路徑所描述之圖形的內部。</span><span class="sxs-lookup"><span data-stu-id="2195f-108">You can use any interface that inherits from the [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) interface to fill the perimeter of the path and the interior of the shape that is described by the path.</span></span>

<span data-ttu-id="2195f-109">在您的程式中使用下列程式碼範例之前，請閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="2195f-109">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="2195f-110">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="2195f-110">Code Example</span></span>

<span data-ttu-id="2195f-111">下列程式碼範例會建立簡單的路徑，以描述以單一色彩填滿的矩形。</span><span class="sxs-lookup"><span data-stu-id="2195f-111">The following code example creates a simple path that describes a rectangle that is filled with a single color.</span></span>

### <a name="create-the-stroke-and-the-fill-brushes"></a><span data-ttu-id="2195f-112">建立筆觸和填滿筆刷</span><span class="sxs-lookup"><span data-stu-id="2195f-112">Create the stroke and the fill brushes</span></span>

<span data-ttu-id="2195f-113">程式碼範例的第一個區段會建立將用來填滿路徑物件的 [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) 。</span><span class="sxs-lookup"><span data-stu-id="2195f-113">The first section of the code example creates the [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) that will be used to fill the path object.</span></span>


```C++
    HRESULT               hr = S_OK;

    XPS_COLOR             xpsColor;
    IXpsOMSolidColorBrush *xpsFillBrush = NULL;
    IXpsOMSolidColorBrush *xpsStrokeBrush = NULL;

    // Set the fill brush color to RED.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColor,
        NULL,          // color profile resource
        &xpsFillBrush);
    // The color profile resource parameter is NULL because
    //  this color type does not use a color profile resource.

    // Set the stroke brush color to BLACK.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0x00;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
            &xpsColor,
            NULL, // This color type does not use a color profile resource.
            &xpsStrokeBrush);

    // The brushes are released below after they have been used.
```



### <a name="define-the-shape"></a><span data-ttu-id="2195f-114">定義圖形</span><span class="sxs-lookup"><span data-stu-id="2195f-114">Define the shape</span></span>

<span data-ttu-id="2195f-115">程式碼範例的第二個區段會建立 [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) 介面。</span><span class="sxs-lookup"><span data-stu-id="2195f-115">The second section of the code example creates the [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface.</span></span> <span data-ttu-id="2195f-116">然後，它會建立 [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) 介面，以指定圖表的形狀，並將圖表加入 **IXpsOMGeometry** 介面。</span><span class="sxs-lookup"><span data-stu-id="2195f-116">It then creates the [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interface that specifies the figure's shape, and adds the figure to the **IXpsOMGeometry** interface.</span></span> <span data-ttu-id="2195f-117">此範例會 *建立矩形所* 指定的矩形。</span><span class="sxs-lookup"><span data-stu-id="2195f-117">The example creates a rectangle that is specified by *rect*.</span></span> <span data-ttu-id="2195f-118">區段只能針對矩形的四個邊定義。</span><span class="sxs-lookup"><span data-stu-id="2195f-118">Segments must be defined for only three of the four sides of the rectangle.</span></span> <span data-ttu-id="2195f-119">圖形的周邊（在此案例中為矩形）會從起點開始，並依幾何圖區段的定義進行擴充。</span><span class="sxs-lookup"><span data-stu-id="2195f-119">The perimeter of the shape, the rectangle in this case, starts from the start point and extends as defined by the segments of the geometry figure.</span></span> <span data-ttu-id="2195f-120">將 [ **IsClosed** ] 屬性設定為 [ **TRUE** ]，就會藉由新增一個將最後一個區段結尾連接到起點的額外區段，來指出矩形已關閉。</span><span class="sxs-lookup"><span data-stu-id="2195f-120">Setting the **IsClosed** property to **TRUE** indicates that the rectangle is closed by adding one additional segment that connects the end of the last segment to the start point.</span></span>


```C++
    // rect is initialized outside of the sample and 
    //  contains the coordinates of the rectangular geometry to create.
    XPS_RECT                            rect = {0,0,100,100};       

    HRESULT                             hr = S_OK;
    IXpsOMGeometryFigure                *rectFigure;
    IXpsOMGeometry                      *imageRectGeometry;
    IXpsOMGeometryFigureCollection      *geomFigureCollection;

    // Define the start point and create an empty figure.
    XPS_POINT                           startPoint = {rect.x, rect.y};
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    // Define the segments of the geometry figure.
    //  First, define the type of each segment.
    XPS_SEGMENT_TYPE segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE,  // each segment is a straight line
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // Define the x and y coordinates of each corner of the figure
    //  the start point has already been defined so only the 
    //  remaining three corners need to be defined.
    FLOAT segmentData[6] = {
        rect.x,                (rect.y + rect.height),
        (rect.x + rect.width), (rect.y + rect.height), 
        (rect.x + rect.width), rect.y 
    };

    // Describe if the segments are stroked (that is if the segment lines
    //  should be drawn as a line).
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE // Yes, draw each of the segment lines.
    };

    // Add the segment data to the figure.
    hr = rectFigure->SetSegments(
                        3, 
                        6, 
                        segmentTypes, 
                        segmentData, 
                        segmentStrokes);

    // Set the closed and filled properties of the figure.
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
 
    // Create the geometry object.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    
    // Get a pointer to the figure collection interface of the geometry...
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );

    // ...and then add the figure created above to this geometry.
    hr = geomFigureCollection->Append( rectFigure );
    // If not needed for anything else, release the rectangle figure.
    rectFigure->Release();

    // when done adding figures, release the figure collection. 
    geomFigureCollection->Release();

    //  When done with the geometry object, release the object.
    // imageRectGeometry->Release();
    //  In this case, imageRectGeometry is used in the next sample
    //  so the geometry object is not released, yet.
    
```



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a><span data-ttu-id="2195f-121">建立路徑，並將其新增至視覺效果集合</span><span class="sxs-lookup"><span data-stu-id="2195f-121">Create the path and add it to the visual collection</span></span>

<span data-ttu-id="2195f-122">這個程式碼範例的最後一個區段會建立並設定 path 物件，然後將它加入至頁面的視覺物件清單。</span><span class="sxs-lookup"><span data-stu-id="2195f-122">The final section of this code example creates and configures the path object, then adds it to the page's list of visual objects.</span></span>


```C++
    HRESULT                    hr = S_OK;
    // The page interface pointer is initialized outside of this sample.
    IXpsOMPath                *rectPath = NULL;
    IXpsOMVisualCollection    *pageVisuals = NULL;

    // Create the new path object.
    hr = xpsFactory->CreatePath( &rectPath );

    // Add the geometry to the path.
    //  imageRectGeometry is initialized outside of this example.
    hr = rectPath->SetGeometryLocal( imageRectGeometry );

    // Set the short description of the path to provide
    //  a textual description of the object for accessibility.
    hr = rectPath->SetAccessibilityShortDescription( L"Red Rectangle" );
    
    // Set the fill and stroke brushes to use the brushes 
    //  created in the first section.
    hr = rectPath->SetFillBrushLocal( xpsFillBrush );
    hr = rectPath->SetStrokeBrushLocal( xpsStrokeBrush);

    // Get the visual collection of this page and add this path to it.
    hr = xpsPage->GetVisuals( &pageVisuals );
    hr = pageVisuals->Append( rectPath );
    // If not needed for anything else, release the rectangle path.
    rectPath->Release();
    
    // When done with the visual collection, release it.
    pageVisuals->Release();

    // When finished with the brushes, release the interface pointers.
    if (NULL != xpsFillBrush) xpsFillBrush->Release();
    if (NULL != xpsStrokeBrush) xpsStrokeBrush->Release();

    // When done with the geometry interface, release it.
    imageRectGeometry->Release();

    // When done with the path interface, release it.
    rectPath->Release();

```



## <a name="best-practices"></a><span data-ttu-id="2195f-123">最佳做法</span><span class="sxs-lookup"><span data-stu-id="2195f-123">Best Practices</span></span>

<span data-ttu-id="2195f-124">加入 [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) 介面所指定之圖形的文字描述。</span><span class="sxs-lookup"><span data-stu-id="2195f-124">Add a textual description of the shape that is specified by the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface.</span></span> <span data-ttu-id="2195f-125">為了讓視力受損的使用者受益，請使用 [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) 和 [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) 方法提供協助工具支援功能的文字內容，例如螢幕閱讀程式。</span><span class="sxs-lookup"><span data-stu-id="2195f-125">For the benefit of visually impaired users, use the [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) and [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) methods to provide textual content for accessibility support features, such as screen readers.</span></span>

## <a name="additional-information"></a><span data-ttu-id="2195f-126">其他資訊</span><span class="sxs-lookup"><span data-stu-id="2195f-126">Additional Information</span></span>

<span data-ttu-id="2195f-127">此頁面上的程式碼範例會使用 [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) 介面做為路徑的填滿筆刷和筆觸筆刷。</span><span class="sxs-lookup"><span data-stu-id="2195f-127">The code example on this page uses an [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) interface as the fill brush and stroke brush for the path.</span></span> <span data-ttu-id="2195f-128">除了 **IXpsOMSolidColorBrush** 介面外，您還可以使用 [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)、 [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)或 [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) 介面。</span><span class="sxs-lookup"><span data-stu-id="2195f-128">In addition to the **IXpsOMSolidColorBrush** interface, you can use an [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush), or [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) interface.</span></span>

<span data-ttu-id="2195f-129">筆劃是可在圖形周邊周圍繪製的線條。</span><span class="sxs-lookup"><span data-stu-id="2195f-129">The stroke is the line that can be drawn around the perimeter of the figure.</span></span> <span data-ttu-id="2195f-130">[XML 檔規格](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)支援許多不同的筆觸線樣式。</span><span class="sxs-lookup"><span data-stu-id="2195f-130">The [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) supports many different stroke line styles.</span></span> <span data-ttu-id="2195f-131">若要指定筆觸線樣式，請使用 [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) 介面的下列方法來設定筆觸屬性：</span><span class="sxs-lookup"><span data-stu-id="2195f-131">To specify the stroke line style, set the stroke properties with the following methods of the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface:</span></span>

-   <span data-ttu-id="2195f-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) 或 [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) ，以設定筆劃筆刷</span><span class="sxs-lookup"><span data-stu-id="2195f-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) or [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) to set the stroke brush</span></span>
-   <span data-ttu-id="2195f-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) 以取得描述筆觸的筆觸虛線集合</span><span class="sxs-lookup"><span data-stu-id="2195f-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) to get the stroke dash collection that describes the strokes</span></span>
-   <span data-ttu-id="2195f-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) 至和 [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) 來描述虛線筆觸的外觀</span><span class="sxs-lookup"><span data-stu-id="2195f-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) to and [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) to describe the appearance of a dashed stroke</span></span>
-   <span data-ttu-id="2195f-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) 和 [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) 定義線條終止樣式</span><span class="sxs-lookup"><span data-stu-id="2195f-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) and [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) to define the line termination style</span></span>
-   <span data-ttu-id="2195f-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) 和 [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) 描述區段的聯結方式</span><span class="sxs-lookup"><span data-stu-id="2195f-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) and [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) to describe how the segments are joined</span></span>
-   <span data-ttu-id="2195f-137">設定筆觸粗細的 [**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness)</span><span class="sxs-lookup"><span data-stu-id="2195f-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) to set the stroke thickness</span></span>

## <a name="related-topics"></a><span data-ttu-id="2195f-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="2195f-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2195f-139">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="2195f-139">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="2195f-140">流覽 XPS OM</span><span class="sxs-lookup"><span data-stu-id="2195f-140">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="2195f-141">將文字寫入至 XPS OM</span><span class="sxs-lookup"><span data-stu-id="2195f-141">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="2195f-142">以 XPS OM 放置影像</span><span class="sxs-lookup"><span data-stu-id="2195f-142">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="2195f-143">將 XPS OM 寫入 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="2195f-143">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="2195f-144">列印 XPS OM</span><span class="sxs-lookup"><span data-stu-id="2195f-144">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="2195f-145">**用於此頁面**</span><span class="sxs-lookup"><span data-stu-id="2195f-145">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="2195f-146">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="2195f-146">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="2195f-147">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="2195f-147">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="2195f-148">**IXpsOMGeometryFigure**</span><span class="sxs-lookup"><span data-stu-id="2195f-148">**IXpsOMGeometryFigure**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="2195f-149">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="2195f-149">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[<span data-ttu-id="2195f-150">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="2195f-150">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="2195f-151">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="2195f-151">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="2195f-152">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="2195f-152">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[<span data-ttu-id="2195f-153">**IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="2195f-153">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="2195f-154">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="2195f-154">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="2195f-155">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="2195f-155">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="2195f-156">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="2195f-156">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="2195f-157">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="2195f-157">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="2195f-158">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="2195f-158">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
