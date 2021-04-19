---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 TIFF 編解碼器的相關資訊。
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: TIFF 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997920"
---
# <a name="tiff-format-overview"></a>TIFF 格式總覽

本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 TIFF 編解碼器的相關資訊。

-   [編解碼器身分識別](#codec-identity)
-   [編碼方式](#encoding)
    -   [編碼器選項](#encoder-options)
-   [解碼](#decoding)

## <a name="codec-identity"></a>編解碼器身分識別

下表提供編解碼器識別資訊。



|                        |                                 |
|------------------------|---------------------------------|
|  (s 的正式名稱)          | 標記的影像檔案格式 (TIFF) |
| 副檔名 (s)  | tiff、.tif                       |
| MIME 類型 (s)            | 影像/tiff、影像/.tif           |
| 規格支援  | TIFF 規格6。0          |



 

下表列出用來識別原生 TIFF 編解碼器元件的 Guid。



| 元件        | 易記名稱             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| 容器格式 | GUID \_ ContainerFormatTiff | 163bcc30-e2e9-4f0b-961da3e9fdb788a3  |
| 解碼器          | CLSID \_ WICTiffDecoder     | b54e85d9-fe23-499f-8b886acea7137502b |
| 編碼器          | CLSID \_ WICTiffEncoder     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>編碼

WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。 如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

### <a name="encoder-options"></a>編碼器選項

已啟用 WIC 的編解碼器在編碼選項層級不同。 編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。 編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。 為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。 如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

TIFF 編解碼器會使用基本的 WIC 選項。 下表列出原生 TIFF 編解碼器所支援的 WIC 編碼器選項。

| 屬性名稱         | VARTYPE | 值範圍 | 預設值    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | VT \_ R4  | 0-1。0     | 0                |
| TiffCompressionMethod | VT \_ UI1 | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

如果編碼器選項存在於編解碼器不支援的 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。

### <a name="compressionquality-option"></a>CompressionQuality 選項

指定所需的壓縮品質。 0.0 表示可用的最有效率壓縮配置。 一般而言，此配置會產生更快速的編碼，但較大的輸出。 值為1.0 時，可指定最有效率的壓縮配置。 一般而言，此配置會導致較長的編碼，但會產生較小的輸出。

預設值為 0。

### <a name="tiffcompressionmethod-option"></a>TiffCompressionMethod 選項

指定 TIFF 壓縮方法。

預設值為 [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)。

## <a name="decoding"></a>解碼

WIC 解碼 Api 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。 如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。 如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

 

 
