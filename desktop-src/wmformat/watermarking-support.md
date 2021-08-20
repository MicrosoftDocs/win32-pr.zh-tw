---
title: 浮水印支援
description: 浮水印支援
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows媒體格式 SDK，浮水印支援
- Windows媒體格式 SDK，數位浮水印
- Advanced Systems Format (ASF) 、浮水印支援
- ASF (Advanced Systems Format) 、浮水印支援
- Advanced Systems Format (ASF) 、數位浮水印
- ASF (Advanced Systems Format) 、數位浮水印
- Windows媒體格式 SDK，DMO
- Advanced Systems Format (ASF) ，DMO
- ASF (Advanced Systems Format) ，DMO
- Windows媒體格式 SDK，IWMWatermarkInfo 介面
- Advanced Systems Format (ASF) ，IWMWatermarkInfo 介面
- ASF (Advanced Systems Format) ，IWMWatermarkInfo 介面
- 浮水印，關於
- 數位浮水印
- DirectX 媒體物件 (DMO) ，關於
- DMO (DirectX 媒體物件) ，關於
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78610c95d041390f819c24a11ccbf393bd62d19037e655e2d1c53b458e0a664b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653431"
---
# <a name="watermarking-support"></a>浮水印支援

數位浮水印是在媒體資料流程的資料中內嵌著作權或其他資訊的一種方式。 浮水印的技巧在不同的解決方案之間有很大的差異。 浮水印最簡單的形式就是將識別影像新增至影片串流的每個畫面格。 電視電臺通常會使用這項技術，在其廣播的右下角插入半透明的標誌。 更複雜的數位浮水印形式 imperceptible 給使用者觀賞或聆聽內容。

Windows 媒體格式 SDK 支援使用數位浮水印 [*DMOs*](wmformat-glossary.md)。 在實務上，浮水印系統非常類似于編解碼器：它會取得媒體範例、對資料執行演算法，以及輸出已改變的範例。 當針對資料流程指定浮水印系統時，寫入器物件會在其處理輸入樣本時包含 DMO。

當您設定浮水印的串流時，必須指定浮水印設定資訊。 設定值會隨著浮水印 DMO 而有所不同。 您所使用的 DMO 應提供描述其所支援之設定值的指示。

如需用來指定浮水印系統之設定的相關資訊，請參閱 [ **IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)

您可以對應用程式進行程式設計，以列舉用戶端電腦上所安裝的浮水印 DMOs。 如需詳細資訊，請參閱 [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) 介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檔案寫入功能**](file-writing-features.md)
</dt> </dl>

 

 




