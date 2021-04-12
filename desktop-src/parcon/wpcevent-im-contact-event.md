---
description: 在家長監護中新增、變更或移除連絡人資訊時，由立即訊息用戶端產生的每個使用者事件。
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: 'WPCEVENT_IM_CONTACT (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9747f7ede57f7a1d77af0f0e8e5425401ee32b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194973"
---
# <a name="wpcevent_im_contact-event"></a>WPCEVENT \_ IM \_ 連絡人事件

在家長監護中新增、變更或移除連絡人資訊時，由立即訊息用戶端產生的每個使用者事件。


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_CONTACT = {0xf, 0x0, 0x10, 0x4, 0x16, 0xf, 0x8000000000000030};
```



## <a name="parameters"></a>參數

<dl> <dt>

*AppName* 
</dt> <dd>

產生事件的立即訊息應用程式名稱。

</dd> <dt>

*AppVersion* 
</dt> <dd>

產生事件之應用程式的版本。

</dd> <dt>

*AccountName* 
</dt> <dd>

此使用者的立即訊息帳戶名稱。

</dd> <dt>

*OldName* 
</dt> <dd>

先前的立即訊息帳戶名稱（如果已刪除或已變更）。

</dd> <dt>

*OldID* 
</dt> <dd>

與先前的立即訊息帳戶名稱相關聯的識別碼。

</dd> <dt>

*NewName* 
</dt> <dd>

新的立即訊息帳戶名稱（如果已新增或變更）。

</dd> <dt>

*NewID* 
</dt> <dd>

與新的立即訊息帳戶名稱相關聯的識別碼。

</dd> <dt>

*原因* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

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

 

 




