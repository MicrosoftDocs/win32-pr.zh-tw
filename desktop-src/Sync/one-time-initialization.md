---
description: 元件的設計通常是在第一次呼叫時執行初始化工作，而不是在載入時執行。
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: One-Time 初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f451e3c51716b4ff6f33b55d8d8602b5d5c28f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971615"
---
# <a name="one-time-initialization"></a>One-Time 初始化

元件的設計通常是在第一次呼叫時執行初始化工作，而不是在載入時執行。 單次初始化函式可確保此初始化只會發生一次，即使有多個執行緒可能會嘗試初始化亦同。

**Windows Server 2003 和 WINDOWS XP：** 應用程式必須使用 [連鎖函數](interlocked-variable-access.md) 或其他同步處理機制，提供自己的同步處理進行單次初始化。 從 Windows Vista 和 Windows Server 2008 開始，可以使用一次性的初始化函數。

單次初始化函數可提供顯著的優點，以確保只有一個執行緒執行初始化：

-   它們已針對速度優化。
-   他們會在需要它們的處理器架構上建立適當的阻礙。
-   它們支援鎖定和平行初始化。
-   它們可避免內部鎖定，因此程式碼可以非同步或同步方式運作。

系統會透過不透明的 **INIT \_ 一** 結構（包含資料和狀態資訊）來管理初始化程式。 呼叫端會配置此結構，並藉由呼叫 [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) (初始化結構，以動態方式初始化結構，) 或將常數 init 指派給結構變數 (以) 靜態方式初始化結構。 **\_ \_ \_** 一開始，儲存在單次初始化結構中的資料是 Null，且其狀態為未初始化。

無法跨進程共用一次性的初始化結構。

執行初始化的執行緒可以選擇性地設定在初始化完成之後可供呼叫端使用的內容。 內容可以是同步處理物件，也可以是值或資料結構。 如果內容是一個值，則 **\_ \_ CTX \_ 保留的 \_ 位一旦** 必須為零，則其低順序初始化。 如果內容是資料結構，資料結構必須對齊 **DWORD**。 在 [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize)或 [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce)函數的 *lpCoNtext* output 參數中，會將內容傳回給呼叫端。

單次初始化可以同步或非同步方式執行。 選擇性的回呼函數可以用於同步單次初始化。

## <a name="synchronous-one-time-initialization"></a>同步單次初始化

下列步驟描述未使用回呼函數的同步單次初始化。

1.  呼叫 [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) 函式的第一個執行緒成功導致單次初始化開始。 若為同步單次初始化，則必須呼叫 **InitOnceBeginInitialize** ，而不需要 **INIT one \_ \_ ASYNC** 旗標。
2.  嘗試初始化的後續執行緒會被封鎖，直到第一個執行緒完成初始化或失敗為止。 如果第一個執行緒失敗，則會允許下一個執行緒嘗試初始化，依此類推。
3.  初始化完成時，執行緒會呼叫 [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) 函數。 執行緒可以選擇性地建立 (或其他內容資料) 的同步處理物件，並在 **InitOnceComplete** 函數的 *lpCoNtext* 參數中指定它。
4.  如果初始化成功，則會將單次初始化結構的狀態變更為已初始化，而如果有任何) 儲存在初始化結構中，則 *lpCoNtext* 控制碼 (。 後續的初始化嘗試會傳回此內容資料。 如果初始化失敗，資料會是 **Null**。

下列步驟描述使用回呼函數的同步單次初始化。

1.  成功呼叫 [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) 函式的第一個執行緒會將指標傳遞至應用程式定義的 [*InitOnceCallback*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) 回呼函式，以及回呼函數所需的任何資料。 如果呼叫成功，則會執行 *InitOnceCallback* 回呼函數。
2.  嘗試初始化的後續執行緒會被封鎖，直到第一個執行緒完成初始化或失敗為止。 如果第一個執行緒失敗，則會允許下一個執行緒嘗試初始化，依此類推。
3.  初始化完成時，回呼函數會傳回。 回呼函數可以選擇性地建立 (或其他內容資料) 的同步處理物件，並在其 *內容* 輸出參數中指定。
4.  如果初始化成功，則會將一次性初始化結構的狀態變更為已初始化，而如果有任何) 儲存在初始化結構中，則 *內容* 控制碼 (。 後續的初始化嘗試會傳回此內容資料。 如果初始化失敗，資料會是 **Null**。

## <a name="asynchronous-one-time-initialization"></a>非同步單次初始化

下列步驟說明非同步一次性初始化。

1.  如果多個執行緒同時嘗試在 **\_ \_ ASYNC** 呼叫 [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize)和 INIT 來開始初始化，則將 *fPending* 參數設為 **TRUE** 的所有線程都能成功執行該函式。 只有一個執行緒在初始化時實際上會成功：其他並行嘗試則不會變更初始化狀態。
2.  當 [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) 傳回時， *fPending* 參數會指出初始化狀態：
    -   如果 *fPending* 為 **FALSE**，則表示一個執行緒在初始化時成功。 其他執行緒應清除其所建立的任何內容資料，並使用 [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize)之 *lpCoNtext* 輸出參數中的內容資料。
    -   如果 *fPending* 為 **TRUE**，表示初始化尚未完成，而且其他執行緒應該繼續。
3.  每個執行緒都會呼叫 [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) 函數。 執行緒可以選擇性地建立 (或其他內容資料) 的同步處理物件，並在 **InitOnceComplete** 的 *lpCoNtext* 參數中指定它。
4.  當 [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) 傳回時，它的傳回值會指出呼叫執行緒是否在初始化時成功。
    -   如果 [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) 成功，呼叫的執行緒就會在初始化時成功。 如果任何) 儲存在初始化結構中，則一次性初始化結構的狀態會變更為已初始化，而 *lpCoNtext* 控制碼 (。
    -   如果 [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) 失敗，則另一個執行緒在初始化時成功。 呼叫端執行緒應該清除其所建立的任何內容資料，並使用 INIT 呼叫 [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) **\_ 一次，只要 \_ 檢查 \_** 一次就能取出儲存在單次初始化結構中的任何內容資料。

## <a name="calling-one-time-initialization-from-multiple-sites"></a>從多個網站呼叫 One-Time 初始化

一次由單一 INIT 所保護的 **單次 \_** 初始化結構可以從多個網站執行; 您可以從每個網站傳遞不同的回呼，而且可以混合使用與不含回呼的同步處理。 初始化仍 guaranted 為只執行一次 sucesfully。

但是，非同步和同步初始化無法混用：一旦嘗試非同步初始化，嘗試啟動同步初始化會失敗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 One-Time 初始化](using-one-time-initialization.md)
</dt> </dl>

 

 
