---
description: '\_當系統處理 wm QUERYENDSESSION 訊息的結果之後，會將 wm ENDSESSION 訊息傳送至應用程式 \_ 。 WM \_ ENDSESSION 訊息會通知應用程式會話是否結束。'
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: 'WM_ENDSESSION 訊息 (WinUser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788cd7c77ffe6e82e7ca95232b64ecd6bdc5e2c97e9f6a0262adb5f9249da156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963461"
---
# <a name="wm_endsession-message"></a>WM \_ ENDSESSION 訊息

當系統處理 [**wm \_ QUERYENDSESSION**](wm-queryendsession.md)訊息的結果之後，會將 **wm \_ ENDSESSION** 訊息傳送至應用程式。 **WM \_ ENDSESSION** 訊息會通知應用程式會話是否結束。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> <dt>

*uMsg* 
</dt> <dd>

**WM \_ ENDSESSION** 識別碼。

</dd> <dt>

*wParam* 
</dt> <dd>

如果會話已結束，則此參數為 **TRUE**;在所有應用程式都從處理此訊息傳回之後，會話就會隨時結束。 否則為 **FALSE**。

</dd> <dt>

*lParam* 
</dt> <dd>

這個參數可以是下列一或多個值。 如果此參數為0，表示系統正在關閉或重新開機 (無法判斷發生) 的事件。



| 值                                                                                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_CLOSEAPP**</dt> <dt>0x1</dt> </dl>        | 如果 *wParam* 為 **TRUE**，則應用程式必須關閉。 任何資料都應該自動儲存，而不提示使用者 (如需詳細資訊，請參閱備註) 。 當應用程式使用需要取代的檔案、必須為系統提供服務，或當系統資源耗盡時，重新開機管理員就會傳送此訊息。 如果應用程式已註冊為使用 [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) 函式重新開機，將會重新開機。 如需詳細資訊，請參閱 [應用程式的指導方針](../rstmgr/guidelines-for-applications.md)。 <br/> 如果 *wParam* 為 **FALSE**，則應用程式不應該關閉。<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_重大**</dt> <dt>0x40000000</dt> </dl> | 應用程式會強制關機。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_登出**</dt> <dt>0x80000000</dt> </dl>       | 使用者正在登出。 如需詳細資訊， [請參閱登出](logging-off.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

請注意，此參數是位元遮罩。 若要測試此值，請使用位運算;請勿測試是否相等。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

具有未儲存資料的應用程式可以將資料儲存至暫存位置，並在應用程式下次啟動時還原資料。 建議應用程式經常儲存其資料和狀態。例如，會在使用者起始的儲存作業之間自動儲存資料，以減少在關機時要儲存的資料量。

當會話結束時，應用程式不需要呼叫 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) 或 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP \[ desktop apps \| UWP 應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | WindowsServer 2003 \[ desktop app \| UWP 應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>WinUser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[登出](logging-off.md)
</dt> <dt>

[關閉](shutting-down.md)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**WM \_ QUERYENDSESSION**](wm-queryendsession.md)
</dt> </dl>

 

 
