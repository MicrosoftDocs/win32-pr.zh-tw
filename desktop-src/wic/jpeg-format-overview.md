---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 JPEG 編解碼器的相關資訊。
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: JPEG 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992460"
---
# <a name="jpeg-format-overview"></a>JPEG 格式總覽

本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 JPEG 編解碼器的相關資訊。

## <a name="codec-identity"></a>編解碼器身分識別

下表提供編解碼器識別資訊。



|                        |                                         |
|------------------------|-----------------------------------------|
|  (s 的正式名稱)          | JPEG 格式 (JPEG) |
| 副檔名 (s)  | jpe、jpeg、jpg                          |
| MIME 類型 (MIME type)              | image/jpeg、image/jpe、image/jpg        |
| 規格支援  | JFIF 規格1.02                 |



 

下表列出用來識別原生 JPEG 編解碼器元件的 Guid。



| 元件        | 易記名稱             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| 容器格式 | GUID \_ ContainerFormatJpeg | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| 解碼器          | CLSID \_ WICJpegDecoder     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| 編碼器          | CLSID \_ WICJpegEncoder     | 1a34f5c1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>編碼

WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。 如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

### <a name="encoder-options"></a>編碼器選項

已啟用 WIC 的編解碼器在編碼選項層級不同。 編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。 編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。 為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。 如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

JPEG 編解碼器會使用基本的 WIC 選項。 下表列出原生 JPEG 編解碼器所支援的 WIC 編碼器選項。



| 屬性名稱                                        | VARTYPE           | 值範圍                                                                       | 預設值                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | VT \_ R4            | 0-1。0                                                                           | 0.9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | VT \_ UI1           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [明亮度](#luminance-option)                       | VT \_ UI4/vt \_ 陣列 | 64專案 (DCT)                                                                   | 預設的亮度表。                                                       |
| [Chrominance](#chrominance-option)                   | VT \_ UI4/vt \_ 陣列 | 64專案 (DCT)                                                                   | 預設的色度資料表。                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | VT \_ UI1           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | VT \_ BOOL          | **TRUE** /**FALSE**                                                                | **FALSE**                                                                      |



 

如果編碼器選項存在於編解碼器不支援的 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。

### <a name="imagequality-option"></a>ImageQuality 選項

指定所需的影像精確度。 0.0 表示可能的精確度最低，而1.0 指定最高的精確度。

預設值為0.9。

### <a name="bitmaptransform-option"></a>BitmapTransform 選項

指定影像解碼期間影像的轉換方式。 此選項必須設定為其中一個 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 列舉值。

預設值為 [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)。

### <a name="luminance-option"></a>亮度選項

指定用於編碼的灰階亮度層級表格。

### <a name="chrominance-option"></a>色度選項

指定要用於編碼的色度資料表。

### <a name="jpegycrcbsubsampling-option"></a>JpegYCrCbSubsampling 選項

指定用於 YCrCb 編碼的次取樣比例。

預設值為 [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption)。

### <a name="suppressapp0-option"></a>SuppressApp0 選項

指定在編碼影像資料時，是否要隱藏 App0 中繼資料的寫入。

預設值為 **FALSE**。

## <a name="decoding"></a>解碼

WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。 如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。 如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

原生 JPEG 編解碼器也支援在畫面格解碼上 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ，以新增解碼影像串流的進階選項。 如需這些 advanced 選項的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

 

 
