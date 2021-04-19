---
description: Gethostbyaddr 函式會使用 WSALookupServiceBegin 函數，將 SVCID \_ INET \_ HOSTNAMEBYADDR 查詢為服務類別 GUID。
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: API 中的 gethostbyaddr 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999856"
---
# <a name="gethostbyaddr-function-in-the-api"></a>API 中的 gethostbyaddr 函式

[**Gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)函式會使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)函數，將 SVCID \_ INET \_ HOSTNAMEBYADDR 查詢為服務類別 GUID。 主機位址是以點 decimnal IPv4 字串的形式提供 (例如，"192.9.200.120" ) 在傳遞給 **WSALookupServiceBegin** 函數的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構的 *lpszServiceInstanceName* 成員中。 Ws2 \_32.dll 會指定 LUP \_ 傳回 \_ blob，而且名稱服務提供者會使用位移來將 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) 結構放在 BLOB (，而不是上述) 所述的指標。 名稱服務提供者也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。 

| 旗標              | 描述                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ 傳回 \_ 名稱 | 從 *lpszServiceInstanceName* 中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構傳回 **h \_ 名稱** 成員。                                                     |
| LUP \_ 傳回 \_ 位址 | 從 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)傳回定址資訊，埠資訊預設為零。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[通訊協定獨立名稱解析](protocol-independent-name-resolution-2.md)
</dt> <dt>

[註冊和名稱解析](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
