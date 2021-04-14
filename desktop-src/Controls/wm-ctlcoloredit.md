---
title: 'WM_CTLCOLOREDIT 訊息 (Winuser .h) '
description: 不是唯讀或停用的編輯控制項，會在 \_ 即將繪製控制項時，將 WM CTLCOLOREDIT 訊息傳送至其父視窗。
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- WM_CTLCOLOREDIT message Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464237"
---
# <a name="wm_ctlcoloredit-message"></a>WM \_ CTLCOLOREDIT 訊息

不是唯讀或停用的編輯控制項，會在即將繪製控制項時，將 **WM \_ CTLCOLOREDIT** 訊息傳送至其父視窗。 藉由回應此訊息，父視窗可使用指定的裝置內容控制碼來設定編輯控制項的文字和背景色彩。


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

編輯控制項視窗的裝置內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

編輯控制項的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則必須傳回筆刷的控制碼。 系統會使用筆刷來繪製編輯控制項的背景。

## <a name="remarks"></a>備註

如果應用程式傳回所建立的筆刷 (例如，藉由使用 [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) 或 [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) 函數) ，應用程式必須釋放筆刷。 如果應用程式傳回的系統筆刷 (例如， [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) 或 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 函式所抓取的) ，則應用程式不需要釋放筆刷。

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取編輯控制項的預設系統色彩。

唯讀或停用的編輯控制項不會傳送 **wm \_ CTLCOLOREDIT** 訊息，而是會傳送 [**wm \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) 訊息。

線上程之間永遠不會傳送 **WM \_ CTLCOLOREDIT** 訊息，它只會在相同的執行緒中傳送。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。 如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。 \_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。

**Rich Edit：** 不支援此訊息。 若要設定 rich edit 控制項的背景色彩，請使用 [**EM \_ SETBKGNDCOLOR**](em-setbkgndcolor.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ SETBKGNDCOLOR**](em-setbkgndcolor.md)
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
</dt> </dl>

 

