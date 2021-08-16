---
description: 執行 IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: 執行 IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0088b756a7a30134224e32fa67ee891f2c48339f9af70447cb760915ad420619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711145"
---
# <a name="implementing-iwicbitmapdecoder"></a>執行 IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>IWICBitmapDecoder

當應用程式要求解碼器時，與編解碼器的第一個互動點是透過 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面。 這是容器層級介面，可讓您存取容器的最上層屬性，最重要的是它所包含的框架。 這是容器層級的解碼器類別上的主要介面。

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

某些影像格式具有全域縮圖、色彩內容或中繼資料，而許多影像格式都只針對每個畫面提供這些格式。 存取這些專案的方法在 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)上是選擇性的，但在 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)上是必要的。 同樣地，某些編解碼器不會使用索引像素格式，因此不需要在任何介面上執行 [CopyPalette](-wic-imp-iwicbitmapframedecode.md) 方法。 如需選擇性 **IWICBitmapDecoder** 方法的詳細資訊，請參閱實 [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)，其中最常見的方法是執行。

### <a name="querycapability"></a>QueryCapability

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) 是用於編解碼器仲裁的方法。  (請參閱[Windows 影像處理元件運作方式](-wic-howwicworks.md)主題中的[探索和仲裁](-wic-howwicworks.md)) 。 如果兩個編解碼器能夠解碼相同的影像格式，或如果發生模式衝突，且兩個編解碼器使用相同的識別模式，則這個方法可讓您選取最能處理任何特定映射的編解碼器。

叫用這個方法時，Windows 影像處理元件 (WIC) 會將包含影像的實際串流傳遞給您。 您必須確認是否可以解碼影像內的每個畫面格，並列舉中繼資料區塊，以精確地宣告此解碼器對傳遞給它的特定檔案資料流程有哪些功能。 這對所有的解碼器而言很重要，但對於以標記的影像檔案格式為基礎的影像格式， (TIFF) 容器特別重要。 探索進程的運作方式是將與登錄中的解碼器相關聯的模式比對實際影像檔案中的模式。 在登錄中宣告您的識別模式，可確保一律會針對影像格式的影像來偵測到您的解碼器。 不過，您仍然可以針對其他格式的影像來偵測到您的解碼器。 例如，所有 TIFF 容器都包含 TIFF 模式，這是 TIFF 影像格式的有效識別模式。 這表示在探索期間，會在影像檔案中找到至少兩個識別模式，而影像格式是以 TIFF 樣式的容器為基礎。 其中一個會是 TIFF 模式，另一個則是實際影像格式模式。 雖然不太可能，但其他不相關的影像格式也可能發生模式衝突。 這就是為什麼探索和仲裁是兩階段的流程。 一律確認傳遞給 [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) 的影像資料流程實際上是您自己影像格式的有效實例。 此外，如果您的編解碼器解碼的影像格式不是您所擁有的規格，則您的 **QueryCapability** 執行應該檢查是否有任何可能在您的編解碼器未實行的影像格式規格下有效的功能。 這樣可確保使用者不會遇到不必要的解碼失敗，或使用您的編解碼器取得未預期的結果。

在對影像執行任何作業之前，您必須先儲存資料流程的目前位置，以便您可以將它還原到其原始位置，然後再從方法返回。 指定功能的 [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) 列舉定義如下：

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

只有當您的編碼器是編碼影像的編碼器時，才應該宣告 **WICBitmapDecoderCapabilitySameEncoder** 。 在確認您是否可以解碼容器中的每個畫面格之後，如果您可以將部分（而非全部的框架）解碼，請 **WICBitmapDecoderCapabilityCanDecodeAllImages** **WICBitmapDecoderCapabilityCanDecodeSomeImages** 如果您可以解碼所有的框架，或不能將其解碼。  (這兩個列舉是互斥的;如果您傳回 **WICBitmapDecoderCapabilityCanDecodeAllImages**，則會忽略 **WICBitmapDecoderCapabilityCanDecodeSomeImages** 。在確認您可以列舉映射容器中的中繼資料區塊之後，) 宣告 **WICBitmapDecoderCapabilityCanEnumerateMetadata** 。 您不必在每個畫面格中檢查縮圖。 如果有全域縮圖，而您可以將它解碼，則可以宣告 **WICBitmapDecoderCapabilityCanDecodeThumbnail**。 如果沒有全域縮圖，則會嘗試將畫面格0的縮圖解碼。 如果其中一個位置沒有任何縮圖，請不要宣告這項功能。

在判斷與傳遞給這個方法的影像資料流程相關的解碼器功能之後，請使用您已確認此解碼器可在此映射上執行的 [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) 來執行或作業，並傳回結果。 請記得將資料流程還原至其原始位置，然後再返回。

### <a name="initialize"></a>初始化

在選取解碼器以解碼特定映射之後，應用程式會叫用 [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) 。 影像資料流程會傳遞至解碼器，而且呼叫端可以選擇性地指定 [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) 快取選項來處理檔案中的中繼資料。

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

有些應用程式使用的中繼資料比其他應用程式更多。 大部分的應用程式不需要存取影像檔案中的所有中繼資料，而且會在需要時要求特定的中繼資料。 其他應用程式則會事先快取所有中繼資料，而不是讓檔案資料流程保持開啟，並且在每次需要存取中繼資料時執行磁片 i/o。 如果呼叫端未指定中繼資料快取選項，預設的快取行為應該是快取的需求。 這表示在應用程式對該中繼資料提出特定要求之前，不應該將中繼資料載入至記憶體。 如果應用程式指定 **WICDecodeMetadataCacheOnLoad**，就應該立即在記憶體中載入中繼資料並加以快取。 當載入中繼資料時，檔案資料流程可能會在快取中繼資料之後釋放。

### <a name="getcontainerformat"></a>GetContainerFormat

若要執行 [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)，只需傳回已具現化之影像的影像格式 GUID。 這個方法也會在 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 和 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)上執行。

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) 會傳回 [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) 物件。 若要取得 **IWICBitmapDecoderInfo** 物件，只要將您的解碼器 GUID 傳遞至 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)上的 [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo)方法，然後在其上要求 **IWICBitmapDecoderInfo** 介面，如下列範例所示。


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) 只會傳回容器中的框架數目。 某些容器格式支援多個框架，而其他則只支援每個容器一個畫面格。

### <a name="getframe"></a>GetFrame

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) 是 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面上的重要方法，因為框架包含實際的影像位，而且從這個方法傳回的框架解碼物件是執行所要求影像之實際解碼的物件。 也就是您在撰寫解碼器時必須執行的另一個物件。 如需框架解碼器的詳細資訊，請參閱 [執行 IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)。

### <a name="getpreview"></a>GetPreview

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) 會傳回影像的預覽。 如需預覽的詳細討論，請參閱[執行 IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)介面上的實[IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)方法。

如果您的影像格式包含內嵌的 JPEG 預覽，強烈建議您將其委派給 WIC 平臺隨附的 JPEG 解碼，以解碼預覽和縮圖，而不是撰寫 JPEG 解碼來將它解碼。 若要這樣做，請搜尋資料流程中的預覽影像資料開始，並在 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)上叫用 [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)方法。


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**概念**
</dt> <dt>

[解碼器介面](-wic-decoderinterfaces.md)
</dt> <dt>

[執行 IWICBitmapCodecProgressNotification (解碼器) ](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



