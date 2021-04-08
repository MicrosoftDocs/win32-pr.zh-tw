---
title: 轉譯內容
description: 轉譯內容
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows Media Format SDK，轉譯內容
- Advanced Systems Format (ASF) 、轉譯內容
- ASF (Advanced Systems Format) ，轉譯內容
- Advanced Systems Format (ASF) 、內容轉譯
- ASF (Advanced 系統格式) 、內容轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840732"
---
# <a name="rendering-content"></a>轉譯內容

Windows Media 格式 SDK 不提供任何常式來轉譯讀取器物件所傳遞的內容。 如果您撰寫應用程式來播放 ASF 檔案中的內容，則必須執行您自己的轉譯常式。

轉譯內容時，您必須小心，以確保會以呈現時間的順序轉譯樣本，並且在轉譯時同步處理來自不同資料流程的樣本。 您用來確保資料流程同步處理的方法，將取決於您針對應用程式所使用的轉譯技術。 一般而言，如果您有音訊和影片串流，則應該同步處理至音訊串流，因為音訊串流中的不一致會比影片串流中的幾個已捨棄的框架更明顯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> <dt>

[**使用非同步讀取器取出媒體範例**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**使用同步讀取器取出媒體範例**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




