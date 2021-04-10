---
description: 本節討論勾點。 攔截是系統訊息處理機制中的一個點，可讓應用程式安裝副程式來監視訊息流量。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\hooks.htm
title: 鉤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74057d25e3152c8782c2be364688bb971b08ddf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194564"
---
# <a name="hooks"></a>鉤

攔截是系統訊息處理機制中的一個點，應用程式可以在其中安裝副程式來監視系統中的訊息流量，並在到達目標視窗程式之前處理特定類型的訊息。

### <a name="in-this-section"></a>本節內容



| Name                                 | 描述                                                         |
|--------------------------------------|---------------------------------------------------------------------|
| [勾點總覽](about-hooks.md)     | 討論如何使用勾點。<br/>                      |
| [使用攔截](using-hooks.md)       | 示範如何執行與攔截相關聯的工作。<br/> |
| [勾點參考](hook-reference.md) | 包含 API 參考。<br/>                              |



 

### <a name="hook-functions"></a>攔截函式



| Name                                               | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera)             | 將指定的訊息和攔截程式碼傳遞給與 [**WH \_ SYSMSGFILTER**](about-hooks.md) 和 **WH \_ MSGFILTER** 攔截程式相關聯的攔截程式。<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex)           | 將攔截資訊傳遞給目前攔截鏈中的下一個勾點程式。 攔截程式可以在處理勾點資訊之前或之後呼叫此函式。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85))                   | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 系統會在呼叫視窗程式之前呼叫這個函式，以處理傳送至執行緒的訊息。<br/>                                                                                                                                                                                                                                                                                                                                               |
| [*CallWndRetProc*](/windows/win32/api/winuser/nc-winuser-hookproc)             | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 系統會在呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式之後呼叫這個函數。 攔截程式可以檢查訊息;它無法加以修改。 <br/>                                                                                                                                                                                                                                                                                         |
| [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85))                           | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 系統會先呼叫此函式，再啟用、建立、終結、最小化、最大化、移動或調整視窗大小;完成系統命令之前，從系統訊息佇列移除滑鼠或鍵盤事件之前，設定鍵盤焦點之前：或在與系統訊息佇列同步處理之前。 以電腦為基礎的訓練 (CBT) 應用程式會使用此攔截程式從系統接收有用的通知。 <br/> |
| [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85))                       | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 系統會先呼叫此函式，然後再呼叫與任何類型之攔截相關的攔截程式。 系統會將要呼叫之攔截的相關資訊傳遞給 [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85)) 攔截程式，以檢查資訊並判斷是否允許呼叫攔截。 <br/>                                                                                                                                                  |
| [*ForegroundIdleProc*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85))     | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 只要前景執行緒即將變成閒置狀態，系統就會呼叫這個函數。 <br/>                                                                                                                                                                                                                                                                                                                                                                   |
| [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))                     | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 每當 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函式從應用程式訊息佇列抓取訊息時，系統就會呼叫這個函式。 將抓取的訊息傳回給呼叫者之前，系統會將訊息傳遞至攔截程式。 <br/>                                                                                                                                                        |
| [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))   | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 一般而言，應用程式會使用此函式來播放一系列 [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) 攔截程式先前錄製的滑鼠和鍵盤訊息。 只要安裝了 [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) 勾點程式，就會停用一般的滑鼠和鍵盤輸入。 <br/>                                                                                                                       |
| [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))       | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 此函數會記錄系統從系統訊息佇列中移除的訊息。 之後，應用程式可以使用 [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) 勾點來播放訊息。 <br/>                                                                                                                                                                                                                                               |
| [*KeyboardProc*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85))                 | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 每當應用程式呼叫 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函式時，系統就會呼叫這個函式，而) 要處理的鍵盤訊息 ([**wm \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) 或 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 。 <br/>                                                                                                                                                                         |
| [*LowLevelKeyboardProc*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85)) | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 每次有新的鍵盤輸入事件張貼到執行緒輸入佇列時，系統就會呼叫這個函式。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [*LowLevelMouseProc*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85))       | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 每次有新的滑鼠輸入事件張貼到執行緒輸入佇列時，系統就會呼叫這個函數。<br/>                                                                                                                                                                                                                                                                                                                                        |
| [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85))                   | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 系統會在對話方塊、訊息方塊、功能表或捲軸中發生輸入事件之後，但在輸入事件所產生的訊息之前，呼叫此函式。 攔截程式可以監視特定應用程式或所有應用程式所建立之對話方塊、訊息方塊、功能表或捲軸的訊息。<br/>                                                                                                                       |
| [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85))                       | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 每當應用程式呼叫 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函式，且有要處理的滑鼠訊息時，系統就會呼叫這個函式。 <br/>                                                                                                                                                                                                                                                           |
| [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)       | 將應用程式定義的勾點程式安裝到勾點。 您可以安裝攔截程式，以監視特定事件種類的系統。 這些事件會與特定的執行緒或相同桌面上的所有線程相關聯，做為呼叫的執行緒。<br/>                                                                                                                                                                                                                                                                                                           |
| [*ShellProc*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))                       | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 函式會從系統接收 Shell 事件的通知。<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [*SysMsgProc*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85))                     | 搭配 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式使用的應用程式定義或程式庫定義的回呼函數。 系統會在對話方塊、訊息方塊、功能表或捲軸中發生輸入事件之後，但在輸入事件所產生的訊息之前，呼叫此函式。 函數可以監視系統中任何對話方塊、訊息方塊、功能表或捲軸的訊息。 <br/>                                                                                                                                                                    |
| [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex) | 移除 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式在勾點中安裝的勾點程式。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="hook-notifications"></a>攔截通知



| Name                                          | 描述                                                                                                                                                                         |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CANCELJOURNAL**](wm-canceljournal.md) | 當使用者取消應用程式的日誌活動時，張貼至應用程式。 訊息是以 **Null** 視窗控制碼張貼。 <br/>                              |
| [**WM \_ QUEUESYNC**](wm-queuesync.md)         | 由 CBT 應用程式傳送，以分隔使用者輸入訊息與透過 [**WH \_ JOURNALPLAYBACK**](about-hooks.md) 程式傳送的其他訊息。 <br/> |



 

### <a name="hook-structures"></a>攔截結構



| Name                                           | 描述                                                                                                                                                                                                                 |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBT \_ CREATEWND**](/windows/win32/api/winuser/ns-winuser-cbt_createwnda)        | 包含在建立視窗之前傳遞給 **WH \_ CBT** 攔截程式 [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85))的資訊。<br/>                                                                                               |
| [**CBTACTI加值稅ESTRUCT**](/windows/win32/api/winuser/ns-winuser-cbtactivatestruct) | 包含在啟動視窗之前傳遞給 **WH \_ CBT** 攔截程式 [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85))的資訊。 <br/>                                                                                            |
| [**CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct)           | 定義傳遞至 **WH \_ CALLWNDPROCRET** 攔截程式 [*CallWndRetProc*](/windows/win32/api/winuser/nc-winuser-hookproc)的訊息參數。 <br/>                                                                                       |
| [**CWPSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpstruct)                 | 定義傳遞至 **WH \_ CALLWNDPROC** 攔截程式 [*CALLWNDPROC*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85))的訊息參數。 <br/>                                                                                                |
| [**DEBUGHOOKINFO**](/windows/win32/api/winuser/ns-winuser-debughookinfo)         | 包含傳遞至 **WH \_ DEBUG** 攔截程式 [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85))的偵錯工具資訊。 <br/>                                                                                                          |
| [**EVENTMSG**](/windows/win32/api/winuser/ns-winuser-eventmsg)                   | 包含傳送至系統訊息佇列之硬體訊息的相關資訊。 這個結構是用來儲存 [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) 回呼函數的訊息資訊。 <br/> |
| [**KBDLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-kbdllhookstruct)     | 包含低層級鍵盤輸入事件的相關資訊。 <br/>                                                                                                                                                    |
| [**MOUSEHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-mousehookstruct)     | 包含傳遞至 **WH \_ 滑鼠** 掛勾程式 [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85))的滑鼠事件相關資訊。 <br/>                                                                                                |
| [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex) | 包含傳遞至 **WH \_ 滑鼠** 掛勾程式 [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85))的滑鼠事件相關資訊。 <br/>                                                                                                |
| [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)       | 包含低層級滑鼠輸入事件的相關資訊。 <br/>                                                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**SetWinEventHook**](/windows/desktop/api/winuser/nf-winuser-setwineventhook)
</dt> </dl>

 

