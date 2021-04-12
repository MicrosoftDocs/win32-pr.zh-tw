---
title: 路由器介面函式
description: 使用下列功能來管理路由器上的介面。
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104299995"
---
# <a name="router-interface-functions"></a><span data-ttu-id="84e15-103">路由器介面函式</span><span class="sxs-lookup"><span data-stu-id="84e15-103">Router Interface Functions</span></span>

<span data-ttu-id="84e15-104">使用下列功能來管理路由器上的介面。</span><span class="sxs-lookup"><span data-stu-id="84e15-104">Use the following functions to administer interfaces on the router.</span></span>



| <span data-ttu-id="84e15-105">管理功能</span><span class="sxs-lookup"><span data-stu-id="84e15-105">Administration Function</span></span>                                          | <span data-ttu-id="84e15-106">Configuration 函數</span><span class="sxs-lookup"><span data-stu-id="84e15-106">Configuration Function</span></span>                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="84e15-107">**MprAdminInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="84e15-107">**MprAdminInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [<span data-ttu-id="84e15-108">**MprConfigInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="84e15-108">**MprConfigInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [<span data-ttu-id="84e15-109">**MprAdminInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="84e15-109">**MprAdminInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [<span data-ttu-id="84e15-110">**MprConfigInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="84e15-110">**MprConfigInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [<span data-ttu-id="84e15-111">**MprAdminInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="84e15-111">**MprAdminInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [<span data-ttu-id="84e15-112">**MprConfigInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="84e15-112">**MprConfigInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [<span data-ttu-id="84e15-113">**MprAdminInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="84e15-113">**MprAdminInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [<span data-ttu-id="84e15-114">**MprConfigInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="84e15-114">**MprConfigInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [<span data-ttu-id="84e15-115">**MprAdminInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="84e15-115">**MprAdminInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [<span data-ttu-id="84e15-116">**MprConfigInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="84e15-116">**MprConfigInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [<span data-ttu-id="84e15-117">**MprAdminInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="84e15-117">**MprAdminInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [<span data-ttu-id="84e15-118">**MprConfigInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="84e15-118">**MprConfigInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

<span data-ttu-id="84e15-119">這些函式會影響介面本身，而不會影響在介面上執行的用戶端。</span><span class="sxs-lookup"><span data-stu-id="84e15-119">These functions affect the interfaces themselves, not clients running on the interfaces.</span></span> <span data-ttu-id="84e15-120">基於這個理由，所有的函式都不需要呼叫端指定特定的傳輸 (IP 或 IPX) ;雖然用戶端 (例如路由通訊協定) 與特定傳輸相關聯，但介面本身並不是。</span><span class="sxs-lookup"><span data-stu-id="84e15-120">For this reason, none of the functions require the caller to specify a particular transport (IP or IPX); although clients (such as routing protocols) are associated with particular transports, the interfaces themselves are not.</span></span>

<span data-ttu-id="84e15-121">這些函式是由 DIM 直接處理。</span><span class="sxs-lookup"><span data-stu-id="84e15-121">These functions are handled directly by DIM.</span></span> <span data-ttu-id="84e15-122">它們不會利用路由器管理員。</span><span class="sxs-lookup"><span data-stu-id="84e15-122">They do not utilize the router managers.</span></span>

<span data-ttu-id="84e15-123">[**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)和 [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)函數無法建立或刪除 LAN 介面。</span><span class="sxs-lookup"><span data-stu-id="84e15-123">The [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) and [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) functions cannot create or delete LAN interfaces.</span></span> <span data-ttu-id="84e15-124">它們只能建立或刪除指定撥號介面。</span><span class="sxs-lookup"><span data-stu-id="84e15-124">They can only create or delete demand-dial interfaces.</span></span> <span data-ttu-id="84e15-125">請參閱 [**路由器 \_ 介面 \_ 類型**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) ，以取得介面類別型清單。</span><span class="sxs-lookup"><span data-stu-id="84e15-125">See [**ROUTER\_INTERFACE\_TYPE**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) for a list of interface types.</span></span>

 

 




