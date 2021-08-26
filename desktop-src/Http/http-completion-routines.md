---
title: HTTP 完成常式
description: 應用程式有數個選項可接收完成指示，並為開發人員提供一些彈性。
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd80259d806d81153a649ad606e40c10986090442e3cab5e04bd864367441871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981668"
---
# <a name="http-completion-routines"></a>HTTP 完成常式

應用程式有數個選項可接收完成指示，並為開發人員提供一些彈性。 這些選項會在等候 API 呼叫完成時封鎖，或使用完成常式進行非同步作業。 使用非同步作業的優點是可增加應用程式的回應能力。

## <a name="blocked-io"></a>封鎖的 i/o

應用程式可以在等候 API 呼叫完成時封鎖，方法是將重 [**迭結構設定**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 為 **Null**。 這真的會封鎖執行緒上的所有作業。 例如，在呼叫 [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)時，呼叫會封鎖，直到連接中斷為止。

## <a name="asynchronous-io"></a>非同步 i/o

偏好不封鎖的應用程式可以使用重迭 [**的結構來**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 取得完成結果。 應用程式會提供重 **迭結構的** 指標，該指標會與事件物件或完成埠一起使用。 使用 i/o 完成埠時，會使用 HTTP 控制碼做為檔案控制代碼，在非同步檔案 i/o 作業中。 下表摘要說明應用程式可用的完成選項。



| 重迭結構 | 事件物件   | 完成埠 | Completion                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| **NULL**             | 不適用 | 忽略         | 作業以同步方式完成。                                                                           |
| 非 **Null**         | 非 **Null**   | **NULL**        | 作業會以非同步方式完成。 重迭通知是藉由向事件物件發出信號來執行。       |
| 非 **Null**         | 忽略        | 非 **Null**    | 作業會以非同步方式完成。 重迭通知是藉由排程完成常式來執行。 |



 

## <a name="returning-the-number-of-bytes-read"></a>傳回讀取的位元組數目

某些使用重 [**迭結構進行**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 非同步完成的函式會傳回 *PBytesReceived* (或 *pBytesSent* 或 *pBytesRead*) 參數，指出同步傳輸的位元組數目。 若為非同步呼叫，這個參數應該設定為 **Null**。 針對同步呼叫， *pBytesReceived* 參數是選擇性的，而且可以是 **Null** 或非 **null**。

如果事件物件用於非同步完成，則會呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來判斷讀取的位元組數目。 如果使用完成埠 (*hFile* 參數與 i/o 完成埠) 相關聯，則應用程式會呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函式來判斷讀取的位元組數目。 如果非同步作業尚未完成，應用程式可以呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式來取得擴充的錯誤資訊。

下表摘要說明函式（例如使用 *pBytesReceived* 參數的 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) ）中同步和非同步完成的完成行為。



| pBytesReceived\* | pOverlapped  | 描述                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| **NULL**         | **NULL**     | 應用程式不會收到傳回的位元組數目資訊。           |
| **NULL**         | 非 **Null** | 非同步作業， *pBytesReceived* 沒有意義。                                |
| 非 **Null**     | **NULL**     | 同步作業， *pBytesReceived* 中傳回的位元組數目。                    |
| 非 **Null**     | 非 **Null** | 非同步作業，即使它不是 **Null**，也會忽略 *pBytesReceived* 。\*\* |



 

> [!Note]  
> \*此參數也可以是 *pBytesSent* 或 *pBytesRead*。

 

> [!Note]  
> \*\*建議應用程式在 *pBytesReceived* 中傳遞 **Null** 以進行非同步作業，並取得從 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)或 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)接收的位元組數目。

 

## <a name="return-codes"></a>傳回碼

HTTP 伺服器 API 會針對非同步函式呼叫傳回三個程式碼類別。

-   沒有 \_ 錯誤
-   錯誤 \_ IO \_ 暫止
-   任何其他 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

當錯誤 \_ IO \_ 暫止或 \_ 從非同步函式呼叫傳回錯誤時，使用者應該會預期事件或完成常式會收到信號。 針對事件或完成埠的 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)函數呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)函式，會傳回完成狀態。 此外，如果未 \_ 傳回任何錯誤，應用程式可以在進行 API 呼叫的相同執行緒上執行後續處理。

如果 HTTP 伺服器 API 傳回錯誤 \_ IO \_ 暫止或沒有錯誤的任何作業 \_ ，則從非同步函式呼叫中，完成常式不會收到信號，且 API 會直接傳回錯誤。

 

 