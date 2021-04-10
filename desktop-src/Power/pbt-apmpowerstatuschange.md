---
description: 通知應用程式電源狀態的變更，例如從電池電源切換至 A/C。
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: 'PBT_APMPOWERSTATUSCHANGE (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192770"
---
# <a name="pbt_apmpowerstatuschange-event"></a><span data-ttu-id="5b17e-103">PBT \_ APMPOWERSTATUSCHANGE 事件</span><span class="sxs-lookup"><span data-stu-id="5b17e-103">PBT\_APMPOWERSTATUSCHANGE event</span></span>

<span data-ttu-id="5b17e-104">通知應用程式電源狀態的變更，例如從電池電源切換至 A/C。</span><span class="sxs-lookup"><span data-stu-id="5b17e-104">Notifies applications of a change in the power status of the computer, such as a switch from battery power to A/C.</span></span> <span data-ttu-id="5b17e-105">當剩餘電池的電力下滑至使用者所指定的臨界值之下，或是如果電池的電力由指定百分比來變更時，系統也會廣播這個事件。</span><span class="sxs-lookup"><span data-stu-id="5b17e-105">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

<span data-ttu-id="5b17e-106">視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。</span><span class="sxs-lookup"><span data-stu-id="5b17e-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="5b17e-107">*WParam* 和 *lParam* 參數的設定方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="5b17e-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMPOWERSTATUSCHANGE
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="5b17e-108">參數</span><span class="sxs-lookup"><span data-stu-id="5b17e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b17e-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="5b17e-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5b17e-110">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5b17e-110">A handle to window.</span></span>

<span data-ttu-id="5b17e-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="5b17e-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="5b17e-112">值</span><span class="sxs-lookup"><span data-stu-id="5b17e-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="5b17e-113">意義</span><span class="sxs-lookup"><span data-stu-id="5b17e-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="5b17e-114"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="5b17e-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="5b17e-115">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b17e-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="5b17e-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="5b17e-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="5b17e-117">值</span><span class="sxs-lookup"><span data-stu-id="5b17e-117">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="5b17e-118">意義</span><span class="sxs-lookup"><span data-stu-id="5b17e-118">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="5b17e-119"><dt>**PBT \_APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="5b17e-119"><dt>**PBT\_APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="5b17e-120">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b17e-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5b17e-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b17e-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b17e-122">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="5b17e-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b17e-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b17e-123">Return value</span></span>

<span data-ttu-id="5b17e-124">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5b17e-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b17e-125">備註</span><span class="sxs-lookup"><span data-stu-id="5b17e-125">Remarks</span></span>

<span data-ttu-id="5b17e-126">應用程式應該藉由呼叫 [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) 函式來取得電腦目前的電源狀態，來處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="5b17e-126">An application should process this event by calling the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve the current power status of the computer.</span></span> <span data-ttu-id="5b17e-127">尤其是，應用程式應該檢查 [**系統 \_ 電源 \_ 狀態**](/windows/desktop/api/Winbase/ns-winbase-system_power_status)結構的 **sps.aclinestatus**、 **BatteryFlag**、 **BatteryLifeTime** 和 **BatteryLifePercent** 成員是否有任何變更。</span><span class="sxs-lookup"><span data-stu-id="5b17e-127">In particular, the application should check the **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime**, and **BatteryLifePercent** members of the [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) structure for any changes.</span></span> <span data-ttu-id="5b17e-128">當電池壽命降至5分鐘以內，或電池壽命的百分比低於10%，或電池壽命變更為3% 時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="5b17e-128">This event can occur when battery life drops to less than 5 minutes, or when the percentage of battery life drops below 10 percent, or if the battery life changes by 3 percent.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b17e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b17e-129">Requirements</span></span>



| <span data-ttu-id="5b17e-130">需求</span><span class="sxs-lookup"><span data-stu-id="5b17e-130">Requirement</span></span> | <span data-ttu-id="5b17e-131">值</span><span class="sxs-lookup"><span data-stu-id="5b17e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b17e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b17e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5b17e-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b17e-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5b17e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b17e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5b17e-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b17e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b17e-136">標頭</span><span class="sxs-lookup"><span data-stu-id="5b17e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b17e-137"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5b17e-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b17e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b17e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b17e-139">系統電源狀態</span><span class="sxs-lookup"><span data-stu-id="5b17e-139">System Power Status</span></span>](system-power-status.md)
</dt> <dt>

[<span data-ttu-id="5b17e-140">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="5b17e-140">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="5b17e-141">**GetSystemPowerStatus**</span><span class="sxs-lookup"><span data-stu-id="5b17e-141">**GetSystemPowerStatus**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[<span data-ttu-id="5b17e-142">**系統 \_ 電源 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="5b17e-142">**SYSTEM\_POWER\_STATUS**</span></span>](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[<span data-ttu-id="5b17e-143">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="5b17e-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




