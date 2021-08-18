---
description: 傳送至 Z 順序中大小、位置或位置的視窗，即將因呼叫 SetWindowPos 函式或其他視窗管理函式而變更。
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: 'WM_WINDOWPOSCHANGING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f10abcb0692374209c2070a465df7c4a5f18672eebf376378d6fb16cbca537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771938"
---
# <a name="wm_windowposchanging-message"></a>WM \_ WINDOWPOSCHANGING 訊息

傳送至 Z 順序中大小、位置或位置的視窗，即將因呼叫 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) 函式或其他視窗管理函式而變更。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_WINDOWPOSCHANGING            0x0046
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

若為具有 Ws 重 [**迭 \_**](window-styles.md) 或 **ws \_ THICKFRAME** 樣式的視窗， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將 [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) 訊息傳送至視窗。 這樣做的目的是要驗證視窗的新大小和位置，以及強制執行 [cs \_ BYTEALIGNCLIENT](about-window-classes.md) 和 cs \_ BYTEALIGNWINDOW 用戶端樣式。 藉由不將 **WM \_ WINDOWPOSCHANGING** 訊息傳遞給 **DefWindowProc** 函數，應用程式可以覆寫這些預設值。

在處理此訊息時，修改 [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) 中的任何值會影響視窗的新大小、位置或位置（以 Z 順序表示）。 應用程式可以藉由設定或清除 **WINDOWPOS****旗標** 成員中的適當位，來防止視窗的變更。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md)
</dt> <dt>

[**WM \_ 移動**](wm-move.md)
</dt> <dt>

[**WM \_ 大小**](wm-size.md)
</dt> <dt>

[**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
