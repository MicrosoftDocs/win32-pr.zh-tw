---
title: 變更用戶端的 Interface-Specific 和全域資訊
description: 若要變更特定用戶端（例如 NAT）的介面資訊，請先使用適當的 \ 0034;GetInfo \ 0034;用來取得目前資訊的函式。
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c8f2ef3c37d75db1cc7686a67108530b16b28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932214"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>變更用戶端的 Interface-Specific 和全域資訊

若要變更特定用戶端（例如 NAT）的介面資訊，請先使用適當的 "GetInfo" 函式來取得目前的資訊。 如果路由器正在執行，請使用 [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo)。 如果路由器未執行，請使用 [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo)。 此呼叫會取得在指定介面上執行之所有用戶端的資訊。 例如，如果 OSPF 和 RIP 都在特定介面上執行，此呼叫會同時抓取這兩者的介面資訊。 您可以使用 [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) 函式，找出對應至您要修改之用戶端的資訊區塊。 然後使用 [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) 函式來執行修改。 最後，使用 [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) 或 [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) 對登錄中的執行中路由器或路由器設定進行變更。

全域用戶端資訊是指不是用戶端執行所在的任何特定介面的相關資訊。 您可以使用類似的程式來修改特定用戶端的全域資訊。 首先，使用 [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) 或 [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)來取得所有用戶端的全域資訊。 然後使用 MprInfo 函數來修改資訊。 最後，使用 [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) 或 [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) 函數，將修改過的資訊儲存回執行中的路由器或登錄。

對上述管理函式的呼叫會透過動態介面管理員 (維度) ，最後轉譯成從路由器管理員到用戶端本身的呼叫。 無論用戶端是否為路由通訊協定，所有用戶端都必須符合 [路由器通訊協定介面](about-routing-protocol-interface.md)一節中所述的介面。 作為此介面的一部分，路由通訊協定必須支援下列函式 () 的其他功能：

-   [**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

路由器管理員會為每個用戶端呼叫 [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) 函式，以收集從呼叫 [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo)所傳回的資訊。 同樣地，當路由器管理員透過 [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) 呼叫接收更新的資訊時，它會使用 [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) 函式來更新每個用戶端的介面資訊。

 

 




