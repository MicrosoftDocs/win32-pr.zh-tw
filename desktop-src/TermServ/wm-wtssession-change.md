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
# <a name="wm_wtssession_change-message"></a>WM \_ WTSSESSION \_ 變更訊息

通知應用程式會話狀態中的變更。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函式接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWnd* \[在\]
</dt> <dd>

視窗的控制碼。

</dd> <dt>

*Msg* \[在\]
</dt> <dd>

指定 (**WM \_ WTSSESSION \_ 變更**) 的訊息。

</dd> <dt>

*wParam* \[在\]
</dt> <dd>

描述傳送會話狀態變更通知原因的狀態碼。 此參數可以是下列其中一個值。

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_主控台 \_ 連接** (0x1) 


</dt> <dd>

*LParam* 所識別的會話已連線到主控台終端機或 RemoteFX 會話。

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_主控台 \_ 中斷** 連線 (0x2) 


</dt> <dd>

*LParam* 識別的會話已從主控台終端機或 RemoteFX 會話中斷連線。

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_REMOTE \_ CONNECT** (0x3) 


</dt> <dd>

*LParam* 所識別的會話已連線到遠端終端機。

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_遠端 \_ 中斷連接** (0x4) 


</dt> <dd>

*LParam* 識別的會話已與遠端終端機機中斷連線。

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_會話 \_ 登** 入 (0x5) 


</dt> <dd>

使用者已登入 *lParam* 識別的會話。

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_會話 \_ 登出** (0x6) 


</dt> <dd>

使用者已登出 *lParam* 所識別的會話。

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_會話 \_ 鎖定** (0x7) 


</dt> <dd>

*LParam* 識別的會話已經鎖定。

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_會話 \_ 解除鎖定** (0x8) 


</dt> <dd>

*LParam* 識別的會話已解除鎖定。

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_會話 \_ 遠端 \_ 控制** (0x9) 


</dt> <dd>

*LParam* 識別的會話已變更其遠端控制狀態。 若要判斷狀態，請呼叫 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 並檢查 **SM \_ REMOTECONTROL** 度量。

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_會話 \_ 建立** (0xA) 


</dt> <dd>

保留供未來使用。

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_會話 \_ 終止** (0xB) 


</dt> <dd>

保留供未來使用。

</dd> </dl> </dd> <dt>

*lParam* \[在\]
</dt> <dd>

會話的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

此訊息只會傳送給已註冊的應用程式，藉由呼叫 [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)來接收此訊息。

應用程式如何回應此訊息的範例包括釋出或取得主控台特定的資源、判斷螢幕繪製方式，或觸發主控台動畫效果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                           |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

