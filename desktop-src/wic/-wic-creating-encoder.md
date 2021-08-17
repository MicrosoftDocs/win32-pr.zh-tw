---
description: 編碼器會將影像資料寫入資料流程。 編碼器可以在將影像圖元寫入串流之前，以數種方式壓縮、加密和更改影像圖元。
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: 編碼總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee4c554046fa99cab53ff3e3acb8e2eadeb1a70a9140370dbc4b426fd576c15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088080"
---
# <a name="encoding-overview"></a>編碼總覽

編碼器會將影像資料寫入資料流程。 編碼器可以在將影像圖元寫入串流之前，以數種方式壓縮、加密和更改影像圖元。 使用某些編碼器會產生取捨，例如，JPEG 會以較佳的方式來交易色彩資訊以提升壓縮。 其他編碼器不會造成這類遺失，例如點陣圖 (BMP) 。 因為許多編解碼器使用專屬技術來達到更佳的壓縮和影像精確度，所以如何編碼影像的詳細資料是由編解碼器開發人員所組成。

本主題包含下列各節。

-   [IWICBitmapEncoder](#iwicbitmapencoder)
-   [IWICBitmapFrameEncode](#iwicbitmapframeencode)
-   [TIFF 編碼範例](#tiff-encoding-example)
-   [編碼器選項使用方式](#encoder-options-usage)
-   [編碼器選項](#encoder-options-usage)
-   [編碼器選項範例](#encoder-options-examples)
-   [相關主題](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 是將影像編碼為目標格式的主要介面，用來將影像的元件（例如縮圖 ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) 和框架 ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)) ）序列化至影像檔案。

序列化程式的運作方式和時機，會留給編解碼器開發人員。 目的檔案格式內的每個資料區塊都應該能夠獨立于順序以外的設定，但同樣地，這是編解碼器開發人員的決策。 不過，一旦呼叫 [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) 方法之後，就不應該允許變更影像，而且應該關閉資料流程。

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 是用於編碼影像個別框架的介面。 它提供了設定個別框架影像處理元件的方法，例如縮圖和框架，以及影像尺寸、DPI 和像素格式。

個別的框架可以使用框架專屬的中繼資料進行編碼，讓 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 透過 [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) 方法提供中繼資料寫入器的存取權。

框架的 [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) 方法會認可個別畫面格的所有變更，並指出該框架的變更應該不會再被接受。

## <a name="tiff-encoding-example"></a>TIFF 編碼範例

在下列範例中，標記的影像檔案格式 (TIFF) 影像是使用 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 和 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)進行編碼。 TIFF 輸出是使用 [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) 自訂的，而點陣圖框架則是使用指定的選項來初始化。 使用 [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)建立映射之後，就會使用 [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) 認可框架，然後使用 [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)來儲存映射。


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride***/;
    UINT cbBufferSize = uiHeight * cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a>編碼器選項使用方式

不同格式的不同編碼器需要針對影像的編碼方式公開不同的選項。 Windows (WIC 的影像處理元件) 提供一致的機制，可表示是否需要編碼選項，同時仍能讓應用程式使用多個編碼器，而不需要特定格式的知識。 這是藉由在 [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)方法和 [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize)方法上提供 [IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag)參數來完成。

元件 factory 提供建立編碼器選項屬性包的簡單建立點。 如果用戶端需要提供簡單、直覺且不衝突的編碼器選項群組合，則編解碼器可以使用此服務。 您必須在建立時使用與該編解碼器相關的所有編碼器選項來初始化映射屬性包。 針對標準集中的編碼器選項，值範圍會在寫入時強制執行。 為了更先進的需要，編解碼器應該撰寫自己的屬性包執行。

應用程式會在畫面格建立期間提供編碼器選項包，並且必須在初始化編碼器框架之前設定任何值。 針對 UI 導向的應用程式，它可以為標準編碼器選項提供固定的 UI，並針對剩餘的選項提供先進的觀點。 您可以透過 Write 方法一次建立一個變更，任何錯誤都會透過 IErrorLog 回報。 變更後，UI 應用程式應該一律重新讀取並顯示所有選項，以防變更造成 cascade 效果。 應用程式應該準備好處理編解碼器的失敗畫面格初始化，只透過其屬性包提供基本的錯誤報表。

## <a name="encoder-options"></a>編碼器選項

應用程式可能預期會遇到下列一組編碼器選項。 編碼器選項反映編碼器和基礎容器格式的功能，因此其本質並不是與編解碼器無關。 可能的話，應該將新選項正規化，以便將它們套用至出現的新編解碼器。



| 屬性名稱      | VARTYPE  | 值                                                                     | 適用的編解碼器 |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | VT \_ R4   | 0-1。0                                                                     | JPEG、HDPhoto     |
| CompressionQuality | VT \_ R4   | 0-1。0                                                                     | TIFF              |
| Lossless           | VT \_ BOOL | **TRUE**， **FALSE**                                                       | HDPhoto           |
| BitmapTransform    | VT \_ UI1  | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

0.0 的 ImageQualty 表示最小的精確度轉譯和1.0 表示最高的精確度，這也可能表示因編解碼器而異。

CompressionQuality 0.0 表示最有效率的壓縮配置，通常會產生快速編碼但較大的輸出。 值為1.0 表示最有效率的可用配置，通常需要更多時間進行編碼，但產生較小的輸出。 視編解碼器的功能而定，此範圍可能會對應到一組不同的可用壓縮方法。

無失真表示編解碼器會將影像編碼為無失真，而不會遺失影像資料。 如果已啟用無損，則會忽略 ImageQuality。

除了上述的一般編碼器選項以外，WIC 提供的編解碼器也支援下列選項。 如果編解碼器必須支援與這些提供的編解碼器使用方式一致的選項，則建議您這樣做。



| 屬性名稱           | VARTYPE           | 值                                                                             | 適用的編解碼器 |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | VT \_ BOOL          | 開啟/關閉                                                                            | PNG               |
| FilterOption            | VT \_ UI1           | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | VT \_ UI1           | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminance               | VT \_ UI4/vt \_ 陣列 | 64專案 (DCT)                                                                   | JPEG              |
| Chrominance             | VT \_ UI4/vt \_ 陣列 | 64專案 (DCT)                                                                   | JPEG              |
| JpegYCrCbSubsampling    | VT \_ UI1           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | VT \_ BOOL          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | VT \_ BOOL          | 開啟/關閉                                                                            | BMP               |



 

使用 **VT \_ EMPTY** 表示 **\* \* 未設定** 為預設值。 如果已設定其他屬性，但不支援這些屬性，則編碼器應忽略它們;如果應用程式想要有可能存在或可能不存在的功能，這可讓應用程式以較少的邏輯編寫程式碼。

## <a name="encoder-options-examples"></a>編碼器選項範例

在上述的 [TIFF 編碼範例](#tiff-encoding-example) 中，已設定特定的編碼器選項。 PROPBAG2 結構的 *pstrName* 成員會設定為適當的屬性名稱，而 VARIANT 會設定為對應的 VARTYPE 和所需的值，在此例中是 [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) 列舉的成員。


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



若要使用預設編碼器選項，只要使用建立框架時傳回的屬性包來初始化點陣圖框架。


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



如果未考慮任何編碼器選項，也可以消除屬性包。


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[解碼總覽](-wic-creating-decoder.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
