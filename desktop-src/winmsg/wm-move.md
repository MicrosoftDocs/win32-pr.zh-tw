---
description: 移動視窗之後傳送。
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: 'WM_MOVE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84c18d7a4f4411f45a3338a057a60942d01905ccefd25b40ee511d3b8a5d915d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810468"
---
# <a name="wm_move-message"></a>WM \_ 移動訊息

移動視窗之後傳送。

視窗會透過其 [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 函數接收此訊息。


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

視窗工作區左上角的 x 和 y 座標。 低序位單字包含 x 座標，而高序位單字包含 y 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

這些參數是以螢幕座標提供，用於重迭和快顯視窗，以及子視窗的父系-工作區座標。

下列範例示範如何從 *lParam* 參數取得位置。


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



您也可以使用 [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) 宏將 *lParam* 參數轉換成 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會在處理 [**wm \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)訊息時，傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。
如果應用程式在不呼叫 **DefWindowProc** 的情況下處理 **wm \_ WINDOWPOSCHANGED** 訊息，則不會傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**點**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
