---
title: Direct2D 的新功能
description: 以下是一些 Direct2D 新增專案。
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 595a0833e88948585622d79907c81a1465e3fa7b11d1ebc8d6bbd697312509bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430468"
---
# <a name="whats-new-in-direct2d"></a>Direct2D 的新功能

以下是一些 Direct2D 新增專案。

## <a name="whats-new-for-windows-10-creators-update"></a>Windows 10 Creators Update 的新功能

已針對 Windows 10 Creators Update 新增或更新下列功能和 Api。

### <a name="support-for-svg-image-rendering"></a>SVG 影像轉譯的支援

從 Windows 10 Creators Update 開始，Direct2D 提供剖析和繪製 SVG 影像的支援，可讓開發人員轉譯其最愛的向量藝術工具所產生的資產，而不需要先將它們轉換成「光柵影像」。 您可以使用這項功能來改善應用程式內圖示的磁片使用量和規模調整行為，並使用 Direct2d 新的 SVG 物件模型 Api，以程式設計方式變更您的應用程式 SVG。 請注意，Direct2D 僅支援適用于影像的有限 SVG 子集，且不支援所有 SVG 繪圖功能。 如果您需要瀏覽器級 SVG 相容性或 SVG 的 web 導向功能，請考慮改為使用 XAML web 導向 [控制項](/uwp/api/Windows.UI.Xaml.Controls.WebView) 。 如需詳細資訊，請參閱下列主題：

-   [Direct2D SVG 影像呈現範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [SVG 支援](svg-support.md)
-   [**ID2D1DeviceCoNtext5：： CreateSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument) 方法
-   [**ID2D1DeviceCoNtext5：:D rawsvgdocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument) 方法
-   [**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement) 介面

### <a name="improved-support-for-color-management"></a>改善對色彩管理的支援

從 Windows 10 Creators Update 開始，Direct2D 提供改良的色彩管理功能。 開發人員不再需要使用 Direct2d 色彩管理效果的 ICC 設定檔;他們現在可以使用 DXGI 色彩空間，或建立自己的參數化色彩空間定義。 如需詳細資訊，請參閱下列主題：

-   [色彩管理效果](color-management.md)
-   [**ID2D1DeviceCoNtext5::CreateColorCoNtextFromDxgiColorSpace**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceCoNtext5::CreateColorCoNtextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>Windows 10 周年更新的新功能

針對 Windows 10 周年更新新增或更新了下列功能和 api。

### <a name="improved-support-for-color-fonts"></a>改善的色彩字型支援

從 Windows 10 周年更新開始，Direct2D 現在支援轉譯各式各樣的色彩字型格式，可讓開發人員在其 Direct2D 提供的應用程式中使用比以往更多的字型類型。 這包括下列項目的支援：

-   ' COLR ' OpenType 資料表，可在字型中啟用精簡向量內容。 自 Windows 8.1 之後 (支援。 ) 
-   「SVG」 OpenType 資料表，可在字型中啟用 SVG 內容。
-   ' CBDT ' OpenType 資料表，可在字型中啟用色彩點陣圖內容。
-   ' Sbix ' OpenType 資料表，可在字型中啟用色彩點陣圖內容。

啟用 [ [**D2D1 \_ 繪圖 \_ 文字 \_ 選項 \_ 啟用 \_ 色彩 \_ 字型**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) ] 旗標時，Direct2D 會自動支援這些色彩字型格式。 如需詳細資訊，請參閱下列主題：

-   [色彩字型](/windows/desktop/DirectWrite/color-fonts)
-   [DirectWrite 色符號範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>新影像效果

從 Windows 10 周年更新開始，Direct2D 包含 AlphaMask、CrossFade、不透明度和淡色效果。 這項功能先前是由複合、ArithmeticComposite 和 ColorMatrix 效果的特定設定所提供，但新的內建效果可讓您更輕鬆地執行這些一般作業。

## <a name="whats-new-for-windows-10"></a>Windows 10 的新功能

已針對 Windows 10 新增或更新下列功能和 Api。

### <a name="sprite-batches"></a>Sprite 批次

從 Windows 10 開始，Direct2D 會提供建立和呈現 sprite 批次的支援。 相較于一般用途的 [**DrawImage**](id2d1devicecontext-drawimage-overload.md) 方法，sprite 批次批次產生的每個映射 CPU 額外負荷極少。 這讓它們適合涉及數百或數千個並行影像的案例，例如遊戲 sprite 或物件系統。 如需詳細資訊，請參閱下列主題：

-   [**ID2D1DeviceCoNtext3：： CreateSpriteBatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch) 方法
-   [**ID2D1DeviceCoNtext3：:D rawspritebatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options)) 方法
-   [**ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch) 介面

### <a name="gradient-meshes"></a>漸層網格

從 Windows 10 開始，Direct2D 會為漸層網格提供新的基本。 漸層網格通常是由圖形設計軟體中的專業 illustrators 所使用，而且可讓演出者轉譯複雜的 (甚至是相片真實的) 彩色圖形，以及向量的所有記憶體和擴充性優點。 如需詳細資訊，請參閱下列主題：

-   [Direct2D 漸層網格範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2D1 \_梯度 \_ 網格 \_ 修補程式**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) 結構
-   [**ID2D1DeviceCoNtext2：:D rawgradientmesh**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh) 方法

### <a name="improved-image-loading-apis"></a>改良的影像載入 Api

從 Windows 10 開始，Direct2D 提供了新的 API，可用於載入影像 ID2D1ImageSource。 映射來源可在現有的映射載入 Api （包括 CreateBitmapFromWicBitmap、點陣圖來源效果和 YCbCr 效果）時改善。 Direct2D 映射來源結合了這些 Api 的功能，可支援任意大型影像、輕鬆整合列印和效果，以及許多優化，包括 YCbCr JPEG 和編制索引的 JPEG。 如需詳細資訊，請參閱下列主題：

-   [Direct2D 相片調整 SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [IWICJpegFrameDecode::SetIndexing](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>改進筆墨轉譯的支援

從 Windows 10 開始，Direct2D 會提供新的基本型別來代表筆墨筆劃。 Direct2D 筆墨筆觸是由貝茲曲線定義、支援不同的鋼筆圖案和轉換，而且可能具有固定或變動的粗細。 Direct2d 筆墨筆觸的內建支援，可讓應用程式輕鬆地轉譯比先前的方法更快、更美觀的筆墨，通常需要應用程式來管理筆墨本身，作為一系列的省略號和 quadrilaterals。 如需詳細資訊，請參閱下列主題：

-   [**ID2D1Ink 介面**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**ID2D1DeviceCoNtext2：:D rawInk 方法**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**ID2D1InkStyle 介面**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>效果著色器連結

Direct2D 效果會使用 HLSL 圖元、頂點和/或計算著色器來執行。 從 Windows 10 開始，Direct2D 現在會自動分析效果圖形，讓您有機會結合和執行個別著色器。 這可能會大幅增加效果輸送量。 內建效果的取用者不需要執行任何動作來受益于效果著色器連結，但是建立自己自訂效果的開發人員應該遵循可利用效果著色器連結的更新最佳作法。 如需詳細資訊，請參閱下列主題：

-   [效果著色器連結](effect-shader-linking.md)
-   [Direct2D HLSL 協助程式](hlsl-helpers.md)
-   [Direct2D 自訂效果 SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

效果著色器連結的設計目的是不影響視覺效果的視覺效果輸出。 不過，這不一定是因為效果有效位數和數位裁剪的特定行為。 如需如何控制這些行為的詳細資訊，請參閱：

-   [控制效果圖形中的有效位數和數位裁剪](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>新的內建效果

從 Windows 10 開始，Direct2D 包含一組豐富的新內建效果，可解決頂尖的開發人員要求，並啟用新的視覺案例類型。 新的效果如下：

### <a name="color"></a>色彩：

-   [RGB 到色調效果](rgb-to-hue-effect.md)
-   [色調至 RGB 效果](hue-to-rgb-effect.md)
-   [3D 查閱資料表效果](3d-lookup-table-effect.md)

### <a name="photo"></a>照片：

-   [對比效果](contrast-effect.md)
-   [曝光效果](exposure-effect.md)
-   [灰階效果](grayscale-effect.md)
-   [醒目顯示和陰影效果](highlights-and-shadows-effect.md)
-   [反轉效果](invert-effect.md)
-   [棕褐色效果](sepia-effect.md)
-   [銳化效果](sharpen-effect.md)
-   [伸直效果](straighten-effect.md)
-   [溫度和色調效果](temperature-and-tint-effect.md)
-   [Vignette 效果](vignette-effect.md)

### <a name="filter"></a>篩選：

-   [Edge 偵測效果](edge-detection-effect.md)

### <a name="stylize"></a>風格

-   [浮凸效果](emboss-effect.md)
-   [色調影響](posterize-effect.md)

### <a name="transparency"></a>透明度：

-   [色度鍵效果](chromakey-effect.md)

[Direct2D 相片調整 SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)中示範了伸直、飽和度、對比、反白顯示和遮蔽，以及溫度和色調效果。

## <a name="whats-new-for-windows-81"></a>Windows 8.1 的新功能

已針對 Windows 8.1 新增或更新下列功能和 Api。

從 Windows 8.1 開始，Direct2D 是建置於 Direct3D 11.2 之上。

### <a name="geometry-realizations"></a>幾何實踐

從 Windows 8.1 開始，Direct2D 提供 geometry 實踐。 幾何實踐可讓應用程式在某些情況下改善幾何轉譯效能，而不會有一些將幾何柵格化到點陣圖的缺點。 如需詳細資訊，請參閱下列主題：

-   [**ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1) 介面
-   [**ID2D1DeviceCoNtext1：:D rawgeometryrealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) 方法

### <a name="support-for-jpeg-ycbcr-images"></a>支援 JPEG YCbCr 影像

從 Windows 8.1 開始，Direct2D 提供以 JPEG Y'CbCr 格式轉譯影像資料的支援。 應用程式可以在其原生 Y'CbCr 標記法中轉譯 JPEG 內容，而不是解壓縮至 BGRA。 這可大幅減少圖形記憶體耗用量和資源建立時間。 如需詳細資訊，請參閱下列主題：

-   Direct2D [YCbCr 效果](ycbcr-effect.md)
-   [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) 介面

### <a name="support-for-block-compressed-formats-dds-files"></a>支援 (DDS 檔案的區塊壓縮格式) 

從 Windows 8.1 開始，Direct2D 支援包含 DXGI 格式的點陣圖 \_ \_ BC1 \_ UNORM、dxgi \_ 格式 \_ BC2 \_ UNORM 和 dxgi \_ 格式 \_ BC3 \_ UNORM 圖元資料。 應用程式可將其影像資產取代為區塊壓縮的 DDS 映射。 這可大幅減少圖形記憶體耗用量和資源建立時間。 如需詳細資訊，請參閱下列主題：

-   [**ID2D1DeviceCoNtext：： CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) 方法
-   [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode) 介面

### <a name="rendering-priority"></a>轉譯優先權

從 Windows 8.1 開始，Direct2D 會提供對每個裝置轉譯優先權的支援。 這項新功能可讓應用程式在一般轉譯優先順序之間切換裝置 (預設) 和低轉譯優先順序 (，裝置將不會在系統) 上封鎖其他轉譯工作。 建議應用程式對使用者回應性不重要的工作使用低轉譯優先順序，例如預先轉譯的內容、最小化的轉譯，以及通常在背景中執行的其他作業。 如需詳細資訊，請參閱下列主題：

-   [**ID2D1Device1：： SetRenderingPriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority) 方法
-   [**D2D1 \_轉譯 \_ 優先權**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority) 列舉

## <a name="whats-new-for-windows-8"></a>Windows 8 的新功能

已針對 Windows 8 新增或更新下列功能和 Api。

已安裝[Windows 7 的平臺更新](/windows/desktop/direct3darticles/platform-update-for-windows-7)Windows 7 支援新的 Direct2D 介面。

裝置和裝置內容的 direct2d 語義已更新為更接近 Direct3D 所使用的語法，並可在 Windows 存放區應用程式上提供精確的操作。 如需詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md) 內容。

選取的相關 Api：

-   [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

命令清單 API 可讓您在螢幕轉譯和列印時共用轉譯路徑。 它也可讓您使用基本專案來建立用來填滿基本專案的影像筆刷。

選取的相關 Api：

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

[Direct2D 效果](effects-overview.md)是一組 api，Windows 8 的新功能，可將高品質效果套用至影像。 它也包含可讓您自行自訂效果的 Api。

選取的相關 Api：

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectCoNtext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

從 Windows 8 開始，Direct2D 包含用於建立多執行緒應用程式的其他 api。 如需詳細資訊，請參閱多 [執行緒 Direct2D 應用程式](multi-threaded-direct2d-apps.md) 。

選取的相關 Api：

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**D2D1 \_ FACTORY \_ 類型 \_ 多 \_ 執行緒**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 