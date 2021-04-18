---
UID: ''
title: KeyboardProc 回呼函式
description: 系統呼叫這個函式會取得訊息函式，且會有要處理的鍵盤訊息。
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
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "106968689"
---
# <a name="keyboardproc-function"></a>KeyboardProc 函式

## <a name="description"></a>Description

搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。
每當應用程式呼叫 [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) 函式時，系統就會呼叫這個函式，而 ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) 或 [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) 處理的鍵盤訊息。

**HOOKPROC** 型別定義此回呼函數的指標。
**KeyboardProc** 是應用程式定義或程式庫定義函數名稱的預留位置。

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>參數

### <a name="code-in"></a>程式碼 [in]

類型： **int**

攔截程式用來判斷如何處理訊息的程式碼。
如果程式 *代碼* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。
此參數可以是下列其中一個值。

| 值 | 意義 |
|-------|---------|
| **HC_ACTION** 0 | *WParam* 和 *lParam* 參數包含按鍵訊息的相關資訊。 |
| **HC_NOREMOVE** 3 | *WParam* 和 *lParam* 參數包含按鍵訊息的相關資訊，而且尚未從訊息佇列中移除按鍵訊息。  (名為 **PeekMessage** 函式的應用程式，並指定 **PM_NOREMOVE** 旗標。 )  |

### <a name="wparam-in"></a>wParam [in]

類型： **WPARAM**

產生擊鍵訊息的索引鍵的 [虛擬金鑰程式碼](/windows/desktop/inputdev/virtual-key-codes) 。

### <a name="lparam-in"></a>lParam [in]

類型： **LPARAM**

重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的索引鍵狀態旗標，以及轉換狀態旗標。
如需 *lParam* 參數的詳細資訊，請參閱 [按鍵訊息旗標](/windows/desktop/inputdev/about-keyboard-input)。
下表描述此值的位。

| Bits | Description |
|-------|---------|
| 0-15 | 重複計數。 值是當使用者按住按鍵時，按鍵重複出現的次數。 |
| 16-23 | 掃描程式碼。 此值取決於 OEM。 |
| 24 | 指出金鑰是否為擴充金鑰，例如，函式金鑰或數位鍵臺上的按鍵。 如果金鑰是擴充索引鍵，則值為1。否則，它是0。 |
| 25-28 | 保留的。 |
| 29 | 內容程式碼。 如果 ALT 鍵已關閉，則此值為1。否則，它是0。 |
| 30 | 先前的金鑰狀態。 如果在傳送訊息之前，金鑰已關閉，則此值為 1;如果金鑰已啟動，則為0。 |
| 31 | 轉換狀態。 如果正在按下索引鍵，則值為0，如果正在釋放，則為1。 |

## <a name="returns"></a>傳回

類型： **LRESULT**

如果程式 *代碼* 小於零，則攔截程式必須傳回 **CallNextHookEx** 傳回的值。

如果程式 *代碼* 大於或等於零，而且攔截程式未處理訊息，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_KEYBOARD](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。
如果攔截程式處理訊息，它可能會傳回非零值，以防止系統將訊息傳遞至其餘的攔截鏈或目標視窗程式。

## <a name="remarks"></a>備註

應用程式會在 **SetWindowsHookEx** 函式的呼叫中指定 **WH_KEYBOARD** 攔截類型和攔截程式指標，以安裝攔截程式。

此攔截可能會在其安裝所在的執行緒內容中呼叫。
呼叫是藉由將訊息傳送至已安裝攔截器的執行緒進行。
因此，安裝攔截的執行緒必須有訊息迴圈。

## <a name="see-also"></a>另請參閱

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)

[鉤](hooks.md)
