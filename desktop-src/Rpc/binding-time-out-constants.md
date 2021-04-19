---
title: '系結超時常數 (Rpcdce .h) '
description: RPC 程式庫會使用系結超時常數來指定在放棄之前，建立伺服器系結所需花費的相對時間量。
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106993743"
---
# <a name="binding-time-out-constants"></a><span data-ttu-id="2243c-103">系結超時常數</span><span class="sxs-lookup"><span data-stu-id="2243c-103">Binding Time-out Constants</span></span>

<span data-ttu-id="2243c-104">RPC 程式庫會使用系結超時常數來指定在放棄之前，建立伺服器系結所需花費的相對時間量。</span><span class="sxs-lookup"><span data-stu-id="2243c-104">The RPC library uses the binding time-out constants to specify the relative amount of time that should be spent to establish a binding to the server before giving up.</span></span> <span data-ttu-id="2243c-105">您可以透過呼叫 [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) 函式來啟用超時。</span><span class="sxs-lookup"><span data-stu-id="2243c-105">The timeout can be enabled with a call to the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function.</span></span> <span data-ttu-id="2243c-106">下列清單包含有效的超時值。</span><span class="sxs-lookup"><span data-stu-id="2243c-106">The following list contains the valid time-out values.</span></span>



| <span data-ttu-id="2243c-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="2243c-107">Constant/value</span></span>                                                                                                                                                                                                                                                                | <span data-ttu-id="2243c-108">Description</span><span class="sxs-lookup"><span data-stu-id="2243c-108">Description</span></span>                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <span data-ttu-id="2243c-109"><dt>**RPC \_C 系結 \_ \_ 無限 \_ 超時時間**</dt> <dt> 10</dt></span><span class="sxs-lookup"><span data-stu-id="2243c-109"><dt>**RPC\_C\_BINDING\_INFINITE\_TIMEOUT**</dt> <dt> 10 </dt></span></span> </dl> | <span data-ttu-id="2243c-110">繼續嘗試永遠建立通訊。</span><span class="sxs-lookup"><span data-stu-id="2243c-110">Keeps trying to establish communications forever.</span></span><br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <span data-ttu-id="2243c-111"><dt>**RPC \_C 系結 \_ \_ 最小 \_ 超時**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2243c-111"><dt>**RPC\_C\_BINDING\_MIN\_TIMEOUT**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="2243c-112">嘗試使用網路通訊協定的最小時間量。</span><span class="sxs-lookup"><span data-stu-id="2243c-112">Tries the minimum amount of time for the network protocol being used.</span></span> <span data-ttu-id="2243c-113">此值會在判斷伺服器是否正在執行時，優先于正確的回應時間。</span><span class="sxs-lookup"><span data-stu-id="2243c-113">This value favors response time over correctness in determining whether the server is running.</span></span><br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <span data-ttu-id="2243c-114"><dt>**RPC \_C 系結 \_ \_ 預設 \_ 超時**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2243c-114"><dt>**RPC\_C\_BINDING\_DEFAULT\_TIMEOUT**</dt> <dt>5</dt></span></span> </dl>       | <span data-ttu-id="2243c-115">嘗試使用網路通訊協定的平均時間量。</span><span class="sxs-lookup"><span data-stu-id="2243c-115">Tries an average amount of time for the network protocol being used.</span></span> <span data-ttu-id="2243c-116">此值可讓您判斷伺服器是否正在執行，並提供回應時間的相等加權。</span><span class="sxs-lookup"><span data-stu-id="2243c-116">This value gives correctness in determining whether a server is running and gives response time equal weight.</span></span> <span data-ttu-id="2243c-117">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="2243c-117">This is the default value.</span></span><br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <span data-ttu-id="2243c-118"><dt>**RPC \_C 系結 \_ \_ 最大 \_ 超時**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2243c-118"><dt>**RPC\_C\_BINDING\_MAX\_TIMEOUT**</dt> <dt>9</dt></span></span> </dl>                   | <span data-ttu-id="2243c-119">嘗試使用網路通訊協定的最長時間量。</span><span class="sxs-lookup"><span data-stu-id="2243c-119">Tries the longest amount of time for the network protocol being used.</span></span> <span data-ttu-id="2243c-120">此值會在判斷伺服器是否正在回應時間執行時，優先于判斷是否正確。</span><span class="sxs-lookup"><span data-stu-id="2243c-120">This value favors correctness in determining whether a server is running over response time.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="2243c-121">備註</span><span class="sxs-lookup"><span data-stu-id="2243c-121">Remarks</span></span>

<span data-ttu-id="2243c-122">上表中的值不是以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="2243c-122">The values in the preceding table are not in seconds.</span></span> <span data-ttu-id="2243c-123">這些值代表以零到10之小數位數的相對時間量。</span><span class="sxs-lookup"><span data-stu-id="2243c-123">These values represent a relative amount of time on a scale of zero to 10.</span></span> <span data-ttu-id="2243c-124">如需避免通訊延遲的詳細資訊，請參閱防止用戶端停止回應。</span><span class="sxs-lookup"><span data-stu-id="2243c-124">For more information on avoiding communication delays, refer to Preventing Client-side Hangs.</span></span>

## <a name="requirements"></a><span data-ttu-id="2243c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="2243c-125">Requirements</span></span>



| <span data-ttu-id="2243c-126">需求</span><span class="sxs-lookup"><span data-stu-id="2243c-126">Requirement</span></span> | <span data-ttu-id="2243c-127">值</span><span class="sxs-lookup"><span data-stu-id="2243c-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2243c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2243c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2243c-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2243c-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2243c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2243c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2243c-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2243c-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2243c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="2243c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2243c-133"><dt>Rpcdce。h</dt></span><span class="sxs-lookup"><span data-stu-id="2243c-133"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





