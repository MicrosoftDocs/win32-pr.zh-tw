---
description: WSALookupServiceBegin 查詢會使用 SVCID \_ INET \_ HOSTNAMEBYADDR 做為服務類別 GUID。
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: SPI 中的 gethostbyaddr 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511441"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>SPI 中的 gethostbyaddr 函式

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)查詢會使用 SVCID \_ INET \_ HOSTNAMEBYADDR 做為服務類別 GUID。 主機位址在 *lpszServiceInstanceName* 中是以小數點分隔的 IPv4 位址字串的形式提供 (例如 192.9.200.120) 。 *Ws2 \_32.dll* 會指定 LUP 傳回 \_ \_ blob，且 NSP 會使用位移而非指標將 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構放在 BLOB (，而不是上述) 所述的指標。 Nsp 也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。



| 旗標              | 描述                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ 傳回 \_ 名稱 | 從 *lpszServiceInstanceName* 中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構傳回 **h \_ 名稱** 成員。                                                     |
| LUP \_ 傳回 \_ 位址 | 從 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)傳回定址資訊，埠資訊預設為零。 |



 

 

 
