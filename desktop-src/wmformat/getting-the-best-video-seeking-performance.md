---
title: 取得最佳的影片搜尋效能
description: 取得最佳的影片搜尋效能
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media Format SDK，最佳的影片搜尋效能
- 先進的系統格式 (ASF) ，最佳的影片搜尋效能
- ASF (Advanced Systems Format) ，最佳的影片搜尋效能
- 先進的系統格式 (ASF) 、影片搜尋效能
- ASF (Advanced Systems Format) ，影片搜尋效能
- Advanced Systems Format (ASF) ，效能
- ASF (Advanced Systems Format) ，效能
- 影片搜尋
- 效能、影片搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969052"
---
# <a name="getting-the-best-video-seeking-performance"></a>取得最佳的影片搜尋效能

搜尋檔案中的內容是很常見的作業，可能會發生效能問題。 以 Windows Media 視訊9編解碼器編碼的影片主要是由差異框架組成，其只會記錄與先前畫面格相關的變更。 重建差異框架需要一些時間，特別是在主要畫面格太遠的時候。 如需設定主要畫面格以進行有效率搜尋的詳細資訊，請參閱設定 [影片串流以搜尋效能](configuring-video-streams-for-seeking-performance.md)。

除了適當的設定之外，您還可以使用影片串流的框架索引來改善搜尋效能。 搜尋框架號碼通常比搜尋展示時間更快。

如果搜尋具有多個資料流程的檔案，您應該只選取所需的資料流程。 針對讀取設定的每個資料流程都會影響搜尋的效能，因為當您搜尋至檔案中的某個點時，會同步處理所有選取的資料流程。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> <dt>

[**使用非同步讀取器依框架編號搜尋**](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[**使用同步讀取器依框架編號搜尋**](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[**使用非同步讀取器依時間進行搜尋**](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[**使用同步讀取器依時間進行搜尋**](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




