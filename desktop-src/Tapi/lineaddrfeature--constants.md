---
description: LINEADDRFEATURE \_ 常數會列出可在位址上叫用的作業。
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: 'LINEADDRFEATURE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982616"
---
# <a name="lineaddrfeature_-constants"></a><span data-ttu-id="28527-103">LINEADDRFEATURE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="28527-103">LINEADDRFEATURE\_ Constants</span></span>

<span data-ttu-id="28527-104">**LINEADDRFEATURE \_** 常數會列出可在位址上叫用的作業。</span><span class="sxs-lookup"><span data-stu-id="28527-104">The **LINEADDRFEATURE\_** constants list the operations that can be invoked on an address.</span></span>

<dl> <dt>

<span data-ttu-id="28527-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**\_向前 LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="28527-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-106">可以轉送位址。</span><span class="sxs-lookup"><span data-stu-id="28527-106">The address can be forwarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="28527-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-108">撥出電話可以放在位址上。</span><span class="sxs-lookup"><span data-stu-id="28527-108">An outgoing call can be placed on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE \_ 取貨**</span><span class="sxs-lookup"><span data-stu-id="28527-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-110">您可以在位址上挑選通話。</span><span class="sxs-lookup"><span data-stu-id="28527-110">A call can be picked up at the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**</span><span class="sxs-lookup"><span data-stu-id="28527-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE\_PICKUPDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-112">[**LinePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)函式可用來收取特定位址的呼叫。</span><span class="sxs-lookup"><span data-stu-id="28527-112">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call on a specific address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ PICKUPGROUP**</span><span class="sxs-lookup"><span data-stu-id="28527-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE\_PICKUPGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-114">您可以使用 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) 函式來挑選群組中的呼叫。</span><span class="sxs-lookup"><span data-stu-id="28527-114">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call in the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPHELD**</span><span class="sxs-lookup"><span data-stu-id="28527-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE\_PICKUPHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-116">具有 **null** 目的地位址的 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)函式 () 可用來收取位址上保留的呼叫。</span><span class="sxs-lookup"><span data-stu-id="28527-116">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call that is held on the address.</span></span> <span data-ttu-id="28527-117">這通常只會用於橋接專屬的相片順序。</span><span class="sxs-lookup"><span data-stu-id="28527-117">This is normally used only in a bridged-exclusive arrangement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**</span><span class="sxs-lookup"><span data-stu-id="28527-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE\_PICKUPWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-119">具有 **null** 目的地位址的 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)函式 () 可用來收取通話等候呼叫。</span><span class="sxs-lookup"><span data-stu-id="28527-119">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call waiting call.</span></span> <span data-ttu-id="28527-120">請注意，這不一定表示等候中的呼叫真的存在，因為電話語音裝置通常無法自動偵測這類呼叫;但是，它會指出將會叫用攔截-flash 函式，以嘗試切換到這類呼叫。</span><span class="sxs-lookup"><span data-stu-id="28527-120">Note that this does not necessarily indicate that a waiting call is actually present, because it is often impossible for a telephony device to automatically detect such a call; it does, however, indicate that the hook-flash function will be invoked to attempt to switch to such a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="28527-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-122">您可以在此位址上設定媒體控制項。</span><span class="sxs-lookup"><span data-stu-id="28527-122">Media control can be set on this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETTERMINAL**</span><span class="sxs-lookup"><span data-stu-id="28527-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-124">您可以設定此位址的終端模式。</span><span class="sxs-lookup"><span data-stu-id="28527-124">The terminal modes for this address can be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**</span><span class="sxs-lookup"><span data-stu-id="28527-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE\_SETUPCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-126">具有 **Null** 初始呼叫的電話會議可以在這個位址設定。</span><span class="sxs-lookup"><span data-stu-id="28527-126">A conference call with a **NULL** initial call can be set up at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**</span><span class="sxs-lookup"><span data-stu-id="28527-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE\_UNCOMPLETECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-128">呼叫完成要求可以在此位址取消。</span><span class="sxs-lookup"><span data-stu-id="28527-128">Call completion requests can be canceled at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE \_ UNPARK**</span><span class="sxs-lookup"><span data-stu-id="28527-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-130">您可以使用此位址來離開呼叫。</span><span class="sxs-lookup"><span data-stu-id="28527-130">Calls can be unparked using this address.</span></span>

> [!Note]  
> <span data-ttu-id="28527-131">如果未在 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)的 **dwAddressFeatures** 成員中設定新修改過的「取貨」位 \_ ，但已設定 LINEADDRFEATURE 取貨位，則任何收取模式都可以運作; 服務提供者只是未指定哪一個。</span><span class="sxs-lookup"><span data-stu-id="28527-131">If none of the new modified "PICKUP" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_PICKUP bit is set, then any of the pickup modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**</span><span class="sxs-lookup"><span data-stu-id="28527-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-133">[**LineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)函式 (有空白的目的地位址) 可用來開啟位址上的「請勿打擾」功能。</span><span class="sxs-lookup"><span data-stu-id="28527-133">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on the address.</span></span> <span data-ttu-id="28527-134">\_也會設定 LINEADDRFEATURE 轉寄。</span><span class="sxs-lookup"><span data-stu-id="28527-134">LINEADDRFEATURE\_FORWARD will also be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28527-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**</span><span class="sxs-lookup"><span data-stu-id="28527-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28527-136">[**LineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)函式可以用來將位址上的呼叫轉送到其他數位。</span><span class="sxs-lookup"><span data-stu-id="28527-136">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on the address to other numbers.</span></span> <span data-ttu-id="28527-137">\_也會設定 LINEADDRFEATURE 轉寄。</span><span class="sxs-lookup"><span data-stu-id="28527-137">LINEADDRFEATURE\_FORWARD will also be set.</span></span>

> [!Note]  
> <span data-ttu-id="28527-138">如果在 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)的 **dwAddressFeatures** 成員中未設定新的已修改 "FORWARD" 位 \_ ，但已設定 LINEADDRFEATURE 轉寄位，則任何轉寄模式都可以運作，而服務提供者只會指定哪一個。</span><span class="sxs-lookup"><span data-stu-id="28527-138">If neither of the new modified "FORWARD" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_FORWARD bit is set, then any of the forward modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28527-139">備註</span><span class="sxs-lookup"><span data-stu-id="28527-139">Remarks</span></span>

<span data-ttu-id="28527-140">無延伸。</span><span class="sxs-lookup"><span data-stu-id="28527-140">No extensibility.</span></span> <span data-ttu-id="28527-141">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="28527-141">All 32 bits are reserved.</span></span>

<span data-ttu-id="28527-142">這個常數會在 [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) 和 [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)) 所傳回的 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (所傳回的 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (中使用。</span><span class="sxs-lookup"><span data-stu-id="28527-142">This constant is used both in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (returned by [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) and in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (returned by [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span></span> <span data-ttu-id="28527-143">**LINEADDRESSCAPS** 會報告服務提供者的位址功能可用性， (主要是指定位址的交換器) 。</span><span class="sxs-lookup"><span data-stu-id="28527-143">**LINEADDRESSCAPS** reports the availability of the address features by the service provider (mainly the switch) for a given address.</span></span> <span data-ttu-id="28527-144">應用程式會在初始化時進行這項判斷。</span><span class="sxs-lookup"><span data-stu-id="28527-144">An application would make this determination when it initializes.</span></span> <span data-ttu-id="28527-145">[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)結構會報告指定的位址，當地址處於目前狀態時，可以實際叫用的位址功能。</span><span class="sxs-lookup"><span data-stu-id="28527-145">The [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure reports, for a given address, which address features can actually be invoked while the address is in the current state.</span></span> <span data-ttu-id="28527-146">在位址狀態變更之後，應用程式會以動態方式進行判斷，通常是由位址上的呼叫相關活動所造成。</span><span class="sxs-lookup"><span data-stu-id="28527-146">An application would make this determination dynamically after address-state changes, typically caused by call-related activities on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="28527-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="28527-147">Requirements</span></span>



| <span data-ttu-id="28527-148">需求</span><span class="sxs-lookup"><span data-stu-id="28527-148">Requirement</span></span> | <span data-ttu-id="28527-149">值</span><span class="sxs-lookup"><span data-stu-id="28527-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="28527-150">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="28527-150">TAPI version</span></span><br/> | <span data-ttu-id="28527-151">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="28527-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="28527-152">標頭</span><span class="sxs-lookup"><span data-stu-id="28527-152">Header</span></span><br/>       | <dl> <span data-ttu-id="28527-153"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="28527-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28527-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28527-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28527-155">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="28527-155">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="28527-156">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="28527-156">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="28527-157">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="28527-157">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="28527-158">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="28527-158">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="28527-159">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="28527-159">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="28527-160">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="28527-160">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




