---
description: Winsock 傳輸 SPI 類似于 Winsock API，因為所有的基本通訊端函數都會出現。
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: API 與 SPI 函數之間的傳輸對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf4167353fa05c5656c588a9dff99c96564a5202ffdc4d21edf358c340634e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739938"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>API 與 SPI 函數之間的傳輸對應

Winsock 傳輸 SPI 類似于 Winsock API，因為所有的基本通訊端函數都會出現。 當新版本的 Winsock 函式和原始版本都存在於 API 時，SPI 中只會顯示新的版本。 以下清單將說明這一點。

-   [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 和 [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) 都對應至 [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))
-   [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) 和 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 對應至 [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 和 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) 對應至 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

其他已折迭至 SPI 增強版的 API 函式包括：

-   [**發送**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

[**Htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)、 [**htons**](/windows/desktop/api/winsock/nf-winsock-htons)、 [**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)和 [**Ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)等支援函式是在 Ws232.dll 中執行 \_ ，而不會向下傳遞給服務提供者。 這些函數的 WSA 版本也是如此。

Windows通訊端服務提供者列舉和封鎖攔截相關函式是在 Ws232.dll 中實現 \_ ，[**因此 WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking)、 [WSASetBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)和 [WSAUnhookBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook)不會顯示為 SPI 函式。

由於錯誤碼會連同 SPI 函式一起傳回，因此 SPI 中不需要 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 和 [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) 的對應專案。

事件物件操作和等候函式（包括 [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)、 [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent)、 [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent)、 [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)和 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ）會直接對應至原生 Windows 服務，因此不會出現在 SPI 中。

在 GetXbyY、WSAAsyncGetXByY 和 WSACancelAsyncRequest 等、 和 [](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest)等 Windows 通訊端1.1 中的所有 tcp/ip 特定名稱轉換和解析函式，以及 [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)會在 Ws232.dll 內實作為 \_ 新的名稱解析功能。 如需詳細資訊，請參閱[Windows 通訊端 1.1 SPI 中的 tcp/ip 相容名稱解析](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md)。 轉換函式（例如 [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) 和 [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) ）是在 Ws2 \_32.dll 內執行。

 

 
