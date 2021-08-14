---
description: 設定在繪製文字時，控制項所使用的字型。
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: 'WM_SETFONT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811bee30237a64955197588f87866d4a64af89edc640762ec16333839aee9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199934"
---
# <a name="wm_setfont-message"></a>WM \_ SETFONT 訊息

設定在繪製文字時，控制項所使用的字型。


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

字型 (**HFONT**) 的控制碼。 如果這個參數是 **Null**，則控制項會使用預設系統字型來繪製文字。

</dd> <dt>

*lParam* 
</dt> <dd>

*LParam* 的低序位字指定是否應在設定字型時立即重新繪製控制項。 如果此參數為 **TRUE**，控制項會自行重新繪製。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

此訊息不會傳回值。

## <a name="remarks"></a>備註

**WM \_ SETFONT** 訊息會套用至所有控制項，而不只是對話方塊中的控制項。

對話方塊控制項擁有者設定控制項字型的最佳時間，是在收到 [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) 訊息時。 應用程式應該呼叫 [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) 函式來刪除不再需要的字型;例如，在終結控制項之後。

由於接收此訊息的結果，控制項的大小不會變更。 為了避免無法容納控制項界限內的文字，應用程式應該在設定字型之前更正控制項視窗的大小。

當對話方塊使用 [DS \_ SETFONT](../dlgbox/about-dialog-boxes.md) 樣式來設定其控制項中的文字時，系統會先將 **WM \_ SETFONT** 訊息傳送至對話方塊程式，然後再建立控制項。 應用程式可以藉 \_ 由呼叫下列任何功能，來建立包含 DS SETFONT 樣式的對話方塊：

-   [**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATE**](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[**MAKELPARAM**](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**WM \_ GETFONT**](wm-getfont.md)
</dt> <dt>

[**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
