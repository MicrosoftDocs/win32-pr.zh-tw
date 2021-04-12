---
description: 接收寫入器是編碼音訊或影片檔案的元件。
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: 接收寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318731"
---
# <a name="sink-writer"></a>接收寫入器

接收寫入器是編碼音訊或影片檔案的元件。

下圖顯示概要說明應用程式如何使用接收寫入器來編碼和音訊/影片檔案。

![顯示接收寫入器的圖表。](images/encoding09.png)

接收寫入器會裝載媒體接收，以及選擇性地裝載一或多個編碼器。 編碼器會將未壓縮的音訊或影片資料轉換成編碼 bitstreams。 媒體接收器會將 bitstreams 輸出至檔案。 接收寫入器會執行下列工作：

-   載入媒體接收器。
-   尋找並載入編碼器。
-   管理編碼器和媒體接收器的資料流程。

應用程式會將音訊/影片資料傳遞給接收寫入器作為輸入。 應用程式如何取得或產生輸入資料並不重要。 其中一個選項是使用 [來源讀取器](source-reader.md)，如下圖所示。 不過，接收寫入器不需要使用來源讀取器。 這兩個元件是獨立的。

![顯示來源讀取器和接收寫入器的圖表。](images/encoding02.png)

## <a name="in-this-section"></a>本節內容

-   [使用接收寫入器](using-the-sink-writer.md)
-   [教學課程：使用接收寫入器編碼影片](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編碼與檔案編寫](encoding-and-file-authoring.md)
</dt> <dt>

[媒體基礎中的編碼總覽](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



