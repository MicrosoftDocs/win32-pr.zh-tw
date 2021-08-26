---
title: 不透明度遮罩概觀
description: 本主題說明如何使用點陣圖和筆刷來定義不透明度遮罩。 包含以下幾節。
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2050cccd37012028e2a86fbf77cd071671ce7201
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626554"
---
# <a name="opacity-masks-overview"></a>不透明度遮罩概觀

本主題說明如何使用點陣圖和筆刷來定義不透明度遮罩。 包含以下幾節。

-   [必要條件](#prerequisites)
-   [什麼是不透明度遮罩？](#what-is-an-opacity-mask)
-   [使用點陣圖作為 FillOpacityMask 方法的不透明度遮罩](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [使用 FillGeometry 方法將筆刷作為不透明度遮罩](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [使用線性漸層筆刷做為不透明度遮罩](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [使用放射狀漸層筆刷做為不透明度遮罩](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [將不透明度遮罩套用至圖層](#apply-an-opacity-mask-to-a-layer)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>先決條件

本總覽假設您已經熟悉基本的 Direct2D 繪圖作業，如 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md) 逐步解說中所述。 您也應該熟悉不同類型的筆刷，如 [筆刷總覽](direct2d-brushes-overview.md)中所述。

## <a name="what-is-an-opacity-mask"></a>什麼是不透明度遮罩？

不透明度遮罩是由筆刷或點陣圖描述的遮罩，會套用到另一個物件，使該物件部分或完全透明。 不透明度遮罩會使用 Alpha 色板資訊來指定如何將物件的來源圖元混合到最後的目的地目標。 遮罩的透明部分表示隱藏基礎影像的區域，而遮罩的不透明部分則會指出遮罩物件的顯示位置。

有幾種方式可以套用不透明度遮罩：

-   使用 [**ID2D1RenderTarget：： FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 方法。 **FillOpacityMask** 方法會繪製呈現目標的矩形區域，然後套用由點陣圖定義的不透明度遮罩。 當您的不透明度遮罩為點陣圖，而您想要填滿矩形區域時，請使用這個方法。
-   使用 [**ID2D1RenderTarget：： FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法。 **FillGeometry** 方法會使用指定的 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)繪製幾何的內部，然後套用由筆刷定義的不透明度遮罩。 當您想要將不透明度遮罩套用至幾何，或想要使用筆刷做為不透明度遮罩時，請使用這個方法。
-   使用 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 來套用不透明度遮罩。 當您想要將不透明度遮罩套用至一組繪圖內容，而不只是單一圖形或影像時，請使用此方法。 如需詳細資訊，請參閱 [圖層總覽](direct2d-layers-overview.md)。

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a>使用點陣圖作為 FillOpacityMask 方法的不透明度遮罩

[**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md)方法會繪製轉譯目標的矩形區域，然後套用由 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)定義的不透明度遮罩。 當您想要使用點陣圖作為矩形區域的不透明度遮罩時，請使用這個方法。

下圖顯示將不透明度遮罩套用 (具有花卉) 影像的效果 [**，以及 fern**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 工廠影像的 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。 產生的影像是裁剪至花卉形狀的植物點陣圖。

![花卉點陣圖的圖，用來做為 fern 工廠圖片上的不透明度遮罩](images/brushes-ovw-bitmapopacity.png)

下列程式碼範例顯示如何完成這項作業。

第一個範例會載入下列點陣圖（ *m \_ pBitmapMask*），以做為點陣圖遮罩使用。 下圖顯示產生的輸出。 請注意，雖然點陣圖的不透明部分會顯示黑色，但是點陣圖中的色彩資訊不會影響到不透明度遮罩;只會使用點陣圖中每個圖元的不透明度資訊。 此點陣圖中完全不透明的圖元已著色為僅供說明之用。

![花卉點陣圖遮罩的圖例](images/bitmapmask.png)

在此範例中， [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 是由範例中其他位置所定義的 Helper 方法 LoadResourceBitmap 所載入。


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



下一個範例會定義套用不透明度遮罩的筆刷（ *m \_ pFernBitmapBrush*）。 這個範例會使用包含 fern 影像的 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) ，但是您可以改用 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)、 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)或 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 。 下圖顯示產生的輸出。

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





現在已定義不透明度遮罩和筆刷，您可以在應用程式的轉譯方法中使用 [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 方法。 當您呼叫 **FillOpacityMask** 方法時，您必須指定所使用的不透明度檢測類型： **D2D1 \_ 不透明度 \_ 遮罩 \_ 內容 \_ 圖形**、 **D2D1 \_ 不透明度 \_ 遮罩 \_ 內容 \_ 文字 \_ 自然**，以及 **D2D1 \_ 不透明度 \_ 遮罩 \_ 內容 \_ 文字 \_ \_ 與 GDI 相容**。 如需這三種類型的意義，請參閱 [**D2D1 \_ 不透明度 \_ 遮罩 \_ 內容**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)。

> [!Note]  
> 從 Windows 8 開始，不需要 [**D2D1 不 \_ 透明度 \_ 遮罩 \_ 內容**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)。 請參閱 [**ID2D1DeviceCoNtext：： FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) 方法，它沒有 **D2D1 \_ 不透明度 \_ 遮罩 \_ 內容** 參數。

 

下一個範例會將轉譯目標的消除鋸齒模式設定為 [**D2D1 \_ 消除鋸齒 \_ 模式 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) ，使不透明度遮罩可正常運作。 然後，它會呼叫 [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 方法，並將不透明度遮罩傳遞 (*m \_ pBitmapMask*) 、套用不透明度遮罩的筆刷 (*m \_ pFernBitmapBrush*) 、不透明度遮罩中的內容類型 ([**D2D1 \_ 不透明度 \_ 遮罩 \_ 內容 \_ 圖形**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) ，以及要繪製的區域。 下圖顯示產生的輸出。

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





此範例中省略了程式碼。

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a>使用 FillGeometry 方法將筆刷作為不透明度遮罩

上一節說明了如何使用 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 做為不透明度遮罩。 Direct2D 也提供 [**ID2D1RenderTarget：： FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法，可讓您在填滿 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)時，選擇性地將筆刷指定為不透明度遮罩。 這可讓您使用 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 或 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) 和點陣圖 (**ID2D1Bitmap**) ，從漸層 (建立不透明度遮罩。

[**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)方法會採用三個參數：

-   第一個參數（ [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)）會定義要繪製的圖形。
-   第二個參數（ [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)）指定用來繪製幾何的筆刷。 此參數必須是將其 x 和 y 延伸模式設定為 [**D2D1 \_ 擴充 \_ 模式 \_ 夾具**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)的 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。
-   第三個參數（ [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)）指定用來做為不透明度遮罩的筆刷。 此筆刷可以是 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)、 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)或 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)。  (技術上，您可以使用 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)，但使用純色筆刷作為不透明度遮罩，並不會產生有趣的結果。 ) 

下列各節說明如何使用 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 和 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 物件做為不透明度遮罩。

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a>使用線性漸層筆刷做為不透明度遮罩

下圖顯示將線性漸層筆刷套用至以花卉點陣圖填滿之矩形的效果。

![套用線性漸層筆刷的花卉點陣圖圖表](images/brushes-ovw-lineargradient-opacitymask.png)

接下來的步驟會說明如何重新建立此效果。

1.  定義要遮罩的內容。 下列範例會建立 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) *m \_ pLinearFadeFlowersBitmap*。 適用于 *m \_ pLinearFadeFlowersBitmap* 的擴充模式會設定為 [**D2D1 \_ 擴充 \_ 模式的 \_ 夾具**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) ，使其可透過 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法與不透明度遮罩一起使用。

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
    <col  />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
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
    <col  />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  定義不透明度遮罩。 下一個程式碼範例會建立對角線性漸層筆刷 (*m \_ PLinearGradientBrush*) ，從位置0將完全不透明的黑色淡化為位置1的完全透明白色。
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



    

3.  使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法。 最後一個範例會使用內容筆刷的 **FillGeometry** 方法，以 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) 填入 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) ，並套用不透明度遮罩 (*m \_ pLinearGradientBrush*) 。
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

此範例中省略了程式碼。

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a>使用放射狀漸層筆刷做為不透明度遮罩

下圖顯示將放射狀漸層筆刷套用至以 foliage 點陣圖填滿之矩形的視覺效果。

![已套用放射狀漸層筆刷的 foliage 點陣圖圖表](images/brushes-ovw-radialgradient-opacitymask.png)

第一個範例會建立 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)， *m \_ pRadialFadeFlowersBitmapBrush*。 如此一來，就可以透過 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法與不透明度遮罩搭配使用，而 *m \_ pRadialFadeFlowersBitmapBrush* 的擴充模式會設定為 [**D2D1 \_ 延伸 \_ 模式的 \_ 夾具**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)。


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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



下一個範例會定義將用作不透明度遮罩的星形漸層筆刷。


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





最後一個程式碼範例會使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) 和不透明度遮罩 (*m \_ pRadialGradientBrush*) 來填滿 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) 。


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



此範例中省略了程式碼。

## <a name="apply-an-opacity-mask-to-a-layer"></a>將不透明度遮罩套用至圖層

當您呼叫 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 將 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 推送至轉譯目標時，您可以使用 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) 結構，將筆刷套用為不透明度遮罩。 下列程式碼範例會使用 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 做為不透明度遮罩。


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



如需使用圖層的詳細資訊，請參閱 [圖層總覽](direct2d-layers-overview.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[筆刷概觀](direct2d-brushes-overview.md)
</dt> <dt>

[圖層總覽](direct2d-layers-overview.md)
</dt> </dl>

 

 
