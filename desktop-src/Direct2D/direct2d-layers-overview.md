---
title: 圖層總覽
description: 描述 Direct2D 圖層的基本概念。
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D，圖層
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ac68ba25d1e8f35c5a41daec4d7a5295235a5d98
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549183"
---
# <a name="layers-overview"></a>圖層總覽

本總覽說明使用 Direct2D 層的基本概念。 包含以下幾節。

-   [什麼是圖層？](#what-are-layers)
-   [Windows 8 和更新版本中的圖層](#layers-in-windows-8-and-later)
    -   [ID2D1DeviceCoNtext 和 PushLayer](#id2d1devicecontext-and-pushlayer)
    -   [D2D1 \_ 圖層 \_ PARAMETERS1 和 D2D1 \_ 圖層 \_ OPTIONS1](/windows)
    -   [混合模式](#blend-modes)
    -   [相互](#interoperation)
-   [建立圖層](#creating-layers)
-   [內容界限](#content-bounds)
-   [幾何遮罩](#geometric-masks)
-   [不透明度遮罩](#opacity-masks)
-   [圖層的替代專案](#alternatives-to-layers)
-   [裁剪任意圖形](#clipping-an-arbitrary-shape)
    -   [軸對齊的剪輯](#axis-aligned-clips)
-   [相關主題](#related-topics)

## <a name="what-are-layers"></a>什麼是圖層？

以 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 物件表示的圖層，可讓應用程式操作一組繪圖作業。 您可以使用圖層，將它「推送」到轉譯目標。 轉譯目標的後續繪圖作業會導向至圖層。 當您完成圖層之後，您會從呈現目標「快顯」圖層，將圖層的內容合成回轉譯目標。

和筆刷一樣，圖層是由呈現目標所建立的裝置相依資源。 您可以在包含建立它之轉譯目標所在的相同資源網域中的任何轉譯目標上使用圖層。 不過，一次只能有一個呈現目標使用的圖層資源。 如需資源的詳細資訊，請參閱 [資源總覽](resources-and-resource-domains.md)。

雖然圖層提供了功能強大的轉譯技術來產生有趣的效果，但應用程式中的圖層數量過多可能會對其效能造成負面影響，因為與管理圖層和分層資源相關聯的成本各有不同。 例如，填滿或清除圖層，然後再將它混合回來（尤其是在高階硬體上）的成本。 然後，會有管理層資源的成本。 如果您經常重新配置這些，產生的 GPU 將會是最重要的問題。 當您設計您的應用程式時，請嘗試最大化重複使用圖層資源。

## <a name="layers-in-windows-8-and-later"></a>Windows 8 和更新版本中的圖層

Windows 8 引進了新的分層相關 Api，可簡化、改善的效能，並將功能新增至圖層。

### <a name="id2d1devicecontext-and-pushlayer"></a>ID2D1DeviceCoNtext 和 PushLayer

[**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)介面衍生自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)介面，也是在 Windows 8 中顯示 Direct2D 內容的關鍵。如需此介面的詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md)內容。 您可以使用裝置內容介面略過呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 方法，然後將 Null 傳遞至 [**ID2D1DeviceCoNtext：:P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) 方法。 Direct2D 會自動管理圖層資源，並可在圖層和效果圖形之間共用資源。

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a>D2D1 \_ 圖層 \_ PARAMETERS1 和 D2D1 \_ 圖層 \_ OPTIONS1

[**D2D1 \_ LAYER \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1)結構與 [**D2D1 圖層 \_ \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)相同，不同之處在于結構的最後一個成員現在是 [**D2D1 \_ LAYER \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)列舉。

[**D2D1 \_圖層 \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) 沒有 ClearType 選項，有兩個不同的選項可讓您用來改善效能：

-   [**D2D1 \_圖 \_ 層 \_ OPTIONS1 \_ 從 \_ 背景初始化**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)： Direct2D 會將基本專案轉譯為圖層，而不會以透明黑色將其清除。 這並不是預設值，但在大部分情況下，會產生較佳的效能。

-   [**D2D1 \_圖層 \_ OPTIONS1 \_ 忽略 \_ Alpha**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)：如果基礎介面設定為 [**D2D1 \_ ALPHA \_ 模式 \_ 忽略**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)，此選項可讓 Direct2D 避免修改圖層的 ALPHA 色板。 在其他情況下請勿使用此功能。

### <a name="blend-modes"></a>混合模式

從 Windows 8 開始，裝置內容具有 [**基本 blend 模式**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) ，可決定每個基本類型如何與目標介面混合。 當您呼叫 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) 方法時，這個模式也適用于圖層。

例如，如果您使用圖層來裁剪具有透明度的基本專案，請在裝置內容上設定 [**D2D1 \_ 基本 \_ BLEND \_ 複製**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) 模式，以取得適當的結果。 複製模式會根據圖層的幾何遮罩，讓裝置內容線性將所有4色通道（包括 Alpha 色板）插補，其中每個圖元都有目標介面的內容。

### <a name="interoperation"></a>互通

從 Windows 8 開始，Direct2D 支援在推送圖層或剪輯時，與 Direct3D 和 GDI 交互操作。 您可以呼叫 [**ID2D1GdiInteropRenderTarget：： GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) ，同時將圖層推送至與 GDI 相交互操作。 您可以呼叫 [**ID2D1DeviceCoNtext：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) ，然後轉譯至基礎介面，以與 Direct3D 交互操作。 使用 Direct3D 或 GDI 在圖層或剪輯內轉譯是您的責任。 如果您嘗試在圖層或剪輯之外轉譯，則結果為未定義。

## <a name="creating-layers"></a>建立圖層

使用圖層需要熟悉 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))、 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 方法，以及 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) 結構，其中包含一組可定義如何使用圖層的參數化資料。 下列清單描述方法和結構。

-   呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 方法來建立圖層資源。
    > [!Note]  
    > 從 Windows 8 開始，您可以略過呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))方法，然後在 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)介面上將 Null 傳遞至 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))方法。 這比較簡單，而且可讓 Direct2D 自動管理圖層資源，以及在圖層和效果圖形之間共用資源。

     

-   當轉譯目標在呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法之後，開始繪製 () 之後，您就可以使用 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 方法。 **PushLayer** 方法會將指定的圖層加入至轉譯目標，讓目標接收所有後續的繪圖作業，直到呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)為止。 這個方法會透過呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))和 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)結構中的 *layerParameters* ，來取得傳回的 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)物件。 下表描述結構的欄位。 

    | 欄位                 | 描述|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **contentBounds**     | 圖層的內容界限。 這些界限以外的內容不會呈現。 此參數的預設值為 [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)。 使用預設值時，內容界限實際上會被視為呈現目標的界限。 |
    | **geometricMask**     |  (選擇性的) 區域（由 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)定義），應將該圖層裁剪至該區域。 如果不應該將圖層裁剪成幾何，請設定為 **Null** 。 |
    | **maskAntialiasMode** | 值，指定 **geometricMask** 欄位所指定之幾何遮罩的消除鋸齒模式。 |
    | **maskTransform**     | 值，指定在組合圖層時，套用至幾何遮罩的轉換。 這是與世界轉換相關的。  |
    | **透明度**           | 圖層的不透明度值。 當對目標進行組合時，圖層中每個資源的不透明度會乘以此值。  |
    | **opacityBrush**      |  (選擇性) 用來修改圖層不透明度的筆刷。 筆刷會對應到圖層，而每個對應筆刷圖元的 Alpha 色板會乘以對應的圖層圖元。 如果圖層不應有不透明度遮罩，則設定為 **Null** 。   |
    | **layerOptions**      | 值，指定圖層是否打算以 ClearType 消除鋸齒來呈現文字。 此參數預設為 off。 開啟它可讓 ClearType 正常運作，但會產生稍微慢的轉譯速度。    |

    

     

    > [!Note]  
    > 從 Windows 8 開始，您無法在圖層中以 ClearType 轉譯，因此 **layerOptions** 參數應一律設定為 [**D2D1 \_ 圖層 \_ 選項 \_ NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)

     

    為了方便起見，Direct2D 提供 [**D2D1：： LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) 方法，以協助您建立 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) 結構。

-   若要將圖層的內容複合到轉譯目標中，請呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 方法。 在呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)方法之前，您必須先呼叫 **PopLayer** 方法。

下列範例顯示如何使用 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))、 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)。 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)結構中的所有欄位都會設定為其預設值，但 **opacityBrush** 會設定為 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)。


```C++
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
```



此範例中省略了程式碼。

請注意，當您呼叫 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) 和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)時，請確定每個 **PushLayer** 都有相符的 **PopLayer** 呼叫。 如果有比 **PushLayer** 呼叫更多的 **PopLayer** 呼叫，轉譯目標會置於錯誤狀態。 如果在所有未處理的層上取出之前呼叫 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) ，轉譯目標會進入錯誤狀態，並傳回錯誤。 若要清除錯誤狀態，請使用 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)。

## <a name="content-bounds"></a>內容界限

**ContentBounds** 會設定要繪製至圖層的限制。 只有內容界限內的專案會呈現回轉譯目標。

接下來的範例會示範如何指定 **contentBounds** ，以便將原始影像裁剪至左上角的內容界限， (10，108) ，而右下角 (121，177) 。 下圖顯示將影像裁剪至內容界限的原始影像和結果。

![原始圖片上的內容界限圖例和產生的裁剪圖片](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



此範例中省略了程式碼。

> [!Note]
>
> 如果您指定 **geometricMask**，則會進一步影響產生的裁剪影像。 如需詳細資訊，請參閱「 [幾何遮罩](#geometric-masks) 」一節。

 

## <a name="geometric-masks"></a>幾何遮罩

幾何遮罩是由 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 物件所定義的剪輯或裁剪，可在呈現目標繪製圖層時遮罩圖層。 您可以使用 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)結構的 **geometricMask** 欄位，將結果遮罩到幾何。 例如，如果您想要顯示由區塊字母 "A" 遮罩的影像，您可以先建立代表封鎖字母 "A" 的幾何，然後使用該幾何作為圖層的幾何遮罩。 然後，在推送圖層之後，您就可以繪製影像。 快顯圖層會導致影像裁剪成封鎖字母「A」圖形。

接下來的範例顯示如何建立包含山區圖形的 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) ，然後將路徑幾何傳遞給 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))。 然後繪製點陣圖和方塊。 如果要轉譯的圖層中只有一個點陣圖，請使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 搭配壓制點陣圖筆刷來提高效率。 下圖顯示範例的輸出。

![套用山的幾何遮罩之後，分葉圖片和產生的圖片的圖例](images/layers-bitmapmask.png)

第一個範例會定義要當做遮罩使用的幾何。


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



下一個範例會使用 geometry 做為圖層的遮罩。


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

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



此範例中省略了程式碼。

> [!Note]
>
> 一般來說，如果您指定 **geometricMask**，您可以使用 **contentBounds** 的預設值 [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)。
>
> 如果 **contentBounds** 為 null，而 **GEOMETRICMASK** 為非 null，則在套用遮罩轉換之後，內容界限實際上是幾何遮罩的範圍。
>
> 如果 **contentBounds** 為非 null，且 **GEOMETRICMASK** 為非 null，則會有效地針對內容界限裁剪已轉換的幾何遮罩，並假設內容界限是無限的。

 

## <a name="opacity-masks"></a>不透明度遮罩

不透明度遮罩是由筆刷或點陣圖描述的遮罩，會套用到另一個物件，使該物件部分或完全透明。 它允許使用筆刷的 Alpha 色板作為內容遮罩。 例如，您可以定義不同于透明的星形漸層筆刷，以建立 vignette 效果。

接下來的範例會使用 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) 作為不透明度遮罩。 然後繪製點陣圖和方塊。 如果要轉譯的圖層中只有一個點陣圖，請使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 搭配壓制點陣圖筆刷來提高效率。 下圖顯示此範例的輸出。

![套用不透明度遮罩之後的樹狀結構圖片和產生的圖片圖例](images/layers-opacitymask.png)


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



此範例中省略了程式碼。

> [!Note]  
> 此範例會使用圖層將不透明度遮罩套用至單一物件，讓範例盡可能簡單。 將不透明度遮罩套用至單一物件時，使用 [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 或 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法（而非圖層）會更有效率。

 

如需如何在不使用圖層的情況下套用不透明度遮罩的指示，請參閱 [不透明度遮罩總覽](opacity-masks-overview.md)。

## <a name="alternatives-to-layers"></a>圖層的替代專案

如先前所述，過多的層級可能會對應用程式的效能造成負面影響。 若要改善效能，請盡可能避免使用圖層;改為使用其替代方案。 下列程式碼範例示範如何使用 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) 和 [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) 來裁剪區域，以替代使用具有內容界限的圖層。


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



同樣地，使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 搭配壓制點陣圖筆刷，作為在圖層中只有一個要轉譯的內容時，使用具有不透明度遮罩的圖層的替代方式，如下列範例所示。


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



除了使用具有幾何遮罩的圖層之外，請考慮使用點陣圖遮罩來裁剪區域，如下列範例所示。


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



最後，如果您想要將不透明度套用至單一基本型別，則應該將不透明度乘以至筆刷色彩，然後轉譯基本類型。 您不需要圖層或不透明度遮罩點陣圖。


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a>裁剪任意圖形

這裡的圖顯示將剪輯套用至影像的結果。

![顯示剪輯前後影像範例的影像。](images/clip.png)

您可以使用具有幾何遮罩的圖層或具有不透明度筆刷的 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法來取得這個結果。

以下是使用圖層的範例：


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



以下是使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法的範例：


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



在此程式碼範例中，當您呼叫 PushLayer 方法時，不會傳入應用程式所建立的圖層。 Direct2D 會為您建立圖層。 Direct2D 可以管理此資源的配置和終結，而不需要應用程式的任何介入。 這可讓 Direct2D 在內部重複使用圖層，並套用資源管理優化。

> [!Note]  
> 在 Windows 8 已對層級使用進行許多優化，建議您盡可能嘗試使用層 Api，而不是 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 。

 

### <a name="axis-aligned-clips"></a>軸對齊的剪輯

如果要裁剪的區域對齊繪圖介面的軸，而不是任意的。 此案例適用于使用剪輯矩形而非圖層。 效能提升比反鋸齒幾何的別名幾何更多。 如需軸對齊剪輯的詳細資訊，請參閱 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 主題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 