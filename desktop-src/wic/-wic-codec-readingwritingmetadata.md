---
description: 本主題概要說明如何使用 Windows 影像處理元件 (WIC) api 來讀取和寫入內嵌于影像檔案的中繼資料。
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: 讀取和寫入影像中繼資料的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191ffbe919e09acb153505fd3b43b50453b67708259206bffe66a0322d485a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088134"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a>讀取和寫入影像中繼資料的總覽

本主題概要說明如何使用 Windows 影像處理元件 (WIC) api 來讀取和寫入內嵌于影像檔案的中繼資料。

本主題包含下列各節。

-   [必要條件](#prerequisites)
-   [簡介](#introduction)
-   [使用查詢讀取器讀取 Metadadata](#reading-metadadata-using-a-query-reader)
    -   [取得查詢讀取器](#obtaining-a-query-reader)
    -   [讀取中繼資料](#reading-metadata)
    -   [其他查詢讀取器方法](#additional-query-reader-methods)
-   [使用查詢寫入器撰寫中繼資料](#writing-metadata-using-a-query-writer)
    -   [取得查詢寫入器](#obtaining-a-query-writer)
    -   [新增中繼資料](#adding-metadata)
    -   [移除中繼資料](#removing-metadata)
    -   [複製重新編碼的中繼資料](#copying-metadata-for-re-encoding)
-   [快速中繼資料編碼](#fast-metadata-encoding)
    -   [將填補加入中繼資料區塊](#adding-padding-to-metadata-blocks)
    -   [取得快速中繼資料編碼器](#obtaining-a-fast-metadata-encoder)
    -   [使用快速中繼資料編碼器](#using-the-fast-metadata-encoder)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

若要瞭解本主題，您應該熟悉 wic 中繼資料系統（如 [Wic 中繼資料總覽](-wic-about-metadata.md)中所述）。 您也應該熟悉用來讀取和寫入中繼資料的查詢語言，如 [中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)中所述。

## <a name="introduction"></a>簡介

WIC 為應用程式開發人員提供元件物件模型 (COM) 元件，以讀取和寫入內嵌在影像檔中的中繼資料。 有兩種方式可以讀取和寫入中繼資料：

-   使用查詢讀取器/寫入器和查詢運算式來查詢區塊內的嵌套區塊或特定中繼資料的中繼資料區塊。
-   使用元資料處理程式 (中繼資料讀取器或中繼資料寫入器) 來存取中繼資料區塊內的嵌套中繼資料區塊或特定中繼資料。

最簡單的方法是使用查詢讀取器/寫入器和查詢運算式來存取中繼資料。 查詢讀取器 ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) 用來讀取中繼資料，而查詢寫入器 ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) 用來寫入中繼資料。 這兩種都使用查詢運算式來讀取或寫入所需的中繼資料。 在幕後，查詢讀取器 (和寫入器) 會使用元資料處理程式來存取查詢運算式所描述的中繼資料。

更先進的方法是直接存取元資料處理程式。 使用區塊讀取器 ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) 或區塊寫入器 ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) ，從個別的框架取得元資料處理程式。 可用的元資料處理程式有兩種類型：中繼資料讀取器 ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) 和中繼資料寫入器 ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) 。

本主題的整個範例都會使用 JPEG 影像檔案的下圖。 此圖表表示的影像是使用 Microsoft 小畫家建立的;評等中繼資料是使用 Windows Vista 的影像中心功能新增的。

![包含評等中繼資料之 jpeg 影像的圖例](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a>使用查詢讀取器讀取 Metadadata

讀取中繼資料最簡單的方式是使用查詢讀取器介面 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)。 查詢讀取器可讓您使用查詢運算式，讀取中繼資料區塊內的中繼資料區塊和專案。

取得查詢讀取器的方法有三種：透過點陣圖解碼 ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)) 、透過其個別的框架 ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) ，或透過查詢寫入器 ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) 。

### <a name="obtaining-a-query-reader"></a>取得查詢讀取器

下列範例程式碼示範如何從影像處理站取得點陣圖解碼器，以及取得個別點陣圖框架。 這段程式碼也會執行從已解碼的框架取得查詢讀取器所需的設定工作。


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



您可以使用映射處理站的 **CreateDecoderFromFilename** 方法，取得 test.jpg 檔案的點陣圖解碼器。 在這個方法中，第四個參數會設定為從 [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) 列舉 WICDecodeMetadataCacheOnDemand 的值。 這會告知解碼器在需要中繼資料時快取中繼資料;您可以藉由取得查詢讀取器或基礎中繼資料讀取器。 使用這個選項可讓您將資料流程保留給快速中繼資料編碼所需的中繼資料，並啟用 JPEG 影像的不失真解碼。 或者，您可以使用其他 **WICDecodeOptions** 值 WICDecodeMetadataCacheOnLoad，這會在載入映射時立即快取內嵌影像中繼資料。

若要取得框架的查詢讀取器，請對框架的 **GetMetadataQueryReader** 方法進行簡單的呼叫。 下列程式碼示範此呼叫。


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



同樣地，也可以在解碼器層級取得查詢讀取器。 對解碼器的 **GetMetadataQueryReader** 方法進行簡單的呼叫，會取得該解碼器的查詢讀取器。 與框架的查詢讀取器不同的是，相較于框架的查詢讀取器，它會讀取個別畫面格以外的影像中繼資料。 不過，此案例並不常見，原生映射格式不支援這項功能。 在框架層級，WIC 讀取和寫入中繼資料所提供的原生映射編解碼器，甚至是針對單一框架格式（例如 JPEG）。

### <a name="reading-metadata"></a>讀取中繼資料

在您繼續實際讀取中繼資料之前，請查看下列 JPEG 檔案的圖表，其中包含內嵌的中繼資料區塊，以及要取出的實際資料。 此圖表提供在影像內的特定中繼資料區塊和專案的標注，提供每個區塊或專案的中繼資料查詢運算式。

![具有中繼資料標注之 jpeg 影像的圖例](graphics/jpegwithcallouts.png)

若要依名稱查詢內嵌的中繼資料區塊或特定專案，請呼叫 **GetMetadataByName** 方法。 這個方法會採用查詢運算式和傳回中繼資料專案的 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 。 下列程式碼會查詢嵌套的中繼資料區塊，並將 PROPVARIANT 值所提供的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 元件轉換成查詢讀取器（如果有找到）。


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



查詢運算式 "/app1/ifd" 正在查詢 App1 區塊中嵌套的 IFD 區塊。 JPEG 影像檔案包含 IFD 的嵌套中繼資料區塊，因此[](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)會以 (vt) 的變數類型 `VT_UNKNOWN` 和 (PunkVal) 的[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面指標來傳回 PROPVARIANT。 然後，您可以查詢 IUnknown 介面是否有查詢讀取器。

下列程式碼會根據與嵌套的 IFD 區塊相關的新查詢讀取器，示範新的查詢。


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



查詢運算式 "/{ushort = 18249}" 會查詢 IFD 區塊，以取得內嵌在標記18249下的 MicrosoftPhoto 評等。 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)值現在會包含的實值型別 `VT_UI2` 和資料值50。

不過，在查詢特定資料值之前，不需要取得嵌套區塊。 例如，您可以改為使用根中繼資料區塊和下列程式碼中所示的查詢來取得相同的資訊，而不是查詢嵌套的 IFD，然後再查詢 MicrosoftPhoto 評等。


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



除了查詢中繼資料區塊中的特定中繼資料專案以外，您也可以列舉中繼資料區塊中的所有中繼資料專案， (不包括) 的嵌套中繼資料區塊中的中繼資料專案。 若要列舉目前區塊中的中繼資料專案，請使用查詢讀取器的 **GetEnumeration** 方法。 這個方法會取得 **IEnumString** 介面，此介面會填入目前區塊中的中繼資料專案。 例如，下列程式碼會列舉先前取得之嵌套的 IFD 區塊的 XMP 評等和 MicrosoftPhoto 評等。


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



如需識別各種影像格式和元資料格式之適當標記的詳細資訊，請參閱 [原生影像格式中繼資料查詢](-wic-native-image-format-metadata-queries.md)。

### <a name="additional-query-reader-methods"></a>其他查詢讀取器方法

除了讀取中繼資料，您也可以取得有關查詢讀取器的其他資訊，並透過其他方式取得中繼資料。 查詢讀取器提供兩種方法，提供查詢讀取器（ **GetContainerFormat** 和 **GetLocation**）的相關資訊。

使用內嵌查詢讀取器時，您可以使用 **GetContainerFormat** 來判斷中繼資料區塊的類型，而且您可以呼叫 **GetLocation** 來取得相對於根中繼資料區塊的路徑。 下列程式碼會查詢內嵌查詢讀取器的位置。


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



內嵌查詢讀取器的 **GetContainerFormat** 呼叫會傳回 IFD 元資料格式 GUID。 對 **GetLocation** 的呼叫會傳回 "/app1/ifd" 的命名空間;為您提供將執行後續查詢來執行新查詢讀取器的相對路徑。 當然，上述程式碼並沒有什麼用處，但它確實會示範如何使用 **GetLocation** 方法來尋找嵌套的中繼資料區塊。

## <a name="writing-metadata-using-a-query-writer"></a>使用查詢寫入器撰寫中繼資料

> [!Note]  
> 本節提供的一些程式碼範例不會顯示在撰寫中繼資料所需的實際步驟內容中。 若要在工作範例的內容中查看程式碼範例，請參閱 how to：使用中繼資料重新編碼影像教學課程。

 

寫入中繼資料的主要元件是查詢寫入器 ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) 。 查詢寫入器可讓您設定和移除中繼資料區塊中的中繼資料區塊和專案。

如同查詢讀取器，有三種方式可以取得查詢寫入器：透過點陣圖編碼器 ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)) 、透過其個別的框架 ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) ，或透過快速的中繼資料編碼器 ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) 。

### <a name="obtaining-a-query-writer"></a>取得查詢寫入器

最常見的查詢寫入器適用于點陣圖的個別框架。 此查詢寫入器會設定並移除影像框架的中繼資料區塊和專案。 若要取得影像框架的查詢寫入器，請呼叫框架的 **GetMetadataQueryWriter** 方法。 下列程式碼示範簡單的方法呼叫，以取得框架的查詢寫入器。


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



同樣地，也可以取得編碼器層級的查詢寫入器。 編碼器的 **GetMetadataQueryWriter** 方法的簡單呼叫會取得編碼器的查詢寫入器。 編碼器的查詢寫入器與框架的查詢編寫器不同，它會在個別框架外寫入影像的中繼資料。 不過，此案例並不常見，原生映射格式不支援這項功能。 在框架層級，WIC 讀取和寫入中繼資料所提供的原生映射編解碼器，甚至是針對單一框架格式（例如 JPEG）。

您也可以直接從映射處理站取得查詢寫入器 ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)) 。 有兩種影像處理站方法會傳回查詢寫入器： **CreateQueryWriter** 和 **CreateQueryWriterFromReader**。

**CreateQueryWriter** 會建立指定之元資料格式和廠商的查詢寫入器。 此查詢寫入器可讓您撰寫特定元資料格式的中繼資料，並將其新增至影像。 下列程式碼示範用來建立 XMP 查詢寫入器的 **CreateQueryWriter** 呼叫。


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



在此範例中，易記名稱 `GUID_MetadataFormatXMP` 會用來做為 *guidMetadataFormat* 參數。 它代表 XMP 元資料格式 GUID，而廠商則代表 Microsoft 建立的處理常式。 或者，如果沒有其他的 XMP 處理常式存在，則可以使用相同的結果來傳遞 **Null** 作為 *pguidVendor* 參數。 如果自訂的 XMP 處理常式與原生 XMP 處理常式一起安裝，則傳遞 **Null** 給廠商會導致查詢寫入器傳回最小的 GUID。

**CreateQueryWriterFromReader** 與 **CreateQueryWriter** 方法類似，不同之處在于它會以查詢讀取器所提供的資料會預先填入新的查詢寫入器。 在維護現有的中繼資料，或移除不想要的中繼資料時，這非常有用。 下列程式碼示範 **CreateQueryWriterFromReader** 呼叫。


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a>新增中繼資料

取得查詢寫入器之後，您可以使用它來加入中繼資料區塊和專案。 若要寫入中繼資料，您可以使用查詢寫入器的 **SetMetadataByName** 方法。 **SetMetadataByName** 接受兩個參數：查詢運算式 (*WzName*) 和 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*) 的指標。 查詢運算式會定義要設定的區塊或專案，而 PROPVARIANT 會提供要設定的實際資料值。

下列範例示範如何使用先前使用 **CreateQueryWriter** 方法取得的 XMP 查詢寫入器來加入標題。


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



在此範例中，值的類型 (vt) 設定為 `VT_LPWSTR` ，表示將會使用字串作為資料值。 因為 *值* 的類型是字串，所以會使用 *pwszVal* 來設定要使用的標題。 接著會使用查詢運算式 "/dc： title" 和新設定的 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)來呼叫 **SetMetadataByName** 。 使用的查詢運算式表示應該設定數位相機 (dc) 架構中的 title 屬性。 請注意，運算式不是 "/xmp/dc： title";這是因為查詢編寫器已經是 XMP 專屬的，而且不包含內嵌的 XMP 區塊，其中 "/xmp/dc： title" 會建議。

到目前為止，您沒有實際將任何中繼資料新增至影像框架。 您只是將資料填入查詢寫入器。 若要將查詢寫入器所代表的中繼資料區塊加入至框架，您可以使用查詢寫入器作為 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)的值，再次呼叫 **SetMetadataByName** 。 這可有效地將查詢寫入器中的中繼資料複製到影像框架。 下列程式碼示範如何在先前取得至框架根中繼資料區塊的 XMP 查詢寫入器中加入中繼資料。


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



在此範例中，會使用 (vt) 的實值型別， `VT_UNKOWN` 表示 COM 介面的值型別。 然後，會使用 XMP 查詢寫入器 (piXMPWriter) 做為 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)的值，使用 AddRef 方法來加入它的參考。 最後，藉由呼叫框架的 **SetMetadataByName** 方法來設定 XMP 查詢寫入器，並傳遞查詢運算式 "/"，指出根區塊和新設定的 PROPVARIANT。

> [!Note]  
> 如果框架已包含您嘗試新增的中繼資料區塊，則會新增您要加入的中繼資料，並覆寫現有的中繼資料。

 

### <a name="removing-metadata"></a>移除中繼資料

查詢寫入器也可讓您藉由呼叫 **RemoveMetadataByName** 方法來移除中繼資料。 **RemoveMetadataByName** 會採用查詢運算式，並移除中繼資料區塊或專案（如果存在的話）。 下列程式碼示範如何移除先前加入的標題。


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



下列程式碼示範如何移除整個 XMP 中繼資料區塊。


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a>複製重新編碼的中繼資料

> [!Note]  
> 此區段中的程式碼只有在來源和目的影像格式相同時才有效。 編碼為不同的影像格式時，無法在單一作業中複製映射的所有中繼資料。

 

若要在將影像重新編碼為相同的影像格式時保留中繼資料，有方法可在單一作業中複製所有中繼資料。 這些作業都遵循類似的模式;每個都會將已解碼的框架中繼資料直接設定為所編碼的新框架。

複製中繼資料的慣用方法是使用已解碼框架的區塊讀取器來初始化新框架的區塊寫入器。 下列程式碼示範這個方法。


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



在此範例中，會分別從來源畫面格和目的框架取得區塊讀取器和區塊寫入器。 區塊寫入器接著會從封鎖讀取器初始化。 這會以封鎖讀取器預先填入的中繼資料來初始化封鎖讀取器。

複製中繼資料的另一個方法是使用編碼器的查詢寫入器來寫入查詢讀取器所參考的中繼資料區塊。 下列程式碼示範這個方法。


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



在這裡，會從已解碼的框架取得查詢讀取器，然後用來做為 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 的屬性值，並將值型別設定為 VT \_ UNKNOWN。 會取得編碼器的查詢寫入器，並使用查詢運算式 "/" 來設定根導覽路徑的中繼資料。 您也可以在設定 nested 中繼資料區塊時使用這個方法，方法是將查詢運算式調整至所需的位置。

同樣地，您也可以使用映射處理站的 **CreateQueryWriterFromReader** 方法，根據已解碼框架的查詢讀取器來建立查詢寫入器。 在這項作業中建立的查詢寫入器將會使用查詢讀取器中的中繼資料預先填入，然後可以在框架中設定。 下列程式碼示範 **CreateQueryWriterFromReader** 複製作業。


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



這個方法會根據查詢讀取器的資料來建立個別的查詢寫入器。 這個新的查詢寫入器接著會在框架中設定。

同樣地，只有當來源和目的地映射的格式相同時，才會使用這些複製中繼資料的作業。 這是因為不同的影像格式會將中繼資料區塊儲存在不同的位置。 舉例來說，JPEG 和 TIFF 都支援 XMP 中繼資料區塊。 在 JPEG 影像中，XMP 區塊位於「 [WIC 中繼資料」總覽](-wic-about-metadata.md)中所述的根中繼資料區塊。 不過，在 TIFF 影像中，XMP 區塊會嵌套在根目錄的 IFD 區塊中。 下圖說明 JPEG 影像與具有相同評等中繼資料的 TIFF 影像之間的差異。

![jpeg 和 tiff 比較。](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a>快速中繼資料編碼

不一定需要重新編碼影像，才能將新的中繼資料寫入其中。 您也可以使用快速的中繼資料編碼器來寫入中繼資料。 快速中繼資料編碼器可將有限數量的中繼資料寫入影像，而不需要重新編碼影像。 這是藉由在部分元資料格式所提供的空白填補內撰寫新的中繼資料來完成。 支援中繼資料填補的原生元資料格式為 Exif、IFD、GPS 和 XMP。

### <a name="adding-padding-to-metadata-blocks"></a>將填補加入中繼資料區塊

您必須要有中繼資料區塊內的空間來寫入更多中繼資料，才能執行快速中繼資料編碼。 如果現有填補內沒有足夠的空間來寫入新的中繼資料，快速中繼資料編碼將會失敗。 若要在影像中加入中繼資料填補，必須重新編碼影像。 如果您要填補的中繼資料區塊支援，您可以使用查詢運算式，以新增任何其他中繼資料專案的相同方式加入填補。 下列範例示範如何將填補新增至內嵌于 App1 區塊中的 IFD 區塊。


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



若要加入填補，請建立 VT UI4 類型的 PROPVARIANT \_ ，以及對應至要加入的填補位元組數目的值。 一般值為4096個位元組。 JPEG、TIFF 和 JPEG XR 的中繼資料查詢是在此表格中。



| 元資料格式 | JPEG 中繼資料查詢                  | TIFF，JPEG XR 中繼資料查詢    |
|-----------------|--------------------------------------|---------------------------------|
| IFD             | /app1/ifd/PaddingSchema：填補      | /ifd/PaddingSchema：填補      |
| EXIF            | /app1/ifd/exif/PaddingSchema：填補 | /ifd/exif/PaddingSchema：填補 |
| XMP             | /xmp/PaddingSchema：填補           | /ifd/xmp/PaddingSchema：填補  |
| GPS             | /app1/ifd/gps/PaddingSchema：填補  | /ifd/gps/PaddingSchema：填補  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a>取得快速中繼資料編碼器

當您擁有具有中繼資料填補的影像時，可以使用映射處理站方法 **CreateFastMetadataEncoderFromDecoder** 和 **CreateFastMetadataEncoderFromFrameDecode** 來取得快速中繼資料編碼器。

顧名思義， **CreateFastMetadataEncoderFromDecoder** 會為編碼器層級的中繼資料建立快速的中繼資料編碼器。 WIC 提供的原生影像格式不支援解碼器層級的中繼資料，但在未來開發影像格式的情況下，會提供此方法。

較常見的案例是使用 **CreateFastMetadataEncoderFromFrameDecode** 從影像框架取得快速的中繼資料編碼器。 下列程式碼會取得已解碼的框架快速中繼資料編碼器，並變更 App1 區塊中的分級值。


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a>使用快速中繼資料編碼器

您可以從快速中繼資料編碼器取得查詢寫入器。 這可讓您使用先前所示範的查詢運算式來寫入中繼資料。 在查詢寫入器中設定中繼資料之後，請認可快速中繼資料編碼器來完成中繼資料更新。 下列程式碼示範如何設定和認可中繼資料變更。


```
    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



如果 **Commit** 因為任何原因而失敗，您將需要重新編碼影像，以確保新的中繼資料會加入至映射。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC 中繼資料總覽](-wic-about-metadata.md)
</dt> <dt>

[中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[中繼資料擴充性總覽](-wic-codec-metadatahandlers.md)
</dt> <dt>

[How to：使用中繼資料重新編碼 JPEG 影像](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
