---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 PNG 編解碼器的相關資訊。
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: PNG 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3d74282f8c14fd94b3661430402a808b04ceb9cf0a061a1648f7a912af5636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086751"
---
# <a name="png-format-overview"></a>PNG 格式總覽

本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 PNG 編解碼器的相關資訊。

## <a name="codec-identity"></a>編解碼器身分識別

下表提供編解碼器識別資訊。



|     元件          | 描述                     |
|------------------------|---------------------------------|
|  (s 的正式名稱)          | 可攜式網路圖形 (PNG) |
| 副檔名 (s)  | png                             |
| MIME 類型 (MIME type)              | image/png                       |
| 規格支援  | PNG 規格1。2           |



 

下表列出用來識別原生 PNG 編解碼器元件的 Guid。



| 元件        | 易記名稱            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| 容器格式 | GUID \_ ContainerFormatPng | 1b7cfaf4-713f-473c-bbcd6137425faeaf |
| 解碼器          | CLSID \_ WICPngDecoder     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| 編碼器          | CLSID \_ WICPngEncoder     | 27949969-876a-41d7-9447568f6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 和更新版本

從 Windows 8 WIC 開始提供額外的 PNG 解碼器

## <a name="encoding"></a>編碼

WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。 如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

### <a name="encoder-options"></a>編碼器選項

已啟用 WIC 的編解碼器在編碼選項層級不同。 編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。 編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。 為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。 如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

PNG 編解碼器使用基本的 WIC 編碼器選項。 下表列出原生 PNG 編解碼器所支援的 WIC 編碼器選項。



| 屬性名稱   | VARTYPE  | 值範圍                                                 | 預設值                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | VT \_ BOOL | **TRUE** /**FALSE**                                          | **FALSE**                                                        |
| FilterOption    | VT \_ UI1  | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

如果編碼器選項存在於編解碼器不支援的 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。

### <a name="interlaceoption"></a>InterlaceOption

指定是否將影像資料編碼為交錯式。

預設值為 **FALSE**。

### <a name="filteroption"></a>FilterOption

指定用於影像壓縮的篩選選項。

預設值為 [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)。

## <a name="decoding"></a>解碼

WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。 如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。 如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

原生 PNG 編解碼器也支援畫面上的 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ，以新增解碼影像資料流程的 advanced 選項。 如需這些 advanced 選項的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

 

 
