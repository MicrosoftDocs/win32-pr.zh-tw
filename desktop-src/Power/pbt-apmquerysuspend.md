---
description: 要求暫停電腦的許可權。 授與使用權限的應用程式在回傳之前應該要執行暫停的準備。
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: 'PBT_APMQUERYSUSPEND (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849268"
---
# <a name="pbt_apmquerysuspend-event"></a><span data-ttu-id="c06ed-104">PBT \_ APMQUERYSUSPEND 事件</span><span class="sxs-lookup"><span data-stu-id="c06ed-104">PBT\_APMQUERYSUSPEND event</span></span>

<span data-ttu-id="c06ed-105">\[PBT \_ APMQUERYSUSPEND 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c06ed-105">\[PBT\_APMQUERYSUSPEND is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c06ed-106">此事件的支援已在 Windows Vista 中移除。</span><span class="sxs-lookup"><span data-stu-id="c06ed-106">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="c06ed-107">請改用 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 。\]</span><span class="sxs-lookup"><span data-stu-id="c06ed-107">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="c06ed-108">要求暫停電腦的許可權。</span><span class="sxs-lookup"><span data-stu-id="c06ed-108">Requests permission to suspend the computer.</span></span> <span data-ttu-id="c06ed-109">授與使用權限的應用程式在回傳之前應該要執行暫停的準備。</span><span class="sxs-lookup"><span data-stu-id="c06ed-109">An application that grants permission should carry out preparations for the suspension before returning.</span></span>

<span data-ttu-id="c06ed-110">視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。</span><span class="sxs-lookup"><span data-stu-id="c06ed-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="c06ed-111">*WParam* 和 *lParam* 參數的設定方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="c06ed-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a><span data-ttu-id="c06ed-112">參數</span><span class="sxs-lookup"><span data-stu-id="c06ed-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c06ed-113">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="c06ed-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c06ed-114">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c06ed-114">A handle to window.</span></span>

<span data-ttu-id="c06ed-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="c06ed-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="c06ed-116">值</span><span class="sxs-lookup"><span data-stu-id="c06ed-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="c06ed-117">意義</span><span class="sxs-lookup"><span data-stu-id="c06ed-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="c06ed-118"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="c06ed-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="c06ed-119">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="c06ed-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="c06ed-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="c06ed-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="c06ed-121">值</span><span class="sxs-lookup"><span data-stu-id="c06ed-121">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="c06ed-122">意義</span><span class="sxs-lookup"><span data-stu-id="c06ed-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <span data-ttu-id="c06ed-123"><dt>**PBT \_APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c06ed-123"><dt>**PBT\_APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c06ed-124">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c06ed-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c06ed-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c06ed-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c06ed-126">動作旗標。</span><span class="sxs-lookup"><span data-stu-id="c06ed-126">The action flags.</span></span> <span data-ttu-id="c06ed-127">如果位0是1，則應用程式可以提示使用者如何準備暫停的指示;否則，應用程式必須在沒有使用者互動的情況下做好準備。</span><span class="sxs-lookup"><span data-stu-id="c06ed-127">If bit 0 is 1, the application can prompt the user for directions on how to prepare for the suspension; otherwise, the application must prepare without user interaction.</span></span> <span data-ttu-id="c06ed-128">所有其他位值都是保留的。</span><span class="sxs-lookup"><span data-stu-id="c06ed-128">All other bit values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c06ed-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="c06ed-129">Return value</span></span>

<span data-ttu-id="c06ed-130">傳回 **TRUE** 以授與暫止的要求。</span><span class="sxs-lookup"><span data-stu-id="c06ed-130">Return **TRUE** to grant the request to suspend.</span></span> <span data-ttu-id="c06ed-131">若要拒絕要求，請退回 **廣播 \_ 查詢 \_ 拒絕**。</span><span class="sxs-lookup"><span data-stu-id="c06ed-131">To deny the request, return **BROADCAST\_QUERY\_DENY**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c06ed-132">備註</span><span class="sxs-lookup"><span data-stu-id="c06ed-132">Remarks</span></span>

<span data-ttu-id="c06ed-133">應用程式應該儘快處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="c06ed-133">An application should process this event as quickly as possible.</span></span> <span data-ttu-id="c06ed-134">只有在已設定 *Flags* 參數中的位0時，應用程式才會提示使用者提供如何準備暫停的指示。</span><span class="sxs-lookup"><span data-stu-id="c06ed-134">The application can prompt the user for directions on how to prepare for suspension only if bit 0 in the *Flags* parameter is set.</span></span> <span data-ttu-id="c06ed-135">但是，如果此訊息是因為使用者正在關閉膝上型電腦而發出的，則無法提示使用者。</span><span class="sxs-lookup"><span data-stu-id="c06ed-135">However, if this message is issued because the user is closing the laptop lid, it will not be possible to prompt the user.</span></span> <span data-ttu-id="c06ed-136">當應用程式關閉膝上型電腦蓋或按下電源按鈕並允許轉換成功時，應用程式應該遵守特定的行為。</span><span class="sxs-lookup"><span data-stu-id="c06ed-136">Applications should respect that the user expects a certain behavior when they close the laptop lid or press the power button and allow the transition to succeed.</span></span>

<span data-ttu-id="c06ed-137">系統大約需要20秒的時間，應用程式才能移除從應用程式訊息佇列傳送 PBT APMQUERYSUSPEND 事件的 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c06ed-137">The system allows approximately 20 seconds for an application to remove the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message that is sending the PBT\_APMQUERYSUSPEND event from the application's message queue.</span></span> <span data-ttu-id="c06ed-138">如果應用程式未在20秒內從佇列中移除訊息，系統會假設應用程式處於沒有回應的狀態，而且應用程式會同意睡眠要求。</span><span class="sxs-lookup"><span data-stu-id="c06ed-138">If an application does not remove the message from its queue in less than 20 seconds, the system will assume that the application is in a non-responsive state, and that the application agrees to the sleep request.</span></span> <span data-ttu-id="c06ed-139">未處理其訊息佇列的應用程式可能會中斷其作業。</span><span class="sxs-lookup"><span data-stu-id="c06ed-139">Applications that do not process their message queues may have their operations interrupted.</span></span> <span data-ttu-id="c06ed-140">從訊息佇列中移除訊息之後，應用程式可能需要花費太多時間才能在進入睡眠狀態之前執行任何必要的作業。</span><span class="sxs-lookup"><span data-stu-id="c06ed-140">After it removes the message from the message queue, an application can take as much time as needed to perform any required operations before entering the sleep state.</span></span> <span data-ttu-id="c06ed-141">這次可能需要花費較長20秒的作業，因為系統只允許20秒的時間讓作業在 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 處理期間完成。</span><span class="sxs-lookup"><span data-stu-id="c06ed-141">Any operations that could take longer then 20 seconds should be performed at this time, since the system allows only 20 seconds for operations to complete during [PBT\_APMSUSPEND](pbt-apmsuspend.md) processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c06ed-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="c06ed-142">Requirements</span></span>



| <span data-ttu-id="c06ed-143">需求</span><span class="sxs-lookup"><span data-stu-id="c06ed-143">Requirement</span></span> | <span data-ttu-id="c06ed-144">值</span><span class="sxs-lookup"><span data-stu-id="c06ed-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c06ed-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c06ed-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c06ed-146">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c06ed-146">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c06ed-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c06ed-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c06ed-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c06ed-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c06ed-149">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c06ed-149">End of client support</span></span><br/>    | <span data-ttu-id="c06ed-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c06ed-150">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="c06ed-151">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c06ed-151">End of server support</span></span><br/>    | <span data-ttu-id="c06ed-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c06ed-152">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="c06ed-153">標頭</span><span class="sxs-lookup"><span data-stu-id="c06ed-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="c06ed-154"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c06ed-154"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c06ed-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c06ed-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c06ed-156">系統喚醒事件</span><span class="sxs-lookup"><span data-stu-id="c06ed-156">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="c06ed-157">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="c06ed-157">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="c06ed-158">PBT \_ APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="c06ed-158">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="c06ed-159">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="c06ed-159">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




