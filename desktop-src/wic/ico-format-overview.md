---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 .ICO 編解碼器的相關資訊。
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: .ICO 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988411"
---
# <a name="ico-format-overview"></a>.ICO 格式總覽

本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 .ICO 編解碼器的相關資訊。

## <a name="codec-identity"></a>編解碼器身分識別

下表提供編解碼器識別資訊。



|                        |                   |
|------------------------|-------------------|
|  (s 的正式名稱)          |  (.ICO) 的圖示格式 |
| 副檔名 (s)  | .ico               |
| MIME 類型 (MIME type)              | 影像/.ico         |
| 規格支援  |                   |



 

下表列出用來識別原生 .ICO 編解碼器元件的 Guid。



| 元件        | 易記名稱            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| 容器格式 | GUID \_ ContainerFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| 解碼器          | CLSID \_ WICIcoDecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| 編碼器          | 無法使用            | 無法使用                       |



 

## <a name="encoding"></a>編碼

WIC 不提供原生的 .ICO 影像編碼器。

## <a name="decoding"></a>解碼

WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。 如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。 如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

 

 



