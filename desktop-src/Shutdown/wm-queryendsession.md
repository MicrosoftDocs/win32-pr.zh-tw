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
# <a name="wm_queryendsession-message"></a>WM \_ QUERYENDSESSION 訊息

當使用者選擇結束會話時，或當應用程式呼叫其中一個系統關閉函式時，會傳送 **WM \_ QUERYENDSESSION** 訊息。 如果有任何應用程式傳回零，會話就不會結束。 當某個應用程式傳回零時，系統就會停止傳送 **WM \_ QUERYENDSESSION** 訊息。

處理此訊息之後，系統會將 *wParam* 參數設定為的 [**wm \_ ENDSESSION**](wm-endsession.md)訊息傳送至 **wm \_ QUERYENDSESSION** 訊息的結果。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
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

**WM \_ QUERYENDSESSION** 識別碼。

</dd> <dt>

*wParam* 
</dt> <dd>

這個參數保留給未來使用。

</dd> <dt>

*lParam* 
</dt> <dd>

這個參數可以是下列一或多個值。 如果此參數為0，表示系統正在關閉或重新開機 (無法判斷發生) 的事件。



| 值                                                                                                                                                                                                                                           | 意義                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_CLOSEAPP**</dt> <dt>0x00000001</dt> </dl> | 應用程式正在使用必須取代的檔案、系統正在進行服務，或系統資源已用盡。 如需詳細資訊，請參閱 [應用程式的指導方針](../rstmgr/guidelines-for-applications.md)。<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_重大**</dt> <dt>0x40000000</dt> </dl> | 應用程式會強制關機。<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_登出**</dt> <dt>0x80000000</dt> </dl>       | 使用者正在登出。 如需詳細資訊， [請參閱登出](logging-off.md)。<br/>                                                                                                                                   |



 

請注意，此參數是位元遮罩。 若要測試此值，請使用位運算;請勿測試是否相等。

</dd> </dl>

## <a name="return-value"></a>傳回值

應用程式應該遵守使用者的意圖，並傳回 **TRUE**。 根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數會針對此訊息傳回 **TRUE** 。

如果關機會損毀正在燒錄的系統或媒體，則應用程式可能會傳回 **FALSE**。 不過，最好的作法是採用使用者的動作。

## <a name="remarks"></a>備註

當應用程式針對此訊息傳回 **TRUE** 時，不論其他應用程式如何回應 **wm \_ QUERYENDSESSION** 訊息，它都會收到 [**WM \_ ENDSESSION**](wm-endsession.md)訊息。 每個應用程式在收到此訊息時，都應該立即傳回 **TRUE** 或 **FALSE** ，並延遲任何清除作業，直到接收到 **WM \_ ENDSESSION** 訊息為止。

應用程式可以顯示使用者介面，以在關機時提示使用者輸入資訊，不過不建議這麼做。 五秒後，系統會顯示導致關機的應用程式相關資訊，並允許使用者將其終止。 例如，Windows XP 會顯示一個對話方塊，而 Windows Vista 會顯示全螢幕，內含應用程式封鎖關機的其他相關資訊。 如果您的應用程式必須封鎖或延遲系統關機，請使用 [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) 函數。 如需詳細資訊，請參閱 [Windows Vista 的關機變更](shutdown-changes-for-windows-vista.md)。

主控台應用程式可以使用 [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) 函式來接收關機通知。

服務應用程式可以使用 [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) 函式來接收處理常式常式中的關機通知。

## <a name="examples"></a>範例

如需範例，請 [參閱登出](logging-off.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | Windows Server 2003 \[ desktop app \| UWP 應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>WinUser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[登出](logging-off.md)
</dt> <dt>

[關閉](shutting-down.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**WM \_ ENDSESSION**](wm-endsession.md)
</dt> </dl>

 

 
