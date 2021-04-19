---
description: LINEAGENTSTATEEX \_ 常數描述某個位址上代理程式的狀態。
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: 'LINEAGENTSTATEEX_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001201"
---
# <a name="lineagentstateex_-constants"></a><span data-ttu-id="8c999-103">LINEAGENTSTATEEX \_ 常數</span><span class="sxs-lookup"><span data-stu-id="8c999-103">LINEAGENTSTATEEX\_ Constants</span></span>

<span data-ttu-id="8c999-104">**LINEAGENTSTATEEX \_ 常數** 描述某個位址上代理程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="8c999-104">The **LINEAGENTSTATEEX\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="8c999-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**</span><span class="sxs-lookup"><span data-stu-id="8c999-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c999-106">代理程式正忙於處理從 ACD 佇列路由傳送的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8c999-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c999-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**</span><span class="sxs-lookup"><span data-stu-id="8c999-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c999-108">代理程式正忙於處理未從代理程式登入的 ACD 佇列傳送至代理程式的撥入電話。</span><span class="sxs-lookup"><span data-stu-id="8c999-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c999-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**</span><span class="sxs-lookup"><span data-stu-id="8c999-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX\_BUSYOUTGOING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c999-110">代理程式正忙於處理外寄呼叫，例如從預測撥號佇列路由傳送的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8c999-110">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c999-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOTREADY**</span><span class="sxs-lookup"><span data-stu-id="8c999-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c999-112">代理程式已登入，但使用的工作不是服務呼叫 (例如在中斷) 上。</span><span class="sxs-lookup"><span data-stu-id="8c999-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="8c999-113">不應將其他呼叫路由傳送至代理程式。</span><span class="sxs-lookup"><span data-stu-id="8c999-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c999-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ 就緒**</span><span class="sxs-lookup"><span data-stu-id="8c999-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c999-115">代理程式已準備好接受呼叫。</span><span class="sxs-lookup"><span data-stu-id="8c999-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c999-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX 已 \_ 發行**</span><span class="sxs-lookup"><span data-stu-id="8c999-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c999-117">代理程式已經發行，可能是因為它們已登出。</span><span class="sxs-lookup"><span data-stu-id="8c999-117">The agent has been released, probably because they logged off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c999-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="8c999-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c999-119">代理程式狀態目前是未知的，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="8c999-119">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="8c999-120">這可以是第一次開啟行或位址時的過渡狀態。</span><span class="sxs-lookup"><span data-stu-id="8c999-120">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c999-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c999-121">Requirements</span></span>



| <span data-ttu-id="8c999-122">需求</span><span class="sxs-lookup"><span data-stu-id="8c999-122">Requirement</span></span> | <span data-ttu-id="8c999-123">值</span><span class="sxs-lookup"><span data-stu-id="8c999-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8c999-124">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="8c999-124">TAPI version</span></span><br/> | <span data-ttu-id="8c999-125">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="8c999-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="8c999-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8c999-126">Header</span></span><br/>       | <dl> <span data-ttu-id="8c999-127"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="8c999-127"><dt>Tapi.h</dt></span></span> </dl> |



 

 




