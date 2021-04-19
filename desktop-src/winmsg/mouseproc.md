---
UID: ''
title: MouseProc 回呼函式
description: 當應用程式呼叫訊息函式時，系統會呼叫此函式，而且會有要處理的滑鼠訊息。
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "106969697"
---
# <a name="mouseproc-function"></a>MouseProc 函式

## <a name="description"></a>Description

搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。
每當應用程式呼叫 [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) 函式，且有要處理的滑鼠訊息時，系統就會呼叫這個函式。

**HOOKPROC** 型別定義此回呼函數的指標。
**MouseProc** 是應用程式定義或程式庫定義函數名稱的預留位置。

```cpp
LRESULT CALLBACK MouseProc(
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
| **HC_NOREMOVE** 3 | *WParam* 和 *lParam* 參數包含滑鼠訊息的相關資訊，而且滑鼠訊息尚未從訊息佇列中移除。  (名為 **PeekMessage** 函式的應用程式，並指定 **PM_NOREMOVE** 旗標。 )  |

### <a name="wparam-in"></a>wParam [in]

類型： **WPARAM**

滑鼠訊息的識別碼。

### <a name="lparam-in"></a>lParam [in]

類型： **LPARAM**

[MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)結構的指標。

## <a name="returns"></a>傳回

類型： **LRESULT**

如果 *nCode* 小於零，則攔截程式必須傳回 **CallNextHookEx** 所傳回的值。

如果 *nCode* 大於或等於零，且攔截程式未處理訊息，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_MOUSE](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。
如果攔截程式處理訊息，它可能會傳回非零值，以防止系統將訊息傳遞至目標視窗程式。

## <a name="remarks"></a>備註

應用程式會在 **SetWindowsHookEx** 函式的呼叫中指定 WH_MOUSE 攔截類型和攔截程式指標，以安裝攔截程式。

攔截程式不得安裝 [WH_JOURNALPLAYBACK](about-hooks.md) 回呼函數。

此攔截可能會在其安裝所在的執行緒內容中呼叫。
呼叫是藉由將訊息傳送至已安裝攔截器的執行緒進行。
因此，安裝攔截的執行緒必須有訊息迴圈。

## <a name="see-also"></a>另請參閱

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[鉤](hooks.md)

[關於勾點](about-hooks.md)
