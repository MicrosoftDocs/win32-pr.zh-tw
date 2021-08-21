---
UID: ''
title: JournalRecordProc 回呼函式
description: 此函數會記錄系統從系統訊息佇列中移除的訊息。
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
ms.openlocfilehash: cc5e1bdbd99b234b347d0b9c10caa7125aead9b68138472e125c8e2a11180609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437115"
---
# <a name="journalrecordproc-function"></a>JournalRecordProc 函式

## <a name="description"></a>Description

搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。
此函數會記錄系統從系統訊息佇列中移除的訊息。
之後，應用程式可以使用 [JournalPlaybackProc](journalplaybackproc.md) 勾點來播放訊息。

**HOOKPROC** 型別定義此回呼函數的指標。
**JournalRecordProc** 是應用程式定義或程式庫定義函數名稱的預留位置。

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>參數

### <a name="code-in"></a>程式碼 [in]

類型： **int**

指定如何處理訊息。
如果程式 *代碼* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。
此參數可以是下列其中一個值。

| 值 | 意義 |
|-------|---------|
| **HC_ACTION** 0 | *LParam* 參數是 [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)結構的指標，其中包含從系統佇列移除之訊息的相關資訊。 攔截程式必須將結構的內容複寫到緩衝區或檔案來記錄。 |
| **HC_SYSMODALOFF** 5 | 系統強制回應對話方塊已損毀。 攔截程式必須繼續錄製。 |
| **HC_SYSMODALON** 4 | 系統強制回應對話方塊隨即顯示。 在對話方塊損毀之前，攔截程式必須停止錄製。 |

### <a name="wparam"></a>wParam

類型： **WPARAM**

不使用這個參數。

### <a name="lparam-in"></a>lParam [in]

類型： **LPARAM**

**EVENTMSG** 結構的指標，其中包含要記錄的訊息。

## <a name="returns"></a>傳回

類型： **LRESULT**

傳回值會被忽略。

## <a name="remarks"></a>備註

**JournalRecordProc** 勾點程式必須複製但不能修改訊息。
當攔截程式將控制權傳回到系統之後，就會繼續處理訊息。

在 **SetWindowsHookEx** 函式的呼叫中指定 [WH_JOURNALRECORD](about-hooks.md)類型和攔截程式指標，以安裝 **JournalRecordProc** 攔截程式。

**JournalRecordProc** 攔截程式不需要存留在動態連結程式庫中。
**JournalRecordProc** 勾點程式可以存留在應用程式本身。

與大部分其他全域攔截程式不同的是， **JournalRecordProc** 和 [JournalPlaybackProc](journalplaybackproc.md) 攔截程式永遠會在設定攔截的執行緒內容中呼叫。

已安裝 **JournalRecordProc** 攔截程式的應用程式應該會監看 [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) 的虛擬機器碼 (，其實作為大部分鍵盤) 的 CTRL + BREAK 按鍵組合。
應用程式應該將此虛擬金鑰程式碼解釋為使用者想要停止記錄的信號。
應用程式應該藉由結束錄製順序和移除 **JournalRecordProc** 攔截程式來回應。
移除是很重要的。
它會防止日誌應用程式在攔截程式內停滯，而無法鎖定系統。

此角色是停止 journl 錄製的信號，表示 CTRL + BREAK 按鍵組合本身無法錄製。
由於 CTRL + C 按鍵組合沒有這類角色做為日誌通知，因此可以記錄。
另外還有兩個無法錄製的按鍵組合： CTRL + ESC 和 CTRL + ALT + DEL。
這兩個按鍵組合會導致系統停止所有的記錄活動， (記錄或播放) 、移除所有日誌勾點，並將 [WM_CANCELJOURNAL](wm-canceljournal.md) 訊息張貼至日誌應用程式。

## <a name="see-also"></a>另請參閱

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalPlaybackProc](journalplaybackproc.md)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[勾點](hooks.md)
