---
description: 發生硬體或軟體例外時，處理器會在發生例外狀況的時間點停止執行，並將控制權轉移至系統。
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: 例外狀況分派
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b7b4f73c9d2c3fbaf15b4390ee6ecc6b9aa06b50524ec080fc45319d3b94767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912728"
---
# <a name="exception-dispatching"></a>例外狀況分派

發生硬體或軟體例外時，處理器會在發生例外狀況的時間點停止執行，並將控制權轉移至系統。 首先，系統會儲存目前線程的電腦狀態，以及描述例外狀況的資訊。 系統接著會嘗試尋找例外狀況處理常式來處理例外狀況。

發生例外狀況之執行緒的電腦狀態會儲存在 [**內容**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) 結構中。 這項資訊 (稱為 *內容記錄*) 可讓系統在例外狀況成功處理時，于例外狀況的位置繼續執行。 例外狀況的描述 (稱為例外狀況 **記錄**) 會儲存在例外狀況 [**\_ 記錄**](/windows/desktop/api/WinNT/ns-winnt-exception_record) 結構中。 因為它會將內容記錄的電腦相依資訊與例外狀況記錄的電腦獨立資訊分開儲存，所以例外狀況處理機制可移植至不同的平臺。

您可以使用 [**GetExceptionInformation**](getexceptioninformation.md) 函式來取得內容和例外狀況記錄中的資訊，並可將其提供給因例外狀況而執行的任何例外狀況處理常式。 例外狀況記錄包含下列資訊。

-   識別例外狀況類型的例外狀況代碼。
-   指出例外狀況是否可持續的旗標。 任何在 noncontinuable 例外狀況之後繼續執行的嘗試都會產生另一個例外狀況。
-   另一個例外狀況記錄的指標。 這有助於在發生嵌套例外狀況時建立連結的例外狀況清單。
-   發生例外狀況的位址。
-   引數陣列，提供例外狀況的其他資訊。

當使用者模式程式碼中發生例外狀況時，系統會使用下列搜尋順序來尋找例外狀況處理常式：

1.  如果正在調試進程，系統就會通知偵錯工具。 如需詳細資訊，請參閱 [偵錯工具例外狀況處理](debugger-exception-handling.md)。
2.  如果進程未進行調試，或相關聯的偵錯工具未處理例外狀況，則系統會藉由搜尋發生例外狀況之執行緒的堆疊框架，嘗試尋找以框架為基礎的例外狀況處理常式。 系統會先搜尋目前的堆疊框架，然後以反向順序搜尋先前的堆疊框架。
3.  如果找不到以框架為基礎的處理常式，或沒有任何以框架為基礎的處理常式處理例外狀況，但進程正在進行調試，系統會第二次通知偵錯工具。
4.  如果進程未進行調試，或相關聯的偵錯工具未處理例外狀況，則系統會根據例外狀況類型提供預設處理。 針對大部分的例外狀況，預設動作是呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函數。

當核心模式程式碼中發生例外狀況時，系統會在嘗試找出例外狀況處理常式的情況下，搜尋核心堆疊的堆疊框架。 如果找不到處理程式，或沒有處理常式處理例外狀況，則系統會關閉，如同已呼叫 [**ExitWindows**](/windows/win32/api/winuser/nf-winuser-exitwindows) 函數。

 

 
