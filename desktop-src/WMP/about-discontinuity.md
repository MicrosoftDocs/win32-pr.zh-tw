---
title: 關於中斷
description: 關於中斷
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，音訊中斷
- DSP 外掛程式、音訊中斷
- 音訊 DSP 外掛程式，中斷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371906"
---
# <a name="about-discontinuity"></a>關於中斷

Windows Media Player 可以在輸入資料流程中的任何時間，藉由呼叫 **IMediaObject：:D iscontinuity** 方法來發出信號。 這會定期發生于資料流程的開頭和結尾，也會在每次搜尋作業之前，或串流內容因任何原因而中斷時進行。 Windows Media Player 外掛程式嚮導所產生的範例 DSP 外掛程式不需要處理不連續，原因如下：

-   PCM 範例是不可部分完成的，這表示它們可以在不考慮串流中其他範例的情況下進行處理。 某些影片格式包含相依于主要畫面格和壓縮範例的資料。
-   撰寫範例程式碼時，一律會強制用戶端處理所有輸出，然後外掛程式才會接受更多輸入。

**IMediaObject：:D iscontinuity** 的預設執行只會傳回 S \_ OK。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行音訊 DSP 外掛程式**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




