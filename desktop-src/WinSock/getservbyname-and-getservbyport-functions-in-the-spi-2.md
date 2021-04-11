---
description: WSALookupServiceBegin 查詢會使用 SVCID \_ INET \_ SERVICEBYNAME 做為服務類別 GUID。
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: SPI 中的 getservbyname 和 getservbyport 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd910dc7ab478c262bd5ca6c480dc3ec58e1b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113072"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>SPI 中的 getservbyname 和 getservbyport 函數

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)查詢會使用 SVCID \_ INET \_ SERVICEBYNAME 做為服務類別 GUID。 *LpszServiceInstanceName* 參數會參考指出服務名稱或服務埠的字串，並 (選擇性地) 服務通訊協定。 字串的格式會以 ftp/tcp 或 21/tcp 或單純的 ftp 來說明。 字串不區分大小寫。 斜線（如果有的話）會將通訊協定識別碼與之前的字串部分隔開。 Ws2 \_32.dll 將會指定 LUP \_ 傳回 \_ BLOB，而且 NSP 會使用位移而非指標將 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) 結構放在 BLOB (，而不是上述) 所述。 Nsp 也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。



| 旗標              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ 傳回 \_ 名稱 | 從 *lpszServiceInstanceName* 中的 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent)結構傳回 **s \_ 名稱** 成員。                                                                                                                                                                                                                                                                                                                                                                                                            |
| LUP \_ 傳回 \_ 類型 | 傳回 *lpServiceClassId* 中的標準 GUID。瞭解識別為 ftp 或21的服務可能會在另一個埠上，根據本機建立的慣例。 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent)結構的 **s \_ 埠** 成員應該指出在本機環境中可以聯繫服務的位置。 當 LUP 傳回類型設定時，所傳回的標準 GUID \_ \_ 應該是 svcs 中的其中一個預先定義 guid，對應于 **SERVENT** 結構中指出的埠號碼。 |



 

 

 



