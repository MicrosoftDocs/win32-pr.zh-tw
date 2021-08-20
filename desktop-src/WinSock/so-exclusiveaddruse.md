---
description: SO \_ EXCLUSIVEADDRUSE 通訊端選項可防止其他通訊端強制系結至相同的位址和埠。
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: 'SO_EXCLUSIVEADDRUSE 通訊端選項 (Winsock2) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9d7b00cc2fcd01fc9d440ce2ef889a9e1be937d5d83af90cfa71bf6f83d14c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927340"
---
# <a name="so_exclusiveaddruse-socket-option"></a>所以 \_ EXCLUSIVEADDRUSE 通訊端選項

SO \_ EXCLUSIVEADDRUSE 通訊端選項可防止其他通訊端強制系結至相同的位址和埠。

## <a name="syntax"></a>Syntax

SO \_ EXCLUSIVEADDRUSE 選項可防止其他通訊端強制系結至相同的位址和埠，這是由 SO \_ REUSEADDR 通訊端選項所啟用的作法。 惡意應用程式可能會執行這類重複使用，以中斷應用程式。 \_EXCLUSIVEADDRUSE 選項對於需要高可用性的系統服務非常有用。

下列程式碼範例將說明如何設定這個選項。


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



若要有任何效果，必須在呼叫系結函式 \_ 之前[](/windows/desktop/api/winsock/nf-winsock-bind)設定 EXCLUSIVADDRUSE 選項， (這也適用于 \_ REUSEADDR 選項) 。 [表 1] 列出設定 \_ EXCLUSIVEADDRUSE 選項的效果。 萬用字元表示系結至萬用字元位址，例如0.0.0.0 （IPv4）和：：（用於 IPv6）。 特定表示系結至特定介面，例如系結指派給介面卡的 IP 位址。 Specific2 表示在特定情況下系結至特定位址，而不是系結至的位址。

> [!Note]  
> 只有在第一個系結以特定位址執行時，才適用 Specific2 案例;如果第一個通訊端系結至萬用字元，則特定的專案會涵蓋所有特定的位址案例。

 

例如，假設電腦具有兩個 IP 介面：10.0.0.1 和10.99.99.99。 如果第一次系結為10.0.0.1 和埠5150，並 \_ 設定 EXCLUSIVEADDRUSE 選項，則第二個系結至10.99.99.99 和埠5150，並設定任何或未設定任何選項。 但是，如果第一個通訊端系結至萬用字元位址 (0.0.0.0) 和埠5150，並 \_ 將 EXCLUSIVEADDRUSE 設定為，則任何後續系結至相同的埠（不論 IP 位址為何）都會失敗，並出現 WSAEADDRINUSE (10048) 或 WSAEACCESS (10013) ，這取決於第二個系結通訊端上所設定的選項。

### <a name="bind-behavior-with-various-options-set"></a>設定各種選項的系結行為



第二個系結

第一個系結

*\_EXCLUSIVEADDRUSE*

*沒有任何選項* 或 *\_ REUSEADDR*

*通 配 符*

*特定*

*通 配 符*

*特定*

$ {ROWSPAN3} $*SO \_ EXCLUSIVEADDRUSE*$ {REMOVE} $  

*通 配 符*

失敗 (10048) 

失敗 (10048) 

失敗 (10048) 

失敗 (10048) 

*特定*

失敗 (10048) 

失敗 (10048) 

失敗 (10048) 

失敗 (10048) 

*Specific2*

n/a

Success

n/a

Success

$ {ROWSPAN3} $*No options*$ {REMOVE} $  

*通 配 符*

失敗 (10048) 

失敗 (10048) 

失敗 (10048) 

失敗 (10048) 

*特定*

失敗 (10048) 

失敗 (10048) 

失敗 (10048) 

失敗 (10048) 

*Specific2*

n/a

Success

n/a

Success

$ {ROWSPAN3} $*SO \_ REUSEADDR*$ {REMOVE} $  

*通 配 符*

失敗 (10013) 

失敗 (10013) 

成功\*

Success

*特定*

失敗 (10013) 

失敗 (10013) 

Success

成功\*

*Specific2*

n/a

Success

n/a

Success

\* 未定義任何通訊端將接收封包的行為。



 

如果第一個系結未設定任何選項或 \_ REUSEADDR，而第二個系結會執行 \_ REUSEADDR，則第二個通訊端已 overtaken 埠，以及與哪些通訊端將接收封包的行為不確定。 \_為了解決這種情況，我們引進了 EXCLUSIVEADDRUSE。

在 \_ 通訊端關閉之後，不能一律立即重複使用具有 EXCLUSIVEADDRUSE 集的通訊端。 例如，如果具有獨佔旗標的接聽通訊端已設定接受接聽通訊端關閉之後的連接，則另一個通訊端無法系結至具有獨佔旗標的第一個接聽通訊端的相同埠，直到接受的連接不再使用中為止。

這種情況可能相當複雜;雖然通訊端已關閉，但基礎傳輸可能不會終止其連線。 即使在關閉通訊端之後，系統也必須傳送所有緩衝的資料、將正常的中斷連接傳送給對等，並等候對等的正常中斷連線。 因此，基礎傳輸可能永遠不會釋放連線，例如當對等通告零大小的視窗或其他這類攻擊時。 在上述範例中，在接受用戶端連線之後，接聽通訊端已關閉。 現在即使用戶端連接已關閉，如果用戶端連線因為未確認的資料而保持在作用中狀態，埠仍可能不會重複使用。

為了避免這種情況，應用程式應該確保正常關機：使用 SD SEND 旗標來呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) \_ ，然後等候 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 迴圈，直到傳回零個位元組為止。 這麼做可避免與埠重複使用相關的問題，並保證對等的所有資料都已成功接收。

\_您可以在通訊端上設定此等量選項，以防止埠進入其中一個作用中的等候狀態; 不過，不建議這麼做，因為它可能會導致不想要的效果，因為這可能會導致連線重設。 例如，如果已接收資料，但對等尚未認可資料，而且本機電腦關閉具有此設定的資料 \_ 集，則會重設連線，對等會捨棄未認可的資料。 此外，挑選適當的時間來進行逗留很困難;值太小會導致許多已中止的連線，而較大的超時可能會讓系統容易遭受拒絕服務的攻擊，方法是建立許多連接，進而拖延許多應用程式執行緒。

> [!Note]  
> 使用 EXCLUSIVEADDRUSE 選項的通訊端 \_ 必須在關閉之前適當地關閉。 如果相關聯的服務需要重新開機，則無法這樣做可能會造成阻絕服務攻擊。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winsock2. h</dt> </dl> |



 

 




