---
title: 影像串流
description: 影像串流
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows媒體格式 SDK，映射資料流程
- 先進的系統格式 (ASF) 、影像串流
- ASF (Advanced 系統格式) 、影像串流
- Windows媒體格式 SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 影像串流，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2067710e6b2be627bd16125d73e567a2f1ba1557ae01b81f55712d8c5a7b8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702862"
---
# <a name="image-streams"></a>影像串流

影像串流是一種特殊類型的資料流程，其中包含指派給簡報時間的靜止影像。 應用程式可以視需要在影像資料流程中顯示圖片，但一般的執行是在下一張圖片（例如投影片放映）之前顯示每張圖片。 影像資料流程通常會在具有音訊串流的檔案中進行編碼，以產生與音樂或語音同步處理的簡單影像呈現。

影像串流就像是影片串流，因為它們是從未壓縮的範例所建立，而這些樣本會壓縮為檔案撰寫程式的一部分，但它們也與任意資料流程相同，因為您必須為內容指派適當的位元速率和緩衝區視窗，而不需要依賴編解碼器指派的屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**任意資料流程**](arbitrary-streams.md)
</dt> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**音訊和影片串流**](audio-and-video-streams.md)
</dt> <dt>

[**寫入影像資料流程**](writing-image-streams.md)
</dt> </dl>

 

 




