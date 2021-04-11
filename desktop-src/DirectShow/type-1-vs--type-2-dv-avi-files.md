---
description: 類型-1 與
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: 類型1與類型 2 DV AVI 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944435"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a>類型1與類型 2 DV AVI 檔案

DV 攝影機產生交錯式音訊-影片;影片的每個畫面格也都包含音訊資訊。 如果您將 DV 資料儲存至 AVI 檔案，您可以選擇：

-   將交錯的資料儲存為 AVI 檔案中的一個資料流程。 這就是所謂的型別1檔。
-   將交錯的資料分割成不同的音訊和影片串流。 這就是所謂的2型別。

針對影片捕獲（最大輸送量很重要），最好使用類型1檔案，因為類型2檔案攜帶了重複的音訊資料。  (視頻串流仍包含音訊資料。 音訊是藉由將資料流程標示為影片來隱藏。 ) 另外，撰寫型別2檔案需要額外的處理器時間來分割交錯的資料流程。

另一方面，如果是即時編輯，則類型1檔案的效率較低。 應用程式必須從交錯的資料流程解壓縮音訊、進行編輯，然後再次交錯資料。 此外，類型1格式與 Microsoft® Video for Windows® (VFW) 不相容。 DirectShow 可以處理這兩種類型的檔案。

您可以使用 [DV Muxer](dv-muxer-filter.md) 篩選器，將類型2檔案轉換成類型1。 您可以使用 [DV 分隔](dv-splitter-filter.md) 器篩選器，將類型1檔案轉換成2型別。 下圖說明這兩種格式之間的差異。

![類型1和類型 2 dv 之間的轉換](images/dv-filters3.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> <dt>

[AVI 檔案格式的 DV 資料](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



