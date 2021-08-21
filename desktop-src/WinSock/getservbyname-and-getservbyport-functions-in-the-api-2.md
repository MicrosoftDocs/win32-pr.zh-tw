---
description: Getservbyname 和 getservbyport 函式會使用 WSALookupServiceBegin 函數來查詢 SVCID \_ INET \_ SERVICEBYNAME 做為服務類別 GUID。
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: API 中的 getservbyname 和 getservbyport 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e5d7cc9b1811eef98cc6d337abc3230ea46bd537a19969a4b412473e671b39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132211"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>API 中的 getservbyname 和 getservbyport 函式

[**Getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)和 [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)函式會使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)函數來查詢 SVCID \_ INET \_ SERVICEBYNAME 做為服務類別 GUID。 傳遞至 **WSALookupServiceBegin** 函式的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構中的 *lpszServiceInstanceName* 成員會參考字串來指出服務名稱或服務埠，並 (選擇性地) 服務通訊協定。 字串的格式會以 FTP 或 TCP 或 21/TCP 或單純的 FTP 來說明。 字串不區分大小寫。 斜線（如果有的話）會將通訊協定識別碼與之前的字串部分隔開。 Ws2 \_32.dll 將會指定 LUP \_ 傳回 \_ BLOB，而且命名空間提供者會使用位移而非指標將 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) 結構放在 BLOB (，而不是上述) 所述。 命名空間提供者也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。

| 旗標              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ 傳回 \_ 名稱 | 從 *lpszServiceInstanceName* 中的 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent)結構傳回 **s \_ 名稱** 成員。                                                                                                                                                                                                                                                                                                                                                                                                               |
| LUP \_ 傳回 \_ 類型 | 傳回 *lpServiceClassId* 中的標準 GUID。瞭解識別為 FTP 或21的服務可能會在另一個埠上，根據本機建立的慣例。 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent)結構的 **s \_ port** 參數應該指出在本機環境中可以聯繫服務的位置。 當 LUP 傳回類型設定時，所傳回的標準 GUID \_ \_ 應該是 Svcs 中的其中一個預先定義 guid，對應于 **SERVENT** 結構中指出的埠號碼。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 通訊端 1.1 API 中的 tcp/ip 相容名稱解析](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[通訊協定獨立名稱解析](protocol-independent-name-resolution-2.md)
</dt> <dt>

[註冊和名稱解析](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



