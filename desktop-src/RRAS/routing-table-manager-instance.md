---
title: 路由表管理員實例
description: 實例是另一個資料表，路由表管理員會使用此資料表來維護有關介面子集的路由資訊。
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d209f254bb9111c786bde6635b43895604785d5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021350"
---
# <a name="routing-table-manager-instance"></a><span data-ttu-id="fdf42-103">路由表管理員實例</span><span class="sxs-lookup"><span data-stu-id="fdf42-103">Routing Table Manager Instance</span></span>

<span data-ttu-id="fdf42-104">實例是另一個資料表，路由表管理員會使用此資料表來維護有關介面子集的路由資訊。</span><span class="sxs-lookup"><span data-stu-id="fdf42-104">An instance is a separate table that the routing table manager uses to maintain routing information about a subset of interfaces.</span></span> <span data-ttu-id="fdf42-105">實例通常用來讓實體路由器作為一組虛擬路由器，也就是每個邏輯網路一個虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="fdf42-105">Instances are typically used to enable a physical router to act as a set of virtual routers – one virtual router per logical network.</span></span>

<span data-ttu-id="fdf42-106">路由表管理員目前只支援一個實例 (識別為零，預設) 。</span><span class="sxs-lookup"><span data-stu-id="fdf42-106">Currently, the routing table manager supports only one instance (identified as zero, the default).</span></span> <span data-ttu-id="fdf42-107">用戶端可以向其他實例註冊，但是除了預設的路由器之外，路由器管理員可辨識或使用它以外的虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="fdf42-107">The client can register with other instances, but no virtual router except the default one is recognized or used by the router manager.</span></span>

 

 




