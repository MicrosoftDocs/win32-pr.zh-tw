---
UID: ''
title: SysMsgProc 回呼函式
description: 系統會在對話方塊、訊息方塊、功能表或捲軸中發生輸入事件之後，呼叫此函式。 |SysMsgProc 回呼函式
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
ms.openlocfilehash: 0d5c7fc116b74dada141e88116ba67209da4a103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106982187"
---
# <a name="sysmsgproc-function"></a>SysMsgProc 函式

## <a name="description"></a>Description

搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。
系統會在對話方塊、訊息方塊、功能表或捲軸中發生輸入事件之後，但在輸入事件所產生的訊息之前，呼叫此函式。
函數可以監視系統中任何對話方塊、訊息方塊、功能表或捲軸的訊息。

**HOOKPROC** 型別定義此回呼函數的指標。
**SysMsgProc** 是應用程式定義或程式庫定義函數名稱的預留位置。

```cpp
LRESULT CALLBACK SysMsgProc(
  _In_ int    nCode,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>參數

### <a name="ncode-in"></a>nCode [in]

類型： **int**

產生訊息的輸入事件種類。
如果 *nCode* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。
此參數可以是下列其中一個值。

| 值 | 意義 |
|-------|---------|
| **MSGF_DIALOGBOX** 0 | 輸入事件發生在訊息方塊或對話方塊中。 |
| **MSGF_MENU** 2 | 輸入事件發生在功能表中。 |
| **MSGF_SCROLLBAR** 5 | 輸入事件發生在捲軸中。 |

### <a name="wparam"></a>wParam

類型： **WPARAM**

不使用這個參數。

### <a name="lparam-in"></a>lParam [in]

類型： **LPARAM**

[訊息訊息結構的指標](/windows/desktop/api/winuser/ns-winuser-msg)。

## <a name="returns"></a>傳回

類型： **LRESULT**

如果 *nCode* 小於零，則攔截程式必須傳回 **CallNextHookEx** 所傳回的值。

如果 *nCode* 大於或等於零，且攔截程式未處理訊息，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_SYSMSGFILTER](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。
如果攔截程式處理訊息，它可能會傳回非零值，以防止系統將訊息傳遞至目標視窗程式。

## <a name="remarks"></a>備註

應用程式會在 **SetWindowsHookEx** 函式的呼叫中指定 **WH_SYSMSGFILTER** 攔截類型和攔截程式指標，以安裝攔截程式。

## <a name="see-also"></a>另請參閱

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[味精](/windows/desktop/api/winuser/ns-winuser-msg)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[鉤](hooks.md)
