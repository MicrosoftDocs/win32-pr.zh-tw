---
description: 電話語音的互動式本質需要 TAPI 成為即時操作環境。
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: 同步/非同步模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b3d3b58e9704719e502fa3efc11bc4dc216479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981567"
---
# <a name="synchronousasynchronous-model"></a>同步/非同步模型

電話語音的互動式本質需要 TAPI 成為即時操作環境。 需要許多 TAPI 功能才能快速完成，並以同步方式將其結果傳回給應用程式。 其他函式 (例如撥號) 可能無法快速完成，因此會以非同步方式運作。

電話語音作業會以同步或非同步方式完成。 這兩個模型的差異如下所示。 *同步* 函式會先執行整個要求，呼叫端的執行緒才能從函式呼叫傳回。 *非同步* 函式會在要求完整執行之前傳回。 當非同步要求稍後完成時，服務提供者會藉由呼叫 TAPI 最初在初始化順序中提供給它的回呼程式來報告完成。

-   非同步作業有一個名為 *dwRequestID* 的參數，其定義的類型 [winspool.drv \_ REQUESTID](./drv-requestid.md) 作為其第一個參數。 這類作業會在函式呼叫中執行其處理的一部分，並在函式呼叫傳回之後，于獨立的執行執行緒中執行其處理的其餘部分。 當函式傳回時，它會傳回負錯誤結果或在函式呼叫中傳遞的 (正) *dwRequestID* 。 負誤差結果表示作業已完成 (且) 失敗。 傳回的正面 *dwRequestID* 表示作業會繼續在獨立執行緒中執行。 在這種情況下，服務提供者最後會呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 程式，並傳遞 *dwRequestID* 和結果碼來指出作業的結果。 結果碼為零表示成功，或一組相同的 (負) 錯誤結果。 在任何情況下，服務提供者絕不能從指定為非同步函式傳回零或 *dwRequestID* 以外的任何正值，因為這樣做可能會產生非預期的結果。 服務提供者應該一律將輸入資料從應用程式記憶體複製到服務提供者記憶體中，然後再從非同步函式傳回。
-   同步作業沒有 *dwRequestID* 作為其第一個參數。 這類作業會在呼叫端的執行執行緒中執行其所有處理，並在傳回時傳回最終結果。 結果為零表示成功或負錯誤碼（失敗）。 服務提供者不會針對同步作業呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 。

請特別注意，相對於原始要求傳回時的「完成」回呼的時機。 一般的非同步要求會由服務提供者所執行，如下列虛擬程式碼所示：

``` syntax
Some_request(Request_ID, ...) {
  check parameters for validity
  check device state for validity
  store Request_ID for Completion Interrupt Handler's use
  manipulate device registers to start physical operation
  return Request_ID  // to indicate asynch operation
}
Operation Completion Interrupt Handler: {
  if operation was successful then
    call "completion" callback passing Request_ID and "success"
  else
    call "completion" callback passing Request_ID and "error num"
  endif
}
```

如果作業順利完成 (或原始要求傳回非常緩慢的) ，則可能會在原始要求回到應用程式之前或甚至是 TAPI 之前，觸發在實體作業完成時執行的中斷處理常式。 這是允許的行為。 TAPI 保證應用程式的最終完成通知會在原始要求傳回之後傳遞。

**TAPI 2.x：** 列出每個函式是以同步方式完成或以非同步方式出現在 [TAPI 快速函數參考](./tapi-quick-function-reference.md)中的狀態。

 

 
