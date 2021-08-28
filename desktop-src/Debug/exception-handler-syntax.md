---
description: '\_ \_ Try 和 \_ \_ except 關鍵字是用來建立以框架為基礎的例外狀況處理常式。 下列範例會顯示例外狀況處理常式的結構。'
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Exception-Handler 語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd24b3ffc84a3469c7c8d97ce505a0292ee538ea8f0b9c1d604bf34f65203ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912738"
---
# <a name="exception-handler-syntax"></a>Exception-Handler 語法

**\_ \_ Try** 和 **\_ \_ except** 關鍵字是用來建立以框架為基礎的例外狀況處理常式。 下列範例會顯示例外狀況處理常式的結構。


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



請注意， **\_ \_ try** 區塊和例外狀況處理常式區塊需要大括弧 ({}) 。 不允許使用 **goto** 語句跳到 **\_ \_ try** 區塊的主體或進入例外狀況處理常式區塊。 這項規則適用于例外狀況處理常式和終止處理常式。

**\_ \_ Try** 區塊包含例外狀況處理常式保護的程式碼受防護主體。 函式可以有任意數目的例外狀況處理常式，而且這些例外狀況處理語句可以嵌套在相同函式或不同函式中。 如果 **\_ \_ try** 區塊中發生例外狀況，系統會接受控制權，並開始搜尋例外狀況處理常式。 如需此搜尋的詳細說明，請參閱 [例外狀況處理](exception-handling.md)。

例外狀況處理常式只接收在單一執行緒內發生的例外狀況。 這表示，如果 **\_ \_ try** 區塊包含 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)或 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)函式的呼叫，則在新的進程或執行緒內發生的例外狀況不會分派至此處理程式。

系統會評估每個例外狀況處理常式的篩選運算式，以防止發生例外狀況的程式碼，直到處理例外狀況或不再有處理常式為止。 篩選運算式必須評估為下列三個值的其中一個。



| 值                              | 意義                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **例外狀況 \_ 執行 \_ 處理常式**    | 系統會將控制項傳送至例外狀況處理常式，然後在找到處理程式的堆疊框架中繼續執行。                                                                                       |
| **例外狀況 \_ 繼續 \_ 搜尋**    | 系統會繼續搜尋處理常式。                                                                                                                                                                          |
| **例外狀況 \_ 繼續 \_ 執行** | 系統會停止其搜尋處理常式，並將控制權傳回給發生例外狀況的時間點。 如果例外狀況是 noncontinuable，這會導致 **例外狀況 \_ noncontinuable \_ 例外** 狀況例外狀況。 |



 

篩選運算式會在例外狀況處理常式所在的函式內容中進行評估，即使例外狀況可能發生在不同的函式中也一樣。 這表示篩選運算式可以存取函式的本機變數。 同樣地，例外狀況處理常式區塊可以存取它所在之函式的本機變數。

如需更多範例，請參閱 [使用例外狀況處理常式](using-an-exception-handler.md)。

如需篩選運算式和篩選函數的詳細資訊，請參閱以 [框架為基礎的例外狀況處理](frame-based-exception-handling.md)。

 

 
