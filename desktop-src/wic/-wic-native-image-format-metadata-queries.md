---
description: 本主題概要說明用來讀取和寫入 GIF、PNG、TIFF 和 JPEG 影像所支援中繼資料的中繼資料查詢語言查詢。
ms.assetid: a6ab1708-dd82-4960-b908-f1daef7374ef
title: 原生影像格式中繼資料查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be5e9c0f853e4c5e48fb5eb41f2d2ab27b4f4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997559"
---
# <a name="native-image-format-metadata-queries"></a>原生影像格式中繼資料查詢

本主題概要說明用來讀取和寫入 GIF、PNG、TIFF 和 JPEG 影像所支援中繼資料的 [中繼資料查詢語言](-wic-codec-metadataquerylanguage.md) 查詢。它包含每個影像格式的特定中繼資料，以及多個格式所支援的中繼資料。

本主題包含下列各節。

-   [先決條件](#prerequisites)
-   [相片中繼資料原則運算式](#photo-metadata-policy-expression)
-   [檔案格式的特定中繼資料](#file-format-specific-metadata)
    -   [GIF 中繼資料](#gif-metadata)
    -   [PNG 中繼資料](#png-metadata)
    -   [TIFF 中繼資料](#tiff-metadata)
    -   [JPEG 中繼資料](#jpeg-metadata)
-   [檔案格式獨立中繼資料](#file-format-independent-metadata)
    -   [IFD 中繼資料](#ifd-metadata)
    -   [EXIF 中繼資料](#exif-metadata)
    -   [GPS 中繼資料](#gps-metadata)
    -   [XMP 中繼資料](#xmp-metadata)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

若要瞭解本主題，您應該熟悉 [Wic 中繼資料總覽](-wic-about-metadata.md)中所述的 WINDOWS 影像處理元件 (wic) 中繼資料系統。 您也應該熟悉用來讀取和寫入中繼資料的查詢語言，如 [中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)中所述。

## <a name="photo-metadata-policy-expression"></a>相片中繼資料原則運算式

除了支援中繼資料查詢語言之外， [WIC](-wic-api.md) 也接受來自 [Windows 屬性系統](../properties/windows-properties-system.md)的標準屬性名稱。 WIC 支援與影像格式相關的 Windows 屬性命名空間子集，如 [相片中繼資料原則](photo-metadata-policies.md)中所述。 用作 WIC 中繼資料查詢的 Windows 屬性稱為相片中繼資料原則運算式。

例如，EXIF 方向旗標的相片中繼資料原則運算式為：

-   [[列印]](-wic-photoprop-system-photo-orientation.md)

一般情況下，建議使用原則運算式，而不是 Windows 屬性命名空間所涵蓋之一般影像中繼資料專案的原生中繼資料查詢。 中繼資料查詢語言最適合用來存取特定影像中繼資料專案的低層級存取，或適用于 Windows 屬性系統不支援的自訂或 advanced 中繼資料專案。 如需詳細資訊，請參閱 [照片中繼資料原則運算式](-wic-codec-metadataquerylanguage.md)。

## <a name="file-format-specific-metadata"></a>檔案格式的特定中繼資料

下列各節包含的資料表會列出每個圖像檔案類型的可用中繼資料查詢。 每個資料表都有下列資料行：

-   **路徑** -用來取得中繼資料專案的查詢路徑。
-   **名稱** -中繼資料專案的名稱。
-   **Type** -從查詢路徑取出的中繼資料專案類型。 [WIC](-wic-api.md)取出的中繼資料會以 PROPVARIANT 的形式傳回，此格式會使用 VARTYPE 列舉來報告資料類型。

WIC 中繼資料 API 會使用查詢路徑來存取影像的內嵌中繼資料。 下列範例程式碼示範如何使用 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) 來查詢 JPEG 的 IFD 中繼資料區塊。


```
// Not shown: image decoding 
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pIFDReader = NULL;

// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

if (SUCCEEDED(hr))
{
    // Get the nested IFD reader.
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pIFDReader);
    }
    PropVariantClear(&value); // Clear value for new query.
}
```



### <a name="gif-metadata"></a>GIF 中繼資料

圖形交換格式 (GIF) 影像格式同時支援全域和框架層級的中繼資料。 下列兩節提供適用于 GIF 全域和框架層級中繼資料的中繼資料查詢路徑。

> [!Note]  
> 如需 GIF 中繼資料的完整清單以及更詳細的資訊，請參閱 W3C 網站上的 [gif 標準](https://www.w3.org/Graphics/GIF/spec-gif89a.txt) 。

 

### <a name="global-metadata"></a>全域中繼資料

下表提供可用來存取全域 GIF 中繼資料的可用中繼資料查詢路徑。



| 路徑                                               | 名稱                       | 類型                                |
|----------------------------------------------------|----------------------------|-------------------------------------|
| /commeNtext 或/ \[ \* \] commeNtext，其中 \* = 0 到 N | 批註延伸          | VT \_ 未知-查詢讀取器/寫入器 |
| /commeNtext/TextEntry                              |                            | VT \_ LPSTR                           |
| /logscrdesc                                        | 邏輯螢幕描述 | VT \_ 未知-查詢讀取器/寫入器 |
| /logscrdesc/Signature                              |                            | VT \_ UI1 \| vt \_ 向量               |
| /logscrdesc/Width                                  |                            | VT \_ UI2                             |
| /logscrdesc/Height                                 |                            | VT \_ UI2                             |
| /logscrdesc/GlobalColorTableFlag                   |                            | VT \_ BOOL                            |
| /logscrdesc/ColorResolution                        |                            | VT \_ UI1                             |
| /logscrdesc/SortFlag                               |                            | VT \_ BOOL                            |
| /logscrdesc/GlobalColorTableSize                   |                            | VT \_ UI1                             |
| /logscrdesc/BackgroundColorIndex                   |                            | VT \_ UI1                             |
| /logscrdesc/PixelAspectRatio                       |                            | VT \_ UI1                             |
| /appext 或/ \[ \* \] appext，其中 \* = 0 到 N         | 應用程式延伸模組      | VT \_ 未知-查詢讀取器/寫入器 |
| /appext/Application                                |                            | VT \_ UI1 \| vt \_ 向量               |
| /appext/Data                                       |                            | VT \_ UI1 \| vt \_ 向量               |



 

### <a name="frame-metadata"></a>框架中繼資料

下表提供可用來存取框架層級 GIF 中繼資料的可用中繼資料查詢路徑。



| 路徑                            | 名稱                      | 類型                              |
|---------------------------------|---------------------------|-----------------------------------|
| /grctlext                       | 圖形控制項延伸模組 | VT \_ 未知-查詢讀取器/寫入器 |
| /grctlext/Disposal              |                           | VT \_ UI1                           |
| /grctlext/UserInputFlag         |                           | VT \_ BOOL                          |
| /grctlext/TransparencyFlag      |                           | VT \_ BOOL                          |
| /grctlext/Delay                 |                           | VT \_ UI2                           |
| /grctlext/TransparentColorIndex |                           | VT \_ UI1                           |
| /imgdesc                        | 映射描述項          | VT \_ 未知-查詢讀取器/寫入器 |
| /imgdesc/Left                   |                           | VT \_ UI2                           |
| /imgdesc/Top                    |                           | VT \_ UI2                           |
| /imgdesc/Width                  |                           | VT \_ UI2                           |
| /imgdesc/Height                 |                           | VT \_ UI2                           |
| /imgdesc/LocalColorTableFlag    |                           | VT \_ BOOL                          |
| /imgdesc/InterlaceFlag          |                           | VT \_ BOOL                          |
| /imgdesc/SortFlag               |                           | VT \_ BOOL                          |
| /imgdesc/LocalColorTableSize    |                           | VT \_ UI1                           |



 

### <a name="png-metadata"></a>PNG 中繼資料

可移植網狀圖形 (PNG) 影像格式支援框架層級中繼資料。

> [!Note]  
> 如需 PNG 中繼資料的完整清單以及更詳細的資訊，請參閱 W3C 網站上的 [png 標準](https://www.w3.org/TR/PNG/) 。

 

### <a name="frame-metadata"></a>框架中繼資料

下表提供可用來存取框架層級 PNG 中繼資料的可用中繼資料查詢路徑。



| 路徑                                                   | 名稱             | 類型                                      |
|--------------------------------------------------------|------------------|-------------------------------------------|
| /tEXt 或/ \[ \* \] 文字，其中 \* = 0 到 N                 | 文字區塊       | VT \_ 未知-文字查詢讀取器/寫入器    |
| /tEXt/{str = \* } where \* = 標識關鍵字的文字 |                  | VT \_ LPSTR                                 |
| /gAMA                                                  | Gama 區塊       | VT \_ 未知-gAMA 查詢讀取器/寫入器    |
| /gAMA/ImageGamma                                       |                  | VT \_ UI4                                   |
| /iTXt 或/ \[ \* \] iTXt，其中 \* = 0 到 N                 | IText 區塊      | VT \_ 未知-iTXt 查詢讀取器/寫入器    |
| /iTXt/Keyword                                          |                  | VT \_ LPSTR                                 |
| /iTXt/CompressionFlag                                  |                  | VT \_ UI1                                   |
| /iTXt/LanguageTag                                      |                  | LPSTR                                     |
| /iTXt/TranslatedKeyword                                |                  | LPWSTR                                    |
| /iTXt/TextEntry                                        |                  | LPWSTR                                    |
| /cHRM                                                  | HRM 區塊        | VT \_ 未知-cHRM 查詢讀取器/寫入器    |
| /cHRM/WhitePointX                                      |                  | VT \_ UI4                                   |
| /cHRM/WhitePointY                                      |                  | VT \_ UI4                                   |
| /cHRM/RedX                                             |                  | VT \_ UI4                                   |
| /cHRM/RedY                                             |                  | VT \_ UI4                                   |
| /cHRM/GreenX                                           |                  | VT \_ UI4                                   |
| /cHRM/GreenY                                           |                  | VT \_ UI4                                   |
| /cHRM/BlueX                                            |                  | VT \_ UI4                                   |
| /cHRM/BlueY                                            |                  | VT \_ UI4                                   |
| /sRGB                                                  | sRGB Chuck       | VT \_ 未知-sRGB 查詢讀取器/寫入器    |
| /sRGB/RenderingIntent                                  |                  | VT \_ UI1                                   |
| /tIME                                                  | 時間區塊       | VT \_ 未知時間查詢讀取器/寫入器    |
| /tIME/Year                                             |                  | VT \_ UI2                                   |
| /tIME/Month                                            |                  | VT \_ UI1                                   |
| /tIME/Day                                              |                  | VT \_ UI1                                   |
| /tIME/Hour                                             |                  | VT \_ UI1                                   |
| /tIME/Minute                                           |                  | VT \_ UI1                                   |
| /tIME/Second                                           |                  | VT \_ UI1                                   |
| /bKGD                                                  | 背景區塊 | VT \_ 未知-bKGB 查詢讀取器/寫入器    |
| /bKGD/BackgroundColor                                  |                  | VT \_ UI1、vt \_ UI2 或 vt \_ UI2 \| vt \_ 向量 |
| /hIST                                                  | >hist 區塊       | VT \_ 未知->hist 查詢讀取器/寫入器    |
| /hIST/Frequencies                                      |                  | VT \_ 向量 \| vt \_ UI2                     |
| /iCCP                                                  | iCCP 區塊       | VT \_ 未知-iCCP 查詢讀取器/寫入器    |
| /iCCP/ProfileName                                      |                  | VT \_ LPSTR                                 |
| /iCCP/ProfileData                                      |                  | VT \_ 向量 \| vt \_ UI1                     |



 

### <a name="tiff-metadata"></a>TIFF 中繼資料

標記的影像檔案格式 (TIFF) 影像格式支援框架層級中繼資料。

> [!Note]  
> 如需 TIFF 中繼資料的完整清單以及更詳細的資訊，請參閱 [tiff 標準](https://www.adobe.io/content/dam/udp/en/open/standards/tiff/TIFF6.pdf)。

 

### <a name="frame-metadata"></a>框架中繼資料

下表提供可用來存取框架層級 TIFF 中繼資料的可用中繼資料查詢路徑。



| 路徑                                          | 名稱            | 類型                                |
|-----------------------------------------------|-----------------|-------------------------------------|
| /ifd                                          | 0 IFD           | VT \_ 未知-查詢讀取器/寫入器 |
| /ifd/{ushort = \* } where \* = 0 至65535        | 依識別碼的 IFD 專案 | 變數                            |
| /ifd/thumb 或/ifd/{ushort = 330}               | 縮圖 IFD   | VT \_ 未知-查詢讀取器/寫入器 |
| /ifd/xmp 或/ifd/{ushort = 700}                 | XMP             | VT \_ 未知-查詢讀取器/寫入器 |
| /ifd/exif 或/ifd/{ushort = 34665}              | Exif            | VT \_ 未知-查詢讀取器/寫入器 |
| /ifd/gps 或/ifd/{ushort = 34853}               | GPS             | VT \_ 未知-查詢讀取器/寫入器 |
| /ifd/exif/interop 或/ifd/exif/{ushort = 40965} | Interop         | VT \_ 未知-查詢讀取器/寫入器 |
| /ifd/iptc 或/ifd/{ushort = 33723}              | IPTC            | VT \_ 未知-查詢讀取器/寫入器 |
| /ifd/iptc/{str = \* } where \* = iptc 關鍵字    | IPTC 專案      | 變數                            |
| /ifd/irb/8bimiptc/iptc                        | IPTC            | VT \_ 未知-查詢讀取器/寫入器 |
| /ifd/irb/8bimiptc/iptc/{str = \* }               | IPTC 專案      | 變數                            |



 

### <a name="jpeg-metadata"></a>JPEG 中繼資料

JPEG 影像格式支援框架層級中繼資料。

> [!Note]  
> 如需 JPEG 中繼資料的完整清單以及更詳細的資訊，請參閱 [EXIF JPEG 標準](http://www.cipa.jp/std/documents/e/DC-008-2010_E.pdf)。

 

### <a name="frame-metadata"></a>框架中繼資料

下表提供可用來存取框架層級 JPEG 中繼資料的可用中繼資料查詢路徑。



| 路徑                                                               | 名稱                 | 類型                                          |
|--------------------------------------------------------------------|----------------------|-----------------------------------------------|
| /app0                                                              | App0                 | VT \_ 未知-App0 查詢讀取器/寫入器        |
| /app0/{ushort = 0}                                                   | 版本              | VT \_ UI2                                       |
| /app0/{ushort = 1}                                                   | 單位                | VT \_ UI1                                       |
| /app0/{ushort = 2}                                                   | DpiX                 | VT \_ UI2                                       |
| /app0/{ushort = 3}                                                   | DpiY                 | VT \_ UI2                                       |
| /app0/{ushort = 4}                                                   | Xthumbnail           | VT \_ UI1                                       |
| /app0/{ushort = 5}                                                   | Ythumbnail           | VT \_ UI1                                       |
| /app0/{ushort = 6}                                                   | ThumbnailData        | VT \_ BLOB                                      |
| /app1                                                              | App1                 | VT \_ 未知-App1 查詢讀取器/寫入器        |
| /app1/ifd 或/app1/{ushort = 0}                                     | 0 IFD                | VT \_ 未知-IFD 查詢讀取器/寫入器         |
| /app1/ifd/exif 或/app1/ifd/{ushort = 34665}                         | EXIF IFD             | VT \_ 未知-EXIF 查詢讀取器/寫入器        |
| /app1/thumb 或/app1/{ushort = 1}                                   | 縮圖 IFD        | VT \_ 未知-SubIFD 查詢讀取器/寫入器      |
| /app13                                                             | App13                | VT \_ 未知-App13 查詢讀取器/寫入器       |
| /app13/irb 或/app13/{ushort = 0}                                    | Irb                  | VT \_ 未知-IRB 查詢讀取器/寫入器         |
| /app13/irb/{ulonglong = \* } where \* = irb 識別碼 (請參閱 irb 規格)  | IRB 專案            | VT \_ 未知-未知的查詢讀取器/寫入器     |
| /app13/irb/{ulonglong = \* }/{}                                       | IRB 專案內容   | VT \_ BLOB                                      |
| /app13/irb/8bimiptc 或/app13/irb/{ulonglong = 61857348781060}       | 8BIMIPTC             | VT \_ 未知-8BIMIPTC 查詢讀取器/寫入器    |
| /app13/irb/8bimiptc/iptc                                           | IPTC                 | VT \_ 未知-IPTC 查詢讀取器/寫入器        |
| /app13/irb/8bimiptc/iptc/{str = \* }                                  | IPTC 專案           | 變數                                      |
| /app13/irb/8bimResInfo 或/app13/irb/{ulonglong = 61857348781037}    | 8BIM 解析資訊 | VT \_ 未知-查詢讀取器/寫入器             |
| /app13/irb/8bimResInfo/PString                                     |                      | VT \_ LPSTR                                     |
| /app13/irb/8bimResInfo/HResolution                                 |                      | VT \_ UI4                                       |
| /app13/irb/8bimResInfo/VResolution                                 |                      | VT \_ UI4                                       |
| /app13/irb/8bimResInfo/WidthUnit                                   |                      | VT \_ UI2                                       |
| /app13/irb/8bimResInfo/HeightUnit                                  |                      | VT \_ UI2                                       |
| /app13/irb/8bimResInfo/HResolutionUnit                             |                      | VT \_ UI2                                       |
| /app13/irb/8bimResInfo/VResolutionUnit                             |                      | VT \_ UI2                                       |
| /com                                                               | JPEG 批註         | VT \_ 未知-批註查詢讀取器/寫入器     |
| /com/TextEntry                                                     |                      | LPSTR                                         |
| /luminance                                                         | Luminance            | VT \_ 未知-亮度查詢讀取器/寫入器   |
| /luminance/TableEntry                                              |                      | VT \_ UI1 \| vt \_ 向量                         |
| /chrominance                                                       | Chrominance          | VT \_ 未知-色度查詢讀取器/寫入器 |
| /chrominance/TableEntry                                            |                      | VT \_ UI1 \| vt \_ 向量                         |
| /xmp                                                               | XMP                  | VT \_ 未知-XMP 查詢讀取器/寫入器         |



 

## <a name="file-format-independent-metadata"></a>檔案格式獨立中繼資料

下列各節包含多種影像格式所支援之元資料格式的相關資訊。 每個資料表都有下列資料行：

-   **相對路徑** -用來取得中繼資料專案的查詢路徑（相對於中繼資料區塊）。
-   **名稱** -中繼資料專案的名稱。
-   **Type** -從查詢路徑取出的中繼資料專案類型。 [WIC](-wic-api.md)取出的中繼資料會以 PROPVARIANT 的形式傳回，此格式會使用 VARTYPE 列舉來報告資料類型。

> [!Note]  
> 此處的表格只提供存取特定元資料格式內中繼資料專案的相對路徑。 若要取得完整的中繼資料查詢，請將此相對路徑附加至特定元資料格式的 metadata block 查詢。

 

例如，若要存取 JPEG 檔案中的 [方向](-wic-photoprop-system-photo-orientation.md) 旗標，請使用下列運算式：

-   /app1/ifd/{ushort = 274}

在 TIFF 檔案中，使用下列運算式：

-   /ifd/{ushort = 274}

在此範例中，請注意，不同的影像格式可能會以不同的方式儲存特定的中繼資料區塊，因此存取特定中繼資料專案的完整中繼資料查詢可能是特定的影像格式。 請參閱每個格式的表格，以找出適當的中繼資料查詢來存取特定的中繼資料區塊。

### <a name="ifd-metadata"></a>IFD 中繼資料

IFD （或影像檔案目錄）是以 TIFF 標準定義的資料結構，其中可以包含影像中繼資料。 它會使用 ushort 類型的標記來識別每個中繼資料專案。 JPEG、TIFF 和 JPEG-XR 支援 IFD 中繼資料。 協力廠商格式（像是相機原始格式）也可能支援 IFD 中繼資料。

此處的表格提供相關的中繼資料查詢路徑，以存取一些常用的 IFD 中繼資料專案。 IFD 資料結構允許協力廠商擴充性，而且此資料表不是詳盡的清單。 如需詳細資訊，請參閱 TIFF 標準。

> [!Note]  
> 雖然 JPEG 和其他格式支援 IFD 資料結構，但不能使用它所定義的所有中繼資料專案。 如需詳細資訊，請參閱每種格式的標準。

 

> [!Note]  
> 下表中的某些中繼資料專案需要額外的解讀或資訊才能正確使用，請參閱 TIFF 標準。 例如， [PhotometricInterpretation](-wic-photoprop-system-photo-photometricinterpretation.md) 中繼資料專案會傳回 VT UI2 類型的 PROPVARIANT \_ 。 不過，根據 TIFF 標準，它會被解釋為列舉。 如需詳細資訊，請參閱 TIFF 標準。

 



| 相對路徑   | 名稱                      | 類型                                           |
|-----------------|---------------------------|------------------------------------------------|
| /{ushort = 256}   | ImageWidth                | VT \_ UI2 或 vt \_ UI4                             |
| /{ushort = 257}   | ImageLength               | VT \_ UI2 或 vt \_ UI4                             |
| /{ushort = 258}   | BitsPerSample             | VT \_ UI2                                        |
| /{ushort = 259}   | 壓縮               | VT \_ UI2                                        |
| /{ushort = 262}   | PhotometricInterpretation | VT \_ UI2                                        |
| /{ushort = 274}   | Orientation               | VT \_ UI2                                        |
| /{ushort = 277}   | SamplesPerPixel           | VT \_ UI2                                        |
| /{ushort = 284}   | PlanarConfiguration       | VT \_ UI2                                        |
| /{ushort = 530}   | YCbCrSubSampling          | VT \_ 向量 \| vt \_ UI2                          |
| /{ushort = 531}   | YCbCrPositioning          | VT \_ UI2                                        |
| /{ushort = 282}   | XResolution               | VT \_ UI8                                        |
| /{ushort = 283}   | YResolution               | VT \_ UI8                                        |
| /{ushort = 296}   | ResolutionUnit            | VT \_ UI2                                        |
| /{ushort = 306}   | Datetime                  | VT \_ LPSTR                                      |
| /{ushort = 270}   | ImageDescription          | VT \_ LPSTR                                      |
| /{ushort = 271}   | 請確定                      | VT \_ LPSTR                                      |
| /{ushort = 272}   | 型號                     | VT \_ LPSTR                                      |
| /{ushort = 305}   | 軟體                  | VT \_ LPSTR                                      |
| /{ushort = 315}   | 演出者                    | VT \_ LPSTR                                      |
| /{ushort = 33432} | 著作權                 | VT \_ LPSTR                                      |
| /{ushort = 338}   | ExtraSamples              | VT \_ UI2                                        |
| /{ushort = 254}   | NewSubfileType            | VT \_ UI4                                        |
| /{ushort = 278}   | RowsPerStrip              | VT \_ UI2 或 vt \_ UI4                             |
| /{ushort = 279}   | StripByteCounts           | VT \_ 向量 \| vt \_ UI2 或 vt \_ 向量 \| vt \_ UI4 |
| /{ushort = 273}   | StripOffsets              | VT \_ 向量 \| vt \_ UI2 或 vt \_ 向量 \| vt \_ UI4 |



 

### <a name="exif-metadata"></a>EXIF 中繼資料

EXIF 中繼資料會定義為 EXIF JPEG 規格的一部分。 EXIF 中繼資料是以 TIFF 標準中所定義的 IFD 資料結構為基礎，並提供其他屬性，例如用來建立映射的裝置和攝影屬性的相關資訊。 它會使用 ushort 類型的標記來識別每個中繼資料專案。 JPEG、TIFF 和 JPEG-XR 支援 EXIF 中繼資料。 協力廠商格式（例如某些相機 raw 格式）也可能支援 EXIF 中繼資料。

下表提供用來存取一些常用的 EXIF 中繼資料專案的相對中繼資料查詢路徑。 EXIF 資料結構允許協力廠商擴充性，而此資料表不是詳盡的清單;如需詳細資訊，請參閱「EXIF 標準」。

> [!Note]  
> 許多 EXIF 中繼資料專案都是在 EXIF 標準中定義為 "有理" 或 "SRATIONAL" 類型。 「有理數」是由分子和分母組成，兩者都是32位不帶正負號的整數。 分子包含在高32位和低32位的分母中。 在 [WIC](-wic-api.md)中，這些會以 PROPVARIANT 分別以 vt \_ UI8 或 vt I8 的類型傳回 \_ ; 實際值會分別儲存為 ULARGE \_ 整數或大 \_ 整數。 若要存取分子和分母，請讀取 ULARGE \_ 整數或大整數值的 HighPart 和 LowPart 成員 \_ 。

 

> [!Note]  
> 下表中的某些中繼資料專案需要額外的解讀或資訊才能正確使用。 例如， [ColorSpace](-wic-photoprop-system-image-colorspace.md) 中繼資料專案會傳回 VT UI2 類型的 PROPVARIANT \_ 。 不過，根據 EXIF 標準，它會被解釋為列舉。 如需詳細資訊，請參閱 EXIF 標準。

 



| 相對路徑   | 名稱                      | 類型                  |
|-----------------|---------------------------|-----------------------|
| /{ushort = 36864} | ExifVersion               | VT \_ BLOB              |
| /{ushort = 40960} | FlashpixVersion           | VT \_ BLOB              |
| /{ushort = 40961} | ColorSpace                | VT \_ UI2               |
| /{ushort = 40962} | PixelXDimension           | VT \_ UI2 或 vt \_ UI4    |
| /{ushort = 40963} | PixelYDimension           | VT \_ UI2 或 vt \_ UI4    |
| /{ushort = 37500} | MakerNote                 | VT \_ BLOB              |
| /{ushort = 37510} | UserComment               | VT \_ LPWSTR            |
| /{ushort = 36867} | DateTimeOriginal          | VT \_ LPSTR             |
| /{ushort = 36868} | DateTimeDigitized         | VT \_ LPSTR             |
| /{ushort = 42016} | ImageUniqueID             | VT \_ LPSTR             |
| /{ushort = 42032} | CameraOwnerName           | VT \_ LPSTR             |
| /{ushort = 42033} | BodySerialNumber          | VT \_ LPSTR             |
| /{ushort = 42034} | LensSpecification         | VT \_ 向量 \| vt \_ UI8 |
| /{ushort = 42035} | LensMake                  | VT \_ LPSTR             |
| /{ushort = 42036} | LensModel                 | VT \_ LPSTR             |
| /{ushort = 42037} | LensSerialNumber          | VT \_ LPSTR             |
| /{ushort = 33434} | ExposureTime              | VT \_ UI8               |
| /{ushort = 33437} | FNumber                   | VT \_ UI8               |
| /{ushort = 34850} | ExposureProgram           | VT \_ UI2               |
| /{ushort = 34852} | SpectralSensitivity       | VT \_ LPSTR             |
| /{ushort = 34855} | PhotographicSensitivity   | VT \_ 向量 \| vt \_ UI2 |
| /{ushort = 34856} | OECF                      | VT \_ BLOB              |
| /{ushort = 34864} | SensitivityType           | VT \_ UI2               |
| /{ushort = 34865} | StandardOutputSensitivity | VT \_ UI4               |
| /{ushort = 34866} | RecommendedExposureIndex  | VT \_ UI4               |
| /{ushort = 34867} | ISOSpeed                  | VT \_ UI4               |
| /{ushort = 34868} | ISOSpeedLatitudeyyy       | VT \_ UI4               |
| /{ushort = 34869} | ISOSpeedLatitudezzz       | VT \_ UI4               |
| /{ushort = 37377} | ShutterSpeedValue         | VT \_ I8                |
| /{ushort = 37378} | ApertureValue             | VT \_ UI8               |
| /{ushort = 37379} | BrightnessValue           | VT \_ I8                |
| /{ushort = 37380} | ExposureBiasValue         | VT \_ I8                |
| /{ushort = 37381} | MaxApertureValue          | VT \_ UI8               |
| /{ushort = 37382} | SubjectDistance           | VT \_ UI8               |
| /{ushort = 37383} | MeteringMode              | VT \_ UI2               |
| /{ushort = 37384} | LightSource               | VT \_ UI2               |
| /{ushort = 37385} | 閃光燈                     | VT \_ UI2               |
| /{ushort = 37386} | FocalLength               | VT \_ UI8               |
| /{ushort = 37396} | SubjectArea               | VT \_ 向量 \| vt \_ UI2 |
| /{ushort = 41483} | FlashEnergy               | VT \_ UI8               |
| /{ushort = 41484} | SpatialFrequencyResponse  | VT \_ BLOB              |
| /{ushort = 41486} | FocalPlaneXResolution     | VT \_ UI8               |
| /{ushort = 41487} | FocalPlaneYResolution     | VT \_ UI8               |
| /{ushort = 41488} | FocalPlaneResolutionUnit  | VT \_ UI2               |
| /{ushort = 41492} | SubjectLocation           | VT \_ 向量 \| vt \_ UI2 |
| /{ushort = 41493} | ExposureIndex             | VT \_ UI8               |
| /{ushort = 41495} | SensingMethod             | VT \_ UI2               |
| /{ushort = 41728} | FileSource                | VT \_ BLOB              |
| /{ushort = 41729} | SceneType                 | VT \_ BLOB              |
| /{ushort = 41730} | CFAPattern                | VT \_ BLOB              |
| /{ushort = 41985} | CustomRendered            | VT \_ UI2               |
| /{ushort = 41986} | ExposureMode              | VT \_ UI2               |
| /{ushort = 41987} | 白平衡              | VT \_ UI2               |
| /{ushort = 41988} | DigitalZoomRatio          | VT \_ UI8               |
| /{ushort = 41989} | FocalLengthIn35mmFilm     | VT \_ UI2               |
| /{ushort = 41990} | SceneCaptureType          | VT \_ UI2               |
| /{ushort = 41991} | GainControl               | VT \_ UI8               |
| /{ushort = 41992} | 這個                  | VT \_ UI2               |
| /{ushort = 41993} | 飽和度                | VT \_ UI2               |
| /{ushort = 41994} | 清晰度                 | VT \_ UI2               |
| /{ushort = 41995} | DeviceSettingDescription  | VT \_ BLOB              |
| /{ushort = 41996} | SubjectDistanceRange      | VT \_ UI2               |



 

### <a name="gps-metadata"></a>GPS 中繼資料

GPS 中繼資料包含地理位置資訊，並定義為 EXIF JPEG 規格的一部分。 它會使用 ushort 類型的標記來識別每個中繼資料專案。 JPEG、TIFF 和 JPEG-XR 支援 GPS 中繼資料;協力廠商格式（像是相機原始格式）也可能支援 GPS 中繼資料。

下表提供相關的中繼資料查詢路徑，以存取一些常用的 GPS 中繼資料專案。 此資料表不是詳盡的清單;如需詳細資訊，請參閱「EXIF 標準」。

> [!Note]  
> 許多 GPS 中繼資料專案都是在 EXIF 標準中定義為 "有理" 類型。 「有理數」是由分子和分母組成，兩者都是32位不帶正負號的整數。 分子包含在高32位和低32位的分母中。 在 [WIC](-wic-api.md)中，這些會傳回為具有 VT UI8 類型的 PROPVARIANT \_ 。 實際的值會儲存為 ULARGE \_ 整數。 若要存取分子和分母，請讀取 ULARGE 整數值的 HighPart 和 LowPart 成員 \_ 。

 

> [!Note]  
> 表格中的特定中繼資料專案需要額外的解讀或資訊才能正確使用。 例如，GPSLatitudeRef 中繼資料專案會傳回 VT LPSTR 類型的 PROPVARIANT \_ 。 根據 EXIF 標準，此字串可以是 "N" 或 "S"，代表北或南部緯度。 如需詳細資訊，請參閱 EXIF 標準。

 



| 相對路徑 | 名稱            | 類型                                          |
|---------------|-----------------|-----------------------------------------------|
| {ushort = 0}    | GPSVersionID    | VT \_ 向量 \| vt \_ UI1                         |
| {ushort = 1}    | GPSLatitudeRef  | VT \_ LPSTR                                     |
| {ushort = 2}    | GPSLatitude     | VT \_ 向量 \| vt \_ UI8                         |
| {ushort = 3}    | GPSLongitudeRef | VT \_ LPSTR                                     |
| {ushort = 4}    | GPSLongitude    | {ushort = 4}GPSLongitude VT \_ VECTOR \| VT \_ UI8 |
| {ushort = 5}    | GPSAltitudeRef  | VT \_ UI1                                       |
| {ushort = 6}    | GPSAltitude     | VT \_ UI8                                       |
| {ushort = 7}    | GPSTimeStamp    | VT \_ 向量 \| vt \_ UI8                         |
| {ushort = 8}    | GPSSatellites   | VT \_ LPSTR                                     |
| {ushort = 9}    | GPSStatus       | VT \_ LPSTR                                     |
| {ushort = 10}   | GPSMeasureMode  | VT \_ LPSTR                                     |
| {ushort = 11}   | GPSDOP          | VT \_ UI8                                       |
| {ushort = 12}   | GPSSpeedRef     | VT \_ LPSTR                                     |
| {ushort = 13}   | GPSSpeed        | VT \_ UI8                                       |
| {ushort = 14}   | GPSTrackRef     | VT \_ LPSTR                                     |
| {ushort = 15}   | GPSTrack        | VT \_ UI8                                       |



 

### <a name="xmp-metadata"></a>XMP 中繼資料

XMP 是以 XML 為基礎且可擴充的中繼資料標準。 中繼資料專案可以是階層式，而且包含複雜的資料結構。 JPEG、TIFF 和 JPEG-XR 支援 XMP 中繼資料。 協力廠商格式（像是相機原始格式）也可能支援 XMP 中繼資料。

您可以從下列來源取得 XMP 標準： <https://www.adobe.com/devnet/xmp.html> 。

XMP 和可讓協力廠商實體發行自己的架構或命名空間，讓他們可以定義新的中繼資料專案，而不需要修改 XMP 標準。 XMP 架構是由 URL 唯一識別，但是 [WIC](-wic-api.md) 提供已知架構的一組易記識別碼。

XMP 中繼資料專案會以字串名稱和架構識別碼來識別。 最佳做法是，每個 XMP 中繼資料查詢都應同時指定架構和名稱。 如果缺少架構識別碼，則 JPEG 會嘗試比對所有存在於 XMP 中繼資料封包內的命名空間的中繼資料名稱。

例如，若要取得 JPEG 影像中的 XMP 架構所定義的評等屬性，請使用下列查詢：

-   /xmp/{wstr =https://ns.adobe.com/xap/1.0/}:Rating

第一個部分 "/xmp" 會捕獲影像的 XMP 中繼資料讀取器/寫入器。 " https://ns.adobe.com/xap/1.0/ " 是 xmp 架構的 URL，如 xmp 標準中所定義。 URL 會以日期運算式括住，以允許使用正斜線 (/) 等字元。 最後，「評等」是由 XMP 架構定義的實際中繼資料專案名稱，並以冒號 (： ) 來與架構識別碼分隔。

在此範例中，WIC 提供適用于 XMP 架構的易記識別碼，可用來取代完整的 URL。 因此，您可以將前一個查詢重寫為：

-   /xmp/xmp：評等

[WIC](-wic-api.md) 針對下列常用的架構提供易記的架構前置詞：



| 架構前置詞  | 架構 URL                                        | 標準連結                                         |
|----------------|---------------------------------------------------|----------------------------------------------------------|
| Rdf            | https://www.w3.org/1999/02/22-rdf-syntax-ns\#      | <https://www.w3.org/TR/REC-rdf-syntax/>                   |
| dc             | https://purl.org/dc/elements/1.1/                  | <https://www.adobe.com/devnet/xmp.html>                   |
| xmp            | https://ns.adobe.com/xap/1.0/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpidq         | https://ns.adobe.com/xmp/Identifier/qual/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpRights      | https://ns.adobe.com/xap/1.0/rights/               | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpMM          | https://ns.adobe.com/xap/1.0/mm/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpBJ          | https://ns.adobe.com/xap/1.0/bj/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpTPg         | https://ns.adobe.com/xap/1.0/t/pg/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| pdf            | https://ns.adobe.com/pdf/1.3/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| Photoshop      | https://ns.adobe.com/photoshop/1.0/                | <https://www.adobe.com/devnet/xmp.html>                   |
| tiff           | https://ns.adobe.com/tiff/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| Exif           | https://ns.adobe.com/exif/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| stDim          | https://ns.adobe.com/xap/1.0/sType/Dimensions\#    | <https://www.adobe.com/devnet/xmp.html>                   |
| xapGImg        | https://ns.adobe.com/xap/1.0/g/img/                | <https://www.adobe.com/devnet/xmp.html>                   |
| stEvt          | https://ns.adobe.com/xap/1.0/sType/ResourceEvent\# | <https://www.adobe.com/devnet/xmp.html>                   |
| stRef          | https://ns.adobe.com/xap/1.0/sType/ResourceRef\#   | <https://www.adobe.com/devnet/xmp.html>                   |
| stVer          | https://ns.adobe.com/xap/1.0/sType/Version\#       | <https://www.adobe.com/devnet/xmp.html>                   |
| stJob          | https://ns.adobe.com/xap/1.0/sType/Job\#           | <https://www.adobe.com/devnet/xmp.html>                   |
| 輔助            | https://ns.adobe.com/exif/1.0/aux/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| Crs            | https://ns.adobe.com/camera-raw-settings/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpDM          | https://ns.adobe.com/xmp/1.0/DynamicMedia/         | <https://www.adobe.com/devnet/xmp.html>                   |
| Iptc4xmpCore   | https://iptc.org/std/Iptc4xmpCore/1.0/xmlns/       | <https://www.iptc.org/cms/site/index.html?channel=CH0099> |
| MicrosoftPhoto | https://ns.microsoft.com/photo/1.0/                | [人員標記總覽](-wic-people-tagging.md)       |
| MP             | https://ns.microsoft.com/photo/1.2/                | [人員標記總覽](-wic-people-tagging.md)       |
| MPRI           | https://ns.microsoft.com/photo/1.2/t/RegionInfo\#  | [人員標記總覽](-wic-people-tagging.md)       |
| MPReg          | https://ns.microsoft.com/photo/1.2/t/Region\#      | [人員標記總覽](-wic-people-tagging.md)       |



 

如果特定架構沒有易記的架構前置詞（例如，如果影像包含使用自訂協力廠商架構的 XMP 中繼資料），則中繼資料查詢應該使用完整的架構 URL。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC 中繼資料總覽](-wic-about-metadata.md)
</dt> <dt>

[中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[中繼資料擴充性總覽](-wic-codec-metadatahandlers.md)
</dt> <dt>

[How to：使用中繼資料重新編碼 JPEG 影像](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
