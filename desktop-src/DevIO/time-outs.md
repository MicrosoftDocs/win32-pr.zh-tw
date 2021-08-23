---
description: 通訊資源的控制碼有一組相關聯的超時參數，這些參數會影響讀取和寫入作業的行為。
ms.assetid: 271d4c68-1f6d-4483-a9a1-703220de761f
title: 逾時
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6226e8a2d13020bd4dc90a416e7ef359fbd919cf54e886c5e691e5fca2cdea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956787"
---
# <a name="time-outs"></a>逾時

通訊資源的控制碼有一組相關聯的超時參數，這些參數會影響讀取和寫入作業的行為。 逾時間隔可能會導致 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)或 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) 作業結束，即使未讀取或寫入指定的字元數也是一樣。 在讀取或寫入作業期間發生超時時，不會將它視為錯誤 (也就是說，讀取或寫入函式的傳回值表示成功) 。 實際讀取或寫入的位元組計數是由 **ReadFile** 或 **WriteFile** (或 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 或 [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) 函式報告，如果 i/o 是以重迭的作業) 來執行。

當應用程式開啟通訊資源時，系統會將資源的超時值設定為上次使用資源時生效的值。 如果通訊資源從未開啟，系統會將超時值設定為某些預設值。 無論是哪一種情況，應用程式都應該一律在開啟資源之後判斷目前的超時值，然後明確地將它們設定為符合其需求。 若要判斷通訊資源目前的超時值，請使用 [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) 函數。 若要變更超時值，請使用 [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) 函數。

超時參數會啟用兩種類型的超時。 當兩個字元的回條之間的時間超過指定的毫秒數時，就會發生間隔超時時間。 當收到第一個字元時開始計時，並在每個新字元收到時重新開機。 當讀取作業所耗用的總時間量超過計算的毫秒數時，就會發生總超時時間。 執行時間會在 i/o 作業開始時立即開始計時。 寫入作業僅支援總時間。 讀取作業支援間隔和總超時時間，可分別或合併使用。

讀取或寫入作業之總超時期間的時間（以毫秒為單位）是使用 [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts)或 [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)函數中指定的 [**COMMTIMEOUTS**](/windows/desktop/api/Winbase/ns-winbase-commtimeouts)結構的乘數和常數值計算。 使用下列公式：


```C++
Timeout = (MULTIPLIER * number_of_bytes) + CONSTANT
```



使用乘數和常數，會根據所要求的資料量，讓總逾時間隔有所差異。 應用程式只能使用常數，方法是將乘數設定為零，或將常數設定為零，只使用乘數。 如果常數和乘數都是零，就不會使用總超時時間。

如果所有讀取超時參數都是零，就不會使用讀取超時值，而且在讀取要求的位元組數目或發生錯誤之前，讀取作業不會完成。 同樣地，如果所有寫入超時參數都是零，寫入作業就會等到寫入要求的位元組數目或發生錯誤時才會完成。

如果讀取間隔超時參數是 **MAXDWORD** 值，而且讀取總超時參數都是零，讀取作業會在讀取輸入緩衝區中可用的任何字元之後立即完成，即使它是空的也是一樣。

當接收中有牢靠時，間隔時間會強制執行讀取作業。 使用間隔時間超時的進程可以設定相當短的間隔參數，讓它可以快速地回應一個或多個字元的小型、隔離的高載，但是在穩定的資料流程中收到資料時，仍可使用單一呼叫來收集大型的字元緩衝區。

當某一種流量控制封鎖傳輸，或呼叫 [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) 函式來暫停字元傳輸時，寫入作業的超時時間可能很有用。

下表摘要說明以 total 和 interval 時間的指定值為基礎的讀取作業行為。



| 總計 | 間隔 | 行為                                                                                                                                                                                 |
|-------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 0        | 當緩衝區完全填滿時傳回。 不會使用超時。                                                                                                                    |
| T     | 0        | 當緩衝區完全填滿，或自作業開始後的 T 毫秒經過時，會傳回。                                                                   |
| 0     | Y        | 當緩衝區填滿或在兩個字元的接收之間經過 Y 毫秒時，會傳回。 直到收到第一個字元時，才會開始計時。 |
| T     | Y        | 當緩衝區完全填滿或發生任何一種超時時，會傳回。                                                                                                     |



 

> [!Note]  
> 不過，該時間與控制實體裝置的系統相關。 若為遠端裝置（如數據機），時間相對於數據機所連接的伺服器系統。 在中，不會考慮任何網路傳播延遲。 例如，用戶端應用程式可能會指定計算為500毫秒的總超時時間。 當伺服器經過500毫秒時，會傳回用戶端的逾時錯誤。 如果有50毫秒的網路傳播延遲，用戶端將不會收到超時時間的通知，直到實際發生超時的50毫秒為止。

 

> [!Note]  
> 超時參數會影響通訊裝置上重迭的讀取和寫入作業行為。 使用重迭的 i/o 時， [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)、 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)或 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) 函數可以在作業完成之前傳回。 超時參數可判斷作業何時完成。

 

 

 
