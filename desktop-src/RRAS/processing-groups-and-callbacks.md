---
title: 處理群組和回呼
description: 下表摘要說明路由通訊協定與多播群組管理員之間操作互動的一連串步驟。
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316636"
---
# <a name="processing-groups-and-callbacks"></a><span data-ttu-id="a5431-103">處理群組和回呼</span><span class="sxs-lookup"><span data-stu-id="a5431-103">Processing Groups and Callbacks</span></span>

<span data-ttu-id="a5431-104">下表摘要說明路由通訊協定與多播群組管理員之間操作互動的一連串步驟。</span><span class="sxs-lookup"><span data-stu-id="a5431-104">The following table summarizes a series of steps in an operational interaction between a routing protocol and the multicast group manager.</span></span> <span data-ttu-id="a5431-105">第一個資料行描述路由通訊協定執行的動作，以及路由通訊協定對多播群組管理員的回應。</span><span class="sxs-lookup"><span data-stu-id="a5431-105">The first column describes the actions that the routing protocol performs and the routing protocol's responses to the multicast group manager.</span></span> <span data-ttu-id="a5431-106">第二個數據行描述多播群組管理員對路由通訊協定的回應，以及多播群組管理員執行的任何動作，例如回呼。</span><span class="sxs-lookup"><span data-stu-id="a5431-106">The second column describes the multicast group manager's responses to the routing protocol and any actions the multicast group manager performs such as callbacks.</span></span> <span data-ttu-id="a5431-107">第三個數據行顯示任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="a5431-107">The third column presents any additional information.</span></span>

<span data-ttu-id="a5431-108">資料表的每個資料列都代表一個步驟。</span><span class="sxs-lookup"><span data-stu-id="a5431-108">Each row of the table represents one step.</span></span>

<span data-ttu-id="a5431-109">此資料表中所列的工作不會以任何特定順序出現;相反地，它們會根據多播群組成員資格的狀態進行。</span><span class="sxs-lookup"><span data-stu-id="a5431-109">The tasks listed in this table do not occur in any specific order; rather, they occur based on the status of multicast group memberships.</span></span> <span data-ttu-id="a5431-110">下表顯示範例順序。</span><span class="sxs-lookup"><span data-stu-id="a5431-110">The table below shows an example order.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5431-111">路由通訊協定動作</span><span class="sxs-lookup"><span data-stu-id="a5431-111">Routing protocol action</span></span></th>
<th><span data-ttu-id="a5431-112">多播群組管理員動作</span><span class="sxs-lookup"><span data-stu-id="a5431-112">Multicast group manager action</span></span></th>
<th><span data-ttu-id="a5431-113">備註</span><span class="sxs-lookup"><span data-stu-id="a5431-113">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5431-114">根據通訊協定所擁有的介面上收到的通訊協定資訊來管理群組成員資格。</span><span class="sxs-lookup"><span data-stu-id="a5431-114">Manage group memberships based on protocol information received on those interfaces that the protocol owns.</span></span> <span data-ttu-id="a5431-115">管理會使用下列功能來執行：</span><span class="sxs-lookup"><span data-stu-id="a5431-115">Management is performed using the following functions:</span></span>
<ul>
<li><span data-ttu-id="a5431-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="a5431-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span></span></li>
<li><span data-ttu-id="a5431-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="a5431-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="a5431-118">從指定的 (s、g) 、 (*、g) 和 (*、\* ) 專案的輸出介面清單中新增和刪除。</span><span class="sxs-lookup"><span data-stu-id="a5431-118">Add to and delete from the outgoing interface list for the specified (s, g), (*, g), and (*, \*) entries.</span></span> <span data-ttu-id="a5431-119">這份清單表示轉送此群組之資料的介面集。</span><span class="sxs-lookup"><span data-stu-id="a5431-119">This list represents the set of interfaces on which data for this group is forwarded.</span></span> <span data-ttu-id="a5431-120">此群組的資料來自指定的來源。</span><span class="sxs-lookup"><span data-stu-id="a5431-120">The data for this group is from the specified source.</span></span></td>

</tr>
<tr class="even">

<td><span data-ttu-id="a5431-121">以回呼的形式將警示傳送至路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a5431-121">Send alerts to routing protocols in the form of callbacks.</span></span> <span data-ttu-id="a5431-122">下列事件會觸發多播群組管理員來叫用回呼：</span><span class="sxs-lookup"><span data-stu-id="a5431-122">The following events trigger the multicast group manager to invoke a callback:</span></span>
<ul>
<li><span data-ttu-id="a5431-123">加入或離開群組 ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a> <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="a5431-123">Join or leave groups ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="a5431-124">群組成員資格由 IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a> <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>) 變更。</span><span class="sxs-lookup"><span data-stu-id="a5431-124">Group membership changed by IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="a5431-125">在錯誤的介面上收到的資料 ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="a5431-125">Data received on wrong interface ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="a5431-126">從新來源或新群組接收的資料 ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> 和 <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="a5431-126">Data received from new sources or to a new group ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> and <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span></span></li>
</ul></td>
<td><span data-ttu-id="a5431-127">使用這些回呼時，當路由器上有數個多播路由通訊協定時，多播群組管理員能夠協調封包轉送。</span><span class="sxs-lookup"><span data-stu-id="a5431-127">Using these callbacks, the multicast group manager is able to coordinate packet forwarding when several multicast routing protocols are present on a router.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5431-128">使用 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>、 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>和 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> 函數，列舉 (MFEs) 的多播轉送專案。</span><span class="sxs-lookup"><span data-stu-id="a5431-128">Enumerate the multicast forwarding entries (MFEs), using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>, and <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> functions.</span></span> <span data-ttu-id="a5431-129">根據列舉的結果，進行多播資料的決定。</span><span class="sxs-lookup"><span data-stu-id="a5431-129">Make decisions about multicast data based on the results of the enumeration.</span></span></td>
<td><span data-ttu-id="a5431-130">傳回要求的 MFEs。</span><span class="sxs-lookup"><span data-stu-id="a5431-130">Return the requested MFEs.</span></span> <span data-ttu-id="a5431-131">當沒有其他 MFEs 要傳回時，傳回 ERROR_NO_MORE 專案。</span><span class="sxs-lookup"><span data-stu-id="a5431-131">Return ERROR_NO_MORE ITEMS when there are no more MFEs to return.</span></span><br/></td>
<td><span data-ttu-id="a5431-132">使用 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>、 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>、 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> 函數來列舉 MFE 統計資料。</span><span class="sxs-lookup"><span data-stu-id="a5431-132">Use the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> functions to enumerate MFE statistics.</span></span> <span data-ttu-id="a5431-133">如需使用這些函數的完整範例，請參閱系統 <a href="administrative-application-scenario.md">管理應用程式案例</a> 。</span><span class="sxs-lookup"><span data-stu-id="a5431-133">See <a href="administrative-application-scenario.md">Administrative Application Scenario</a> for a complete example of using these functions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5431-134">使用 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> 函式修改 MFE 中的上游相鄰。</span><span class="sxs-lookup"><span data-stu-id="a5431-134">Modify the upstream neighbor in an MFE using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> function.</span></span></td>

<td><span data-ttu-id="a5431-135">用戶端會使用此函數來修改連入介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5431-135">Clients use this function to modify the information regarding the incoming interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

