---
description: WSAAccept 函式可讓應用程式取得呼叫端資訊，例如呼叫端識別碼和服務品質，然後再決定是否接受連入連線要求。
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: 連接設定和卸載
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c5e8c8a95c9baa90e95bd7b7da2702f3522b2a575d3d0181271428837e27b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051716"
---
# <a name="connection-setup-and-teardown"></a>連接設定和卸載

[**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)函式可讓應用程式取得呼叫端資訊，例如呼叫端識別碼和服務品質，然後再決定是否接受連入連線要求。 這是透過應用程式提供的條件函數的回呼來完成。

[**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)函式中的參數所指定的使用者對使用者資料和 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)的條件函數可以在連接建立期間傳送給對等，前提是服務提供者支援這項功能。

支援此) 的通訊協定也可能 (，以便在連線終止時于端點之間交換使用者資料。 起始清除的結束可以呼叫 [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) 函式，以指出不會再傳送任何資料，也不會起始連接清除順序。 針對特定的通訊協定，卸載的一部分是從終止啟動器傳送中斷連接的資料。 收到通知後，遠端端點已起始卸載 (通常是由 FD \_ 關閉指示) ，可呼叫 [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) 函式來接收中斷連線資料（如果有的話）。

若要說明如何使用中斷連線資料，請考慮下列案例。 用戶端/伺服器應用程式的用戶端一半負責終止通訊端連接。 與終止一致，它會提供 (使用中斷連接資料) 其使用伺服器處理的交易總數。 接著，伺服器會以其與所有用戶端一起處理的交易累計總數來回應。 呼叫和指示的順序可能會如下所示：

| 用戶端                                                                                                              | 伺服器端                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  (1) 叫用 [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) 以結束會話並提供交易總計。            |                                                                                                                                                                                                                               |
|                                                                                                                          |  (2) 將 FD \_ 關閉、以零的傳回值 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv)，或從 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)傳回 [WSAEDISCON](windows-sockets-error-codes-2.md)錯誤，表示正常關機正在進行中。 |
|                                                                                                                          |  (3) 叫用 [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) 以取得用戶端的交易總計。                                                                                                                                |
|                                                                                                                          |  (4) 計算所有交易的累積總計。                                                                                                                                                                       |
|                                                                                                                          |  (5) 叫用 [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) 來傳輸總計。                                                                                                                                          |
|  (6) 接收 FD \_ 關閉指示。                                                                                        |  (5a) 叫用 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)。                                                                                                                                                                             |
|  (7) 叫用 [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) 來接收和儲存累積的交易總計。 |                                                                                                                                                                                                                               |
|  (8) Invoke [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

請注意，步驟 (5a) 必須遵循步驟 (5) ，但與步驟 (6) 、 (7) 或 (8) 之間沒有時間關聯性。

 

 



