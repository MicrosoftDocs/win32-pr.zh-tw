---
title: 'CDN_INCLUDEITEM (Commdlg 的通知碼) '
description: 由 [開啟] 或 [另存新檔] 對話方塊傳送，以判斷對話方塊是否應在 shell 資料夾的專案清單中顯示專案。
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a91c61e4a7c2786e67ed28e2c62e5963762659c
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590775"
---
# <a name="cdn_includeitem-notification-code"></a>CDN \_ INCLUDEITEM 通知碼

\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。 我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]

由 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊傳送，以判斷對話方塊是否應在 shell 資料夾的專案清單中顯示專案。 當使用者開啟資料夾時，對話方塊會為資料夾中的每個專案傳送 **CDN \_ INCLUDEITEM** 通知。 只有在建立對話方塊時設定了 **OFN \_ ENABLEINCLUDENOTIFY** 旗標，對話方塊才會傳送此通知。

您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)結構的指標。

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員會指出 **CDN \_ INCLUDEITEM** 通知訊息。

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)結構的 **.psf** 成員是要列舉其專案之資料夾的介面指標。 **Pidl** 成員是專案識別碼清單的指標，該清單會識別相對於資料夾的專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式傳回零，對話方塊就會從專案清單中排除專案。

若要包含專案，請從攔截程式傳回非零值。

## <a name="remarks"></a>備註

無論 **CDN \_ INCLUDEITEM** 傳回的值為何，對話方塊一律會包含同時具有 **SFGAO \_ FILESYSTEM** 和 **SFGAO \_ FILESYSANCESTOR** 屬性的專案。

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

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

 

