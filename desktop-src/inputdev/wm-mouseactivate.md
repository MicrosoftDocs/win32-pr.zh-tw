---
title: 'WM_MOUSEACTI加值稅E 訊息 (Winuser .h) '
description: 當游標在非作用中視窗，且使用者按下滑鼠按鍵時傳送。 只有當子視窗將它傳遞給 DefWindowProc 函數時，父視窗才會接收此訊息。
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- WM_MOUSEACTI加值稅E 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094351"
---
# <a name="wm_mouseactivate-message"></a>WM \_ MOUSEACTI加值稅E 訊息

當游標在非作用中視窗，且使用者按下滑鼠按鍵時傳送。 只有當子視窗將它傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數時，父視窗才會接收此訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

正在啟動之視窗最上層父視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位單字會指定 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式所傳回的點擊測試值，作為處理 [**WM \_ NCHITTEST**](wm-nchittest.md) 訊息的結果。 如需點擊測試值的清單，請參閱 **WM \_ NCHITTEST**。

高序位單字指定當使用者按下滑鼠按鍵時所產生之滑鼠訊息的識別碼。 滑鼠訊息會被捨棄或張貼至視窗，視傳回值而定。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會指定是否應啟用視窗，以及是否應捨棄滑鼠訊息的識別碼。 它必須是下列值之一。



| 傳回碼/值                                                                                                                                          | Description                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**MA \_啟動**</dt> <dt>1</dt> </dl>         | 啟動視窗，不捨棄滑鼠訊息。<br/>         |
| <dl> <dt>**MA \_ACTI加值稅EANDEAT**</dt> <dt>2</dt> </dl>   | 啟用視窗，並捨棄滑鼠訊息。<br/>                 |
| <dl> <dt>**MA \_NOACTI加值稅E**</dt> <dt>3</dt> </dl>       | 不會啟動視窗，也不會捨棄滑鼠訊息。<br/> |
| <dl> <dt>**MA \_NOACTI加值稅EANDEAT**</dt> <dt>4</dt> </dl> | 不會啟動視窗，但會捨棄滑鼠訊息。<br/>         |



 

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會先將訊息傳遞給子視窗的父視窗，然後再進行任何處理。 父視窗會決定是否要啟動子視窗。 如果它啟用子視窗，父視窗應該會傳回 **ma \_ NOACTI加值稅E** 或 **ma \_ NOACTI加值稅EANDEAT** ，以防止系統進一步處理訊息。

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

**概念**
</dt> <dt>

[滑鼠輸入](mouse-input.md)
</dt> </dl>

 

