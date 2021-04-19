---
description: '\_當系統處理 wm QUERYENDSESSION 訊息的結果之後，會將 wm ENDSESSION 訊息傳送至應用程式 \_ 。 WM \_ ENDSESSION 訊息會通知應用程式會話是否結束。'
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: 'WM_ENDSESSION 訊息 (WinUser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa62f356d881182dd6e6fd9e0558332bcc1b3fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974551"
---
# <a name="wm_endsession-message"></a><span data-ttu-id="10ce9-104">WM \_ ENDSESSION 訊息</span><span class="sxs-lookup"><span data-stu-id="10ce9-104">WM\_ENDSESSION message</span></span>

<span data-ttu-id="10ce9-105">當系統處理 [**wm \_ QUERYENDSESSION**](wm-queryendsession.md)訊息的結果之後，會將 **wm \_ ENDSESSION** 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="10ce9-105">The **WM\_ENDSESSION** message is sent to an application after the system processes the results of the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message.</span></span> <span data-ttu-id="10ce9-106">**WM \_ ENDSESSION** 訊息會通知應用程式會話是否結束。</span><span class="sxs-lookup"><span data-stu-id="10ce9-106">The **WM\_ENDSESSION** message informs the application whether the session is ending.</span></span>

<span data-ttu-id="10ce9-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="10ce9-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="10ce9-108">參數</span><span class="sxs-lookup"><span data-stu-id="10ce9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10ce9-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="10ce9-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="10ce9-110">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="10ce9-110">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="10ce9-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="10ce9-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="10ce9-112">**WM \_ ENDSESSION** 識別碼。</span><span class="sxs-lookup"><span data-stu-id="10ce9-112">The **WM\_ENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="10ce9-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10ce9-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10ce9-114">如果會話已結束，則此參數為 **TRUE**;在所有應用程式都從處理此訊息傳回之後，會話就會隨時結束。</span><span class="sxs-lookup"><span data-stu-id="10ce9-114">If the session is being ended, this parameter is **TRUE**; the session can end any time after all applications have returned from processing this message.</span></span> <span data-ttu-id="10ce9-115">否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="10ce9-115">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="10ce9-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10ce9-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10ce9-117">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="10ce9-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="10ce9-118">如果此參數為0，表示系統正在關閉或重新開機 (無法判斷發生) 的事件。</span><span class="sxs-lookup"><span data-stu-id="10ce9-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="10ce9-119">值</span><span class="sxs-lookup"><span data-stu-id="10ce9-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="10ce9-120">意義</span><span class="sxs-lookup"><span data-stu-id="10ce9-120">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="10ce9-121"><dt>**ENDSESSION \_CLOSEAPP**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="10ce9-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x1</dt></span></span> </dl>        | <span data-ttu-id="10ce9-122">如果 *wParam* 為 **TRUE**，則應用程式必須關閉。</span><span class="sxs-lookup"><span data-stu-id="10ce9-122">If *wParam* is **TRUE**, the application must shut down.</span></span> <span data-ttu-id="10ce9-123">任何資料都應該自動儲存，而不提示使用者 (如需詳細資訊，請參閱備註) 。</span><span class="sxs-lookup"><span data-stu-id="10ce9-123">Any data should be saved automatically without prompting the user (for more information, see Remarks).</span></span> <span data-ttu-id="10ce9-124">當應用程式使用需要取代的檔案、必須為系統提供服務，或當系統資源耗盡時，重新開機管理員就會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="10ce9-124">The Restart Manager sends this message when the application is using a file that needs to be replaced, when it must service the system, or when system resources are exhausted.</span></span> <span data-ttu-id="10ce9-125">如果應用程式已註冊為使用 [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) 函式重新開機，將會重新開機。</span><span class="sxs-lookup"><span data-stu-id="10ce9-125">The application will be restarted if it has registered for restart using the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function.</span></span> <span data-ttu-id="10ce9-126">如需詳細資訊，請參閱 [應用程式的指導方針](../rstmgr/guidelines-for-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="10ce9-126">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span> <br/> <span data-ttu-id="10ce9-127">如果 *wParam* 為 **FALSE**，則應用程式不應該關閉。</span><span class="sxs-lookup"><span data-stu-id="10ce9-127">If *wParam* is **FALSE**, the application should not shut down.</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="10ce9-128"><dt>**ENDSESSION \_重大**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="10ce9-128"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="10ce9-129">應用程式會強制關機。</span><span class="sxs-lookup"><span data-stu-id="10ce9-129">The application is forced to shut down.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="10ce9-130"><dt>**ENDSESSION \_登出**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="10ce9-130"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="10ce9-131">使用者正在登出。</span><span class="sxs-lookup"><span data-stu-id="10ce9-131">The user is logging off.</span></span> <span data-ttu-id="10ce9-132">如需詳細資訊， [請參閱登出](logging-off.md)。</span><span class="sxs-lookup"><span data-stu-id="10ce9-132">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="10ce9-133">請注意，此參數是位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="10ce9-133">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="10ce9-134">若要測試此值，請使用位運算;請勿測試是否相等。</span><span class="sxs-lookup"><span data-stu-id="10ce9-134">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10ce9-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="10ce9-135">Return value</span></span>

<span data-ttu-id="10ce9-136">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="10ce9-136">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="10ce9-137">備註</span><span class="sxs-lookup"><span data-stu-id="10ce9-137">Remarks</span></span>

<span data-ttu-id="10ce9-138">具有未儲存資料的應用程式可以將資料儲存至暫存位置，並在應用程式下次啟動時還原資料。</span><span class="sxs-lookup"><span data-stu-id="10ce9-138">Applications that have unsaved data could save the data to a temporary location and restore it the next time the application starts.</span></span> <span data-ttu-id="10ce9-139">建議應用程式經常儲存其資料和狀態。例如，會在使用者起始的儲存作業之間自動儲存資料，以減少在關機時要儲存的資料量。</span><span class="sxs-lookup"><span data-stu-id="10ce9-139">It is recommended that applications save their data and state frequently; for example, automatically save data between save operations initiated by the user to reduce the amount of data to be saved at shutdown.</span></span>

<span data-ttu-id="10ce9-140">當會話結束時，應用程式不需要呼叫 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) 或 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="10ce9-140">The application need not call the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) or [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function when the session is ending.</span></span>

## <a name="requirements"></a><span data-ttu-id="10ce9-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="10ce9-141">Requirements</span></span>



| <span data-ttu-id="10ce9-142">需求</span><span class="sxs-lookup"><span data-stu-id="10ce9-142">Requirement</span></span> | <span data-ttu-id="10ce9-143">值</span><span class="sxs-lookup"><span data-stu-id="10ce9-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10ce9-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10ce9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="10ce9-145">Windows XP \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10ce9-145">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="10ce9-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10ce9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="10ce9-147">Windows Server 2003 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10ce9-147">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="10ce9-148">標頭</span><span class="sxs-lookup"><span data-stu-id="10ce9-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="10ce9-149"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="10ce9-149"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10ce9-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10ce9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ce9-151">登出</span><span class="sxs-lookup"><span data-stu-id="10ce9-151">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="10ce9-152">關閉</span><span class="sxs-lookup"><span data-stu-id="10ce9-152">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="10ce9-153">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="10ce9-153">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="10ce9-154">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="10ce9-154">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="10ce9-155">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="10ce9-155">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="10ce9-156">**WM \_ QUERYENDSESSION**</span><span class="sxs-lookup"><span data-stu-id="10ce9-156">**WM\_QUERYENDSESSION**</span></span>](wm-queryendsession.md)
</dt> </dl>

 

 
