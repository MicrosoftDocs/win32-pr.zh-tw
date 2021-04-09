---
description: 當視窗的大小或位置即將變更時，傳送至視窗。 應用程式可以使用此訊息來覆寫視窗的預設最大大小和位置，或其預設的最小或最大追蹤大小。
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: 'WM_GETMINMAXINFO 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850643"
---
# <a name="wm_getminmaxinfo-message"></a>WM \_ GETMINMAXINFO 訊息

當視窗的大小或位置即將變更時，傳送至視窗。 應用程式可以使用此訊息來覆寫視窗的預設最大大小和位置，或其預設的最小或最大追蹤大小。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo)結構的指標，其中包含預設最大化的位置和維度，以及預設的最小和最大追蹤大小。 應用程式可以藉由設定此結構的成員來覆寫預設值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

追蹤大小上限是可使用框線來調整視窗大小的最大視窗大小。 最小的追蹤大小是可使用框線來調整視窗大小的最小視窗大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
