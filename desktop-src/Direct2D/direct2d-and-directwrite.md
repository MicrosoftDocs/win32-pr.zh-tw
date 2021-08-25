---
title: 使用 Direct2D 和 DirectWrite 的文字轉譯
description: 與其他 api （例如 GDI、GDI+ 或 WPF）不同的是，Direct2D 可與另一個 api （DirectWrite）交互操作，以操作和轉譯文字。 本主題說明這些個別元件的優點和互通性。
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd95e7644b5f429d4dd91d2276213d5b7ffb92b058d8e530bfcf47fee77fea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698225"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>使用 Direct2D 和 DirectWrite 的文字轉譯

與其他 api （例如[GDI](/windows/desktop/gdi/windows-gdi)、GDI+ 或 WPF）不同的是， [Direct2D](./direct2d-portal.md)可與另一個 api （ [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)）交互操作，以操作和轉譯文字。 本主題說明這些個別元件的優點和互通性。

本主題包含下列各節。

-   [Direct2D 可進行累加式採用](#direct2d-enables-incremental-adoption)
-   [文字服務與文字轉譯](#text-services-versus-text-rendering)
-   [字型與文字](#glyphs-versus-text)
-   [DirectWrite 和 Direct2D](#directwrite-and-direct2d)
    -   [DrawText](#drawtextlayout)
    -   [DrawTextLayout](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [圖像呈現](#glyph-rendering)
-   [結論](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D 可進行累加式採用

將應用程式從一個圖形 API 移至另一個圖形 API 可能會很困難或不是您想要的各種原因。 這可能是因為您必須支援仍然採用較舊介面的外掛程式，因為應用程式本身太大而無法在一個版本中移植到新的 API，或因為較新 api 的某些部分是理想的，但較舊的 API 在應用程式的其他部分中運作良好。

因為[Direct2D](./direct2d-portal.md)和[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)會實作為個別的元件，所以您可以升級整個2d 圖形系統，或只升級其文字部分。 例如，您可以將應用程式更新為使用 DirectWrite 做為文字，但仍使用[GDI](/windows/desktop/gdi/windows-gdi)或 GDI+ 來呈現。

## <a name="text-services-versus-text-rendering"></a>文字服務與文字轉譯

隨著應用程式的發展，其文字處理需求日益增加。 一開始，文字通常局限于靜態配置的 UI，而且文字是在定義完善的方塊中轉譯，例如按鈕。 當應用程式開始提供大量的語言時，此方法變得更困難，因為翻譯文字的寬度和高度在不同語言之間可能會有很大的差異。 為了進行調整，應用程式開始動態配置 UI 的方式，取決於實際轉譯的文字大小，而不是相反的。

為了協助應用程式完成這項工作， [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)提供 [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)介面。 此 API 可讓應用程式指定具有複雜特性的文字片段，例如不同的字型和字型大小、底線、strikethroughs、雙向文字、效果、省略號，甚至是內嵌的非字元字元 (例如點陣圖圖釋或圖示) 。 然後，應用程式可以變更文字的各種特性，因為它會反復地判斷其 UI 版面配置。 [DirectWrite 的 Hello World 範例](/samples/browse/?redirectedfrom=MSDN-samples)（如下圖所示）和[教學課程：開始使用與 DirectWrite](/windows/desktop/DirectWrite/getting-started-with-directwrite)主題中顯示許多效果。

!["hello world" 範例的螢幕擷取畫面。](images/dwrite-hello-world.png)

版面配置可以根據) WPF 的 (寬度，將字元放在理想的寬度，也可以將字元對齊到最接近的圖元位置 (，因為 [GDI](/windows/desktop/gdi/windows-gdi) 會) 。

除了取得文字度量之外，應用程式也可以點擊測試各部分的文字。 例如，它可能會想要知道文字中的超連結已按一下。  (如需點擊測試的詳細資訊，請參閱 [如何在文字版面配置上執行點擊測試](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) 主題。 ) 

文字版面配置介面會與應用程式所使用的轉譯 API 分離，如下圖所示：

![文字版面配置和圖形 api 圖表。](images/direct2d-directwrite1.png)

這是可能的分隔，因為 DirectWrite 提供轉譯介面 ([**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)) 應用程式可使用您想要的任何圖形 API 來執行轉譯文字。 轉譯文字版面配置時，DirectWrite 會呼叫應用程式實 [**IDWriteTextRenderer：:D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)回呼方法。 這種方法必須負責執行繪圖作業或傳遞它們。

針對繪圖字元， [Direct2D](./direct2d-portal.md)會提供 [**ID2D1RenderTarget：:D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)來繪製至 Direct2D 介面， [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)提供 [**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)來繪製至 gdi 介面，然後使用 gdi 將其傳送至視窗。 簡單地來說，Direct2D 和 DirectWrite 中的 **DrawGlyphRun** 與應用程式在 [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)上執行的 [**DrawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)方法具有完全相容的參數。

遵循類似的分隔、文字特定功能 (例如，字型列舉和管理、圖像分析等等) 是由[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)來處理，而不是[Direct2D](./direct2d-portal.md)。 Direct2D 會直接接受 DirectWrite 物件。 為了協助現有的 GDI 應用程式充分利用 DirectWrite，它會提供 [**IDWriteGdiInterop**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop)方法介面，方法是執行下列動作：

-   從 [GDI](/windows/desktop/gdi/windows-gdi)邏輯字型建立 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)字型 ([**CreateFontFromLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)) 。
-   從 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)字型轉換成 [GDI](/windows/desktop/gdi/windows-gdi)邏輯字型 ([**ConvertFontFaceToLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)) 。
-   從選取至 HDC 的字型中取出[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)字型。  ([**CreateFontFaceFromHdc**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)) 
-   在系統記憶體 ([**CreateBitmapRenderTarget**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)) 中建立 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) [**點陣圖呈現目標**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget)。

## <a name="glyphs-versus-text"></a>字型與文字

文字是一組 Unicode 程式碼點 (字元) ，其中包含各種樣式修飾詞 (字型、權數、底線、strikethroughs，以及在矩形中配置的) 。 相反地，字型是特定字型檔案的特定索引。 圖像會定義一組可以呈現的曲線，但它沒有任何文字意義。 字元和字元之間可能有多對多對應。 來自相同字型且在基準上依序排列的字元序列，稱為 [GlyphRun](/windows/desktop/DirectWrite/glyphs-and-glyph-runs)。 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)和 [Direct2D](./direct2d-portal.md)都會呼叫其最精確的圖像轉譯 API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) ，並且具有非常類似的簽章。 以下是來自 Direct2D 的 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) ：


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



而這個方法是 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)中的 [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) ：


```
STDMETHOD(DrawGlyphRun)(
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        IDWriteRenderingParams* renderingParams,
        COLORREF textColor,
        __out_opt RECT* blackBoxRect = NULL
        ) PURE;
```



[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)版本會保留基準來源、測量模式和圖像執行參數，並包含額外的參數。

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)也可讓您藉由實 [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)介面，為圖像使用自訂轉譯器。 此介面也有 **DrawGlyphRun** 方法，如下列程式碼範例所示。


```
STDMETHOD(DrawGlyphRun)(
        __maybenull void* clientDrawingContext,
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
        __maybenull IUnknown* clientDrawingEffect
        ) PURE;
```



此版本包含更多在您執行 [自訂文字](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer)轉譯器時很有用的參數。 最後一個參數會用於應用程式所執行的自訂繪製效果。  (如需有關用戶端繪製效果的詳細資訊，請參閱 [如何將用戶端繪製效果新增至文字版面](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout)配置。

每個圖像執行會從原點開始，並放在從這個原點開始的行。 圖像會由目前的世界轉換以及相關聯轉譯目標上選取的文字轉譯設定進行變更。 此 API 通常只會由執行其專屬配置的應用程式直接呼叫 (例如，字處理器) 或已執行 [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) 介面的應用程式。

## <a name="directwrite-and-direct2d"></a>DirectWrite 和 Direct2D

[Direct2D](./direct2d-portal.md) 透過 [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)提供圖像層級轉譯服務。 不過，這需要應用程式執行轉譯的詳細資料，這基本上會從 GDI 自行重現 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) API 的功能。

因此， [Direct2D](./direct2d-portal.md) 會提供接受文字而非字元的 Api： [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 和 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))。 這兩種方法都會轉譯為 Direct2D 介面。 若要轉譯成 GDI 介面，請 [**IDWriteBitmapRenderTarget：提供:D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 。 但是，這個方法需要應用程式執行自訂文字轉譯器。  (需詳細資訊，請參閱轉譯 [為 GDI 介面](/windows/desktop/DirectWrite/render-to-a-gdi-surface) 主題。 ) 

應用程式的文字使用方式通常會啟動簡單：例如，在固定配置按鈕上放置 **[確定] 或 [** **取消** ]。 不過，隨著時間的增加，隨著國際化和其他功能的新增，它會變得更複雜。 最後，許多應用程式都必須使用[DirectWrite 的](/windows/desktop/DirectWrite/direct-write-portal)文字版面設定物件，並執行文字轉譯器。

因此， [Direct2D](./direct2d-portal.md) 提供多層式 api，可讓應用程式輕鬆啟動，而不需要再追蹤或放棄其工作程式碼。 簡化的視圖如下圖所示：

![directwrite 和 direct2d 應用程式圖表。](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>DrawText

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 是最簡單的 api 使用方式。 它會採用 Unicode 字串、前景筆刷、單一格式物件和目的地矩形。 它會在版面配置矩形內配置並轉譯整個字串，並選擇性地將其裁剪。 當您在固定配置 UI 中放入一段簡單的文字時，這會很有用。

### <a name="drawtextlayout"></a>DrawTextLayout

藉由建立 [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) 物件，應用程式就可以開始測量和排列文字和其他 UI 專案，並支援多個字型、樣式、底線和 strikethroughs。 [Direct2D](./direct2d-portal.md) 提供的 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) API 可直接接受此物件，並在指定的點轉譯文字。  (寬度和高度是由版面設定物件) 所提供。 除了執行所有預期的文字版面配置功能之外，Direct2D 還會將任何效果物件轉譯為筆刷，並將該筆刷套用至選取的字元範圍。 它也會呼叫任何内嵌物件。 然後，應用程式就可以將非字元字元插入 (圖示，並) 到文字中。 使用文字版面設定物件的另一個優點是，圖像位置會快取在其中。 因此，您可以針對多個繪製呼叫重複使用相同的版面設定物件，以避免重新計算每個呼叫的圖像位置，以大幅提升效能。 這項功能不會出現在 GDI 的 [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))中。

### <a name="drawglyphrun"></a>DrawGlyphRun

最後，應用程式可以執行 [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) 介面本身，並呼叫 [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) 和 [**graphicswindow.fillrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) 本身，或任何其他轉譯 API。 所有與文字版面設定物件的現有互動都會保持不變。

如需如何執行自訂文字轉譯器的範例，請參閱 [使用自訂文字](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) 轉譯器的轉譯主題。

## <a name="glyph-rendering"></a>圖像呈現

將 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)新增至現有的 GDI 應用程式，可讓應用程式使用 [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) API 來轉譯圖像。 DirectWrite 提供的 [**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)方法將以純色呈現給記憶體 DC，而不需要任何額外的 api，例如 [Direct2D](./direct2d-portal.md)。

這可讓應用程式取得 advanced text 轉譯功能，如下所示：

-   子圖元 ClearType 可讓應用程式將字元放在子圖元位置，以允許清晰的圖像呈現和圖像版面配置。
-   Y 方向消除鋸齒讓在較大的圖像上呈現曲線更為順暢。

移至 [Direct2D](./direct2d-portal.md) 的應用程式也會取得下列功能：

-   硬體加速：
-   使用任意 [Direct2D](./direct2d-portal.md) 筆刷（例如星形漸層、線性漸層和點陣圖）填滿文字的功能。
-   更多支援透過 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))、 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 和 [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) api 進行分層和裁剪。
-   支援灰階文字轉譯的能力。 這會根據文字筆刷的不透明度和文字的消除鋸齒，正確地填入目的地 Alpha 通道。

為了有效率地支援硬體加速， [Direct2D](./direct2d-portal.md) 會使用稍微不同的近似值來進行 Gamma 更正，稱為「 *Alpha 更正*」。 這並不需要 Direct2D，就能在轉譯文字時檢查呈現目標色彩圖元。

## <a name="conclusion"></a>結論

本主題說明[Direct2D](./direct2d-portal.md)和[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)之間的差異和相似性，以及提供它們作為個別合作 api 的架構動機。

 

 