---
title: 不透明度遮罩概觀
description: 本主題說明如何使用點陣圖和筆刷來定義不透明度遮罩。 包含以下幾節。
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a4757a30247da465e0ae5226bd923219e3e665
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104556222"
---
# <a name="opacity-masks-overview"></a><span data-ttu-id="98866-104">不透明度遮罩概觀</span><span class="sxs-lookup"><span data-stu-id="98866-104">Opacity Masks Overview</span></span>

<span data-ttu-id="98866-105">本主題說明如何使用點陣圖和筆刷來定義不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-105">This topic describes how to use bitmaps and brushes to define opacity masks.</span></span> <span data-ttu-id="98866-106">包含以下幾節。</span><span class="sxs-lookup"><span data-stu-id="98866-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="98866-107">先決條件</span><span class="sxs-lookup"><span data-stu-id="98866-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="98866-108">什麼是不透明度遮罩？</span><span class="sxs-lookup"><span data-stu-id="98866-108">What Is an Opacity Mask?</span></span>](#what-is-an-opacity-mask)
-   [<span data-ttu-id="98866-109">使用點陣圖作為 FillOpacityMask 方法的不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="98866-109">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [<span data-ttu-id="98866-110">使用 FillGeometry 方法將筆刷作為不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="98866-110">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [<span data-ttu-id="98866-111">使用線性漸層筆刷做為不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="98866-111">Use an Linear Gradient Brush as an Opacity Mask</span></span>](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [<span data-ttu-id="98866-112">使用放射狀漸層筆刷做為不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="98866-112">Use a Radial Gradient Brush as an Opacity Mask</span></span>](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [<span data-ttu-id="98866-113">將不透明度遮罩套用至圖層</span><span class="sxs-lookup"><span data-stu-id="98866-113">Apply an Opacity Mask to a Layer</span></span>](#apply-an-opacity-mask-to-a-layer)
-   [<span data-ttu-id="98866-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="98866-114">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="98866-115">必要條件</span><span class="sxs-lookup"><span data-stu-id="98866-115">Prerequisites</span></span>

<span data-ttu-id="98866-116">本總覽假設您已經熟悉基本的 Direct2D 繪圖作業，如 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md) 逐步解說中所述。</span><span class="sxs-lookup"><span data-stu-id="98866-116">This overview assumes that you are familiar with basic Direct2D drawing operations, as described in the [Creating a Simple Direct2D Application](direct2d-quickstart.md) walkthrough.</span></span> <span data-ttu-id="98866-117">您也應該熟悉不同類型的筆刷，如 [筆刷總覽](direct2d-brushes-overview.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="98866-117">You should also be familiar with the different types of brushes, as described in the [Brushes Overview](direct2d-brushes-overview.md).</span></span>

## <a name="what-is-an-opacity-mask"></a><span data-ttu-id="98866-118">什麼是不透明度遮罩？</span><span class="sxs-lookup"><span data-stu-id="98866-118">What Is an Opacity Mask?</span></span>

<span data-ttu-id="98866-119">不透明度遮罩是由筆刷或點陣圖描述的遮罩，會套用到另一個物件，使該物件部分或完全透明。</span><span class="sxs-lookup"><span data-stu-id="98866-119">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="98866-120">不透明度遮罩會使用 Alpha 色板資訊來指定如何將物件的來源圖元混合到最後的目的地目標。</span><span class="sxs-lookup"><span data-stu-id="98866-120">An opacity mask uses alpha channel information to specify how the source pixels of the object are blended into the final destination target.</span></span> <span data-ttu-id="98866-121">遮罩的透明部分表示隱藏基礎影像的區域，而遮罩的不透明部分則會指出遮罩物件的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="98866-121">The transparent portions of the mask indicate the areas where the underlying image is hidden, whereas the opaque portions of the mask indicate where the masked object is visible.</span></span>

<span data-ttu-id="98866-122">有幾種方式可以套用不透明度遮罩：</span><span class="sxs-lookup"><span data-stu-id="98866-122">There are several ways to apply an opacity mask:</span></span>

-   <span data-ttu-id="98866-123">使用 [**ID2D1RenderTarget：： FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="98866-123">Use the [**ID2D1RenderTarget::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method.</span></span> <span data-ttu-id="98866-124">**FillOpacityMask** 方法會繪製呈現目標的矩形區域，然後套用由點陣圖定義的不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-124">The **FillOpacityMask** method paints a rectangular region of a render target and then applies an opacity mask, defined by a bitmap.</span></span> <span data-ttu-id="98866-125">當您的不透明度遮罩為點陣圖，而您想要填滿矩形區域時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="98866-125">Use this method when your opacity mask is a bitmap and you want to fill a rectangular region.</span></span>
-   <span data-ttu-id="98866-126">使用 [**ID2D1RenderTarget：： FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法。</span><span class="sxs-lookup"><span data-stu-id="98866-126">Use the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="98866-127">**FillGeometry** 方法會使用指定的 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)繪製幾何的內部，然後套用由筆刷定義的不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-127">The **FillGeometry** method paints the interior of geometry with the specified [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), then applies an opacity mask, defined by a brush.</span></span> <span data-ttu-id="98866-128">當您想要將不透明度遮罩套用至幾何，或想要使用筆刷做為不透明度遮罩時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="98866-128">Use this method when you want to apply an opacity mask to a geometry or you want to use a brush as an opacity mask.</span></span>
-   <span data-ttu-id="98866-129">使用 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 來套用不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-129">Use an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) to apply an opacity mask.</span></span> <span data-ttu-id="98866-130">當您想要將不透明度遮罩套用至一組繪圖內容，而不只是單一圖形或影像時，請使用此方法。</span><span class="sxs-lookup"><span data-stu-id="98866-130">Use this approach when you want to apply an opacity mask to a group of drawing content, not just a single shape or image.</span></span> <span data-ttu-id="98866-131">如需詳細資訊，請參閱 [圖層總覽](direct2d-layers-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="98866-131">For details, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a><span data-ttu-id="98866-132">使用點陣圖作為 FillOpacityMask 方法的不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="98866-132">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>

<span data-ttu-id="98866-133">[**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md)方法會繪製轉譯目標的矩形區域，然後套用由 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)定義的不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-133">The [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method paints a rectangular region of a render target and then applies an opacity mask, defined by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="98866-134">當您想要使用點陣圖作為矩形區域的不透明度遮罩時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="98866-134">Use this method when you have a bitmap that you want to use as an opacity mask for a rectangular region.</span></span>

<span data-ttu-id="98866-135">下圖顯示將不透明度遮罩套用 (具有花卉) 影像的效果 [**，以及 fern**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 工廠影像的 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。</span><span class="sxs-lookup"><span data-stu-id="98866-135">The following diagram shows an effect of applying the opacity mask (an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with an image of a flower) to an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with an image of a fern plant.</span></span> <span data-ttu-id="98866-136">產生的影像是裁剪至花卉形狀的植物點陣圖。</span><span class="sxs-lookup"><span data-stu-id="98866-136">The resulting image is a bitmap of a plant clipped to the flower shape.</span></span>

![花卉點陣圖的圖，用來做為 fern 工廠圖片上的不透明度遮罩](images/brushes-ovw-bitmapopacity.png)

<span data-ttu-id="98866-138">下列程式碼範例顯示如何完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="98866-138">The following code examples shows how this is accomplished.</span></span>

<span data-ttu-id="98866-139">第一個範例會載入下列點陣圖（ *m \_ pBitmapMask*），以做為點陣圖遮罩使用。</span><span class="sxs-lookup"><span data-stu-id="98866-139">The first example loads the following bitmap, *m\_pBitmapMask*, for use as a bitmap mask.</span></span> <span data-ttu-id="98866-140">下圖顯示產生的輸出。</span><span class="sxs-lookup"><span data-stu-id="98866-140">The following illustration shows the output that is produced.</span></span> <span data-ttu-id="98866-141">請注意，雖然點陣圖的不透明部分會顯示黑色，但是點陣圖中的色彩資訊不會影響到不透明度遮罩;只會使用點陣圖中每個圖元的不透明度資訊。</span><span class="sxs-lookup"><span data-stu-id="98866-141">Note that, although the opaque portion of the bitmap appears black, the color information in the bitmap has no effect on the opacity mask; only the opacity information of each pixel in the bitmap is used.</span></span> <span data-ttu-id="98866-142">此點陣圖中完全不透明的圖元已著色為僅供說明之用。</span><span class="sxs-lookup"><span data-stu-id="98866-142">The fully opaque pixels in this bitmap have been colored black for illustrative purposes only.</span></span>

![花卉點陣圖遮罩的圖例](images/bitmapmask.png)

<span data-ttu-id="98866-144">在此範例中， [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 是由範例中其他位置所定義的 Helper 方法 LoadResourceBitmap 所載入。</span><span class="sxs-lookup"><span data-stu-id="98866-144">In this example, the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is loaded by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



<span data-ttu-id="98866-145">下一個範例會定義套用不透明度遮罩的筆刷（ *m \_ pFernBitmapBrush*）。</span><span class="sxs-lookup"><span data-stu-id="98866-145">The next example defines the brush, *m\_pFernBitmapBrush*, to which the opacity mask is applied.</span></span> <span data-ttu-id="98866-146">這個範例會使用包含 fern 影像的 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) ，但是您可以改用 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)、 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)或 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 。</span><span class="sxs-lookup"><span data-stu-id="98866-146">This example uses an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that contains an image of a fern, but you could use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) instead.</span></span> <span data-ttu-id="98866-147">下圖顯示產生的輸出。</span><span class="sxs-lookup"><span data-stu-id="98866-147">The following illustration shows the output that is produced.</span></span>

![點陣圖筆刷使用的點陣圖圖例](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





<span data-ttu-id="98866-149">現在已定義不透明度遮罩和筆刷，您可以在應用程式的轉譯方法中使用 [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="98866-149">Now that opacity mask and the brush are defined, you can use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method in your application's rendering method.</span></span> <span data-ttu-id="98866-150">當您呼叫 **FillOpacityMask** 方法時，您必須指定所使用的不透明度檢測類型： **D2D1 \_ 不透明度 \_ 遮罩 \_ 內容 \_ 圖形**、 **D2D1 \_ 不透明度 \_ 遮罩 \_ 內容 \_ 文字 \_ 自然**，以及 **D2D1 \_ 不透明度 \_ 遮罩 \_ 內容 \_ 文字 \_ \_ 與 GDI 相容**。</span><span class="sxs-lookup"><span data-stu-id="98866-150">When you call the **FillOpacityMask** method, you must specify the type of opacity mask you are using: **D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**, **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_NATURAL**, and **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_GDI\_COMPATIBLE**.</span></span> <span data-ttu-id="98866-151">如需這三種類型的意義，請參閱 [**D2D1 \_ 不透明度 \_ 遮罩 \_ 內容**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)。</span><span class="sxs-lookup"><span data-stu-id="98866-151">For the meanings of these three types, see [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span></span>

> [!Note]  
> <span data-ttu-id="98866-152">從 Windows 8 開始，不需要 [**D2D1 不 \_ 透明度 \_ 遮罩 \_ 內容**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) 。</span><span class="sxs-lookup"><span data-stu-id="98866-152">Starting with Windows 8, the [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) is not required.</span></span> <span data-ttu-id="98866-153">請參閱 [**ID2D1DeviceCoNtext：： FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) 方法，它沒有 **D2D1 \_ 不透明度 \_ 遮罩 \_ 內容** 參數。</span><span class="sxs-lookup"><span data-stu-id="98866-153">See the [**ID2D1DeviceContext::FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) method, which has no **D2D1\_OPACITY\_MASK\_CONTENT** parameter.</span></span>

 

<span data-ttu-id="98866-154">下一個範例會將轉譯目標的消除鋸齒模式設定為 [**D2D1 \_ 消除鋸齒 \_ 模式 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) ，使不透明度遮罩可正常運作。</span><span class="sxs-lookup"><span data-stu-id="98866-154">The next example sets the render target's antialiasing mode to [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) so that the opacity mask will work properly.</span></span> <span data-ttu-id="98866-155">然後，它會呼叫 [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 方法，並將不透明度遮罩傳遞 (*m \_ pBitmapMask*) 、套用不透明度遮罩的筆刷 (*m \_ pFernBitmapBrush*) 、不透明度遮罩中的內容類型 ([**D2D1 \_ 不透明度 \_ 遮罩 \_ 內容 \_ 圖形**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) ，以及要繪製的區域。</span><span class="sxs-lookup"><span data-stu-id="98866-155">It then calls the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method and passes it the opacity mask (*m\_pBitmapMask*), the brush to which the opacity mask is applied (*m\_pFernBitmapBrush*), the type of content inside the opacity mask ([**D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)), and the area to paint.</span></span> <span data-ttu-id="98866-156">下圖顯示產生的輸出。</span><span class="sxs-lookup"><span data-stu-id="98866-156">The following illustration shows the output that is produced.</span></span>

![套用不透明度遮罩的 fern 植物圖片圖例](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





<span data-ttu-id="98866-158">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="98866-158">Code has been omitted from this example.</span></span>

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a><span data-ttu-id="98866-159">使用 FillGeometry 方法將筆刷作為不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="98866-159">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>

<span data-ttu-id="98866-160">上一節說明了如何使用 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 做為不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-160">The preceding section described how to use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) as an opacity mask.</span></span> <span data-ttu-id="98866-161">Direct2D 也提供 [**ID2D1RenderTarget：： FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法，可讓您在填滿 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)時，選擇性地將筆刷指定為不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-161">Direct2D also provides the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, which enables you to optionally specify brush as an opacity mask when you fill an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span></span> <span data-ttu-id="98866-162">這可讓您使用 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 或 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) 和點陣圖 (**ID2D1Bitmap**) ，從漸層 (建立不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-162">This enables you to create opacity masks from gradients (using [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) and bitmaps (using **ID2D1Bitmap**).</span></span>

<span data-ttu-id="98866-163">[**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)方法會採用三個參數：</span><span class="sxs-lookup"><span data-stu-id="98866-163">The [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method takes three parameters:</span></span>

-   <span data-ttu-id="98866-164">第一個參數（ [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)）會定義要繪製的圖形。</span><span class="sxs-lookup"><span data-stu-id="98866-164">The first parameter, an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), defines the shape to paint.</span></span>
-   <span data-ttu-id="98866-165">第二個參數（ [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)）指定用來繪製幾何的筆刷。</span><span class="sxs-lookup"><span data-stu-id="98866-165">The second parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies the brush used to paint the geometry.</span></span> <span data-ttu-id="98866-166">此參數必須是將其 x 和 y 延伸模式設定為 [**D2D1 \_ 擴充 \_ 模式 \_ 夾具**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)的 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。</span><span class="sxs-lookup"><span data-stu-id="98866-166">This parameter must be an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that has its x- and y-extend modes set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>
-   <span data-ttu-id="98866-167">第三個參數（ [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)）指定用來做為不透明度遮罩的筆刷。</span><span class="sxs-lookup"><span data-stu-id="98866-167">The third parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies a brush to use as the opacity mask.</span></span> <span data-ttu-id="98866-168">此筆刷可以是 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)、 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)或 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)。</span><span class="sxs-lookup"><span data-stu-id="98866-168">This brush may be an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), or an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span> <span data-ttu-id="98866-169"> (技術上，您可以使用 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)，但使用純色筆刷作為不透明度遮罩，並不會產生有趣的結果。 ) </span><span class="sxs-lookup"><span data-stu-id="98866-169">(Technically, you may use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), but using a solid color brush as an opacity mask doesn't produce interesting results.)</span></span>

<span data-ttu-id="98866-170">下列各節說明如何使用 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 和 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 物件做為不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-170">The following sections describe how to use [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) and [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) objects as opacity masks.</span></span>

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="98866-171">使用線性漸層筆刷做為不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="98866-171">Use an Linear Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="98866-172">下圖顯示將線性漸層筆刷套用至以花卉點陣圖填滿之矩形的效果。</span><span class="sxs-lookup"><span data-stu-id="98866-172">The following diagram shows the effect of applying a linear gradient brush to a rectangle that is filled with a bitmap of flowers.</span></span>

![套用線性漸層筆刷的花卉點陣圖圖表](images/brushes-ovw-lineargradient-opacitymask.png)

<span data-ttu-id="98866-174">接下來的步驟會說明如何重新建立此效果。</span><span class="sxs-lookup"><span data-stu-id="98866-174">The steps that follow describe how to re-create this effect.</span></span>

1.  <span data-ttu-id="98866-175">定義要遮罩的內容。</span><span class="sxs-lookup"><span data-stu-id="98866-175">Define the content to be masked.</span></span> <span data-ttu-id="98866-176">下列範例會建立 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) *m \_ pLinearFadeFlowersBitmap*。</span><span class="sxs-lookup"><span data-stu-id="98866-176">The following example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pLinearFadeFlowersBitmap*.</span></span> <span data-ttu-id="98866-177">適用于 *m \_ pLinearFadeFlowersBitmap* 的擴充模式會設定為 [**D2D1 \_ 擴充 \_ 模式的 \_ 夾具**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) ，使其可透過 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法與不透明度遮罩一起使用。</span><span class="sxs-lookup"><span data-stu-id="98866-177">The extend mode x- and y- for *m\_pLinearFadeFlowersBitmap* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) so that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="98866-178">C++</span><span class="sxs-lookup"><span data-stu-id="98866-178">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="98866-179">C++</span><span class="sxs-lookup"><span data-stu-id="98866-179">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  <span data-ttu-id="98866-180">定義不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-180">Define the opacity mask.</span></span> <span data-ttu-id="98866-181">下一個程式碼範例會建立對角線性漸層筆刷 (*m \_ PLinearGradientBrush*) ，從位置0將完全不透明的黑色淡化為位置1的完全透明白色。</span><span class="sxs-lookup"><span data-stu-id="98866-181">The next code example creates a diagonal linear gradient brush (*m\_pLinearGradientBrush*) that fades from fully opaque black at position 0 to completely transparent white at position 1.</span></span>
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  <span data-ttu-id="98866-182">使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法。</span><span class="sxs-lookup"><span data-stu-id="98866-182">Use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="98866-183">最後一個範例會使用內容筆刷的 **FillGeometry** 方法，以 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) 填入 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) ，並套用不透明度遮罩 (*m \_ pLinearGradientBrush*) 。</span><span class="sxs-lookup"><span data-stu-id="98866-183">The final example uses the **FillGeometry** method to the content brush to fill a [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*) with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pLinearFadeFlowersBitmap*) and applies an opacity mask (*m\_pLinearGradientBrush*).</span></span>
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

<span data-ttu-id="98866-184">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="98866-184">Code has been omitted from this example.</span></span>

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="98866-185">使用放射狀漸層筆刷做為不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="98866-185">Use a Radial Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="98866-186">下圖顯示將放射狀漸層筆刷套用至以 foliage 點陣圖填滿之矩形的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="98866-186">The following diagram shows the visual effect of applying a radial gradient brush to a rectangle that is filled with a bitmap of foliage.</span></span>

![已套用放射狀漸層筆刷的 foliage 點陣圖圖表](images/brushes-ovw-radialgradient-opacitymask.png)

<span data-ttu-id="98866-188">第一個範例會建立 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)， *m \_ pRadialFadeFlowersBitmapBrush*。</span><span class="sxs-lookup"><span data-stu-id="98866-188">The first example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pRadialFadeFlowersBitmapBrush*.</span></span> <span data-ttu-id="98866-189">如此一來，就可以透過 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法與不透明度遮罩搭配使用，而 *m \_ pRadialFadeFlowersBitmapBrush* 的擴充模式會設定為 [**D2D1 \_ 延伸 \_ 模式的 \_ 夾具**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)。</span><span class="sxs-lookup"><span data-stu-id="98866-189">So that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, the extend mode x- and y- for *m\_pRadialFadeFlowersBitmapBrush* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98866-190">C++</span><span class="sxs-lookup"><span data-stu-id="98866-190">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98866-191">C++</span><span class="sxs-lookup"><span data-stu-id="98866-191">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="98866-192">下一個範例會定義將用作不透明度遮罩的星形漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="98866-192">The next example defines the radial gradient brush that will be used as the opacity mask.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





<span data-ttu-id="98866-193">最後一個程式碼範例會使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) 和不透明度遮罩 (*m \_ pRadialGradientBrush*) 來填滿 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) 。</span><span class="sxs-lookup"><span data-stu-id="98866-193">The final code example uses the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pRadialFadeFlowersBitmapBrush*) and the opacity mask (*m\_pRadialGradientBrush*) to fill an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*).</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



<span data-ttu-id="98866-194">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="98866-194">Code has been omitted from this example.</span></span>

## <a name="apply-an-opacity-mask-to-a-layer"></a><span data-ttu-id="98866-195">將不透明度遮罩套用至圖層</span><span class="sxs-lookup"><span data-stu-id="98866-195">Apply an Opacity Mask to a Layer</span></span>

<span data-ttu-id="98866-196">當您呼叫 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 將 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 推送至轉譯目標時，您可以使用 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) 結構，將筆刷套用為不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-196">When you call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) to push an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) onto an render target, you can use the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to apply a brush as an opacity mask.</span></span> <span data-ttu-id="98866-197">下列程式碼範例會使用 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 做為不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="98866-197">The following code example uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) as an opacity mask.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="98866-198">如需使用圖層的詳細資訊，請參閱 [圖層總覽](direct2d-layers-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="98866-198">For more information about using layers, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="98866-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="98866-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98866-200">筆刷概觀</span><span class="sxs-lookup"><span data-stu-id="98866-200">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="98866-201">圖層總覽</span><span class="sxs-lookup"><span data-stu-id="98866-201">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

 

 