---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: SPI 中的 Helper 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0073eeb9310764ff100431da6491cedd322fa3c803f7465875980956d6059c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112153"
---
# <a name="helper-functions-in-the-spi"></a>SPI 中的 Helper 函數

-   [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

[**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)函式會抓取命名空間提供者已保留的服務類別架構資訊。 它也會在其 [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)的執行中由 Windows 通訊端 2 DLL 使用。

下列巨集定義于 *Svcguid .h* 標頭檔中，可協助在已知的服務類別與這些命名空間之間進行對應。

| 巨集名稱                                                                              | 描述                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **SVCID \_ TCP (埠)**<br/> **SVCID \_ UDP (埠)**<br/>                         | 如果是網際網路通訊協定的 TCP 或 UDP 埠，則會傳回 GUID。                                                                               |
| **為 \_ SVCID \_ TCP (GUID)**<br/> **是 \_ SVCID \_ UDP (GUID)**<br/>                 | 如果 TCP 或 UDP 的 GUID 在允許的範圍內，則傳回 **TRUE** 。                                                                         |
| **\_從 \_ SVCID \_ TCP (GUID 的埠)**<br/> **埠 \_ 從 \_ SVCID \_ UDP (GUID)**<br/> | 傳回與 GUID 相關聯的 TCP 或 UDP 埠。                                                                                              |
| **SVCID \_ NETWARE (SAPID)**<br/>                                                    | 假設服務廣告通訊協定 (SAP) 識別碼，則會傳回 GUID。 此宏會搭配 NetWare 環境內的 SAP 命名空間使用。 |
| **\_從 \_ SVCID \_ NETWARE (GUID) SAPID**<br/>                                        | 傳回與 GUID 相關聯的 NetWare SAP 識別碼。 此宏會搭配 NetWare 環境內的 SAP 命名空間使用。               |
| **是 \_ SVCID \_ NETWARE (GUID)**<br/>                                                 | 如果適用于 NetWare 的 GUID 位於允許的範圍內，則傳回 **TRUE** 。 此宏會搭配 NetWare 環境內的 SAP 命名空間使用。    |



 

> [!Note]  
> *Svcguid* 標頭檔不會自動包含在 *Winsock2* 標頭檔中。

 

 

 




