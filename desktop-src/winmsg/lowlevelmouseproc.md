---
UID: ''
title: LowLevelMouseProc 回呼函式
description: 每次有新的滑鼠輸入事件張貼到執行緒輸入佇列時，系統就會呼叫這個函數。
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 53f75d14395388ce22ce86ef73f8819892c3fe7285909b1f38c801af476636a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705784"
---
# <a name="lowlevelmouseproc-function"></a>LowLevelMouseProc 函式

## <a name="description"></a>描述

搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。
每次有新的滑鼠輸入事件張貼到執行緒輸入佇列時，系統就會呼叫這個函數。

**HOOKPROC** 型別定義此回呼函數的指標。
**LowLevelMouseProc** 是應用程式定義或程式庫定義函數名稱的預留位置。

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>參數

### <a name="ncode-in"></a>nCode [in]

類型： **int**

攔截程式用來判斷如何處理訊息的程式碼。
如果 *nCode* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。
此參數可以是下列其中一個值。

| 值 | 意義 |
|-------|---------|
| **HC_ACTION** 0 | *WParam* 和 *lParam* 參數包含滑鼠訊息的相關資訊。 |

### <a name="wparam-in"></a>wParam [in]

類型： **WPARAM**

滑鼠訊息的識別碼。
這個參數可以是下列其中一個訊息： [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)、 [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup)、 [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove)、 [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)、 [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) 或 [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)。

### <a name="lparam-in"></a>lParam [in]

類型： **LPARAM**

[MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)結構的指標。

## <a name="returns"></a>傳回

類型： **LRESULT**

如果 *nCode* 小於零，則攔截程式必須傳回 **CallNextHookEx** 所傳回的值。

如果 *nCode* 大於或等於零，且攔截程式未處理訊息，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_MOUSE_LL](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。
如果攔截程式處理訊息，它可能會傳回非零值，以防止系統將訊息傳遞至其餘的攔截鏈或目標視窗程式。

## <a name="remarks"></a>備註

應用程式會在 **SetWindowsHookEx** 函式的呼叫中指定 **WH_MOUSE_LL** 攔截類型和攔截程式指標，以安裝攔截程式。

此攔截器會在其安裝所在的執行緒內容中呼叫。
呼叫是藉由將訊息傳送至已安裝攔截器的執行緒進行。
因此，安裝攔截的執行緒必須有訊息迴圈。

滑鼠輸入可以來自本機滑鼠驅動程式，或是來自 [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) 函式的呼叫。
如果輸入來自 **mouse_event** 的呼叫，則輸入為「已插入」。
不過， **WH_MOUSE_LL** 的勾點不會插入另一個進程。
相反地，內容會切換回已安裝攔截的進程，並在其原始內容中呼叫。
然後，內容會切換回產生事件的應用程式。

攔截程式應處理訊息的時間，比下列登錄機碼中 **LowLevelHooksTimeout** 值指定的資料輸入少： **HKEY_CURRENT_USER\Control Panel\Desktop**。

值會以毫秒來表示。
如果攔截程式超時，系統會將訊息傳遞至下一個攔截。
不過，在 Windows 7 和更新版本上，會以無訊息方式移除攔截，而不需要呼叫。
應用程式沒有辦法知道是否已移除攔截。

**注意：**  偵錯工具攔截無法追蹤這種類型的低層級滑鼠掛勾。
如果應用程式必須使用低層級的勾點，則應該在將工作關閉到工作者執行緒的專用線程上執行勾點，然後立即傳回。
在大部分的情況下，應用程式必須使用低層級的勾點，而改為監視原始輸入。
這是因為原始輸入可以更有效率地監視以其他執行緒為目標的滑鼠和鍵盤訊息，而非低層級的勾點。
如需原始輸入的詳細資訊，請參閱 [原始輸入](/windows/desktop/inputdev/raw-input)。

## <a name="see-also"></a>另請參閱

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)

[WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup)

[WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove)

[WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)

[WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown)

[WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)

[勾點](hooks.md)

[關於勾點](about-hooks.md)
