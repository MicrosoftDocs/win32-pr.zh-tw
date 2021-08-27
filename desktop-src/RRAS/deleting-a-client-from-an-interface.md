---
title: 從介面刪除用戶端
description: 若要從特定介面刪除用戶端（例如路由通訊協定），請使用 MprAdminInterfaceTransportGetInfo 或 MprConfigInterfaceTransportGetInfo 來取得介面的所有用戶端資訊。
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e5b93e062f5971f6e43ad1d7c08f7a0c2ef3bff72e66849815a053b342b13b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127888"
---
# <a name="deleting-a-client-from-an-interface"></a>從介面刪除用戶端

若要從特定介面刪除用戶端（例如路由通訊協定），請使用 [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) 或 [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) 來取得介面的所有用戶端資訊。 使用 [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) 移除要刪除之用戶端的資訊區塊。 然後使用 [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) 來新增零長度的區塊，以供要刪除的用戶端使用。 最後，使用 [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) 或 [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) 將資訊儲存回正在執行的路由器或登錄中。

如果路由器管理員收到用戶端的長度為零的介面資訊區塊，就會知道要從介面刪除該用戶端。 路由器管理員會藉由呼叫用戶端的 [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)執行來刪除用戶端。 請注意，傳遞不包含用戶端資訊區塊的資訊標頭，以及傳遞包含用戶端之零長度資訊區塊的資訊標頭，兩者之間的重要差異。 在第一種情況下，路由器管理員不會針對用戶端採取任何動作。 在第二種情況下，路由器管理員會從介面刪除用戶端。

 

 




