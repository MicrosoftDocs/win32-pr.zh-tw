---
description: 新增 IPv6 支援時，您必須確定您的應用程式會定義大小正確的資料結構。
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: 變更 IPv6 Winsock Html5 應用程式的資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999c0d0c5a335c1367165c227fc1aad805579db5a790a19d316a1624e922947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741548"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>變更 IPv6 Winsock Html5 應用程式的資料結構

新增 IPv6 支援時，您必須確定您的應用程式會定義大小正確的資料結構。 IPv6 位址的大小遠超過 IPv4 位址。 當儲存 IP 位址時，以硬式編碼來處理 IPv4 位址大小的結構，將會導致您的應用程式發生問題，且必須加以修改。

最佳做法

確保您的結構正確大小的最佳方法是使用 [**SOCKADDR \_ 儲存體**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) 結構。 **SOCKADDR \_ 儲存體** 結構與 IP 位址版本無關。 使用 **SOCKADDR \_ 儲存體** 結構來儲存 IP 位址時，可以使用一個程式碼基底適當地處理 IPv4 和 IPv6 位址。

下列範例（取自附錄 B 中的 Server .c 檔案的摘錄）會識別 **SOCKADDR \_ 儲存** 結構的適當使用。 請注意，如下列範例所示，如這個範例所示，此結構可正常地處理 IPv4 或 IPv6 位址。


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

#define BUFFER_SIZE 512
#define DEFAULT_PORT "27015"

int main(int argc, char **argv)
{
    char Buffer[BUFFER_SIZE] = {0};
    char *Hostname;
    int Family = AF_UNSPEC;
    int SocketType = SOCK_STREAM;
    char *Port = DEFAULT_PORT;
    char *Address = NULL;
    int i = 0;
    DWORD dwRetval = 0;
    int iResult = 0;
    int FromLen = 0;
    int AmountRead = 0;

    SOCKADDR_STORAGE From;

    WSADATA wsaData;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;

    // Parse arguments
    if (argc >= 1) {
        Hostname = argv[1];
    }    

   // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    From.ss_family = (ADDRESS_FAMILY) Family;
    
    //...
        
        return 0;
}
```



> [!Note]  
> [**SOCKADDR \_ 儲存體**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))結構是 Windows XP 的新結構。

 

要避免的程式碼

一般而言，許多應用程式會使用 [**sockaddr**](sockaddr-2.md) 結構來儲存與通訊協定無關的位址，或 IP 位址的 **sockaddr \_** 結構。 結構中的 sockaddr 結構和 **sockaddr \_** 都夠大，足以容納 ipv6 位址，因此，如果您的應用程式與 ipv6 相容，則兩者都不足夠。

程式碼撰寫工作

**從 IPv4 將現有的程式碼基底修改為 IPv4 和 IPv6 互通性**

1.  取得 Checkv4.exe 公用程式。 此公用程式隨附于 Microsoft Windows 軟體開發套件 (SDK) 可透過 MSDN 訂用帳戶取得，或從 web 下載。
2.  針對您的程式碼執行 Checkv4.exe 公用程式。 瞭解如何在 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md)一節中，針對您的檔案執行 Checkv4.exe 公用程式。
3.  此公用程式會警示您 **\_ 在結構中** 使用 **sockaddr** 或 sockaddr，並提供有關如何使用 IPv6 相容結構 [**sockaddr \_ 儲存體**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))來取代任何的建議。
4.  請適當地取代任何這類實例和相關聯的程式碼，以使用 **SOCKADDR \_ 儲存體** 結構。

或者，您可以 **\_ 在結構中** 搜尋 **sockaddr** 和 sockaddr 實例的程式碼基底，並視需要將所有 (和其他相關聯的程式碼變更為 **sockaddr \_ 儲存體** 結構的) 。

> [!Note]  
> **Addrinfo** 和 **SOCKADDR \_ 儲存體** 結構分別包含 (**ai \_ 系列** 與 **ss \_ 系列**) 的通訊協定和位址家族成員。 RFC 2553 將 [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa)的 **ai \_ 系列** 成員指定為 int，而 **ss \_ 系列** 則指定為簡短; 因此，在這些成員之間的直接複製會導致編譯器錯誤。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 通訊端應用程式的 IPv6 指南](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的雙重堆疊通訊端](dual-stack-sockets.md)
</dt> <dt>

[IPv6 Winsock 應用程式的函式呼叫](function-calls-2.md)
</dt> <dt>

[使用硬式編碼的 IPv4 位址](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的消費者介面問題](user-interface-issues-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的基礎通訊協定](underlying-protocols-2.md)
</dt> </dl>

 

 
