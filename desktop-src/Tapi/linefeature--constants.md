---
description: LINEFEATURE \_ 常數列出可以使用此 API 在行上叫用的作業。
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: 'LINEFEATURE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995098"
---
# <a name="linefeature_-constants"></a><span data-ttu-id="241ce-103">LINEFEATURE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="241ce-103">LINEFEATURE\_ Constants</span></span>

<span data-ttu-id="241ce-104">**LINEFEATURE \_ 常數** 列出可以使用此 API 在行上叫用的作業。</span><span class="sxs-lookup"><span data-stu-id="241ce-104">The **LINEFEATURE\_ constants** list the operations that can be invoked on a line using this API.</span></span>

<dl> <dt>

<span data-ttu-id="241ce-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="241ce-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241ce-106">裝置特定的作業可以使用於這一行。</span><span class="sxs-lookup"><span data-stu-id="241ce-106">Device-specific operations can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241ce-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE \_ DEVSPECIFICFEAT**</span><span class="sxs-lookup"><span data-stu-id="241ce-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE\_DEVSPECIFICFEAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241ce-108">裝置特定功能可以在這一行上使用。</span><span class="sxs-lookup"><span data-stu-id="241ce-108">Device-specific features can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241ce-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**\_向前 LINEFEATURE**</span><span class="sxs-lookup"><span data-stu-id="241ce-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241ce-110">所有位址的轉送都可以使用於這一行。</span><span class="sxs-lookup"><span data-stu-id="241ce-110">Forwarding of all addresses can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241ce-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE \_ FORWARDDND**</span><span class="sxs-lookup"><span data-stu-id="241ce-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241ce-112">[**LineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)函式 (有空白的目的地位址) 可用來開啟行上所有位址的「請勿打擾」功能。</span><span class="sxs-lookup"><span data-stu-id="241ce-112">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on all addresses on the line.</span></span> <span data-ttu-id="241ce-113">\_也會設定 LINEFEATURE 轉寄。</span><span class="sxs-lookup"><span data-stu-id="241ce-113">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="241ce-114">此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="241ce-114">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241ce-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE \_ FORWARDFWD**</span><span class="sxs-lookup"><span data-stu-id="241ce-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241ce-116">[**LineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)函式可以用來將該行上所有位址的呼叫轉送到其他數位。</span><span class="sxs-lookup"><span data-stu-id="241ce-116">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on all address on the line to other numbers.</span></span> <span data-ttu-id="241ce-117">\_也會設定 LINEFEATURE 轉寄。</span><span class="sxs-lookup"><span data-stu-id="241ce-117">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="241ce-118">此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="241ce-118">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241ce-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="241ce-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241ce-120">您可以使用未指定的位址，將外寄呼叫放在這一行。</span><span class="sxs-lookup"><span data-stu-id="241ce-120">An outgoing call can be placed on this line using an unspecified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241ce-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE \_ SETDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="241ce-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE\_SETDEVSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241ce-122">您可以線上路裝置上叫用 [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) 函式。</span><span class="sxs-lookup"><span data-stu-id="241ce-122">The [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) function can be invoked on the line device.</span></span> <span data-ttu-id="241ce-123">此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="241ce-123">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241ce-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE \_ SETMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="241ce-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241ce-125">您可以在這一行設定媒體控制項。</span><span class="sxs-lookup"><span data-stu-id="241ce-125">Media control can be set on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241ce-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_ SETTERMINAL**</span><span class="sxs-lookup"><span data-stu-id="241ce-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241ce-127">您可以設定這一行的終端模式。</span><span class="sxs-lookup"><span data-stu-id="241ce-127">Terminal modes for this line can be set.</span></span>

> [!Note]  
> <span data-ttu-id="241ce-128">如果在 [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)的 **dwLineFeatures** 成員中未設定新的已修改 "FORWARD" 位 \_ ，但已設定 LINEFEATURE 轉寄位，則任何轉寄模式都可以運作，而服務提供者只會指定哪一個。</span><span class="sxs-lookup"><span data-stu-id="241ce-128">If neither of the new modified "FORWARD" bits is set in the **dwLineFeatures** member in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) but the LINEFEATURE\_FORWARD bit is set, then any of the forward modes can work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="241ce-129">備註</span><span class="sxs-lookup"><span data-stu-id="241ce-129">Remarks</span></span>

<span data-ttu-id="241ce-130">無延伸。</span><span class="sxs-lookup"><span data-stu-id="241ce-130">No extensibility.</span></span> <span data-ttu-id="241ce-131">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="241ce-131">All 32 bits are reserved.</span></span>

<span data-ttu-id="241ce-132">LINEFEATURE \_ 常數用於 [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)) 所傳回的 [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (。</span><span class="sxs-lookup"><span data-stu-id="241ce-132">The LINEFEATURE\_ constants are used in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (returned by [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span></span> <span data-ttu-id="241ce-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) 報表，適用于給定的行，在行處於目前狀態時，可以實際叫用的線條特徵。</span><span class="sxs-lookup"><span data-stu-id="241ce-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) reports, for a given line, which line features can actually be invoked while the line is in the current state.</span></span> <span data-ttu-id="241ce-134">應用程式會在行狀態變更之後動態進行這項判斷，通常是由一行上的位址或呼叫相關的活動所造成。</span><span class="sxs-lookup"><span data-stu-id="241ce-134">An application would make this determination dynamically after line state changes, typically caused by address or call-related activities on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="241ce-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="241ce-135">Requirements</span></span>



| <span data-ttu-id="241ce-136">需求</span><span class="sxs-lookup"><span data-stu-id="241ce-136">Requirement</span></span> | <span data-ttu-id="241ce-137">值</span><span class="sxs-lookup"><span data-stu-id="241ce-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="241ce-138">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="241ce-138">TAPI version</span></span><br/> | <span data-ttu-id="241ce-139">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="241ce-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="241ce-140">標頭</span><span class="sxs-lookup"><span data-stu-id="241ce-140">Header</span></span><br/>       | <dl> <span data-ttu-id="241ce-141"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="241ce-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="241ce-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="241ce-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="241ce-143">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="241ce-143">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="241ce-144">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="241ce-144">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="241ce-145">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="241ce-145">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="241ce-146">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="241ce-146">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




