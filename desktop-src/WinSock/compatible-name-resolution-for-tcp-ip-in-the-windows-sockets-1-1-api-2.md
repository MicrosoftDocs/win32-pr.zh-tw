---
description: 請注意，名稱解析的所有 Windows 通訊端1.1 函式都是 IPv4 TCP/IP 網路專用的。
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973463"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析

> [!Note]  
> 所有適用于名稱解析的 Windows 通訊端1.1 函式都是 IPv4 TCP/IP 網路專用的功能。 應用程式開發人員強烈建議您繼續使用這些僅支援 IPv4 的傳輸特定功能。

 

應用程式開發人員應該使用與通訊協定無關的下列功能，並同時支援 IPv6 和 IPv4 名稱解析。

-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows 通訊端1.1 定義了數個用來搭配 TCP/IP (IP 第4版) 網路進行名稱解析的常式。 這些有時稱為 **getXbyY** 函式，並包含下列各項：

<dl>

[**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

這些函數的非同步版本也已定義。

<dl>

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

另外還有兩個函式（現在會在 Winsock2.dll 中執行），分別用來將類似的 Ipv4 位址標記法轉換成字串和二進位標記法。

<dl>

[**inet \_ 位址**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

為了保持與 Windows 通訊端1.1 的嚴格回溯相容性，只要至少有一個命名空間提供者支援 AF INET 位址系列，就會繼續支援所有舊的 IPv4 函式 (這些函式與 \_ IP 版本6（以 AF INET6) 表示）無關 \_ 。

Ws2 \_32.dll 會使用適當的 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **下一個** / **End** 函數呼叫順序，來實作為新的通訊協定獨立名稱解析設備的相容性功能。 以下提供 **getXbyY** 函式如何對應至名稱解析函式的詳細資料。 WSs2 \_32.dll 會處理 **getXbyY** 函數的非同步和同步版本之間的差異，因此只會討論同步 **getXbyY** 函式的實作為。

本節說明 Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析。 下列清單說明本節中的主題：

-   [API 中的 GetXbyY 基本方法](basic-approach-for-getxbyy-in-the-api-2.md)
-   [API 中的 getprotobyname 和 getprotobynumber 函式](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [API 中的 getservbyname 和 getservbyport 函式](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [API 中的 gethostbyname 函式](gethostbyname-function-in-the-api-2.md)
-   [API 中的 gethostbyaddr 函式](gethostbyaddr-function-in-the-api-2.md)
-   [API 中的 gethostname 函式](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[通訊協定獨立名稱解析](protocol-independent-name-resolution-2.md)
</dt> <dt>

[註冊和名稱解析](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
