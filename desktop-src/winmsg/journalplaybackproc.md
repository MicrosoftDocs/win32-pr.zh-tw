---
UID: ''
title: JournalPlaybackProc 回呼函式
description: 播放一系列先前錄製的滑鼠和鍵盤訊息。
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
ms.openlocfilehash: bee538bf2c20cc3cadb6f0bdf6f5dd6a2ae12dfe8a21baeb56b8ad62cb23ff3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437125"
---
# <a name="journalplaybackproc-function"></a>JournalPlaybackProc 函式

## <a name="description"></a>描述

搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。
一般而言，應用程式會使用此函式來播放一系列 **JournalRecordProc** 攔截程式先前錄製的滑鼠和鍵盤訊息。
只要安裝了 **JournalPlaybackProc** 勾點程式，就會停用一般的滑鼠和鍵盤輸入。

**HOOKPROC** 型別定義此回呼函數的指標。
**JournalPlaybackProc** 是應用程式定義或程式庫定義函數名稱的預留位置。

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
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
| **HC_GETNEXT** 1 | 攔截程式必須將目前的滑鼠或鍵盤訊息複製到 *lParam* 參數所指向的 [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)結構。 |
| **HC_NOREMOVE** 3 | 應用程式已呼叫 [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) 函式，並將 wRemoveMsg 設定為 **PM_NOREMOVE**，表示不會在 **PeekMessage** 處理之後從訊息佇列中移除訊息。 |
| **HC_NOREMOVE** 2 | 攔截程式必須做好準備，才能將下一個滑鼠或鍵盤訊息複製到 *lParam* 所指向的 **EVENTMSG** 結構。 收到 **HC_GETNEXT** 程式碼時，攔截程式必須將訊息複製到結構中。 |
| **HC_SYSMODALOFF** 5 | 系統強制回應對話方塊已損毀。 攔截程式必須繼續播放訊息。 |
| **HC_SYSMODALON** 4 | 系統強制回應對話方塊隨即顯示。 在對話方塊損毀之前，攔截程式必須停止播放訊息。 |

### <a name="wparam"></a>wParam

類型： **WPARAM**

不使用這個參數。

### <a name="lparam"></a>lParam

類型： **LPARAM**

**EVENTMSG** 結構的指標，代表由攔截程式處理的訊息。
只有在 **HC_GETNEXT** 程式 *代碼* 參數時，此參數才有效。

## <a name="returns"></a>傳回

類型： **LRESULT**

若要讓系統在處理訊息之前先等待，傳回值必須是系統應等候的時間量（以時鐘為單位）。

 (可以計算目前和先前輸入訊息中的時間成員之間的差異來計算這個值。 ) 

若要立即處理訊息，傳回值應為零。 只有當攔截程式碼 **HC_GETNEXT** 時，才會使用傳回值;否則會予以忽略。

## <a name="remarks"></a>備註

**JournalPlaybackProc** 攔截程式應將輸入訊息複製到 *lParam* 參數。
訊息必須先前使用 **JournalRecordProc** 攔截程式記錄，而不應該修改訊息。

若要一次或一次取出相同的訊息，您可以呼叫攔截程式，將程式 *代碼* 參數設定為 **HC_GETNEXT** ，而不需要將程式 *代碼* 設為 **HC_SKIP** 的中間呼叫。

如果程式 *代碼* 是 **HC_GETNEXT** ，且傳回值大於零，則系統會睡眠傳回值所指定的毫秒數。 當系統繼續時，它會再呼叫一次攔截程式，將程式 *代碼* 設為 **HC_GETNEXT** ，以取得相同的訊息。
這個新呼叫 **JournalPlaybackProc** 的傳回值應為零。否則，系統會返回 [睡眠]，以取得傳回值所指定的毫秒數、再次呼叫 **JournalPlaybackProc** 等等。
系統會顯示為沒有回應。

與大部分其他全域攔截程式不同的是， **JournalRecordProc** 和 **JournalPlaybackProc** 攔截程式永遠會在設定攔截的執行緒內容中呼叫。

當攔截程式將控制權傳回到系統之後，就會繼續處理訊息。 如果 **HC_SKIP** 程式 *代碼*，攔截程式必須做好準備，以便在下一次呼叫時傳回下一個記錄的事件訊息。

在 **SetWindowsHookEx** 函式的呼叫中指定 [WH_JOURNALPLAYBACK](about-hooks.md)類型和攔截程式指標，以安裝 **JournalPlaybackProc** 攔截程式。

如果使用者在日誌播放期間按下 CTRL + ESC 或 CTRL + ALT + DEL，系統會停止播放、解除與日誌播放程式的掛鉤，然後將 [WM_CANCELJOURNAL](wm-canceljournal.md) 訊息張貼至日誌應用程式。

如果攔截程式傳回 **WM_KEYLAST** 範圍 **WM_KEYFIRST** 中的訊息，則適用下列條件：

* **EVENTMSG** 結構的 **paramL** 成員會指定已按下之索引鍵的虛擬按鍵碼。
* **EVENTMSG** 結構的 **paramH** 成員會指定掃描程式碼。
* 沒有任何方法可以指定重複計數。
事件一律會用來代表一個關鍵事件。

## <a name="see-also"></a>另請參閱

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalRecordProc](journalrecordproc.md)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[勾點](hooks.md)
