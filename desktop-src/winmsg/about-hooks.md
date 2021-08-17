---
description: 本主題討論如何使用勾點。
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: 攔截
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10754f7275ce06c17b668e04c7792e6296a854fbe14a6ebc9544fbb70c73e9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201223"
---
# <a name="hooks-overview"></a>攔截

攔截 *器是一* 種機制，可讓應用程式攔截事件，例如訊息、滑鼠動作和按鍵。 攔截特定事件種類的函式稱為攔截 *程式。* 攔截程式可以對它收到的每個事件採取動作，然後修改或捨棄事件。

下列範例會使用於攔截：

-   監視訊息以進行調試
-   提供宏錄製和播放的支援
-   提供 help 鍵支援 (F1) 
-   模擬滑鼠和鍵盤輸入
-   執行以電腦為基礎的訓練 (CBT) 應用程式

> [!Note]  
> 攔截通常會讓系統變慢，因為它們會增加系統必須針對每個訊息執行的處理量。 您應該只在必要時才安裝攔截，並儘快將它移除。

 

本節將討論下列各項：

-   [攔截鏈](#hook-chains)
-   [攔截程式](#hook-procedures)
-   [掛勾類型](#hook-types)
    -   [WH \_ CALLWNDPROC 和 WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
    -   [WH \_ CBT](#wh_cbt)
    -   [WH \_ DEBUG](#wh_debug)
    -   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
    -   [WH \_ GETMESSAGE](#wh_getmessage)
    -   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
    -   [WH \_ JOURNALRECORD](#wh_journalrecord)
    -   [WH \_ 鍵盤 \_ LL](#wh_keyboard_ll)
    -   [WH \_ 鍵盤](#wh_keyboard)
    -   [WH \_ 滑鼠 \_ LL](#wh_mouse_ll)
    -   [WH \_ 滑鼠](#wh_mouse)
    -   [WH \_ MSGFILTER 和 WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [WH \_ SHELL](#wh_shell)

## <a name="hook-chains"></a>攔截鏈

系統支援許多不同類型的攔截;每個類型都可讓您存取其訊息處理機制的不同層面。 例如，應用程式可以使用 WH 的 [ \_ 滑鼠](#wh_mouse) 掛勾來監視滑鼠訊息的訊息流量。

系統會針對每一種類型的勾點維護個別的勾點。 攔截 *鏈* 是指向特殊應用程式定義回呼函式的指標清單，稱為攔截 *程式*。 當發生與特定類型之攔截相關聯的訊息時，系統會將該訊息傳遞給勾點中所參考的每個攔截程式，然後再一次。 攔截程式可以採取的動作取決於所涉及的掛勾類型。 某些攔截程式類型的攔截程式只能監視訊息;其他人可以修改訊息或停止其進度，使其無法到達下一個勾點程式或目的地視窗。

## <a name="hook-procedures"></a>攔截程式

為了充分利用特定類型的攔截程式，開發人員會提供攔截程式，並使用 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式將它安裝到與攔截相關聯的鏈中。 攔截程式必須有下列語法：

``` syntax
LRESULT CALLBACK HookProc(
  int nCode, 
  WPARAM wParam, 
  LPARAM lParam
)
{
   // process event
   ...

   return CallNextHookEx(NULL, nCode, wParam, lParam);
}
```

*HookProc* 是應用程式定義名稱的預留位置。

*NCode* 參數是攔截程式用來判斷要執行之動作的攔截程式碼。 攔截程式碼的值取決於攔截的類型;每個類型都有自己的一組特性，也就是攔截碼。 *WParam* 和 *lParam* 參數的值取決於攔截程式碼，但它們通常包含已傳送或張貼之訊息的相關資訊。

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)函式一律會在攔截鏈的開頭安裝攔截程式。 當特定類型的攔截器所監視的事件發生時，系統會在與攔截相關聯的掛勾鏈開頭呼叫程式。 鏈中的每個攔截程式會決定是否要將事件傳遞到下一個程式。 攔截程式會藉由呼叫 [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex) 函數，將事件傳遞至下一個程式。

請注意，某些攔截程式類型的攔截程式只能監視訊息。 無論特定程式是否呼叫 [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex)，系統都會將訊息傳遞至每個攔截程式。

*全域* 攔截會監視與呼叫執行緒位於相同桌面的所有線程的訊息。 *執行緒特定的勾* 點只會監視個別執行緒的訊息。 全域攔截程式可以在與呼叫執行緒相同的桌面的任何應用程式內容中呼叫，因此程式必須位於不同的 DLL 模組中。 只有在相關聯的執行緒內容中，才會呼叫執行緒特定的勾點程式。 如果應用程式為它自己的其中一個執行緒安裝攔截程式，則攔截程式可以是與應用程式的其餘部分程式碼或 DLL 中的其他程式碼相同的模組。 如果應用程式針對不同應用程式的執行緒安裝攔截程式，則程式必須位於 DLL 中。 如需詳細資訊，請參閱 [動態連結程式庫](../dlls/dynamic-link-libraries.md)。

> [!Note]  
> 您應該只針對進行調試時使用全域攔截;否則，您應該避免這些問題。 全域勾點會危害系統效能，並與其他可執行相同類型之全域攔截的應用程式產生衝突。

 

## <a name="hook-types"></a>掛勾類型

每種類型的勾點都可讓應用程式監視系統訊息處理機制的不同層面。 下列各節說明可用的勾點。

-   [WH \_ CALLWNDPROC 和 WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
-   [WH \_ CBT](#wh_cbt)
-   [WH \_ DEBUG](#wh_debug)
-   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
-   [WH \_ GETMESSAGE](#wh_getmessage)
-   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
-   [WH \_ JOURNALRECORD](#wh_journalrecord)
-   [WH \_ 鍵盤 \_ LL](#wh_keyboard_ll)
-   [WH \_ 鍵盤](#wh_keyboard)
-   [WH \_ 滑鼠 \_ LL](#wh_mouse_ll)
-   [WH \_ 滑鼠](#wh_mouse)
-   [WH \_ MSGFILTER 和 WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
-   [WH \_ SHELL](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>WH \_ CALLWNDPROC 和 WH \_ CALLWNDPROCRET

**WH \_ CALLWNDPROC** 和 **WH \_ CALLWNDPROCRET** 勾點可讓您監視傳送至視窗程式的訊息。 系統會先呼叫 **WH \_ CALLWNDPROC** 攔截程式，再將訊息傳遞至接收視窗程式，並在視窗程式處理訊息之後呼叫 **WH \_ CALLWNDPROCRET** 攔截程式。

**WH \_ CALLWNDPROCRET** 勾點會將 [**CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct)結構的指標傳遞至攔截程式。 結構包含處理訊息之視窗程式的傳回值，以及與訊息相關聯的訊息參數。 子類別化視窗不適用於在進程間設定的訊息。

如需詳細資訊，請參閱 [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) 和 [*CallWndRetProc*](/windows/win32/api/winuser/nc-winuser-hookproc) 回呼函數。

### <a name="wh_cbt"></a>WH \_ CBT

系統會先呼叫 **WH 的 \_ CBT** 攔截程式，然後再啟用、建立、終結、最小化、最大化、移動或調整視窗大小、完成系統命令之前，先從系統訊息佇列移除滑鼠或鍵盤事件，然後再設定輸入焦點，或在與系統訊息佇列進行同步處理之前。 攔截程式傳回的值會決定系統是否允許或防止其中一項作業。 **WH 的 \_ cbt** 攔截主要用於以電腦為基礎的訓練 (CBT) 應用程式。

如需詳細資訊，請參閱 [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)) 回呼函數。

如需詳細資訊，請參閱 [WinEvents](/windows/desktop/WinAuto/winevents-infrastructure)。

### <a name="wh_debug"></a>WH \_ DEBUG

系統會先呼叫 **WH \_** 的偵測攔截程式，再呼叫與系統中任何其他連結相關聯的勾點程式。 您可以使用此攔截來判斷是否允許系統呼叫與其他類型之攔截相關聯的勾點程式。

如需詳細資訊，請參閱 [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85)) 回呼函數。

### <a name="wh_foregroundidle"></a>WH \_ FOREGROUNDIDLE

**WH \_ FOREGROUNDIDLE** 勾點可讓您在其前景執行緒閒置的期間，執行低優先順序的工作。 當應用程式的前景執行緒即將閒置時，系統會呼叫 **WH \_ FOREGROUNDIDLE** 攔截程式。

如需詳細資訊，請參閱 [*ForegroundIdleProc*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85)) 回呼函數。

### <a name="wh_getmessage"></a>WH \_ GETMESSAGE

**WH \_ GETMESSAGE** 攔截可讓應用程式監視有關 [**GETMESSAGE**](/windows/win32/api/winuser/nf-winuser-getmessage)或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)函式所傳回的訊息。 您可以使用 **WH \_ GETMESSAGE** 掛勾來監視滑鼠和鍵盤輸入，以及張貼至訊息佇列的其他訊息。

如需詳細資訊，請參閱 [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) 回呼函數。

### <a name="wh_journalplayback"></a>WH \_ JOURNALPLAYBACK

**WH \_ JOURNALPLAYBACK** 攔截可讓應用程式將訊息插入系統訊息佇列。 您可以使用此攔截來播放先前使用 [WH \_ JOURNALRECORD](#wh_journalrecord)錄製的一系列滑鼠和鍵盤事件。 只要安裝了 **WH \_ JOURNALPLAYBACK** 勾點，就會停用一般滑鼠和鍵盤輸入。 **WH \_ JOURNALPLAYBACK** 攔截是一種全域攔截，不能用來做為執行緒特定的勾點。

**WH \_ JOURNALPLAYBACK** 勾點會傳回超時值。 此值會告訴系統在處理來自播放攔截的目前訊息之前，要等待的毫秒數。 這可讓攔截控制其播放事件的時間。

如需詳細資訊，請參閱 [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) 回呼函數。

### <a name="wh_journalrecord"></a>WH \_ JOURNALRECORD

**WH \_ JOURNALRECORD** 勾點可讓您監視和記錄輸入事件。 一般來說，您會使用這個攔截來記錄一系列的滑鼠和鍵盤事件，稍後再使用 [WH \_ JOURNALPLAYBACK](#wh_journalplayback)播放。 **WH \_ JOURNALRECORD** 攔截是一種全域攔截，不能用來做為執行緒特定的勾點。

如需詳細資訊，請參閱 [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) 回呼函數。

### <a name="wh_keyboard_ll"></a>WH \_ 鍵盤 \_ LL

**WH \_ 鍵盤 \_** 串連可讓您監視要張貼線上程輸入佇列中的鍵盤輸入事件。

如需詳細資訊，請參閱 [*LowLevelKeyboardProc*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85)) 回呼函數。

### <a name="wh_keyboard"></a>WH \_ 鍵盤

**WH \_ 鍵盤** 勾點可讓應用程式監視有關 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)函式所傳回之 [**wm \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)和 [**wm \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)訊息的訊息流量。 您可以使用 **WH \_ 鍵盤** 掛勾來監視張貼至訊息佇列的鍵盤輸入。

如需詳細資訊，請參閱 [*KeyboardProc*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85)) 回呼函數。

### <a name="wh_mouse_ll"></a>WH \_ 滑鼠 \_ LL

**WH 的 \_ 滑鼠 \_ LL** 可讓您監視要張貼線上程輸入佇列中的滑鼠輸入事件。

如需詳細資訊，請參閱 [*LowLevelMouseProc*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85)) 回呼函數。

### <a name="wh_mouse"></a>WH \_ 滑鼠

**WH 的 \_ 滑鼠** 勾點可讓您監視有關 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)函式要傳回的滑鼠訊息。 您可以使用 **WH \_ 滑鼠** 掛勾來監視張貼到訊息佇列的滑鼠輸入。

如需詳細資訊，請參閱 [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)) 回呼函數。

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>WH \_ MSGFILTER 和 WH \_ SYSMSGFILTER

**WH \_ MSGFILTER** 和 **WH \_ SYSMSGFILTER** 勾點可讓您監視要由功能表、捲軸、訊息方塊或對話方塊處理的訊息，以及偵測當使用者按下 ALT + tab 或 ALT + ESC 鍵組合時，何時即將啟動不同的視窗。 **WH \_ MSGFILTER** 攔截只能監視傳遞至已安裝攔截程式之應用程式所建立之功能表、捲軸、訊息方塊或對話方塊的訊息。 **WH \_ SYSMSGFILTER** 攔截會監視所有應用程式的這類訊息。

**WH \_ MSGFILTER** 和 **WH \_ SYSMSGFILTER** 勾點可讓您在強制回應迴圈期間執行訊息篩選，這相當於在主要訊息迴圈中完成的篩選。 例如，應用程式通常會在從佇列中取得訊息的時間和分派訊息的時間之間，檢查主迴圈中的新訊息，並適當地執行特殊處理。 不過，在強制回應迴圈期間，系統會在不允許應用程式在其主要訊息迴圈中篩選訊息的機會下，抓取並分派訊息。 如果應用程式安裝 **WH \_ MSGFILTER** 或 **WH \_ SYSMSGFILTER** 攔截程式，系統會在強制回應迴圈期間呼叫程式。

應用程式可以藉由呼叫 [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera)函式，直接呼叫 **WH \_ MSGFILTER** 掛勾。 藉由使用這個函數，應用程式可以使用相同的程式碼在強制回應迴圈期間篩選訊息，因為它在主要訊息迴圈中使用。 若要這樣做，請在 **WH \_ MSGFILTER** 攔截程式中封裝篩選作業，並在 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)和 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)函數的呼叫之間呼叫 **CallMsgFilter** 。

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

[**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera)的最後一個引數會直接傳遞至攔截程式;您可以輸入任何值。 藉由定義常數（例如 **MSGF \_ MAINLOOP**），攔截程式就可以使用此值來判斷呼叫程式的位置。

如需詳細資訊，請參閱 [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) 和 [*SysMsgProc*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85)) 回呼函數。

### <a name="wh_shell"></a>WH \_ SHELL

Shell 應用程式可以使用 **WH \_ shell** 攔截來接收重要通知。 當 SHELL 應用程式即將啟動，以及建立或終結最上層視窗時，系統會呼叫 **WH \_ shell** 攔截程式。

請注意，自訂 shell 應用程式不會接收 **WH \_ shell** 訊息。 因此，將本身註冊為預設 shell 的任何應用程式，都必須在 (之前呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式，或任何其他應用程式) 可以接收 **WH \_ shell** 訊息。 您必須使用 **SPI \_ SETMINIMIZEDMETRICS** 和 [**MINIMIZEDMETRICS**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) 結構來呼叫此函數。 將此結構的 **iArrange** 成員設定為 **ARW \_ HIDE**。

如需詳細資訊，請參閱 [*ShellProc*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) 回呼函數。

 

 
