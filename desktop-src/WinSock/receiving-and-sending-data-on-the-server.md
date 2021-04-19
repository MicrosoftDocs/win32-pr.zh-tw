---
description: 下列程式碼示範伺服器所使用的接收和傳送函數。
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: 接收和傳送伺服器上的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ab20f074db750bef6459c6b9fcb5fd5636a522
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971734"
---
# <a name="receiving-and-sending-data-on-the-server"></a>接收和傳送伺服器上的資料

下列程式碼示範伺服器所使用的 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 和 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send) 函數。

### <a name="to-receive-and-send-data-on-a-socket"></a>在通訊端上接收和傳送資料


```C++
#define DEFAULT_BUFLEN 512

char recvbuf[DEFAULT_BUFLEN];
int iResult, iSendResult;
int recvbuflen = DEFAULT_BUFLEN;

// Receive until the peer shuts down the connection
do {

    iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);

        // Echo the buffer back to the sender
        iSendResult = send(ClientSocket, recvbuf, iResult, 0);
        if (iSendResult == SOCKET_ERROR) {
            printf("send failed: %d\n", WSAGetLastError());
            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }
        printf("Bytes sent: %d\n", iSendResult);
    } else if (iResult == 0)
        printf("Connection closing...\n");
    else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }

} while (iResult > 0);
```



[**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send)和 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv)函式都會分別傳回已傳送或接收的位元組數目的整數值，或發生錯誤。 每個函式也會採用相同的參數：作用中通訊端、 **字元** 緩衝區、要傳送或接收的位元組數目，以及要使用的任何旗標。

下一步：[中斷伺服器的](disconnecting-the-server.md)連線

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[Winsock 伺服器應用程式](winsock-server-application.md)
</dt> <dt>

[接受連接](accepting-a-connection.md)
</dt> </dl>

 

 



