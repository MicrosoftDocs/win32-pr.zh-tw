---
description: 提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DDS 編解碼器的相關資訊。
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: DDS 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a9fd00f17d17b7bb227a04e56bbc9369de86eb03f9c953a73267400d4a6df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204475"
---
# <a name="dds-format-overview"></a>DDS 格式總覽

本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DDS 編解碼器的相關資訊。

## <a name="codec-identity"></a>編解碼器身分識別

下表提供編解碼器識別資訊。



| 元件              | 描述        |
|------------------------|--------------------|
|  (s 的正式名稱)          | DirectDraw 介面 |
| 副檔名 (s)  | Dds                |
| MIME 類型 (MIME type)              | image/vnd-ms   |



 

下表列出用來識別原生 DDS 編解碼器元件的 Guid。



| 元件        | 易記名稱            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| 容器格式 | GUID \_ ContainerFormatDds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| 解碼器          | CLSID \_ WICDdsDecoder     | 9053699f-a341-429d-9e90ee437cf80c73 |
| 編碼器          | CLSID \_ WICDdsEncoder     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>像素格式支援

請注意，DDS 格式支援任何有效的 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值。 不過，WIC DDS 編解碼器只支援解碼和編碼包含下列格式的檔案：

-   DXGI \_ 格式 \_ BC1 \_ UNORM
-   DXGI \_ 格式 \_ BC2 \_ UNORM
-   DXGI \_ 格式 \_ BC3 \_ UNORM

## <a name="encoding"></a>編碼

WIC 編碼 Api 設計成與編解碼器無關，因此支援 WIC 的編解碼器影像編碼本質上是相同的。 如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

DDS 檔案格式有獨特的需求，從其對 mipmap 和材質陣列等概念的支援而產生。 若要完全控制 DDS 影像編碼的控制權，您應該使用 [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) 介面設定 dds 特定的編碼參數。

## <a name="decoding"></a>解碼

WIC 解碼 Api 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。 如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。 如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

## <a name="block-compressed-data-access"></a>封鎖壓縮的資料存取

除了支援標準 WIC 編解碼器介面之外，DDS 解碼器還可讓您使用特定的 DDS 介面（ [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) 和 [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode)），直接存取原生區塊壓縮的資料。 若要使用這些介面，請分別呼叫 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 和 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)的 QueryInterface。

 

 
