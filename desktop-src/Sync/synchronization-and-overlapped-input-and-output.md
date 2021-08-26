---
description: 您可以在檔案、具名管道和序列通訊裝置上執行同步或非同步 (也稱為重迭) i/o 作業。
ms.assetid: db44990e-5a0f-4153-8ff6-79dd7cda48af
title: 同步處理和重迭的輸入和輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e462e4c2cffa3f1c9dee9bc33a7c75b910ce8139dbdfab9c190b4691c4b6bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975908"
---
# <a name="synchronization-and-overlapped-input-and-output"></a>同步處理和重迭的輸入和輸出

您可以在檔案、具名管道和序列通訊裝置上執行同步或非同步 (也稱為重迭) i/o 作業。 [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile)、 [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile)、 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)、 [**WaitCommEvent**](/windows/win32/api/winbase/nf-winbase-waitcommevent)、 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)和 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)函數可以同步或非同步方式執行。 [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)和 [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex)函數只能以非同步方式執行。

以同步方式執行函式時，會等到作業完成時才會傳回。 這表示，呼叫執行緒的執行可能會在等候耗時的作業完成時，封鎖無限期的執行時間。 針對重迭作業呼叫的函式可能會立即傳回，即使作業尚未完成也一樣。 這可讓您在背景執行耗時的 i/o 作業，而呼叫執行緒可以自由執行其他工作。 例如，單一執行緒可以在不同的控制碼上執行同時的 i/o 作業，或在相同的控制碼上執行同時的讀取和寫入作業。

為了在完成重迭的作業時同步處理其執行，呼叫執行緒會使用 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) 函式、 [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) 函式或其中一個 [等候](wait-functions.md) 函式來判斷已完成重迭作業的時間。 您也可以使用 [**HasOverlappedIoCompleted**](/windows/desktop/api/WinBase/nf-winbase-hasoverlappediocompleted) 宏來輪詢是否完成。

若要取消所有暫止的非同步 i/o 作業，請使用 [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) 函數，並 [**提供可指定**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 要取消之要求的重迭結構。 您可以使用 [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio) 函式來取消呼叫執行緒針對指定檔案控制代碼發出的暫止非同步 i/o 作業。

重迭作業需要使用檔案旗標重迭旗標建立的檔案、命名 **管道 \_ \_** 或通訊裝置。 當執行緒呼叫函式 (例如 [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) 函式) 來執行重迭的作業時，呼叫的執行緒必須指定重 [**迭結構的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指標。  (如果此指標為 **Null**，則函式傳回值可能會不正確地表示作業已完成。 ) 重 **迭結構的** 所有成員都必須初始化為零，除非事件將用來指示 i/o 作業的完成。 如果使用事件，重 **迭結構的** **hEvent** 成員會指定已配置事件物件的控制碼。 系統會在作業完成之前，將事件物件的狀態設定為未收到信號，以進行 i/o 函數的呼叫。 當作業完成時，系統會將事件物件的狀態設定為收到信號。 只有在同時有一個以上的未處理 i/o 作業時，才需要事件。 如果未使用事件，每個完成的 i/o 作業都會表示檔案、具名管道或通訊裝置。

當呼叫函式來執行重迭的作業時，作業可能會在函數傳回之前完成。 發生這種情況時，會以同步方式執行作業的方式來處理結果。 但是，如果作業未完成，則函式的傳回值為 **FALSE**，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回 **錯誤 \_ IO \_ 暫** 止。

執行緒可以透過下列兩種方法之一來管理重迭的作業：

-   使用 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) 或 [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) 函式來等候重迭的作業完成。 如果使用 **GetOverlappedResultEx** ，呼叫執行緒可以指定重迭作業的超時，或執行可提供警示等候。
-   在其中一個 [等候](wait-functions.md)函式中，指定重設成重 [**設的事件**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)物件的控制碼，然後在 wait 函數傳回之後，呼叫 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)或 [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)。 此函式會傳回已完成重迭作業的結果，以及適合這類資訊的函式，它會報告已傳送的實際位元組數目。

在單一執行緒上執行多個同時重迭的作業時，呼叫的執行緒 [**必須為每**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 個作業指定一個重迭的結構。 每個重迭的 **結構都必須** 指定不同的手動重設事件物件的控制碼。 為了等候任何一個重迭的作業完成，執行緒會將所有手動重設的事件控制碼指定為其中一個多物件 [等候](wait-functions.md)函式中的等候準則。 多物件等候函式的傳回值會指出已發出的手動重設事件物件已收到信號，所以執行緒可以判斷哪一個重迭作業導致等候作業完成。

您可以更安全地針對每個重迭的作業使用個別的事件物件，而不是指定事件物件，或針對多個作業重複使用相同的事件物件。 如果 [**未在重迭的結構中**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指定事件物件，系統會在重迭的作業完成時，表示檔案、具名管道或通訊裝置的狀態。 因此，您可以將這些控制碼指定為 wait 函式中的同步處理物件，雖然它們的用途可能很難管理，因為當在相同的檔案、具名管道或通訊裝置上執行同時重迭的作業時，並沒有辦法知道哪些作業導致物件的狀態被告知。

執行緒不應該重複使用事件，因為假設事件只會由該執行緒的重迭運算發出信號。 事件會在與正在完成的重迭作業相同的執行緒上收到信號。 在多個執行緒上使用相同的事件可能會導致競爭情形，在此情況中，其作業會針對使用該事件的其他執行緒先和提前完成的執行緒正確地發出信號。 然後，當下一個重迭的作業完成時，所有使用該事件的執行緒都會再次收到事件的信號，依此類推，直到所有重迭的作業完成為止。

如需說明如何使用重迭作業、完成常式和 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數的範例，請參閱 [使用管道](../ipc/using-pipes.md)。

* * Windows Vista、Windows Server 2003 和 Windows XP： * *

[**重複使用**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)重迭的結構時，請務必小心。 如果 **在** 多個執行緒上重複使用重迭結構，而且 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) 是在 *bWait* 參數設定為 **TRUE** 的情況下呼叫，則呼叫執行緒必須確定相關聯的事件會在重複使用結構之前收到信號。 在呼叫 **GetOverlappedResult** 之後，您可以使用 [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject)函式來強制執行緒等候，直到作業完成為止。 請注意，事件物件必須是手動重設事件物件。 如果使用 autoreset 事件物件，則呼叫 **GetOverlappedResult** 並將 *bWait* 參數設為 **TRUE** ，會導致函式無限期地封鎖。 從 Windows 7 和 Windows Server 2008 R2 開始，此行為已變更，因為應用程式會在應用程式資訊清單中指定 Windows 7 做為支援的作業系統。 如需詳細資訊，請參閱 [應用程式資訊清單](/previous-versions/windows/desktop/adrms_sdk/application-manifests)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[I/o 概念](../fileio/i-o-concepts.md)
</dt> </dl>

 

 
