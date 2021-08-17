---
description: 下列程式碼示範在建立連接之後，用戶端所使用的傳送和接收函式。
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: 在用戶端上傳送和接收資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3150c853f50e8626451cc344179645289058df928600d71bf437dc95d9738986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740559"
---
# <a name="sending-and-receiving-data-on-the-client"></a>在用戶端上傳送和接收資料

下列程式碼示範在建立連接之後，用戶端所使用的 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send) 和 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 函式。

## <a name="client"></a>用戶端


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



[**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send)和 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv)函式都會分別傳回已傳送或接收的位元組數目的整數值，或發生錯誤。 每個函式也會採用相同的參數：作用中通訊端、 **字元** 緩衝區、要傳送或接收的位元組數目，以及要使用的任何旗標。

下一步：[中斷用戶端](disconnecting-the-client.md)連線

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[Winsock 用戶端應用程式](winsock-client-application.md)
</dt> <dt>

[連接至通訊端](connecting-to-a-socket.md)
</dt> </dl>

 

 



