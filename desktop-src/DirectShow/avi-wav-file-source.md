---
description: AVI/WAV 檔案來源
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: AVI/WAV 檔案來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8c99de9eed21afa716c4f3ee81a5d1cc4e9731739526f7c9531c758b30a22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689358"
---
# <a name="aviwav-file-source"></a>AVI/WAV 檔案來源

(已淘汰。 若是 AVI 和 WAV 檔案，請使用檔案 [來源 (Async) ](file-source--async--filter.md) 和 [AVI 分隔器](avi-splitter-filter.md) 或 [WAVE](wave-parser-filter.md)剖析器。 ) 

AVI/WAV 檔案來源篩選器會讀取 AVI 和 WAV 來源檔案，並針對檔案類型產生適當的輸出圖釘。

針對 WAV 檔案，此篩選會建立音訊輸出針腳，以產生可連接到音訊轉譯篩選器或仲介音訊轉換篩選器的音訊串流。

對於 AVI 檔案，此篩選會建立影片輸出圖釘，它會產生適合 AVI 編解碼器篩選器的壓縮 AVI 資料流程，而音訊輸出圖釘則會產生適合音訊轉譯篩選或中間音訊轉換篩選的音訊串流。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



