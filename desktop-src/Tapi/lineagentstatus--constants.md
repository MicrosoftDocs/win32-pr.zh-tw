---
description: LINEAGENTSTATUS \_ 常數會列出代理程式之 LINEAGENTSTATUS 結構的成員更新狀態。
ms.assetid: 068a2b24-a430-4cf5-b70d-5574e981a899
title: 'LINEAGENTSTATUS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1fb7afb2703a50d97d0423662a10c92743beb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996081"
---
# <a name="lineagentstatus_-constants"></a>LINEAGENTSTATUS \_ 常數

**LINEAGENTSTATUS \_ 常數** 會列出代理程式之 [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)結構的成員更新狀態。

<dl> <dt>

<span id="LINEAGENTSTATUS_ACTIVITY"></span><span id="lineagentstatus_activity"></span>**LINEAGENTSTATUS \_ 活動**
</dt> <dd> <dl> <dt>



[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)中的 **dwActivityID**、 **dwActivitySize** 或 **dwActivityOffset** 成員已更新。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_ACTIVITYLIST"></span><span id="lineagentstatus_activitylist"></span>**LINEAGENTSTATUS \_ ACTIVITYLIST**
</dt> <dd> <dl> <dt>



[**LINEAGENTACTIVITYLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentactivitylist)已更新。 應用程式可以呼叫 [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) 來取得更新的清單。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_CAPSCHANGE"></span><span id="lineagentstatus_capschange"></span>**LINEAGENTSTATUS \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)中的功能已更新。 應用程式可以呼叫 [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa) 來取得更新的清單。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUP"></span><span id="lineagentstatus_group"></span>**LINEAGENTSTATUS \_ 群組**
</dt> <dd> <dl> <dt>



[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)已更新。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUPLIST"></span><span id="lineagentstatus_grouplist"></span>**LINEAGENTSTATUS \_ GROUPLIST**
</dt> <dd> <dl> <dt>



[**LINEAGENTGROUPLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentgrouplist)已更新。 應用程式可以呼叫 [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista) 來取得更新的清單。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_NEXTSTATE"></span><span id="lineagentstatus_nextstate"></span>**LINEAGENTSTATUS \_ NEXTSTATE**
</dt> <dd> <dl> <dt>



[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)中的 **dwNextState** 成員已更新。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_STATE"></span><span id="lineagentstatus_state"></span>**LINEAGENTSTATUS \_ 狀態**
</dt> <dd> <dl> <dt>



[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)中的 **dwState** 成員已更新。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDNEXTSTATES"></span><span id="lineagentstatus_validnextstates"></span>**LINEAGENTSTATUS \_ VALIDNEXTSTATES**
</dt> <dd> <dl> <dt>



[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)中的 **dwValidNextStates** 成員已更新。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDSTATES"></span><span id="lineagentstatus_validstates"></span>**LINEAGENTSTATUS \_ VALIDSTATES**
</dt> <dd> <dl> <dt>



[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)中的 **dwValidStates** 成員已更新。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINEAGENTACTIVITYLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentactivitylist)
</dt> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**LINEAGENTGROUPLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentgrouplist)
</dt> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista)
</dt> <dt>

[**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)
</dt> <dt>

[**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)
</dt> </dl>

 

 




