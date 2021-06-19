---
description: 通知應用程式發生電源管理事件。
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: 'WM_POWERBROADCAST 訊息 (WinUser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b205a146b731bdf8cf9adc1563621232c24c10b4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396503"
---
# <a name="wm_powerbroadcast-message"></a><span data-ttu-id="e28c1-103">WM \_ POWERBROADCAST 訊息</span><span class="sxs-lookup"><span data-stu-id="e28c1-103">WM\_POWERBROADCAST message</span></span>

<span data-ttu-id="e28c1-104">通知應用程式發生電源管理事件。</span><span class="sxs-lookup"><span data-stu-id="e28c1-104">Notifies applications that a power-management event has occurred.</span></span>

<span data-ttu-id="e28c1-105">視窗會透過其 **WindowProc** 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e28c1-105">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="e28c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="e28c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e28c1-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="e28c1-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e28c1-108">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e28c1-108">A handle to window.</span></span>

</dd> <dt>
  
<span data-ttu-id="e28c1-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="e28c1-109">*uMsg*</span></span>
</dt> <dd> 

| <span data-ttu-id="e28c1-110">值</span><span class="sxs-lookup"><span data-stu-id="e28c1-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="e28c1-111">意義</span><span class="sxs-lookup"><span data-stu-id="e28c1-111">Meaning</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="e28c1-112"><dt>\* \* \* \* WM \_POWERBROADCAST \* \*</dt> \* <dt>536 (0x218) </dt></span><span class="sxs-lookup"><span data-stu-id="e28c1-112"><dt>\*\*\*\*WM\_POWERBROADCAST\*\*\*\*</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="e28c1-113">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="e28c1-113">Message identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e28c1-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e28c1-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e28c1-115">電源管理事件。</span><span class="sxs-lookup"><span data-stu-id="e28c1-115">The power-management event.</span></span> <span data-ttu-id="e28c1-116">此參數可以是下列其中一個事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e28c1-116">This parameter can be one of the following event identifiers.</span></span>



| <span data-ttu-id="e28c1-117">事件</span><span class="sxs-lookup"><span data-stu-id="e28c1-117">Event</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="e28c1-118">意義</span><span class="sxs-lookup"><span data-stu-id="e28c1-118">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="e28c1-119"><dt>**[PBT \_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="e28c1-119"><dt>**[PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="e28c1-120">電源狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="e28c1-120">Power status has changed.</span></span><br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="e28c1-121"><dt>**[PBT \_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="e28c1-121"><dt>**[PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span></span> </dl>        | <span data-ttu-id="e28c1-122">作業從低電源狀態自動繼續。</span><span class="sxs-lookup"><span data-stu-id="e28c1-122">Operation is resuming automatically from a low-power state.</span></span> <span data-ttu-id="e28c1-123">每次系統繼續時，就會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e28c1-123">This message is sent every time the system resumes.</span></span><br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="e28c1-124"><dt>**[PBT \_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="e28c1-124"><dt>**[PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span></span> </dl>                  | <span data-ttu-id="e28c1-125">作業正在從低電源狀態繼續。</span><span class="sxs-lookup"><span data-stu-id="e28c1-125">Operation is resuming from a low-power state.</span></span> <span data-ttu-id="e28c1-126">如果使用者輸入觸發繼續（例如按下某個按鍵），則會在 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 之後傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e28c1-126">This message is sent after [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) if the resume is triggered by user input, such as pressing a key.</span></span><br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="e28c1-127"><dt>**[PBT \_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="e28c1-127"><dt>**[PBT\_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                          | <span data-ttu-id="e28c1-128">系統正在暫停操作。</span><span class="sxs-lookup"><span data-stu-id="e28c1-128">System is suspending operation.</span></span><br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="e28c1-129"><dt>**[PBT \_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="e28c1-129"><dt>**[PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span></span> </dl>   | <span data-ttu-id="e28c1-130">已收到電源設定變更事件。</span><span class="sxs-lookup"><span data-stu-id="e28c1-130">A power setting change event has been received.</span></span> <br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="e28c1-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e28c1-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e28c1-132">事件特定資料。</span><span class="sxs-lookup"><span data-stu-id="e28c1-132">The event-specific data.</span></span> <span data-ttu-id="e28c1-133">對於大部分的事件，此參數是保留的，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="e28c1-133">For most events, this parameter is reserved and not used.</span></span>

<span data-ttu-id="e28c1-134">如果 *wParam* 參數為 [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)，則 *lParam* 參數是 [**POWERBROADCAST \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e28c1-134">If the *wParam* parameter is [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md), the *lParam* parameter is a pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e28c1-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="e28c1-135">Return value</span></span>

<span data-ttu-id="e28c1-136">如果應用程式處理此訊息，則應該傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="e28c1-136">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="e28c1-137">備註</span><span class="sxs-lookup"><span data-stu-id="e28c1-137">Remarks</span></span>

<span data-ttu-id="e28c1-138">當系統繼續時，系統一律會傳送 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="e28c1-138">The system always sends a [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) message whenever the system resumes.</span></span> <span data-ttu-id="e28c1-139">如果系統繼續回應使用者輸入，例如按下按鍵，則系統也會在傳送 PBT APMRESUMEAUTOMATIC 之後傳送 **PBT \_ APMRESUMESUSPEND** 訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e28c1-139">If the system resumes in response to user input such as pressing a key, the system also sends a **PBT\_APMRESUMESUSPEND** message after sending PBT\_APMRESUMEAUTOMATIC.</span></span>

<span data-ttu-id="e28c1-140">**WM \_POWERBROADCAST** 訊息不會區分不同的低電源狀態。</span><span class="sxs-lookup"><span data-stu-id="e28c1-140">**WM\_POWERBROADCAST** messages do not distinguish between different low-power states.</span></span> <span data-ttu-id="e28c1-141">應用程式只能判斷系統是否進入或已從低電源狀態繼續;它無法判斷特定的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="e28c1-141">An application can determine only that the system is entering or has resumed from a low-power state; it cannot determine the specific power state.</span></span> <span data-ttu-id="e28c1-142">系統會記錄有關 Windows 系統事件記錄檔中電源狀態轉換的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e28c1-142">The system records details about power state transitions in the Windows System event log.</span></span>

<span data-ttu-id="e28c1-143">為了防止系統轉換成 Windows Vista 的低電源狀態，應用程式必須呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 來通知系統它正在使用中。</span><span class="sxs-lookup"><span data-stu-id="e28c1-143">To prevent the system from transitioning to a low-power state in Windows Vista, an application must call [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) to inform the system that it is in use.</span></span>

<span data-ttu-id="e28c1-144">在 [需求] 區段中指定的任何作業系統上，不支援下列訊息：</span><span class="sxs-lookup"><span data-stu-id="e28c1-144">The following messages are not supported on any of the operating systems specified in the Requirements section:</span></span>

- <span data-ttu-id="e28c1-145">PBT_APMQUERYSTANDBY</span><span class="sxs-lookup"><span data-stu-id="e28c1-145">PBT_APMQUERYSTANDBY</span></span>  
- <span data-ttu-id="e28c1-146">PBT_APMQUERYSTANDBYFAILED</span><span class="sxs-lookup"><span data-stu-id="e28c1-146">PBT_APMQUERYSTANDBYFAILED</span></span>  
- <span data-ttu-id="e28c1-147">PBT_APMSTANDBY</span><span class="sxs-lookup"><span data-stu-id="e28c1-147">PBT_APMSTANDBY</span></span>  
- <span data-ttu-id="e28c1-148">PBT_APMRESUMESTANDBY</span><span class="sxs-lookup"><span data-stu-id="e28c1-148">PBT_APMRESUMESTANDBY</span></span>  

## <a name="requirements"></a><span data-ttu-id="e28c1-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="e28c1-149">Requirements</span></span>



| <span data-ttu-id="e28c1-150">需求</span><span class="sxs-lookup"><span data-stu-id="e28c1-150">Requirement</span></span> | <span data-ttu-id="e28c1-151">值</span><span class="sxs-lookup"><span data-stu-id="e28c1-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e28c1-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e28c1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e28c1-153">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e28c1-153">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e28c1-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e28c1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e28c1-155">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e28c1-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e28c1-156">標頭</span><span class="sxs-lookup"><span data-stu-id="e28c1-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="e28c1-157"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e28c1-157"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e28c1-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e28c1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e28c1-159">WM \_ POWERBROADCAST 訊息</span><span class="sxs-lookup"><span data-stu-id="e28c1-159">WM\_POWERBROADCAST Messages</span></span>](wm-powerbroadcast-messages.md)
</dt> <dt>

[<span data-ttu-id="e28c1-160">電源管理訊息</span><span class="sxs-lookup"><span data-stu-id="e28c1-160">Power Management Messages</span></span>](power-management-messages.md)
</dt> </dl>

 

 




