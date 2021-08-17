---
title: 執行 Video DSP 外掛程式
description: 執行 Video DSP 外掛程式
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Windows Media Player 外掛程式、影片 DSP
- 外掛程式、視頻 DSP
- 數位信號處理外掛程式，執行程式碼
- DSP 外掛程式，執行程式碼
- 數位信號處理外掛程式，修改範例程式碼
- DSP 外掛程式，修改範例程式碼
- 數位信號處理外掛程式、影片執行
- DSP 外掛程式、影片執行
- 影片 DSP 外掛程式，執行程式碼
- 影片 DSP 外掛程式，修改範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4afdbabd36167c11ef7c1c57aeccb475605f9365c550c572422af3440d760ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135701"
---
# <a name="implementing-a-video-dsp-plug-in"></a>執行 Video DSP 外掛程式

電腦影片顯示介面卡支援一組影片格式。 數位視訊編碼器也支援一組影片格式。 嘗試播放特定的影片檔案時，Windows Media Player 必須選擇要用於轉譯的格式。 播放程式會嘗試在影片編解碼器支援的格式與視頻顯示器介面卡支援的格式（也就是產生最高品質的格式）之間尋找最相符的結果。

若要建立可處理影片的 Windows Media Player DSP 外掛程式，您必須先決定要讓外掛程式處理的影片格式。 範例影片 DSP 外掛程式適用于下列影片格式：

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

您選擇要處理的格式是由您決定。 您可以移除範例外掛程式的格式，使其不再受到支援，而且您可以加入程式碼來處理其他格式。

下列各節提供在為 Windows Media Player 建立自己的影片 DSP 外掛程式之前，您應該知道的其他資訊：

-   [範例影片 DSP 外掛程式中的影片格式協調](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [範例影片 DSP 外掛程式中的 DoProcessOutput](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [處理影片](processing-the-video.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行您的 DSP 程式碼**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




