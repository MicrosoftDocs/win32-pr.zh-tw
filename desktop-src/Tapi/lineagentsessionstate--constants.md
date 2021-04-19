---
description: LINEAGENTSESSIONSTATE \_ 常數描述各種代理程式會話狀態。
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: 'LINEAGENTSESSIONSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981628"
---
# <a name="lineagentsessionstate_-constants"></a><span data-ttu-id="9c9d7-103">LINEAGENTSESSIONSTATE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="9c9d7-103">LINEAGENTSESSIONSTATE\_ Constants</span></span>

<span data-ttu-id="9c9d7-104">**LINEAGENTSESSIONSTATE \_ 常數** 描述各種代理程式會話狀態。</span><span class="sxs-lookup"><span data-stu-id="9c9d7-104">The **LINEAGENTSESSIONSTATE\_ constants** describe various agent session states.</span></span>

<dl> <dt>

<span data-ttu-id="9c9d7-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE \_ BUSYONCALL**</span><span class="sxs-lookup"><span data-stu-id="9c9d7-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE\_BUSYONCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c9d7-106">代理程式正忙於處理呼叫。</span><span class="sxs-lookup"><span data-stu-id="9c9d7-106">The agent is busy handling a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c9d7-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE \_ BUSYWRAPUP**</span><span class="sxs-lookup"><span data-stu-id="9c9d7-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE\_BUSYWRAPUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c9d7-108">代理程式正忙於處理呼叫的包裝。</span><span class="sxs-lookup"><span data-stu-id="9c9d7-108">The agent is busy handling the wrap-up of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c9d7-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="9c9d7-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE\_ENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c9d7-110">代理程式會話已結束。</span><span class="sxs-lookup"><span data-stu-id="9c9d7-110">The agent session has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c9d7-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ NOTREADY**</span><span class="sxs-lookup"><span data-stu-id="9c9d7-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c9d7-112">代理程式已登入，但使用的工作不是服務呼叫 (例如在中斷) 上。</span><span class="sxs-lookup"><span data-stu-id="9c9d7-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="9c9d7-113">不應將其他呼叫路由傳送至代理程式。</span><span class="sxs-lookup"><span data-stu-id="9c9d7-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c9d7-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ 就緒**</span><span class="sxs-lookup"><span data-stu-id="9c9d7-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c9d7-115">代理程式已準備好接受呼叫。</span><span class="sxs-lookup"><span data-stu-id="9c9d7-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c9d7-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE 已 \_ 發行**</span><span class="sxs-lookup"><span data-stu-id="9c9d7-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c9d7-117">代理程式會話已發行。</span><span class="sxs-lookup"><span data-stu-id="9c9d7-117">The agent session has been released.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c9d7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c9d7-118">Requirements</span></span>



| <span data-ttu-id="9c9d7-119">需求</span><span class="sxs-lookup"><span data-stu-id="9c9d7-119">Requirement</span></span> | <span data-ttu-id="9c9d7-120">值</span><span class="sxs-lookup"><span data-stu-id="9c9d7-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9c9d7-121">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="9c9d7-121">TAPI version</span></span><br/> | <span data-ttu-id="9c9d7-122">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="9c9d7-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="9c9d7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9c9d7-123">Header</span></span><br/>       | <dl> <span data-ttu-id="9c9d7-124"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="9c9d7-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




