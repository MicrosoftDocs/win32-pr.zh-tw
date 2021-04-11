---
description: 當呼叫 SetWindowPos 函式或另一個視窗管理函式時，傳送至 Z 順序的大小、位置或位置的視窗已變更。
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: 'WM_WINDOWPOSCHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112841"
---
# <a name="wm_windowposchanged-message"></a>WM \_ WINDOWPOSCHANGED 訊息

當呼叫 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) 函式或另一個視窗管理函式時，傳送至 Z 順序的大小、位置或位置的視窗已變更。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)結構的指標，其中包含視窗新大小和位置的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會傳送 [**Wm \_ 大小**](wm-size.md) 和 [**WM \_ 將訊息移**](wm-move.md) 至視窗。 如果應用程式在不呼叫 **DefWindowProc** 的情況下處理 **wm \_ WINDOWPOSCHANGED** 訊息，則不會傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。 在不呼叫 **DefWindowProc** 的情況下，于 **WM \_ WINDOWPOSCHANGED** 訊息中執行任何移動或大小變更處理會更有效率。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**WM \_ 移動**](wm-move.md)
</dt> <dt>

[**WM \_ 大小**](wm-size.md)
</dt> <dt>

[**WM \_ WINDOWPOSCHANGING**](wm-windowposchanging.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
