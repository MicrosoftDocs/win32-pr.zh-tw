---
description: 通知應用程式，在暫停後系統已繼續操作。
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: 'PBT_APMRESUMESUSPEND (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987533"
---
# <a name="pbt_apmresumesuspend-event"></a><span data-ttu-id="ac0f1-103">PBT \_ APMRESUMESUSPEND 事件</span><span class="sxs-lookup"><span data-stu-id="ac0f1-103">PBT\_APMRESUMESUSPEND event</span></span>

<span data-ttu-id="ac0f1-104">通知應用程式，在暫停後系統已繼續操作。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-104">Notifies applications that the system has resumed operation after being suspended.</span></span>

<span data-ttu-id="ac0f1-105">視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-105">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="ac0f1-106">*WParam* 和 *lParam* 參數的設定方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-106">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="ac0f1-107">參數</span><span class="sxs-lookup"><span data-stu-id="ac0f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac0f1-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="ac0f1-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ac0f1-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-109">A handle to window.</span></span>

<span data-ttu-id="ac0f1-110"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="ac0f1-110"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="ac0f1-111">值</span><span class="sxs-lookup"><span data-stu-id="ac0f1-111">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="ac0f1-112">意義</span><span class="sxs-lookup"><span data-stu-id="ac0f1-112">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="ac0f1-113"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="ac0f1-113"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="ac0f1-114">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-114">Message identifier.</span></span><br/> |



 

<span data-ttu-id="ac0f1-115"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="ac0f1-115"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="ac0f1-116">值</span><span class="sxs-lookup"><span data-stu-id="ac0f1-116">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="ac0f1-117">意義</span><span class="sxs-lookup"><span data-stu-id="ac0f1-117">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="ac0f1-118"><dt>**PBT \_APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="ac0f1-118"><dt>**PBT\_APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span></span> </dl> | <span data-ttu-id="ac0f1-119">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-119">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ac0f1-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac0f1-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac0f1-121">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-121">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac0f1-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac0f1-122">Return value</span></span>

<span data-ttu-id="ac0f1-123">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-123">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac0f1-124">備註</span><span class="sxs-lookup"><span data-stu-id="ac0f1-124">Remarks</span></span>

<span data-ttu-id="ac0f1-125">只有當應用程式在電腦暫停之前收到 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件時，才會收到此事件。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-125">An application can receive this event only if it received the [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended.</span></span> <span data-ttu-id="ac0f1-126">否則，應用程式將會收到 [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-126">Otherwise, the application will receive a [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event.</span></span>

<span data-ttu-id="ac0f1-127">如果系統因為使用者活動而喚醒 (例如按下電源按鈕) ，或系統在實體主控台上偵測到使用者互動 (例如在喚醒的情況下使用滑鼠或鍵盤輸入) ，則系統會先廣播 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 事件，然後再廣播 PBT \_ APMRESUMESUSPEND 事件。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-127">If the system wakes due to user activity (such as pressing the power button) or if the system detects user interaction at the physical console (such as mouse or keyboard input) after waking unattended, the system first broadcasts the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event, then it broadcasts the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="ac0f1-128">此外，系統也會開啟顯示器。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-128">In addition, the system turns on the display.</span></span> <span data-ttu-id="ac0f1-129">您的應用程式應該在系統進入睡眠狀態時重新開啟已關閉的檔案，並為使用者輸入做好準備。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-129">Your application should reopen files that it closed when the system entered sleep and prepare for user input.</span></span>

<span data-ttu-id="ac0f1-130">如果系統因為外部喚醒信號而喚醒 (遠端喚醒) ，系統只會廣播 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-130">If the system wakes due to an external wake signal (remote wake), the system broadcasts only the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event.</span></span> <span data-ttu-id="ac0f1-131">PBT \_ APMRESUMESUSPEND 事件不會傳送。</span><span class="sxs-lookup"><span data-stu-id="ac0f1-131">The PBT\_APMRESUMESUSPEND event is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac0f1-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac0f1-132">Requirements</span></span>



| <span data-ttu-id="ac0f1-133">需求</span><span class="sxs-lookup"><span data-stu-id="ac0f1-133">Requirement</span></span> | <span data-ttu-id="ac0f1-134">值</span><span class="sxs-lookup"><span data-stu-id="ac0f1-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0f1-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac0f1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ac0f1-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac0f1-136">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ac0f1-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac0f1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ac0f1-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac0f1-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ac0f1-139">標頭</span><span class="sxs-lookup"><span data-stu-id="ac0f1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac0f1-140"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ac0f1-140"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac0f1-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac0f1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac0f1-142">系統喚醒事件</span><span class="sxs-lookup"><span data-stu-id="ac0f1-142">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="ac0f1-143">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="ac0f1-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="ac0f1-144">PBT \_ APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="ac0f1-144">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="ac0f1-145">PBT \_ APMRESUMECRITICAL</span><span class="sxs-lookup"><span data-stu-id="ac0f1-145">PBT\_APMRESUMECRITICAL</span></span>](pbt-apmresumecritical.md)
</dt> <dt>

[<span data-ttu-id="ac0f1-146">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="ac0f1-146">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




