---
title: 'WM_NCXBUTTONUP 訊息 (Winuser .h) '
description: 當使用者放開第一個或第二個 X 按鈕，而游標位於視窗的非工作區時張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。
ms.assetid: 07ab5d4e-9912-4867-9146-8abc5addc15d
keywords:
- WM_NCXBUTTONUP 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCXBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eab2067d3d16c3ae0864ba7ddf04b5666efa0186d0a7d55ebd5eddaa7533790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829898"
---
# <a name="wm_ncxbuttonup-message"></a>WM \_ NCXBUTTONUP 訊息

當使用者放開第一個或第二個 X 按鈕，而游標位於視窗的非工作區時張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則 *不* 會張貼此訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_NCXBUTTONUP                  0x00AC
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位字組指定 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式所傳回的點擊測試值，使其無法處理 [**WM \_ NCHITTEST**](wm-nchittest.md) 訊息。 如需點擊測試值的清單，請參閱 **WM \_ NCHITTEST**。

高序位單字表示已發行的按鈕。 它可以是下列值之一。



| 值                                                                                                                                                                                                     | 意義                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | 第一個 X 按鈕已釋放。<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | 第二個 X 按鈕已釋放。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**點**](/previous-versions//dd162808(v=vs.85))結構的指標，其中包含資料指標的 x 和 y 座標。 座標是相對於畫面的左上角。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE**。 如需處理傳回值的詳細資訊，請參閱「備註」一節。

## <a name="remarks"></a>備註

使用下列程式碼取得 *wParam* 參數中的資訊。


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



您也可以使用下列程式碼，從 *lParam* 取得 x 和 y 座標：


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> 請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。 具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。

 

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會測試指定的點以取得資料指標的位置，並執行適當的動作。 如果有的話，它會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至視窗。

不同于 [**wm \_ NCLBUTTONUP**](wm-nclbuttonup.md)、 [**wm \_ NCMBUTTONUP**](wm-ncmbuttonup.md)和 [**wm \_ NCRBUTTONUP**](wm-ncrbuttonup.md) 訊息，應用程式應該會在處理時從這個訊息傳回 **TRUE** 。 這樣做會允許在早于 Windows 2000 的 Windows 系統上模擬此訊息的軟體，以判斷視窗程式是否已處理訊息或呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)來處理訊息。

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

[**WM \_ NCXBUTTONDBLCLK**](wm-ncxbuttondblclk.md)
</dt> <dt>

[**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
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

 

