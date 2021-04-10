---
description: 通知應用程式電腦即將進入暫停狀態。
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: 'PBT_APMSUSPEND (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6982e00565329c85e06765879b9b72b07fe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192769"
---
# <a name="pbt_apmsuspend-event"></a><span data-ttu-id="5d83f-103">PBT \_ APMSUSPEND 事件</span><span class="sxs-lookup"><span data-stu-id="5d83f-103">PBT\_APMSUSPEND event</span></span>

<span data-ttu-id="5d83f-104">通知應用程式電腦即將進入暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="5d83f-104">Notifies applications that the computer is about to enter a suspended state.</span></span> <span data-ttu-id="5d83f-105">此事件通常會在所有應用程式和可安裝的驅動程式都傳回 **TRUE** 至先前的 [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) 事件時廣播。</span><span class="sxs-lookup"><span data-stu-id="5d83f-105">This event is typically broadcast when all applications and installable drivers have returned **TRUE** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="5d83f-106">視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。</span><span class="sxs-lookup"><span data-stu-id="5d83f-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="5d83f-107">*WParam* 和 *lParam* 參數的設定方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="5d83f-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="5d83f-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d83f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d83f-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="5d83f-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5d83f-110">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5d83f-110">A handle to window.</span></span>

<span data-ttu-id="5d83f-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="5d83f-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="5d83f-112">值</span><span class="sxs-lookup"><span data-stu-id="5d83f-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="5d83f-113">意義</span><span class="sxs-lookup"><span data-stu-id="5d83f-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="5d83f-114"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="5d83f-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="5d83f-115">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d83f-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="5d83f-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="5d83f-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="5d83f-117">值</span><span class="sxs-lookup"><span data-stu-id="5d83f-117">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="5d83f-118">意義</span><span class="sxs-lookup"><span data-stu-id="5d83f-118">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="5d83f-119"><dt>**PBT \_APMSUSPEND**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="5d83f-119"><dt>**PBT\_APMSUSPEND**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="5d83f-120">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d83f-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5d83f-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d83f-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d83f-122">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="5d83f-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d83f-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d83f-123">Return value</span></span>

<span data-ttu-id="5d83f-124">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5d83f-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d83f-125">備註</span><span class="sxs-lookup"><span data-stu-id="5d83f-125">Remarks</span></span>

<span data-ttu-id="5d83f-126">應用程式應該藉由完成儲存資料所需的所有工作來處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="5d83f-126">An application should process this event by completing all tasks necessary to save data.</span></span>

<span data-ttu-id="5d83f-127">系統大約需要兩秒鐘的時間讓應用程式處理此通知。</span><span class="sxs-lookup"><span data-stu-id="5d83f-127">The system allows approximately two seconds for an application to handle this notification.</span></span> <span data-ttu-id="5d83f-128">如果應用程式在其時間配額到期之後仍在執行作業，系統可能會中斷應用程式。</span><span class="sxs-lookup"><span data-stu-id="5d83f-128">If an application is still performing operations after its time allotment has expired, the system may interrupt the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d83f-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d83f-129">Requirements</span></span>



| <span data-ttu-id="5d83f-130">需求</span><span class="sxs-lookup"><span data-stu-id="5d83f-130">Requirement</span></span> | <span data-ttu-id="5d83f-131">值</span><span class="sxs-lookup"><span data-stu-id="5d83f-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d83f-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d83f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5d83f-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d83f-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5d83f-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d83f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5d83f-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d83f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5d83f-136">標頭</span><span class="sxs-lookup"><span data-stu-id="5d83f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d83f-137"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5d83f-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d83f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d83f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d83f-139">系統睡眠準則</span><span class="sxs-lookup"><span data-stu-id="5d83f-139">System Sleep Criteria</span></span>](system-sleep-criteria.md)
</dt> <dt>

[<span data-ttu-id="5d83f-140">系統喚醒事件</span><span class="sxs-lookup"><span data-stu-id="5d83f-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="5d83f-141">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="5d83f-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="5d83f-142">PBT \_ APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="5d83f-142">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="5d83f-143">**SetSystemPowerState**</span><span class="sxs-lookup"><span data-stu-id="5d83f-143">**SetSystemPowerState**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[<span data-ttu-id="5d83f-144">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="5d83f-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




