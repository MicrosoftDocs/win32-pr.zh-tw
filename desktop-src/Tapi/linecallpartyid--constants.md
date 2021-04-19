---
description: LINECALLPARTYID \_ 位旗標常數描述有關呼叫中參與之合作物件的性質。
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: 'LINECALLPARTYID_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001860"
---
# <a name="linecallpartyid_-constants"></a><span data-ttu-id="41002-103">LINECALLPARTYID \_ 常數</span><span class="sxs-lookup"><span data-stu-id="41002-103">LINECALLPARTYID\_ Constants</span></span>

<span data-ttu-id="41002-104">**LINECALLPARTYID \_** 位旗標常數描述有關呼叫中參與之合作物件的性質。</span><span class="sxs-lookup"><span data-stu-id="41002-104">The **LINECALLPARTYID\_** bit-flag constants describe the nature of the information available about the parties involved in a call.</span></span>

<dl> <dt>

<span data-ttu-id="41002-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**LINECALLPARTYID \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="41002-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**LINECALLPARTYID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41002-106">合作物件識別碼資訊是以標準位址格式或可撥位址格式的合作物件位址所組成。</span><span class="sxs-lookup"><span data-stu-id="41002-106">Party identifier information consists of the party's address in either canonical address format or dialable address format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41002-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID 已 \_ 封鎖**</span><span class="sxs-lookup"><span data-stu-id="41002-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41002-108">無法使用合作物件識別碼資訊，因為它已被遠端方封鎖。</span><span class="sxs-lookup"><span data-stu-id="41002-108">Party identifier information is not available because it has been blocked by the remote party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41002-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**LINECALLPARTYID \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="41002-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**LINECALLPARTYID\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41002-110">合作物件識別碼資訊包含合作物件名稱 (例如，從保留在切換) 內的目錄。</span><span class="sxs-lookup"><span data-stu-id="41002-110">Party identifier information consists of the party's name (as, for example, from a directory kept inside the switch).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41002-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID \_ OUTOFAREA**</span><span class="sxs-lookup"><span data-stu-id="41002-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID\_OUTOFAREA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41002-112">呼叫的呼叫端識別碼資訊無法使用，因為它不會傳播到網路的所有方法。</span><span class="sxs-lookup"><span data-stu-id="41002-112">Caller ID information for the call is not available because it is not propagated all the way by the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41002-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ 部分**</span><span class="sxs-lookup"><span data-stu-id="41002-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41002-114">合作物件識別碼資訊是有效的，但只限于部分資訊。</span><span class="sxs-lookup"><span data-stu-id="41002-114">Party identifier information is valid but it is limited to partial information only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41002-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="41002-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41002-116">無法使用合作物件識別碼資訊，稍後將無法使用。</span><span class="sxs-lookup"><span data-stu-id="41002-116">Party identifier information is not available and will not become available later.</span></span> <span data-ttu-id="41002-117">資訊可能因為未指定的原因而無法使用。</span><span class="sxs-lookup"><span data-stu-id="41002-117">Information may be unavailable for unspecified reasons.</span></span> <span data-ttu-id="41002-118">例如，資訊並非由網路傳遞、服務提供者已忽略，依此類推。</span><span class="sxs-lookup"><span data-stu-id="41002-118">For example, the information was not delivered by the network, it was ignored by the service provider, and so forth.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41002-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="41002-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41002-120">合作物件識別碼資訊目前未知，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="41002-120">Party identifier information is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41002-121">備註</span><span class="sxs-lookup"><span data-stu-id="41002-121">Remarks</span></span>

<span data-ttu-id="41002-122">無延伸。</span><span class="sxs-lookup"><span data-stu-id="41002-122">No extensibility.</span></span> <span data-ttu-id="41002-123">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="41002-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="41002-124">針對每個牽涉到呼叫的合作物件， **LINECALLPARTYID \_** 常數描述合作物件識別碼資訊的格式化方式。</span><span class="sxs-lookup"><span data-stu-id="41002-124">For each of the possible parties involved in a call, the **LINECALLPARTYID\_** constants describe how the party identifier information is formatted.</span></span> <span data-ttu-id="41002-125">這項資訊是在 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) 資料結構中提供。</span><span class="sxs-lookup"><span data-stu-id="41002-125">This information is supplied in the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="41002-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="41002-126">Requirements</span></span>



| <span data-ttu-id="41002-127">需求</span><span class="sxs-lookup"><span data-stu-id="41002-127">Requirement</span></span> | <span data-ttu-id="41002-128">值</span><span class="sxs-lookup"><span data-stu-id="41002-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="41002-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="41002-129">TAPI version</span></span><br/> | <span data-ttu-id="41002-130">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="41002-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="41002-131">標頭</span><span class="sxs-lookup"><span data-stu-id="41002-131">Header</span></span><br/>       | <dl> <span data-ttu-id="41002-132"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="41002-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




