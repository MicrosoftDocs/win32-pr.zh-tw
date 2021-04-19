---
description: Windows 通訊端2支援重迭的 i/o，而且所有的傳輸提供者都支援這項功能。
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: 重迭的 i/o 和事件物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed034f06243959d94a1ada7eaa71e33c84cd35ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974034"
---
# <a name="overlapped-io-and-event-objects"></a>重迭的 i/o 和事件物件

Windows 通訊端2支援重迭的 i/o，而且所有的傳輸提供者都支援這項功能。 重迭的 i/o 會遵循在 Windows 中建立的模型，並可在使用 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket)函數建立的通訊端上執行，或在使用 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)函式建立的通訊端上，使用 *dwFlags* 參數中所設定的 **WSA \_ 旗 \_** 標重迭旗標

> [!Note]  
> 使用重迭的屬性建立通訊端，並不會影響通訊端目前是否處於封鎖或非封鎖模式。 使用重迭屬性建立的通訊端可以用來執行重迭的 i/o，這樣做並不會變更通訊端的封鎖模式。 由於重迭的 i/o 作業不會封鎖，因此通訊端的封鎖模式與這些作業無關。

 

針對接收，應用程式會使用 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) 或 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) 函數來提供要接收資料的緩衝區。 如果有一或多個緩衝區在網路收到資料的時間之前張貼，則在使用者的緩衝區抵達時，該資料就會立即放在使用者的緩衝區中。 因此，它可以避免叫用 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 或 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 函式時所發生的複製作業。 如果在張貼接收緩衝區時資料已存在，則會立即複製到使用者的緩衝區。

當應用程式未張貼任何接收緩衝區時，如果資料到達，則網路會將設定為熟悉的操作操作樣式。 也就是說，傳入的資料會在內部緩衝處理，直到應用程式發出接收呼叫，因而提供可複製資料的緩衝區。 當應用程式使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 將接收緩衝區的大小設定為零時，就會發生例外狀況。 在此情況下，可靠的通訊協定只允許在應用程式緩衝區張貼時接收資料，而且不可靠的通訊協定上的資料將會遺失。

在傳送端，應用程式會使用 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) 或 [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) 來提供已填滿緩衝區的指標，然後在網路取用緩衝區的內容之前，以任何方式同意不要擾亂緩衝區。

重迭的傳送和接收呼叫會立即傳回。 傳回值為零表示 i/o 作業已立即完成，而且對應的完成指示已發生。 也就是說，相關聯的事件物件已收到信號，或完成常式已排入佇列，並且將在呼叫執行緒進入可提供警示等候狀態時執行。

通訊端錯誤的傳回值 \_ 加上 [WSA \_ IO \_ 暫](windows-sockets-error-codes-2.md) 止的錯誤碼，表示已成功起始重迭的作業，而且當取用傳送緩衝區或接收作業完成時，將會提供後續的指示。 不過，對於位元組資料流程樣式的通訊端，無論緩衝區是否已滿，就會在每次傳入的資料用盡時進行。 任何其他錯誤碼都會指出重迭的作業未成功啟動，而且即將出現任何完成指示。

傳送和接收作業可以重迭。 您可以叫用接收函式數次，以張貼接收緩衝區以準備傳入資料，而且可以叫用傳送函式數次，以將多個緩衝區排入佇列以傳送。 雖然應用程式可以依賴一連串的重迭傳送緩衝區（依提供的順序傳送），但對應的完成指示可能會以不同的順序進行。 同樣地，在接收端，緩衝區可以依提供的順序填滿，但完成指示可能會以不同順序發生。

在許多情況下，使用 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)、 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)、 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)、 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)、 [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)和類似函數的 Winsock 重迭作業都可以取消。 不過，若要繼續使用已取消未完成作業的通訊端，行為是未定義的。 取消重迭的作業之後，應呼叫 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函數。 因此，為了獲得最佳結果，您應該呼叫 **導致 closesocket** 函式來關閉通常會停止所有暫止作業的通訊端，而不是直接取消 i/o。

重迭 i/o 的延遲完成功能也適用于 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)，這是 [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)的增強版本。

 

 
