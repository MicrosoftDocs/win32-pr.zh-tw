---
title: 使用非正方形圖元讀取資料流程
description: 使用非正方形圖元讀取資料流程
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows媒體格式 SDK，讀取影片串流
- Windows媒體格式 SDK、影片串流
- Windows媒體格式 SDK、非正方形圖元
- 'Windows媒體格式 SDK，圖元 (非正方形) '
- Advanced Systems Format (ASF) ，讀取影片串流
- ASF (Advanced 系統格式) ，讀取影片串流
- Advanced Systems Format (ASF) 、影片串流
- ASF (Advanced 系統格式) 、影片串流
- Advanced Systems Format (ASF) 、非平方圖元
- ASF (Advanced Systems Format) 、非正方形圖元
- 'Advanced Systems Format (ASF) 、圖元 (非正方形) '
- 'ASF (Advanced Systems Format) ，圖元 (非正方形) '
- 讀取影片串流
- 影片串流，讀取
- 影片串流，非正方形圖元
- 非正方形圖元
- '圖元 (非正方形) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9173c7b5dca81f11a6e35afafe30efa33d86c604adcadb59a51b17ab8130422c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846025"
---
# <a name="reading-streams-with-non-square-pixels"></a>使用非正方形圖元讀取資料流程

需要正確處理非正方形圖元的讀取器應用程式，應該在每個範例的 ASF 標頭和資料單位延伸中檢查資料流程層級的屬性。 在兩種情況下，必須調整輸出矩形以補償非正方形圖元。

從裝置（例如 DV (數位視訊）捕獲來源內容時，若其 CCD 中有非正方形圖元的數位視訊) 攝影機，讀取器應用程式必須調整其影片輸出矩形，以便在具有正方形圖元的電腦監視器上正確顯示影像。

當您的讀者應用程式輸出將在 NTSC 電視上播放的影片時（例如透過視訊卡上的 S-video 輸出連線），您必須調整影片矩形，讓影像在電視的非正方形圖元上正確顯示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用非正方形圖元讀取和寫入影片串流**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




