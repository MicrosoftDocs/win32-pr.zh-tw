---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 BMP 編解碼器的相關資訊。
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: BMP 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444959"
---
# <a name="bmp-format-overview"></a>BMP 格式總覽

本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 BMP 編解碼器的相關資訊。

## <a name="codec-identity"></a>編解碼器身分識別

下表提供編解碼器識別資訊。



| 元件              | 描述           |
|------------------------|-----------------------|
|  (s 的正式名稱)          | Windows 點陣圖格式 |
| 副檔名 (s)  | bmp、dib              |
| MIME 類型 (MIME type)              | image/bmp             |
| 規格支援  | BMP 規格 v5  |



 

下表列出用來識別原生 BMP 編解碼器元件的 Guid。



| 元件        | 易記名稱            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| 容器格式 | GUID \_ ContainerFormatBmp | 0af1d87e-fcfe-4188-bdeba7906471cbe3 |
| 解碼器          | CLSID \_ WICBmpDecoder     | 6b462062-7cbf-400d-9fdb813dd10f2778 |
| 編碼器          | CLSID \_ WICBmpEncoder     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>編碼

WIC 編碼 API 設計成與編解碼器無關，因此支援 WIC 的編解碼器影像編碼本質上是相同的。 如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

### <a name="encoder-options"></a>編碼器選項

已啟用 WIC 的編解碼器在編碼選項層級不同。 編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。 編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。 為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。 如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

下表列出原生 BMP 編解碼器所支援的 WIC 編碼器選項。



| 屬性名稱               | VARTYPE      | 值範圍                      | 預設值      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **VT \_ BOOL** | **VARIANT \_ TRUE/VARIANT \_ FALSE** | **VARIANT \_ FALSE** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

指定是否允許以 GUID \_ WICPixelFormat32bppBGRA 像素格式來編碼資料。 如果這個選項設定為 **VARIANT \_ TRUE**，就會以 BITMAPV5HEADER 標頭寫出 BMP。

預設值為 **VARIANT \_ FALSE**。

如果編碼器選項存在於編解碼器不支援的 IPropertyBag2 選項清單中，則會予以忽略。

請注意，對於16位和32位的 Windows BMP 檔案，BMP 編解碼器會忽略任何 Alpha 色板，因為許多舊版影像檔案在此額外通道中包含不正確資料。 從 Windows 8 開始，使用 **BITMAPV5HEADER** 與有效 Alpha 通道內容撰寫的32位 Windows BMP 檔案會以 WICPixelFormat32bppBGRA 的形式讀取

## <a name="decoding"></a>解碼

WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。 如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。 如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

 

 
