---
title: 'EN_LINK (Richedit 的通知碼) '
description: 當 \_ 使用者按下滑鼠時，或當滑鼠指標停留在具有 CFE 連結效果的文字上方時，豐富的編輯控制項就會傳送連結通知碼給您 \_ 。
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466533"
---
# <a name="en_link-notification-code"></a>EN \_ 連結通知碼

當 \_ 使用者按下滑鼠時，或當滑鼠指標停留在具有 **CFE \_ 連結** 效果的文字上方時，豐富的編輯控制項就會傳送連結通知碼給您。 無視窗的 rich edit 控制項會使用 [**ITextHost：： TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) 方法傳送這個通知。 控制項的父視窗會透過 [**WM \_ 通知**](wm-notify.md) 訊息接收此通知碼。


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

藉由呼叫 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 函式與 GWL 識別碼值來抓取的視窗識別碼 \_ 。

</dd> <dt>

*lParam* 
</dt> <dd>

[**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink)結構的指標。 結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構、通知程式碼的相關資訊，以及 [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) 結構，指出具有 **CFE \_ 連結** 效果的字元範圍。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以允許控制項繼續正常處理訊息。

傳回非零值，以防止控制項處理訊息。

**Windows 8**： [傳回連結] 會 **\_ \_ \_ 預設** 為指示 rich edit 控制項執行預設動作。

## <a name="remarks"></a>備註

若要在連結具有焦點時接收 e **\_ 連結** 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ 連結**](rich-edit-control-event-mask-flags.md)旗標。

如果連結沒有焦點，則若要接收 **En-us \_ 連結** 通知碼，請在以 [**EM \_ SETEDITSTYLE**](em-seteditstyle.md)訊息傳送的遮罩中指定 **SES \_ NOFOCUSLINKNOTIFY** 旗標。

當滑鼠指標停留在具有 **CFE \_ 連結** 效果的文字上方時，rich edit 控制項會傳送以 **\_ 連結** 通知碼傳送的訊息：

-   [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)
-   [**WM \_ RBUTTONDBLCLK**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)

**CFE \_ 連結** 效果通常會識別包含 URL 的文字範圍。 當應用程式在 \_ url 上方時變更滑鼠指標，或藉由啟動瀏覽器來查看 url 所識別的位置，應用程式可以處理 En-us 連結通知碼。

如果您傳送 [**EM \_ AUTOURLDETECT**](em-autourldetect.md) 訊息來啟用自動 URL 偵測，rich edit 控制項會自動為修改過的文字設定其識別為 url 的 **CFE \_ 連結** 效果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**EM \_ AUTOURLDETECT**](em-autourldetect.md)
</dt> <dt>

[**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2：： SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

