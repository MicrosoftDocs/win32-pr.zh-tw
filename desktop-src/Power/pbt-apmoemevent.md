---
description: 通知應用程式 APM BIOS 已發出 APM OEM 事件的信號。
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: 'PBT_APMOEMEVENT (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a99b99bdaf69b1a53a24ad33cd898fd1c806694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977051"
---
# <a name="pbt_apmoemevent-event"></a><span data-ttu-id="acd28-103">PBT \_ APMOEMEVENT 事件</span><span class="sxs-lookup"><span data-stu-id="acd28-103">PBT\_APMOEMEVENT event</span></span>

<span data-ttu-id="acd28-104">\[PBT \_ APMOEMEVENT 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="acd28-104">\[PBT\_APMOEMEVENT is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="acd28-105">此事件的支援已在 Windows Vista 中移除。\]</span><span class="sxs-lookup"><span data-stu-id="acd28-105">Support for this event was removed in Windows Vista.\]</span></span>

<span data-ttu-id="acd28-106">通知應用程式 APM BIOS 已發出 APM OEM 事件的信號。</span><span class="sxs-lookup"><span data-stu-id="acd28-106">Notifies applications that the APM BIOS has signaled an APM OEM event.</span></span>

<span data-ttu-id="acd28-107">視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。</span><span class="sxs-lookup"><span data-stu-id="acd28-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="acd28-108">*WParam* 和 *lParam* 參數的設定方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="acd28-108">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
```



## <a name="parameters"></a><span data-ttu-id="acd28-109">參數</span><span class="sxs-lookup"><span data-stu-id="acd28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acd28-110">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="acd28-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="acd28-111">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="acd28-111">A handle to window.</span></span>

<span data-ttu-id="acd28-112"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="acd28-112"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="acd28-113">值</span><span class="sxs-lookup"><span data-stu-id="acd28-113">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="acd28-114">意義</span><span class="sxs-lookup"><span data-stu-id="acd28-114">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="acd28-115"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="acd28-115"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="acd28-116">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="acd28-116">Message identifier.</span></span><br/> |



 

<span data-ttu-id="acd28-117"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="acd28-117"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="acd28-118">值</span><span class="sxs-lookup"><span data-stu-id="acd28-118">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="acd28-119">意義</span><span class="sxs-lookup"><span data-stu-id="acd28-119">Meaning</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <span data-ttu-id="acd28-120"><dt>**PBT \_APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="acd28-120"><dt>**PBT\_APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span></span> </dl> | <span data-ttu-id="acd28-121">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="acd28-121">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="acd28-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acd28-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acd28-123">由系統 APM BIOS 發出信號的 OEM 定義事件代碼。</span><span class="sxs-lookup"><span data-stu-id="acd28-123">The OEM-defined event code that was signaled by the system's APM BIOS.</span></span> <span data-ttu-id="acd28-124">OEM 事件碼位於 0200h-02FFh 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="acd28-124">OEM event codes are in the range 0200h - 02FFh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acd28-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="acd28-125">Return value</span></span>

<span data-ttu-id="acd28-126">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="acd28-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acd28-127">備註</span><span class="sxs-lookup"><span data-stu-id="acd28-127">Remarks</span></span>

<span data-ttu-id="acd28-128">因為並非所有 APM BIOS 都提供 OEM 事件通知，所以在某些電腦上可能永遠不會廣播此事件。</span><span class="sxs-lookup"><span data-stu-id="acd28-128">Because not all APM BIOS implementations provide OEM event notifications, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="acd28-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="acd28-129">Requirements</span></span>



| <span data-ttu-id="acd28-130">需求</span><span class="sxs-lookup"><span data-stu-id="acd28-130">Requirement</span></span> | <span data-ttu-id="acd28-131">值</span><span class="sxs-lookup"><span data-stu-id="acd28-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acd28-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acd28-132">Minimum supported client</span></span><br/> | <span data-ttu-id="acd28-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acd28-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="acd28-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acd28-134">Minimum supported server</span></span><br/> | <span data-ttu-id="acd28-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acd28-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="acd28-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="acd28-136">End of client support</span></span><br/>    | <span data-ttu-id="acd28-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="acd28-137">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="acd28-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="acd28-138">End of server support</span></span><br/>    | <span data-ttu-id="acd28-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="acd28-139">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="acd28-140">標頭</span><span class="sxs-lookup"><span data-stu-id="acd28-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="acd28-141"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="acd28-141"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acd28-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acd28-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acd28-143">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="acd28-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="acd28-144">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="acd28-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




