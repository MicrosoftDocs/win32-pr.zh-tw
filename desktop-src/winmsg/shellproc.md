---
UID: ''
title: ShellProc 回呼函式
description: 函式會從系統接收 Shell 事件的通知。
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
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "106968895"
---
# <a name="shellproc-function"></a>ShellProc 函式

## <a name="description"></a>Description

搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。
函式會從系統接收 Shell 事件的通知。

**HOOKPROC** 型別定義此回呼函數的指標。
**ShellProc** 是應用程式定義或程式庫定義函數名稱的預留位置。

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>參數

### <a name="ncode-in"></a>nCode [in]

類型： **int**

攔截程式碼。
如果 *nCode* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。
此參數可以是下列其中一個值。

| 值 | 意義 |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** 11 | 協助工具狀態已變更。 |
| **HSHELL_ACTI加值稅ESHELLWINDOW** 3 | Shell 應會啟用其主視窗。 |
| **HSHELL_APPCOMMAND** 12 | 使用者已完成輸入事件 (例如，按下滑鼠上的應用程式命令按鈕或鍵盤上的應用程式命令鍵) ，而且應用程式未處理該輸入所產生的 [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) 訊息。 如果 Shell 程式處理 [WM_COMMAND](/windows/desktop/menurc/wm-command) 訊息，則不應呼叫 **CallNextHookEx**。 如需詳細資訊，請參閱傳回值一節。 |
| **HSHELL_GETMINRECT** 5 | 視窗會最小化或最大化。 系統需要視窗的最小化矩形座標。 |
| **HSHELL_LANGUAGE** 8 | 鍵盤語言已變更或已載入新的鍵盤配置。 |
| **HSHELL_REDRAW** 6 | 已重新繪製工作列中視窗的標題。 |
| **HSHELL_TASKMAN** 7 | 使用者已選取 [工作清單]。 提供工作清單的 shell 應用程式應該會傳回 **TRUE** ，以防止 Windows 啟動其工作清單。 |
| **HSHELL_WINDOWACTI加值稅ED** 4 | 啟用已變更為不同的最上層、無主視窗。 |
| **HSHELL_WINDOWCREATED** 1 | 已建立最上層的無主視窗。 當系統呼叫此攔截時，會存在此視窗。 |
| **HSHELL_WINDOWDESTROYED** 2 | 最上層的無主視窗即將終結。 當系統呼叫此攔截時，視窗仍然存在。 |
| **HSHELL_WINDOWREPLACED** 13 | 即將取代最上層視窗。 當系統呼叫此攔截時，會存在此視窗。 |

### <a name="wparam-in"></a>wParam [in]

類型： **WPARAM**

此參數取決於 *nCode* 參數的值，如下表所示。

| nCode | wParam |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** | 指出哪些協助工具已變更狀態。 這個值是下列其中一項： **ACCESS_FILTERKEYS**、 **ACCESS_MOUSEKEYS** 或 **ACCESS_STICKYKEYS**。 |
| **HSHELL_APPCOMMAND** | 指出 **WM_APPCOMMAND** 訊息最初傳送的位置;例如，視窗的控制碼。 如需詳細資訊，請參閱 **WM_APPCOMMAND** 中的 cmd 參數。 |
| **HSHELL_GETMINRECT** | 最小化或最大化視窗的控制碼。 |
| **HSHELL_LANGUAGE** | 視窗的控制碼。 |
| **HSHELL_REDRAW** | 重新繪製之視窗的控制碼。 |
| **HSHELL_WINDOWACTI加值稅ED** | 已啟動視窗的控制碼。 |
| **HSHELL_WINDOWCREATED** | 已建立之視窗的控制碼。 |
| **HSHELL_WINDOWDESTROYED** | 已損毀視窗的控制碼。 |
| **HSHELL_WINDOWREPLACED** | 要取代之視窗的控制碼。 Windows 2000：不支援。 |

### <a name="lparam-in"></a>lParam [in]

類型： **LPARAM**

此參數取決於 *nCode* 參數的值，如下表所示。

| nCode | lParam |
|-------|---------|
| **HSHELL_APPCOMMAND** | `GET_APPCOMMAND_LPARAM(lParam)` 是對應至輸入事件的應用程式命令。 `GET_DEVICE_LPARAM(lParam)` 表示產生輸入事件的專案;例如滑鼠或鍵盤。 如需詳細資訊，請參閱 **WM_APPCOMMAND** 下的 *uDevice* 參數描述。 `GET_FLAGS_LPARAM(lParam)`取決於 **WM_APPCOMMAND** 中 *cmd* 的值。 例如，它可能會指出最初傳送 **WM_APPCOMMAND** 訊息時，哪些虛擬機器碼已關閉。 如需詳細資訊，請參閱 **WM_APPCOMMAND** 下的 *dwCmdFlags* description 參數。 |
| **HSHELL_GETMINRECT** | [矩形](/previous-versions/dd162897(v=vs.85))結構的指標。 |
| **HSHELL_LANGUAGE** | 鍵盤配置的控制碼。 |
| **HSHELL_MONITORCHANGED** | 移至不同監視的視窗控制碼。 |
| **HSHELL_REDRAW** | 如果視窗閃爍，此值為 **TRUE** ，否則為 **FALSE** 。 |
| **HSHELL_WINDOWACTI加值稅ED** | 如果視窗處於全螢幕模式，則此值為 TRUE，否則為 **FALSE** 。 |
| **HSHELL_WINDOWREPLACED** | 新視窗的控制碼。 Windows 2000：不支援。 |

## <a name="returns"></a>傳回

類型： **LRESULT**

除非 nCode 的值 **HSHELL_APPCOMMAND** ，而且 shell 程式處理 **WM_COMMAND** 訊息，否則傳回值應為零。
在此情況下，傳回值應為非零。

## <a name="remarks"></a>備註

藉由在 **SetWindowsHookEx** 函式的呼叫中指定 [WH_SHELL](about-hooks.md)攔截類型和攔截程式的指標，來安裝此攔截程式。

## <a name="see-also"></a>另請參閱

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand)

[WM_COMMAND](/windows/desktop/menurc/wm-command)

[鉤](hooks.md)
