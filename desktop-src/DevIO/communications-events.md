---
description: 進程可以監視通訊資源中發生的一組事件。 例如，應用程式可以使用事件監視來判斷 CTS (清除傳送) 和 DSR (資料集就緒) 發出變更狀態。
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: 通訊事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466bd5076405427c7c348c1df3706cb7b5c3edc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110704"
---
# <a name="communications-events"></a>通訊事件

進程可以監視通訊資源中發生的一組事件。 例如，應用程式可以使用事件監視來判斷 CTS (清除傳送) 和 DSR (資料集就緒) 發出變更狀態。

進程可以使用 [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) 函式來建立事件遮罩，以監視指定通訊資源上的事件。 若要判斷通訊資源的目前事件遮罩，處理常式可以使用 [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) 函數。 下列值會指定可以監視的事件。



| 值           | 意義                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EV \_ 中斷**   | 在輸入時偵測到中斷。                                                                                                                                                                                                                    |
| **EV \_ CTS**     | CTS (清除傳送) 信號變更狀態。                                                                                                                                                                                                     |
| **EV \_ DSR**     | DSR (資料集就緒) 信號已變更狀態。                                                                                                                                                                                                    |
| **EV \_ ERR**     | 發生行狀態錯誤。 行狀態錯誤為 **ce \_ 框架**、 **ce \_ 溢出** 和 **ce \_ RXPARITY**。                                                                                                                                        |
| **EV \_ 環形**    | 偵測到鈴聲指示器 (Indicator)。                                                                                                                                                                                                                    |
| **EV \_ RLSD**    | RLSD (接收行信號偵測) 信號已變更狀態。                                                                                                                                                                                       |
| **EV \_ RXCHAR**  | 會接收字元並放到輸入緩衝區。                                                                                                                                                                                          |
| **EV \_ RXFLAG**  | 已收到事件字元，並將其放在輸入緩衝區中。 事件字元是在裝置的 [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) 結構中指定的，此結構會使用 [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) 函數套用至序列埠。 |
| **EV \_ TXEMPTY** | 輸出緩衝區中的最後一個字元已傳送。                                                                                                                                                                                                 |



 

在指定一組事件之後，進程會使用 [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) 函數來等候其中一個事件發生。 **WaitCommEvent** 可以同步使用，或做為重迭的作業。 如需以重迭作業的形式執行函數的詳細資訊，請參閱 [同步](/windows/desktop/Sync/synchronization)處理。

當事件遮罩中指定的其中一個事件發生時，程式會完成等候作業，並設定事件遮罩變數來指出偵測到的事件種類。 如果針對通訊資源呼叫 [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) ，但該資源的等候暫止，則 [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) 會傳回錯誤。

[**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)函式會偵測自上一次呼叫 [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)或 **WaitCommEvent** 之後發生的事件。 例如，如果您將 **EV \_ RXCHAR** 事件指定為等待滿足的事件，當驅動程式輸入緩衝區中的字元自上一次呼叫 **WaitCommEvent** 或 **SetCommMask** 之後，就會滿足 **WaitCommEvent** 的呼叫。 因此，假設有下列的虛擬化，在 T1 和 T2 之間收到的任何字元都會滿足下一次的 **WaitCommEvent** 呼叫。


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



當您監視當信號 (CTS、DSR 等) 變更狀態時所發生的事件時， [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) 會回報變更，但不會報告目前的狀態。 若要查詢 CTS 的目前狀態 (清除傳送) 、DSR (資料準備就緒) 、RLSD (接收行信號偵測) 和環形指標信號，處理常式可以使用 [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus) 函式。

 

 
