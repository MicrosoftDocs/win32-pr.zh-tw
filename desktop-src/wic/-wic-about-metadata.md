---
description: 本主題介紹 Windows 影像處理元件 (WIC) 所提供的映射中繼資料支援。
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: WIC 中繼資料總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f5031759dd73861a97aace623b35f229b75952
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472024"
---
# <a name="wic-metadata-overview"></a>WIC 中繼資料總覽

本主題介紹 Windows 影像處理元件 (WIC) 所提供的映射中繼資料支援。 它提供讀取和寫入影像中繼資料、中繼資料查詢語言和元資料處理程式擴充性的簡介。

影像中繼資料是內嵌在影像檔內的資料，可提供映射的其他相關資訊，例如用來捕捉影像的裝置，或影像的維度。 雖然它包含在影像檔案本身內，但此中繼資料不是轉譯資料的一部分。 WIC 提供的介面可讓您針對數種常見的元資料格式讀取和寫入此中繼資料，包括可延伸的中繼資料平臺 (XMP) 、交換影像檔 (EXIF) ，以及 Png 文字資料 (文字) 。

本主題包含下列各節。

-   [先決條件](#prerequisites)
-   [簡介](#introduction)
-   [讀取影像中繼資料](#reading-image-metadata)
-   [寫入影像中繼資料](#writing-image-metadata)
-   [中繼資料擴充性](#metadata-extensibility)
-   [支援的元資料格式](#supported-metadata-formats)
-   [中繼資料元件摘要](#metadata-component-summary)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

若要瞭解本主題，您應該熟悉 WIC 編碼器和解碼器介面，以及其相關元件物件模型 (COM) 元件，如[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)所述。 它也有助於讓您大致熟悉目前使用的一些影像處理元資料格式。

## <a name="introduction"></a>簡介

中繼資料提供有關影像的延伸資訊。 這項資訊可以用數種方式來使用。 影像可能包含中繼資料，例如描述、評等、類別標記和著作權資訊。 存取中繼資料可讓您更輕鬆地執行工作，例如資產管理、檔案位置或決定著作權資訊。 例如，Windows Vista 中的 Windows 影像中心可讓您將描述和分類標記新增至影像。 這可讓您更有效率地探索映射，並提供方便的方式來分類影像。 使用 WIC Api 和通用元資料格式，應用程式可以輕鬆地將這類的中繼資料寫入或讀取至影像。

下圖說明 JPEG 檔案的內容，其中包含內嵌的中繼資料區塊和中繼資料專案。

![具有評等中繼資料的 jpeg 影像](graphics/jpeg.png)

在此範例影像中，中繼資料會內嵌在影像檔案框架內的影像檔案中。 JPEG 格式不支援多個影像框架，因此中繼資料在概念上會附加到這個單一框架。 支援多個框架的格式（例如 TIFF）可能會有附加至每個影像框架的中繼資料，如圖所示。 雖然目前並不受原生映射編解碼器支援，有些影像格式也可以支援影像框架以外的中繼資料。 WIC 有足夠的彈性，可處理影像個別框架以外的框架層級中繼資料和中繼資料。

## <a name="reading-image-metadata"></a>讀取影像中繼資料

WIC Api 提供 COM 元件，可讓應用程式輕鬆地讀取和寫入影像中繼資料。

讀取中繼資料的主要方法是使用中繼資料查詢讀取器 ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) 來存取特定的中繼資料專案。 中繼資料查詢讀取器元件是由編解碼器所執行，而且可以在解碼器層級或透過個別的影像框架（這是較常見的方法）來存取。 下列程式碼示範如何使用查詢讀取器的 **GetMetadataQueryReader** 方法，來存取個別框架的查詢讀取器。


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



查詢讀取器會提供方法來取得特定中繼資料的相關資訊，以及用來指定要抓取之中繼資料專案的方法。 下列程式碼會使用查詢運算式，要求 (IFD) 區塊的 App1 嵌套影像檔案目錄內的特定中繼資料專案。 這是藉由使用查詢讀取器的 **GetMetadataByName** 方法來完成。 下列程式碼示範如何使用查詢讀取器來取得 MicrosoftPhoto 分級值。


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



上述範例中的 pwzRatingQuery 變數是用來存取中繼資料專案 MicrosoftPhoto 評等的查詢字串。 這個字串是使用中繼資料查詢語言建立的。 若要建立這個字串，需要知道元資料格式和中繼資料查詢語言，才能取得個別的中繼資料專案。 如需有關中繼資料查詢語言的詳細資訊，請參閱 [中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)。

在幕後，查詢讀取器會使用中繼資料讀取器 ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) 來存取查詢運算式所描述的中繼資料。 除了使用查詢讀取器，您也可以直接存取中繼資料讀取器來讀取中繼資料。 您可以藉由查詢區塊讀取器 ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) 介面，從解碼器或個別的框架取得中繼資料讀取器。

## <a name="writing-image-metadata"></a>寫入影像中繼資料

寫入中繼資料的程式與讀取的方式類似，差別在於使用中繼資料查詢寫入器 ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) 。 查詢編寫器介面是由影像編碼器所執行，而且在查詢讀取器中，中繼資料會在編碼器和個別畫面上 (存取，視影像格式支援) 而定。

下列程式碼示範如何從編碼器框架取得查詢寫入器，並移除先前讀取的分級值。


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



寫入中繼資料的另一種方式是透過快速中繼資料更新。 快速中繼資料編碼是一種寫入影像中繼資料的方式，而不需要重新編碼影像檔案。 這是藉由將新的中繼資料資訊寫入元資料格式的填補區域來完成。 快速中繼資料編碼器 ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) 是從元件 factory 取得（以映射編碼器為基礎）。 快速中繼資料編碼器接著會取得用來寫入中繼資料的查詢寫入器。 最後，快速編碼器會認可變更。

下列程式碼示範如何取得快速的中繼資料編碼器，並使用它來寫入 MicrosoftRating 值。


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

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



並非所有的元資料格式都支援快速中繼資料。 若要查看支援快速中繼資料編碼的原生支援格式，請參閱本檔稍後的 [支援的元資料格式](#supported-metadata-formats) 一節中的表格。

在幕後，查詢寫入器會使用中繼資料寫入器 ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) 來寫入查詢運算式所描述的中繼資料。 除了使用查詢讀取器之外，您也可以直接存取中繼資料寫入器來寫入中繼資料。 您可以使用查詢區塊寫入器 ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) 介面，從解碼器或個別的框架取得中繼資料寫入器。

## <a name="metadata-extensibility"></a>中繼資料擴充性

如先前所述，WIC 提供數個元資料處理程式來讀取和寫入一般元資料格式的中繼資料。 不過，有些元資料格式並非原生支援。 因此，WIC 會提供 Api 來建立可將中繼資料支援延伸至其他格式的其他元資料處理程式。

若要完全支援其他元資料格式，必須開發兩種類型的處理常式：中繼資料讀取器，用來讀取中繼資料和中繼資料寫入器來寫入中繼資料。 雖然這兩個處理常式通常會以特定格式的配對來執行，但這不是必要條件。 在某些情況下，可能只有讀取能力或只需要寫入功能。

如需有關使用 WIC Api 的中繼資料擴充性的詳細資訊，請參閱 [中繼資料](-wic-codec-metadatahandlers.md)擴充性總覽。

## <a name="supported-metadata-formats"></a>支援的元資料格式

WIC 提供數種常見元資料格式的支援。 下表列出支援的元資料格式、其版本、支援元資料格式的影像格式，以及元資料格式是否支援快速中繼資料編碼。 如需快速中繼資料編碼的詳細資訊，請參閱本檔稍早的「 [撰寫映射中繼資料](#writing-image-metadata) 」一節。



| 支援的元資料格式 | 中繼資料規格版本 | 影像格式支援 | 支援快速中繼資料編碼 |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | JFIF 1.02                      | JPEG                 | 否                              |
| App1                       | JFIF 1.02                      | JPEG、TIFF           | 否                              |
| App13                      | Unknown                        | JPEG、TIFF           | 否                              |
| IFD                        | TIFF 6。0                       | JPEG、TIFF           | 是                             |
| IRB                        | Unknown                        | JPEG、TIFF           | 否                              |
| Exif                       | Exif 2。2                       | JPEG、TIFF           | 是                             |
| XMP                        | XMP 1.0 (9 月 2005)             | JPEG、TIFF           | 是                             |
| GPS                        | Exif 2。2                       | JPEG、TIFF           | 是                             |
| IPTC                       | IPTC 4。0                       | JPEG、TIFF           | 是                             |
| 文本                       | PNG 1。2                        | PNG                  | 否                              |



 

> [!Note]  
> 如果區塊的大小成長，則 IPTC 只支援 FME，因為 IPTC 不支援填補。

 

## <a name="metadata-component-summary"></a>中繼資料元件摘要

下表描述支援中繼資料的 WIC 介面，以及其對應的元件。 這些元件提供映射中繼資料的存取權。 如需這些元件的詳細資訊，請參閱[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)。 


| 元件 | 描述 | 
|-----------|-------------|
| 點陣圖解碼 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)  | <ul><li>讀取影像資料流程並產生可用的點陣圖來源。 與容器格式相關聯，例如標記的影像檔案格式 (TIFF) 或 (JPEG) 的聯合攝影專家群組。</li><li>執行 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> 介面，以列舉不在框架內的解碼器資料流程中的所有中繼資料區塊。</li><li>公開查詢讀取器，以讀取與不在框架內的影像相關聯的中繼資料。</li></ul> | 
| 點陣圖框架解碼 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)  | <ul><li>從解碼器所持有的影像串流存取個別的畫面格。</li><li>實 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> 介面，以列舉框架資料流程中的所有中繼資料區塊。</li><li>使用查詢運算式來公開查詢讀取器，以讀取與框架相關聯的中繼資料。</li></ul> | 
| 點陣圖編碼器 (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)  | <ul><li>將點陣圖來源寫入影像資料流程。 與容器格式相關聯，例如 TIFF 或 JPEG。</li><li>執行 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> 介面，以建立要寫入編碼器資料流程的中繼資料區塊清單。</li><li>使用查詢運算式，公開查詢寫入器來寫入與影像相關聯的中繼資料。</li></ul> | 
| Bitma 框架編碼 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)  | <ul><li>建立將編碼為編碼器所持有之資料流程的框架。</li><li>實 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> 介面，以建立要寫入框架資料流程的中繼資料區塊清單。</li><li>使用查詢運算式，公開查詢寫入器來寫入與框架相關聯的中繼資料。</li></ul> | 




 

下表描述 WIC 中繼資料元件。 這些元件可讓您在上表所列的元件所公開的影像中讀取和寫入中繼資料。 


| 元件 | 描述 | 
|-----------|-------------|
| 中繼資料查詢讀取器 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)  | <ul><li>接受查詢字串，並流覽基礎中繼資料階層以取得中繼資料。</li></ul> | 
| 中繼資料查詢寫入器 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)  | <ul><li>接受查詢字串，並流覽基礎中繼資料階層以取得、設定和移除中繼資料。</li></ul> | 
| 中繼資料區塊讀取器 (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)  | <ul><li>管理位於中繼資料階層最上方之 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> 物件的唯讀集合，並啟用所有中繼資料區塊的列舉。</li><li>由點陣圖解碼器和解碼點陣圖框架所執行。</li><li>由協力廠商元件開發人員為自訂編解碼器所執行。</li></ul> | 
| 中繼資料區塊寫入器 (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)  | <ul><li>管理中繼資料階層頂端 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> 物件的讀取和寫入集合。</li><li>由點陣圖編碼器和點陣圖框架編碼所執行。</li><li>由協力廠商元件開發人員為自訂編解碼器所執行。</li></ul> | 
| 中繼資料讀取器 (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)  | <ul><li>剖析中繼資料的資料流程，並管理中繼資料專案的唯讀集合。 與元資料格式（如 EXIF、IFD 和 XMP）相關聯。</li><li>作為字典，並在給定格式和識別碼時傳回值。</li><li>由自訂元資料類型的協力廠商元件開發人員所執行。</li></ul> | 
| 中繼資料寫入器 (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)  | <ul><li>剖析和序列化中繼資料的資料流程，並管理中繼資料專案的讀取/寫入集合。</li><li>由自訂元資料類型的協力廠商元件開發人員所執行。</li></ul> | 
| 快速中繼資料編碼器<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a> | <ul><li>公開寫入中繼資料階層的語義，這些中繼資料會就地更新中繼資料，而不需要重新編碼影像。</li></ul> | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[中繼資料擴充性總覽](-wic-codec-metadatahandlers.md)
</dt> <dt>

[How to：使用中繼資料重新編碼 JPEG 影像](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



