---
title: 改善 Direct2D 應用程式的效能
description: 描述改善 Direct2D 效能的技術。
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D，效能
- Direct2D，點陣圖
- Direct2D，資源使用量
- Direct2D、Flush 方法
- Direct2D、靜態內容
- Direct2D 的效能
- Direct2D 的點陣圖
- Direct2D，GDI 交互操作
- Direct2D，互通性
- 互通性，Direct2D
- '圖形裝置介面 (GDI) '
- 'GDI (圖形裝置介面) '
- '互通性、圖形裝置介面 (GDI) '
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 34adfd708ef3c1b8d7a6af145d9d1c9505b01beb1ba9b31834e267123ad05b69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641498"
---
# <a name="improving-the-performance-of-direct2d-apps"></a>改善 Direct2D 應用程式的效能

雖然 [Direct2D](./direct2d-portal.md) 是硬體加速的，且適用于高效能，但您必須正確使用這些功能才能將輸送量最大化。 此處所示的技巧衍生自研究一般案例，可能不適用於所有應用程式案例。 因此，請仔細瞭解應用程式行為和效能目標，以協助達到您想要的結果。

-   [資源使用量](#resource-usage)
    -   [重複使用資源](#reuse-resources)
-   [限制使用 flush](#restrict-the-use-of-flush)
-   [點陣圖](#create-large-bitmaps)
    -   [建立大型點陣圖](#create-large-bitmaps)
    -   [建立點陣圖的塔](#create-an-atlas-of-bitmaps)
    -   [建立共用點陣圖](#create-shared-bitmaps)
    -   [複製點陣圖](#copying-bitmaps)
-   [在虛線區分上使用磚點陣圖](#use-tiled-bitmap-over-dashing)
-   [呈現複雜靜態內容的一般指導方針](#general-guidelines-for-rendering-complex-static-content)
    -   [使用色彩點陣圖的完整場景快取](#full-scene-caching-using-a-color-bitmap)
    -   [使用 A8 點陣圖和 FillOpacityMask 方法的每一基本快取](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [使用 geometry 實踐的每個基本快取](#per-primitive-caching-using-geometry-realizations)
-   [幾何轉譯](#geometry-rendering)
    -   [針對繪製幾何使用特定的繪圖基本](#use-specific-draw-primitive-over-draw-geometry)
    -   [呈現靜態幾何](#rendering-static-geometry)
    -   [使用多執行緒裝置內容](#use-a-multithreaded-device-context)
-   [使用 Direct2D 繪製文字](#use-a-multithreaded-device-context)
    -   [DrawTextLayout 與 DrawText 的比較](#drawtextlayout-vs-drawtext)
    -   [選擇正確的文字呈現模式](#choosing-the-right-text-rendering-mode)
    -   [Caching](#full-scene-caching-using-a-color-bitmap)
-   [裁剪任意圖形](#clipping-an-arbitrary-shape)
    -   [Windows 8 中的 PushLayer](#pushlayer-in-windows-8)
    -   [軸對齊的剪輯](#axis-aligned-clips)
-   [DXGI 互通性：避免頻繁切換](#dxgi-interoperability-avoid-frequent-switches)
-   [知道您的像素格式](#know-your-pixel-format)
-   [場景複雜性](#scene-complexity)
    -   [瞭解場景複雜性](#understand-scene-complexity)
-   [改善 Direct2D 列印應用程式的效能](#improving-performance-for-direct2d-printing-apps)
    -   [當您建立 D2D 列印控制項時，設定正確的屬性值](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [避免使用特定的 Direct2D 繪製模式](#avoid-using-certain-direct2d-drawing-patterns)
    -   [以直接且簡單的方式繪製文字](#draw-text-in-a-direct-and-plain-way)
    -   [盡可能繪製原始點陣圖](#draw-the-original-bitmaps-when-possible)
-   [結論](#conclusion)

## <a name="resource-usage"></a>資源使用量

在影片或系統記憶體中，資源是某種類型的配置。 點陣圖和筆刷是資源的範例。

在 Direct2D 中，您可以在軟體和硬體中建立資源。 在硬體上建立和刪除資源是昂貴的作業，因為它們需要大量的額外負荷來與視訊卡通訊。 讓我們來看看 Direct2D 如何將內容轉譯為目標。

在 Direct2D 中，所有轉譯命令都包含在呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 和 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)的呼叫之間。 這些呼叫會對轉譯目標進行。 呼叫轉譯作業之前，您必須先呼叫 **BeginDraw** 方法。 呼叫 **BeginDraw** 之後，內容通常會建立一批轉譯命令，但是會延遲這些命令的處理，直到下列其中一個陳述成立為止：

-   發生 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 。 呼叫 **EndDraw** 時，會導致任何批次繪製作業完成，並傳回作業的狀態。
-   您可以明確呼叫 [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)： **flush** 方法會導致處理批次，併發出所有暫止的命令。
-   保存呈現命令的緩衝區已滿。 如果在完成前兩個條件之前，此緩衝區已滿，則會清除轉譯命令。

在清除基本專案之前，Direct2D 會保留對應資源的內部參考，例如點陣圖和筆刷。

### <a name="reuse-resources"></a>重複使用資源

如先前所述，資源的建立和刪除在硬體上很昂貴。 因此，請盡可能重複使用資源。 在遊戲開發過程中建立點陣圖建立範例。 通常會在遊戲中構成場景的點陣圖，同時以後續的框架對框架轉譯所需的所有不同變化來建立。 在實際的場景轉譯和重新呈現時，會重複使用這些點陣圖，而不是重新建立。

> [!Note]  
> 您無法重複使用資源來調整視窗大小。 調整視窗大小時，必須重新建立某些隨比例依存的資源，例如相容轉譯目標，而且可能需要重新建立某些圖層資源，因為視窗內容必須重新繪製。 這對於維護轉譯場景的整體品質而言很重要。

 

## <a name="restrict-the-use-of-flush"></a>限制使用 flush

因為 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法會導致批次處理轉譯命令的處理，所以建議您不要使用它。 針對大部分的常見案例，請將資源管理留給 Direct2D。

## <a name="bitmaps"></a>點陣圖

如先前所述，建立和刪除資源在硬體上是相當昂貴的作業。 點陣圖是經常使用的一種資源。 在視訊卡上建立點陣圖很昂貴。 重複使用它們可讓應用程式更快。

### <a name="create-large-bitmaps"></a>建立大型點陣圖

視訊卡通常會有最小的記憶體配置大小。 如果要求的配置小於此值，系統就會配置此最小大小的資源，而剩餘的記憶體會被浪費，並無法供其他專案使用。 如果您需要許多小型點陣圖，更好的方法是配置一個大型點陣圖，並將所有小點陣圖內容儲存在這個大型點陣圖中。 然後，您可以在需要較小點陣圖的位置讀取較大點陣圖的子領域。 通常，您應該在小型點陣圖之間包含填補 (透明的黑色圖元) ，以避免在作業期間較小影像之間的任何互動。 這也稱為 *塔*，其優點是減少點陣圖建立的額外負荷，以及小型點陣圖配置的記憶體浪費。 建議您將大部分的點陣圖保持至少為 64 KB，並限制小於 4 KB 的點陣圖數目。

### <a name="create-an-atlas-of-bitmaps"></a>建立點陣圖的塔

有一些常見的案例，例如點陣圖塔可以提供很好的服務。 小型點陣圖可以儲存在大型點陣圖內。 當您藉由指定目的地矩形來需要這些小型點陣圖時，可以從較大的點陣圖提取這些小點陣圖。 例如，應用程式必須繪製多個圖示。 所有與圖示相關聯的點陣圖都可以預先載入大型點陣圖。 而且在轉譯時，可以從大型點陣圖取出它們。

> [!Note]  
> 在視訊記憶體中建立的 Direct2D 點陣圖受限於儲存該點陣圖的介面卡所支援的點陣圖大小上限。 建立大於該點陣圖的點陣圖可能會導致錯誤。

 

> [!Note]  
> 從 Windows 8 開始，Direct2D 包含可讓此程式變得更容易的[塔效果](atlas.md)。

 

### <a name="create-shared-bitmaps"></a>建立共用點陣圖

建立共用點陣圖可讓 advanced 呼叫者建立 Direct2D 點陣圖物件，這些物件是直接由現有物件所支援，且已與轉譯目標相容。 這可避免建立多個表面，並有助於減少效能負擔。

> [!Note]  
> 共用點陣圖通常僅限於軟體目標或可與 DXGI 互通的目標。 使用 [**CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1))、 [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))和 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) 方法來建立共用點陣圖。

 

### <a name="copying-bitmaps"></a>複製點陣圖

建立 DXGI 介面是一項昂貴的作業，因此當您可以時重複使用現有的表面。 即使是在軟體中，如果點陣圖大多是您想要的表單，但不只是小部分，最好是更新該部分，而不是將整個點陣圖擲回並重新建立所有專案。 雖然您可以使用 [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) 來達到相同的結果，但轉譯通常是比複製更昂貴的作業。 這是因為若要改善快取位置，硬體實際上不會將點陣圖儲存為點陣圖所定址的相同記憶體順序。 相反地，點陣圖可能會 swizzled。 驅動程式 (會隱藏 CPU 的 swizzling，因為驅動程式很慢，而且只用于較低的元件) ，或 GPU 上的記憶體管理員。 由於在轉譯時，資料如何寫入轉譯目標的條件約束，因此通常不會 swizzled 轉譯目標，或在您知道永遠不需要轉譯為介面的情況下，以較不理想的方式來 swizzled。 因此， [](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) \* 系統會提供 CopyFrom 方法，將矩形從來源複製到 Direct2D 點陣圖。

CopyFrom 可用於下列三種形式：

-   [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a>在虛線區分上使用磚點陣圖

由於基礎演算法的高品質和精確度，轉譯虛線是非常耗費資源的作業。 對於大部分不涉及直線幾何的案例，使用並排點陣圖可以更快速地產生相同的效果。

## <a name="general-guidelines-for-rendering-complex-static-content"></a>呈現複雜靜態內容的一般指導方針

如果您在框架上轉譯相同的內容框架，則快取內容，特別是當場景很複雜時。

有三種快取技術可供您使用：

-   使用色彩點陣圖的完整場景快取。
-   使用 A8 點陣圖和 [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) 方法的每一基本快取。
-   使用 geometry 實踐的每個基本的快取。

讓我們更詳細地查看每一個。

### <a name="full-scene-caching-using-a-color-bitmap"></a>使用色彩點陣圖的完整場景快取

當您轉譯靜態內容時，在動畫這類案例中，請建立另一個完整色彩點陣圖，而不是直接寫入螢幕點陣圖。 儲存目前的目標、將目標設定為中繼點陣圖，然後轉譯靜態內容。 然後切換回原始的螢幕點陣圖，並在其上繪製中繼點陣圖。

以下為範例：


```C++
// Create a bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_B8G8R8A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &sceneBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render static content to the sceneBitmap.
m_d2dContext->SetTarget(sceneBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Render sceneBitmap to oldTarget.
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->DrawBitmap(sceneBitmap.Get());
```



此範例會使用中繼點陣圖來快取，並在轉譯時切換裝置內容指向的點陣圖。 這樣就不需要針對相同的目的建立相容的轉譯目標。

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a>使用 A8 點陣圖和 FillOpacityMask 方法的每一基本快取

當完整場景不是靜態的，但包含像是靜態的幾何或文字等元素時，您可以使用每個基本的快取技術。 這項技術可保留所快取之基本的消除鋸齒特性，並且可與變更的筆刷類型搭配使用。 它會使用 A8 點陣圖，其中 A8 是一種像素格式，代表8位的 Alpha 色板。 A8 點陣圖適合用來以遮罩的形式繪製幾何/文字。 當您必須操作靜態內容的不透明度，而不是自行操作內容時，您可以轉譯、旋轉、扭曲或調整遮罩的不透明度。

以下為範例：


```C++
// Create an opacity bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render to the opacityBitmap.
m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Call the FillOpacityMask method
// Note: for this call to work correctly the anti alias mode must be D2D1_ANTIALIAS_MODE_ALIASED. 
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->FillOpacityMask(
    opacityBitmap.Get(),
    m_contentBrush().Get(),
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS);
```



## <a name="per-primitive-caching-using-geometry-realizations"></a>使用 geometry 實踐的每個基本快取

另一項依基本的快取技術，稱為 geometry 實踐，可在處理幾何時提供更大的彈性。 當您想要重複繪製別名或防鋸齒型幾何時，將其轉換成幾何實踐並重複繪製實踐，會比重複繪製幾何本身更快速。 幾何實踐通常也會耗用比不透明度遮罩更少的記憶體 (特別是對於大型幾何) 而言，它們對調整的變更較不敏感。 如需詳細資訊，請參閱 [幾何實踐總覽](geometry-realizations-overview.md)。

以下為範例：


```C++
    // Compute a flattening tolerance based on the scales at which the realization will be used.
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(...);

    ComPtr<ID2D1GeometryRealization> geometryRealization;

    // Create realization of the filled interior of the geometry.
    m_d2dDeviceContext1->CreateFilledGeometryRealization(
        geometry.Get(),
        flatteningTolerance,
        &geometryRealization
        );

    // In your app's rendering code, draw the geometry realization with a brush.
    m_d2dDeviceContext1->BeginDraw();
    m_d2dDeviceContext1->DrawGeometryRealization(
        geometryRealization.Get(),
        m_brush.Get()
        );
    m_d2dDeviceContext1->EndDraw();
```



## <a name="geometry-rendering"></a>幾何轉譯

### <a name="use-specific-draw-primitive-over-draw-geometry"></a>針對繪製幾何使用特定的繪圖基本

使用更特定的繪製 *基本* 呼叫，例如透過一般 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)呼叫的 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) 。 這是因為使用 **graphicswindow.drawrectangle** 時，幾何已經是已知的，所以轉譯速度更快。

### <a name="rendering-static-geometry"></a>呈現靜態幾何

在幾何為靜態的案例中，請使用上述的每一基本快取技術。 不透明度遮罩和幾何實踐可以大幅改善包含靜態幾何的場景呈現速度。

### <a name="use-a-multithreaded-device-context"></a>使用多執行緒裝置內容

預期會轉譯大量複雜幾何內容的應用程式，應該考慮在建立 [Direct2D](./direct2d-portal.md)裝置內容時，指定 [**D2D1 \_ 裝置 \_ 內容 \_ 選項來 \_ 啟用 \_ 多 \_ 執行緒 \_ 優化**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options)旗標。 當指定這個旗標時，Direct2D 會將轉譯分佈到系統上所有的邏輯核心，這可能會大幅降低整體轉譯時間。

注意：

-   從 Windows 8.1 起，此旗標只會影響路徑幾何轉譯。 它對僅包含其他基本類型 (例如文字、點陣圖或幾何實踐) 的場景沒有任何影響。
-   在 (軟體中轉譯時，此旗標也不會有任何影響，也就是使用變形 Direct3D 裝置) 轉譯時。 若要控制軟體多執行緒，呼叫端在 \_ \_ \_ \_ \_ \_ 建立變形 DIRECT3D 裝置時，應使用 D3D11 建立裝置防止內部執行緒優化旗標。
-   指定此旗標可能會在轉譯期間增加尖峰工作集，也可能會在已利用多執行緒處理的應用程式中增加執行緒爭用。

## <a name="drawing-text-with-direct2d"></a>使用 Direct2D 繪製文字

Direct2D 文字轉譯功能提供兩個部分。 第一個部分（公開為 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 和 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法）可讓呼叫端傳遞字串和格式化參數，或針對多種格式傳遞 DWrite 文字版面設定物件。 這應該適用于大部分的呼叫端。 轉譯文字（公開為 [**ID2D1RenderTarget：:D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) 方法）的第二種方式，為已經知道要轉譯之圖像位置的客戶提供了點陣化。 下列兩個一般規則可協助改善在 Direct2D 中繪製的文字效能。

### <a name="drawtextlayout-vs-drawtext"></a>DrawTextLayout 與 DrawText 的比較

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))和 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)都可讓應用程式輕鬆地轉譯 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) API 所格式化的文字。 **DrawTextLayout** 會將現有的 [**DWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)物件繪製至 [**RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)， **DrawText** 會根據傳入的參數，為呼叫端建立 DirectWrite 的版面配置。 如果相同的文字必須轉譯多次，請使用 **DrawTextLayout** 而不是 **DrawText**，因為 **DrawText** 會在每次呼叫它時建立版面配置。

### <a name="choosing-the-right-text-rendering-mode"></a>選擇正確的文字呈現模式

將文字消除鋸齒模式設定為明確 [**D2D1 \_ 文字 \_ 消除鋸齒 \_ 模式 \_ 灰階**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) 。 轉譯灰階文字的品質相當於 ClearType，但速度更快。

### <a name="caching"></a>快取

使用完整場景或每個基本點陣圖快取，例如繪製其他基本專案。

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

在 Windows 8 已對層級使用進行許多優化，建議您盡可能嘗試使用層 api，而不是 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 。

### <a name="pushlayer-in-windows-8"></a>Windows 8 中的 PushLayer

[**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)介面衍生自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)介面，也是在 Windows 8 中顯示 Direct2D 內容的關鍵。如需此介面的詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md)內容。 您可以使用裝置內容介面略過呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 方法，然後將 Null 傳遞至 [**ID2D1DeviceCoNtext：:P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) 方法。 Direct2D 會自動管理圖層資源，並可在圖層和效果圖形之間共用資源。

### <a name="axis-aligned-clips"></a>軸對齊的剪輯

如果要裁剪的區域對齊繪圖介面的軸，而不是任意的。 此案例適用于使用剪輯矩形而非圖層。 效能提升比反鋸齒幾何的別名幾何更多。 如需軸對齊剪輯的詳細資訊，請參閱 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 主題。

## <a name="dxgi-interoperability-avoid-frequent-switches"></a>DXGI 互通性：避免頻繁切換

Direct2D 可與 Direct3D 介面無縫交互操作。 這非常適合用來建立可轉譯2D 和3D 內容混合的應用程式。 但在繪製 Direct2D 和 Direct3D 內容之間的每個切換都會影響效能。

當轉譯為 DXGI 介面時，Direct2D 會在轉譯時儲存 Direct3D 裝置的狀態，並在轉譯完成時加以還原。 每次 Direct2D 轉譯批次完成時，這個儲存和還原的成本以及排清所有2D 作業的成本都是付費的，但是 Direct3D 裝置也不會排清。 因此，若要提高效能，請限制 Direct2D 與 Direct3D 之間的轉譯切換數目。

## <a name="know-your-pixel-format"></a>知道您的像素格式

當您建立轉譯目標時，您可以使用 [**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) 結構來指定呈現目標所使用的像素格式和 Alpha 模式。 Alpha 色板是像素格式的一部分，可指定涵蓋範圍值或不透明度資訊。 如果轉譯目標未使用 Alpha 色板，則應該使用 [**D2D1 \_ Alpha \_ 模式 \_ 忽略**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha 模式來建立它。 這會讓您花費在轉譯不需要的 Alpha 通道時所花費的時間。

如需像素格式和 Alpha 模式的詳細資訊，請參閱 [支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)。

## <a name="scene-complexity"></a>場景複雜性

當您在將呈現的場景中分析效能作用點時，瞭解場景是否為填滿速率系結或端點系結，可提供有用的資訊。

-   填滿率：填滿速率是指圖形配接器可轉譯和寫入視訊記憶體的圖元數（以秒為單位）。
-   頂點系結：當場景包含許多複雜幾何時，即為頂點系結。

### <a name="understand-scene-complexity"></a>瞭解場景複雜性

您可以藉由改變轉譯目標的大小來分析場景的複雜度。 如果顯示效能提升的比例減少轉譯目標的大小，則應用程式會有填滿速率的限制。 否則，場景複雜性就是效能瓶頸。

當場景為填滿速率時，減少轉譯目標的大小可改善效能。 這是因為要轉譯的圖元數會隨著轉譯目標的大小而按比例減少。

當場景是頂點系結時，請降低幾何的複雜度。 但請記住，這是以影像品質的費用來完成。 因此，您應該在所需的品質與所需的效能之間做出謹慎的取捨決策。

## <a name="improving-performance-for-direct2d-printing-apps"></a>改善 Direct2D 列印應用程式的效能

[Direct2D](./direct2d-portal.md) 提供與列印的相容性。 您可以傳送相同的 Direct2D 繪圖命令 (格式為 Direct2D 命令清單) 至 Direct2D 列印控制項以進行列印，如果您不知道要繪製的裝置，或如何將繪圖轉譯成列印。

您可以進一步微調其 [Direct2D](./direct2d-portal.md) 列印控制項和 Direct2D 繪圖命令的使用方式，以提供更佳效能的列印結果。

當 [Direct2D](./direct2d-portal.md) print 控制項看到 Direct2D 程式碼模式時，會導致列印品質或效能降低 (例如，本主題稍後所列的程式碼模式) 提醒您可避免效能問題的情況下，會輸出 debug 訊息。 若要查看這些偵錯工具訊息，您需要在程式碼中啟用 [Direct2D Debug 層](direct2ddebuglayer-portal.md) 。 請參閱 [偵錯工具訊息](direct2ddebuglayer-debugmessages.md) ，以取得啟用偵錯工具訊息輸出的指示。

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a>當您建立 D2D 列印控制項時，設定正確的屬性值

當您建立 [Direct2D](./direct2d-portal.md) 列印控制項時，可以設定三個屬性。 其中有兩個屬性會影響 Direct2D 列印控制項處理特定 Direct2D 命令的方式，進而影響整體效能。

-   字型子集模式： [Direct2D](./direct2d-portal.md) 列印控制項會在傳送要列印的頁面之前，在每個頁面中使用這些字型資源。 此模式可減少列印所需的頁面資源大小。 根據頁面上的字型使用方式，您可以選擇不同的字型子集模式來獲得最佳效能。
    -   [**D2D1 \_列印 \_ 字型 \_ 子集 \_ 模式 \_ 預設**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) 會在大部分情況下提供最佳的列印效能。 當設定為此模式時， [Direct2D](./direct2d-portal.md) 列印控制項會使用啟發學習法策略來決定何時要設定字型的子集。
    -   針對具有1或2個頁面的簡短列印工作，建議使用 [**D2D1 \_ 列印 \_ 字型 \_ 子集 \_ 模式 \_ EACHPAGE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) ，其中 [Direct2D](./direct2d-portal.md) 列印控制項會在每個頁面中將字型資源子集及內嵌，然後在頁面列印後捨棄該字型子集。 此選項可確保每個頁面都能在產生後立即列印，但會稍微增加列印 (所需的頁面資源大小（通常是大型字型子集) ）。
    -   針對具有許多文字頁面和小型字型大小的列印工作 (例如使用單一字型) 的100頁面，我們建議 [**D2D1 \_ 列印 \_ 字型 \_ 子集 \_ 模式 \_ NONE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode)，其中 [Direct2D](./direct2d-portal.md) 列印控制項完全不會子集字型資源; 相反地，它會連同首次使用字型的頁面一起送出原始字型資源，然後重新使用字型資源來取得較新的頁面，而不需要重新傳送這些字型資源。
-   點陣 DPI：當 [Direct2D](./direct2d-portal.md) 列印控制項在 DIRECT2D-XPS 轉換期間需要將 Direct2D 命令進行點陣化時，它會使用此 DPI 來進行點陣。 換句話說，如果頁面沒有任何柵格化的內容，則設定任何 DPI 將不會變更效能和品質。 根據頁面上的柵格化使用方式，您可以選擇不同的柵格化 Dpi，以獲得精確度與效能之間的最佳平衡。
    -   如果您在建立 [Direct2D](./direct2d-portal.md) 列印控制項時未指定值，則150是預設值，在大部分情況下，這是列印品質和列印效能的最佳平衡。
    -   較高的 DPI 值通常會產生更佳的列印品質 (如更詳細的保留) 但較低的效能，因為它會產生較大的點陣圖。 我們不建議任何大於300的 DPI 值，因為這不會導致人類眼睛以視覺化方式可感知額外的資訊。
    -   較低的 DPI 可能表示效能較佳，但也可能產生較低的品質。

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a>避免使用特定的 Direct2D 繪製模式

[Direct2D](./direct2d-portal.md)可以用視覺化方式呈現，以及列印子系統可以在整個列印管線中維護和傳輸的內容之間有一些差異。 Direct2D 列印控制項會藉由將逼近或柵格化列印子系統原本不支援的 Direct2D 基本專案，來橋接這些間距。 這類近似值通常會導致列印精確度較低、列印效能較低，或兩者都有。 因此，即使客戶可以針對螢幕和列印轉譯使用相同的繪圖模式，在所有情況下都不是理想的做法。 最好不要盡可能針對列印路徑使用這類 Direct2D 的基本和模式，或者您也可以在圖形化的位置，完全掌控您的品質和柵格化影像的大小。

以下是列印效能和品質不理想的案例清單，而您可能會想要考慮將程式碼路徑改變為最佳列印效能。

-   避免使用 [**D2D1 \_ 基本 \_ blend \_ SOURCEOVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)以外的基本 blend 模式。
-   在繪製非 [**D2D1 \_ 複合 \_ 模式 \_ 來源 \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) 的影像以及 **D2D1 \_ 複合 \_ 模式 \_ 目的地 \_** 時，請避免使用撰寫模式。
-   避免繪製 GDI 中繼檔案。
-   避免將複製來源背景的層級資源 (呼叫 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) ，並將 [**D2D1 \_ layer \_ OPTIONS1 \_ INITIALIZE \_ 從 \_ 背景初始化**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) 為 **D2D1 \_ layer \_ PARAMETERS1** 結構) 。
-   避免使用 D2D1 延伸模式的夾具來建立點陣圖筆刷或影像筆刷 \_ \_ \_ 。 \_ \_ \_ 如果您不在意任何 (（例如）所系結的影像以外的圖元，建議您使用 D2D1 延伸模式鏡像，而附加至筆刷的影像已知大於填滿的目的地區域) 。
-   避免使用 [透視轉換](3d-perspective-transform.md)繪製點陣圖。

### <a name="draw-text-in-a-direct-and-plain-way"></a>以直接且簡單的方式繪製文字

當轉譯文字以顯示，以提升效能及/或更佳的視覺品質時，Direct2D 有數個優化。 但並非所有優化都能改善列印效能和品質，因為紙張列印通常是以更高的 DPI 呈現，而列印並不需要容納動畫等案例。 因此，我們建議您直接繪製原始文字或字元，並在建立要列印的命令清單時，避免下列任何優化。

-   避免使用 [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask) 方法來繪製文字。
-   避免在別名模式中繪製文字。

### <a name="draw-the-original-bitmaps-when-possible"></a>盡可能繪製原始點陣圖

如果目標點陣圖是 JPEG、PNG、TIFF 或 JPEG XR，您可以從磁片檔案或記憶體內資料流程建立 WIC 點陣圖，然後使用 [**ID2D1DeviceCoNtext：： CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))從該 WIC 點陣圖建立 [Direct2D](./direct2d-portal.md)點陣圖，最後直接將該 Direct2D 點陣圖傳遞給 Direct2D 列印控制項，而不需進一步操作。 如此一來，Direct2D 列印控制項就能夠重複使用點陣圖串流，這通常會略過多餘的點陣圖編碼和解碼) ，以更佳的列印效能 (，並在) 時保留點陣圖中的中繼資料（例如色彩設定檔）時，提供更好的列印品質 (。

繪製原始點陣圖可為應用程式提供下列優點。

-   一般情況下， [Direct2D](./direct2d-portal.md) 列印會保留原始資訊 (而不會遺失或雜訊) 直到管線中的延遲為止，特別是當應用程式不知道 (或不想) 知道列印管線的詳細資料時 (像是列印到的印表機、目標印表機的 DPI，以及) 。
-   在許多情況下，延遲點陣圖柵格化表示較佳的效能 (例如，將96DPI 相片列印到600DPI 印表機) 。
-   在某些情況下，傳遞原始影像是接受高精確度 (的唯一方法，例如內嵌色彩設定檔) 。

不過，您無法選擇這樣的優化，因為：

-   藉由查詢印表機資訊和早期的點陣化，您可以完全掌控紙上的最終外觀，來點陣化內容。
-   在某些情況下，早期的點陣化實際上可能會改善應用程式的端對端效能 (例如列印錢包大小的相片) 。
-   在某些情況下，傳遞原始點陣圖需要大幅變更現有的程式碼架構 (例如，影像延遲載入，以及在特定應用程式) 中找到的資源更新路徑。

## <a name="conclusion"></a>結論

雖然 Direct2D 是硬體加速的，且適用于高效能，但您必須正確使用這些功能才能將輸送量最大化。 我們在這裡探討的技巧衍生自研究一般案例，可能不適用於所有應用程式案例。

 

 
