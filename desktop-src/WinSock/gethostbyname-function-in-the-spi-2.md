---
description: Winsock SPI 中的 Gethostbyname 函式。
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: SPI 中的 gethostbyname 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972034"
---
# <a name="gethostbyname-function-in-the-spi"></a>SPI 中的 gethostbyname 函式

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)查詢會使用 SVCID \_ INET \_ HOSTADDRBYNAME 做為服務類別 GUID。 主機名稱是在 *lpszServiceInstanceName* 中提供。 *Ws2 \_32.dll* 會指定 LUP 傳回 \_ \_ blob，且 NSP 會使用位移而非指標將 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構放在 BLOB (，而不是上述) 所述的指標。 Nsp 也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。



| 旗標              | 描述                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ 傳回 \_ 名稱 | 從 *lpszServiceInstanceName* 中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構傳回 **h \_ 名稱** 成員。                                                                                                                                                            |
| LUP \_ 傳回 \_ 位址 | 從 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)傳回定址資訊，埠資訊預設為零。 請注意，此常式不會解析由以小數點分隔的 IPv4 位址字串組成的主機名稱。 |



 

 

 
