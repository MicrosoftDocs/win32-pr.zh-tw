---
UID: ''
title: MessageProc 回呼函式
description: 系統會在對話方塊、訊息方塊、功能表或捲軸中發生輸入事件之後，呼叫此函式。 |MessageProc 回呼函式
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
ms.openlocfilehash: 6da307d00c9291ab8c27b97c5012c9887b5c12fcbc541beb5a9b7e8c176ec5a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200780"
---
# <a name="messageproc-function"></a>MessageProc 函式

## <a name="description"></a>Description

搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。
系統會在對話方塊、訊息方塊、功能表或捲軸中發生輸入事件之後，但在輸入事件所產生的訊息之前，呼叫此函式。
攔截程式可以監視特定應用程式或所有應用程式所建立之對話方塊、訊息方塊、功能表或捲軸的訊息。

**HOOKPROC** 型別定義此回呼函數的指標。
**MessageProc** 是應用程式定義或程式庫定義函數名稱的預留位置。

```cpp
LRESULT CALLBACK MessageProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>參數

### <a name="code-in"></a>程式碼 [in]

類型： **int**

產生訊息的輸入事件種類。
如果程式 *代碼* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並傳回 **CallNextHookEx** 所傳回的值。
此參數可以是下列其中一個值。

| 值 | 意義 |
|-------|---------|
| **MSGF_DDEMGR** 0x8001 | 當動態資料交換管理程式庫 (DDEML) 等待同步交易完成時，就會發生輸入事件。 如需 DDEML 的詳細資訊，請參閱[動態資料交換管理程式庫](../dataxchg/dynamic-data-exchange-management-library.md)。 |
| **MSGF_DIALOGBOX** 0 | 輸入事件發生在訊息方塊或對話方塊中。 |
| **MSGF_MENU** 2 | 輸入事件發生在功能表中。 |
| **MSGF_SCROLLBAR** 5 | 輸入事件發生在捲軸中。 |

### <a name="wparam"></a>wParam

類型： **WPARAM**

不使用這個參數。

### <a name="lparam-in"></a>lParam [in]

類型： **LPARAM**

訊息 [結構的](/windows/win32/api/winuser/ns-winuser-msg) 指標。

## <a name="returns"></a>傳回

類型： **LRESULT**

如果程式 *代碼* 小於零，則攔截程式必須傳回 **CallNextHookEx** 傳回的值。

如果程式 *代碼* 大於或等於零，而且攔截程式未處理訊息，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_MSGFILTER](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。
如果攔截程式處理訊息，它可能會傳回非零值，以防止系統將訊息傳遞至其餘的攔截鏈或目標視窗程式。

## <a name="remarks"></a>備註

應用程式會在 **SetWindowsHookEx** 函式的呼叫中指定 **WH_MSGFILTER** 攔截類型和攔截程式指標，以安裝攔截程式。

如果使用 DDEML 和執行同步交易的應用程式必須在分派訊息之前處理訊息，則必須使用 **WH_MSGFILTER** 攔截。

## <a name="see-also"></a>另請參閱

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[味精](/windows/win32/api/winuser/ns-winuser-msg)

[勾點](hooks.md)
