---
description: 從 Windows 8.1 開始，Windows 影像處理元件 (WIC) JPEG 編解碼器可支援在其原生 YCbCr 表單中讀取和寫入影像資料。
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: JPEG YCbCr 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f8548a458f70265d248e1d686ad3bc300d7cfee2bc1e0ab2262ee652f0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086774"
---
# <a name="jpeg-ycbcr-support"></a>JPEG YCbCr 支援

從 Windows 8.1 開始， [Windows 影像處理元件 (WIC) ](-wic-about-windows-imaging-codec.md) JPEG 編解碼器可支援在其原生 YC<sub>b</sub>C<sub>r</sub>表單中讀取和寫入影像資料。 WIC YC<sub>b</sub>C<sub>r</sub> 支援可以搭配 [Direct2D](../direct2d/direct2d-portal.md) 使用，以呈現具有影像效果的 YC<sub>b</sub>C<sub>r</sub> 圖元資料。 此外，WIC JPEG 編解碼器也可以透過媒體基礎使用特定相機驅動程式所產生的 YC<sub>b</sub>C<sub>r</sub> 圖元資料。

YC<sub>b</sub>C<sub>r</sub> 圖元資料耗用的記憶體明顯小於標準 BGRA 像素格式。 此外，存取 YC<sub>b</sub>C<sub>r</sub> 資料可讓您將 JPEG 解碼/編碼管線的一些階段卸載至 Direct2D，也就是 GPU 加速。 藉由使用 YC<sub>b</sub>C<sub>r</sub>，您的應用程式可以減少相同大小和品質影像的 JPEG 記憶體耗用量和載入時間。 或者，您的應用程式可以使用更高解析度的 JPEG 影像，而不會受到效能的影響。

本主題說明 YC<sub>b</sub>C<sub>r</sub> 資料的運作方式，以及如何在 WIC 和 Direct2D 中使用它。

-   [關於 JPEG YC<sub>b</sub>C<sub>r</sub> 資料](#about-jpeg-ycbcr-data)
    -   [YC<sub>b</sub>C<sub>r</sub> 色彩模型](#ycbcr-color-model)
    -   [平面與交錯記憶體版面配置](#planar-versus-interleaved-memory-layouts)
    -   [色度次取樣](#chroma-subsampling)
    -   [YC<sub>b</sub>C<sub>r</sub>的 JPEG 用法](#jpeg-usage-of-ycbcr)
-   [使用 JPEG YC<sub>b</sub>C<sub>r</sub> 資料](#using-jpeg-ycbcr-data)
    -   [使用 YC<sub>b</sub>C<sub>r</sub> JPEG 影像](#using-ycbcr-jpeg-images)
    -   [Windows映射處理元件 Api](#windows-imaging-component-apis)
    -   [Direct2D Api](#direct2d-apis)
    -   [判斷是否支援 YC<sub>b</sub>C<sub>r</sub> 設定](#determining-if-the-ycbcr-configuration-is-supported)
    -   [解碼 YC<sub>b</sub>C<sub>r</sub> 圖元資料](#decoding-ycbcr-pixel-data)
    -   [轉換 YC<sub>b</sub>C<sub>r</sub> 圖元資料](#transforming-ycbcr-pixel-data)
    -   [編碼 YC<sub>b</sub>C<sub>r</sub> 圖元資料](#encoding-ycbcr-pixel-data)
    -   [解碼 Windows 10 中的 YC<sub>b</sub>C<sub>r</sub>圖元資料](#decoding-ycbcr-pixel-data-in-windows-10)
-   [相關主題](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>關於 JPEG YC<sub>b</sub>C<sub>r</sub> 資料

本節將說明一些重要概念，以瞭解 WIC 中的 YC<sub>b</sub>C<sub>r</sub> 支援如何運作及其主要優點。

### <a name="ycsubbsubcsubrsub-color-model"></a>YC<sub>b</sub>C<sub>r</sub> 色彩模型

Windows 8 和較早版本中的 WIC 支援四種不同的[色彩模型](-wic-codec-native-pixel-formats.md)，最常見的是 RGB/BGR。 此色彩模型使用紅色、綠色和藍色元件定義色彩資料;也可以使用第四個 Alpha 元件。

以下是分解成紅色、綠色和藍色元件的影像。

![分解成紅色、綠色和藍色元件的影像。](graphics/ycbcr1.png)

YC<sub>b</sub>C<sub>r</sub> 是一種替代色彩模型，會使用亮度元件定義色彩資料 (Y) 和兩個色度元件 (c<sub>b</sub> 和 c<sub>r</sub>) 。 它通常用於數位影像處理和影片案例中。 YC<sub>b</sub>C<sub>r</sub> 的詞彙通常會與 YUV 交替使用，雖然這兩個技術在技術上不同。

YC<sub>b</sub>C<sub>r</sub> 有幾種變化，不同之處在于色彩空間和動態範圍定義– WIC 特別支援 JPEG JFIF YC<sub>b</sub>C<sub>r</sub> 資料。 如需詳細資訊，請參閱 [JPEG Itu-t T81 規格](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)。

以下是在其 Y、C<sub>b</sub>和 c<sub>r</sub> 元件中分解的影像。

![分解為其 y、cb 和 cr 元件的影像。](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>平面與交錯記憶體版面配置

本節說明在記憶體中存取和儲存 RGB 圖元資料與 YC<sub>b</sub>C<sub>r</sub> 資料之間的一些差異。

RGB 圖元資料通常是使用交錯記憶體配置儲存。 這表示單一色彩元件的資料會在圖元之間交錯，且每個圖元會連續儲存在記憶體中。

以下圖顯示以交錯式記憶體配置儲存的 RGBA 圖元資料。

![此圖顯示以交錯式記憶體配置儲存的 rgba 圖元資料。](graphics/ycbcr3.png)

YC<sub>b</sub>C<sub>r</sub> 資料通常會使用平面記憶體配置儲存。 這表示每個色彩元件會分別儲存在其本身的連續平面中，總共三個平面。 在另一個常見的設定中，C<sub>b</sub> 和 c<sub>r</sub> 元件會交錯並儲存在一起，而 Y 元件會保留在自己的平面中，總共兩個平面。

以下顯示平面 Y 和交錯<sub>式 c</sub><sub>r</sub>圖元資料的圖表，這是常見的 YC<sub>b</sub>c<sub>r</sub>記憶體配置。

![顯示平面 y 和交錯 cbcr 圖元資料的圖表，這是常見的 ycbcr 記憶體配置。](graphics/ycbcr4.png)

在 WIC 和 Direct2D 中，會將每個色彩平面視為其本身的相異物件 ([IWICBitmapSource](-wic-imp-iwicbitmapsource.md) 或 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)) ，而且這些平面會形成 YC <sub>b</sub>C <sub>r</sub> 影像的支援資料。

雖然 WIC 支援在2和3平面設定中存取 YC<sub>b</sub>C<sub>r</sub> 資料，但 Direct2D 只支援先前的 (Y 和 c<sub>b</sub>c<sub>r</sub>) 。 因此，當搭配使用 WIC 和 Direct2D 時，您應該一律使用2個平面 YC<sub>b</sub>C<sub>r</sub> 設定。

### <a name="chroma-subsampling"></a>色度次取樣

YC<sub>b</sub>C<sub>r</sub> 色彩模型非常適合數位影像案例，因為它可以利用人類視覺系統的特定層面。 尤其是，人類對影像的亮度 (亮度) 的變化更敏感，且色度 (色彩) 較不敏感。 藉由將色彩資料分割成不同的亮度和色度元件，我們可以選擇性地壓縮色度元件，以在品質降到最短的情況下節省空間。

執行這項操作的其中一種技術稱為「色度次取樣」。 C<sub>b</sub> 和 c<sub>r</sub> 平面是在一或兩個水準和垂直維度中 subsampled (downscaled) 。 基於歷史原因，每個色度的取樣模式通常是使用三個部分 J:a： b 的比率。



| 次取樣模式 | 水準縮小 | 垂直縮小 | 每圖元的位數\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1 倍                   | 1 倍                 | 24               |
| 4:2:2            | 2x                   | 1 倍                 | 16               |
| 4:4:0            | 1 倍                   | 2x                 | 16               |
| 4:2:0            | 2x                   | 2x                 | 12               |



 

\* 包含 Y 資料。

從上表中，如果您使用 YC<sub>b</sub>C<sub>r</sub> 來儲存未壓縮的影像資料，您可以將記憶體節省25% 到62.5%，而每圖元 RGBA 資料可節省25% 到32位，視使用的色度次取樣模式而定。

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>YC<sub>b</sub>C<sub>r</sub>的 JPEG 用法

概括而言，JPEG 解壓縮管線包含下列階段：

1.  執行熵 (例如 Huffman) 解壓縮
2.  執行 dequantization
3.  執行反向離散余弦轉換
4.  在 C<sub>b</sub>c<sub>r</sub> 資料上執行色度 upsampling
5.  視需要將 YC<sub>b</sub>C<sub>r</sub> 資料轉換成 RGBA () 

藉由讓 JPEG 編解碼器產生 YC<sub>b</sub>C<sub>r</sub> 資料，我們可以避免解碼程式的最後兩個步驟，或將它們延遲到 GPU。 除了上一節所列的記憶體節省之外，這可大幅減少將映射解碼所需的整體時間。 在編碼 YC<sub>b</sub>C<sub>r</sub> 資料時也適用相同的節省量。

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>使用 JPEG YC<sub>b</sub>C<sub>r</sub> 資料

本節說明如何使用 WIC 和 Direct2D 來操作 YC<sub>b</sub>C<sub>r</sub> 資料。

若要查看實務中所使用之檔的指導方針，請參閱 [Direct2D 和 WIC 範例中的 JPEG YCbCr 優化](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) ，其中示範在 Direct2D 應用程式中解碼和轉譯 YC<sub>b</sub>C<sub>r</sub> 內容所需的所有步驟。

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>使用 YC<sub>b</sub>C<sub>r</sub> JPEG 影像

大部分的 JPEG 影像都會儲存為 YC<sub>b</sub>C<sub>r</sub>。 某些 Jpeg 包含 CMYK 或灰階資料，而且不會使用 YC<sub>b</sub>C<sub>r</sub>。 這表示您通常（但不一定）可以直接使用既有的 JPEG 內容，而不需要任何修改。

WIC 和 Direct2D 不支援每個可能的 YC<sub>b</sub>C<sub>r</sub> 設定，而 Direct2D 中的 YC<sub>b</sub>c<sub>r</sub> 支援取決於基礎圖形硬體和驅動程式。 基於這個原因，一般用途的影像處理管線必須健全于未使用 YC<sub>b</sub>c<sub>r</sub> (包括其他常見的影像格式，例如 PNG 或 BMP) ，或無法使用 YC<sub>b</sub>C<sub>r</sub> 支援的情況。 建議您保留現有的 BGRA 型映射管線，並啟用 YC<sub>b</sub>C<sub>r</sub> 作為效能優化（如果有的話）。

### <a name="windows-imaging-component-apis"></a>Windows映射處理元件 Api

Windows 8.1 中的 WIC 會新增三個新介面，以提供對 JPEG YC<sub>b</sub>C<sub>r</sub>資料的存取。

### <a name="iwicplanarbitmapsourcetransform"></a>IWICPlanarBitmapSourceTransform

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) 類似于 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)，不同之處在于它會在平面設定中產生圖元，包括 YC <sub>b</sub>C <sub>r</sub> 資料。 您可以藉由在支援平面存取的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 執行上呼叫 QueryInterface 來取得這個介面。 這包括 JPEG 編解碼器對 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 以及 [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)、 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)和 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)的實作為。

### <a name="iwicplanarbitmapframeencode"></a>IWICPlanarBitmapFrameEncode

[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) 提供編碼平面圖元資料的功能，包括 YC <sub>b</sub>C <sub>r</sub> 資料。 您可以藉由呼叫 [**IWICBITMAPFRAMEENCODE**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)JPEG 編解碼器的 QueryInterface 來取得這個介面。

### <a name="iwicplanarformatconverter"></a>IWICPlanarFormatConverter

[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) 可讓 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) 取用平面圖元資料（包括 YC <sub>b</sub>C <sub>r</sub>），並將它轉換成交錯的像素格式。 它不會公開將交錯圖元資料轉換成平面格式的能力。 您可以藉由在提供的 **IWICFormatConverter** 執行 Windows 上呼叫 QueryInterface 來取得這個介面。

### <a name="direct2d-apis"></a>Direct2D Api

Windows 8.1 中的 Direct2D 支援 YC<sub>b</sub>c<sub>r</sub>平面圖元資料（具有新的 YC<sub>b</sub>c<sub>r</sub>影像效果）。 此效果提供轉譯 YC<sub>b</sub>C<sub>r</sub> 資料的能力。 效果會採用輸入兩個 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 介面：一個是以 dxgi 格式 R8 UNORM 格式來包含平面 Y 資料 \_ \_ \_ ，另一個則包含 dxgi \_ 格式 \_ R8G8 UNORM 格式的交錯 CbCr 資料 \_ 。 您通常會使用此效果來取代可能包含 BGRA 圖元資料的 **ID2D1Bitmap** 。

YC<sub>b</sub>c<sub>r</sub>影像效果的目的是要搭配可提供 YC<sub>b</sub>c<sub>r</sub>資料的 WIC YC<sub>b</sub>c<sub>r</sub> api 一起使用。 這可有效地將部分解碼工作從 CPU 卸載至 GPU，以便更快速且平行處理。

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>判斷是否支援 YC<sub>b</sub>C<sub>r</sub> 設定

如先前所述，您的應用程式應該很健全，以 YC<sub>b</sub>C<sub>r</sub> 支援無法使用的情況。 本節討論您的應用程式應該檢查的條件。 如果下列任何一項檢查失敗，您的應用程式應該會切換回標準的 BGRA 型管線。

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>WIC 元件是否支援 YC<sub>b</sub>C<sub>r</sub> 資料存取？

只有 Windows 提供的 JPEG 編解碼器和某些 WIC 轉換支援 YC<sub>b</sub>C<sub>r</sub>資料存取。 如需完整清單，請參閱[Windows 影像處理元件 api](#windows-imaging-component-apis)一節。

若要取得其中一個平面 YC<sub>b</sub>C<sub>r</sub> 介面，請呼叫原始介面上的 QueryInterface。 如果元件不支援 YC<sub>b</sub>C<sub>r</sub> 資料存取，這將會失敗。

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>要求的 WIC 轉換是否支援 YC<sub>b</sub>C<sub>r</sub>？

取得 [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)之後，您應該先呼叫 [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform)。 這個方法會將您想要套用至平面 YC<sub>b</sub>C<sub>r</sub> 資料的一組完整轉換做為輸入參數，並傳回指出支援的布林值，以及最接近可傳回之要求大小的維度。 使用 [**IWICPlanarBitmapSourceTransform：： CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels)存取圖元資料之前，您應該先檢查這三個值。

此模式類似于 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 的使用方式。

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>圖形驅動程式是否支援搭配 Direct2D 使用 YC<sub>b</sub>C<sub>r</sub> 所需的功能？

只有當您使用 Direct2D YC<sub>b</sub>c<sub>r</sub> 效果轉譯 YC<sub>b</sub>c<sub>r</sub> 內容時，才需要進行這項檢查。 Direct2D 會使用<sub></sub>dxgi<sub> </sub> \_ 格式 \_ R8 \_ UNORM 和 dxgi \_ 格式 \_ R8G8 \_ UNORM 像素格式（無法從所有圖形驅動程式使用）儲存 YC b C r 資料。

使用 YC <sub>b</sub>C <sub>r</sub> 映射效果之前，您應該呼叫 [**ID2D1DeviceCoNtext：： IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) ，以確定驅動程式支援兩種格式。

### <a name="sample-code"></a>範例程式碼

以下是示範建議的檢查的程式碼範例。 此範例取自 [Direct2D 和 WIC 範例中的 JPEG YCbCr 優化](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)。


```C++
bool DirectXSampleRenderer::DoesWicSupportRequestedYCbCr()
{
    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    HRESULT hr = m_wicScaler.As(&wicPlanarSource);
    if (SUCCEEDED(hr))
    {
        BOOL isTransformSupported;
        uint32 supportedWidth = m_cachedBitmapPixelWidth;
        uint32 supportedHeight = m_cachedBitmapPixelHeight;
        DX::ThrowIfFailed(
            wicPlanarSource->DoesSupportTransform(
                &supportedWidth,
                &supportedHeight,
                WICBitmapTransformRotate0,
                WICPlanarOptionsDefault,
                SampleConstants::WicYCbCrFormats,
                m_planeDescriptions,
                SampleConstants::NumPlanes,
                &isTransformSupported
                )
            );

        // The returned width and height may be larger if IWICPlanarBitmapSourceTransform does not
        // exactly support what is requested.
        if ((isTransformSupported == TRUE) &&
            (supportedWidth == m_cachedBitmapPixelWidth) &&
            (supportedHeight == m_cachedBitmapPixelHeight))
        {
            return true;
        }
    }

    return false;
}

bool DirectXSampleRenderer::DoesDriverSupportYCbCr()
{
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    return (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8_UNORM)) &&
        (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8G8_UNORM));
}
```



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>解碼 YC<sub>b</sub>C<sub>r</sub> 圖元資料

如果您想要取得 YC <sub>b</sub>C <sub>r</sub> 圖元資料，您應該呼叫 [**IWICPlanarBitmapSourceTransform：： CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels)。 這個方法會將圖元資料複製到已填滿 [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) 結構的陣列中，您想要 (例如 Y 和 c <sub>b</sub>c <sub>r</sub>) 的每個資料平面都有一個。 **WICBitmapPlane** 包含圖元資料的相關資訊，並指向將接收資料的記憶體緩衝區。

如果您想要使用 YC <sub>b</sub>C <sub>r</sub>圖元資料搭配其他 WIC api，您應該建立適當設定的 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)、呼叫 [**鎖定**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock)以取得基礎記憶體緩衝區，並將緩衝區與用來接收 YC <sub>b</sub>C <sub>r</sub>圖元資料的 [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane)產生關聯。 然後，您就可以正常使用 [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) 。

最後，如果您想要在 Direct2D 中轉譯 YC <sub>b</sub>c <sub>r</sub>資料，您應該從每個 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)建立 [**ID2D1BITMAP**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ，並使用它們做為 YC <sub>b</sub>C <sub>r</sub>影像效果的來源。 WIC 可讓您要求多個平面設定。 與 Direct2D 交互操作時，您應該要求兩個平面，一個使用 GUID WICPixelFormat8bppY，另一個使用 \_ guid \_ WICPixelFormat16bppCbCr，因為這是 Direct2D 所預期的設定。

### <a name="code-sample"></a>程式碼範例

以下程式碼範例示範在 Direct2D 中解碼和轉譯 YC<sub>b</sub>C<sub>r</sub> 資料的步驟。 此範例取自 [Direct2D 和 WIC 範例中的 JPEG YCbCr 優化](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)。


```C++
void DirectXSampleRenderer::CreateYCbCrDeviceResources()
{
    auto wicFactory = m_deviceResources->GetWicImagingFactory();
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    DX::ThrowIfFailed(
        m_wicScaler.As(&wicPlanarSource)
        );

    ComPtr<IWICBitmap> bitmaps[SampleConstants::NumPlanes];
    ComPtr<IWICBitmapLock> locks[SampleConstants::NumPlanes];
    WICBitmapPlane planes[SampleConstants::NumPlanes];

    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        DX::ThrowIfFailed(
            wicFactory->CreateBitmap(
                m_planeDescriptions[i].Width,
                m_planeDescriptions[i].Height,
                m_planeDescriptions[i].Format,
                WICBitmapCacheOnLoad,
                &bitmaps[i]
                )
            );

        LockBitmap(bitmaps[i].Get(), WICBitmapLockWrite, nullptr, &locks[i], &planes[i]);
    }

    DX::ThrowIfFailed(
        wicPlanarSource->CopyPixels(
            nullptr, // Copy the entire source region.
            m_cachedBitmapPixelWidth,
            m_cachedBitmapPixelHeight,
            WICBitmapTransformRotate0,
            WICPlanarOptionsDefault,
            planes,
            SampleConstants::NumPlanes
            )
        );

    DX::ThrowIfFailed(d2dContext->CreateEffect(CLSID_D2D1YCbCr, &m_d2dYCbCrEffect));

    ComPtr<ID2D1Bitmap1> d2dBitmaps[SampleConstants::NumPlanes];
    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        // IWICBitmapLock must be released before using the IWICBitmap.
        locks[i] = nullptr;

        // First ID2D1Bitmap1 is DXGI_FORMAT_R8 (Y), second is DXGI_FORMAT_R8G8 (CbCr).
        DX::ThrowIfFailed(d2dContext->CreateBitmapFromWicBitmap(bitmaps[i].Get(), &d2dBitmaps[i]));
        m_d2dYCbCrEffect->SetInput(i, d2dBitmaps[i].Get());
    }
}

void DirectXSampleRenderer::LockBitmap(
    _In_ IWICBitmap *pBitmap,
    DWORD bitmapLockFlags,
    _In_opt_ const WICRect *prcSource,
    _Outptr_ IWICBitmapLock **ppBitmapLock,
    _Out_ WICBitmapPlane *pPlane
    )
{
    // ComPtr guarantees the IWICBitmapLock is released if an exception is thrown.
    ComPtr<IWICBitmapLock> lock;
    DX::ThrowIfFailed(pBitmap->Lock(prcSource, bitmapLockFlags, &lock));
    DX::ThrowIfFailed(lock->GetStride(&pPlane->cbStride));
    DX::ThrowIfFailed(lock->GetDataPointer(&pPlane->cbBufferSize, &pPlane->pbBuffer));
    DX::ThrowIfFailed(lock->GetPixelFormat(&pPlane->Format));
    *ppBitmapLock = lock.Detach();
}
```



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>轉換 YC<sub>b</sub>C<sub>r</sub> 圖元資料

轉換 YC <sub>b</sub>C <sub>r</sub> 資料與解碼幾乎完全相同，因為兩者都牽涉到 [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)。 唯一的差別是您取得介面的 WIC 物件。 Windows 提供的 scaler、翻轉旋轉旋轉和色彩轉換全都支援 YC<sub>b</sub>C<sub>r</sub>存取。

### <a name="chaining-transforms-together"></a>將轉換連結在一起

WIC 支援將多個轉換連結在一起的概念。 例如，您可以建立下列 WIC 管線：

![從 jpeg 解碼器開始的 wic 管線圖表。](graphics/ycbcr5.png)

然後，您可以在 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) 上呼叫 QueryInterface 來取得 [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)。 色彩轉換可以與上述轉換進行通訊，而且可以公開管線中每個階段的匯總功能。 WIC 可確保 YC<sub>b</sub>C<sub>r</sub> 資料會透過整個進程保留。 此連結僅適用于使用支援 YC<sub>b</sub>C<sub>r</sub> 存取的元件時。

### <a name="jpeg-codec-optimizations"></a>JPEG 編解碼器優化

類似于 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)的 jpeg 框架解碼執行， [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) 的 jpeg 框架解碼會支援原生 JPEG DCT 網域調整和旋轉。 您可以直接從 JPEG 解碼器要求兩個縮小的電源或旋轉。 這通常會比使用離散轉換產生更高的品質和效能。

此外，當您將一或多個 WIC 轉換轉換成 JPEG 解碼器之後，它可以利用原生 JPEG 調整和旋轉來滿足匯總要求的作業。

### <a name="format-conversions"></a>格式轉換

使用 [**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) 將平面 YC <sub>b</sub>C <sub>r</sub> 圖元資料轉換成交錯的像素格式，例如 GUID \_ WICPixelFormat32bppPBGRA。 Windows 8.1 中的 WIC 不提供轉換成平面 YC<sub>b</sub>C<sub>r</sub>像素格式的能力。

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>編碼 YC<sub>b</sub>C<sub>r</sub> 圖元資料

使用 [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) 將 YC <sub>b</sub>C <sub>r</sub> 圖元資料編碼成 JPEG 編碼器。 編碼 YC <sub>b</sub>C <sub>r</sub> 資料 **IWICPlanarBitmapFrameEncode** 類似，但不同于使用 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)編碼交錯資料。 平面介面只會公開撰寫平面框架影像資料的功能，您應該繼續使用畫面格編碼介面來設定中繼資料或縮圖，並在作業結束時認可。

在一般情況下，您應該遵循下列步驟：

1.  正常取得 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 。 如果您想要設定色度次取樣，請在建立框架時設定 [**JpegYCrCbSubsampling**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) 編碼器選項。
2.  如果您需要設定中繼資料或縮圖，請使用 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 正常進行。
3.  [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)的 QueryInterface。
4.  使用 [**IWICPlanarBitmapFrameEncode：： WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource)或 [**IWICPlanarBitmapFrameEncode：： WRITEPIXELS**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels)來設定 YC <sub>b</sub>C <sub>r</sub>圖元資料。 與其 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 對應專案不同，您會以 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 或 [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) 陣列提供這些方法，其中包含 YC <sub>b</sub>C <sub>r</sub> 圖元平面。
5.  當您完成時，請呼叫 [**IWICBitmapFrameEncode：： Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)。

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>解碼 Windows 10 中的 YC<sub>b</sub>C<sub>r</sub>圖元資料

從 Windows 10 組建1507開始，Direct2D 提供 [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)，這是一個比較簡單的方式，可將 jpeg 解碼成 Direct2D，同時利用 YC <sub>b</sub>C <sub>r</sub>優化。 **ID2D1ImageSourceFromWic** 會自動為您執行所有必要的 YC <sub>b</sub>C <sub>r</sub> 功能檢查;如果可能的話，它會使用優化的代碼路徑，否則會使用 fallback。 它也會啟用新的優化，例如僅快取所需的映射子領域加寬。

如需有關使用 [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)的詳細資訊，請參閱 Direct2D 相片調整 SDK [範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)。

## <a name="related-topics"></a>相關主題

* [Direct2D 和 WIC 範例中的 JPEG YCbCr 優化](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)
