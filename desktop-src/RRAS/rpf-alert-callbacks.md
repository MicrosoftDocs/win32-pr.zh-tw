---
title: RPF 警示回呼
description: 當多播群組管理員收到來自新來源的封包或來自新群組的封包的通知之後，多播群組管理員會在路由表的多播視圖中查閱來源的路由。
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675976"
---
# <a name="rpf-alert-callbacks"></a><span data-ttu-id="1722b-103">RPF 警示回呼</span><span class="sxs-lookup"><span data-stu-id="1722b-103">RPF Alert Callbacks</span></span>

<span data-ttu-id="1722b-104">當多播群組管理員收到來自新來源的封包或來自新群組的封包的通知之後，多播群組管理員會在路由表的多播視圖中查閱來源的路由。</span><span class="sxs-lookup"><span data-stu-id="1722b-104">After the multicast group manager receives notification of a packet from a new source or of a packet that is destined for a new group, the multicast group manager looks up the route to the source in the multicast view of the routing table.</span></span> <span data-ttu-id="1722b-105">然後，多播群組管理員會叫用 [**PMGM \_ RPF \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) 回呼給擁有資料抵達介面的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1722b-105">The multicast group manager then invokes the [**PMGM\_RPF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) callback to the protocol that owns the interface the data arrived on.</span></span>

<span data-ttu-id="1722b-106">叫用此回呼之後，如果路由通訊協定必須在不同的介面上接收群組的資料，路由通訊協定就可以變更傳入的介面。</span><span class="sxs-lookup"><span data-stu-id="1722b-106">After this callback is invoked, the routing protocol can change the incoming interface if the routing protocol must receive the data for the group on a different interface.</span></span>

 

 




