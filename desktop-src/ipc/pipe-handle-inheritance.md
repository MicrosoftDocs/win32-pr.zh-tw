---
description: 管道伺服器控制是否可透過下列方式繼承其控制碼。
ms.assetid: 72302f8b-f3a2-4efc-aab1-e596b8323984
title: 管道控制碼繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cf91d4393b43011a2df632806f96da1e713b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689512"
---
# <a name="pipe-handle-inheritance"></a>管道控制碼繼承

管道伺服器控制是否可透過下列方式繼承其控制碼：

-   [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)函式會接收 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構。 如果管道伺服器將此結構的 **bInheritHandle** 成員設為 **TRUE**，則可以繼承 **CreatePipe** 所建立的控制碼。
-   管道伺服器可以使用 [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) 函數來變更管道控制碼的繼承。 管道伺服器可以建立可繼承管道控制碼的基類重複，或可繼承的基類管道控制碼重複。
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)函數可讓管道伺服器指定子進程是否全部繼承或全部都不繼承它的可繼承控制碼。

當子進程繼承管道控制碼時，系統會讓進程存取管道。 不過，父進程必須將控制碼值傳達給子進程。 父進程通常會將標準輸出控制碼重新導向至子進程，如下列步驟所示：

1.  呼叫 [**GetStdHandle**](/windows/console/getstdhandle) 函數，以取得目前的標準輸出控制碼;儲存此控制碼，讓您可以在建立子進程之後還原原始的標準輸出控制碼。
2.  呼叫 [**SetStdHandle**](/windows/console/setstdhandle) 函數，將標準輸出控制碼設定為管道的寫入控制碼。 現在父進程可以建立子進程。
3.  呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函數，以關閉管道的寫入控制碼。 在子進程繼承寫入控制碼之後，父進程就不再需要它的複本。
4.  呼叫 [**SetStdHandle**](/windows/console/setstdhandle) 來還原原始標準輸出控制碼。

子進程會使用 [**GetStdHandle**](/windows/console/getstdhandle) 函式來取得其標準輸出控制碼，現在是管道的寫入結束控制碼。 子進程接著會使用 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 函式，將其輸出傳送至管道。 當子系使用管道完成時，它應該藉由呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 或終止來關閉管道控制碼，這會自動關閉控制碼。

父進程會使用 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 函式來接收來自管道的輸入。 資料會以位元組資料流程的形式寫入至匿名管道。 這表示，從管道讀取的父進程無法區分以個別寫入作業撰寫的位元組，除非父進程和子進程都使用通訊協定來指出寫入作業結束的位置。 當管道的所有寫入控制碼都關閉時， **ReadFile** 函數會傳回零。 在呼叫 **ReadFile** 之前，父進程必須關閉管道寫入端的控制碼。 如果沒有這樣做， **ReadFile** 作業就無法傳回零，因為父進程具有管道寫入結尾的開啟控制碼。

重新導向標準輸入控制碼的程式，與重新導向標準輸出控制碼的程式類似，不同之處在于管道的讀取控制碼是用來做為子系的標準輸入控制碼。 在此情況下，父進程必須確保子進程不會繼承管道的寫入控制碼。 如果沒有這麼做，子進程所執行的 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 作業就無法傳回零，因為子進程具有管道寫入結束的控制碼。

如需使用匿名管道來重新導向子進程之標準控制碼的範例程式，請參閱 [使用重新導向的輸入和輸出建立子進程](/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output)。

 

 
