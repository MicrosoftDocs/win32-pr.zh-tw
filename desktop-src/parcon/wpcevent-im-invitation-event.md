---
description: 提供的每個使用者事件，可供立即訊息用戶端用來記錄對話的起始。
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: 'WPCEVENT_IM_INVITATION (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978085"
---
# <a name="wpcevent_im_invitation-event"></a>WPCEVENT \_ IM \_ 邀請事件

提供的每個使用者事件，可供立即訊息用戶端用來記錄對話的起始。


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a>參數

<dl> <dt>

*AppName* 
</dt> <dd>

產生事件的應用程式名稱。

</dd> <dt>

*AppVersion* 
</dt> <dd>

產生事件之應用程式的版本字串。

</dd> <dt>

*AccountName* 
</dt> <dd>

立即訊息帳戶識別字串。

</dd> <dt>

*ConvID* 
</dt> <dd>

交談的識別碼。

</dd> <dt>

*RequestingIP* 
</dt> <dd>

字串，其中包含正在傳送邀請的電腦 IP 位址。

</dd> <dt>

*傳送者* 
</dt> <dd>

發出邀請之帳戶的立即訊息帳戶識別字串。

</dd> <dt>

*原因* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*RecipCount* 
</dt> <dd>

接收邀請的收件者計數，以及收件者欄位中定義的身分識別。

</dd> <dt>

*收件者* 
</dt> <dd>

包含邀請收件者之立即訊息帳戶識別字串的分隔字串。

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

 

 




