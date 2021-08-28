---
description: 有兩種類型的輸入/輸出 (i/o) 同步處理：同步 i/o 和非同步 i/o。 非同步 i/o 也稱為重迭 i/o。
ms.assetid: ade51d98-cc9d-4b33-9c52-559a9cb14707
title: 同步和非同步 i/o
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 99ab06fac66c0ff3033407326c190ce0d08e643ca30b24ff17b7420e61782222
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981820"
---
# <a name="synchronous-and-asynchronous-io"></a>同步和非同步 i/o

另請參閱 [i/o 相關的範例應用程式](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io)。

有兩種類型的輸入/輸出 (i/o) 同步處理：同步 i/o 和非同步 i/o。 非同步 i/o 也稱為重迭 i/o。

在 *同步檔案 i/o* 中，執行緒會啟動 i/o 作業，並立即進入等候狀態，直到 i/o 要求完成為止。 執行非同步檔案 *i/o* 的執行緒會呼叫適當的函式，將 i/o 要求傳送到核心。 如果核心接受要求，呼叫執行緒會繼續處理另一個工作，直到核心向執行緒發出 i/o 作業完成為止。 然後，它會中斷其目前的工作，並視需要處理 i/o 作業的資料。

下圖說明這兩種同步處理類型。

![同步和非同步 i/o](images/fig2bedit.png)

在預期 i/o 要求需要花費大量時間的情況下，例如重新整理或備份大型資料庫或慢速的通訊連結時，非同步 i/o 通常是將處理效率優化的好方法。 不過，對於相對快速的 i/o 作業，處理核心 i/o 要求和核心信號的額外負荷，可能會使非同步 i/o 變得更小，特別是當需要進行許多快速的 i/o 作業時。 在此情況下，同步 i/o 會更好。 如何完成這些工作的機制和實行詳細資料，會根據所使用的裝置控制碼類型以及應用程式的特定需求而異。 換句話說，通常有多種方法可解決此問題。

## <a name="synchronous-and-asynchronous-io-considerations"></a>同步和非同步 i/o 考慮

如果為同步 i/o 開啟檔案或裝置 (也就是未指定檔案 **\_ \_ 旗** 標重迭) ，後續對函式的呼叫（例如 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ）可以封鎖呼叫執行緒的執行，直到發生下列其中一個事件為止：

-   在此範例中，i/o 作業 (完成，資料寫入) 。
-   發生 I/O 錯誤。  (例如，管線已從另一端關閉。 ) 
-   呼叫本身發生錯誤 (例如，一或多個參數) 無效。
-   進程中的另一個執行緒會使用封鎖執行緒的執行緒控制碼來呼叫 [**CancelSynchronousIo**](cancelsynchronousio-func.md) 函式，而此控制碼會終止該執行緒的 i/o 作業，而導致 i/o 作業失敗。
-   封鎖的執行緒由系統終止;例如，進程本身已終止，或另一個執行緒使用封鎖執行緒的控制碼呼叫 [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) 函式。  (這通常視為最後手段，而不是良好的應用程式設計。 ) 

在某些情況下，應用程式的設計和用途可能無法接受此延遲，因此應用程式設計人員應該考慮使用非同步 i/o 搭配適當的執行緒同步處理物件（例如 [i/o 完成埠](i-o-completion-ports.md)）。 如需有關執行緒同步處理的詳細資訊，請參閱 [關於同步](/windows/desktop/Sync/about-synchronization)處理。

進程會在 *dwFlagsAndAttributes* 參數中指定檔案 **旗標重 \_ \_** 迭旗標，以在呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)時開啟非同步 i/o 的檔案。 如果未指定檔案旗標重迭，則會開啟檔案以進行同步 i/o。 **\_ \_** 開啟非同步 i/o 的檔案時，會將重 [**迭結構的**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) 指標傳遞至 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)的呼叫。 執行同步 i/o 時，呼叫 **ReadFile** 和 **WriteFile** 不需要此結構。

> [!Note]  
> 如果檔案或裝置開啟為非同步 i/o，則使用該控制碼的函式（例如 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ）的後續呼叫通常會立即傳回，但可能也會以同步方式與封鎖的執行相關。 如需詳細資訊，請參閱 [https://support.microsoft.com/kb/156932](https://support.microsoft.com/kb/156932)。

 

雖然 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 是最常用來開啟檔案、磁片區、匿名管道和其他類似裝置的函式，但 i/o 作業也可以使用從其他系統物件 *轉換* 的控制碼來執行， [**例如通訊端**](/windows/desktop/api/winsock2/nf-winsock2-socket) 所建立的通訊端或 [**接受**](/windows/desktop/api/winsock2/nf-winsock2-accept) 函數。

藉由呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數與檔案 **旗標 \_ \_ 備份 \_ 語義** 屬性，即可取得目錄物件的控制碼。 目錄控制碼幾乎不會用到，備份應用程式是通常會使用這些應用程式的幾個應用程式之一。

開啟非同步 i/o 的檔案物件之後，必須正確地建立及初始化重迭 [**的結構，**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 並將其傳遞至每個函式的呼叫，例如 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)。 在非同步讀取和寫入作業中使用重迭 [**的結構時，請**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) 記住下列事項：

-   在檔案物件的所有非同步 i/o 作業都完成之前，請勿解除配置或修改重 [**迭結構或**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 資料緩衝區。
-   如果 [**您將重迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標宣告為區域變數，請勿在檔案物件的所有非同步 i/o 作業都完成之前結束區域函數。 如果區域函式提前結束，則重迭 **的結構將** 會超出範圍，且在該函式之外遇到的任何 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) 或 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) 函數將無法存取它。

您也可以建立事件，並將控制碼放在重迭 [**的結構中**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ; [等候](/windows/desktop/Sync/wait-functions) 函式可用來等候 i/o 作業完成，方法是等候事件控制碼。

如先前所述，當使用非同步控制碼時，應用程式應該在決定何時釋放與該控制碼上指定之 i/o 作業相關聯的資源時，請小心。 如果將控制碼提前解除配置， [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) 或 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) 可能會不正確地報告 i/o 作業是否已完成。 此外， **WriteFile** 函式有時會傳回 **TRUE** ，並將 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 值設為 [ **錯誤 \_ 成功**]，即使它使用非同步控制碼 (也可以傳回 **FALSE** ，並將 **錯誤 \_ IO \_ 擱置**) 。 習慣同步 i/o 設計的程式設計師通常會釋出資料緩衝區資源，原因是 **TRUE** 和 **錯誤 \_ 成功** 表示作業已完成。 但是，如果 [i/o 完成埠](i-o-completion-ports.md) 與這個非同步控制碼搭配使用，即使 i/o 作業立即完成，也會傳送完成封包。 換言之，如果應用程式在 **WriteFile** 傳回 **TRUE** 之後，除了 i/o 完成埠常式中的 **錯誤 \_ 成功** ，也會有雙精度的錯誤狀況。 在此範例中，建議是讓完成埠常式完全負責這類資源的所有釋放作業。

系統不會在支援檔案指標的檔案和裝置的非同步控制碼上維護檔案指標 (也就是說，搜尋裝置) ，因此檔案位置必須傳遞至重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 相關位移資料成員中的讀取和寫入功能。 如需詳細資訊，請參閱 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) 和 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)。

當讀取或寫入資料時，系統會維護同步控制碼的檔案指標位置，也可以使用 [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) 或 [**SetFilePointerEx**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointerex) 函數來更新。

應用程式也可以等候檔案控制代碼來同步處理完成 i/o 作業，但這麼做需要非常小心。 每次啟動 i/o 作業時，作業系統會將檔案控制代碼設定為未收到信號狀態。 每次完成 i/o 作業時，作業系統會將檔案控制代碼設定為已發出信號的狀態。 因此，如果應用程式啟動兩個 i/o 作業，並等候檔案控制代碼，就無法在控制碼設為已發出信號的狀態時，判斷哪一項作業已完成。 如果應用程式必須在單一檔案上執行多個非同步 i/o 作業，則應該等候每個 i/o 作業 [**之特定重**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 迭結構中的事件控制碼，而不是在一般檔案控制代碼上。

若要取消所有暫止的非同步 i/o 作業，請使用下列其中一項：

-   [**CancelIo**](cancelio.md)：此函式只會取消呼叫執行緒針對指定檔案控制代碼發出的作業。
-   [**CancelIoEx**](cancelioex-func.md)：此函式會取消執行緒針對指定的檔案控制代碼所發出的所有作業。

使用 [**CancelSynchronousIo**](cancelsynchronousio-func.md) 來取消暫止的同步 i/o 作業。

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)和 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)函式可讓應用程式指定要執行的常式 (請在完成非同步 I/o 要求時參閱 [**FileIOCompletionRoutine**](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)) 。

 

 
