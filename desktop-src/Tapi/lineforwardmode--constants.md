---
description: LINEFORWARDMODE \_ 位旗標常數描述可轉送位址之呼叫的條件。
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: 'LINEFORWARDMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984760"
---
# <a name="lineforwardmode_-constants"></a><span data-ttu-id="baaf7-103">LINEFORWARDMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="baaf7-103">LINEFORWARDMODE\_ Constants</span></span>

<span data-ttu-id="baaf7-104">**LINEFORWARDMODE \_** 位旗標常數描述可轉送位址之呼叫的條件。</span><span class="sxs-lookup"><span data-stu-id="baaf7-104">The **LINEFORWARDMODE\_** bit-flag constants describe the conditions under which calls to an address can be forwarded.</span></span>

<dl> <dt>

<span data-ttu-id="baaf7-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="baaf7-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-106">將所有呼叫轉寄于忙碌狀態，而不考慮其來源。</span><span class="sxs-lookup"><span data-stu-id="baaf7-106">Forward all calls on busy, irrespective of their origin.</span></span> <span data-ttu-id="baaf7-107">當對忙碌中的內部和外部呼叫進行轉送，而且無法另外控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-107">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE \_ BUSYEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="baaf7-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE\_BUSYEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-109">將所有外部呼叫轉寄于忙碌中。</span><span class="sxs-lookup"><span data-stu-id="baaf7-109">Forward all external calls on busy.</span></span> <span data-ttu-id="baaf7-110">當對忙碌中的內部和外部呼叫進行轉送，而且沒有任何答案可以個別控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-110">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE \_ BUSYINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="baaf7-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE\_BUSYINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-112">將所有內部呼叫轉寄于忙碌中。</span><span class="sxs-lookup"><span data-stu-id="baaf7-112">Forward all internal calls on busy.</span></span> <span data-ttu-id="baaf7-113">當對忙碌中的內部和外部呼叫進行轉送，而且沒有任何答案可以個別控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-113">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE \_ BUSYNA**</span><span class="sxs-lookup"><span data-stu-id="baaf7-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE\_BUSYNA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-115">將所有呼叫轉寄于忙碌/沒有回應，而不論其來源。</span><span class="sxs-lookup"><span data-stu-id="baaf7-115">Forward all calls on busy/no answer, irrespective of their origin.</span></span> <span data-ttu-id="baaf7-116">當對忙碌中的內部和外部呼叫進行轉送，而且無法另外控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-116">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE \_ BUSYNAEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="baaf7-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE\_BUSYNAEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-118">將所有外部呼叫轉寄于忙碌/沒有回應。</span><span class="sxs-lookup"><span data-stu-id="baaf7-118">Forward all external calls on busy/no answer.</span></span> <span data-ttu-id="baaf7-119">當待命上的呼叫轉送，而且無法針對內部呼叫分開控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-119">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE \_ BUSYNAINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="baaf7-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE\_BUSYNAINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-121">將所有內部呼叫轉寄于忙碌/沒有回應。</span><span class="sxs-lookup"><span data-stu-id="baaf7-121">Forward all internal calls on busy/no answer.</span></span> <span data-ttu-id="baaf7-122">當待命上的呼叫轉送，而且無法針對內部呼叫分開控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-122">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE \_ BUSYNASPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="baaf7-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE\_BUSYNASPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-124">在忙碌/沒有回應的情況中，會在指定的位址 (選擇性呼叫轉送) 發出的所有呼叫。</span><span class="sxs-lookup"><span data-stu-id="baaf7-124">Forward on busy/no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE \_ BUSYSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="baaf7-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE\_BUSYSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-126">將源自指定位址的所有呼叫轉寄 (選擇性呼叫轉送) 。</span><span class="sxs-lookup"><span data-stu-id="baaf7-126">Forward on busy all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE \_ NOANSW**</span><span class="sxs-lookup"><span data-stu-id="baaf7-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE\_NOANSW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-128">將所有呼叫轉寄于沒有答案的位置，而不管其來源。</span><span class="sxs-lookup"><span data-stu-id="baaf7-128">Forward all calls on no answer, irrespective of their origin.</span></span> <span data-ttu-id="baaf7-129">當內部和外部呼叫的呼叫轉送無法分開控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-129">Use this value when call forwarding for internal and external calls on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE \_ NOANSWEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="baaf7-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE\_NOANSWEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-131">將所有外部呼叫轉寄于無回應。</span><span class="sxs-lookup"><span data-stu-id="baaf7-131">Forward all external calls on no answer.</span></span> <span data-ttu-id="baaf7-132">當無法接聽內部和外部呼叫的時，請使用此值來分開控制。</span><span class="sxs-lookup"><span data-stu-id="baaf7-132">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE \_ NOANSWINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="baaf7-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE\_NOANSWINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-134">轉寄所有內部呼叫，而不接聽。</span><span class="sxs-lookup"><span data-stu-id="baaf7-134">Forward all internal calls on no answer.</span></span> <span data-ttu-id="baaf7-135">當無法接聽內部和外部呼叫的時，請使用此值來分開控制。</span><span class="sxs-lookup"><span data-stu-id="baaf7-135">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE \_ NOANSWSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="baaf7-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE\_NOANSWSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-137">將發出于指定位址的所有呼叫轉寄 (選擇性呼叫轉送) 。</span><span class="sxs-lookup"><span data-stu-id="baaf7-137">Forward on no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="baaf7-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-139">呼叫會轉送，但在發生轉送的情況下，並不知道將會發生轉送，而且服務提供者永遠不知道。</span><span class="sxs-lookup"><span data-stu-id="baaf7-139">Calls are forwarded, but the conditions under which forwarding will occur are not known, and will never be known by the service provider.</span></span> <span data-ttu-id="baaf7-140"> (TAPI 1.4 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="baaf7-140">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE \_ UNCOND**</span><span class="sxs-lookup"><span data-stu-id="baaf7-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE\_UNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-142">無條件轉寄所有呼叫，而不考慮其來源。</span><span class="sxs-lookup"><span data-stu-id="baaf7-142">Forward all calls unconditionally, irrespective of their origin.</span></span> <span data-ttu-id="baaf7-143">當內部和外部呼叫的無條件轉送無法分開控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-143">Use this value when unconditional forwarding for internal and external calls cannot be controlled separately.</span></span> <span data-ttu-id="baaf7-144">無條件轉送會覆寫在忙碌及/或沒有回應狀況時的轉送。</span><span class="sxs-lookup"><span data-stu-id="baaf7-144">Unconditional forwarding overrides forwarding on busy and/or no answer conditions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE \_ UNCONDEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="baaf7-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE\_UNCONDEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-146">無條件轉寄所有外部呼叫。</span><span class="sxs-lookup"><span data-stu-id="baaf7-146">Forward all external calls unconditionally.</span></span> <span data-ttu-id="baaf7-147">當內部和外部呼叫的無條件轉送可以個別控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-147">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE \_ UNCONDINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="baaf7-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE\_UNCONDINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-149">無條件轉送所有內部呼叫。</span><span class="sxs-lookup"><span data-stu-id="baaf7-149">Forward all internal calls unconditionally.</span></span> <span data-ttu-id="baaf7-150">當內部和外部呼叫的無條件轉送可以個別控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-150">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE \_ UNCONDSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="baaf7-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE\_UNCONDSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-152">將源自指定位址的所有呼叫無條件轉寄 (選擇性呼叫轉送) 。</span><span class="sxs-lookup"><span data-stu-id="baaf7-152">Unconditionally forward all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baaf7-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="baaf7-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="baaf7-154">呼叫會轉送，但目前不知道轉送發生的條件。</span><span class="sxs-lookup"><span data-stu-id="baaf7-154">Calls are forwarded, but the conditions under which forwarding will occur are not known at this time.</span></span> <span data-ttu-id="baaf7-155">未來可能會有已知的狀況。</span><span class="sxs-lookup"><span data-stu-id="baaf7-155">It is possible that the conditions may become known at a future time.</span></span> <span data-ttu-id="baaf7-156"> (TAPI 1.4 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="baaf7-156">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="baaf7-157">備註</span><span class="sxs-lookup"><span data-stu-id="baaf7-157">Remarks</span></span>

<span data-ttu-id="baaf7-158">無延伸。</span><span class="sxs-lookup"><span data-stu-id="baaf7-158">No extensibility.</span></span> <span data-ttu-id="baaf7-159">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="baaf7-159">All 32 bits are reserved.</span></span>

<span data-ttu-id="baaf7-160">LINEFORWARDMODE 所定義的位旗標 \_ 不是直角。</span><span class="sxs-lookup"><span data-stu-id="baaf7-160">The bit flags defined by LINEFORWARDMODE\_ are not orthogonal.</span></span> <span data-ttu-id="baaf7-161">無條件轉送會忽略任何特定的狀況，例如忙碌或沒有回應。</span><span class="sxs-lookup"><span data-stu-id="baaf7-161">Unconditional forwarding ignores any specific condition such as busy or no answer.</span></span> <span data-ttu-id="baaf7-162">如果無條件轉寄沒有作用，則在忙碌和沒有回應的情況下進行轉送，可以個別或個別控制。</span><span class="sxs-lookup"><span data-stu-id="baaf7-162">If unconditional forwarding is not in effect, then forwarding on busy and on no answer can be controlled separately or not separately.</span></span> <span data-ttu-id="baaf7-163">如果個別控制，則 \_ 可以另外使用 LINEFORWARDMODE 忙碌和 LINEFORWARDMODE \_ NOANSW 旗標。</span><span class="sxs-lookup"><span data-stu-id="baaf7-163">If controlled separately, the LINEFORWARDMODE\_BUSY and LINEFORWARDMODE\_NOANSW flags can be used separately.</span></span> <span data-ttu-id="baaf7-164">如果未另外控制，則必須使用旗標 LINEFORWARDMODE \_ BUSYNA。</span><span class="sxs-lookup"><span data-stu-id="baaf7-164">If not controlled separately, the flag LINEFORWARDMODE\_BUSYNA must be used.</span></span> <span data-ttu-id="baaf7-165">同樣地，如果內部和外部呼叫的轉送可以個別控制，則 \_ 可以個別使用 LINEFORWARDMODE internal 和 LINEFORWARDMODE \_ 外部旗標，否則會使用組合。</span><span class="sxs-lookup"><span data-stu-id="baaf7-165">Similarly, if forwarding of internal and external calls can be controlled separately, then LINEFORWARDMODE\_INTERNAL and LINEFORWARDMODE\_EXTERNAL flags can be used separately; otherwise the combination is used.</span></span>

<span data-ttu-id="baaf7-166">位址功能指出指派給一行的每個位址都有哪些轉送模式可用。</span><span class="sxs-lookup"><span data-stu-id="baaf7-166">Address capabilities indicate which forwarding modes are available for each address assigned to a line.</span></span> <span data-ttu-id="baaf7-167">應用程式可以使用 [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) 在交換器設定轉送條件。</span><span class="sxs-lookup"><span data-stu-id="baaf7-167">An application can use [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) to set forwarding conditions at the switch.</span></span>

<span data-ttu-id="baaf7-168">為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，如果協商的版本不支援，則不會使用這些 LINEFORWARDMODE \_ 值。</span><span class="sxs-lookup"><span data-stu-id="baaf7-168">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEFORWARDMODE\_ values if the negotiated version does not support them.</span></span>

## <a name="requirements"></a><span data-ttu-id="baaf7-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="baaf7-169">Requirements</span></span>



| <span data-ttu-id="baaf7-170">需求</span><span class="sxs-lookup"><span data-stu-id="baaf7-170">Requirement</span></span> | <span data-ttu-id="baaf7-171">值</span><span class="sxs-lookup"><span data-stu-id="baaf7-171">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="baaf7-172">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="baaf7-172">TAPI version</span></span><br/> | <span data-ttu-id="baaf7-173">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="baaf7-173">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="baaf7-174">標頭</span><span class="sxs-lookup"><span data-stu-id="baaf7-174">Header</span></span><br/>       | <dl> <span data-ttu-id="baaf7-175"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="baaf7-175"><dt>Tapi.h</dt></span></span> </dl> |



 

 




