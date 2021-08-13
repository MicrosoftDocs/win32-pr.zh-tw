---
description: 解碼器介面
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: 解碼器介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a52a0924f6302e45b10cb32a1d621db04967d33a3251ee39cce359e5030af5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393520"
---
# <a name="decoder-interfaces"></a>解碼器介面

下表顯示 Windows 影像處理元件 (WIC) 的解碼器所實的介面，而類別圖表則顯示繼承階層。

Container-Level 的解碼器介面



| 介面                                                                                       | 職責                             | 實作                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | 容器層級服務                     | 必要                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | & 取消支援的進度通知 | 建議                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | 中繼資料列舉                         | 選擇性 (只有支援容器層級中繼資料的格式才需要)  |



 

Frame-Level 的解碼器介面



| 介面                                                           | 職責          | 實作                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | 框架層級服務      | 必要                      |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)     | 中繼資料列舉      | 必要                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | 原生解碼器轉換 | 建議                   |
| [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)                       | 原始處理服務   | 只有 Raw 格式的必要 |



 

![wic 介面繼承階層](graphics/wicinterfaces.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[執行 WIC-Enabled 的解碼器](-wic-implementingwicdecoder.md)
</dt> <dt>

[執行 IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



