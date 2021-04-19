---
description: LINECALLORIGIN \_ 常數描述呼叫的來源。
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: 'LINECALLORIGIN_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985558"
---
# <a name="linecallorigin_-constants"></a><span data-ttu-id="40b06-103">LINECALLORIGIN \_ 常數</span><span class="sxs-lookup"><span data-stu-id="40b06-103">LINECALLORIGIN\_ Constants</span></span>

<span data-ttu-id="40b06-104">**LINECALLORIGIN \_** 常數描述呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="40b06-104">The **LINECALLORIGIN\_** constants describe the origin of a call.</span></span>

<dl> <dt>

<span data-ttu-id="40b06-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**LINECALLORIGIN \_ 會議**</span><span class="sxs-lookup"><span data-stu-id="40b06-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**LINECALLORIGIN\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40b06-106">通話控制碼適用于會議電話，也就是應用程式與交換器中的會議橋接器的連接。</span><span class="sxs-lookup"><span data-stu-id="40b06-106">The call handle is for a conference call, that is, it is the application's connection to the conference bridge in the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40b06-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ 外部**</span><span class="sxs-lookup"><span data-stu-id="40b06-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40b06-108">呼叫是以外部線路上的撥入電話來產生。</span><span class="sxs-lookup"><span data-stu-id="40b06-108">The call originated as an incoming call on an external line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40b06-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="40b06-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN\_INBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40b06-110">呼叫是以來電的形式產生，但服務提供者無法判斷它是否來自相同交換器上的另一個站，或從外部線路。</span><span class="sxs-lookup"><span data-stu-id="40b06-110">The call originated as an incoming call, but the service provider is unable to determine whether it came from another station on the same switch or from an external line.</span></span> <span data-ttu-id="40b06-111">只有在已協商 TAPI 1.4 版或更新版本時，服務提供者才能使用此常數。</span><span class="sxs-lookup"><span data-stu-id="40b06-111">Service providers can use this constant only when TAPI version 1.4 or later has been negotiated.</span></span> <span data-ttu-id="40b06-112">否則，服務提供者可以替代 LINECALLORIGIN \_ UNAVAIL。</span><span class="sxs-lookup"><span data-stu-id="40b06-112">Otherwise, the service provider can substitute LINECALLORIGIN\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40b06-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ 內部**</span><span class="sxs-lookup"><span data-stu-id="40b06-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40b06-114">呼叫是源自相同切換環境內部之站上的撥入電話。</span><span class="sxs-lookup"><span data-stu-id="40b06-114">The call originated as an incoming call at a station internal to the same switching environment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40b06-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="40b06-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN\_OUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40b06-116">由此站發出的呼叫會被撥出呼叫。</span><span class="sxs-lookup"><span data-stu-id="40b06-116">The call originated from this station as an outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40b06-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="40b06-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40b06-118">呼叫來源無法使用，而且永遠不會成為此呼叫的已知。</span><span class="sxs-lookup"><span data-stu-id="40b06-118">The call origin is not available and will never become known for this call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40b06-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="40b06-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40b06-120">呼叫來源目前未知，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="40b06-120">The call origin is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40b06-121">備註</span><span class="sxs-lookup"><span data-stu-id="40b06-121">Remarks</span></span>

<span data-ttu-id="40b06-122">無延伸。</span><span class="sxs-lookup"><span data-stu-id="40b06-122">No extensibility.</span></span> <span data-ttu-id="40b06-123">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="40b06-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="40b06-124">呼叫的來源會儲存在呼叫之 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)結構的 **>dworigin** 成員中。</span><span class="sxs-lookup"><span data-stu-id="40b06-124">The origin of a call is stored in the **dwOrigin** member of the call's [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="40b06-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="40b06-125">Requirements</span></span>



| <span data-ttu-id="40b06-126">需求</span><span class="sxs-lookup"><span data-stu-id="40b06-126">Requirement</span></span> | <span data-ttu-id="40b06-127">值</span><span class="sxs-lookup"><span data-stu-id="40b06-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="40b06-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="40b06-128">TAPI version</span></span><br/> | <span data-ttu-id="40b06-129">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="40b06-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="40b06-130">標頭</span><span class="sxs-lookup"><span data-stu-id="40b06-130">Header</span></span><br/>       | <dl> <span data-ttu-id="40b06-131"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="40b06-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




