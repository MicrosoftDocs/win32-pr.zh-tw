---
description: Windows通訊端1.1 定義了數個常式，用於 TCP/IP 網路的 IPv4 名稱解析。 這些通常稱為 GetXbyY 函式，並包含下列各項。
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Windows 通訊端 1.1 SPI 中的 tcp/ip 相容名稱解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea355eb85d41a507e4970bf0c8d925a41ed81ca51c08b9c77955ad702a62d27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051676"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>Windows 通訊端 1.1 SPI 中的 tcp/ip 相容名稱解析

Windows通訊端1.1 定義了數個常式，用於 TCP/IP 網路的 IPv4 名稱解析。 這些通常稱為 **GetXbyY** 函式，並包含下列各項。

[**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)

[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)

這些函數的非同步版本也已定義。

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

這些函式僅適用于 TCP/IP 網路;不建議使用與通訊協定無關的應用程式開發人員繼續使用這些傳輸特有的功能。 不過，若要保留與 Windows 通訊端1.1 的嚴格回溯相容性，只要至少有一個命名空間提供者支援 AF INET 位址系列，上述函式就會繼續受到支援 \_ 。

*Ws2 \_32.dll* 使用適當的 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)、 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)函數呼叫順序，來實作為新的通訊協定獨立名稱解析設備的相容性函數。 以下提供 **GetXbyY** 函式如何對應至名稱解析函式的詳細資料。 Ws2 \_32.dll 會處理 **GetXbyY** 函數的非同步和同步版本之間的差異，因此只會討論同步 **GetXbyY** 函式的執行。

 

 
