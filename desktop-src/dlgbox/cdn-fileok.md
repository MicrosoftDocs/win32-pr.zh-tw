---
title: 'CDN_FILEOK (Commdlg 的通知碼) '
description: 當使用者指定檔案名，並按一下 [確定] 按鈕時，由 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊傳送。
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- CDN_FILEOK 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968986"
---
# <a name="cdn_fileok-notification-code"></a>CDN \_ FILEOK 通知碼

當使用者指定檔案名，並按一下 [**確定**] 按鈕時，由 Explorer 樣式的 [**開啟**] 或 [**另存** 新檔] 對話方塊傳送。

您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構的指標。

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構包含 [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員會指出 **CDN \_ FILEOK** 通知訊息。

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構也包含 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的指標，其 **lpstrFile** 成員會指定所選檔案名的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果攔截程式傳回零，對話方塊會接受指定的檔案名並關閉。

若要拒絕指定的檔案名，並強制對話方塊保持開啟，請從攔截程式傳回非零值，並呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函式來設定非零的 **DWL \_ MSGRESULT** 值。

## <a name="remarks"></a>備註

只有在使用 **OFN \_ EXPLORER** 值建立對話方塊時，系統才會傳送此通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ 通知**](../controls/wm-notify.md)
</dt> </dl>

 

