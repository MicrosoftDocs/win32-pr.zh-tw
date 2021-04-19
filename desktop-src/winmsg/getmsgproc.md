---
UID: ''
title: GetMsgProc 回呼函式
description: 當訊息函式從應用程式訊息佇列取得訊息時，系統會呼叫此函數。
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "106966595"
---
# <a name="getmsgproc-function"></a>GetMsgProc 函式

## <a name="-description"></a>-description

搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。 每當 [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) 函式從應用程式訊息佇列抓取訊息時，系統就會呼叫這個函式。
將抓取的訊息傳回給呼叫者之前，系統會將訊息傳遞至攔截程式。

**HOOKPROC** 型別定義此回呼函數的指標。
**GetMsgProc** 是應用程式定義或程式庫定義函數名稱的預留位置。

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a>-參數

### <a name="code-in"></a>程式碼 [in]

類型： **int**

指定攔截程式是否必須處理訊息。
如果 **HC_ACTION** 程式 *代碼*，則攔截程式必須處理訊息。
如果程式 *代碼* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。

### <a name="wparam-in"></a>wParam [in]

類型： **WPARAM**

指定是否已從佇列中移除訊息。
此參數可以是下列其中一個值。

| 值 | 意義 |
|-------|---------|
| **PM_NOREMOVE** 0x0000 | 尚未從佇列中移除訊息。  (名為 **PeekMessage** 函式的應用程式，並指定 **PM_NOREMOVE** 旗標。 )  |
| **PM_REMOVE** 0x0001 | 已從佇列中移除訊息。  (名為 **GetMessage** 的應用程式，或指定 **PM_REMOVE** 旗標的應用程式，稱為 **PeekMessage** 函數。 ) |

### <a name="lparam-in"></a>lParam [in]

類型： **LPARAM**

訊息 [結構的](/windows/desktop/api/winuser/ns-winuser-msg) 指標，其中包含有關訊息的詳細資料。

## <a name="-returns"></a>-傳回

如果程式 *代碼* 小於零，則攔截程式必須傳回 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)傳回的值。

如果程式 *代碼* 大於或等於零，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_GETMESSAGE](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。
如果攔截程式未呼叫 **CallNextHookEx**，則傳回值應該為零。

## <a name="-remarks"></a>-備註

**GetMsgProc** 攔截程式可以檢查或修改訊息。
在攔截程式將控制權傳回給系統之後， **GetMessage** 或 **PeekMessage** 函式會將訊息連同任何修改傳回給原本呼叫它的應用程式。

應用程式會藉由在 **SetWindowsHookEx** 函式的呼叫中指定 **WH_GETMESSAGE** 攔截類型和攔截程式的指標，來安裝此攔截程式。

## <a name="see-also"></a>另請參閱

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[味精](/windows/desktop/api/winuser/ns-winuser-msg)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[鉤](hooks.md)
