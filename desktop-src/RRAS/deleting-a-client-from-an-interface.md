---
title: 從介面刪除用戶端
description: 若要從特定介面刪除用戶端（例如路由通訊協定），請使用 MprAdminInterfaceTransportGetInfo 或 MprConfigInterfaceTransportGetInfo 來取得介面的所有用戶端資訊。
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585a37920b59f47a0c933427d7218d08a61bed9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932375"
---
# <a name="deleting-a-client-from-an-interface"></a><span data-ttu-id="0ca83-103">從介面刪除用戶端</span><span class="sxs-lookup"><span data-stu-id="0ca83-103">Deleting a Client from an Interface</span></span>

<span data-ttu-id="0ca83-104">若要從特定介面刪除用戶端（例如路由通訊協定），請使用 [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) 或 [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) 來取得介面的所有用戶端資訊。</span><span class="sxs-lookup"><span data-stu-id="0ca83-104">To delete a client, such as a routing protocol, from a particular interface, use either [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) or [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) to retrieve all the client information for the interface.</span></span> <span data-ttu-id="0ca83-105">使用 [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) 移除要刪除之用戶端的資訊區塊。</span><span class="sxs-lookup"><span data-stu-id="0ca83-105">Use [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) to remove the information block for the client to be deleted.</span></span> <span data-ttu-id="0ca83-106">然後使用 [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) 來新增零長度的區塊，以供要刪除的用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="0ca83-106">Then use [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) to add a zero-length block for the client to be deleted.</span></span> <span data-ttu-id="0ca83-107">最後，使用 [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) 或 [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) 將資訊儲存回正在執行的路由器或登錄中。</span><span class="sxs-lookup"><span data-stu-id="0ca83-107">Finally, use [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) or [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) to save the information back to either the running router or the registry.</span></span>

<span data-ttu-id="0ca83-108">如果路由器管理員收到用戶端的長度為零的介面資訊區塊，就會知道要從介面刪除該用戶端。</span><span class="sxs-lookup"><span data-stu-id="0ca83-108">If the router manager receives a zero-length interface information block for a client, it knows to delete that client from the interface.</span></span> <span data-ttu-id="0ca83-109">路由器管理員會藉由呼叫用戶端的 [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)執行來刪除用戶端。</span><span class="sxs-lookup"><span data-stu-id="0ca83-109">The router manager deletes the client by calling the client's implementation of [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface).</span></span> <span data-ttu-id="0ca83-110">請注意，傳遞不包含用戶端資訊區塊的資訊標頭，以及傳遞包含用戶端之零長度資訊區塊的資訊標頭，兩者之間的重要差異。</span><span class="sxs-lookup"><span data-stu-id="0ca83-110">Note the important distinction between passing an information header that does not contain an information block for a client, and passing an information header that contains a zero-length information block for the client.</span></span> <span data-ttu-id="0ca83-111">在第一種情況下，路由器管理員不會針對用戶端採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="0ca83-111">In the first case, the router manager takes no action with respect to the client.</span></span> <span data-ttu-id="0ca83-112">在第二種情況下，路由器管理員會從介面刪除用戶端。</span><span class="sxs-lookup"><span data-stu-id="0ca83-112">In the second case, the router manager deletes the client from the interface.</span></span>

 

 




