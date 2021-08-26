---
description: 在家長監護中嘗試接收訊息時，電子郵件客戶程式所產生的每個使用者事件。
ms.assetid: 3b8d9bac-16b0-49e9-b360-b2d6e82f1753
title: 'WPCEVENT_EMAIL_RECEIVED (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81a51e79125403504aae2ed6e823c10044ffc35ed36ff139e8333f955338d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951558"
---
# <a name="wpcevent_email_received-event"></a>WPCEVENT \_ 電子郵件 \_ 收到事件

在家長監護中嘗試接收訊息時，電子郵件客戶程式所產生的每個使用者事件。


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_RECEIVED = {0x4, 0x0, 0x10, 0x4, 0x16, 0x4, 0x8000000000000030};
```



## <a name="parameters"></a>參數

<dl> <dt>

*傳送者* 
</dt> <dd>

傳送實體的電子郵件帳戶名稱。

</dd> <dt>

*AppName* 
</dt> <dd>

產生事件的電子郵件應用程式名稱。

</dd> <dt>

*AppVersion* 
</dt> <dd>

產生事件的電子郵件應用程式的版本。

</dd> <dt>

*主體* 
</dt> <dd>

所接收訊息的主旨行。

</dd> <dt>

*原因* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*RecipCount* 
</dt> <dd>

接收訊息的電子郵件地址，以及在 [收件者] 欄位中定義身分識別的電子郵件數目。

</dd> <dt>

*收件者* 
</dt> <dd>

分隔的字串，其中包含訊息之所有收件者的電子郵件帳戶名稱。

</dd> <dt>

*AttachCount* 
</dt> <dd>

訊息的附件計數。

</dd> <dt>

*AttachmentName* 
</dt> <dd>

分隔的字串，其中包含訊息之所有附件的名稱。

</dd> <dt>

*ReceivedTime* 
</dt> <dd>

嘗試接收訊息的時間。

</dd> <dt>

*EmailAccount* 
</dt> <dd>

此使用者的電子郵件帳戶名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 標頭<br/>                   | <dl> <dt>Wpcevent。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用適用于家長監護的記錄 Api](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC 的 \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




