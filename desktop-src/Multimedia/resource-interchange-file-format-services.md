---
title: 資源交換檔案格式服務
description: 資源交換檔案格式服務
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- '多媒體檔案 i/o、資源交換檔案格式 (RIFF) '
- '檔案 i/o、資源交換檔案格式 (RIFF) '
- '輸入和輸出 (i/o) 、資源交換檔案格式 (RIFF) '
- 'I/o (輸入和輸出) 、資源交換檔案格式 (RIFF) '
- mmioOpen 函式
- " (RIFF) 的資源交換檔案格式"
- 'RIFF (資源交換檔案格式) '
- RIFF I/O
- RIFF 區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cca3792ccded248951065c7b69f2e50d27e0ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314680"
---
# <a name="resource-interchange-file-format-services"></a>資源交換檔案格式服務

多媒體檔案的慣用格式是 (RIFF) 的資源交換檔案格式。 RIFF 檔案 i/o 函式適用于基本的緩衝和無緩衝檔案 i/o 服務。 您可以用與其他檔案類型相同的方式來開啟、讀取和寫入 RIFF 檔案。 如需 RIFF 的詳細資訊，請參閱 [AVIFile 函數和宏](avifile-functions-and-macros.md)。

RIFF 檔案會使用四個字元的代碼來識別檔案元素。 這些程式碼是32位的數量，代表一到四個 ASCII 英數位元的序列，並以空白字元填補右邊。 四個字元代碼的資料類型為 **FOURCC**。 使用 [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) 宏將四個字元轉換成四個字元的代碼。 若要將以 null 終止的字串轉換成四個字元的程式碼，請使用 [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) 函式。

RIFF 檔的基本組建區塊是一個 *區塊*。 區塊是多媒體資料的邏輯單元，例如影片剪輯中的單一畫面格。 每個區塊都包含下欄欄位：

-   指定區塊識別碼的四個字元的代碼
-   指定區塊中資料成員大小的雙精度值
-   資料欄位

下圖顯示包含兩個 subchunks 的 "RIFF" 區塊。

![riff 包含兩個 subchunks 影像的區塊](images/mmio1.gif)

包含在另一個區塊中的區塊是 *subchunk*。 唯一允許包含 subchunks 的區塊是具有 "RIFF" 或 "LIST" 區塊識別碼的區塊。 包含另一個區塊的區塊稱為 *父區塊*。 RIFF 檔案中的第一個區塊必須是 "RIFF" 區塊。 檔案中的所有其他區塊都是 "RIFF" 區塊的 subchunks。

"RIFF" 區塊在資料欄位的前四個位元組中包含額外的欄位。 這個額外的欄位提供欄位的 *表單類型* 。 表單類型是四個字元的代碼，可識別儲存在檔案中的資料格式。 例如，Microsoft 波形-音訊檔案的格式為 "WAVE"。

「清單」區塊也會在資料欄位的前四個位元組中包含額外的欄位。 此額外欄位包含欄位的 *清單類型* 。 清單類型是識別清單內容的四個字元的代碼。 例如，清單類型為 "INFO" 的 "LIST" 區塊可以包含 "ICOP" 和 "ICRD" 區塊，以提供著作權和建立日期資訊。 下圖顯示「RIFF」區塊，其中包含「清單」區塊和另一個 subchunk (「清單」區塊包含兩個 subchunks) 。

![包含清單區塊影像的 riff 區塊](images/mmio2.gif)

多媒體檔案 i/o 服務包含兩個函式，可供您在 RIFF 檔中的區塊之間進行流覽： [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) 和 [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)。 您可以使用這些函數做為高階搜尋函式。 當您下降到區塊時，檔案位置會設定為區塊的資料欄位， (從區塊開頭算起的8個位元組) 。 針對 "RIFF" 和 "LIST" 區塊，檔案位置會設定為表單類型或清單類型後面的位置， (從區塊開頭的12個位元組開始) 。 當您將區塊遞增時，檔案位置會設定為在區塊結尾之後的位置。

若要建立新的區塊，請使用 [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) 函式，在開啟的檔案中的目前位置寫入區塊標頭。 **MmioAscend**、 **mmioDescend** 和 **MmioCreateChunk** 函式會使用 [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)結構來指定和取得 "RIFF" 區塊的相關資訊。

 

 