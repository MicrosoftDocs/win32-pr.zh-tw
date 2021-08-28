---
title: 'WM_NOTIFY 訊息 (Winuser .h) '
description: 當事件發生時，由通用控制項傳送至其父視窗，或控制項需要一些資訊。
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- WM_NOTIFY 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9139f2dab6410eeb2bacbde93b5e163c0591f350626046861426ddc53beab389
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539708"
---
# <a name="wm_notify-message"></a>WM \_ 通知訊息

當事件發生時，由通用控制項傳送至其父視窗，或控制項需要一些資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

傳送訊息之通用控制項的識別碼。 此識別碼不保證是唯一的。 應用程式應該使用 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的 **hwndFrom** 或 **idFrom** 成員 (作為 *lParam* 參數傳遞，) 來識別控制項。

</dd> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知碼和其他資訊。 針對某些通知訊息，這個參數會指向較大的結構，此結構的 **NMHDR** 結構是其第一個成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

除非另有指定的通知訊息，否則會忽略傳回值。

## <a name="remarks"></a>備註

訊息的目的地必須是控制項父系的 **HWND** 。 您可以使用 [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent)來取得此值，如下列範例所示，其中 *m \_ controlHwnd* 是控制項本身的 **HWND** 。


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



應用程式會在父視窗的視窗程式中處理訊息，如下列範例所示，這會處理上述範例中的自訂控制項所傳送的通知訊息。


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



某些通知會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送，CHIEFLY 已在 API 中的那些通知。 如需詳細資訊，請參閱 [控制訊息](control-messages.md)。

如果訊息處理常式是在對話方塊程式中，您必須使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 來設定傳回值。

針對 Windows Vista 和更新版本的系統，無法在進程間傳送 **WM \_ 通知** 訊息。

許多通知都有提供 ANSI 和 Unicode 格式。 傳送 **wm \_ 通知** 訊息的視窗會使用 [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) 訊息來判斷應該使用哪一種格式。 如需進一步討論，請參閱 **WM \_ NOTIFYFORMAT** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ NOTIFYFORMAT**](wm-notifyformat.md)
</dt> </dl>

 

