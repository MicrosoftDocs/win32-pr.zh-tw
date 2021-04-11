---
title: 本地離開回呼
description: 當 IGMP 通知多播群組管理員之後，介面上的群組沒有其他接收者存在時，多播群組管理員會叫用該 \_ \_ 介面上的路由通訊協定的 PMGM 本地離開回呼回呼（如果有的話） \_ 。 此回呼會通知路由通訊協定的變更。
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98d32e041b048e15497bc7fe35d17628b9331d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021662"
---
# <a name="local-leave-callbacks"></a><span data-ttu-id="5d491-104">本地離開回呼</span><span class="sxs-lookup"><span data-stu-id="5d491-104">Local Leave Callbacks</span></span>

<span data-ttu-id="5d491-105">當 IGMP 通知多播群組管理員之後，介面上的群組沒有其他接收者存在時，多播群組管理員會叫用該介面上的路由通訊協定的 [**PMGM \_ 本地 \_ 離開 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) 回呼（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="5d491-105">After the multicast group manager is notified by IGMP that there are no more receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback to the routing protocol on that interface if one exists.</span></span> <span data-ttu-id="5d491-106">此回呼會通知路由通訊協定的變更。</span><span class="sxs-lookup"><span data-stu-id="5d491-106">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="5d491-107">此回呼和 [**PMGM 的 \_ 本機 \_ 聯結 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) 回呼會用來同步處理 IGMP 和路由通訊協定之間的轉送。</span><span class="sxs-lookup"><span data-stu-id="5d491-107">This callback and the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




