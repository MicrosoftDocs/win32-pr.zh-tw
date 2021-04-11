---
description: 執行 IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: 執行 IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194128"
---
# <a name="implementing-iwicbitmapframeencode"></a>執行 IWICBitmapFrameEncode

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 是 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 介面的編碼器對應項。 您可以在框架層級編碼類別上執行這個介面，這是針對每個框架執行影像位實際編碼的類別。


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [初始化](#initialize)
-   [SetSize 和 SetResolution](#setsize-and-setresolution)
-   [SetPixelFormat](#setpixelformat)
-   [SetColorCoNtexts](#setcolorcontexts)
-   [GetMetadataQueryWriter](#getmetadataquerywriter)
-   [SetThumbnail](#setthumbnail)
-   [WritePixels](#writepixels)
-   [WriteSource](#writesource)
-   [認可](#commit)
-   [SetPalette](#setpalette)

### <a name="initialize"></a>初始化

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) 是在 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 物件具現化之後，在該物件上叫用的第一個方法。 這個方法有一個參數，可以設定為 **Null**。 此參數代表編碼器選項，和您在容器層級解碼器的 [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)方法中建立的相同 [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))實例，並在該方法的 pIEncoderOptions 參數中傳回給呼叫端。 屆時，您已填入 IPropertyBag2 結構，其中包含的屬性代表您的框架層級編碼器所支援的編碼選項。 呼叫端現在已提供這些屬性的值，以指出特定編碼選項參數，並將相同的物件傳回給您，以初始化 **IWICBitmapFrameEncode** 物件。 編碼影像位時，您應該套用指定的選項。

### <a name="setsize-and-setresolution"></a>SetSize 和 SetResolution

[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) 和 [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) 很容易理解。 呼叫端會使用這些方法來指定編碼影像的大小和解析度。

### <a name="setpixelformat"></a>SetPixelFormat

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) 是用來要求用來將影像編碼的像素格式。 如果要求的像素格式不受支援，您應該傳回 *pPixelFormat* 所支援的最接近像素格式的 GUID，也就是 in/out 參數。

### <a name="setcolorcontexts"></a>SetColorCoNtexts

[**SetColorCoNtexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) 可用來指定一個或多個有效的色彩內容 (也稱為色彩設定檔) 用於此影像。 請務必指定色彩內容，如此一來，稍後再將影像解碼的應用程式就可以從來源色彩設定檔轉換成用來顯示或列印影像之裝置的目的地設定檔。 如果沒有色彩設定檔，就無法在不同的裝置上取得一致的色彩。 當使用者的相片在不同的監視器上看起來不同時，這可能會讓使用者感到沮喪，而且他們無法取得列印來比對畫面上顯示的內容。

### <a name="getmetadataquerywriter"></a>GetMetadataQueryWriter

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) 會傳回 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) ，讓應用程式用來在影像框架的中繼資料區塊中插入或編輯特定的中繼資料屬性。

您可以透過數種方式從 [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)具現化 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 。 您可以從 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)建立它，就像 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)是從 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)介面上 [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)方法中的 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)建立的相同方式。


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



您也可以從現有的 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)建立它，例如使用先前的方法所取得的。


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



*PguidVendor* 參數可讓您指定查詢寫入器在具現化中繼資料寫入器時所要使用的特定廠商。 例如，如果您提供自己的中繼資料寫入器，您可能會想要指定自己的廠商 GUID。 如果您沒有喜好設定，則可以將 **Null** 傳遞給這個參數。

### <a name="setthumbnail"></a>SetThumbnail

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) 可用來提供縮圖。 所有影像都應該在全域、每個畫面上或兩者提供縮圖。 **GetThumbnail** 和 **SetThumbnail** 方法在容器層級是選擇性的，但如果編解碼器 \_ \_ 從 [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)方法傳回 WINCODEC ERR CODECNOTHUMBNAIL，Windows 影像處理元件 (WIC) 將會叫用框架0的 [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)方法。 如果在任何地方都找不到縮圖，WIC 必須將完整的影像解碼，並將其調整為縮圖大小，這可能會對較大的影像產生較大的效能影響。

縮圖的大小和解析度應可讓您快速解碼和顯示。 基於這個理由，縮圖是最常見的 JPEG 影像。 請注意，如果您將 JPEG 用於縮圖，就不需要撰寫 JPEG 編碼程式來將其編碼，或使用 JPEG 解碼來將其解碼。 您應一律委派給 WIC 平臺隨附的 JPEG 編解碼器，以便編碼和解碼縮圖。

### <a name="writepixels"></a>WritePixels

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) 是一種方法，用來從記憶體中的點陣圖傳入掃描行以進行編碼。 方法會重複呼叫，直到傳入所有掃描行為止。 *LineCount* 參數會指出要在此呼叫中寫入多少掃描行。 *CbStride* 參數會指出每個掃描行的位元組數目。 *cbBufferSize* 指出 pbPixels 參數中所傳遞的緩衝區大小，其中包含要編碼的實際影像位。 如果累計呼叫中掃描行的總高度大於 [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) 方法中指定的高度，則傳回 WINCODEC \_ ERR \_ TOOMANYSCANLINES。

當 [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) 是 **WICBitmapEncoderCacheInMemory** 時，掃描行應該在記憶體中快取，直到傳入所有掃描行為止。 如果編碼器快取選項是 **WICBitmapEncoderCacheTempFile**，則應該將掃描行快取在初始化物件時所建立的暫存檔案中。 在上述任一情況下，除非呼叫者呼叫 [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)，否則不應將映射編碼。 在 **WICBitmapEncoderNoCache** 快取選項的情況下，編碼器應該盡可能編碼收到的掃描行。  (在某些格式中，這是不可能的，而且必須在呼叫 Commit 之前快取掃描行。 ) 

大部分的原始編解碼器都不會執行 [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)，因為它們不支援改變原始檔案中的影像位。 不過，原始編解碼器仍應採用 **WritePixels**，因為新增中繼資料時，可能會增加檔案的大小，需要在磁片上重寫檔案。 在這種情況下，您必須能夠複製現有的映射位，也就是 **WritePixels** 方法的用途。

### <a name="writesource"></a>WriteSource

[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) 用來編碼 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 物件。 第一個參數是 **IWICBitmapSource** 物件的指標。 第二個參數是指定要編碼之區域的 WICRect。 只要每個矩形的寬度與要編碼的最終影像寬度相同，就可以連續多次呼叫這個方法。 如果以 prc 參數傳遞的矩形寬度與 SetSize 方法中指定的寬度不同，則會傳回 WINCODEC \_ ERR \_ SOURCERECTDOESNOTMATCHDIMENSIONS。 如果累計呼叫中掃描行的總高度大於 SetSize 方法中指定的高度，則傳回 WINCODEC \_ ERR \_ TOOMANYSCANLINES。

使用先前所述的 [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) 方法，快取選項的運作方式與此方法相同。

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) 是將編碼的影像位序列化為檔案資料流程的方法，並逐一查看框架的所有中繼資料寫入器，要求他們將其中繼資料序列化為數據流。 在編碼器快取選項為 WICBitmapEncoderCacheInMemory 或 WICBitmapEncoderCacheTempFile 的情況下，此方法也會負責編碼影像，而且當快取選項為 WICBitmapEncoderCacheTempFile 時， **Commit** 方法也應該在編碼之前，先刪除用來快取影像資料的暫存檔案。

當所有組成影像的掃描行或矩形都已使用 [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) 或 [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) 方法傳入時，一律會叫用這個方法。 透過 WritePixels 或 WriteSource 的累積呼叫所組成的最後矩形大小，必須和 SetSize 方法中指定的大小相同。 如果大小不符合預期的大小，這個方法應該會傳回 WINCODECERROR \_ UNEXPECTEDSIZE。

若要逐一查看中繼資料寫入器，並告訴每個中繼資料寫入器將其中繼資料序列化，請移至資料流程、叫用 GetWriterByIndex 逐一查看每個區塊的寫入器，然後在每個中繼資料寫入器上叫用 IWICPersistStream。


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a>SetPalette

只有具有索引格式的編解碼器才需要執行 [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) 方法。 如果影像使用已編制索引的格式，請使用這個方法來指定影像中所使用之色彩的調色板。 如果您的編解碼器沒有已編制索引的格式，請 \_ \_ 從這個方法傳回 WINCODEC ERR PALETTEUNAVAILABLE。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[執行 IWICBitmapCodecProgressNotification (編碼器) ](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[執行 IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
