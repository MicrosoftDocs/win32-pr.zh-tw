---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DNG 編解碼器的相關資訊。
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: DNG 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319303"
---
# <a name="dng-format-overview"></a>DNG 格式總覽

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DNG 編解碼器的相關資訊。

-   [編解碼器身分識別](#codec-identity)
-   [解碼](#decoding)

## <a name="codec-identity"></a>編解碼器身分識別

下表提供編解碼器識別資訊。



|                        |                                                      |
|------------------------|------------------------------------------------------|
|  (s 的正式名稱)          | 數位負面 (DNG)                                |
| 副檔名 (s)  | .dng                                                 |
| MIME 類型 (s)            | image/DNG                                            |
| 規格支援  | 數位負面 (DNG) 規格版本1.4.0。0 |



 

下表列出用來識別原生 DNG 編解碼器元件的 Guid。



| 元件        | 易記名稱             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| 容器格式 | GUID \_ ContainerFormatAdng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| 解碼器          | CLSID \_ WICAdngDecoder     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>解碼

WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。 如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。 如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

此解碼器不支援解碼原始感應器資料，而且只支援在 NewSubFileType 等於1的 IFD 中內嵌非原始影像表示的檔案。

 

 



