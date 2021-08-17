---
description: 執行原始編解碼器的一般指導方針
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: 執行原始編解碼器的一般指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5081edfc6f49dc1d145fc3e2ce7e5f993fb2e7e250aeb0f1091579dd3f45461
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204626"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>執行原始編解碼器的一般指導方針

相較于 JPEG 或 TIFF 等非原始影像類型，原始影像格式預期在 Windows 中的行為有兩個顯著的差異：

-   大部分的原始影像格式會假設為「唯讀」，而且可能不支援將圖元編碼為原始格式。 不過，因為 Windows 影像處理元件 (WIC) 需要編碼器支援中繼資料回寫，所以原始編解碼器作者應計畫至少執行一個基本架構編碼器類別。
-   相較于其他格式，解碼完整大小的原始影像可能需要很長的時間。 基於這個理由，Microsoft 建議採取某些方法來將解碼延遲降至最低，並確保支援快速轉譯縮圖和預覽等案例。

    例如，所有原始編解碼器作者都必須執行 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 介面，這個介面會提供一種機制，在目標點陣圖大小之前通知編碼器，藉此啟用對較小輸出影像大小的優化解碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



