---
description: 當使用者取消應用程式的日誌活動時，張貼至應用程式。 訊息是以 Null 視窗控制碼張貼。
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: 'WM_CANCELJOURNAL 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8672f86393275c46383c6eb27c7eb1884178b86635ea93bf758de16521e6d2c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849334"
---
# <a name="wm_canceljournal-message"></a>WM \_ CANCELJOURNAL 訊息

當使用者取消應用程式的日誌活動時，張貼至應用程式。 訊息是以 **Null** 視窗控制碼張貼。


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **void**

此訊息不會傳回值。 它的目的是要在應用程式的主要迴圈或 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 攔截程式內進行處理，而不是從視窗程式來處理。

## <a name="remarks"></a>備註

日誌記錄和播放模式是在系統上強加的模式，可讓應用程式依序記錄或播放使用者輸入。 當應用程式安裝 [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) 或 [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) 攔截程式時，系統會進入這些模式。 當系統處於這兩種記錄模式時，應用程式必須從輸入佇列中輪流讀取輸入。 如果有任何一個應用程式在系統處於記錄模式時停止讀取輸入，則會強制其他應用程式等候。

為了確保健全的系統，其中一個應用程式無法使其無回應，系統會在使用者按下 CTRL + ESC 或 CTRL + ALT + DEL 時，自動取消任何日誌活動。 系統接著將任何日誌攔截程式解除掛接，並將具有 **Null** 視窗控制碼的 **WM \_ CANCELJOURNAL** 訊息張貼至設定日誌攔截的應用程式。

**WM \_ CANCELJOURNAL** 訊息具有 **Null** 視窗控制碼，因此無法分派至視窗程式。 有兩種方式可讓應用程式查看 **WM \_ CANCELJOURNAL** 訊息：如果應用程式是在它自己的主要迴圈中執行，它必須在呼叫 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) ，以及呼叫 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)時攔截訊息。 如果應用程式不是在它自己的主要迴圈中執行，它必須設定 [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) 攔截程式 (透過呼叫 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) ，指定監看訊息的 **WH \_ GETMESSAGE** 攔截型別) 。

當應用程式看到 **WM \_ CANCELJOURNAL** 訊息時，它可以採用兩個專案：使用者已刻意取消日誌記錄或播放模式，而系統已解除所有日誌記錄或播放攔截程式。

請注意，上面所述的按鍵組合 (CTRL + ESC 或 CTRL + ALT + DEL) 導致系統取消記錄。 如果有任何一個應用程式沒有回應，則會為使用者提供復原方法。 [**VK \_ 取消**](../inputdev/virtual-key-codes.md)虛擬機器碼 (通常會實作為 CTRL + BREAK 按鍵組合) 是 [筆記本記錄] 模式中的應用程式應該監看的應用程式是否為使用者希望取消日誌活動的信號。 不同之處在于， **VK \_ CANCEL** 的監看是記錄應用程式的建議行為，而 ctrl + ESC 或 ctrl + ALT + DEL 會導致系統取消記錄，而不考慮日誌應用程式的行為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))
</dt> <dt>

[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**概念**
</dt> <dt>

[勾點](hooks.md)
</dt> </dl>

 

 
