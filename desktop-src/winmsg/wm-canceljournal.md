---
description: 當使用者取消應用程式的日誌活動時，張貼至應用程式。 訊息是以 Null 視窗控制碼張貼。
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: 'WM_CANCELJOURNAL 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994395"
---
# <a name="wm_canceljournal-message"></a><span data-ttu-id="b66f0-104">WM \_ CANCELJOURNAL 訊息</span><span class="sxs-lookup"><span data-stu-id="b66f0-104">WM\_CANCELJOURNAL message</span></span>

<span data-ttu-id="b66f0-105">當使用者取消應用程式的日誌活動時，張貼至應用程式。</span><span class="sxs-lookup"><span data-stu-id="b66f0-105">Posted to an application when a user cancels the application's journaling activities.</span></span> <span data-ttu-id="b66f0-106">訊息是以 **Null** 視窗控制碼張貼。</span><span class="sxs-lookup"><span data-stu-id="b66f0-106">The message is posted with a **NULL** window handle.</span></span>


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a><span data-ttu-id="b66f0-107">參數</span><span class="sxs-lookup"><span data-stu-id="b66f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b66f0-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b66f0-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b66f0-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b66f0-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b66f0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b66f0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b66f0-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b66f0-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b66f0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b66f0-112">Return value</span></span>

<span data-ttu-id="b66f0-113">類型： **void**</span><span class="sxs-lookup"><span data-stu-id="b66f0-113">Type: **void**</span></span>

<span data-ttu-id="b66f0-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b66f0-114">This message does not return a value.</span></span> <span data-ttu-id="b66f0-115">它的目的是要在應用程式的主要迴圈或 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 攔截程式內進行處理，而不是從視窗程式來處理。</span><span class="sxs-lookup"><span data-stu-id="b66f0-115">It is meant to be processed from within an application's main loop or a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) hook procedure, not from a window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b66f0-116">備註</span><span class="sxs-lookup"><span data-stu-id="b66f0-116">Remarks</span></span>

<span data-ttu-id="b66f0-117">日誌記錄和播放模式是在系統上強加的模式，可讓應用程式依序記錄或播放使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="b66f0-117">Journal record and playback modes are modes imposed on the system that let an application sequentially record or play back user input.</span></span> <span data-ttu-id="b66f0-118">當應用程式安裝 [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) 或 [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) 攔截程式時，系統會進入這些模式。</span><span class="sxs-lookup"><span data-stu-id="b66f0-118">The system enters these modes when an application installs a [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) or [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) hook procedure.</span></span> <span data-ttu-id="b66f0-119">當系統處於這兩種記錄模式時，應用程式必須從輸入佇列中輪流讀取輸入。</span><span class="sxs-lookup"><span data-stu-id="b66f0-119">When the system is in either of these journaling modes, applications must take turns reading input from the input queue.</span></span> <span data-ttu-id="b66f0-120">如果有任何一個應用程式在系統處於記錄模式時停止讀取輸入，則會強制其他應用程式等候。</span><span class="sxs-lookup"><span data-stu-id="b66f0-120">If any one application stops reading input while the system is in a journaling mode, other applications are forced to wait.</span></span>

<span data-ttu-id="b66f0-121">為了確保健全的系統，其中一個應用程式無法使其無回應，系統會在使用者按下 CTRL + ESC 或 CTRL + ALT + DEL 時，自動取消任何日誌活動。</span><span class="sxs-lookup"><span data-stu-id="b66f0-121">To ensure a robust system, one that cannot be made unresponsive by any one application, the system automatically cancels any journaling activities when a user presses CTRL+ESC or CTRL+ALT+DEL.</span></span> <span data-ttu-id="b66f0-122">系統接著將任何日誌攔截程式解除掛接，並將具有 **Null** 視窗控制碼的 **WM \_ CANCELJOURNAL** 訊息張貼至設定日誌攔截的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b66f0-122">The system then unhooks any journaling hook procedures, and posts a **WM\_CANCELJOURNAL** message, with a **NULL** window handle, to the application that set the journaling hook.</span></span>

<span data-ttu-id="b66f0-123">**WM \_ CANCELJOURNAL** 訊息具有 **Null** 視窗控制碼，因此無法分派至視窗程式。</span><span class="sxs-lookup"><span data-stu-id="b66f0-123">The **WM\_CANCELJOURNAL** message has a **NULL** window handle, therefore it cannot be dispatched to a window procedure.</span></span> <span data-ttu-id="b66f0-124">有兩種方式可讓應用程式查看 **WM \_ CANCELJOURNAL** 訊息：如果應用程式是在它自己的主要迴圈中執行，它必須在呼叫 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) ，以及呼叫 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)時攔截訊息。</span><span class="sxs-lookup"><span data-stu-id="b66f0-124">There are two ways for an application to see a **WM\_CANCELJOURNAL** message: If the application is running in its own main loop, it must catch the message between its call to [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) and its call to [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span></span> <span data-ttu-id="b66f0-125">如果應用程式不是在它自己的主要迴圈中執行，它必須設定 [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) 攔截程式 (透過呼叫 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) ，指定監看訊息的 **WH \_ GETMESSAGE** 攔截型別) 。</span><span class="sxs-lookup"><span data-stu-id="b66f0-125">If the application is not running in its own main loop, it must set a [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) hook procedure (through a call to [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) specifying the **WH\_GETMESSAGE** hook type) that watches for the message.</span></span>

<span data-ttu-id="b66f0-126">當應用程式看到 **WM \_ CANCELJOURNAL** 訊息時，它可以採用兩個專案：使用者已刻意取消日誌記錄或播放模式，而系統已解除所有日誌記錄或播放攔截程式。</span><span class="sxs-lookup"><span data-stu-id="b66f0-126">When an application sees a **WM\_CANCELJOURNAL** message, it can assume two things: the user has intentionally canceled the journal record or playback mode, and the system has already unhooked any journal record or playback hook procedures.</span></span>

<span data-ttu-id="b66f0-127">請注意，上面所述的按鍵組合 (CTRL + ESC 或 CTRL + ALT + DEL) 導致系統取消記錄。</span><span class="sxs-lookup"><span data-stu-id="b66f0-127">Note that the key combinations mentioned above (CTRL+ESC or CTRL+ALT+DEL) cause the system to cancel journaling.</span></span> <span data-ttu-id="b66f0-128">如果有任何一個應用程式沒有回應，則會為使用者提供復原方法。</span><span class="sxs-lookup"><span data-stu-id="b66f0-128">If any one application is made unresponsive, they give the user a means of recovery.</span></span> <span data-ttu-id="b66f0-129">[**VK \_ 取消**](../inputdev/virtual-key-codes.md)虛擬機器碼 (通常會實作為 CTRL + BREAK 按鍵組合) 是 [筆記本記錄] 模式中的應用程式應該監看的應用程式是否為使用者希望取消日誌活動的信號。</span><span class="sxs-lookup"><span data-stu-id="b66f0-129">The [**VK\_CANCEL**](../inputdev/virtual-key-codes.md) virtual key code (usually implemented as the CTRL+BREAK key combination) is what an application that is in journal record mode should watch for as a signal that the user wishes to cancel the journaling activity.</span></span> <span data-ttu-id="b66f0-130">不同之處在于， **VK \_ CANCEL** 的監看是記錄應用程式的建議行為，而 ctrl + ESC 或 ctrl + ALT + DEL 會導致系統取消記錄，而不考慮日誌應用程式的行為。</span><span class="sxs-lookup"><span data-stu-id="b66f0-130">The difference is that watching for **VK\_CANCEL** is a suggested behavior for journaling applications, whereas CTRL+ESC or CTRL+ALT+DEL cause the system to cancel journaling regardless of a journaling application's behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="b66f0-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b66f0-131">Requirements</span></span>



| <span data-ttu-id="b66f0-132">需求</span><span class="sxs-lookup"><span data-stu-id="b66f0-132">Requirement</span></span> | <span data-ttu-id="b66f0-133">值</span><span class="sxs-lookup"><span data-stu-id="b66f0-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b66f0-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b66f0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b66f0-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b66f0-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b66f0-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b66f0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b66f0-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b66f0-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b66f0-138">標頭</span><span class="sxs-lookup"><span data-stu-id="b66f0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b66f0-139"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b66f0-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b66f0-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b66f0-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="b66f0-141">**參考**</span><span class="sxs-lookup"><span data-stu-id="b66f0-141">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="b66f0-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b66f0-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b66f0-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b66f0-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b66f0-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b66f0-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b66f0-145">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="b66f0-145">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="b66f0-146">**概念**</span><span class="sxs-lookup"><span data-stu-id="b66f0-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b66f0-147">鉤</span><span class="sxs-lookup"><span data-stu-id="b66f0-147">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
