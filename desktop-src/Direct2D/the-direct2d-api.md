---
title: Direct2D API 概觀
description: 提供 Direct2D 物件模型的總覽。
ms.assetid: b1362ef6-40fc-4fa5-ba5b-22c622c39f04
keywords:
- Direct2D，關於
- Direct2D、標頭檔
- Direct2D，物件模型
- Direct2D，介面
- ID2D1Factory 介面
- Direct2D，轉譯目標
- 呈現目標，關於
- Direct2D，繪製命令
- 呈現目標，繪製命令
- Direct2D，錯誤處理
- 轉譯目標，錯誤處理
- 錯誤處理
- 筆刷
- 呈現目標，筆刷
- geometries
- Direct2D，幾何
- Direct2D 的點陣圖
- Direct2D，點陣圖
- 原
- Direct2D，基本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f757ea6f1dd2b5db0d0c96297098bc6a8443bf25
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882848"
---
# <a name="direct2d-api-overview"></a>Direct2D API 概觀

Direct2D 會提供類似于 Direct3D 的 API，以搭配 C 或 c + + 使用。 API 會公開各種繪圖相關的功能：

-   使用 Direct2D、Direct3D 或 GDI 轉譯顯示器和螢幕呈現的目標。
-   用於管理繪圖狀態的物件，例如座標空間轉換和消除鋸齒模式。
-   幾何資料的標記法，以及幾何處理的函數。
-   點陣圖、幾何和文字的呈現功能。
-   使用以 GDI 或 Direct3D 建立的圖形內容進行布建。

本主題概要說明組成 Direct2D API 的物件。 它包含下列區段：

-   [Direct2D 標頭檔](#direct2d-header-files)
-   [Direct2D 介面](#direct2d-interfaces)
-   [ID2D1Factory 介面](#the-id2d1factory-interface)
-   [呈現目標](#render-targets)
    -   [呈現目標功能](#render-target-features)
    -   [呈現目標資源](#render-target-resources)
    -   [繪製命令](#drawing-commands)
    -   [錯誤處理](#error-handling)
-   [繪製資源](#drawing-resources)
    -   [筆刷](#brushes)
    -   [幾何](#geometries)
    -   [點陣圖](#bitmaps)
-   [繪製文字](#drawing-text)
-   [Direct2D 基本專案](#direct2d-primitives)
-   [相關主題](#related-topics)

## <a name="direct2d-header-files"></a>Direct2D 標頭檔

Direct2D API 是由下列標頭檔所定義。

| 標頭檔         | 說明                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------|
| d2d1。h              | 定義主要 Direct2D API 的 C 和 c + + 版本。                                                                      |
| d2d1helper。h        | 定義 c + + helper 函數、類別和結構。                                                                       |
| d2dbasetypes。h      | 定義 Direct2D 的繪圖基本專案，例如點和矩形。 此標頭包含在 d2d1 中。                 |
| d2derr。h            | 定義 Direct2D 的錯誤碼。 此標頭包含在 d2d1 中。                                                   |
| d2d1 \_ 1. h           | 定義 Windows 8 和更新版本之主要 Direct2D API 的 C 和 c + + 版本。                                              |
| d2d1 \_ 1helper。h     | 定義 Windows 8 和更新版本的 c + + helper 函數、類別和結構。                                               |
| d2d1effects。h       | 針對 Windows 8 和更新版本的 Direct2D API，定義 C 和 c + + 版本的影像效果部分。                            |
| d2d1effecthelpers。h | 針對 Windows 8 和更新版本，定義 c + + helper 函式、類別和影像效果的結構。 Direct2D API 的一部分。 |



 

若要使用 Direct2D，您的應用程式應該包含 d2d1 .h 標頭檔。

若要編譯 Direct2D 應用程式，請將 d2d1 新增至程式庫清單。 您可以在[Windows 7 的 Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx)中找到 d2d1 .h 和 d2d1。

下列各節說明 Direct2D API 所提供的一些通用介面。

## <a name="direct2d-interfaces"></a>Direct2D 介面

Direct2D API 的根目錄是 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 和 [**ID2D1Resource**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) 介面。 **ID2D1Factory** 物件會建立 **ID2D1Resource** 物件，並作為使用 Direct2D 的起點。 所有其他 Direct2D 物件都是繼承自 **ID2D1Resource** 介面。 Direct2D 資源有兩種類型：與裝置無關的資源和裝置相依的資源。

-   與裝置無關的資源不會與特定的轉譯裝置相關聯，而且可以在應用程式的存留期內保存。
-   與裝置相關的資源會與特定的轉譯裝置相關聯，而且如果移除該裝置，則會停止運作。

 (需有關資源和資源分享的詳細資訊，請參閱 [資源總覽](resources-and-resource-domains.md)。 ) 

## <a name="the-id2d1factory-interface"></a>ID2D1Factory 介面

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)介面是使用 Direct2D 的起點。 您可以使用 **ID2D1Factory** 來具現化 Direct2D 資源。 若要建立 ID2D1Factory，您可以使用其中一個 [**CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) 方法。

Factory 會定義一組可產生下列繪圖資源的建立 *資源* 方法：

-   轉譯目標是轉譯繪製命令的物件。
-   繪製狀態欄塊是儲存繪圖狀態資訊的物件，例如目前的轉換和消除鋸齒模式。
-   幾何是代表簡單且可能複雜之圖形的物件。

Factory 可以建立的其中一個最有用的物件是 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)，如下一節所述。

## <a name="render-targets"></a>呈現目標

轉譯目標是繼承自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 介面的資源。 轉譯目標會建立用來繪製和執行繪圖作業的資源。 有幾種轉譯目標可用於以下列方式呈現圖形：

-   [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 物件會將內容轉譯至視窗。
-   [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) 物件會轉譯成 GDI 裝置內容。
-   點陣圖轉譯目標物件會將內容轉譯為非螢幕點陣圖。
-   DXGI 轉譯目標物件會轉譯成 DXGI 介面，以搭配 Direct3D 使用。

由於轉譯目標是與特定轉譯裝置相關聯，因此它是裝置相依的資源，如果裝置已移除，就會停止運作。

### <a name="render-target-features"></a>呈現目標功能

您可以指定轉譯目標是否應使用硬體加速，以及本機或遠端電腦是否應該呈現遠端顯示器。 您可以設定呈現目標，以進行別名或反鋸齒呈現。 針對具有大量基本專案的轉譯場景，開發人員也可以在別名模式中轉譯2D 圖形，並使用 D3D 多取樣消除鋸齒來達成更高的擴充性。

轉譯目標也可以將繪圖作業分組為 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 介面所代表的圖層。 當轉譯畫面格時，圖層會用來收集要組合在一起的繪圖作業。 在某些案例中，這可能是轉譯成點陣圖轉譯目標的實用替代方式，然後重複使用點陣圖內容，因為階層式配置成本低於 [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)。

轉譯目標可以建立與本身相容的新轉譯目標，這適用于中繼的非畫面轉譯，同時保留原始上設定的各種呈現目標屬性。

您也可以在 Direct2D 轉譯目標上使用 GDI 來轉譯，方法是在 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)的轉譯目標上呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，此方法上具有 [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc)和 [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc)方法，可用來取出 GDI 裝置內容。 只有當轉譯目標是使用 [**D2D1 轉譯 \_ \_ 目標 \_ 使用 \_ GDI \_ 相容**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) 旗標集建立時，才可以透過 gdi 轉譯。 這適用于主要以 Direct2D 轉譯，但具有擴充性模型或其他需要能夠以 GDI 轉譯之舊版內容的應用程式。 如需詳細資訊，請參閱 [Direct2D 和 GDI 互通性總覽](direct2d-and-gdi-interoperation-overview.md)。

### <a name="render-target-resources"></a>呈現目標資源

就像 factory 一樣，轉譯目標可以建立繪圖資源。 轉譯目標所建立的任何資源都是與裝置相關的資源 (就像呈現目標) 一樣。 轉譯目標可建立下列類型的資源：

-   點陣圖
-   筆刷
-   圖層
-   網狀

### <a name="drawing-commands"></a>繪製命令

若要轉譯內容，您可以使用呈現目標繪製方法。 開始繪製之前，請先呼叫 [**ID2D1RenderTarget：： BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法。 完成繪製之後，您會呼叫 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。 在這些呼叫之間，您會使用 Draw 和 Fill 方法來呈現繪圖資源。 大部分的繪圖和填滿方法都採用圖形 (基本或幾何) ，以及用來填滿或大綱圖形的筆刷。

轉譯目標也提供剪下、套用不透明度遮罩，以及轉換座標空間的方法。

Direct2D 使用左方座標系統：正 X 軸的值會繼續往右，y 軸的正值則會往下進行。

### <a name="error-handling"></a>錯誤處理

轉譯目標繪製命令不會指出要求的作業是否成功。 若要找出是否有繪圖錯誤，請呼叫轉譯目標 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法或 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法來取得 **HRESULT**。

## <a name="drawing-resources"></a>繪製資源

下列各節描述可由轉譯目標和 factory 介面建立的一些資源。

### <a name="brushes"></a>筆刷

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)介面所代表的筆刷是由轉譯目標所建立的裝置相依資源，可繪製具有其輸出的區域。 不同的筆刷有不同類型的輸出。 某些筆刷會以純色繪製區域，有些則使用漸層或影像。 Direct2D 提供四種類型的筆刷：

-   [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 以純色繪製區域。
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 會繪製具有線性漸層的區域，以線上條（漸層軸）混合兩個以上的色彩。
-   [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 繪製一個具有放射狀漸層的區域，可在橢圓形周圍混合兩個或多個色彩。
-   [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 會以點陣圖繪製區域。

若要建立筆刷，請使用其中一個 [**ID2D1RenderTarget：：**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)create *&lt; Type &gt;* 筆刷方法，例如 [**CreateRadialGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))。 筆刷可以與轉譯目標繪製和填滿方法搭配使用，以繪製形狀筆觸或外框，或做為不透明度遮罩。

如需筆刷的詳細資訊，請參閱 [筆刷總覽](direct2d-brushes-overview.md)。

### <a name="geometries"></a>幾何

除了基本繪圖基本專案，例如點、矩形和省略號之外，Direct2D 還提供 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 介面來描述簡單和複雜的圖形。 繼承自 **ID2D1Geometry** 的介面會定義不同類型的圖形，例如代表矩形的 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) 、代表圓角矩形的 [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) ，以及代表省略號的 [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) 。

您可以使用 [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) 介面來指定以線條、曲線和弧形組成的一連串圖表，以建立更複雜的圖形。 **ID2D1GeometrySink** 會傳遞至 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)的 Open 方法，以產生複雜的幾何。 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)也可以與 DirectWrite API 搭配使用，以將格式化文字的路徑大綱解壓縮以進行藝術呈現。

Geometry 介面提供的方法可透過擴展或簡化現有的幾何，或產生多個幾何的交集或等位，來操作圖形。 它們也提供方法來判斷幾何是否為交集或重迭、抓取界限資訊、計算幾何的區域或長度，以及沿著幾何插上位置。 Direct2D 也可讓您建立從幾何鑲嵌的三角形網格。

若要建立幾何，請使用其中一個 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)：： create *&lt; &gt; 類型* 幾何方法，例如 [**CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry)。 Geometry 是與裝置無關的資源。

若要呈現幾何，請使用轉譯目標的 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 和 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法。

如需幾何的詳細資訊，請參閱 [幾何總覽](direct2d-geometries-overview.md)。

### <a name="bitmaps"></a>點陣圖

Direct2D 不提供載入或儲存點陣圖的方法;相反地，它可讓您使用[Windows 影像處理元件 (WIC) ](../wic/-wic-about-windows-imaging-codec.md)建立點陣圖。 點陣圖資源可以使用 WIC 載入，然後用來透過 [**ID2D1RenderTarget：： CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap))方法建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。

點陣圖也可以從以其他方式設定的記憶體內部資料中建立。 點陣圖建立之後，就可以由轉譯目標 [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) 方法或點陣圖筆刷繪製。

因為在硬體轉譯目標上建立點陣圖資源通常是昂貴的作業，所以 Direct2D 可以使用 [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)、 [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)和 [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) 方法來更新點陣圖 (或點陣圖) 部分的內容。 使用這些方法可能會節省與其他 GPU 材質配置相關聯的成本。

## <a name="drawing-text"></a>繪製文字

Direct2D 的設計目的是要使用新文字 API 的文字作業，DirectWrite。 為了更簡單地使用 DirectWrite API，轉譯目標提供三種轉譯 DirectWrite 文字資源的方法： [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))、 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)和 [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)。 由於 Direct2D 會使用 GPU 進行 ClearType 文字轉譯程式，因此，Direct2D 提供的 CPU 使用率低於文字作業的 GDI 和更佳的擴充性，因為有更多的 GPU 處理能力可用。

[**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))是針對最簡單的案例所設計，其中包含以最少量的格式轉譯 Unicode 文字字串。 透過 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法可提供更複雜的版面配置和印刷樣式彈性，它會使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件來指定要轉譯的內容和格式。 **IDWriteTextLayout** 可讓您為文字的子字串和其他先進的印刷樣式選項指定個別的格式。

針對需要精確控制圖像層級配置的案例， [**ID2D1RenderTarget：:D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)方法可以搭配 [DirectWrite](../directwrite/direct-write-portal.md)所提供的測量設備使用。

若要使用 DirectWrite API，請包含 dwrite .h 標頭。 如同 Direct2D，DirectWrite 會使用 factory [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)來建立文字物件。 使用 [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory)函式來建立 factory，然後使用其 create 方法來建立 DirectWrite 資源 (例如 [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))) 。

如需 DirectWrite 的詳細資訊，請參閱 DirectWrite 主題的[簡介](../directwrite/introducing-directwrite.md)。

## <a name="direct2d-primitives"></a>Direct2D 基本專案

Direct2D 會定義一組基本類型，類似于其他繪圖 Api 所提供的基本類型。 它會提供色彩結構、用於執行轉換的矩陣結構，以及浮點數和整數版本的點、矩形、橢圓形和大小結構。 通常，您會使用這些結構的浮點版本。

您未使用 factory 或轉譯目標來具現化 Direct2D 基本專案。 您可以直接建立它們，或使用 d2d1helper 中定義的 helper 方法來建立它們。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> <dt>

[DirectWriteHello World 範例](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[DirectWrite 簡介](../directwrite/introducing-directwrite.md)
</dt> <dt>

[資源總覽](resources-and-resource-domains.md)
</dt> <dt>

[Windows 影像處理元件 (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
