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
# <a name="listening-on-a-socket"></a>在通訊端上接聽

當通訊端系結至系統上的 IP 位址和埠之後，伺服器必須在該 IP 位址和埠上接聽連入連線要求。

## <a name="to-listen-on-a-socket"></a>在通訊端上接聽

呼叫 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 函式，傳遞所建立之通訊端的參數和待處理專案的 *值，這* 是要接受的暫止連接佇列的最大長度。 在此範例中， *待* 處理專案（backlog）參數設定為 **SOMAXCONN**。 這個值是特殊的常數，會指示此通訊端的 Winsock 提供者允許佇列中有合理數量的暫止連接。 檢查一般錯誤的傳回值。


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



下一步： [接受連接](accepting-a-connection.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[Winsock 伺服器應用程式](winsock-server-application.md)
</dt> <dt>

[系結通訊端](binding-a-socket.md)
</dt> </dl>

 

 



