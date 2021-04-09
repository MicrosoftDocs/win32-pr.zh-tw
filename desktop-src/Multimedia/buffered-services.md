---
title: 緩衝的服務
description: 緩衝的服務
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- 多媒體檔案 i/o、緩衝的服務
- 檔案 i/o，緩衝服務
- 輸入和輸出 (i/o) 、緩衝的服務
- I/o (輸入和輸出) 、緩衝的服務
- 緩衝的 i/o
- mmioOpen 函式
- 內部 i/o 緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d014ed765609dd43886cc7b33987f8fd5ac7e65a
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "103945543"
---
# <a name="buffered-services"></a>緩衝的服務

存取媒體裝置時，大部分的檔案 i/o 額外負荷都會發生。 如果您正在讀取或寫入許多小部分的資訊，裝置可能會花很多時間移至媒體上的實體位置，以進行每個讀取或寫入操作。 在此情況下，您可以使用緩衝的檔案 i/o 服務來達到更佳的效能。 使用緩衝的 i/o 時，檔案 i/o 管理員會維護一個大於您正在讀取或寫入之資訊區塊的中繼緩衝區。 只有當緩衝區必須填滿或寫入磁片時，才會存取裝置。

在您設定和使用緩衝的檔案 i/o 之前，您必須決定是否要檔案 i/o 管理員或應用程式佈建緩衝區。 更簡單的方式是讓檔案 i/o 管理員配置緩衝區。 但是，如果您想要直接存取緩衝區或開啟記憶體檔案，您可以讓應用程式佈建緩衝區。 如需使用記憶體檔案的詳細資訊，請參閱 [執行記憶體檔 i/o](performing-memory-file-i-o.md)。 如需直接存取 i/o 緩衝區的範例，請參閱存取檔案 [I/o 緩衝區](accessing-a-file-i-o-buffer.md)

檔案 i/o 管理員所配置的緩衝區稱為內部 i/o 緩衝區。 若要使用內部緩衝區開啟已緩衝處理之 i/o 的檔案，請 \_ 在使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 函數開啟檔案時，指定 MMIO ALLOCBUF 旗標。 下圖顯示在開啟檔案以進行緩衝讀取作業之後，檔案 i/o 緩衝區的初始狀態。 緩衝是透明的; 您可以讀取和搜尋，就像是使用未緩衝處理的 i/o 一樣。 **MmioOpen** 函式已設定 PchNext 和 *pchEndRead* ，以指向檔案 i/o 緩衝區的開頭。

![顯示「pchEndRead」和「pchNext」指向檔案 i/o 緩衝區開頭的螢幕擷取畫面。](images/mmio7.gif)

下圖顯示檔案開啟以進行緩衝寫入作業之後，檔案 i/o 緩衝區的初始狀態。 **MmioOpen** 函式已設定 **pchNext** 指向檔案 i/o 緩衝區的開頭，而 **pchEndWrite** 指向緩衝區的結尾。

![在檔案 i/o 緩衝區開頭顯示 ' pchNext '，並在結尾顯示 ' pchEndWrite ' 的螢幕擷取畫面。](images/mmio11.gif)

內部 i/o 緩衝區的預設大小為8K。 如果這個大小不適當，您可以使用 [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) 函數來變更緩衝區大小。 您也可以使用此函式，在針對未緩衝處理的 i/o 開啟的檔案上啟用緩衝處理，或是提供您自己的緩衝區作為記憶體檔案使用。

您可以使用 [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) 函式，將 i/o 緩衝區的內容強制寫入磁片。 但是，當您使用 [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) 函式來關閉檔案時，不需要呼叫 **mmioFlush** 來排清 I/o 緩衝區，而 **mmioClose** 函式會自動將其清除。 如果您用盡磁碟空間， **mmioFlush** 可能會失敗，即使先前對 [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) 函式的呼叫成功。 同樣地， **mmioClose** 可能會在清除其 i/o 緩衝區時失敗。

與效能相關的應用程式（例如從 CD-ROM 即時串流資料的應用程式）可以直接存取 i/o 緩衝區來優化檔案 i/o 效能。 如果您選擇這麼做，您應該要特別小心，因為您略過檔案 i/o 管理員所提供的一些保護和錯誤檢查。

多媒體檔案 i/o 管理員會使用 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) 結構來維護開啟檔案的相關狀態資訊。 您可以使用此結構中的三個成員來讀取和寫入 i/o 緩衝區： **pchNext**、 **pchEndRead** 和 **pchEndWrite**。 **PchNext** 成員指向緩衝區中要讀取或寫入的下一個位置。 您必須在讀取和寫入緩衝區時，遞增這個成員。 **PchEndRead** 成員會識別您可以從緩衝區讀取的最後一個有效字元。 同樣地，這個成員會識別緩衝區中您可以寫入的最後一個位置。 更精確地說， **pchEndRead** 和 **pchEndWrite** 會指向緩衝區中最後一個有效資料之後的記憶體位置。 您可以使用 [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) 和 [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) 函數來取得和設定有關檔案 i/o 緩衝區的狀態資訊。 下圖顯示在讀取作業期間，應用程式呼叫 **mmioAdvance** 之後 i/o 緩衝區的狀態。 **MmioAdvance** 函式會填滿緩衝區，並將 **pchEndRead** 指標設定為緩衝區的結尾。

![在檔案 i/o 緩衝區開頭顯示 ' pchNext '，並在結尾顯示 ' pchEndRead ' 的螢幕擷取畫面。](images/mmio8.gif)

在下圖中，應用程式會在 **pchNext** 所指定的位置從 i/o 緩衝區讀取，並將指標前進。

![在檔案 i/o 緩衝區中間顯示 ' pchNext '，並在結尾顯示 ' pchEndRead ' 的螢幕擷取畫面。](images/mmio9.gif)

同樣地，在寫入作業中，應用程式會寫入 i/o 緩衝區，並將 **pchNext** 指標前進，如下圖所示。

![在檔案 i/o 緩衝區中間顯示 ' pchNext '，並在結尾顯示 ' pchEndWrite ' 的螢幕擷取畫面。](images/mmio12.gif)

應用程式填滿緩衝區之後，它會呼叫 **mmioAdvance** 將緩衝區排清到磁片。 **MmioAdvance** 函式會將 **pchNext** 重設為指向緩衝區的開頭，如下圖所示。

![在檔案 i/o 緩衝區開頭顯示 ' pchNext ' 的螢幕擷取畫面、E O F 中間的緩衝區，以及緩衝區結尾的 ' pchEndWrite '。](images/mmio13.gif)

當您到達 i/o 緩衝區的結尾時，如果您正在進行寫入，則必須將緩衝區前移以從磁片填滿磁片（如果您正在讀取）或將它排清至磁片。 使用 [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) 函式來推進 i/o 緩衝區。 若要從磁片填入 i/o 緩衝區，請使用 **mmioAdvance** 搭配 MMIO \_ READ 旗標。 如果檔案中沒有足夠的資料來填滿緩衝區， **MMIOINFO** 結構的 **pchEndRead** 成員會指向緩衝區中最後一個有效位元組後面的位置。 若要將緩衝區排清到磁片，請 \_ 在 **MMIOINFO** 結構的 **DWFLAGS** 成員中設定 mmio DIRTY 旗標，然後使用 MMIO WRITE 旗標來呼叫 **mmioAdvance** \_ 。

例如，在讀取作業期間， **mmioAdvance** 函式會設定 **pchEndRead** 以指向緩衝區中有效資料的結尾，如下圖所示。

![在檔案 i/o 緩衝區開頭顯示 ' pchNext ' 的螢幕擷取畫面、E O F 結尾的緩衝區，以及緩衝區結尾的 ' pchEndRead '。](images/mmio10.gif)

同樣地，在寫入作業期間，應用程式會呼叫 **mmioAdvance** 來排清緩衝區，並將 **pchNext** 前移至緩衝區中有效資料的結尾，如下圖所示。

![檔案 i/o 緩衝區映射](images/mmio14.gif)

 

 