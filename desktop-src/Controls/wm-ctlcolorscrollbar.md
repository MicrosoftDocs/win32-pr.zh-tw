---
title: 'WM_CTLCOLORSCROLLBAR 訊息 (Winuser .h) '
description: '\_當控制項即將繪製時，會將 WM CTLCOLORSCROLLBAR 訊息傳送到捲軸控制項的父視窗。'
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35dba3394c3d8fd99fef88d6fa1869ea1129d95ae8a82cc33f2935e5688871a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018556"
---
# <a name="wm_ctlcolorscrollbar-message"></a>WM \_ CTLCOLORSCROLLBAR 訊息

當控制項即將繪製時，會將 **WM \_ CTLCOLORSCROLLBAR** 訊息傳送到捲軸控制項的父視窗。 藉由回應此訊息，父視窗可以使用顯示內容控制碼來設定捲軸控制項的背景色彩。

視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

捲軸控制項的裝置內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

捲軸的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則必須將控制碼傳回給筆刷。 系統會使用筆刷來繪製捲軸控制項的背景。

## <a name="remarks"></a>備註

如果應用程式傳回所建立的筆刷 (例如，藉由使用 [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) 或 [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) 函數) ，應用程式必須釋放筆刷。 如果應用程式傳回的系統筆刷 (例如， [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) 或 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 函式所抓取的) ，則應用程式不需要釋放筆刷。

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取捲軸控制項的預設系統色彩。

線上程之間永遠不會傳送 **WM \_ CTLCOLORSCROLLBAR** 訊息，它只會在相同的執行緒內傳送。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。 如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。 \_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。

只有子捲軸控制項才會使用 **WM \_ CTLCOLORSCROLLBAR** 訊息。 附加至視窗 (WS \_ SCROLL 和 WS \_ VSCROLL) 不會產生此訊息的捲軸。 若要自訂附加至視窗之捲軸的外觀，請使用一般捲軸函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md)
</dt> <dt>

[**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md)
</dt> <dt>

[**WM \_ CTLCOLORLISTBOX**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**WM \_ CTLCOLORDLG**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

