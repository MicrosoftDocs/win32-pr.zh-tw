---
description: Windows (WIC) 的影像處理元件已更新為新版本的 Windows。 本主題提供這些新功能的快速簡介。
ms.assetid: 710B71CE-6FCC-46DA-A65C-6E4FC6A04275
title: WIC 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420d501dd495081764a7fba89f73d21077c04b05d92e7c2b47c3c2c2d51d7d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204013"
---
# <a name="whats-new-in-wic"></a>WIC 的新功能

Windows (WIC) 的影像處理元件已更新為新版本的 Windows。 本主題提供這些新功能的快速簡介。

## <a name="whats-new-for-windows-10-version-1507"></a>Windows 10 的新功能，版本1507

### <a name="access-to-low-level-jpeg-data-for-wic-decoding-and-encoding"></a>存取適用于 WIC 解碼和編碼的低層級 JPEG 資料

從 Windows 10 開始，WIC 1507 版可讓您存取低層級 JPEG 資料結構，包括 Huffman 和量化資料表。 如需詳細資訊，請參閱下列主題：

-   [**IWICJpegFrameDecode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframedecode) 介面
-   [**IWICJpegFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframeencode) 介面

### <a name="jpeg-indexing"></a>JPEG 索引

JPEG 索引是一種技術，可大幅提升隨機存取大型 JPEG 影像之小型子領域的效能，代價是有一些額外的記憶體使用量。 任何 WIC 的呼叫者都可以利用 JPEG 索引。

[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)介面的設計目的是要在開啟時，利用 JPEG 索引。 例如，ID2D1ImageSource API 只會在案例中要求影像的需要區段，例如大型解析度影像的平移和縮放。 如需詳細資訊，請參閱下列主題：

-   [**IWICJpegFrameDecode：： SetIndexing**](/windows/win32/api/Wincodec/nf-wincodec-iwicjpegframedecode-setindexing) 方法
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) 介面

## <a name="whats-new-for-windows-81"></a>Windows 8.1 的新功能

### <a name="support-for-jpeg-ycbcr-images"></a>支援 JPEG YCbCr 影像

從 Windows 8.1 開始，WIC 提供以原生格式解碼、轉換及編碼 JPEG Y'CbCr 影像資料的支援。 這可讓應用程式在使用 Y'CbCr 編碼的 Jpeg 時，大幅減少某些影像作業的處理時間和記憶體耗用量。 如需詳細資訊，請參閱下列主題：

-   [Direct2D](-wic-sample-d2d-viewer.md)[YCbCr 效果](../direct2d/ycbcr-effect.md)
-   [**IWICPlanarBitmapSourceTransform**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) 介面
-   [**IWICPlanarBitmapFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) 介面

### <a name="support-for-block-compressed-formats-dds-files"></a>支援 (DDS 檔案的區塊壓縮格式) 

從 Windows 8.1 開始，WIC 會加入新的編解碼器，以支援以下列格式編碼的 DDS 影像： DXGI \_ format \_ BC1 \_ UNORM、dxgi \_ format \_ BC2 \_ UNORM 和 DXGI \_ format \_ BC3 \_ UNORM。 您可以使用標準 WIC 介面，以已解碼的格式存取 DDS 區塊壓縮的資料，或直接使用新的 DDS 特定介面進行存取。 如需詳細資訊，請參閱下列主題：

-   [**IWICDdsDecoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsdecoder) 介面
-   [**IWICDdsEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsencoder) 介面

## <a name="whats-new-for-windows-8"></a>Windows 8 的新功能

在 Windows 8 中，WIC 已更新數個新功能。 您也可以透過適用于[Windows 7](../direct3darticles/platform-update-for-windows-7.md)的平臺更新，在 Windows 7 和 Windows Server 2008 R2 上取得 WIC 的更新版本，此版本可透過[Windows 7 的平臺更新](https://support.microsoft.com/kb/2670838)取得。

### <a name="improved-direct2d-integration"></a>改良的 Direct2D 整合

Windows 8 中的 wic 可提供這些 api 來改善 Direct2D 與 WIC 的整合：

-   [**IWICImageEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicimageencoder) -可將 Direct2D [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) 內容編碼為 [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)的新介面。 這個介面的方法會採用 [**WICImageParameters**](/windows/win32/api/Wincodec/ns-wincodec-wicimageparameters)的指標，也就是控制編碼的參數。
-   [**IWICImagingFactory2**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory2) -使用 [**CreateImageEncoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) 方法的新 WIC factory。 此介面繼承自原始的 WIC factory [**IWICImagingFactory**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory)，並以相同的方式建立。

### <a name="changes-to-bmp-codec-alpha-support"></a>BMP 編解碼器 Alpha 支援的變更

Windows 8 中的 WIC 支援以 [WICPixelFormat32bppBGRA](-wic-codec-native-pixel-formats.md)格式的影像形式載入 [**BITMAPV5HEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header)影像檔案。 此外，BMP 編碼器支援新的布林值 "EnableV5Header32bppBGRA"，它會指示編碼器使用32bppBGRA 影像資料來寫入 **BITMAPV5HEADER** 。

如需 BMP 格式的詳細資訊，請參閱 [Bmp 格式總覽](bmp-format-overview.md)。

### <a name="new-pixel-formats"></a>新的像素格式

Windows 8 中的 WIC 定義了下列新的像素格式：

-   GUID \_ WICPixelFormat32bppRGB
-   GUID \_ WICPixelFormat64bppRGB
-   GUID \_ WICPixelFormat96bppRGBFloat
-   GUID \_ WICPixelFormat64bppPRGBAHalf

> [!Note]  
> TIFF 內建編解碼器會傳回 GUID \_ WICPixelFormat96bppRGBFloat 資料。 內建的編解碼器未使用其他三種格式。

 

### <a name="restrictions-to-component-extensibility-in-appcontainer"></a>AppContainer 中元件擴充性的限制

在包含所有 Windows 存放區應用程式的 AppContainer 進程中執行時，WIC 將只會使用 Windows 提供的元件，而不論系統上是否已安裝額外的元件。 未在 AppContainer 中執行的應用程式不會受到影響。

應用程式不需要在 AppContainger 中執行任何程式碼變更，但 [**WICComponentEnumerateOptions**](/windows/win32/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions) 旗標和廠商 GUID 參數將不會有任何作用。 如果無法由 Windows 提供的編解碼器解碼，則 WIC 將無法載入映射，而且呼叫 [**CreateComponentEnumerator**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentenumerator)方法只會傳回 Windows 提供的元件。

### <a name="changes-to-clsid_wicpngdecoder-and-png-decoder-color-context-support"></a>CLSID \_ WICPngDecoder 和 PNG 解碼器色彩內容支援的變更

**CLSID \_** 已新增 WICPngDecoder1 與 **clsid \_ WICPNGDECODER** 相同的 GUID，並新增了 **clsid \_ WICPngDecoder2** 。

針對 Windows 8 SDK 編譯時， **clsid \_ WICPngDecoder** 會 \# 定義為 **clsid \_ WICPngDecoder2** ，以使用新的 PNG 解碼器行為來升級新編譯的應用程式。 應用程式應繼續指定 **CLSID \_ WICPngDecoder**。

指定 **CLSID \_ WICPngDecoder2** 將會建立 WIC PNG 解碼器的版本，此版本將會從 cHRM 和 GAMA 區塊產生 [**IWICColorCoNtext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) 。 這可讓此色彩空間中繼資料與其他 Windows api 搭配使用，以用於管理來源影像的色彩。 如果有 iCCP 區塊，則不會從 gAMA 和 cHRM 區塊產生 **IWICColorCoNtext** ，如果出現 srgb 區塊，或 GAMA 和 cHRM 區塊指出 sRGB 色彩空間，則不會產生。

應用程式可以指定 **CLSID \_ WICPngDecoder1** 來建立不會從 gAMA 和 CHRM 區塊產生 [**IWICColorCoNtext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) 的 WIC PNG 解碼版本。 這與舊版 Windows 中的 PNG 解碼器行為相符。

### <a name="changes-to-wincodec_sdk_version"></a>WINCODEC \_ SDK 版本的 \_ 變更

針對 Windows 8 sdk 進行編譯時，會將 **WINCODEC \_ sdk \_ 版本** \# 定義為 **WINCODEC \_ sdk \_ VERSION2** ，以使用新的 PNG 解碼器行為來升級新編譯的應用程式。 否則，它會 \# 定義為 **WINCODEC \_ SDK \_ VERSION1**。 應用程式應繼續指定 **WINCODEC \_ SDK \_ 版本**。

在呼叫 [**WICCreateImagingFactory \_ Proxy**](-wic-codec-wiccreateimagingfactory-proxy.md)以建立映射處理站時指定 **WINCODEC \_ SDK \_ 版本**，會導致建立 **CLSID \_ WICPngDecoder2** ，而不是從 [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)方法及其變異的 **clsid \_ WICPngDecoder1** 建立。 此外，解碼器元件資訊列舉值會傳回 **clsid \_ WICPngDecoder2** 元件資訊，但不會傳回 **clsid \_ WICPngDecoder1** 資訊。

在上述案例中，指定 **WINCODEC \_ SDK \_ VERSION1** 將會導致使用 **clsid \_ WICPngDecoder1** ，而不是 **clsid \_ WICPngDecoder2** 。

### <a name="changes-to-clsid_wicimagingfactory"></a>CLSID WICImagingFactory 的變更 \_

**CLSID \_** 已新增 WICImagingFactory1 與 **clsid \_ WICIMAGINGFACTORY** 相同的 GUID，並新增了 **clsid \_ WICImagingFactory2** 。

針對 Windows 8 SDK 編譯時， **clsid \_ WICImagingFactory** 會 \# 定義為 **clsid \_ WICImagingFactory2** ，以使用新的 PNG 解碼器行為來升級新編譯的應用程式。 應用程式應繼續指定 **CLSID \_ WICImagingFactory**。

當呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立映射處理站時，指定 **clsid \_ WICImagingFactory2** 會導致建立 **CLSID \_ WICPngDecoder2** ，而不是 [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)方法及其變異的 **clsid \_ WICPngDecoder1** 。 此外，解碼器元件資訊列舉值會傳回 **clsid \_ WICPngDecoder2** 元件資訊，但不會傳回 **clsid \_ WICPngDecoder1** 資訊。

在上述案例中，指定 **clsid \_ WICImagingFactory1** 會導致使用 **clsid \_ WICPngDecoder1** ，而不是 **clsid \_ WICPngDecoder2** 。

## <a name="whats-new-for-windows-7"></a>Windows 7 的新功能

在 Windows 7 中，WIC 已更新數個新功能。 本主題提供這些新功能的快速簡介。

### <a name="updates-to-the-tiff-codec"></a>TIFF 編解碼器的更新

已更新 Windows 7 的 WIC TIFF 編解碼器，以支援先前版本的 WIC 不支援的數個功能。

-   支援大型 TIFF 檔案。
-   將已平平的 TIFF 影像解碼。
-   將平面 (平面) TIFF 影像。
-   解碼 JPEG 編碼的 TIFF 影像。

### <a name="progressive-decoding"></a>漸進式解碼

漸進式解碼能讓您在整個影像下載完成之前，以累加方式解碼和轉譯部分影像。 這項功能可大幅改善從網際網路流覽影像時的使用者體驗，因為使用者不需要等待整個影像下載，就可以開始進行解碼。 使用漸進式解碼時，使用者可以在下載整個影像之前，看到有可用資料的影像預覽。 這項功能對於任何用來從網際網路或受限頻寬的資料來源來查看影像的應用程式而言是不可或缺的。

如需詳細資訊，請參閱 [漸進式解碼總覽](-wic-progressive-decoding.md)。

### <a name="extended-metadata-support-for-jpeg-png-and-gif"></a>JPEG、PNG 和 GIF 的延伸中繼資料支援

在 Windows 7 中，WIC 已擴充其對 JPEG、PNG 和 GIF 影像的中繼資料支援。

-   新增動畫 GIF 和 GIF 屬性的支援。
-   擴充的 JPG 元資料處理程式，可支援色度、亮度和批註中繼資料。
-   擴充的 PNG 元資料處理程式，可支援時間、sRGB、iCCP、>hist、cHRM、iTXt、bKGD 和 gAMA 中繼資料。
-   新增 ResolutionInfo 中繼資料和 IPTC 摘要中繼資料的新8BIM 元資料處理程式。
-   已新增邏輯螢幕描述元的新元資料處理程式 (LSD) 、影像描述元 (IMD) 、圖形控制項延伸 (GCE) ，以及應用程式延伸模組 (n) 中繼資料。
-   支援跨越 APPn 區塊的中繼資料。

### <a name="multi-threaded-apartment-support"></a>多執行緒的單元支援

多執行緒單元內的物件 (MTA) 可由 MTA 內任意數目的執行緒同時呼叫，以提供多核心系統和特定伺服器案例的效能提升。 此外，位於 MTA 內的 WIC 編解碼器，可以呼叫位於 MTA 內的其他物件，而不需要在存留于不同 STA 單元的執行緒之間呼叫的封送處理成本。 在 Windows 7 中，所有內建的 WIC 編解碼器都已更新為支援 MTA，包括 JPEG、TIFF、PNG、GIF、.ico 和 BMP。 強烈建議您撰寫編解碼器以支援 MTA。 不支援 MTA 的編解碼器會在多執行緒應用程式中造成效能大幅降低，因為封送處理。 啟用 MTA 支援需要在編解碼器中執行適當的同步處理。 這些同步處理技術的確切執行已超出本檔的範圍。 以下提供同步處理元件物件模型 (COM) 物件的一般參考。

### <a name="metadata-working-group-implementations"></a>中繼資料工作群組實施

目前有各種不同的中繼資料儲存格式包含重迭的屬性，不含任何明確的產業標準或讀取和寫入這些元資料格式的一致方法指引。 為了協助使用這各種格式和屬性， (MWG) 的中繼資料工作群組形成。 MWG 的目的是要提供指導方針，以確保各種平臺、應用程式和裝置之間的互通性。 MWG 所建立的指導方針適用于 XMP、Exif 和 IPTC 元資料欄位，以及 JPEG、TIFF 和 PSD 影像格式。

在 Windows 7 中，相片元資料處理程式和中繼資料原則層已更新為根據 MWG 所建立的指導方針來讀取和寫入影像中繼資料。 如需有關中繼資料工作群組 (MWG) 的詳細資訊，請參閱已 [建立的中繼資料指導方針](https://s3.amazonaws.com/software.tagthatphoto.com/docs/mwg_guidance.pdf)。

### <a name="windows-7-features-supported-on-windows-vista-and-windows-server-2008"></a>Windows Vista 和 Windows Server 2008 支援 Windows 7 功能

[Windows Vista 的平臺更新](../win7ip/platform-update-for-windows-vista-portal.md)是一組執行時間程式庫，可讓開發人員將應用程式的目標設為 Windows 7 和 Windows Vista。 Windows Server 2008 的平臺更新是一組執行時間程式庫，可讓開發人員將應用程式的目標設為 Windows Server 2008 R2 和 Windows server 2008。 適用于 Windows Vista 的平臺更新和 Windows server 2008 的平臺更新，將透過 Windows Update 提供給所有 Windows Vista 和 Windows Server 2008 客戶。 需要適用于 Windows Server 2008 Windows Vista 或平臺更新的協力廠商應用程式，可以讓 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。 如需這兩項更新的詳細資訊，請參閱 Windows Vista 的平臺更新。

 

 
