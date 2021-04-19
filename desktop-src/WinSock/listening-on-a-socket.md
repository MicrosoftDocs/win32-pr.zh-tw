---
description: 當通訊端系結至系統上的 IP 位址和埠之後，伺服器必須在該 IP 位址和埠上接聽連入連線要求。
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: 在通訊端上接聽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989911"
---
# <a name="listening-on-a-socket"></a><span data-ttu-id="cefba-103">在通訊端上接聽</span><span class="sxs-lookup"><span data-stu-id="cefba-103">Listening on a Socket</span></span>

<span data-ttu-id="cefba-104">當通訊端系結至系統上的 IP 位址和埠之後，伺服器必須在該 IP 位址和埠上接聽連入連線要求。</span><span class="sxs-lookup"><span data-stu-id="cefba-104">After the socket is bound to an IP address and port on the system, the server must then listen on that IP address and port for incoming connection requests.</span></span>

## <a name="to-listen-on-a-socket"></a><span data-ttu-id="cefba-105">在通訊端上接聽</span><span class="sxs-lookup"><span data-stu-id="cefba-105">To listen on a socket</span></span>

<span data-ttu-id="cefba-106">呼叫 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 函式，傳遞所建立之通訊端的參數和待處理專案的 *值，這* 是要接受的暫止連接佇列的最大長度。</span><span class="sxs-lookup"><span data-stu-id="cefba-106">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, passing as parameters the created socket and a value for the *backlog*, maximum length of the queue of pending connections to accept.</span></span> <span data-ttu-id="cefba-107">在此範例中， *待* 處理專案（backlog）參數設定為 **SOMAXCONN**。</span><span class="sxs-lookup"><span data-stu-id="cefba-107">In this example, the *backlog* parameter was set to **SOMAXCONN**.</span></span> <span data-ttu-id="cefba-108">這個值是特殊的常數，會指示此通訊端的 Winsock 提供者允許佇列中有合理數量的暫止連接。</span><span class="sxs-lookup"><span data-stu-id="cefba-108">This value is a special constant that instructs the Winsock provider for this socket to allow a maximum reasonable number of pending connections in the queue.</span></span> <span data-ttu-id="cefba-109">檢查一般錯誤的傳回值。</span><span class="sxs-lookup"><span data-stu-id="cefba-109">Check the return value for general errors.</span></span>


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="cefba-110">下一步： [接受連接](accepting-a-connection.md)</span><span class="sxs-lookup"><span data-stu-id="cefba-110">Next Step: [Accepting a Connection](accepting-a-connection.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="cefba-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="cefba-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cefba-112">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="cefba-112">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="cefba-113">Winsock 伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="cefba-113">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="cefba-114">系結通訊端</span><span class="sxs-lookup"><span data-stu-id="cefba-114">Binding a Socket</span></span>](binding-a-socket.md)
</dt> </dl>

 

 



