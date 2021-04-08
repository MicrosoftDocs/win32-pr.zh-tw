---
title: 寫入影像資料流程
description: 寫入影像資料流程
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Advanced Systems Format (ASF) 、撰寫映射串流
- ASF (Advanced Systems Format) 、撰寫影像串流
- 先進的系統格式 (ASF) 、影像串流
- ASF (Advanced 系統格式) 、影像串流
- 影像串流，寫入
- 資料流程，寫入影像資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932934"
---
# <a name="writing-image-streams"></a>寫入影像資料流程

影像資料流程的輸入必須是 RGB 格式的點陣圖影像。 寫入器會使用 JPEG 格式來協調輸入影像樣本的壓縮。 在您開始撰寫包含影像資料流程的檔案之前，您必須使用 g wszJPEGCompressionQuality 設定來設定輸入的影像品質 \_ 。 使用 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) 將品質設定為 **DWORD** 值範圍從1到100。 低值代表高壓縮率，以品質為代價，而高數值則會產生需要更多空間的高品質影像。

影像串流通常需要比一般影片串流更大的緩衝區視窗。 所需的確切大小取決於影像的類型和影像品質，還有其他因素。 使用試用版和錯誤來判斷您想要處理之影像的適當大小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**影像串流**](image-streams.md)
</dt> <dt>

[**若要設定輸入設定**](to-set-input-settings.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




