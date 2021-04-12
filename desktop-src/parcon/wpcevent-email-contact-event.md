---
description: 電子郵件客戶程式所產生的每個使用者事件，會記錄在家長監護中新增、變更或刪除連絡人的時間。
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: 'WPCEVENT_EMAIL_CONTACT (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0974030e53756b44f2be2e8550707161f2d6d461
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194974"
---
# <a name="wpcevent_email_contact-event"></a>WPCEVENT \_ 電子郵件 \_ 連絡人活動

電子郵件客戶程式所產生的每個使用者事件，會記錄在家長監護中新增、變更或刪除連絡人的時間。


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_CONTACT = {0xe, 0x0, 0x10, 0x4, 0x16, 0xe, 0x8000000000000030};
```



## <a name="parameters"></a>參數

<dl> <dt>

*AppName* 
</dt> <dd>

產生事件的電子郵件應用程式名稱。

</dd> <dt>

*AppVersion* 
</dt> <dd>

產生事件的電子郵件應用程式的版本。

</dd> <dt>

*OldName* 
</dt> <dd>

先前的電子郵件帳戶名稱（如果已刪除或已變更）。

</dd> <dt>

*OldID* 
</dt> <dd>

與先前電子郵件帳戶名稱相關聯的識別碼。

</dd> <dt>

*NewName* 
</dt> <dd>

新的電子郵件帳戶名稱（如果已新增或變更）。

</dd> <dt>

*NewID* 
</dt> <dd>

與新電子郵件帳戶名稱相關聯的識別碼。

</dd> <dt>

*原因* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*EmailAccount* 
</dt> <dd>

此使用者的電子郵件帳戶名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 標頭<br/>                   | <dl> <dt>Wpcevent。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用適用于家長監護的記錄 Api](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC 的 \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




