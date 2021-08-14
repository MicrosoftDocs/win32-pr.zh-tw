---
title: 路由器介面函式
description: 使用下列功能來管理路由器上的介面。
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcaaf257e31623036a075c21da66d4665b3afe7e821f8f246f6a225e02b8272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787834"
---
# <a name="router-interface-functions"></a>路由器介面函式

使用下列功能來管理路由器上的介面。



| 管理功能                                          | Configuration 函數                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [**MprConfigInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [**MprAdminInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [**MprConfigInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [**MprAdminInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [**MprConfigInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [**MprAdminInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [**MprConfigInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

這些函式會影響介面本身，而不會影響在介面上執行的用戶端。 基於這個理由，所有的函式都不需要呼叫端指定特定的傳輸 (IP 或 IPX) ;雖然用戶端 (例如路由通訊協定) 與特定傳輸相關聯，但介面本身並不是。

這些函式是由 DIM 直接處理。 它們不會利用路由器管理員。

[**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)和 [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)函數無法建立或刪除 LAN 介面。 它們只能建立或刪除指定撥號介面。 請參閱 [**路由器 \_ 介面 \_ 類型**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) ，以取得介面類別型清單。

 

 




