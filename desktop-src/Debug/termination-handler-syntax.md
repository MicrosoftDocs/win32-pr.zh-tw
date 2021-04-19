---
description: '\_ \_ Try 和 \_ \_ finally 關鍵字是用來建立終止處理常式。 下列範例顯示終止處理常式的結構。'
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Termination-Handler 語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967048"
---
# <a name="termination-handler-syntax"></a>Termination-Handler 語法

**\_ \_ Try** 和 **\_ \_ finally** 關鍵字是用來建立終止處理常式。 下列範例顯示終止處理常式的結構。


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



如需範例，請參閱 [使用終止處理常式](using-a-termination-handler.md)。

如同例外狀況處理常式一樣， **\_ \_ try** 區塊和 **\_ \_ finally** 區塊都需要大括弧 ({}) ，而且不允許使用 **goto** 語句跳到任一個區塊。

**\_ \_ Try** 區塊包含受終止處理常式保護的程式碼受防護主體。 函數可以有任意數目的終止處理常式，而這些終止處理區塊可以嵌套在相同函式或不同函式中。

當控制權的流程離開 **\_ \_ try** 區塊時，就會執行 **\_ \_ finally** 區塊。 但是，如果您在 **\_ \_ try** 區塊內呼叫下列任何函式，則不會執行 **\_ \_ finally** 區塊： [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)、 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)或 **abort**。

**\_ \_ Finally** 區塊會在終止處理常式所在的函數內容中執行。 這表示 **\_ \_ finally** 區塊可以存取該函數的區域變數。 **\_ \_ Finally** 區塊的執行可透過下列任何方式來終止。

-   執行區塊中的最後一個語句，並接續至下一個指令
-   使用 control 語句 (**return**、 **break**、 **continue** 或 **goto**) 
-   使用 **longjmp** 或跳到例外狀況處理常式

如果因為叫用以框架為基礎之例外狀況處理常式之例外狀況處理區塊的例外狀況而終止 **\_ \_ try** 區塊的執行，則會在執行例外狀況處理區塊之前執行 **\_ \_ finally** 區塊。 同樣地，從 **\_ \_ try** 區塊呼叫 **longjmp** C 執行時間程式庫函式會造成 **\_ \_ finally** 區塊執行，然後繼續執行 **longjmp** 作業的目標。 如果 **\_ \_ try** 區塊執行由於 control 語句 (**return**、 **break**、 **continue** 或 **goto**) 而終止，則會執行 **\_ \_ finally** 區塊。

[**AbnormalTermination**](abnormaltermination.md)函式可以在 **\_ \_ finally** 區塊中使用，以判斷 **\_ \_ try** 區塊是否順序終止，也就是是否到達右大括弧 (} ) 。 由於呼叫 **longjmp**、跳到例外狀況處理常式，或 **傳回、****中斷**、**繼續** 或 **goto** 語句，因此離開 **\_ \_ try** 區塊會被視為異常終止。 請注意，順序結束失敗會導致系統以反向順序搜尋所有堆疊框架，以判斷是否必須呼叫任何終止處理常式。 這可能會導致效能降低，因為執行數百個指令。

為了避免終止處理常式異常終止，執行應該會繼續到區塊結尾。 您也可以執行 **\_ \_ leave** 語句。 **\_ \_ Leave** 語句允許立即終止 **\_ \_ try** 區塊，而不會造成異常終止和其效能負面影響。 請檢查您的編譯器檔，以判斷是否支援 **\_ \_ leave** 語句。

如果 **\_ \_ finally** 區塊的執行因為 **return** control 語句而終止，它相當於封閉函數中右大括弧的 **goto** 。 因此，封入函數將會傳回。

 

 
