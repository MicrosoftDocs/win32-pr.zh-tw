---
title: 'Windows 動畫錯誤碼 (Winerror.h .h) '
description: 如果發生錯誤，Windows 動畫會以 HRESULT 值傳回程序代碼。 本節提供 Windows 動畫特定的錯誤碼清單。 如需一般 COM 錯誤碼的清單，請參閱 COM 錯誤碼。
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968342"
---
# <a name="windows-animation-error-codes"></a><span data-ttu-id="feec6-105">Windows 動畫錯誤碼</span><span class="sxs-lookup"><span data-stu-id="feec6-105">Windows Animation Error Codes</span></span>

<span data-ttu-id="feec6-106">如果發生錯誤，Windows 動畫會以 **HRESULT** 值傳回程序代碼。</span><span class="sxs-lookup"><span data-stu-id="feec6-106">If an error occurs, Windows Animation returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="feec6-107">本節提供 Windows 動畫特定的錯誤碼清單。</span><span class="sxs-lookup"><span data-stu-id="feec6-107">This section provides a list of error codes specific to Windows Animation.</span></span> <span data-ttu-id="feec6-108">如需一般 COM 錯誤碼的清單，請參閱 [Com 錯誤碼](/windows/desktop/com/com-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="feec6-108">For a list of general COM error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="feec6-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI \_ E \_ 建立 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="feec6-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI\_E\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-110">0x802A0001</span><span class="sxs-lookup"><span data-stu-id="feec6-110">0x802A0001</span></span>
</dt> <dt>



<span data-ttu-id="feec6-111">無法建立物件。</span><span class="sxs-lookup"><span data-stu-id="feec6-111">The object could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI \_ E \_ 關機 \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="feec6-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI\_E\_SHUTDOWN\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-113">0x802A0002</span><span class="sxs-lookup"><span data-stu-id="feec6-113">0x802A0002</span></span>
</dt> <dt>



<span data-ttu-id="feec6-114">已在動畫管理員上呼叫 [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) 方法，導致動畫管理員關閉，以及建立的所有動畫變數和分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="feec6-114">The [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method has been called on the animation manager, causing the animation manager to shut down and all the animation variables and storyboards it created to be released.</span></span>

> [!Note]  
> <span data-ttu-id="feec6-115">在 [**關閉**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown)之後，任何動畫物件都不能呼叫任何方法。</span><span class="sxs-lookup"><span data-stu-id="feec6-115">No methods can be called on any animation object after [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI \_ E 不 \_ 合法的 \_ 重新進入**</span><span class="sxs-lookup"><span data-stu-id="feec6-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI\_E\_ILLEGAL\_REENTRANCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-117">0x802A0003</span><span class="sxs-lookup"><span data-stu-id="feec6-117">0x802A0003</span></span>
</dt> <dt>



<span data-ttu-id="feec6-118">這種回呼類型無法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="feec6-118">This method cannot be called during this type of callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI \_ E \_ 物件 \_ 密封**</span><span class="sxs-lookup"><span data-stu-id="feec6-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI\_E\_OBJECT\_SEALED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-120">0x802A0004</span><span class="sxs-lookup"><span data-stu-id="feec6-120">0x802A0004</span></span>
</dt> <dt>



<span data-ttu-id="feec6-121">此物件已密封，因此不再允許這項變更。</span><span class="sxs-lookup"><span data-stu-id="feec6-121">This object has been sealed, so this change is no longer allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**\_ \_ \_ 未設定 UI E \_ 值**</span><span class="sxs-lookup"><span data-stu-id="feec6-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**UI\_E\_VALUE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-123">0x802A0005</span><span class="sxs-lookup"><span data-stu-id="feec6-123">0x802A0005</span></span>
</dt> <dt>



<span data-ttu-id="feec6-124">要求的值從未設定過，因此無法取出。</span><span class="sxs-lookup"><span data-stu-id="feec6-124">The requested value has never been set, and therefore cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**UI \_ E \_ 值 \_ 未 \_ 判斷**</span><span class="sxs-lookup"><span data-stu-id="feec6-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**UI\_E\_VALUE\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-126">0x802A0006</span><span class="sxs-lookup"><span data-stu-id="feec6-126">0x802A0006</span></span>
</dt> <dt>



<span data-ttu-id="feec6-127">無法判斷要求的值。</span><span class="sxs-lookup"><span data-stu-id="feec6-127">The requested value cannot be determined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI \_ E \_ 不正確 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="feec6-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI\_E\_INVALID\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-129">0x802A0007</span><span class="sxs-lookup"><span data-stu-id="feec6-129">0x802A0007</span></span>
</dt> <dt>



<span data-ttu-id="feec6-130">回呼傳回了不正確輸出參數。</span><span class="sxs-lookup"><span data-stu-id="feec6-130">A callback returned an invalid output parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**\_需要 UI E \_ 布林值 \_**</span><span class="sxs-lookup"><span data-stu-id="feec6-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI\_E\_BOOLEAN\_EXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-132">0x802A0008</span><span class="sxs-lookup"><span data-stu-id="feec6-132">0x802A0008</span></span>
</dt> <dt>



<span data-ttu-id="feec6-133">回呼傳回的成功碼不是 S \_ OK 或 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="feec6-133">A callback returned a success code other than S\_OK or S\_FALSE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI \_ E \_ 不同的 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="feec6-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI\_E\_DIFFERENT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-135">0x802A0009</span><span class="sxs-lookup"><span data-stu-id="feec6-135">0x802A0009</span></span>
</dt> <dt>



<span data-ttu-id="feec6-136">這個物件所擁有的參數是由不同的物件所擁有。</span><span class="sxs-lookup"><span data-stu-id="feec6-136">A parameter that should be owned by this object is owned by a different object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI \_ E \_ 模糊 \_ 相符**</span><span class="sxs-lookup"><span data-stu-id="feec6-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI\_E\_AMBIGUOUS\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-138">0x802A000A</span><span class="sxs-lookup"><span data-stu-id="feec6-138">0x802A000A</span></span>
</dt> <dt>



<span data-ttu-id="feec6-139">有一個以上的專案符合搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="feec6-139">More than one item matched the search criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI \_ E \_ FP \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="feec6-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI\_E\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-141">0x802A000B</span><span class="sxs-lookup"><span data-stu-id="feec6-141">0x802A000B</span></span>
</dt> <dt>



<span data-ttu-id="feec6-142">發生浮點溢位。</span><span class="sxs-lookup"><span data-stu-id="feec6-142">A floating-point overflow occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI \_ E \_ 錯誤的 \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="feec6-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI\_E\_WRONG\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-144">0x802A000C</span><span class="sxs-lookup"><span data-stu-id="feec6-144">0x802A000C</span></span>
</dt> <dt>



<span data-ttu-id="feec6-145">您只能從建立物件的執行緒呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="feec6-145">This method can only be called from the thread that created the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI E 分鏡腳本 \_ \_ \_ 活動**</span><span class="sxs-lookup"><span data-stu-id="feec6-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI\_E\_STORYBOARD\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-147">0x802A0101</span><span class="sxs-lookup"><span data-stu-id="feec6-147">0x802A0101</span></span>
</dt> <dt>



<span data-ttu-id="feec6-148">分鏡腳本目前為排程。</span><span class="sxs-lookup"><span data-stu-id="feec6-148">The storyboard is currently in the schedule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI E 分鏡腳本 \_ \_ \_ 未 \_ 播放**</span><span class="sxs-lookup"><span data-stu-id="feec6-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI\_E\_STORYBOARD\_NOT\_PLAYING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-150">0x802A0102</span><span class="sxs-lookup"><span data-stu-id="feec6-150">0x802A0102</span></span>
</dt> <dt>



<span data-ttu-id="feec6-151">腳本未播放。</span><span class="sxs-lookup"><span data-stu-id="feec6-151">The storyboard is not playing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI \_ E \_ \_ \_ 在結束後 \_ 啟動主要畫面格**</span><span class="sxs-lookup"><span data-stu-id="feec6-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI\_E\_START\_KEYFRAME\_AFTER\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-153">0x802A0103</span><span class="sxs-lookup"><span data-stu-id="feec6-153">0x802A0103</span></span>
</dt> <dt>



<span data-ttu-id="feec6-154">開始的主要畫面格可能會在結束主要畫面格之後發生。</span><span class="sxs-lookup"><span data-stu-id="feec6-154">The start keyframe might occur after the end keyframe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI \_ E 結束主要畫面格 \_ \_ \_ 未 \_ 判定**</span><span class="sxs-lookup"><span data-stu-id="feec6-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI\_E\_END\_KEYFRAME\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-156">0x802A0104</span><span class="sxs-lookup"><span data-stu-id="feec6-156">0x802A0104</span></span>
</dt> <dt>



<span data-ttu-id="feec6-157">可能無法判斷達到開始主要畫面格的結束主要畫面格時間。</span><span class="sxs-lookup"><span data-stu-id="feec6-157">It might not be possible to determine the end keyframe time when the start keyframe is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI \_ E \_ 迴圈重 \_ 迭**</span><span class="sxs-lookup"><span data-stu-id="feec6-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI\_E\_LOOPS\_OVERLAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-159">0x802A0105</span><span class="sxs-lookup"><span data-stu-id="feec6-159">0x802A0105</span></span>
</dt> <dt>



<span data-ttu-id="feec6-160">兩個重複的分鏡腳本部分可能會重迭。</span><span class="sxs-lookup"><span data-stu-id="feec6-160">Two repeated portions of a storyboard might overlap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**\_ \_ \_ 已使用 UI E \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="feec6-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**UI\_E\_TRANSITION\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-162">0x802A0106</span><span class="sxs-lookup"><span data-stu-id="feec6-162">0x802A0106</span></span>
</dt> <dt>



<span data-ttu-id="feec6-163">轉換已加入至不同的分鏡腳本，或已新增至已完成播放且已發行的分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="feec6-163">The transition has already been added to a different storyboard or has been added to a storyboard that has finished playing and been released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI \_ E \_ 轉換 \_ 不 \_ 在分鏡腳本中 \_**</span><span class="sxs-lookup"><span data-stu-id="feec6-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI\_E\_TRANSITION\_NOT\_IN\_STORYBOARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-165">0x802A0107</span><span class="sxs-lookup"><span data-stu-id="feec6-165">0x802A0107</span></span>
</dt> <dt>



<span data-ttu-id="feec6-166">轉換尚未新增至任何分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="feec6-166">The transition has not been added to any storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI \_ E \_ 轉換 \_ ECLIPSED**</span><span class="sxs-lookup"><span data-stu-id="feec6-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI\_E\_TRANSITION\_ECLIPSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-168">0x802A0108</span><span class="sxs-lookup"><span data-stu-id="feec6-168">0x802A0108</span></span>
</dt> <dt>



<span data-ttu-id="feec6-169">轉換可能會 eclipse 腳本中的另一個轉換開始。</span><span class="sxs-lookup"><span data-stu-id="feec6-169">The transition might eclipse the beginning of another transition in the storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**\_ \_ \_ \_ 上次 \_ 更新前的 UI E 時間**</span><span class="sxs-lookup"><span data-stu-id="feec6-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI\_E\_TIME\_BEFORE\_LAST\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-171">0x802A0109</span><span class="sxs-lookup"><span data-stu-id="feec6-171">0x802A0109</span></span>
</dt> <dt>



<span data-ttu-id="feec6-172">指定的時間早于傳遞至上次更新的時間。</span><span class="sxs-lookup"><span data-stu-id="feec6-172">The specified time is earlier than the time passed to the last update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feec6-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI \_ E \_ 計時器 \_ 用戶端 \_ 已 \_ 連線**</span><span class="sxs-lookup"><span data-stu-id="feec6-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI\_E\_TIMER\_CLIENT\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feec6-174">0x802A010A</span><span class="sxs-lookup"><span data-stu-id="feec6-174">0x802A010A</span></span>
</dt> <dt>



<span data-ttu-id="feec6-175">此用戶端已連接到計時器。</span><span class="sxs-lookup"><span data-stu-id="feec6-175">This client is already connected to a timer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="feec6-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="feec6-176">Requirements</span></span>



| <span data-ttu-id="feec6-177">需求</span><span class="sxs-lookup"><span data-stu-id="feec6-177">Requirement</span></span> | <span data-ttu-id="feec6-178">值</span><span class="sxs-lookup"><span data-stu-id="feec6-178">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feec6-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="feec6-179">Minimum supported client</span></span><br/> | <span data-ttu-id="feec6-180">Windows 7、Windows Vista 和 windows Vista \[ 桌面應用程式的平臺更新\]</span><span class="sxs-lookup"><span data-stu-id="feec6-180">Windows 7, Windows Vista and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="feec6-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="feec6-181">Minimum supported server</span></span><br/> | <span data-ttu-id="feec6-182">都不支援</span><span class="sxs-lookup"><span data-stu-id="feec6-182">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="feec6-183">標頭</span><span class="sxs-lookup"><span data-stu-id="feec6-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="feec6-184"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="feec6-184"><dt>Winerror.h</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="feec6-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="feec6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feec6-186">Windows 動畫參考</span><span class="sxs-lookup"><span data-stu-id="feec6-186">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

