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
# <a name="processing-groups-and-callbacks"></a>處理群組和回呼

下表摘要說明路由通訊協定與多播群組管理員之間操作互動的一連串步驟。 第一個資料行描述路由通訊協定執行的動作，以及路由通訊協定對多播群組管理員的回應。 第二個數據行描述多播群組管理員對路由通訊協定的回應，以及多播群組管理員執行的任何動作，例如回呼。 第三個數據行顯示任何其他資訊。

資料表的每個資料列都代表一個步驟。

此資料表中所列的工作不會以任何特定順序出現;相反地，它們會根據多播群組成員資格的狀態進行。 下表顯示範例順序。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>路由通訊協定動作</th>
<th>多播群組管理員動作</th>
<th>備註</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>根據通訊協定所擁有的介面上收到的通訊協定資訊來管理群組成員資格。 管理會使用下列功能來執行：
<ul>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></li>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></li>
</ul></td>
<td>從指定的 (s、g) 、 (*、g) 和 (*、* ) 專案的輸出介面清單中新增和刪除。 這份清單表示轉送此群組之資料的介面集。 此群組的資料來自指定的來源。</td>

</tr>
<tr class="even">

<td>以回呼的形式將警示傳送至路由通訊協定。 下列事件會觸發多播群組管理員來叫用回呼：
<ul>
<li>加入或離開群組 ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a> <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>) 。</li>
<li>群組成員資格由 IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a> <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>) 變更。</li>
<li>在錯誤的介面上收到的資料 ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>) 。</li>
<li>從新來源或新群組接收的資料 ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> 和 <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>) 。</li>
</ul></td>
<td>使用這些回呼時，當路由器上有數個多播路由通訊協定時，多播群組管理員能夠協調封包轉送。</td>
</tr>
<tr class="odd">
<td>使用 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>、 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>和 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> 函數，列舉 (MFEs) 的多播轉送專案。 根據列舉的結果，進行多播資料的決定。</td>
<td>傳回要求的 MFEs。 當沒有其他 MFEs 要傳回時，傳回 ERROR_NO_MORE 專案。<br/></td>
<td>使用 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>、 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>、 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> 函數來列舉 MFE 統計資料。 如需使用這些函數的完整範例，請參閱系統 <a href="administrative-application-scenario.md">管理應用程式案例</a> 。<br/></td>
</tr>
<tr class="even">
<td>使用 <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> 函式修改 MFE 中的上游相鄰。</td>

<td>用戶端會使用此函數來修改連入介面的相關資訊。</td>
</tr>
</tbody>
</table>



 

 

