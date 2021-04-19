---
description: 同步管道 i/o 和非同步管道 i/o。 ReadFile、WriteFile、TransactNamedPipe 和 ConnectNamedPipe 函數可以同步或非同步方式，在管道上執行輸入和輸出作業。
ms.assetid: 5ab9bb7f-1f99-4041-bba8-2863f34dbcaf
title: 同步和重迭的管道 i/o
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3becfb19dfe5fa49d4121246a576fb3200226b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988435"
---
# <a name="synchronous-and-overlapped-pipe-io"></a>同步和重迭的管道 i/o

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)、 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)和 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)函數可以同步或非同步方式，在管道上執行輸入和輸出作業。 當函式以同步方式執行時，它會等到執行的作業完成後才會傳回。 這表示，呼叫執行緒的執行可能會在等候需要花費很多時間的作業完成時，封鎖無限期。 當函式以非同步方式執行時，它會立即傳回，即使操作尚未完成。 這可讓您在背景執行耗時的作業，而呼叫執行緒可以自由執行其他工作。

使用非同步 i/o 可讓管道伺服器使用迴圈來執行下列步驟：

1.  在等候函式的呼叫中指定多個事件物件，並等候其中一個物件設定為已發出信號的狀態。
2.  使用 wait 函式的傳回值來判斷已完成的重迭運算。
3.  執行清除已完成的作業所需的工作，並起始該管道控制碼的下一次操作。 這可能牽涉到針對相同的管道控制碼啟動另一個重迭的作業。

重迭的作業可讓一個管道同時讀取和寫入資料，以及針對單一線程，在多個管道控制碼上執行同時的 i/o 作業。 這可讓單一執行緒的管道伺服器有效率地處理與多個管道用戶端之間的通訊。 如需範例，請參閱使用重迭 [i/o 的具名管道伺服器](named-pipe-server-using-overlapped-i-o.md)。

若要讓管道伺服器使用同步作業來與多個用戶端通訊，它必須為每個管道用戶端建立個別的執行緒，讓一個或多個執行緒可以在其他執行緒等候時執行。 如需使用同步作業之多執行緒管道伺服器的範例，請參閱 [多執行緒管道伺服器](multithreaded-pipe-server.md)。

## <a name="enabling-asynchronous-operation"></a>啟用非同步作業

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)、 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)和 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)函式只有在您針對指定的管道控制碼啟用重迭模式，並 [**指定對重迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)有效指標時，才能以非同步方式執行。 如果重 **迭指標** 為 **Null**，則函式傳回值可能會不正確地表示作業已完成。 因此，強烈建議您如果建立的控制碼的檔案旗標 \_ \_ 重迭，而且想要使用非同步行為，您應該一律指定有效的重迭結構。

[**指定之**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構的 **hEvent** 成員必須包含手動重設事件物件的控制碼。 這是 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) 函數所建立的同步處理物件。 起始重迭作業的執行緒會使用事件物件來判斷作業何時完成。 當您在相同的控制碼上執行並行作業時，不應該使用管道控制碼進行同步處理，因為沒有辦法知道哪一項作業的完成會導致管道控制碼收到信號。 在相同管道控制碼上執行同時作業的唯一可靠方法，是針對每個作業 **使用個別的** 重迭結構及其本身的事件物件。 如需事件物件的詳細資訊，請參閱 [同步](/windows/desktop/Sync/synchronization)處理。

此外，當重迭的作業完成時，您也可以使用 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 或 [**GetQueuedCompletionStatusEx**](/windows/desktop/FileIO/getqueuedcompletionstatusex-func) 函數來通知您。 在此情況下，您不 [**需要在重迭的結構中**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指派手動重設事件，並且會以非同步讀取或寫入作業的相同方式，對管道控制碼執行完成。 如需詳細資訊，請參閱 [I/o 完成埠](/windows/desktop/FileIO/i-o-completion-ports)。

當 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)、 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)和 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 作業以非同步方式執行時，會發生下列其中一種情況：

-   如果函式傳回時作業已完成，則傳回值會指出作業成功或失敗。 如果發生錯誤，則傳回值為零，而且 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回錯誤 IO 擱置以外的值 \_ \_ 。
-   如果函式傳回時作業未完成，則傳回值為零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤 \_ IO \_ 暫止。 在此情況下，呼叫執行緒必須等候作業完成。 接著，呼叫的執行緒必須呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來判斷結果。

## <a name="using-completion-routines"></a>使用完成常式

[**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)和 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)函數提供另一種形式的重迭 i/o。 不同于重迭的 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 函式（使用事件物件來表示完成），擴充函數會指定 *完成常式*。 完成常式是在讀取或寫入作業完成時，已排入佇列以便執行的函式。 在呼叫 **ReadFileEx** 和 **WriteFileEx** 的執行緒啟動 *可提供警示等候* 作業之前，不會執行完成常式，方法是呼叫其中一個 [可提供警示 wait 函數](/windows/desktop/Sync/wait-functions) ，並將 *fAlertable* 參數設定為 **TRUE**。 在可提供警示等候作業中，函式也會在 **ReadFileEx** 或 **WriteFileEx** 完成常式排入佇列以供執行時傳回。 管道伺服器可以使用擴充的函式，對每個連接到它的用戶端執行一系列的讀取和寫入作業。 順序中的每個讀取或寫入作業都會指定一個完成常式，而每個完成常式都會起始順序中的下一個步驟。 如需範例，請參閱 [使用完成常式的具名管道伺服器](named-pipe-server-using-completion-routines.md)。

 

 
