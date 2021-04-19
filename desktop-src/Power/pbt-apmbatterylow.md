---
description: 通知應用程式電池電力偏低。
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: 'PBT_APMBATTERYLOW (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997528"
---
# <a name="pbt_apmbatterylow-event"></a><span data-ttu-id="65e91-103">PBT \_ APMBATTERYLOW 事件</span><span class="sxs-lookup"><span data-stu-id="65e91-103">PBT\_APMBATTERYLOW event</span></span>

<span data-ttu-id="65e91-104">\[PBT \_ APMBATTERYLOW 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="65e91-104">\[PBT\_APMBATTERYLOW is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="65e91-105">此事件的支援已在 Windows Vista 中移除。</span><span class="sxs-lookup"><span data-stu-id="65e91-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="65e91-106">請改用 [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="65e91-106">Use [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) instead.\]</span></span>

<span data-ttu-id="65e91-107">通知應用程式電池電力偏低。</span><span class="sxs-lookup"><span data-stu-id="65e91-107">Notifies applications that the battery power is low.</span></span>

<span data-ttu-id="65e91-108">視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。</span><span class="sxs-lookup"><span data-stu-id="65e91-108">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="65e91-109">*WParam* 和 *lParam* 參數的設定方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="65e91-109">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="65e91-110">參數</span><span class="sxs-lookup"><span data-stu-id="65e91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65e91-111">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="65e91-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="65e91-112">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="65e91-112">A handle to the window.</span></span>

<span data-ttu-id="65e91-113"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="65e91-113"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="65e91-114">值</span><span class="sxs-lookup"><span data-stu-id="65e91-114">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="65e91-115">意義</span><span class="sxs-lookup"><span data-stu-id="65e91-115">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="65e91-116"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="65e91-116"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="65e91-117">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="65e91-117">Message identifier.</span></span><br/> |



 

<span data-ttu-id="65e91-118"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="65e91-118"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="65e91-119">值</span><span class="sxs-lookup"><span data-stu-id="65e91-119">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="65e91-120">意義</span><span class="sxs-lookup"><span data-stu-id="65e91-120">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <span data-ttu-id="65e91-121"><dt>**PBT \_APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="65e91-121"><dt>**PBT\_APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span></span> </dl> | <span data-ttu-id="65e91-122">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="65e91-122">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="65e91-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65e91-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65e91-124">Reserved，必須為零。</span><span class="sxs-lookup"><span data-stu-id="65e91-124">Reserved, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65e91-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="65e91-125">Return value</span></span>

<span data-ttu-id="65e91-126">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="65e91-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65e91-127">備註</span><span class="sxs-lookup"><span data-stu-id="65e91-127">Remarks</span></span>

<span data-ttu-id="65e91-128">當系統的 APM BIOS 發出 APM 電池低通知時，就會廣播此事件。</span><span class="sxs-lookup"><span data-stu-id="65e91-128">This event is broadcast when a system's APM BIOS signals an APM battery low notification.</span></span> <span data-ttu-id="65e91-129">因為某些 APM BIOS 的執行不會在電池偏低時提供通知，所以在某些電腦上可能永遠不會廣播此事件。</span><span class="sxs-lookup"><span data-stu-id="65e91-129">Because some APM BIOS implementations do not provide notifications when batteries are low, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="65e91-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="65e91-130">Requirements</span></span>



| <span data-ttu-id="65e91-131">需求</span><span class="sxs-lookup"><span data-stu-id="65e91-131">Requirement</span></span> | <span data-ttu-id="65e91-132">值</span><span class="sxs-lookup"><span data-stu-id="65e91-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e91-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65e91-133">Minimum supported client</span></span><br/> | <span data-ttu-id="65e91-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65e91-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="65e91-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65e91-135">Minimum supported server</span></span><br/> | <span data-ttu-id="65e91-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65e91-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="65e91-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="65e91-137">End of client support</span></span><br/>    | <span data-ttu-id="65e91-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="65e91-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="65e91-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="65e91-139">End of server support</span></span><br/>    | <span data-ttu-id="65e91-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65e91-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="65e91-141">標頭</span><span class="sxs-lookup"><span data-stu-id="65e91-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="65e91-142"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="65e91-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65e91-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65e91-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e91-144">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="65e91-144">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="65e91-145">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="65e91-145">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




