---
title: 'WM_XBUTTONDOWN 訊息 (Winuser .h) '
description: 當使用者按下第一個或第二個 X 按鈕，而游標位於視窗的工作區時張貼。
ms.assetid: 4d972841-1513-4925-9d59-2557233561a2
keywords:
- WM_XBUTTONDOWN 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_XBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a53ed8c6cfd285927ad3a0be83ce219ece8a203e0e062995c2abb1725042f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716978"
---
# <a name="wm_xbuttondown-message"></a>WM \_ XBUTTONDOWN 訊息

當使用者按下第一個或第二個 X 按鈕，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_XBUTTONDOWN                  0x020B
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位單字指出是否有不同的虛擬機器碼已關閉。 它可以是下列一或多個值。



| 值                                                                                                                                                                                                               | 意義                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_控制項**</dt> <dt>0x0008</dt> </dl>    | CTRL 鍵已關閉。<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_LBUTTON**</dt> <dt>0x0001</dt> </dl>    | 左邊的滑鼠按鍵已關閉。<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_MBUTTON**</dt> <dt>0x0010</dt> </dl>    | 中間的滑鼠按鍵已關閉。<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_RBUTTON**</dt> <dt>0x0002</dt> </dl>    | 滑鼠右鍵已關閉。<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_SHIFT**</dt> <dt>0x0004</dt> </dl>          | SHIFT 鍵已關閉。<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_XBUTTON1**</dt> <dt>0x0020</dt> </dl> | 第一個 X 按鈕已關閉。<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_XBUTTON2**</dt> <dt>0x0040</dt> </dl> | 第二個 X 按鈕已關閉。<br/>     |



 

高序位單字表示按下的按鈕。 它可以是下列值之一。



| 值                                                                                                                                                                                                     | 意義                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | 按一下第一個 X 按鈕。<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | 按一下第二個 X 按鈕。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字組指定游標的 x 座標。 座標相對於工作區的左上角。

高序位字組指定游標的 y 座標。 座標相對於工作區的左上角。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE**。 如需處理傳回值的詳細資訊，請參閱「備註」一節。

## <a name="remarks"></a>備註

使用下列程式碼來取得 *wParam* 參數中的資訊：


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam);
```



使用下列程式碼來取得水準和垂直位置：


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。 如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。 您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。

> [!IMPORTANT]
> 請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。 具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。

 

不同于 [**wm \_ LBUTTONDOWN**](wm-lbuttondown.md)、 [**wm \_ MBUTTONDOWN**](wm-mbuttondown.md)和 [**wm \_ RBUTTONDOWN**](wm-rbuttondown.md) 訊息，應用程式應該會在處理時從這個訊息傳回 **TRUE** 。 這麼做可讓在早于 Windows 2000 的 Windows 系統上模擬此訊息的軟體，判斷視窗程式是否已處理訊息或呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)來處理訊息。

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

[**取得 \_ KEYSTATE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**取得 \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**取得 \_ XBUTTON \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)
</dt> <dt>

[**WM \_ XBUTTONUP**](wm-xbuttonup.md)
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

 

