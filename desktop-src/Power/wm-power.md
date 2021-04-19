---
description: 通知應用程式系統（通常是電池供電的個人電腦）即將進入暫停模式。
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: 'WM_POWER 訊息 (WinUser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979142"
---
# <a name="wm_power-message"></a><span data-ttu-id="54673-103">WM \_ 電源訊息</span><span class="sxs-lookup"><span data-stu-id="54673-103">WM\_POWER message</span></span>

<span data-ttu-id="54673-104">通知應用程式系統（通常是電池供電的個人電腦）即將進入暫停模式。</span><span class="sxs-lookup"><span data-stu-id="54673-104">Notifies applications that the system, typically a battery-powered personal computer, is about to enter a suspended mode.</span></span>

> [!Note]  
> <span data-ttu-id="54673-105">**WM \_ 電源** 訊息已過時。</span><span class="sxs-lookup"><span data-stu-id="54673-105">The **WM\_POWER** message is obsolete.</span></span> <span data-ttu-id="54673-106">它僅提供給以16位 Windows 為基礎的應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="54673-106">It is provided only for compatibility with 16-bit Windows-based applications.</span></span> <span data-ttu-id="54673-107">應用程式應該使用 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="54673-107">Applications should use the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span>

 

<span data-ttu-id="54673-108">視窗會透過其 **WindowProc** 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="54673-108">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a><span data-ttu-id="54673-109">參數</span><span class="sxs-lookup"><span data-stu-id="54673-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54673-110">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="54673-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="54673-111">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="54673-111">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="54673-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="54673-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="54673-113">**WM \_ 電源** 訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="54673-113">The **WM\_POWER** message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="54673-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54673-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54673-115">電源事件通知。</span><span class="sxs-lookup"><span data-stu-id="54673-115">The power-event notification.</span></span> <span data-ttu-id="54673-116">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="54673-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="54673-117">值</span><span class="sxs-lookup"><span data-stu-id="54673-117">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="54673-118">意義</span><span class="sxs-lookup"><span data-stu-id="54673-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <span data-ttu-id="54673-119"><dt>**PWR \_ CRITICALRESUME**</dt></span><span class="sxs-lookup"><span data-stu-id="54673-119"><dt>**PWR\_CRITICALRESUME**</dt></span></span> </dl> | <span data-ttu-id="54673-120">表示在進入暫停模式之後，系統會繼續作業，而不會先將 **PWR \_ SUSPENDREQUEST** 通知訊息廣播至應用程式。</span><span class="sxs-lookup"><span data-stu-id="54673-120">Indicates that the system is resuming operation after entering suspended mode without first broadcasting a **PWR\_SUSPENDREQUEST** notification message to the application.</span></span> <span data-ttu-id="54673-121">應用程式應該執行任何必要的復原動作。</span><span class="sxs-lookup"><span data-stu-id="54673-121">An application should perform any necessary recovery actions.</span></span><br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <span data-ttu-id="54673-122"><dt>**PWR \_ SUSPENDREQUEST**</dt></span><span class="sxs-lookup"><span data-stu-id="54673-122"><dt>**PWR\_SUSPENDREQUEST**</dt></span></span> </dl> | <span data-ttu-id="54673-123">指出系統即將進入暫停模式。</span><span class="sxs-lookup"><span data-stu-id="54673-123">Indicates that the system is about to enter suspended mode.</span></span><br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <span data-ttu-id="54673-124"><dt>**PWR \_ SUSPENDRESUME**</dt></span><span class="sxs-lookup"><span data-stu-id="54673-124"><dt>**PWR\_SUSPENDRESUME**</dt></span></span> </dl>    | <span data-ttu-id="54673-125">表示在進入暫停模式之後，系統會繼續作業，也就是，系統會在系統暫停之前，將 **PWR \_ SUSPENDREQUEST** 通知訊息廣播至應用程式。</span><span class="sxs-lookup"><span data-stu-id="54673-125">Indicates that the system is resuming operation after having entered suspended mode normally that is, the system broadcast a **PWR\_SUSPENDREQUEST** notification message to the application before the system was suspended.</span></span> <span data-ttu-id="54673-126">應用程式應該執行任何必要的復原動作。</span><span class="sxs-lookup"><span data-stu-id="54673-126">An application should perform any necessary recovery actions.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="54673-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54673-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54673-128">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="54673-128">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54673-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="54673-129">Return value</span></span>

<span data-ttu-id="54673-130">應用程式傳回的值取決於 *wParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="54673-130">The value an application returns depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="54673-131">如果 *wParam* 是 **PWR \_ SUSPENDREQUEST**，則傳回值為 **PWR \_ 無法** 防止系統進入暫停狀態，否則為 **PWR \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="54673-131">If *wParam* is **PWR\_SUSPENDREQUEST**, the return value is **PWR\_FAIL** to prevent the system from entering the suspended state; otherwise, it is **PWR\_OK**.</span></span> <span data-ttu-id="54673-132">如果 *wParam* 是 **PWR \_ SUSPENDRESUME** 或 **PWR \_ CRITICALRESUME**，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="54673-132">If *wParam* is **PWR\_SUSPENDRESUME** or **PWR\_CRITICALRESUME**, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="54673-133">備註</span><span class="sxs-lookup"><span data-stu-id="54673-133">Remarks</span></span>

<span data-ttu-id="54673-134">此訊息只會廣播至在系統上執行的應用程式，該應用程式符合 Advanced 電源管理 (APM) 基本輸入/輸出系統 (BIOS) 規格。</span><span class="sxs-lookup"><span data-stu-id="54673-134">This message is broadcast only to an application that is running on a system that conforms to the Advanced Power Management (APM) basic input/output system (BIOS) specification.</span></span> <span data-ttu-id="54673-135">此訊息是由電源管理驅動程式廣播到 **EnumWindows** 函式所傳回的每個視窗。</span><span class="sxs-lookup"><span data-stu-id="54673-135">The message is broadcast by the power-management driver to each window returned by the **EnumWindows** function.</span></span>

<span data-ttu-id="54673-136">暫停模式是最大量省電的狀態，但會保留所有運算元據和參數。</span><span class="sxs-lookup"><span data-stu-id="54673-136">The suspended mode is the state in which the greatest amount of power savings occurs, but all operational data and parameters are preserved.</span></span> <span data-ttu-id="54673-137">系統會保留隨機存取記憶體 (RAM) 內容，但許多裝置可能會關閉。</span><span class="sxs-lookup"><span data-stu-id="54673-137">Random-access memory (RAM) contents are preserved, but many devices are likely to be turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="54673-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="54673-138">Requirements</span></span>



| <span data-ttu-id="54673-139">需求</span><span class="sxs-lookup"><span data-stu-id="54673-139">Requirement</span></span> | <span data-ttu-id="54673-140">值</span><span class="sxs-lookup"><span data-stu-id="54673-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54673-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54673-141">Minimum supported client</span></span><br/> | <span data-ttu-id="54673-142">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54673-142">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="54673-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54673-143">Minimum supported server</span></span><br/> | <span data-ttu-id="54673-144">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54673-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="54673-145">標頭</span><span class="sxs-lookup"><span data-stu-id="54673-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="54673-146"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="54673-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54673-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54673-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54673-148">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="54673-148">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




