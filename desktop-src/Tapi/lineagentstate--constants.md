---
description: LINEAGENTSTATE \_ 常數描述某個位址上代理程式的狀態。
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: 'LINEAGENTSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984864"
---
# <a name="lineagentstate_-constants"></a><span data-ttu-id="0eea9-103">LINEAGENTSTATE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="0eea9-103">LINEAGENTSTATE\_ Constants</span></span>

<span data-ttu-id="0eea9-104">**LINEAGENTSTATE \_ 常數** 描述某個位址上代理程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="0eea9-104">The **LINEAGENTSTATE\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="0eea9-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE \_ BUSYACD**</span><span class="sxs-lookup"><span data-stu-id="0eea9-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-106">代理程式正忙於處理從 ACD 佇列路由傳送的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0eea9-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0eea9-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE \_ BUSYINCOMING**</span><span class="sxs-lookup"><span data-stu-id="0eea9-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-108">代理程式正忙於處理未從代理程式登入的 ACD 佇列傳送至代理程式的撥入電話。</span><span class="sxs-lookup"><span data-stu-id="0eea9-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0eea9-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE \_ BUSYOTHER**</span><span class="sxs-lookup"><span data-stu-id="0eea9-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE\_BUSYOTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-110">代理程式正忙於處理另一種類型的呼叫，例如，預測撥號程式未傳送給代理程式的外寄個人呼叫。</span><span class="sxs-lookup"><span data-stu-id="0eea9-110">The agent is busy handling another type of call, such as an outgoing personal call not transferred to the agent by a predictive dialer.</span></span> <span data-ttu-id="0eea9-111">當已知代理程式在呼叫上忙碌，但呼叫的類型未知時，也可以使用此值。</span><span class="sxs-lookup"><span data-stu-id="0eea9-111">This value can also be used when the agent is known to be busy on a call but the type of call is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0eea9-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE \_ BUSYOUTBOUND**</span><span class="sxs-lookup"><span data-stu-id="0eea9-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE\_BUSYOUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-113">代理程式正忙於處理外寄呼叫，例如從預測撥號佇列路由傳送的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0eea9-113">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0eea9-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE \_ LOGGEDOFF**</span><span class="sxs-lookup"><span data-stu-id="0eea9-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE\_LOGGEDOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-115">位址上未登入任何代理程式。</span><span class="sxs-lookup"><span data-stu-id="0eea9-115">No agent is logged in on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0eea9-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ NOTREADY**</span><span class="sxs-lookup"><span data-stu-id="0eea9-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-117">代理程式已登入，但使用的工作不是服務呼叫 (例如在中斷) 上。</span><span class="sxs-lookup"><span data-stu-id="0eea9-117">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="0eea9-118">不應將其他呼叫路由傳送至代理程式。</span><span class="sxs-lookup"><span data-stu-id="0eea9-118">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0eea9-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ 就緒**</span><span class="sxs-lookup"><span data-stu-id="0eea9-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-120">代理程式已準備好接受呼叫。</span><span class="sxs-lookup"><span data-stu-id="0eea9-120">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0eea9-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="0eea9-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-122">代理程式狀態未知，而且永遠不會變成已知。</span><span class="sxs-lookup"><span data-stu-id="0eea9-122">The agent state is unknown and will never become known.</span></span> <span data-ttu-id="0eea9-123">在 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)中，這個條件也可以由設定為0的 **dwAgentState** 成員表示。</span><span class="sxs-lookup"><span data-stu-id="0eea9-123">In [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), this condition can also be represented by the **dwAgentState** member being set to 0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0eea9-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="0eea9-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-125">代理程式狀態目前是未知的，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="0eea9-125">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="0eea9-126">這可以是第一次開啟行或位址時的過渡狀態。</span><span class="sxs-lookup"><span data-stu-id="0eea9-126">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0eea9-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE \_ WORKINGAFTERCALL**</span><span class="sxs-lookup"><span data-stu-id="0eea9-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE\_WORKINGAFTERCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0eea9-128">代理程式已完成先前的呼叫，但仍佔用與該呼叫相關的工作。</span><span class="sxs-lookup"><span data-stu-id="0eea9-128">The agent has completed the preceding call, but is still occupied with work related to that call.</span></span> <span data-ttu-id="0eea9-129">代理程式應該不會收到額外的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0eea9-129">The agent should not receive additional calls.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0eea9-130">備註</span><span class="sxs-lookup"><span data-stu-id="0eea9-130">Remarks</span></span>

<span data-ttu-id="0eea9-131">這組常數的上層16位會保留給裝置專屬的擴充。</span><span class="sxs-lookup"><span data-stu-id="0eea9-131">The upper 16 bits of this set of constants are reserved for device-specific extensions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eea9-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="0eea9-132">Requirements</span></span>



| <span data-ttu-id="0eea9-133">需求</span><span class="sxs-lookup"><span data-stu-id="0eea9-133">Requirement</span></span> | <span data-ttu-id="0eea9-134">值</span><span class="sxs-lookup"><span data-stu-id="0eea9-134">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0eea9-135">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="0eea9-135">TAPI version</span></span><br/> | <span data-ttu-id="0eea9-136">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0eea9-136">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0eea9-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0eea9-137">Header</span></span><br/>       | <dl> <span data-ttu-id="0eea9-138"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="0eea9-138"><dt>Tapi.h</dt></span></span> </dl> |



 

 




