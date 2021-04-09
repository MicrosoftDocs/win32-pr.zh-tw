---
description: 本主題將介紹新的可延伸中繼資料平臺 (XMP) 架構和 Windows 7 相片屬性 PeopleNames，可讓您在數位相片中標記個人。
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: 人員標記總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115777"
---
# <a name="people-tagging-overview"></a>人員標記總覽

本主題將介紹新的可延伸中繼資料平臺 (XMP) 架構和 Windows 7 相片屬性 [PeopleNames](../properties/props-system-photo-peoplenames.md) ，可讓您在數位相片中標記個人。 本主題也會討論如何使用 Windows 影像處理元件 (WIC) API 來讀取和寫入人員標記所需的中繼資料。

本主題包含下列各節。

-   [先決條件](#prerequisites)
-   [簡介](#introduction)
-   [人員標記](#people-tagging-overview)
    -   [人員名稱](#people-names)
    -   [人員矩形](#people-rectangles)
-   [架構參考](#schema-reference)
    -   [Microsoft Photo 1.2 架構](#microsoft-photo-12-schema)
    -   [Microsoft Photo RegionInfo 架構](#microsoft-photo-regioninfo-schema)
    -   [Microsoft 相片區域架構](#microsoft-photo-regioninfo-schema)
    -   [範例中繼資料](#sample-metadata)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

若要瞭解本主題，您應該熟悉 WIC 解碼介面及其相關元件物件模型 (COM) 元件，如 [Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)所述。 它也有助於對影像處理中繼資料（尤其是 XMP）有大致熟悉。

## <a name="introduction"></a>簡介

Microsoft 建立了新的 XMP 架構來標記數位影像內的人員。 此架構可讓應用程式將影像中的個人名稱和位置，儲存為影像內的中繼資料。 除了新的架構，Windows 7 也提供新的相片屬性 [PeopleNames](../properties/props-system-photo-peoplenames.md) 。 這個新的屬性可讓應用程式讀取儲存在影像中繼資料中的個人名稱。 WIC 利用這些新功能，可讓應用程式輕鬆地讀取和寫入人員標記中繼資料到數位相片。

## <a name="people-tagging"></a>人員標記

WIC 為應用程式開發人員提供讀取影像資料和影像中繼資料的 COM 元件。 針對讀取和寫入中繼資料（例如新的人員標記功能），WIC 提供 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) 和 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 介面。 這些介面可讓應用程式使用 [中繼資料查詢語言](-wic-codec-metadataquerylanguage.md) ，將中繼資料寫入影像的個別框架。 下一節示範如何使用 WIC 查詢讀取器和寫入器，將人員標記中繼資料讀取及寫入影像的中繼資料中。

### <a name="people-names"></a>人員名稱

人物標記功能的一部分，就是能夠直接取得在影像內標記的人員名稱清單。 [PeopleNames](../properties/props-system-photo-peoplenames.md)和 WIC 的元資料處理程式都支援這部分的功能。 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)介面與 PeopleNames 屬性搭配使用，可讀取影像中所識別的人員名稱，並儲存在影像中繼資料中。

下列程式碼範例示範從影像框架取得的查詢讀取器，以查詢影像的中繼資料是否有 [PeopleNames](../properties/props-system-photo-peoplenames.md) 屬性的標記名稱。


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



查詢運算式 "PeopleNames" 會查詢屬性的框架。 如果人物標記中繼資料存在且包含人員的名稱， [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 值將會設定為 VT LPWSTR， \_ 而且資料值將會包含已標記名稱的清單。 如需有關讀取影像中繼資料的詳細資訊，請參閱 [讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)。

如果影像實際包含人物標記中繼資料，則查詢 [人員名稱] 標籤只會很有用。 若要執行此程式，應用程式必須先撰寫它。 若要撰寫人員名稱中繼資料，請使用中繼資料的 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 和明確的 XMP 路徑。 下列程式碼範例將示範如何使用查詢寫入器，將名稱寫入至查詢路徑。


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



請注意建立 XMP 結構並設定它的步驟 `MPRI:Regions/{ulong=0}` 。 若未執行此步驟，WIC 將無法識別稍後要放置的位置 `PersonDisplayName` 。 另請注意，系統會使用明確的查詢路徑，而不是 [PeopleNames](-wic-photoprop-system-photo-peoplenames.md)，其中繼資料原則不支援寫入中繼資料。

### <a name="people-rectangles"></a>人員矩形

不過，人們的名字只是人員標記功能的一部分。 除了在中繼資料中儲存人員的名稱之外，架構也支援區域資訊，識別特定區域 (矩形) 該人員顯示于影像中。

矩形資訊會以四個逗號分隔的十進位值來表示，例如 "0.25，0.25，0.25，0.25"。 前兩個值指定左上角座標;最後兩個指定矩形的高度和寬度。 用來定義人物矩形的影像維度會正規化為1，這表示在 "0.25，0.25，0.25，0.25" 範例中，矩形會從影像左邊距離的上到上距離的距離開始的1/4。 矩形的高度和寬度都是其個別影像維度大小的1/4。

識別個人的矩形資訊會以與人員名稱相同的方式寫入，在相同的結構內。 若要撰寫矩形中繼資料，請使用中繼資料的 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 和明確的 XMP 路徑。 下列程式碼範例會繼續上一個範例，並將代表 ' John Doe ' 的矩形加入至映射的中繼資料。 請注意，它會使用相同的 `{ulong=0}` 索引，將這個矩形與 ' John Doe ' 產生關聯。


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a>結構描述參考

適用于人員標記的 Microsoft XMP 架構會定義一組屬性，以在數位相片中標記個人。

下列各節提供人員標記所需的架構定義。 架構定義盡可能使用 Adobe 的可延伸中繼資料平臺所提供的慣例 [ (XMP) 規格](https://www.adobe.com/devnet/xmp/)。 本主題中的架構定義會顯示 XML 命名空間統一資源識別元 (URI) 來識別架構和慣用的架構命名空間前置詞，後面接著列出針對架構定義的所有屬性的資料表。 每個資料表都有下列資料行：

-   **Property** -屬性的名稱，包括慣用的命名空間前置詞。

-   **數值型別** -屬性的數值型別。 人員標記支援架構會盡可能使用 XMP 實數值型別，包括日期和文字。 陣列類型的前面會有容器類型： `alt` 、 `bag` 或 `seq` 。

-   **類別** 架構屬性是內部或外部：

    -   內部中繼資料必須由應用程式設定。

    -   外部中繼資料必須由使用者設定，而且與檔的內容無關。

-   **描述** -屬性的描述。

### <a name="microsoft-photo-12-schema"></a>Microsoft Photo 1.2 架構

Microsoft Photo 1.2 架構為影像區域提供一組屬性。

-   架構命名空間 URI 為 `https://ns.microsoft.com/photo/1.2/` 。
-   慣用的架構命名空間前置詞為 `MP` 。



| 屬性      | 值類型 | 類別 | 描述                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP： RegionInfo | RegionInfo | 內部 | **必要** ：儲存人物標記中繼資料的根目錄。 請參閱下面的「Microsoft Photo RegionInfo 架構」一節。 |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Microsoft Photo RegionInfo 架構

Microsoft Photo RegionInfo 1.2 架構會提供一組區域資訊的屬性。

-   架構命名空間 URI 為 `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` 。
-   慣用的架構命名空間前置詞為 `MPRI` 。



| 屬性              | 值類型 | 類別 | 描述                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI:DateRegionsValid | Date       | 外部 | **選用** ：上次建立區域的日期。                                                          |
| MPRI：區域          | 包區域 | 外部 | **必要** ：儲存人物標記區域。 請參閱下面的「Microsoft 照片區域架構」一節。 |



 

### <a name="microsoft-photo-region-schema"></a>Microsoft 相片區域架構

Microsoft Photo Region 1.2 架構為影像區域提供一組屬性。

-   架構命名空間 URI 為 `https://ns.microsoft.com/photo/1.2/t/Region#` 。
-   慣用的架構命名空間前置詞為 `MPReg` 。



| MPReg：屬性          | 值類型 | 類別 | 描述                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPReg:PersonDisplayName | Text       | 外部 | **必要** ：將人員的名稱儲存在指定的矩形中。                                                                                                                                                                                                                                            |
| MPReg：矩形         | Text       | 外部 | **選擇性** ：儲存用來識別相片中人員的矩形。 矩形會儲存為四個以逗號分隔的十進位值。 前兩個值會指定左上角座標;最後兩個指定矩形的高度和寬度。 十進位值必須正規化為1。 |
| MPReg:PersonEmailDigest | Text       | 外部 | **選擇性** ：儲存人員的即時電子郵件地址的 sha-1 加密訊息雜湊。                                                                                                                                                                                                                     |
| MPReg:PersonLiveIdCID   | Text       | 外部 | **選擇性** ：儲存人員的即時 CID 帶正負號的十進位標記法，這是公開識別即時身分識別的64位整數。                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>範例中繼資料

以下是人員標記的 XMP 中繼資料標記法。

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC 中繼資料總覽](-wic-about-metadata.md)
</dt> <dt>

[讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
