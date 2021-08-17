---
title: 'CDN_INITDONE (Commdlg 的通知碼) '
description: 當系統完成對話方塊中的控制項排列時，由 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊傳送。 系統會移動標準控制項，以騰出空間給子對話方塊的控制項。
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- CDN_INITDONE 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_INITDONE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032cf03b6205f2184986d28ca115060b3bf7a99991ef6256f3b87f995c33341d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721049"
---
# <a name="cdn_initdone-notification-code"></a>CDN \_INITDONE 通知碼

\[從 Windows Vista 開始，[[一般專案] 對話方塊](../shell/common-file-dialog.md)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。 我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]

當系統完成對話方塊中的控制項排列時，由 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊傳送。 系統會移動標準控制項，以騰出空間給子對話方塊的控制項。

您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構的指標。 **OFNOTIFY** 結構包含 [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員指出 **CDN 的 \_ INITDONE** 通知訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

只有在使用 **OFN \_ EXPLORER** 值建立對話方塊時，系統才會傳送此通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含 Windows .h) </dt> </dl> |



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

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

