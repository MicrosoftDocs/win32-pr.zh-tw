---
description: LINECONNECTEDMODE \_ 位旗標常數描述連接呼叫的不同 substates。
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: 'LINECONNECTEDMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998848"
---
# <a name="lineconnectedmode_-constants"></a><span data-ttu-id="d9f15-103">LINECONNECTEDMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="d9f15-103">LINECONNECTEDMODE\_ Constants</span></span>

<span data-ttu-id="d9f15-104">**LINECONNECTEDMODE \_** 位旗標常數描述連接呼叫的不同 substates。</span><span class="sxs-lookup"><span data-stu-id="d9f15-104">The **LINECONNECTEDMODE\_** bit-flag constants describe different substates of a connected call.</span></span> <span data-ttu-id="d9f15-105">在撥號狀態轉換為已連線，且在 \_ 指出呼叫在 LINECALLSTATE 連線中的行 CALLSTATE 訊息內，可以使用模式作為應用程式的撥號狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d9f15-105">A mode is available as call status to the application after the call state transitions to connected, and within the LINE\_CALLSTATE message indicating the call is in LINECALLSTATE\_CONNECTED.</span></span> <span data-ttu-id="d9f15-106">當呼叫位於與其他工作站 (橋接) 的共用位址時，就會使用這些值 (如需詳細資訊，請參閱 [**LINEADDRESSSHARING \_ 常數**](lineaddresssharing--constants.md)) ，主要是電子關鍵系統。</span><span class="sxs-lookup"><span data-stu-id="d9f15-106">These values are used when the call is on an address that is shared (bridged) with other stations (for more information, see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="d9f15-107">**LINECONNECTEDMODE \_ 常數** 具有下列值：</span><span class="sxs-lookup"><span data-stu-id="d9f15-107">The **LINECONNECTEDMODE\_constants** have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="d9f15-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ 使用中**</span><span class="sxs-lookup"><span data-stu-id="d9f15-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9f15-109">指出呼叫是在目前工作站上連接 (目前的工作站是呼叫) 中的參與者。</span><span class="sxs-lookup"><span data-stu-id="d9f15-109">Indicates that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="d9f15-110">如果撥號狀態模式為 0 (零) ，應用程式應該假設值為「作用中」 (這會是非橋接位址) 上的情況。</span><span class="sxs-lookup"><span data-stu-id="d9f15-110">If the call state mode is 0 (zero), the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="d9f15-111">如果使用者加入並透過手動動作離開通話，則模式可以在呼叫期間于作用中和非作用中切換。</span><span class="sxs-lookup"><span data-stu-id="d9f15-111">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span> <span data-ttu-id="d9f15-112">在這種橋接的情況下， [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) 或 [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) 作業可能不會實際卸載或放置通話，因為來電中其他工作站的狀態可能會控制 (例如，當其他工作站參與時，嘗試「保留」來電是不可能的) ;相反地，如果呼叫仍在其他工作站上連線，則可能會變更為非作用中模式。</span><span class="sxs-lookup"><span data-stu-id="d9f15-112">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call may be changed to the INACTIVE mode if it remains CONNECTED at other stations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9f15-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE \_ ACTIVEHELD**</span><span class="sxs-lookup"><span data-stu-id="d9f15-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE\_ACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9f15-114">指出工作站是呼叫中的作用中參與者，但遠端合作物件已將呼叫放置在待命 (另一方將) 的呼叫視為處於舉 servicerequeststatusenum.onhold 狀態。</span><span class="sxs-lookup"><span data-stu-id="d9f15-114">Indicates that the station is an active participant in the call, but that the remote party has placed the call on hold (the other party considers the call to be in the onhold state).</span></span> <span data-ttu-id="d9f15-115">一般來說，只有當呼叫的兩個端點落在相同的切換網域內時，才會提供這類資訊。</span><span class="sxs-lookup"><span data-stu-id="d9f15-115">Normally, such information is available only when both endpoints of the call fall within the same switching domain.</span></span> <span data-ttu-id="d9f15-116">此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d9f15-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="d9f15-117"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="d9f15-117">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9f15-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ 確認**</span><span class="sxs-lookup"><span data-stu-id="d9f15-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9f15-119">指出服務提供者收到肯定通知，指出呼叫已進入線上狀態 (例如，透過回答監督或類似的機制) 。</span><span class="sxs-lookup"><span data-stu-id="d9f15-119">Indicates that the service provider received affirmative notification that the call has entered the connected state (for example, through answer supervision or similar mechanisms).</span></span> <span data-ttu-id="d9f15-120">此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d9f15-120">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="d9f15-121"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="d9f15-121">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9f15-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ 非使用中**</span><span class="sxs-lookup"><span data-stu-id="d9f15-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9f15-123">指出呼叫在一或多個其他工作站上為作用中，但目前的工作站不是呼叫中的參與者。</span><span class="sxs-lookup"><span data-stu-id="d9f15-123">Indicates that the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="d9f15-124">如果撥號狀態模式為零，則應用程式應該假設值為「作用中」 (這會是非橋接位址) 上的情況。</span><span class="sxs-lookup"><span data-stu-id="d9f15-124">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="d9f15-125">處於非使用中狀態的呼叫可以使用 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)聯結。</span><span class="sxs-lookup"><span data-stu-id="d9f15-125">A call in the INACTIVE state can be joined using [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="d9f15-126">許多在連接狀態下都有效的作業，可能無法在非使用中的模式下使用，例如監視音調和數位，因為工作站實際上並未參與呼叫;當呼叫處於非使用中模式時，監視通常會暫停 (但未取消) 。</span><span class="sxs-lookup"><span data-stu-id="d9f15-126">Many operations that are valid in calls in the CONNECTED state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9f15-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE \_ INACTIVEHELD**</span><span class="sxs-lookup"><span data-stu-id="d9f15-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE\_INACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9f15-128">指出此工作站不是呼叫中的作用中參與者，而且遠端方已將呼叫置於待命狀態。</span><span class="sxs-lookup"><span data-stu-id="d9f15-128">Indicates that the station is not an active participant in the call, and that the remote party has placed the call on hold.</span></span> <span data-ttu-id="d9f15-129">此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d9f15-129">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="d9f15-130"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="d9f15-130">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9f15-131">備註</span><span class="sxs-lookup"><span data-stu-id="d9f15-131">Remarks</span></span>

<span data-ttu-id="d9f15-132">不可延伸。</span><span class="sxs-lookup"><span data-stu-id="d9f15-132">Not extensible.</span></span> <span data-ttu-id="d9f15-133">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="d9f15-133">All 32 bits are reserved.</span></span>

<span data-ttu-id="d9f15-134">為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，而且不會使用 \_ 經過協商的版本不支援的 LINECONNECTEDMODE 值。</span><span class="sxs-lookup"><span data-stu-id="d9f15-134">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use those LINECONNECTEDMODE\_ values that are not supported on the negotiated version.</span></span> <span data-ttu-id="d9f15-135">未 cognizant LINECONNECTEDMODE 的應用程式 \_ 很有可能會假設 LINECALLSTATE 連接的呼叫位於 \_ LINECONNECTEDMODE \_ ACTIVE 中。</span><span class="sxs-lookup"><span data-stu-id="d9f15-135">Applications that are not cognizant of LINECONNECTEDMODE\_ will most likely assume that a call that is in LINECALLSTATE\_CONNECTED is in LINECONNECTEDMODE\_ACTIVE.</span></span>

<span data-ttu-id="d9f15-136">\_ \_ 當呼叫位於與其他工作站共用 (橋接的位址時，會使用 LINECONNECTEDMODE ACTIVE 和 LINECONNECTEDMODE 非使用中的值; 請參閱 [**LINEADDRESSSHARING \_ 常數**](lineaddresssharing--constants.md)) ，主要是電子金鑰系統。</span><span class="sxs-lookup"><span data-stu-id="d9f15-136">The LINECONNECTEDMODE\_ACTIVE and LINECONNECTEDMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="d9f15-137">如果連接的撥號狀態模式為「作用中」，這表示呼叫是在目前的工作站上連接 (目前的工作站是呼叫中的參與者) 。</span><span class="sxs-lookup"><span data-stu-id="d9f15-137">If the connected call state mode is "active," it means that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="d9f15-138">如果通話狀態模式為「非使用中」，則會在一或多個其他工作站上使用中的呼叫，但目前的工作站不是呼叫的參與者。</span><span class="sxs-lookup"><span data-stu-id="d9f15-138">If the call state mode is "inactive," the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="d9f15-139">如果撥號狀態模式為零，則應用程式應該假設值為「作用中」 (這會是非橋接位址) 上的情況。</span><span class="sxs-lookup"><span data-stu-id="d9f15-139">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="d9f15-140">如果使用者加入並透過手動動作離開通話，則模式可以在呼叫期間于作用中和非作用中切換。</span><span class="sxs-lookup"><span data-stu-id="d9f15-140">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span>

<span data-ttu-id="d9f15-141">在這種橋接的情況下， [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) 或 [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) 作業可能不會實際卸載或放置通話，因為來電中其他工作站的狀態可能會控制 (例如，在其他工作站參與時嘗試「保留」來電將無法) ;相反地，呼叫可以直接變更為非作用中模式（如果它仍在其他工作站上連線）。</span><span class="sxs-lookup"><span data-stu-id="d9f15-141">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating will not be possible); instead, the call can simply be changed to the INACTIVE mode if it remains connected at other stations.</span></span> <span data-ttu-id="d9f15-142">處於非使用中狀態的呼叫可以使用 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)聯結。</span><span class="sxs-lookup"><span data-stu-id="d9f15-142">A call in the INACTIVE state can be joined using the [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="d9f15-143">許多在連接狀態下都有效的作業，可能無法在非使用中的模式下使用，例如監視音調和數位，因為工作站實際上並未參與呼叫;當呼叫處於非使用中模式時，監視通常會暫停 (但未取消) 。</span><span class="sxs-lookup"><span data-stu-id="d9f15-143">Many operations that are valid in calls in the connected state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f15-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9f15-144">Requirements</span></span>



| <span data-ttu-id="d9f15-145">需求</span><span class="sxs-lookup"><span data-stu-id="d9f15-145">Requirement</span></span> | <span data-ttu-id="d9f15-146">值</span><span class="sxs-lookup"><span data-stu-id="d9f15-146">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d9f15-147">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d9f15-147">TAPI version</span></span><br/> | <span data-ttu-id="d9f15-148">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d9f15-148">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d9f15-149">標頭</span><span class="sxs-lookup"><span data-stu-id="d9f15-149">Header</span></span><br/>       | <dl> <span data-ttu-id="d9f15-150"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="d9f15-150"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f15-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9f15-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f15-152">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="d9f15-152">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[<span data-ttu-id="d9f15-153">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="d9f15-153">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="d9f15-154">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="d9f15-154">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




