---
description: Windows通訊端2引進重迭的 i/o，而且需要所有的傳輸提供者都支援這項功能。
ms.assetid: 90d49171-e211-4426-aa56-88aaeac7c578
title: 重迭的輸入/輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d260cccd13bfb8e872e0ac7346c112efff2f77cf115e3fe2f8dd3d3fb94deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641788"
---
# <a name="overlapped-inputoutput"></a>重迭的輸入/輸出

Windows通訊端2引進重迭的 i/o，而且需要所有的傳輸提供者都支援這項功能。 只有在使用 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)函式建立的通訊端上，會 \_ 設定 WSA 旗標重迭 \_ 旗標，並遵循 Windows 中建立的模型，才能執行重迭的 i/o。

若要接收，用戶端會使用 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) 或 [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) 來提供要接收資料的緩衝區。 如果有一或多個緩衝區在網路收到資料的時間之前張貼，則資料可能會在到達時立即將資料放入使用者的緩衝區，進而避免發生另一種情況的複製操作。 如果資料在接收緩衝區已張貼時抵達，則會立即複製到使用者的緩衝區。 當應用程式未張貼任何接收緩衝區時，如果資料到達，服務提供者會將內送資料在內部緩衝處理的同步處理樣式，直到用戶端發出接收呼叫，並藉此提供可複製資料的緩衝區為止。 如果應用程式使用 [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) 將接收緩衝區的大小設定為零，就會發生例外狀況。 在此情況下，可靠的通訊協定只允許在應用程式緩衝區張貼時接收資料，而不可靠的通訊協定上的資料將會遺失。

在傳送端，用戶端會使用 [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) 或 [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) 來提供已填滿緩衝區的指標，然後同意在網路耗用緩衝區的內容之前，不以任何方式干擾緩衝區。

重迭的傳送和接收呼叫會立即傳回。 傳回值為零表示 i/o 作業已立即完成，而且對應的完成指示已發生。 也就是說，關聯的事件物件已收到信號，或完成常式已透過 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)排入佇列。 通訊端錯誤的傳回值加上由 \_ WSA IO 暫止的錯誤碼， \_ 表示已成功起始重迭的作業 \_ ，而且當取用傳送緩衝區或填滿接收緩衝區時，會提供後續的指示。 任何其他錯誤碼都會指出重迭的作業未成功啟動，而且即將出現任何完成指示。

傳送和接收作業可以重迭。 接收函式可能會多次叫用以張貼接收緩衝區以準備傳入的資料，而且可以多次叫用傳送函式，以將傳送的多個緩衝區排入佇列。 請注意，雖然一連串重迭的傳送緩衝區會以提供的順序傳送，但對應的完成指示可能會以不同的順序進行。 同樣地，在接收端，緩衝區會以提供的順序填滿，但完成指示可能會以不同順序進行。

重迭 i/o 的延遲完成功能也可供 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))。

## <a name="delivering-completion-indications"></a>傳遞完成指示

服務提供者有兩種方式可表示重迭的完成：設定用戶端指定的事件物件，或叫用用戶端指定的完成常式。 在這兩種情況下，資料結構（ [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped)）會與每個重迭運算相關聯。 此結構是由用戶端所配置，並由它用來指出如果在完成時要設定任何) 的事件物件 (。 服務提供者可能會使用 **WSAOVERLAPPED** 結構作為儲存結果之控制碼的位置 (例如，已傳輸的位元組數、更新的旗標、錯誤碼等 ) 用於特定的重迭運算。 若要取得這些結果，用戶端必須叫用 [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult)，將指標傳入對應的重迭結構。

如果選取了特定重迭 i/o 要求的事件型完成指示，用戶端可能會使用 [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) 常式來輪詢或等候重迭作業的完成。 如果針對特定的重迭 i/o 要求選取完成-以常式為基礎的完成指示，則只有 **WSPGetOverlappedResult** 的輪詢選項可用。 用戶端也可以使用其他方法來等候 (例如使用 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)) ，直到對應的事件物件已發出信號，或服務提供者已叫用指定的完成常式為止。 指出完成之後，用戶端可能會叫用 **WSPGetOverlappedResult**，並預期會立即完成呼叫。

## <a name="invoking-socket-io-completion-routines"></a>叫用通訊端 i/o 完成常式

如果重迭作業的 *lpCompletionRoutine* 參數不是 **Null**，則在重迭的作業完成時，服務提供者必須負責排列用戶端指定之完成常式的調用。 因為完成常式必須在起始重迭運算的相同執行緒內容中執行，所以無法直接從服務提供者叫用。 Ws2 \_32.DLL 提供 (APC) 機制的非同步程序呼叫，以促進完成常式的調用。

服務提供者會藉由呼叫 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)來排列要在適當執行緒中執行的函式。 您可以從任何進程和執行緒內容呼叫這個函式，甚至是與用來起始重迭作業的執行緒和進程不同的內容。

[**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) 會將 [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) 結構的指標、要叫用之 APC 函式的指標，以及後續傳遞至 apc 函數的32位內容值作為輸入參數。 服務提供者一律會透過 *lpThreadId* 參數提供給重迭函數的正確 **WSATHREADID** 結構指標。 提供者應該在本機儲存 **WSATHREADID** 結構，並提供指向這個 **WSATHREADID** 結構複本的指標，作為 **WPUQueueApc** 的輸入參數。 **WPUQueueApc** 函式傳回之後，提供者就可以處置其 **WSATHREADID** 的複本。

此程式 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) 只會將足夠的資訊，以指定的參數來呼叫指定的 APC 函式，但不會呼叫它。 當目標執行緒進入可提供警示等候狀態時，此資訊會被清除佇列，並在該目標執行緒和處理內容中呼叫 APC 函數。 因為 APC 機制只支援單一32位的內容值，所以 APC 函式本身不能是用戶端指定的完成常式，這會牽涉到更多參數。 服務提供者必須改為提供其本身的 APC 函式指標，該函式會使用提供的內容值來存取重迭作業所需的結果資訊，然後再叫用用戶端指定的完成常式。

對於使用者模式元件執行重迭 i/o 的服務提供者而言，APC 機制的一般使用方式如下：

-   當 i/o 作業完成時，提供者會配置小型緩衝區，並將其封裝至用戶端提供的完成程式和參數值的指標，以傳遞給程式。
-   它會將一個 APC 排入佇列，並將緩衝區的指標指定為內容值，並將其本身的中繼程式指定為目的程式。
-   當目標執行緒最後進入可提供警示 wait 狀態時，會在適當的執行緒內容中呼叫服務提供者的中繼程式。
-   中繼程式只會解壓縮參數、解除配置緩衝區，然後呼叫用戶端提供的完成程式。
-   若為核心模式元件所執行之重迭 i/o 的服務提供者，一般的實作為類似，不同之處在于執行會使用標準核心介面將 APC 排入佇列。

相關核心介面的描述超出 Windows 通訊端2規格的範圍。

> [!Note]  
> 服務提供者必須允許 Windows 通訊端2用戶端從通訊端 i/o 完成常式的內容中叫用傳送和接收作業，並保證針對指定的通訊端，i/o 完成常式不會進行嵌套。

 

在某些情況下，多層式服務提供者可能需要在內部背景工作執行緒內起始和完成重迭的作業。 在此情況下，連入函式呼叫中將無法使用 [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) 。 服務提供者介面提供 upcall （ [**WPUOpenCurrentThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuopencurrentthread)），以取得目前線程的 **WSATHREADID** 。 當不再需要這個 **WSATHREADID** 時，應該呼叫 [**WPUCloseThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread)來傳回其資源。

 

 
