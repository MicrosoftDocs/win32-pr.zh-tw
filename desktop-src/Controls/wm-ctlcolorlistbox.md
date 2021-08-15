---
title: 'WM_CTLCOLORLISTBOX 訊息 (Winuser .h) '
description: 在系統繪製清單方塊之前，傳送至清單方塊的父視窗。 藉由回應此訊息，父視窗可以使用指定的顯示裝置內容控制碼，來設定清單方塊的文字和背景色彩。
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1713c7251dfe837d5796b708fa5b77f0aa5e372c031c251199cb871dbd7c5608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077662"
---
# <a name="wm_ctlcolorlistbox-message"></a>WM \_ CTLCOLORLISTBOX 訊息

在系統繪製清單方塊之前，傳送至清單方塊的父視窗。 藉由回應此訊息，父視窗可以使用指定的顯示裝置內容控制碼，來設定清單方塊的文字和背景色彩。


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單方塊的裝置內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

清單方塊的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則必須將控制碼傳回給筆刷。 系統會使用筆刷來繪製清單方塊的背景。

## <a name="remarks"></a>備註

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取清單方塊的預設系統色彩。

線上程之間永遠不會傳送 **WM \_ CTLCOLORLISTBOX** 訊息。 它只會在一個執行緒內傳送。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。 如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 **DWL \_ MSGRESULT** 值會被忽略。

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
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

