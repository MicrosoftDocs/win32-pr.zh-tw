---
description: 管道伺服器會在 CreateNamedPipe 函數的 dwPipeMode 參數中指定管道類型模式、讀取模式和等候模式。 管道用戶端可以使用 CreateFile 函式，為管道控制碼指定這些管線模式。
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: 具名管道類型、讀取和等候模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b8ba69ef0d795747070072511c84abf5a3950db3b9c03ec18973f4d29bbd51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014888"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>具名管道類型、讀取和等候模式

管道伺服器會在 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)函數的 *dwPipeMode* 參數中指定管道類型模式、讀取模式和等候模式。 管道用戶端可以使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式，為管道控制碼指定這些管線模式。

## <a name="type-mode"></a>類型模式

管道的類型模式會決定資料如何寫入具名管道。 您可以透過具名管道將資料傳輸為位元組資料流程或訊息串流。 當呼叫 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) 來建立具名管道的實例時，管道伺服器會指定管道類型。 管道的所有實例都必須使用相同的類型模式。

若要建立位元組類型管道，請指定管道 \_ 類型 \_ byte 或使用預設值。 資料會以位元組資料流程的形式寫入管道，而系統不會區分以不同寫入作業寫入的位元組。

若要建立訊息類型管道，請指定管道 \_ 類型 \_ 訊息。 系統會將每個寫入作業中寫入的位元組視為訊息單位來處理管道。 系統一律會對訊息類型管道執行寫入作業，如同啟用寫入模式一樣。

## <a name="read-mode"></a>讀取模式

管道的讀取模式會決定如何從具名管道讀取資料。 當呼叫 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)時，管道伺服器會指定管道控制碼的初始讀取模式。 您可以在位元組讀取模式或訊息讀取模式中讀取資料。 Byte 類型管道的控制碼只能在位元組讀取模式中。 訊息類型管道的控制碼可以是位元組讀取或訊息讀取模式。 針對訊息類型管道，伺服器和用戶端控制碼對相同管道實例的讀取模式可能會不同。

若要在位元組讀取模式中建立管道控制碼，請指定管道 \_ READMODE \_ 位元組或使用預設值。 資料會從管道讀取為位元組資料流程。 當讀取管道中的所有可用位元組，或讀取指定的位元組數目時，就會順利完成讀取作業。

若要在訊息讀取模式中建立管道控制碼，請指定管道 \_ READMODE \_ 訊息。 資料會從管道讀取為訊息的資料流程。 只有在讀取整個訊息時，才會成功完成讀取作業。 如果要讀取的指定位元組數目小於下一個訊息的大小，則函式會在傳回零 (前盡可能讀取最多的訊息，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數會傳回錯誤的 \_ \_ 資料) 。 您可以使用另一個讀取操作來讀取訊息的其餘部分。

若為管道用戶端， [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 所傳回的管道控制碼一開始一律為位元組讀取模式。 管道用戶端和管道伺服器都可以使用 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) 函式來變更管道控制碼的讀取模式。 管道控制碼必須有 [檔案 \_ 寫入 \_ 屬性] 存取權限。

## <a name="wait-mode"></a>等候模式

管道控制碼的等候模式會決定 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)和 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 函數如何處理冗長的作業。 在封鎖等候模式中，函式會無限期等待管道另一端的進程完成作業。 在非封鎖等候模式中，函式會在其他需要無限等待的情況下立即傳回。

當管道為空白時， [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 作業會受到管道控制碼的等候模式影響。 在封鎖等候控制碼的情況下，除非有資料可從寫入管道另一端的執行緒取得，否則作業不會順利完成。 使用非封鎖等候控制碼時，函式會立即傳回零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回錯誤的 \_ \_ 資料。

當管道的緩衝區中沒有足夠的空間時， [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 作業會受到管道控制碼的等候模式影響。 在封鎖等候控制碼的情況下，寫入作業在緩衝區中建立足夠的空間之後，就不會成功，因為執行緒是從管道的另一端讀取。 使用非封鎖等候控制碼時，寫入作業會立即傳回非零值，而不會寫入任何 (任何位元組的訊息類型管道) 或寫入緩衝區保留字節類型管線)  (的位元組數。

當沒有用戶端連接或等候連接到管道實例時， [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 作業會受到管道控制碼的等候模式影響。 使用封鎖等候控制碼時，連接作業不會成功，直到管道用戶端藉由呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函式連接到管道實例為止。 使用非封鎖等候控制碼時，連接作業會立即傳回零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回錯誤 \_ 管道 \_ 接聽。

依預設， [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) 或 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式所傳回的所有具名管道控制碼，都會在啟用封鎖等候模式的情況下建立。 若要以非封鎖等候模式建立管道，管道伺服器會在 \_ 呼叫 **CreateNamedPipe** 時指定管道 NOWAIT。

管道用戶端和管道伺服器都可以藉由 \_ \_ 在 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) 函數的呼叫中指定管道等候或管道 NOWAIT，來變更管道控制碼的等候模式。

> [!Note]  
> 支援非封鎖式等候模式，以支援與 Microsoft LAN Manager 版本2.0 的相容性。 此模式不能用來達到與具名管道 (i/o) 的重迭輸入和輸出。 應該改為使用重迭的 i/o，因為它可讓耗時的作業在函式傳回之後于背景中執行。 如需重迭 i/o 的詳細資訊，請參閱 [同步和重迭的輸入和輸出](synchronous-and-overlapped-input-and-output.md)。

 

 

 
