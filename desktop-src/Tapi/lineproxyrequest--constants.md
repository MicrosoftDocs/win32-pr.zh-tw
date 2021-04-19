---
description: 這些常數會在兩個內容中使用。
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: 'LINEPROXYREQUEST_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba34a3a7f7b1f41f0c32783c4132afcfafef1aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993597"
---
# <a name="lineproxyrequest_-constants"></a><span data-ttu-id="ebc40-103">LINEPROXYREQUEST \_ 常數</span><span class="sxs-lookup"><span data-stu-id="ebc40-103">LINEPROXYREQUEST\_ Constants</span></span>

<span data-ttu-id="ebc40-104">這些常數會在兩個內容中使用。</span><span class="sxs-lookup"><span data-stu-id="ebc40-104">These constants are used in two contexts.</span></span> <span data-ttu-id="ebc40-105">首先，您可以在指定 LINEOPENOPTION PROXY 選項時，在與 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)傳入的 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)結構中使用 **DWORD** 值陣列 \_ ，以指出應用程式願意處理哪些函數。</span><span class="sxs-lookup"><span data-stu-id="ebc40-105">First, they can be used in an array of **DWORD** values in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) when the LINEOPENOPTION\_PROXY option is specified, to indicate which functions the application is willing to handle.</span></span> <span data-ttu-id="ebc40-106">其次，在 [**行 \_ PROXYREQUEST**](line-proxyrequest.md) 中使用它們，並透過 **\_ PROXYREQUEST** 訊息來傳遞至處理常式應用程式，以指出要處理的要求類型，以及緩衝區中的資料格式。</span><span class="sxs-lookup"><span data-stu-id="ebc40-106">Second, they are used in the [**LINE\_PROXYREQUEST**](line-proxyrequest.md) passed to the handler application by a **LINE\_PROXYREQUEST** message to indicate the type of request that is to be processed and the format of the data in the buffer.</span></span>

<dl> <dt>

<span data-ttu-id="ebc40-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST \_ AGENTSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="ebc40-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST\_AGENTSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-108">與 [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-108">Associated with [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**LINEPROXYREQUEST \_ CREATEAGENT**</span><span class="sxs-lookup"><span data-stu-id="ebc40-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**LINEPROXYREQUEST\_CREATEAGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-110">與 [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-110">Associated with [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST \_ CREATEAGENTSESSION**</span><span class="sxs-lookup"><span data-stu-id="ebc40-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST\_CREATEAGENTSESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-112">與 [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-112">Associated with [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST**</span><span class="sxs-lookup"><span data-stu-id="ebc40-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST\_GETAGENTACTIVITYLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-114">與 [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-114">Associated with [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST \_ GETAGENTCAPS**</span><span class="sxs-lookup"><span data-stu-id="ebc40-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST\_GETAGENTCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-116">與 [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-116">Associated with [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST \_ GETAGENTGROUPLIST**</span><span class="sxs-lookup"><span data-stu-id="ebc40-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST\_GETAGENTGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-118">與 [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-118">Associated with [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST \_ GETAGENTINFO**</span><span class="sxs-lookup"><span data-stu-id="ebc40-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST\_GETAGENTINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-120">與 [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-120">Associated with [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="ebc40-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-122">與 [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-122">Associated with [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONLIST**</span><span class="sxs-lookup"><span data-stu-id="ebc40-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-124">與 [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-124">Associated with [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST \_ GETAGENTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="ebc40-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST\_GETAGENTSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-126">與 [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-126">Associated with [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST \_ GETGROUPLIST**</span><span class="sxs-lookup"><span data-stu-id="ebc40-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST\_GETGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-128">與 [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-128">Associated with [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST \_ GETQUEUEINFO**</span><span class="sxs-lookup"><span data-stu-id="ebc40-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST\_GETQUEUEINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-130">與 [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-130">Associated with [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST \_ GETQUEUELIST**</span><span class="sxs-lookup"><span data-stu-id="ebc40-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST\_GETQUEUELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-132">與 [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-132">Associated with [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST \_ SETAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="ebc40-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST\_SETAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-134">與 [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-134">Associated with [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST \_ SETAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="ebc40-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST\_SETAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-136">與 [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-136">Associated with [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD**</span><span class="sxs-lookup"><span data-stu-id="ebc40-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-138">與 [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-138">Associated with [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE**</span><span class="sxs-lookup"><span data-stu-id="ebc40-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST\_SETAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-140">與 [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-140">Associated with [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST \_ SETAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="ebc40-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST\_SETAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-142">與 [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-142">Associated with [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST \_ SETAGENTSTATEEX**</span><span class="sxs-lookup"><span data-stu-id="ebc40-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST\_SETAGENTSTATEEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-144">與 [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-144">Associated with [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc40-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD**</span><span class="sxs-lookup"><span data-stu-id="ebc40-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc40-146">與 [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod)相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebc40-146">Associated with [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebc40-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebc40-147">Requirements</span></span>



| <span data-ttu-id="ebc40-148">需求</span><span class="sxs-lookup"><span data-stu-id="ebc40-148">Requirement</span></span> | <span data-ttu-id="ebc40-149">值</span><span class="sxs-lookup"><span data-stu-id="ebc40-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ebc40-150">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ebc40-150">TAPI version</span></span><br/> | <span data-ttu-id="ebc40-151">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ebc40-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ebc40-152">標頭</span><span class="sxs-lookup"><span data-stu-id="ebc40-152">Header</span></span><br/>       | <dl> <span data-ttu-id="ebc40-153"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="ebc40-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebc40-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebc40-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc40-155">撥置中心常數</span><span class="sxs-lookup"><span data-stu-id="ebc40-155">Call Center Constants</span></span>](call-center-constants.md)
</dt> <dt>

[<span data-ttu-id="ebc40-156">撥置中心函數</span><span class="sxs-lookup"><span data-stu-id="ebc40-156">Call Center Functions</span></span>](call-center-functions.md)
</dt> </dl>

 

 




