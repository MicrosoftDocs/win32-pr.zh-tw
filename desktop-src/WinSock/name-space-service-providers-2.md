---
description: 命名空間提供者會在 Winsock 命名空間 SPI 和現有名稱服務的原生程式設計介面（例如 DNS、X 500 或 NetWare 目錄服務 (NDS) ）之間，執行介面對應。
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: 命名空間服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e975c7ad0e5df29910624bb8f0b9d94fd24d9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970420"
---
# <a name="namespace-service-providers"></a>命名空間服務提供者

命名空間提供者會在 Winsock 命名空間 SPI 和現有名稱服務的原生程式設計介面（例如 DNS、X 500 或 NetWare 目錄服務 (NDS) ）之間，執行介面對應。 雖然命名空間提供者只支援一個命名空間，但是有可能會安裝指定命名空間的多個提供者。 單一 DLL 也有可能建立多個命名空間提供者的實例。 安裝命名空間提供者時，會維護 [**WSANAMESPACE \_ 資訊**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) 結構的目錄。 應用程式可能會使用 [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) 來找出電腦支援的命名空間。

在 Windows Vista 和更新版本上，提供了增強的 [**WSANAMESPACE \_ INFOEX**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) 結構和 [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) 函數。

在64位平臺上，會提供類似的 [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) 和 [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) 函數來列舉32位目錄。

如需詳細資訊，請參閱 [Winsock 命名空間服務提供者需求](winsock-namespace-service-provider-requirements.md) 。

## <a name="legacy-getxbyy-service-providers"></a>舊版 GetXbyY 服務提供者

Windows 通訊端2完全支援在 Windows 通訊端1.1 版中找到的 TCP/IP 特定名稱解析功能。 它會藉由在 SPI 中包含一組 **GetXbyY** 函式來完成這項工作。 不過，這組函式的處理方式與 SPI 函式的其餘部分有些不同。 SPI 中出現的 **GetXbyY** 函式會以 GETXBYYSP 開頭 \_ ，並在下表中摘要說明。

Berkeley 樣式函數



| SPI 函式名稱           | Description                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ gethostbyaddr    | 為指定的主機位址提供 [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) 結構。        |
| GETXBYYSP \_ gethostbyname    | 提供指定之主機名稱的 [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) 結構。           |
| GETXBYYSP \_ getprotobyname   | 提供指定之通訊協定名稱的 [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) 結構。     |
| GETXBYYSP \_ getprotobynumber | 為指定的通訊協定編號提供 [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) 結構。   |
| GETXBYYSP \_ getservbyname    | 為指定的服務提供 [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) 結構，例如 e。        |
| GETXBYYSP \_ getservbyport    | 在指定的埠上提供服務的 [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) 結構。 |
| GETXBYYSP \_ gethostname      | 傳回本機電腦的標準主機名稱。                                   |



 

非同步樣式函數



| SPI 函式名稱                   | Description                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ WSAAsyncGetHostByAddr    | 為指定的主機位址提供 [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) 結構。        |
| GETXBYYSP \_ WSAAsyncGetHostByName    | 提供指定之主機名稱的 [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) 結構。           |
| GETXBYYSP \_ WSAAsyncGetProtoByName   | 提供指定之通訊協定名稱的 [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) 結構。     |
| GETXBYYSP \_ WSAAsyncGetProtoByNumber | 為指定的通訊協定編號提供 [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) 結構。   |
| GETXBYYSP \_ WSAAsyncGetServByName    | 提供指定服務名稱的 [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) 結構。        |
| GETXBYYSP \_ WSAAsyncGetServByPort    | 在指定的埠上提供服務的 [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) 結構。 |
| GETXBYYSP \_ WSACancelAsyncRequest    | 取消非同步 **GetXbyY** 操作。                                           |



 

SPI 中這些 **GetXbyY** 函式的語法和語義與在 API 規格中記載的語法和語法完全相同，因此不會在此處重複。

Windows 通訊端 2 DLL 只允許一個服務提供者提供這些服務。 因此，在啟動時，不需要在服務提供者所收到的程式資料表中包含這些函式的指標。 在 Windows 環境中，執行這些函式之 DLL 的路徑是從下列登錄路徑中找到的值取出。 此登錄專案預設不存在：

**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **WinSock2** \\ **參數** \\ **GetXByYLibraryPath**

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In 預設 GetXbyY 服務提供者

預設的 **GetXbyY** 服務提供者已整合到標準的 Windows 通訊端2執行時間元件中。 這個預設提供者會執行上述所有的函式，因此這些函式不需要由任何命名空間提供者來執行。 不過，命名空間提供者可自由提供任何或所有這些函式 (，因此只要儲存字串，就會覆寫預設) ，也就是在指示的登錄機碼中執行這些函式之 DLL 的路徑。 未由命名提供者 DLL 匯出的任何 **GetXbyY** 函數，都會透過內建預設值提供。 不過，請注意，如果提供者想要提供任何非同步版本的 **GetXbyY** 函式，則應該提供所有的非同步函式，讓取消作業可以正確運作。

預設 **GetXbyY** 服務提供者的目前實作為位於 Wsock32.dll 內。 根據透過主控台建立 TCP/IP 設定的方式，將會使用 DNS 或本機主機檔案來進行名稱解析。 使用 DNS 時，預設 **GetXbyY** 服務提供者會使用標準 Windows 通訊端 1.1 API 呼叫來與 DNS 伺服器通訊。 使用設定為預設 TCP/IP 堆疊的任何 TCP/IP 堆疊，就會發生這些交易。 不過，有兩個特殊案例值得一提。

GETXBYYSP gethostname 的預設執行會從登錄取得 \_ 本機主機名稱。 這會對應至指派給 "我的電腦" 的名稱。 GETXBYYSP \_ gethostbyname 和 GETXBYYSP WSAAsyncGetHostByName 的預設實， \_ 一律會將提供的主機名稱與本機主機名稱進行比較。 如果兩者相符，則預設的執行會使用私用介面探查 Microsoft TCP/IP 堆疊，以便探索其本機 IP 位址。 因此，為了完全獨立于 Microsoft TCP/IP 堆疊，命名空間提供者必須同時執行 GETXBYYSP \_ gethostbyname 和 GETXBYYSP \_ WSAAsyncGetHostByName。

 

 



