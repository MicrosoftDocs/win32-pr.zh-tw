---
description: 以下是基本 Winsock TCP/IP 用戶端應用程式的完整原始碼。
ms.assetid: 42e003d8-1471-4f7f-b01a-23c7041036ea
title: 完成 Winsock 用戶端程式代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a9000aa117f7262bcd11663eee6fe8f5791538b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991722"
---
# <a name="complete-winsock-client-code"></a><span data-ttu-id="f75fb-103">完成 Winsock 用戶端程式代碼</span><span class="sxs-lookup"><span data-stu-id="f75fb-103">Complete Winsock Client Code</span></span>

<span data-ttu-id="f75fb-104">以下是基本 Winsock TCP/IP 用戶端應用程式的完整原始碼。</span><span class="sxs-lookup"><span data-stu-id="f75fb-104">The following is the complete source code for the basic Winsock TCP/IP Client Application.</span></span>

## <a name="winsock-client-source-code"></a><span data-ttu-id="f75fb-105">Winsock 用戶端原始程式碼</span><span class="sxs-lookup"><span data-stu-id="f75fb-105">Winsock Client Source Code</span></span>


```C++
#define WIN32_LEAN_AND_MEAN

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdlib.h>
#include <stdio.h>


// Need to link with Ws2_32.lib, Mswsock.lib, and Advapi32.lib
#pragma comment (lib, "Ws2_32.lib")
#pragma comment (lib, "Mswsock.lib")
#pragma comment (lib, "AdvApi32.lib")


#define DEFAULT_BUFLEN 512
#define DEFAULT_PORT "27015"

int __cdecl main(int argc, char **argv) 
{
    WSADATA wsaData;
    SOCKET ConnectSocket = INVALID_SOCKET;
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;
    const char *sendbuf = "this is a test";
    char recvbuf[DEFAULT_BUFLEN];
    int iResult;
    int recvbuflen = DEFAULT_BUFLEN;
    
    // Validate the parameters
    if (argc != 2) {
        printf("usage: %s server-name\n", argv[0]);
        return 1;
    }

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed with error: %d\n", iResult);
        return 1;
    }

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if ( iResult != 0 ) {
        printf("getaddrinfo failed with error: %d\n", iResult);
        WSACleanup();
        return 1;
    }

    // Attempt to connect to an address until one succeeds
    for(ptr=result; ptr != NULL ;ptr=ptr->ai_next) {

        // Create a SOCKET for connecting to server
        ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
            ptr->ai_protocol);
        if (ConnectSocket == INVALID_SOCKET) {
            printf("socket failed with error: %ld\n", WSAGetLastError());
            WSACleanup();
            return 1;
        }

        // Connect to server.
        iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
        if (iResult == SOCKET_ERROR) {
            closesocket(ConnectSocket);
            ConnectSocket = INVALID_SOCKET;
            continue;
        }
        break;
    }

    freeaddrinfo(result);

    if (ConnectSocket == INVALID_SOCKET) {
        printf("Unable to connect to server!\n");
        WSACleanup();
        return 1;
    }

    // Send an initial buffer
    iResult = send( ConnectSocket, sendbuf, (int)strlen(sendbuf), 0 );
    if (iResult == SOCKET_ERROR) {
        printf("send failed with error: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }

    printf("Bytes Sent: %ld\n", iResult);

    // shutdown the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed with error: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }

    // Receive until the peer closes the connection
    do {

        iResult = recv(ConnectSocket, recvbuf, recvbuflen, 0);
        if ( iResult > 0 )
            printf("Bytes received: %d\n", iResult);
        else if ( iResult == 0 )
            printf("Connection closed\n");
        else
            printf("recv failed with error: %d\n", WSAGetLastError());

    } while( iResult > 0 );

    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="f75fb-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="f75fb-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f75fb-107">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="f75fb-107">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="f75fb-108">執行 Winsock 用戶端和伺服器程式碼範例</span><span class="sxs-lookup"><span data-stu-id="f75fb-108">Running the Winsock Client and Server Code Sample</span></span>](finished-server-and-client-code.md)
</dt> <dt>

[<span data-ttu-id="f75fb-109">完整的 Winsock 伺服器程式碼</span><span class="sxs-lookup"><span data-stu-id="f75fb-109">Complete Winsock Server Code</span></span>](complete-server-code.md)
</dt> </dl>

 

 



