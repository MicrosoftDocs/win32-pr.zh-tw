---
description: 將應用程式從 Berkeley 通訊端環境移植到 Windows 環境的一個主要問題，就是封鎖;也就是說，叫用不會傳回的函式，直到相關聯的作業完成為止。
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Windows通訊端1.1 封鎖常式和 EINPROGRESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4028549862412b80d1343851fb2a147da804095821fdefab4b6aae0eb6ec5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641218"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Windows通訊端1.1 封鎖常式和 EINPROGRESS

將應用程式從 Berkeley 通訊端環境移植到 Windows 環境的一個主要問題，就是封鎖;也就是說，叫用不會傳回的函式，直到相關聯的作業完成為止。 當作業需要很長的時間才能完成時，會發生問題：例如，可能會封鎖的 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 函式，直到從對等系統收到資料為止。 Berkeley 通訊端模型內的預設行為是讓通訊端在封鎖模式下運作，除非程式設計師明確要求將作業視為非封鎖。 Windows通訊端1.1 環境無法採用先占式排程。 因此，強烈建議程式設計人員盡可能使用非封鎖 (非同步) 作業，Windows 通訊端1.1。 因為這不一定是可行的，所以提供了以下所述的虛擬封鎖功能。

> [!Note]  
> Windows通訊端2只會在已建立的32位作業系統上執行，而鎖死不是問題。 Windows 通訊端2中不需要 Windows 通訊端1.1 所建議的程式設計作法。

 

即使是在封鎖通訊端上，某些函式（例如 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind)、 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)和 [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) ）會立即完成。 這些函數的封鎖和非封鎖作業之間沒有任何差異。 其他作業（例如，「 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv)」）可以立即完成或需要任意時間才能完成，視不同的傳輸條件而定。 套用至封鎖通訊端時，這些作業稱為封鎖作業。 下列函數可以封鎖：

-   [**recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**發送**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)

使用16位 Windows 通訊端1.1，無法立即完成的封鎖作業會由虛擬封鎖處理，如下所示。

服務提供者會起始作業，然後輸入迴圈來分派任何 Windows 訊息 (產生處理器給另一個執行緒（如有必要) ），然後檢查 Windows 通訊端函數是否完成。 如果函式已完成，或已叫用 [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) ，封鎖函式就會完成，並產生適當的結果。

服務提供者必須允許安裝不會處理訊息的封鎖攔截函式，以避免在封鎖作業未完成的情況下重新執行訊息的可能性。 最簡單的這類封鎖攔截函數會傳回 **FALSE**。 如果 Windows 通訊端 DLL 相依于內部作業的訊息，它可以在執行應用程式封鎖攔截之前執行 **PeekMessage** (**hMyWnd**... ) ，讓它可以取得其訊息，而不會影響系統的其餘部分。

在16位 Windows 通訊端1.1 環境中，如果收到封鎖作業正在進行之進程的 Windows 訊息，則應用程式會嘗試發出另一個 Windows 通訊端呼叫的風險。 由於難以安全地管理此狀況，Windows 通訊端1.1 不支援這類應用程式行為。 不允許應用程式進行多個嵌套 Windows 通訊端函數呼叫。 特定工作只允許一個未處理的函式呼叫。 唯一的例外是為了協助程式設計人員在這種情況下所提供的兩個函數： [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) 和 [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)。

您可以隨時呼叫 [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking)函式，以判斷封鎖 Windows 通訊端1.1 呼叫是否正在進行中。 同樣地，您可以隨時呼叫 [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) 函式來取消進行中的封鎖呼叫。 Windows 通訊端函式的任何其他嵌套都失敗，並出現錯誤 WSAEINPROGRESS。

請強調，這項限制適用于封鎖和非封鎖作業。 針對在呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)時協商2.0 版或更高版本的 Windows 通訊端2應用程式，作業的嵌套不會有任何限制。 在罕見的情況下，作業可能會變成嵌套，例如在 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)條件式接受回呼期間，或是服務提供者輪流叫用 Windows 通訊端2函式時。

雖然這項機制足以滿足簡單的應用程式，但它無法支援更高階應用程式的複雜訊息分派需求 (例如，使用 MDI 模型) 。 針對這類應用程式，Windows 通訊端 API 包含 [**WSASetBlockingHook**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)函式，可讓應用程式指定可呼叫的特殊常式，而不是上述討論中所述的預設訊息分派常式。

只有在下列所有條件都成立時，Windows 通訊端提供者才會呼叫封鎖攔截：

-   常式是定義為可以封鎖的常式。
-   指定的通訊端是封鎖的通訊端。
-   無法立即完成要求。

通訊端預設會設定為封鎖，但使用 **FIONBIO** IOCTL 或 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)函數的 [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)函數可以將通訊端設定為非封鎖模式。

封鎖攔截程式永遠不會被呼叫，且如果應用程式遵循下列指導方針，應用程式就不需要擔心封鎖攔截的重新進入問題：

-   它只會使用非封鎖通訊端。
-   它會使用 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) 和/或 **WSAAsyncGetXByY** 常式，而不是 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 和 **getXbyY** 常式。

如果 Windows 通訊端1.1 應用程式會叫用採用記憶體物件指標的非同步或非封鎖作業 (緩衝區或全域變數（例如) 作為引數），則應用程式必須負責確保物件可在整個作業中使用 Windows 通訊端。 應用程式不能叫用任何可能影響對應的 Windows 函式，或處理所涉及記憶體的可行性。

 

 



