---
title: 'WM_CTLCOLORBTN 訊息 (Winuser .h) '
description: 在 \_ 繪製按鈕之前，會將 WM CTLCOLORBTN 訊息傳送至按鈕的父視窗。 父視窗可以變更按鈕的文字和背景色彩。 不過，只有主控描繪的按鈕會回應父視窗處理此訊息。
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- WM_CTLCOLORBTN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5689d7c76499f1ed180f76831af325c5e311bf06e052ea1446805c39ddf8642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407637"
---
# <a name="wm_ctlcolorbtn-message"></a>WM \_ CTLCOLORBTN 訊息

在繪製按鈕之前，會將 **WM \_ CTLCOLORBTN** 訊息傳送至按鈕的父視窗。 父視窗可以變更按鈕的文字和背景色彩。 不過，只有主控描繪的按鈕會回應父視窗處理此訊息。


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定按鈕的顯示內容之控制碼的 **HDC** 。

</dd> <dt>

*lParam* 
</dt> <dd>

指定按鈕之控制碼的 **HWND** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則必須將控制碼傳回給筆刷。 系統會使用筆刷來繪製按鈕的背景。

## <a name="remarks"></a>備註

如果應用程式傳回所建立的筆刷 (例如，藉由使用 [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) 或 [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) 函數) ，應用程式必須釋放筆刷。 如果應用程式傳回的系統筆刷 (例如， [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) 或 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 函式所抓取的) ，則應用程式不需要釋放筆刷。

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取按鈕的預設系統色彩。 具有 [**BS \_**](button-styles.md)按鈕、 [**BS \_ DEFPUSHBUTTON**](button-styles.md)或 [**BS \_ PUSHLIKE**](button-styles.md) 樣式的按鈕不會使用傳回的筆刷。 具有這些樣式的按鈕一律會以預設的系統色彩繪製。 繪圖推播按鈕需要數種不同的筆刷-臉部、反白顯示和陰影，但是 **WM \_ CTLCOLORBTN** 訊息只允許傳回一個筆刷。 若要為推播按鈕提供自訂外觀，請使用主控描繪按鈕。 如需詳細資訊，請參閱 [建立 Owner-Drawn 控制項](user-controls-intro.md)。

線上程之間永遠不會傳送 **WM \_ CTLCOLORBTN** 訊息。 它只會在一個執行緒內傳送。

核取方塊或選項按鈕的文字色彩會套用至方塊或按鈕、其核取記號和文字。 這些按鈕的焦點矩形會維持系統預設色彩 (通常是黑色) 。 群組方塊的文字色彩會套用至文字，但不會套用至定義方塊的線條。 按下按鈕的文字色彩只適用于其焦點矩形;它不會影響文字的色彩。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。 如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。 \_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**其他資源**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

