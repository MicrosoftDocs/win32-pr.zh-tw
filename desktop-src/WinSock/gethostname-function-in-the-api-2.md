---
description: Gethostname 函式會使用 WSALookupServiceBegin 函數，將 SVCID \_ 主機名稱查詢為服務類別 GUID。
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: API 中的 gethostname 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970424"
---
# <a name="gethostname-function-in-the-api"></a>API 中的 gethostname 函式

[**Gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)函式會使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)函數，將 SVCID \_ 主機名稱查詢為服務類別 GUID。 如果傳遞給 **WSALookupServiceBegin** 函式之 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構的 **lpszServiceInstanceName** 成員是 **null** 或參考 **null** 字串 (也就是。 "" ) ，將會解析本機主機。 否則，就會在指定的主機名稱上進行查閱。 基於模擬 **gethostname** 的目的 \_ ，Ws232.dll 指定 **lpszServiceInstanceName** 成員的 **Null** 指標，並指定 LUP \_ \_ 傳回名稱，以便在 **lpszServiceInstanceName** 成員中傳回主機名稱。 如果應用程式使用此查詢並指定 LUP \_ RETURN \_ ADDR，則會在 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構中提供主機位址。 此查詢的 LUP 傳回 \_ \_ BLOB 動作未定義。 除非傳遞給 **WSALookupServiceBegin** 函式之 **WSAQUERYSET** 結構的 **lpszQueryString** 成員參考 FTP 之類的服務（在此情況下，會提供指定服務的完整傳輸位址），否則埠資訊會預設為零。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[通訊協定獨立名稱解析](protocol-independent-name-resolution-2.md)
</dt> <dt>

[註冊和名稱解析](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
