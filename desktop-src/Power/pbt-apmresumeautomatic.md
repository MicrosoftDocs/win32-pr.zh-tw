---
description: 通知應用程式系統正在從睡眠或休眠狀態繼續進行。 此事件會在每次系統繼續時傳遞，且不會指出使用者是否存在。
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: 'PBT_APMRESUMEAUTOMATIC (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849267"
---
# <a name="pbt_apmresumeautomatic-event"></a><span data-ttu-id="593ea-104">PBT \_ APMRESUMEAUTOMATIC 事件</span><span class="sxs-lookup"><span data-stu-id="593ea-104">PBT\_APMRESUMEAUTOMATIC event</span></span>

<span data-ttu-id="593ea-105">通知應用程式系統正在從睡眠或休眠狀態繼續進行。</span><span class="sxs-lookup"><span data-stu-id="593ea-105">Notifies applications that the system is resuming from sleep or hibernation.</span></span> <span data-ttu-id="593ea-106">此事件會在每次系統繼續時傳遞，且不會指出使用者是否存在。</span><span class="sxs-lookup"><span data-stu-id="593ea-106">This event is delivered every time the system resumes and does not indicate whether a user is present.</span></span>

<span data-ttu-id="593ea-107">視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。</span><span class="sxs-lookup"><span data-stu-id="593ea-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="593ea-108">*WParam* 和 *lParam* 參數的設定方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="593ea-108">The *wParam* and *lParam* parameters are set as described following.</span></span>

> [!Note]  
> <span data-ttu-id="593ea-109">在 Windows 10 的1507系統或更新版本中，如果系統從睡眠狀態只繼續進入休眠狀態，則不會傳遞此事件。</span><span class="sxs-lookup"><span data-stu-id="593ea-109">In Windows 10, version 1507 systems or later, if the system is resuming from sleep only to immediately enter hibernation, this event is not delivered.</span></span> <span data-ttu-id="593ea-110">在此情況下，不會傳送 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="593ea-110">A [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message is not sent in this case.</span></span>

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="593ea-111">參數</span><span class="sxs-lookup"><span data-stu-id="593ea-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="593ea-112">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="593ea-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="593ea-113">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="593ea-113">A handle to window.</span></span>

<span data-ttu-id="593ea-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="593ea-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="593ea-115">值</span><span class="sxs-lookup"><span data-stu-id="593ea-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="593ea-116">意義</span><span class="sxs-lookup"><span data-stu-id="593ea-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="593ea-117"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="593ea-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="593ea-118">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="593ea-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="593ea-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="593ea-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="593ea-120">值</span><span class="sxs-lookup"><span data-stu-id="593ea-120">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="593ea-121">意義</span><span class="sxs-lookup"><span data-stu-id="593ea-121">Meaning</span></span>                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="593ea-122"><dt>**PBT \_APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="593ea-122"><dt>**PBT\_APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="593ea-123">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="593ea-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="593ea-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="593ea-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="593ea-125">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="593ea-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="593ea-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="593ea-126">Return value</span></span>

<span data-ttu-id="593ea-127">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="593ea-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="593ea-128">備註</span><span class="sxs-lookup"><span data-stu-id="593ea-128">Remarks</span></span>

<span data-ttu-id="593ea-129">如果系統在廣播 PBT APMRESUMEAUTOMATIC 之後偵測到任何使用者活動 \_ ，它會廣播 [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) 事件，讓應用程式知道他們可以繼續與使用者進行完全互動。</span><span class="sxs-lookup"><span data-stu-id="593ea-129">If the system detects any user activity after broadcasting PBT\_APMRESUMEAUTOMATIC, it will broadcast a [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) event to let applications know they can resume full interaction with the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="593ea-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="593ea-130">Requirements</span></span>



| <span data-ttu-id="593ea-131">需求</span><span class="sxs-lookup"><span data-stu-id="593ea-131">Requirement</span></span> | <span data-ttu-id="593ea-132">值</span><span class="sxs-lookup"><span data-stu-id="593ea-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="593ea-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="593ea-133">Minimum supported client</span></span><br/> | <span data-ttu-id="593ea-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="593ea-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="593ea-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="593ea-135">Minimum supported server</span></span><br/> | <span data-ttu-id="593ea-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="593ea-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="593ea-137">標頭</span><span class="sxs-lookup"><span data-stu-id="593ea-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="593ea-138"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="593ea-138"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="593ea-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="593ea-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="593ea-140">系統喚醒事件</span><span class="sxs-lookup"><span data-stu-id="593ea-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="593ea-141">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="593ea-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="593ea-142">PBT \_ APMRESUMESUSPEND</span><span class="sxs-lookup"><span data-stu-id="593ea-142">PBT\_APMRESUMESUSPEND</span></span>](pbt-apmresumesuspend.md)
</dt> <dt>

[<span data-ttu-id="593ea-143">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="593ea-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




