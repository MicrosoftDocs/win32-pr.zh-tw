---
description: 通知應用程式系統已繼續操作。
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: 'PBT_APMRESUMECRITICAL (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983632"
---
# <a name="pbt_apmresumecritical-event"></a><span data-ttu-id="2c68a-103">PBT \_ APMRESUMECRITICAL 事件</span><span class="sxs-lookup"><span data-stu-id="2c68a-103">PBT\_APMRESUMECRITICAL event</span></span>

<span data-ttu-id="2c68a-104">\[PBT \_ APMRESUMECRITICAL 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2c68a-104">\[PBT\_APMRESUMECRITICAL is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2c68a-105">此事件的支援已在 Windows Vista 中移除。</span><span class="sxs-lookup"><span data-stu-id="2c68a-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="2c68a-106">請改用 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="2c68a-106">Use [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) instead.\]</span></span>

<span data-ttu-id="2c68a-107">通知應用程式系統已繼續操作。</span><span class="sxs-lookup"><span data-stu-id="2c68a-107">Notifies applications that the system has resumed operation.</span></span> <span data-ttu-id="2c68a-108">此事件可能表示部分或所有應用程式未收到 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="2c68a-108">This event can indicate that some or all applications did not receive a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event.</span></span> <span data-ttu-id="2c68a-109">例如，此事件可以在失敗的電池造成重大暫停之後廣播。</span><span class="sxs-lookup"><span data-stu-id="2c68a-109">For example, this event can be broadcast after a critical suspension caused by a failing battery.</span></span>

<span data-ttu-id="2c68a-110">視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。</span><span class="sxs-lookup"><span data-stu-id="2c68a-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="2c68a-111">*WParam* 和 *lParam* 參數的設定方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="2c68a-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="2c68a-112">參數</span><span class="sxs-lookup"><span data-stu-id="2c68a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c68a-113">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="2c68a-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2c68a-114">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2c68a-114">A handle to window.</span></span>

<span data-ttu-id="2c68a-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="2c68a-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="2c68a-116">值</span><span class="sxs-lookup"><span data-stu-id="2c68a-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="2c68a-117">意義</span><span class="sxs-lookup"><span data-stu-id="2c68a-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="2c68a-118"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="2c68a-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="2c68a-119">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c68a-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="2c68a-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="2c68a-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="2c68a-121">值</span><span class="sxs-lookup"><span data-stu-id="2c68a-121">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="2c68a-122">意義</span><span class="sxs-lookup"><span data-stu-id="2c68a-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <span data-ttu-id="2c68a-123"><dt>**PBT \_APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="2c68a-123"><dt>**PBT\_APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="2c68a-124">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c68a-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c68a-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c68a-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c68a-126">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="2c68a-126">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c68a-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c68a-127">Return value</span></span>

<span data-ttu-id="2c68a-128">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c68a-128">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c68a-129">備註</span><span class="sxs-lookup"><span data-stu-id="2c68a-129">Remarks</span></span>

<span data-ttu-id="2c68a-130">由於未事先通知就緊急暫停，因此先前可用的資源和資料在應用程式收到此事件時可能不存在。</span><span class="sxs-lookup"><span data-stu-id="2c68a-130">Because a critical suspension occurs without prior notification, resources and data previously available may not be present when the application receives this event.</span></span> <span data-ttu-id="2c68a-131">應用程式應該嘗試將其狀態還原成其最佳能力。</span><span class="sxs-lookup"><span data-stu-id="2c68a-131">The application should attempt to restore its state to the best of its ability.</span></span> <span data-ttu-id="2c68a-132">在重大的暫止中，系統會維護 DRAM 和本機硬碟的狀態，但可能不會維護網路連接。</span><span class="sxs-lookup"><span data-stu-id="2c68a-132">While in a critical suspension, the system maintains the state of the DRAM and local hard disks, but may not maintain net connections.</span></span> <span data-ttu-id="2c68a-133">應用程式可能需要針對在重大暫停前于網路上開啟的檔案採取行動。</span><span class="sxs-lookup"><span data-stu-id="2c68a-133">An application may need to take action with respect to files that were open on the network before critical suspension.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c68a-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c68a-134">Requirements</span></span>



| <span data-ttu-id="2c68a-135">需求</span><span class="sxs-lookup"><span data-stu-id="2c68a-135">Requirement</span></span> | <span data-ttu-id="2c68a-136">值</span><span class="sxs-lookup"><span data-stu-id="2c68a-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c68a-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c68a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2c68a-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c68a-138">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2c68a-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c68a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2c68a-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c68a-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c68a-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2c68a-141">End of client support</span></span><br/>    | <span data-ttu-id="2c68a-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c68a-142">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="2c68a-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2c68a-143">End of server support</span></span><br/>    | <span data-ttu-id="2c68a-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c68a-144">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="2c68a-145">標頭</span><span class="sxs-lookup"><span data-stu-id="2c68a-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c68a-146"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2c68a-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c68a-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c68a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c68a-148">系統喚醒事件</span><span class="sxs-lookup"><span data-stu-id="2c68a-148">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="2c68a-149">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="2c68a-149">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="2c68a-150">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="2c68a-150">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




