---
title: 瞭解 MprInfo 函式和資訊標頭
description: 下列函式會要求呼叫端傳遞資訊結構或標頭做為其中一個參數。
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932277"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a>瞭解 MprInfo 函式和資訊標頭

下列函式會要求呼叫端傳遞資訊結構或 *標頭* 做為其中一個參數。



| 管理功能                                                        | Configuration 函數                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| 沒有管理功能                                                     | [**MprConfigTransportCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [**MprAdminInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [**MprConfigInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

同樣地，下列函數會傳回信息標頭。



| 管理功能                                                        | Configuration 函數                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

針對傳輸函式，資訊標頭包含傳輸的全域資訊。 針對 (InterfaceTransport) 函式的用戶端，標頭包含用戶端特定的資訊 (例如，正在管理的 OSPF) 。

資訊標頭和其內容只能使用 [MprInfo](router-information-functions.md) 函式來操作。 開發人員不應該嘗試直接操作資訊標頭的內容。

僅介面函式（例如 [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) ）不需要使用 MprInfo 函式。 使用這些函式傳遞和傳回的資訊一律採用 [**MPR \_ 介面**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) 結構的形式。

 

 




