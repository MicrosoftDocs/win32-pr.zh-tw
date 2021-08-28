---
description: 管道作業（包括管道用戶端和伺服器）可以呼叫數個函式的其中一個（除了 CallNamedPipe），以讀取和寫入具名管道。
ms.assetid: ae06455e-33bc-433d-be8f-aeb8eeb99b1d
title: 具名管道作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21bc389071a2861754b5d71659ec3cb836204c631a75de67565933f28e8632c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602149"
---
# <a name="named-pipe-operations"></a>具名管道作業

當管道伺服器第一次呼叫 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) 函式時，它會使用 *nMaxInstances* 參數來指定可同時存在之管道的實例數目上限。 只要不超過實例的數目上限，伺服器就可以重複呼叫 **CreateNamedPipe** 來建立管道的其他實例。 如果函式成功，每個呼叫都會將控制碼傳回給具名管道實例的伺服器端。

當管道伺服器建立管道實例時，管道用戶端就可以藉由呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函式來與其連接。 如果有可用的管道實例， **CreateFile** 會將控制碼傳回給管道實例的用戶端。 如果沒有可用的管道實例，管道用戶端可以使用 [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) 函式來等待管道變成可用。

管道伺服器可以藉由呼叫 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 函式來判斷管道用戶端連接到管道實例的時間。 如果管道控制碼處於封鎖等候模式，則在用戶端連接之前， **ConnectNamedPipe** 不會傳回。

管道用戶端和伺服器可以呼叫數個函式的其中一個（除了 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) ），以讀取和寫入具名管道。 這些函式的行為取決於管線的型別，以及指定管道控制碼的作用中模式，如下所示：

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)和 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)函數可以搭配 byte 類型或訊息類型的管道使用。
-   如果已針對重迭的作業開啟管道控制碼， [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) 和 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) 函數可以搭配 byte 類型或訊息類型管道使用。
-   [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)函式可以用來讀取，而不需移除位元組類型管道或訊息類型管道的內容。 **PeekNamedPipe** 也可以傳回管道實例的其他相關資訊。
-   如果呼叫進程的管道控制碼設定為訊息讀取模式，則 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) 函數可以搭配 message 類型的雙工管道使用。 此函式會寫入要求訊息，並在單一作業中讀取回復訊息，從而增強網路效能。

管道伺服器在管道用戶端啟動之前，不應執行封鎖讀取操作。 否則，可能會發生競爭情況。 這通常發生在初始化程式碼（例如 C 執行時間程式庫的程式碼）需要鎖定和檢查繼承的控制碼時。

當用戶端和伺服器使用管道實例完成時，伺服器應該先呼叫 [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) 函式，以確保用戶端會讀取寫入管道的所有位元組或訊息。 在用戶端從管道讀取所有資料之前， **FlushFileBuffers** 不會傳回。 然後伺服器會呼叫 [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe) 函式來關閉管道用戶端的連接。 此函式會讓用戶端的控制碼無效（如果尚未關閉）。 管線中任何未讀取的資料都會被捨棄。 用戶端中斷連線之後，伺服器會呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式來關閉其對管道實例的控制碼。 或者，伺服器可以使用 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) ，讓新的用戶端連接到此管道的實例。

進程可以藉由呼叫 [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo) 函式來取得具名管道的相關資訊，此函式會傳回管道的類型、輸入和輸出緩衝區的大小，以及可建立的管道實例數目上限。 [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)函式會報告管道控制碼的讀取和等候模式、目前的管道實例數目，以及透過網路通訊之管道的其他資訊。 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)函式會設定管道控制碼的讀取模式和等候模式。 針對與遠端伺服器通訊的管道用戶端，此函式也會控制要收集的最大位元組數目，或在傳送訊息之前等候的最長時間， (假設用戶端的控制碼未開啟且已啟用寫入模式的) 。

 

 
