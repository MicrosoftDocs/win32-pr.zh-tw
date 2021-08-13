---
description: 例外狀況可由硬體或軟體起始，並可在核心模式和使用者模式程式碼中進行。 結構化例外狀況處理提供單一機制來處理核心模式和使用者模式例外狀況。
ms.assetid: 760ddcaa-a18c-4fdf-836c-9028a2e4b62e
title: '例外狀況處理 (錯誤處理) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253776619100095ae1ba9c92fa2caa373bc950bdf6725c6ef5d0239520320bd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260868"
---
# <a name="exception-handling-error-handling"></a>例外狀況處理 (錯誤處理) 

例外狀況可由硬體或軟體起始，並可在核心模式和使用者模式程式碼中進行。 結構化例外狀況處理提供單一機制來處理核心模式和使用者模式例外狀況。

執行特定的指令序列可能會導致硬體所起始的例外狀況。 例如，當進程嘗試讀取或寫入沒有適當存取權的虛擬位址時，硬體就會產生存取違規。

需要例外狀況處理的事件也可能會在執行軟體常式期間發生 (例如，) 指定不正確參數值時。 發生這種情況時，執行緒可以藉由呼叫 [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) 函式來明確起始例外狀況。 此函數可讓呼叫執行緒指定描述例外狀況的資訊。

例外狀況可以是持續性或 noncontinuable。 當事件不在硬體中，或如果接續沒有意義時，就會發生 noncontinuable 例外狀況。 Noncontinuable 例外狀況不會終止應用程式。 因此，應用程式可能可以攔截例外狀況並執行。 不過，noncontinuable 例外狀況通常是因為堆疊損毀或其他嚴重問題而產生，因此難以從例外狀況中復原。

 

 
