---
description: 執行 IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: 執行 IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d02105470f837dba0689b665473c01c42f6cd6497a85424ea6eea3371696f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088010"
---
# <a name="implementing-iwicbitmapencoder"></a>執行 IWICBitmapEncoder

-   [IWICBitmapEncoder](#implementing-iwicbitmapencoder)
    -   [初始化](#initialize)
    -   [GetContainerFormat](#getcontainerformat)
    -   [GetEncoderInfo](#getencoderinfo)
    -   [CreateNewFrame](#createnewframe)
    -   [認可](#commit)
    -   [SetPreview](#setpreview)
-   [相關主題](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

-   [初始化](#initialize)
-   [GetContainerFormat](#getcontainerformat)
-   [GetEncoderInfo](#getencoderinfo)
-   [CreateNewFrame](#createnewframe)
-   [認可](#commit)
-   [SetPreview](#setpreview)

這個介面是 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面的對應項，而且是用來編碼影像檔案的起點。 如同 **IWICBitmapDecoder** 是用來從映射容器取得容器層級的屬性和個別的框架， [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 是用來設定容器層級的屬性，並將個別的影像框架序列化到容器中。 您可以在容器層級編碼器類別上執行此介面。

``` syntax
interface IWICBitmapEncoder : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IStream *pIStream,
              WICBitmapEncoderCacheOption cacheOption );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetEncoderInfo ( IWICBitmapEncoderInfo **pIEncoderInfo );
   HRESULT CreateNewFrame ( IWICBitmapFrameEncode **ppIFrameEncode,
              IPropertyBag2 **ppIEncoderOptions );
   HRESULT Commit ( void );

   // Optional methods
   HRESULT SetPreview ( IWICBitmapSource *pIPreview );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT SetColorContexts ( UINT cCount,
              IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
              **ppIMetadataQueryWriter );
   HRESULT SetPalette ( IWICPalette *pIPalette);
};
```

如同在實 [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)中所討論，某些影像格式具有全域縮圖、色彩內容或中繼資料，而許多影像格式都只會以每個畫面為基礎提供這些格式。 因此，設定這些方法的方法在 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)上是選擇性的，但在 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)上是必要的。 我們將在 **IWICBitmapFrameEncode** 上的 **IWICBitmapEncoder** 一節中討論選擇性的方法，這些方法是最常實作為的。

如果您不支援全域縮圖，請 \_ \_ 從 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)上的 SetThumbnail 方法傳回 WINCODEC ERR CODECNOTHUMBNAIL。 如果您不支援容器層級的選擇區，或您正在編碼的影像沒有已編制索引的格式，請 \_ \_ 從 SetPalette 方法傳回 WINCODEC ERR PALETTEUNAVAILABLE。 若為任何其他不支援的方法，則傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。

### <a name="initialize"></a>初始化

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) 是在 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 具現化之後，在其上叫用的第一個方法。 影像串流會傳遞至編碼器，而呼叫端可以選擇性地指定快取選項。 在解碼器的案例中，資料流程是唯讀的，但傳遞給編碼器的資料流程是可寫入的資料流程，編碼器會在其中序列化所有的影像資料和中繼資料。 編碼器上的快取選項也不同。

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

應用程式可選擇要求編碼器快取記憶體中的影像資料、將其快取到暫存檔案中，或直接寫入磁片檔案，而不需要快取。 當系統要求您在暫存檔案中快取資料時，編碼器應該在磁片上建立暫存檔案，並直接寫入該檔案，而不在記憶體中快取。 當呼叫端選取 [無快取] 選項時，每個畫面格都必須依序認可，才能建立下一個畫面格。

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)的執行方式與 [執行 IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)中的 [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md)方法相同。

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) 會傳回 [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) 物件。 若要取得 **IWICBitmapEncoderInfo** 物件，只需將您的編碼器 GUID 傳遞至 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)上的 [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo)方法，然後在其上要求 **IWICBitmapEncoderInfo** 介面。

請參閱在[GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md)下[執行 IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)的範例。

### <a name="createnewframe"></a>CreateNewFrame

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)是 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)上 [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)的編碼器對應項。 這個方法會傳回 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 物件，也就是實際序列化容器內特定框架之影像資料的物件。

Windows 影像處理元件 (WIC) 的其中一個優點是，它為應用程式提供一個抽象層，讓它們以相同方式使用所有影像格式。 不過，並非所有的影像格式都完全相同。 某些影像格式具有其他人沒有的功能。 為了讓應用程式能夠利用這些獨特的功能，必須提供方法讓編解碼器公開。 這是編碼器選項的用途。 如果您的編解碼器支援任何編碼器選項，您應該建立一個 [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 物件來公開您支援的編碼器選項，然後在此方法的 *ppIEncoderOptions* 參數中傳回該物件。 接著，呼叫者可以使用這個 IPropertyBag2 物件來判斷編解碼器支援的編碼器選項。 如果呼叫端想要為任何支援的編碼器選項指定值，則會將值指派給 IPropertyBag2 物件中的相關屬性，並在其 Initialize 方法中將其傳遞至新建立的 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 物件。

若要具現化 [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 物件，您必須先建立 PROPBAG2 結構來指定編碼器支援的每個編碼器選項，以及每個屬性的資料類型。 然後，您必須執行 IPropertyBag2 物件，以在寫入時強制執行每個屬性的值範圍，並調解任何衝突或重迭的值。 針對簡單的非衝突編碼器選項組，您可以叫用 [**CreateEncoderPropertyBag**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) 方法，它會使用您在 PROPBAG2 結構中指定的屬性來建立簡單的 IPropertyBag2 物件。 您仍然必須強制執行值範圍。 如需更高階的編碼器選項，或如果您需要協調衝突的值，您應該撰寫自己的 IPropertyBag2 執行。


```C++
UINT cuiPropertyCount = 0;
IPropertyBag2* pPropertyBag = NULL;
PROPBAG2* pPropBagOptions;
HRESULT hr;

// Insert code here to initialize piPropertyBag with the 
// supported options for your encoder, and to initialize 
// cuiPropertyCount to the number of encoder option properties
// you are exposing.
...

hr = pComponentFactory->CreateEncoderPropertyBag( 
   pPropBagOptions, cuiPropertyCount, &pPropertyBag);
```



WIC 提供一些常用影像格式所使用的一組標準編碼器選項。 所有標準編碼器選項都是選擇性的，且不需要編解碼器就能支援它們。 提供這些標準選項的原因是因為許多應用程式會公開使用者介面，讓使用者在以支援這些選項的格式儲存影像檔時指定這些選項。 提供標準方式來指定這些選項，可讓應用程式輕鬆地以一致的方式將它們傳達給編碼器。 標準編碼器選項列于下表。



| 編碼器選項     | VARTYPE  | 值範圍               |
|--------------------|----------|---------------------------|
| Lossless           | VT \_ BOOL | True/False                |
| ImageQuality       | VT \_ R4   | 0.0-1。0                   |
| CompressionQuality | VT \_ R4   | 0.0-1。0                   |
| BitmapTransform    | VT \_ UI1  | WICBitmapTransformOptions |



 

如果您的編解碼器支援不失真編碼，您應該公開不失真編碼器選項，讓應用程式要求以 losslessly 編碼的影像。 如果呼叫端將此屬性設定為 True，您應該忽略 ImageQuality 選項，並將影像 losslessly 編碼。

ImageQuality 選項可讓應用程式指定用來編碼影像的精確度程度。 此選項可讓使用者在影像品質與速度及/或檔案大小之間進行取捨。 JPEG 是支援此取捨的影像格式範例。 值為0.0 表示精確度為低重要性，而且編碼器應使用其最大量的演算法。 值為1.0 表示精確度是最重要的，而且編碼器應該盡可能保留最高的精確度。 根據您的編解碼器 (，這可能與不失真選項同義。 但是，如果您的編解碼器支援不失真編碼，而且不失真選項設定為 True，則應忽略 ImageQuality 選項。 ) 

CompressionQuality 選項可讓應用程式指定將影像編碼時所要使用的壓縮效率。 非常有效率的演算法可能會產生較小的影像檔案品質與較低效率的壓縮演算法相同，但編碼可能需要較長的時間。 此選項可讓使用者指定檔案大小與編碼速度之間的取捨，同時保留相同等級的品質。 TIFF 是支援此取捨的影像格式範例。  (請注意，JPEG 之類的格式支援不同層級的壓縮，但較高的壓縮率會產生較低的影像品質。 因此，JPEG 影像格式會公開 ImageQuality 選項，而不是 CompressionQuality 選項。針對此選項 ) 0.0 的值，表示您應該儘快壓縮影像，而不會降低精確度，因為較大的檔案大小。 值為1.0 時，表示您應該在相同的品質) 層級上建立最小的可能檔案大小 (，而不論其編碼所需的時間長度為何。 編解碼器可以同時支援 ImageQuality 選項和 CompressionQuality 選項，其中 ImageQuality 選項會指定 lossiness 的可接受程度，而 CompressionQuality 選項則會在指定的品質層級提供大小/速度的取捨。

BitmapTransform 選項提供一個方法，讓呼叫端在編碼時指定旋轉角度或垂直或水準翻轉方向。 用來指定所要求之轉換的 WICBitmapTransformOptions 列舉，與透過 IWICBitmapSourceTransform 介面進行解碼期間要求轉換時所用的列舉相同。

請注意，編碼器不限於標準編碼器選項。 編碼器選項的目的是要讓編碼器公開其功能，而且您可以公開的功能類型沒有任何限制。 請確定您的編碼器選項有妥善記載。 雖然應用程式可以使用您從這個方法傳回的屬性包，來探索您支援之選項的名稱、類型和值範圍，但它們的唯一方法是從您的檔中找出其意義，或如何在使用者介面中加以公開。

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) 是在所有的影像資料和中繼資料都已序列化為數據流之後，您所呼叫的方法。 您應使用此方法將預覽影像資料序列化為數據流，以及任何全域縮圖、中繼資料、調色板或其他專案（如果適用）。 這個方法不應該關閉檔案資料流程，因為開啟資料流程的應用程式應該會關閉它。

IWICBitmapFrameEncode： Commit 方法的區段有 IWICBitmapEncoderCacheOptions 如何影響此方法行為的詳細資料。

### <a name="setpreview"></a>SetPreview

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) 用來建立映射的預覽。 雖然並非絕對要求每個影像都有預覽，但強烈建議您這麼做。 新式數位攝影機和掃描器會產生非常高的解析度影像，通常很大，因此需要大量的處理時間來進行解碼。 下一代攝影機的影像會更大。 最好提供較小、較低解析度的影像版本（通常是 JPEG 格式），當使用者要求它時，可以快速解碼並「立即」顯示。 應用程式可能會在要求實際影像進行解碼之前要求預覽，以提供更好的使用者體驗，並在 theyare 等候解碼實際影像時顯示影像的螢幕大小表示。 雖然編解碼器應該提供預覽，但不支援 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 的編解碼器絕對應該這麼做。

如果您提供 JPEG 預覽，就不需要撰寫 JPEG 編碼器來編碼。 您應委派給 WIC 平臺隨附的 JPEG 編碼器，以將預覽和縮圖編碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

**概念**
</dt> <dt>

[編碼器介面](-wic-encoderinterfaces.md)
</dt> <dt>

[執行 IWICBitmapCodecProgressNotification (編碼器) ](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
