---
title: 'WM_CTLCOLORSTATIC 訊息 (Winuser .h) '
description: 靜態控制項，或是唯讀或停用的編輯控制項， \_ 會在即將繪製控制項時，將 WM CTLCOLORSTATIC 訊息傳送至其父視窗。
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- WM_CTLCOLORSTATIC 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2df23b86539d07c9e1551d64f59e60e54df24ae2d48b316996542fb80c92ae8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539928"
---
# <a name="wm_ctlcolorstatic-message"></a>WM \_ CTLCOLORSTATIC 訊息

靜態控制項，或是唯讀或停用的編輯控制項，會在即將繪製控制項時，將 **WM \_ CTLCOLORSTATIC** 訊息傳送至其父視窗。 藉由回應此訊息，父視窗可使用指定的裝置內容控制碼來設定靜態控制項的文字前景和背景色彩。

視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

靜態控制項視窗的裝置內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

靜態控制項的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則傳回值會是系統用來繪製靜態控制項背景之筆刷的控制碼。

## <a name="remarks"></a>備註

如果應用程式傳回所建立的筆刷 (例如，藉由使用 [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) 或 [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) 函數) ，應用程式必須釋放筆刷。 如果應用程式傳回的系統筆刷 (例如， [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) 或 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 函式所抓取的) ，則應用程式不需要釋放筆刷。

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取靜態控制項的預設系統色彩。

您可以設定已停用編輯控制項的文字背景色彩，但無法設定文字前景色彩。 系統一律會使用色彩 \_ GRAYTEXT。

編輯非唯讀或停用的控制項不會傳送 **wm \_ CTLCOLORSTATIC** 訊息，而是會傳送 [**wm \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) 訊息。

線上程之間永遠不會傳送 **WM \_ CTLCOLORSTATIC** 訊息; 它只會在同一個執行緒內傳送。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。 如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。 \_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。

## <a name="examples"></a>範例

下列 c + + 範例顯示如何設定靜態控制項的文字前景和背景色彩，以回應 **WM \_ CTLCOLORSTATIC** 訊息。 `hbrBkgnd`變數是靜態 **HBRUSH** 變數，它會初始化為 Null，並在對 **WM \_ CTLCOLORSTATIC** 的呼叫之間儲存背景筆刷。 當不再需要時，您必須呼叫 [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) 函式來終結筆刷，通常是在相關聯的對話方塊終結時。


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



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

[**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md)
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

 

