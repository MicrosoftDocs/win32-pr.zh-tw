---
description: 以電腦為基礎的訓練 (CBT) 應用程式傳送，以將使用者輸入訊息與透過 WH JOURNALPLAYBACK 程式傳送的其他訊息分開 \_ 。
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: 'WM_QUEUESYNC 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977330"
---
# <a name="wm_queuesync-message"></a>WM \_ QUEUESYNC 訊息

以電腦為基礎的訓練 (CBT) 應用程式傳送，以將使用者輸入訊息與透過 [**WH \_ JOURNALPLAYBACK**](about-hooks.md) 程式傳送的其他訊息分開。


```C++
#define WM_QUEUESYNC                    0x0023
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

如果 CBT 應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

每當 CBT 應用程式使用 [**WH \_ JOURNALPLAYBACK**](about-hooks.md) 程式時，第一個和最後一則訊息為 **WM \_ QUEUESYNC**。 這可讓 CBT 應用程式攔截並檢查使用者起始的訊息，而不需要針對其所傳送的事件執行此動作。

如果應用程式指定 **Null** 視窗控制碼，則會將訊息張貼至使用中視窗的訊息佇列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**概念**
</dt> <dt>

[鉤](hooks.md)
</dt> </dl>

 

 
