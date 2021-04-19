---
description: '\_當使用者選擇結束會話時，或當應用程式呼叫其中一個系統關閉函式時，會傳送 WM QUERYENDSESSION 訊息。'
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: 'WM_QUERYENDSESSION 訊息 (WinUser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2e2f82388b229523f371c680d6ccc7c4b1e27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987390"
---
# <a name="wm_queryendsession-message"></a><span data-ttu-id="6942b-103">WM \_ QUERYENDSESSION 訊息</span><span class="sxs-lookup"><span data-stu-id="6942b-103">WM\_QUERYENDSESSION message</span></span>

<span data-ttu-id="6942b-104">當使用者選擇結束會話時，或當應用程式呼叫其中一個系統關閉函式時，會傳送 **WM \_ QUERYENDSESSION** 訊息。</span><span class="sxs-lookup"><span data-stu-id="6942b-104">The **WM\_QUERYENDSESSION** message is sent when the user chooses to end the session or when an application calls one of the system shutdown functions.</span></span> <span data-ttu-id="6942b-105">如果有任何應用程式傳回零，會話就不會結束。</span><span class="sxs-lookup"><span data-stu-id="6942b-105">If any application returns zero, the session is not ended.</span></span> <span data-ttu-id="6942b-106">當某個應用程式傳回零時，系統就會停止傳送 **WM \_ QUERYENDSESSION** 訊息。</span><span class="sxs-lookup"><span data-stu-id="6942b-106">The system stops sending **WM\_QUERYENDSESSION** messages as soon as one application returns zero.</span></span>

<span data-ttu-id="6942b-107">處理此訊息之後，系統會將 *wParam* 參數設定為的 [**wm \_ ENDSESSION**](wm-endsession.md)訊息傳送至 **wm \_ QUERYENDSESSION** 訊息的結果。</span><span class="sxs-lookup"><span data-stu-id="6942b-107">After processing this message, the system sends the [**WM\_ENDSESSION**](wm-endsession.md) message with the *wParam* parameter set to the results of the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="6942b-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="6942b-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="6942b-109">參數</span><span class="sxs-lookup"><span data-stu-id="6942b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6942b-110">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="6942b-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6942b-111">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6942b-111">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="6942b-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="6942b-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="6942b-113">**WM \_ QUERYENDSESSION** 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6942b-113">The **WM\_QUERYENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6942b-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6942b-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6942b-115">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="6942b-115">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="6942b-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6942b-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6942b-117">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="6942b-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="6942b-118">如果此參數為0，表示系統正在關閉或重新開機 (無法判斷發生) 的事件。</span><span class="sxs-lookup"><span data-stu-id="6942b-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="6942b-119">值</span><span class="sxs-lookup"><span data-stu-id="6942b-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="6942b-120">意義</span><span class="sxs-lookup"><span data-stu-id="6942b-120">Meaning</span></span>                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="6942b-121"><dt>**ENDSESSION \_CLOSEAPP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6942b-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6942b-122">應用程式正在使用必須取代的檔案、系統正在進行服務，或系統資源已用盡。</span><span class="sxs-lookup"><span data-stu-id="6942b-122">The application is using a file that must be replaced, the system is being serviced, or system resources are exhausted.</span></span> <span data-ttu-id="6942b-123">如需詳細資訊，請參閱 [應用程式的指導方針](../rstmgr/guidelines-for-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="6942b-123">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="6942b-124"><dt>**ENDSESSION \_重大**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="6942b-124"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="6942b-125">應用程式會強制關機。</span><span class="sxs-lookup"><span data-stu-id="6942b-125">The application is forced to shut down.</span></span><br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="6942b-126"><dt>**ENDSESSION \_登出**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="6942b-126"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="6942b-127">使用者正在登出。</span><span class="sxs-lookup"><span data-stu-id="6942b-127">The user is logging off.</span></span> <span data-ttu-id="6942b-128">如需詳細資訊， [請參閱登出](logging-off.md)。</span><span class="sxs-lookup"><span data-stu-id="6942b-128">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                   |



 

<span data-ttu-id="6942b-129">請注意，此參數是位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="6942b-129">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="6942b-130">若要測試此值，請使用位運算;請勿測試是否相等。</span><span class="sxs-lookup"><span data-stu-id="6942b-130">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6942b-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="6942b-131">Return value</span></span>

<span data-ttu-id="6942b-132">應用程式應該遵守使用者的意圖，並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6942b-132">Applications should respect the user's intentions and return **TRUE**.</span></span> <span data-ttu-id="6942b-133">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數會針對此訊息傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="6942b-133">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE** for this message.</span></span>

<span data-ttu-id="6942b-134">如果關機會損毀正在燒錄的系統或媒體，則應用程式可能會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6942b-134">If shutting down would corrupt the system or media that is being burned, the application can return **FALSE**.</span></span> <span data-ttu-id="6942b-135">不過，最好的作法是採用使用者的動作。</span><span class="sxs-lookup"><span data-stu-id="6942b-135">However, it is good practice to respect the user's actions.</span></span>

## <a name="remarks"></a><span data-ttu-id="6942b-136">備註</span><span class="sxs-lookup"><span data-stu-id="6942b-136">Remarks</span></span>

<span data-ttu-id="6942b-137">當應用程式針對此訊息傳回 **TRUE** 時，不論其他應用程式如何回應 **wm \_ QUERYENDSESSION** 訊息，它都會收到 [**WM \_ ENDSESSION**](wm-endsession.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="6942b-137">When an application returns **TRUE** for this message, it receives the [**WM\_ENDSESSION**](wm-endsession.md) message, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span> <span data-ttu-id="6942b-138">每個應用程式在收到此訊息時，都應該立即傳回 **TRUE** 或 **FALSE** ，並延遲任何清除作業，直到接收到 **WM \_ ENDSESSION** 訊息為止。</span><span class="sxs-lookup"><span data-stu-id="6942b-138">Each application should return **TRUE** or **FALSE** immediately upon receiving this message, and defer any cleanup operations until it receives the **WM\_ENDSESSION** message.</span></span>

<span data-ttu-id="6942b-139">應用程式可以顯示使用者介面，以在關機時提示使用者輸入資訊，不過不建議這麼做。</span><span class="sxs-lookup"><span data-stu-id="6942b-139">Applications can display a user interface prompting the user for information at shutdown, however it is not recommended.</span></span> <span data-ttu-id="6942b-140">五秒後，系統會顯示導致關機的應用程式相關資訊，並允許使用者將其終止。</span><span class="sxs-lookup"><span data-stu-id="6942b-140">After five seconds, the system displays information about the applications that are preventing shutdown and allows the user to terminate them.</span></span> <span data-ttu-id="6942b-141">例如，Windows XP 會顯示一個對話方塊，而 Windows Vista 會顯示全螢幕，內含應用程式封鎖關機的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6942b-141">For example, Windows XP displays a dialog box, while Windows Vista displays a full screen with additional information about the applications blocking shutdown.</span></span> <span data-ttu-id="6942b-142">如果您的應用程式必須封鎖或延遲系統關機，請使用 [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) 函數。</span><span class="sxs-lookup"><span data-stu-id="6942b-142">If your application must block or postpone system shutdown, use the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span> <span data-ttu-id="6942b-143">如需詳細資訊，請參閱 [Windows Vista 的關機變更](shutdown-changes-for-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="6942b-143">For more information, see [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).</span></span>

<span data-ttu-id="6942b-144">主控台應用程式可以使用 [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) 函式來接收關機通知。</span><span class="sxs-lookup"><span data-stu-id="6942b-144">Console applications can use the [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) function to receive shutdown notification.</span></span>

<span data-ttu-id="6942b-145">服務應用程式可以使用 [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) 函式來接收處理常式常式中的關機通知。</span><span class="sxs-lookup"><span data-stu-id="6942b-145">Service applications can use the [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function to receive shutdown notifications in a handler routine.</span></span>

## <a name="examples"></a><span data-ttu-id="6942b-146">範例</span><span class="sxs-lookup"><span data-stu-id="6942b-146">Examples</span></span>

<span data-ttu-id="6942b-147">如需範例，請 [參閱登出](logging-off.md)。</span><span class="sxs-lookup"><span data-stu-id="6942b-147">For an example, see [Logging Off](logging-off.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6942b-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="6942b-148">Requirements</span></span>



| <span data-ttu-id="6942b-149">需求</span><span class="sxs-lookup"><span data-stu-id="6942b-149">Requirement</span></span> | <span data-ttu-id="6942b-150">值</span><span class="sxs-lookup"><span data-stu-id="6942b-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6942b-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6942b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="6942b-152">Windows XP \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6942b-152">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="6942b-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6942b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="6942b-154">Windows Server 2003 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6942b-154">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="6942b-155">標頭</span><span class="sxs-lookup"><span data-stu-id="6942b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="6942b-156"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6942b-156"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6942b-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6942b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6942b-158">登出</span><span class="sxs-lookup"><span data-stu-id="6942b-158">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="6942b-159">關閉</span><span class="sxs-lookup"><span data-stu-id="6942b-159">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="6942b-160">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6942b-160">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="6942b-161">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="6942b-161">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[<span data-ttu-id="6942b-162">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="6942b-162">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="6942b-163">**WM \_ ENDSESSION**</span><span class="sxs-lookup"><span data-stu-id="6942b-163">**WM\_ENDSESSION**</span></span>](wm-endsession.md)
</dt> </dl>

 

 
