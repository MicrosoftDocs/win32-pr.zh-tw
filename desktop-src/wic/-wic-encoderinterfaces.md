---
description: 編碼器介面
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: 編碼器介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193562"
---
# <a name="encoder-interfaces"></a>編碼器介面


下表顯示 Windows 影像處理元件 (WIC) 編碼器所執行的介面，而類別圖表會顯示繼承階層。

Container-Level 編碼器介面



| 介面                                                                                       | 職責                             | 實作                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)                                             | 容器層級服務                     | 必要                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | & 取消支援的進度通知 | 建議                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | 中繼資料序列化服務              | 選擇性 (只有支援容器層級中繼資料的格式才需要)  |



 

Frame-Level 編碼器介面



| 介面                                                       | 職責                | 實作 |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | 框架層級服務            | 必要       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | 中繼資料序列化服務 | 必要       |



 

![wic 編碼器介面繼承階層](graphics/wicencoderinterfaces.png)

您會發現編碼器介面幾乎是解碼介面的鏡像影像，而且這些介面上的大部分方法都對應至相關的解碼器介面上的方法。 既然您已熟悉啟用 WIC 的解碼器，您現在也會熟悉啟用 WIC 的編碼器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[執行 WIC-Enabled 編碼器](-wic-implementingwicencoder.md)
</dt> <dt>

[執行 IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



