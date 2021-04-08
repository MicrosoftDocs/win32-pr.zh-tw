---
title: 'WM_CTLCOLORDLG 訊息 (Winuser .h) '
description: 在系統繪製對話方塊之前，傳送至對話方塊。 藉由回應此訊息，對話方塊可以使用指定的顯示裝置內容控制碼來設定其文字和背景色彩。
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- WM_CTLCOLORDLG 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685571"
---
# <a name="wm_ctlcolordlg-message"></a>WM \_ CTLCOLORDLG 訊息

在系統繪製對話方塊之前，傳送至對話方塊。 藉由回應此訊息，對話方塊可以使用指定的顯示裝置內容控制碼來設定其文字和背景色彩。


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

對話方塊的裝置內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

對話方塊的控制代碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則必須將控制碼傳回給筆刷。 系統會使用筆刷來繪製對話方塊的背景。

## <a name="remarks"></a>備註

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取對話方塊的預設系統色彩。

系統不會自動損毀傳回的筆刷。 當不再需要時，應用程式會負責終結筆刷。

線上程之間永遠不會傳送 **WM \_ CTLCOLORDLG** 訊息。 它只會在一個執行緒內傳送。

請注意，會將 **WM \_ CTLCOLORDLG** 訊息傳送至對話方塊本身; 所有其他 **WM \_ CTLCOLOR \** _ 訊息都會傳送給控制項的擁有者。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換為 _ *INT \_ PTR** 並直接傳回值。 如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 **DWL \_ MSGRESULT** 值會被忽略。

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

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**概念**
</dt> <dt>

[對話方塊](dialog-boxes.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

