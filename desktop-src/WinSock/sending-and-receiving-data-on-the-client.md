---
description: 下列程式碼示範在建立連接之後，用戶端所使用的傳送和接收函式。
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: 在用戶端上傳送和接收資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d91ee507d78bc2638a6d3f7383cd6a930651e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997859"
---
# <a name="sending-and-receiving-data-on-the-client"></a><span data-ttu-id="41149-103">在用戶端上傳送和接收資料</span><span class="sxs-lookup"><span data-stu-id="41149-103">Sending and Receiving Data on the Client</span></span>

<span data-ttu-id="41149-104">下列程式碼示範在建立連接之後，用戶端所使用的 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send) 和 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 函式。</span><span class="sxs-lookup"><span data-stu-id="41149-104">The following code demonstrates the [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions used by the client once a connection is established.</span></span>

## <a name="client"></a><span data-ttu-id="41149-105">用戶端</span><span class="sxs-lookup"><span data-stu-id="41149-105">Client</span></span>


```C++
#define DEFAULT_BUFLEN 512

int recvbuflen = DEFAULT_BUFLEN;

const char *sendbuf = "this is a test";
char recvbuf[DEFAULT_BUFLEN];

int iResult;

// Send an initial buffer
iResult = send(ConnectSocket, sendbuf, (int) strlen(sendbuf), 0);
if (iResult == SOCKET_ERROR) {
    printf("send failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

printf("Bytes Sent: %ld\n", iResult);

// shutdown the connection for sending since no more data will be sent
// the client can still use the ConnectSocket for receiving data
iResult = shutdown(ConnectSocket, SD_SEND);
if (iResult == SOCKET_ERROR) {
    printf("shutdown failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

// Receive data until the server closes the connection
do {
    iResult = recv(ConnectSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0)
        printf("Bytes received: %d\n", iResult);
    else if (iResult == 0)
        printf("Connection closed\n");
    else
        printf("recv failed: %d\n", WSAGetLastError());
} while (iResult > 0);
```



<span data-ttu-id="41149-106">[**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send)和 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv)函式都會分別傳回已傳送或接收的位元組數目的整數值，或發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="41149-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="41149-107">每個函式也會採用相同的參數：作用中通訊端、 **字元** 緩衝區、要傳送或接收的位元組數目，以及要使用的任何旗標。</span><span class="sxs-lookup"><span data-stu-id="41149-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="41149-108">下一步：[中斷用戶端](disconnecting-the-client.md)連線</span><span class="sxs-lookup"><span data-stu-id="41149-108">Next Step: [Disconnecting the Client](disconnecting-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="41149-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="41149-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41149-110">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="41149-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="41149-111">Winsock 用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="41149-111">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="41149-112">連接至通訊端</span><span class="sxs-lookup"><span data-stu-id="41149-112">Connecting to a Socket</span></span>](connecting-to-a-socket.md)
</dt> </dl>

 

 



