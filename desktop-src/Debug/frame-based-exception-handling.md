---
description: 以框架為基礎的例外狀況處理常式，可讓您處理例外狀況可能會發生在特定程式碼序列中的可能性。 以框架為基礎的例外狀況處理常式是由下列元素所組成。
ms.assetid: 07aac772-f917-48b7-91a9-3b5d4cb43600
title: 以框架為基礎的例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb72118aca7653e9bc15e7f4ff4b75e46b1abad5bab7dee4a3397ae5f98e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573118"
---
# <a name="frame-based-exception-handling"></a>以框架為基礎的例外狀況處理

以 *框架為基礎的例外狀況處理常式* ，可讓您處理例外狀況可能會發生在特定程式碼序列中的可能性。 以框架為基礎的例外狀況處理常式是由下列元素所組成。

-   受保護的程式碼主體
-   篩選運算式
-   例外狀況處理常式區塊

以特定語言的語法宣告以框架為基礎的例外狀況處理常式。 例如，在 Microsoft c/c + + 優化編譯器中，它們是使用 **\_ \_ try** 和 **\_ \_ except** 來執行。 如需詳細資訊，請參閱 [處理常式語法](handler-syntax.md)。

*受保護的程式碼主體* 是一組一或多個語句，篩選運算式和例外狀況處理常式區塊會提供例外狀況處理保護。 受防護主體可以是程式碼區塊、一組嵌套區塊，或整個程式或函式。 使用 Microsoft C/c + + 優化編譯器，受保護的主體會以大括弧括住， ({}) 在 **\_ \_ try** 關鍵字之後。

以框架為基礎之例外狀況處理常式的 *篩選運算式* 是在受防護主體中發生例外狀況時，由系統評估的運算式。 這項評估會產生系統的下列其中一項動作。

-   系統會停止其搜尋例外狀況處理常式、還原電腦狀態，並在發生例外狀況的位置繼續執行執行緒。
-   系統會繼續搜尋例外狀況處理常式。
-   系統會將控制項傳送至例外狀況處理常式，然後在找到例外狀況處理常式的堆疊框架中依序繼續執行執行緒。 如果處理常式不在發生例外狀況的堆疊框架中，系統會回溯堆疊，離開目前的堆疊框架和任何其他堆疊框架，直到它回到例外狀況處理常式的堆疊框架為止。 在執行例外狀況處理常式之前，會針對因將控制項傳送至例外狀況處理常式而終止的任何程式碼受防護主體執行終止處理常式。 如需終止處理常式的詳細資訊，請參閱 [終止處理](termination-handling.md)。

篩選運算式可以是簡單運算式，也可以叫用嘗試處理例外狀況的 *篩選函數* 。 您可以從篩選運算式內呼叫 [**GetExceptionCode**](getexceptioncode.md) 和 [**GetExceptionInformation**](getexceptioninformation.md) 函數，以取得所篩選之例外狀況的相關資訊。 **GetExceptionCode** 會傳回可識別例外狀況類型的程式碼，而 **GetExceptionInformation** 會傳回 [**例外狀況 \_ 指標**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) 結構的指標，其中包含 [**內容**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) 和 [**例外狀況 \_ 記錄**](/windows/desktop/api/WinNT/ns-winnt-exception_record) 結構的指標。

這些函數無法從篩選函式內呼叫，但其傳回值可以做為參數傳遞至篩選函數。 [**GetExceptionCode**](getexceptioncode.md) 可用於例外狀況處理常式區塊內，但 [**GetExceptionInformation**](getexceptioninformation.md) 無法使用，因為它所指向的資訊通常是在堆疊上，而且當控制項傳送至例外狀況處理常式時終結。 不過，應用程式可以將資訊複製到安全的儲存體，以供例外狀況處理常式使用。

篩選函式的優點是它可以處理例外狀況，並傳回值，讓系統從發生例外狀況的位置繼續執行。 相反地，使用例外狀況處理常式區塊時，執行會依序從例外狀況處理常式繼續執行，而不是從例外狀況的點繼續。

處理例外狀況可能很簡單，像是注意錯誤，並設定稍後將檢查的旗標、列印警告或錯誤訊息，或採取其他限制動作。 如果可以繼續執行，則可能也需要藉由修改內容記錄來變更電腦狀態。 如需處理分頁錯誤例外狀況的篩選函式範例，請參閱 [使用虛擬記憶體函數](../memory/using-the-memory-management-functions.md)。

[**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)函數可以當做篩選運算式中的篩選函數使用。 \_ \_ 除非正在調試進程，否則會傳回例外狀況執行處理常式，在此情況下，會傳回例外狀況 \_ 繼續 \_ 搜尋。

 

 
