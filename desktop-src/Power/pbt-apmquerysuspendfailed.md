---
description: 通知應用程式，暫停電腦的許可權遭到拒絕。
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: 'PBT_APMQUERYSUSPENDFAILED (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978967"
---
# <a name="pbt_apmquerysuspendfailed-event"></a><span data-ttu-id="58734-103">PBT \_ APMQUERYSUSPENDFAILED 事件</span><span class="sxs-lookup"><span data-stu-id="58734-103">PBT\_APMQUERYSUSPENDFAILED event</span></span>

<span data-ttu-id="58734-104">\[PBT \_ APMQUERYSUSPENDFAILED 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="58734-104">\[PBT\_APMQUERYSUSPENDFAILED is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="58734-105">此事件的支援已在 Windows Vista 中移除。</span><span class="sxs-lookup"><span data-stu-id="58734-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="58734-106">請改用 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 。\]</span><span class="sxs-lookup"><span data-stu-id="58734-106">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="58734-107">通知應用程式，暫停電腦的許可權遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="58734-107">Notifies applications that permission to suspend the computer was denied.</span></span> <span data-ttu-id="58734-108">如果有任何應用程式或驅動程式傳回「 **廣播 \_ 查詢 \_ 拒絕** 」至先前的 [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) 事件，則會廣播此事件。</span><span class="sxs-lookup"><span data-stu-id="58734-108">This event is broadcast if any application or driver returned **BROADCAST\_QUERY\_DENY** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="58734-109">視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。</span><span class="sxs-lookup"><span data-stu-id="58734-109">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="58734-110">*WParam* 和 *lParam* 參數的設定方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="58734-110">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="58734-111">參數</span><span class="sxs-lookup"><span data-stu-id="58734-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58734-112">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="58734-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="58734-113">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="58734-113">A handle to window.</span></span>

<span data-ttu-id="58734-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="58734-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="58734-115">值</span><span class="sxs-lookup"><span data-stu-id="58734-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="58734-116">意義</span><span class="sxs-lookup"><span data-stu-id="58734-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="58734-117"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="58734-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="58734-118">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="58734-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="58734-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="58734-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="58734-120">值</span><span class="sxs-lookup"><span data-stu-id="58734-120">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="58734-121">意義</span><span class="sxs-lookup"><span data-stu-id="58734-121">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <span data-ttu-id="58734-122"><dt>**PBT \_APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="58734-122"><dt>**PBT\_APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="58734-123">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="58734-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="58734-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58734-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58734-125">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="58734-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58734-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="58734-126">Return value</span></span>

<span data-ttu-id="58734-127">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="58734-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58734-128">備註</span><span class="sxs-lookup"><span data-stu-id="58734-128">Remarks</span></span>

<span data-ttu-id="58734-129">應用程式通常會藉由繼續正常操作來回應此事件。</span><span class="sxs-lookup"><span data-stu-id="58734-129">Applications typically respond to this event by resuming normal operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="58734-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="58734-130">Requirements</span></span>



| <span data-ttu-id="58734-131">需求</span><span class="sxs-lookup"><span data-stu-id="58734-131">Requirement</span></span> | <span data-ttu-id="58734-132">值</span><span class="sxs-lookup"><span data-stu-id="58734-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58734-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58734-133">Minimum supported client</span></span><br/> | <span data-ttu-id="58734-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58734-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="58734-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58734-135">Minimum supported server</span></span><br/> | <span data-ttu-id="58734-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58734-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58734-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="58734-137">End of client support</span></span><br/>    | <span data-ttu-id="58734-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="58734-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="58734-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="58734-139">End of server support</span></span><br/>    | <span data-ttu-id="58734-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58734-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="58734-141">標頭</span><span class="sxs-lookup"><span data-stu-id="58734-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="58734-142"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="58734-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58734-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58734-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58734-144">電源管理</span><span class="sxs-lookup"><span data-stu-id="58734-144">Power Management</span></span>](power-management-portal.md)
</dt> <dt>

[<span data-ttu-id="58734-145">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="58734-145">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="58734-146">PBT \_ APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="58734-146">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="58734-147">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="58734-147">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




