---
description: 通知應用程式對裝置或電腦的硬體設定有變更。
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: 'WM_DEVICECHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581500"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="bb22d-103">WM \_ DEVICECHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="bb22d-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="bb22d-104">通知應用程式對裝置或電腦的硬體設定有變更。</span><span class="sxs-lookup"><span data-stu-id="bb22d-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="bb22d-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="bb22d-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a><span data-ttu-id="bb22d-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb22d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb22d-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="bb22d-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bb22d-108">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bb22d-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="bb22d-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="bb22d-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="bb22d-110">**WM \_ DEVICECHANGE** 識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb22d-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bb22d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb22d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb22d-112">已發生的事件。</span><span class="sxs-lookup"><span data-stu-id="bb22d-112">The event that has occurred.</span></span> <span data-ttu-id="bb22d-113">此參數可以是 Dbt .h 標頭檔中的下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bb22d-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>

| <span data-ttu-id="bb22d-114">值</span><span class="sxs-lookup"><span data-stu-id="bb22d-114">Value</span></span> | <span data-ttu-id="bb22d-115">意義</span><span class="sxs-lookup"><span data-stu-id="bb22d-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="bb22d-116">**[DBT \_ DEVNODES \_ 已變更](dbt-devnodes-changed.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-116">**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</span></span></br><span data-ttu-id="bb22d-117">0x0007</span><span class="sxs-lookup"><span data-stu-id="bb22d-117">0x0007</span></span> | <span data-ttu-id="bb22d-118">已在系統中新增或移除裝置。</span><span class="sxs-lookup"><span data-stu-id="bb22d-118">A device has been added to or removed from the system.</span></span> |
| <span data-ttu-id="bb22d-119">**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-119">**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span></span></br><span data-ttu-id="bb22d-120">0x0017</span><span class="sxs-lookup"><span data-stu-id="bb22d-120">0x0017</span></span> | <span data-ttu-id="bb22d-121">已要求許可權來變更目前的設定 (dock 或移除) 。</span><span class="sxs-lookup"><span data-stu-id="bb22d-121">Permission is requested to change the current configuration (dock or undock).</span></span> |
| <span data-ttu-id="bb22d-122">**[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-122">**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</span></span></br><span data-ttu-id="bb22d-123">0x0018</span><span class="sxs-lookup"><span data-stu-id="bb22d-123">0x0018</span></span> | <span data-ttu-id="bb22d-124">目前的設定已變更，因為停駐或解除卸載。</span><span class="sxs-lookup"><span data-stu-id="bb22d-124">The current configuration has changed, due to a dock or undock.</span></span> |
| <span data-ttu-id="bb22d-125">**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-125">**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span></span></br><span data-ttu-id="bb22d-126">0x0019</span><span class="sxs-lookup"><span data-stu-id="bb22d-126">0x0019</span></span> | <span data-ttu-id="bb22d-127">已取消變更目前設定 (dock 或取消停駐) 的要求。</span><span class="sxs-lookup"><span data-stu-id="bb22d-127">A request to change the current configuration (dock or undock) has been canceled.</span></span> |
| <span data-ttu-id="bb22d-128">**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-128">**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</span></span></br><span data-ttu-id="bb22d-129">0x8000</span><span class="sxs-lookup"><span data-stu-id="bb22d-129">0x8000</span></span> | <span data-ttu-id="bb22d-130">已插入裝置或媒體片段，且現在已可供使用。</span><span class="sxs-lookup"><span data-stu-id="bb22d-130">A device or piece of media has been inserted and is now available.</span></span> |
| <span data-ttu-id="bb22d-131">**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-131">**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span></span></br><span data-ttu-id="bb22d-132">0x8001</span><span class="sxs-lookup"><span data-stu-id="bb22d-132">0x8001</span></span> | <span data-ttu-id="bb22d-133">要求移除裝置或媒體部分的許可權。</span><span class="sxs-lookup"><span data-stu-id="bb22d-133">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="bb22d-134">任何應用程式都可以拒絕此要求，並取消移除。</span><span class="sxs-lookup"><span data-stu-id="bb22d-134">Any application can deny this request and cancel the removal.</span></span> |
| <span data-ttu-id="bb22d-135">**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-135">**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span></span></br><span data-ttu-id="bb22d-136">0x8002</span><span class="sxs-lookup"><span data-stu-id="bb22d-136">0x8002</span></span> | <span data-ttu-id="bb22d-137">移除裝置或媒體片段的要求已取消。</span><span class="sxs-lookup"><span data-stu-id="bb22d-137">A request to remove a device or piece of media has been canceled.</span></span> |
| <span data-ttu-id="bb22d-138">**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-138">**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span></span></br><span data-ttu-id="bb22d-139">0x8003</span><span class="sxs-lookup"><span data-stu-id="bb22d-139">0x8003</span></span> | <span data-ttu-id="bb22d-140">即將移除的裝置或媒體片段。</span><span class="sxs-lookup"><span data-stu-id="bb22d-140">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="bb22d-141">無法拒絕。</span><span class="sxs-lookup"><span data-stu-id="bb22d-141">Cannot be denied.</span></span> |
| <span data-ttu-id="bb22d-142">**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-142">**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span></span></br><span data-ttu-id="bb22d-143">0x8004</span><span class="sxs-lookup"><span data-stu-id="bb22d-143">0x8004</span></span> | <span data-ttu-id="bb22d-144">已移除裝置或媒體片段。</span><span class="sxs-lookup"><span data-stu-id="bb22d-144">A device or piece of media has been removed.</span></span> |
| <span data-ttu-id="bb22d-145">**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-145">**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span></span></br><span data-ttu-id="bb22d-146">0x8005</span><span class="sxs-lookup"><span data-stu-id="bb22d-146">0x8005</span></span> | <span data-ttu-id="bb22d-147">發生裝置特定事件。</span><span class="sxs-lookup"><span data-stu-id="bb22d-147">A device-specific event has occurred.</span></span> |
| <span data-ttu-id="bb22d-148">**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-148">**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</span></span></br><span data-ttu-id="bb22d-149">0x8006</span><span class="sxs-lookup"><span data-stu-id="bb22d-149">0x8006</span></span> | <span data-ttu-id="bb22d-150">發生自訂事件。</span><span class="sxs-lookup"><span data-stu-id="bb22d-150">A custom event has occurred.</span></span> |
| <span data-ttu-id="bb22d-151">**[DBT 的 \_ 使用者](dbt-userdefined.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22d-151">**[DBT\_USERDEFINED](dbt-userdefined.md)**</span></span></br><span data-ttu-id="bb22d-152">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="bb22d-152">0xFFFF</span></span> | <span data-ttu-id="bb22d-153">此訊息的意義是使用者定義的。</span><span class="sxs-lookup"><span data-stu-id="bb22d-153">The meaning of this message is user-defined.</span></span> |

</dd> <dt>

<span data-ttu-id="bb22d-154">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb22d-154">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb22d-155">包含事件特定資料之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bb22d-155">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="bb22d-156">其格式取決於 *wParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="bb22d-156">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="bb22d-157">如需詳細資訊，請參閱每個事件的檔。</span><span class="sxs-lookup"><span data-stu-id="bb22d-157">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb22d-158">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb22d-158">Return value</span></span>

<span data-ttu-id="bb22d-159">傳回 **TRUE** 以授與要求。</span><span class="sxs-lookup"><span data-stu-id="bb22d-159">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="bb22d-160">退回 **廣播 \_ 查詢 \_ 拒絕** 以拒絕要求。</span><span class="sxs-lookup"><span data-stu-id="bb22d-160">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb22d-161">備註</span><span class="sxs-lookup"><span data-stu-id="bb22d-161">Remarks</span></span>

<span data-ttu-id="bb22d-162">針對提供軟體可控制功能的裝置（例如彈出和鎖定），系統通常會傳送 [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) 訊息，讓應用程式和設備磁碟機正常地結束其裝置的使用。</span><span class="sxs-lookup"><span data-stu-id="bb22d-162">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="bb22d-163">如果系統強制移除裝置，則在這麼做之前，它可能不會傳送 [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="bb22d-163">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb22d-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb22d-164">Requirements</span></span>

| <span data-ttu-id="bb22d-165">需求</span><span class="sxs-lookup"><span data-stu-id="bb22d-165">Requirement</span></span> | <span data-ttu-id="bb22d-166">值</span><span class="sxs-lookup"><span data-stu-id="bb22d-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb22d-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb22d-167">Minimum supported client</span></span> | <span data-ttu-id="bb22d-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb22d-168">Windows XP</span></span> |
| <span data-ttu-id="bb22d-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb22d-169">Minimum supported server</span></span> | <span data-ttu-id="bb22d-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb22d-170">Windows Server 2003</span></span>|
| <span data-ttu-id="bb22d-171">標頭</span><span class="sxs-lookup"><span data-stu-id="bb22d-171">Header</span></span> | <dl> <span data-ttu-id="bb22d-172"><dt>Winuser (包含 Windows .h 或 Dbt) </dt></span><span class="sxs-lookup"><span data-stu-id="bb22d-172"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="bb22d-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb22d-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb22d-174">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="bb22d-174">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="bb22d-175">DBT \_ CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="bb22d-175">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="bb22d-176">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="bb22d-176">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="bb22d-177">DBT \_ DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="bb22d-177">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="bb22d-178">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="bb22d-178">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="bb22d-179">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="bb22d-179">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="bb22d-180">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="bb22d-180">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="bb22d-181">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="bb22d-181">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="bb22d-182">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="bb22d-182">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="bb22d-183">DBT \_ DEVNODES \_ 已變更</span><span class="sxs-lookup"><span data-stu-id="bb22d-183">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="bb22d-184">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="bb22d-184">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="bb22d-185">DBT 的 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="bb22d-185">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>
