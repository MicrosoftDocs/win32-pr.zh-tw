---
description: 通知應用程式對裝置或電腦的硬體設定有變更。
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: 'WM_DEVICECHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385909"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="8f6d0-103">WM \_ DEVICECHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="8f6d0-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="8f6d0-104">通知應用程式對裝置或電腦的硬體設定有變更。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="8f6d0-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="8f6d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="8f6d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f6d0-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="8f6d0-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8f6d0-108">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="8f6d0-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="8f6d0-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8f6d0-110">**WM \_ DEVICECHANGE** 識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8f6d0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f6d0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f6d0-112">已發生的事件。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-112">The event that has occurred.</span></span> <span data-ttu-id="8f6d0-113">此參數可以是 Dbt .h 標頭檔中的下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>



| <span data-ttu-id="8f6d0-114">值</span><span class="sxs-lookup"><span data-stu-id="8f6d0-114">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="8f6d0-115">意義</span><span class="sxs-lookup"><span data-stu-id="8f6d0-115">Meaning</span></span>                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <span data-ttu-id="8f6d0-116"><dt>**[DBT \_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-116"><dt>**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span></span> </dl>             | <span data-ttu-id="8f6d0-117">已取消變更目前設定 (dock 或取消停駐) 的要求。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-117">A request to change the current configuration (dock or undock) has been canceled.</span></span><br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <span data-ttu-id="8f6d0-118"><dt>**[DBT \_CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-118"><dt>**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span></span> </dl>                                         | <span data-ttu-id="8f6d0-119">目前的設定已變更，因為停駐或解除卸載。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-119">The current configuration has changed, due to a dock or undock.</span></span><br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <span data-ttu-id="8f6d0-120"><dt>**[DBT \_CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-120"><dt>**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span></span> </dl>                                                 | <span data-ttu-id="8f6d0-121">發生自訂事件。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-121">A custom event has occurred.</span></span><br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <span data-ttu-id="8f6d0-122"><dt>**[DBT \_DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-122"><dt>**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span></span> </dl>                                         | <span data-ttu-id="8f6d0-123">已插入裝置或媒體片段，且現在已可供使用。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-123">A device or piece of media has been inserted and is now available.</span></span><br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <span data-ttu-id="8f6d0-124"><dt>**[DBT \_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-124"><dt>**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span></span> </dl>                         | <span data-ttu-id="8f6d0-125">要求移除裝置或媒體部分的許可權。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-125">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="8f6d0-126">任何應用程式都可以拒絕此要求，並取消移除。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-126">Any application can deny this request and cancel the removal.</span></span><br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <span data-ttu-id="8f6d0-127"><dt>**[DBT \_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-127"><dt>**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span></span> </dl> | <span data-ttu-id="8f6d0-128">移除裝置或媒體片段的要求已取消。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-128">A request to remove a device or piece of media has been canceled.</span></span><br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <span data-ttu-id="8f6d0-129"><dt>**[DBT \_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-129"><dt>**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span></span> </dl>             | <span data-ttu-id="8f6d0-130">已移除裝置或媒體片段。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-130">A device or piece of media has been removed.</span></span><br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <span data-ttu-id="8f6d0-131"><dt>**[DBT \_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-131"><dt>**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span></span> </dl>                 | <span data-ttu-id="8f6d0-132">即將移除的裝置或媒體片段。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-132">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="8f6d0-133">無法拒絕。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-133">Cannot be denied.</span></span><br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <span data-ttu-id="8f6d0-134"><dt>**[DBT \_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-134"><dt>**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span></span> </dl>                     | <span data-ttu-id="8f6d0-135">發生裝置特定事件。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-135">A device-specific event has occurred.</span></span><br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <span data-ttu-id="8f6d0-136"><dt>**[DBT \_DEVNODES \_ 已變更](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-136"><dt>**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span></span> </dl>                            | <span data-ttu-id="8f6d0-137">已在系統中新增或移除裝置。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-137">A device has been added to or removed from the system.</span></span><br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <span data-ttu-id="8f6d0-138"><dt>**[DBT \_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-138"><dt>**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span></span> </dl>                         | <span data-ttu-id="8f6d0-139">已要求許可權來變更目前的設定 (dock 或移除) 。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-139">Permission is requested to change the current configuration (dock or undock).</span></span><br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <span data-ttu-id="8f6d0-140"><dt>**[DBT \_使用者](dbt-userdefined.md)**</dt>的 <dt>0xffff</dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-140"><dt>**[DBT\_USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span></span> </dl>                                                 | <span data-ttu-id="8f6d0-141">此訊息的意義是使用者定義的。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-141">The meaning of this message is user-defined.</span></span><br/>                                                                                |



 

</dd> <dt>

<span data-ttu-id="8f6d0-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f6d0-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f6d0-143">包含事件特定資料之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-143">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="8f6d0-144">其格式取決於 *wParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-144">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="8f6d0-145">如需詳細資訊，請參閱每個事件的檔。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-145">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f6d0-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f6d0-146">Return value</span></span>

<span data-ttu-id="8f6d0-147">傳回 **TRUE** 以授與要求。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-147">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="8f6d0-148">退回 **廣播 \_ 查詢 \_ 拒絕** 以拒絕要求。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-148">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f6d0-149">備註</span><span class="sxs-lookup"><span data-stu-id="8f6d0-149">Remarks</span></span>

<span data-ttu-id="8f6d0-150">針對提供軟體可控制功能的裝置（例如彈出和鎖定），系統通常會傳送 [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) 訊息，讓應用程式和設備磁碟機正常地結束其裝置的使用。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-150">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="8f6d0-151">如果系統強制移除裝置，則在這麼做之前，它可能不會傳送 [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="8f6d0-151">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f6d0-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f6d0-152">Requirements</span></span>



| <span data-ttu-id="8f6d0-153">需求</span><span class="sxs-lookup"><span data-stu-id="8f6d0-153">Requirement</span></span> | <span data-ttu-id="8f6d0-154">值</span><span class="sxs-lookup"><span data-stu-id="8f6d0-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f6d0-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f6d0-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8f6d0-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f6d0-156">Windows XP</span></span><br/>                                                                                             |
| <span data-ttu-id="8f6d0-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f6d0-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8f6d0-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f6d0-158">Windows Server 2003</span></span><br/>                                                                                    |
| <span data-ttu-id="8f6d0-159">標頭</span><span class="sxs-lookup"><span data-stu-id="8f6d0-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f6d0-160"><dt>Winuser (包含 Windows .h 或 Dbt) </dt></span><span class="sxs-lookup"><span data-stu-id="8f6d0-160"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f6d0-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f6d0-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f6d0-162">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="8f6d0-162">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-163">DBT \_ CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="8f6d0-163">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-164">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="8f6d0-164">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-165">DBT \_ DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="8f6d0-165">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-166">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="8f6d0-166">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-167">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="8f6d0-167">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-168">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="8f6d0-168">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-169">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="8f6d0-169">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-170">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="8f6d0-170">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-171">DBT \_ DEVNODES \_ 已變更</span><span class="sxs-lookup"><span data-stu-id="8f6d0-171">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-172">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="8f6d0-172">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="8f6d0-173">DBT 的 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="8f6d0-173">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

 

