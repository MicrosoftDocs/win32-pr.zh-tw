---
description: 檢查函式失敗時，會提供資訊清單常數通訊端 \_ 錯誤。 雖然使用此常數並非強制的，但建議使用。 下列範例說明如何使用通訊端 \_ 錯誤常數。
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: 函數失敗時傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b277da114c8c86c53339590eeff3e831cbaf2a4277765bf53047b3d07991b026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740930"
---
# <a name="return-values-on-function-failure"></a>函數失敗時傳回值

檢查函式失敗時，會提供資訊清單常數 **通訊端 \_ 錯誤** 。 雖然使用此常數並非強制的，但建議使用。 下列範例說明如何使用 **通訊端 \_ 錯誤** 常數。

一般的 BSD 樣式 (在 Windows 上將無法運作) 


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Windows風格


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[錯誤碼-errno、h \_ errno 和 WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[處理 Winsock 錯誤](handling-winsock-errors.md)
</dt> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> <dt>

[Windows通訊端錯誤碼](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



