---
description: 以下是開始使用 Windows 通訊端程式設計的逐步指南。
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: 使用 Winsock 開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcce956d7dcb142e4a51ac3a461868dfa055acc9a2d1624b6a6dff5132f86ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132151"
---
# <a name="getting-started-with-winsock"></a>使用 Winsock 開始使用

以下是開始使用 Windows 通訊端程式設計的逐步指南。 其設計目的是要讓您瞭解基本的 Winsock 函數和資料結構，以及它們如何一起運作。

用於說明的用戶端和伺服器應用程式是非常基本的用戶端和伺服器。 Microsoft Windows 軟體開發套件 (SDK) 隨附的範例包含更先進的程式碼範例。

用戶端和伺服器應用程式的前幾個步驟都相同。

-   [關於伺服器和用戶端](about-clients-and-servers.md)
-   [建立基本 Winsock 應用程式](creating-a-basic-winsock-application.md)
-   [初始化 Winsock](initializing-winsock.md)

下列各節說明建立 Winsock 用戶端應用程式的其餘步驟。

-   [建立用戶端的通訊端](creating-a-socket-for-the-client.md)
-   [連接至通訊端](connecting-to-a-socket.md)
-   [在用戶端上傳送和接收資料](sending-and-receiving-data-on-the-client.md)
-   [中斷用戶端連線](disconnecting-the-client.md)

下列各節說明建立 Winsock 伺服器應用程式的其餘步驟。

-   [建立伺服器的通訊端](creating-a-socket-for-the-server.md)
-   [系結通訊端](binding-a-socket.md)
-   [在通訊端上接聽](listening-on-a-socket.md)
-   [接受連接](accepting-a-connection.md)
-   [接收和傳送伺服器上的資料](receiving-and-sending-data-on-the-server.md)
-   [中斷伺服器的連線](disconnecting-the-server.md)

這些基本範例的完整原始程式碼。

-   [執行 Winsock 用戶端和伺服器程式碼範例](finished-server-and-client-code.md)
-   [完成 Winsock 用戶端程式代碼](complete-client-code.md)
-   [完整的 Winsock 伺服器程式碼](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Advanced Winsock 範例

Windows SDK 包含數個更先進的 Winsock 用戶端和伺服器範例。 根據預設，Winsock 範例原始程式碼會由 Windows 7 的 Windows SDK 安裝在下列目錄中：

*C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ NetDs \\ winsock*

在舊版的 Windows SDK 上，上述路徑中的版本號碼會變更。 例如，Windows Vista 的 Windows SDK 會在下列預設目錄中安裝 Winsock 範例原始程式碼：

*C： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ 範例 \\ NetDs \\ winsock*

以下是在下列目錄中，依序從較高到較低效能的順序列出的更先進範例：

-   Iocp

    此目錄包含三個使用 i/o 完成埠的範例程式。 這些套裝程式括使用 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函數的 winsock 伺服器 (iocpserver) 、使用 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) 函式的 winsock 伺服器 (iocpserverex) ，以及用來測試其中一種伺服器的簡單多執行緒 Winsock 用戶端 (iocpclient) 。 伺服器程式支援透過 TCP/IP 連接的多個用戶端，並傳送伺服器接著回顯至用戶端的任意大小資料緩衝區。 為了方便起見，我們開發了簡單的用戶端程式 iocpclient，並持續將資料傳送到伺服器，以使用多個執行緒來壓力。 使用 i/o 完成埠的 Winsock 伺服器可提供最大的效能功能。

-   重疊

    此目錄包含使用重迭 i/o 的範例伺服器程式。 範例程式會使用 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) 函式和重迭 i/o 來有效處理來自用戶端的多個非同步連接要求。 伺服器使用 **AcceptEx** 函式，在單一執行緒 Win32 應用程式中多工不同的用戶端連接。 使用重迭的 i/o 可提供更大的擴充性。

-   WSAPoll

    此目錄包含基本的範例程式，示範如何使用 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函數。 結合的用戶端和伺服器程式為非封鎖，並且使用 **WSAPoll** 函式來判斷何時可能傳送或接收，而不會封鎖。 此範例較適用于說明，而不是高效能伺服器。

-   simple

    此目錄包含三個基本的範例程式，示範伺服器如何使用多個執行緒。 這些套裝程式括簡單的 TCP/UDP 伺服器 (simples) ，這是一種僅限 TCP 的伺服器 (simples \_ ioctl) ，它會使用 Win32 主控台應用程式中的 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 函式來支援多個用戶端要求，而用戶端 TCP/udp 程式 (simplec) 用於測試伺服器。 伺服器示範如何使用多個執行緒來處理多個用戶端要求。 因為為每個用戶端要求建立個別的執行緒，所以這個方法有擴充性問題。

-   accept

    此目錄包含基本的範例伺服器和用戶端程式。 伺服器示範如何使用 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 函式或使用 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) 函式的非同步接受，來使用非封鎖接受。 此範例較適用于說明，而不是高效能伺服器。

 

 
