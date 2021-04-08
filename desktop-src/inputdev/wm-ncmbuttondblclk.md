---
title: 'WM_NCMBUTTONDBLCLK 訊息 (Winuser .h) '
description: 當使用者按兩下滑鼠左鍵，而游標位於視窗的非工作區內時，即會張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。
ms.assetid: 7c0f8d6e-eb37-4873-a3f8-777e8b0b22bc
keywords:
- WM_NCMBUTTONDBLCLK 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCMBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612a0a7ca0a5731691ec244df505e3d058216e2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685799"
---
# <a name="wm_ncmbuttondblclk-message"></a>WM \_ NCMBUTTONDBLCLK 訊息

當使用者按兩下滑鼠左鍵，而游標位於視窗的非工作區內時，即會張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_NCMBUTTONDBLCLK              0x00A9
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式所傳回的點擊測試值，做為處理 [**WM \_ NCHITTEST**](wm-nchittest.md)訊息的結果。 如需點擊測試值的清單，請參閱 **WM \_ NCHITTEST**。

</dd> <dt>

*lParam* 
</dt> <dd>

[**點**](/previous-versions//dd162808(v=vs.85))結構，包含資料指標的 x 和 y 座標。 座標是相對於畫面的左上角。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

視窗不需要 **CS \_ DBLCLKS** 樣式即可接收 **WM \_ NCMBUTTONDBLCLK** 訊息。

當使用者按下、放開，然後在系統的按兩下時間限制內再次按下滑鼠按鍵時，系統會產生 **WM \_ NCMBUTTONDBLCLK** 訊息。 按兩下中間的滑鼠按鍵實際上會產生四個訊息： [**wm \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md)、 [**wm \_ NCMBUTTONUP**](wm-ncmbuttonup.md)、 **wm \_ NCMBUTTONDBLCLK** 和 **wm \_ NCMBUTTONUP** 。

您也可以使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 和 [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏，從 *LPARAM* 中解壓縮 X 和 Y 座標的值。


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> 請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。 具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。

 

如果適合這麼做，系統會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windowsx) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**取得 \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

[**WM \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md)
</dt> <dt>

[**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**概念**
</dt> <dt>

[滑鼠輸入](mouse-input.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**點**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

