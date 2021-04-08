---
title: 'WM_WTSSESSION_CHANGE 訊息 (Winuser .h) '
description: 通知應用程式會話狀態中的變更。
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- WM_WTSSESSION_CHANGE 訊息遠端桌面服務
topic_type:
- apiref
api_name:
- WM_WTSSESSION_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f1dc421aa160824a194588711e84f961ea4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685575"
---
# <a name="wm_wtssession_change-message"></a><span data-ttu-id="46d33-104">WM \_ WTSSESSION \_ 變更訊息</span><span class="sxs-lookup"><span data-stu-id="46d33-104">WM\_WTSSESSION\_CHANGE message</span></span>

<span data-ttu-id="46d33-105">通知應用程式會話狀態中的變更。</span><span class="sxs-lookup"><span data-stu-id="46d33-105">Notifies applications of changes in session state.</span></span>

<span data-ttu-id="46d33-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="46d33-106">The window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a><span data-ttu-id="46d33-107">參數</span><span class="sxs-lookup"><span data-stu-id="46d33-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d33-108">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46d33-108">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d33-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="46d33-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="46d33-110">*Msg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46d33-110">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d33-111">指定 (**WM \_ WTSSESSION \_ 變更**) 的訊息。</span><span class="sxs-lookup"><span data-stu-id="46d33-111">Specifies the message (**WM\_WTSSESSION\_CHANGE**).</span></span>

</dd> <dt>

<span data-ttu-id="46d33-112">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46d33-112">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d33-113">描述傳送會話狀態變更通知原因的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="46d33-113">Status code describing the reason the session state change notification was sent.</span></span> <span data-ttu-id="46d33-114">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="46d33-114">This parameter can be one of the following values.</span></span>

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span data-ttu-id="46d33-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_主控台 \_ 連接** (0x1) </span><span class="sxs-lookup"><span data-stu-id="46d33-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS\_CONSOLE\_CONNECT** (0x1)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-116">*LParam* 所識別的會話已連線到主控台終端機或 RemoteFX 會話。</span><span class="sxs-lookup"><span data-stu-id="46d33-116">The session identified by *lParam* was connected to the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span data-ttu-id="46d33-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_主控台 \_ 中斷** 連線 (0x2) </span><span class="sxs-lookup"><span data-stu-id="46d33-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS\_CONSOLE\_DISCONNECT** (0x2)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-118">*LParam* 識別的會話已從主控台終端機或 RemoteFX 會話中斷連線。</span><span class="sxs-lookup"><span data-stu-id="46d33-118">The session identified by *lParam* was disconnected from the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span data-ttu-id="46d33-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_REMOTE \_ CONNECT** (0x3) </span><span class="sxs-lookup"><span data-stu-id="46d33-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS\_REMOTE\_CONNECT** (0x3)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-120">*LParam* 所識別的會話已連線到遠端終端機。</span><span class="sxs-lookup"><span data-stu-id="46d33-120">The session identified by *lParam* was connected to the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span data-ttu-id="46d33-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_遠端 \_ 中斷連接** (0x4) </span><span class="sxs-lookup"><span data-stu-id="46d33-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS\_REMOTE\_DISCONNECT** (0x4)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-122">*LParam* 識別的會話已與遠端終端機機中斷連線。</span><span class="sxs-lookup"><span data-stu-id="46d33-122">The session identified by *lParam* was disconnected from the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span data-ttu-id="46d33-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_會話 \_ 登** 入 (0x5) </span><span class="sxs-lookup"><span data-stu-id="46d33-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS\_SESSION\_LOGON** (0x5)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-124">使用者已登入 *lParam* 識別的會話。</span><span class="sxs-lookup"><span data-stu-id="46d33-124">A user has logged on to the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span data-ttu-id="46d33-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_會話 \_ 登出** (0x6) </span><span class="sxs-lookup"><span data-stu-id="46d33-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS\_SESSION\_LOGOFF** (0x6)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-126">使用者已登出 *lParam* 所識別的會話。</span><span class="sxs-lookup"><span data-stu-id="46d33-126">A user has logged off the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span data-ttu-id="46d33-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_會話 \_ 鎖定** (0x7) </span><span class="sxs-lookup"><span data-stu-id="46d33-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS\_SESSION\_LOCK** (0x7)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-128">*LParam* 識別的會話已經鎖定。</span><span class="sxs-lookup"><span data-stu-id="46d33-128">The session identified by *lParam* has been locked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span data-ttu-id="46d33-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_會話 \_ 解除鎖定** (0x8) </span><span class="sxs-lookup"><span data-stu-id="46d33-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS\_SESSION\_UNLOCK** (0x8)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-130">*LParam* 識別的會話已解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="46d33-130">The session identified by *lParam* has been unlocked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span data-ttu-id="46d33-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_會話 \_ 遠端 \_ 控制** (0x9) </span><span class="sxs-lookup"><span data-stu-id="46d33-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS\_SESSION\_REMOTE\_CONTROL** (0x9)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-132">*LParam* 識別的會話已變更其遠端控制狀態。</span><span class="sxs-lookup"><span data-stu-id="46d33-132">The session identified by *lParam* has changed its remote controlled status.</span></span> <span data-ttu-id="46d33-133">若要判斷狀態，請呼叫 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 並檢查 **SM \_ REMOTECONTROL** 度量。</span><span class="sxs-lookup"><span data-stu-id="46d33-133">To determine the status, call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) and check the **SM\_REMOTECONTROL** metric.</span></span>

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span data-ttu-id="46d33-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_會話 \_ 建立** (0xA) </span><span class="sxs-lookup"><span data-stu-id="46d33-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS\_SESSION\_CREATE** (0xA)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-135">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="46d33-135">Reserved for future use.</span></span>

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span data-ttu-id="46d33-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_會話 \_ 終止** (0xB) </span><span class="sxs-lookup"><span data-stu-id="46d33-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS\_SESSION\_TERMINATE** (0xB)</span></span>


</dt> <dd>

<span data-ttu-id="46d33-137">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="46d33-137">Reserved for future use.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="46d33-138">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46d33-138">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d33-139">會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="46d33-139">The identifier of the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d33-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="46d33-140">Return value</span></span>

<span data-ttu-id="46d33-141">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="46d33-141">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="46d33-142">備註</span><span class="sxs-lookup"><span data-stu-id="46d33-142">Remarks</span></span>

<span data-ttu-id="46d33-143">此訊息只會傳送給已註冊的應用程式，藉由呼叫 [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)來接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="46d33-143">This message is sent only to applications that have registered to receive this message by calling [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span></span>

<span data-ttu-id="46d33-144">應用程式如何回應此訊息的範例包括釋出或取得主控台特定的資源、判斷螢幕繪製方式，或觸發主控台動畫效果。</span><span class="sxs-lookup"><span data-stu-id="46d33-144">Examples of how applications can respond to this message include releasing or acquiring console-specific resources, determining how a screen is to be painted, or triggering console animation effects.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d33-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="46d33-145">Requirements</span></span>



| <span data-ttu-id="46d33-146">需求</span><span class="sxs-lookup"><span data-stu-id="46d33-146">Requirement</span></span> | <span data-ttu-id="46d33-147">值</span><span class="sxs-lookup"><span data-stu-id="46d33-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d33-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46d33-148">Minimum supported client</span></span><br/> | <span data-ttu-id="46d33-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46d33-149">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="46d33-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46d33-150">Minimum supported server</span></span><br/> | <span data-ttu-id="46d33-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46d33-151">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="46d33-152">標頭</span><span class="sxs-lookup"><span data-stu-id="46d33-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d33-153"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="46d33-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d33-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46d33-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d33-155">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="46d33-155">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[<span data-ttu-id="46d33-156">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="46d33-156">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

