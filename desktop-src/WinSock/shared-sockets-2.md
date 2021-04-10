---
description: 引進 WSADuplicateSocket 函式，以啟用跨進程的通訊端共用。
ms.assetid: f7cf40e9-f3a6-4b62-8a78-df25464e2365
title: 共用通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6753b01f6389254756254d2ebe196af8e2a8a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943829"
---
# <a name="shared-sockets"></a>共用通訊端

引進 [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) 函式，以啟用跨進程的通訊端共用。 來源進程會呼叫 **WSADuplicateSocket** 來取得目標處理序識別碼的特殊 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構。 它會使用一些處理序間通訊 (IPC) 機制，將此結構的內容傳遞至目標進程。 然後，目標進程會在 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)的呼叫中使用 **WSAPROTOCOL \_ 資訊** 結構。 這個函式所傳回的通訊端描述項會是基礎通訊端的額外通訊端描述元，因此會變成共用。 可以在指定進程的執行緒之間共用通訊端，而不使用 **WSADuplicateSocket** 函式，因為通訊端描述項在進程的所有線程中都是有效的。

參考共用通訊端的兩個 (或多個) 描述項，可以獨立于 i/o 的考慮使用。 不過，Winsock 介面不會執行任何類型的存取控制，因此進程必須協調共用通訊端上的任何作業。 共用通訊端的常見範例是使用一個進程來建立通訊端並建立連線。 然後，此程式會將通訊端交給其他負責資訊交換的進程。

[**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa)函式會建立通訊端描述項，而不是基礎通訊端。 如此一來，與通訊端相關聯的所有狀態都會保留在所有描述項的共通範圍內。 例如，使用一個描述項執行的 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 作業，之後會使用來自任何或所有描述項的 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 來顯示。 進程可以在重複的通訊端上呼叫 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) ，而描述項將會解除配置。 不過，基礎通訊端會保持開啟，直到以最後剩下的描述項呼叫 **導致 closesocket** 為止。

共用通訊端上的通知受限於 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) 和 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式的一般條件約束。 使用任何共用描述項來發出上述其中一項呼叫，就會取消通訊端先前的任何事件註冊，無論使用哪一個描述項進行註冊。 例如，可能無法讓進程收到「接收 FD \_ 讀取事件」和「進程 B 接收 fd」 \_ 寫入事件。 在需要這類緊密協調的情況下，建議開發人員使用執行緒，而不是個別的進程。

 

 
