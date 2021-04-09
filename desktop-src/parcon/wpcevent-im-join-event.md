---
description: 當實體嘗試加入家長監護中進行中的對話時，立即訊息應用程式所產生的每個使用者事件。
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: 'WPCEVENT_IM_JOIN (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b020eb3d4204f946002f59f472e5c95b715f88f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849116"
---
# <a name="wpcevent_im_join-event"></a>WPCEVENT \_ IM \_ 聯結事件

當實體嘗試加入家長監護中進行中的對話時，立即訊息應用程式所產生的每個使用者事件。


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
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

此使用者的立即訊息帳戶識別字串。

</dd> <dt>

*ConvID* 
</dt> <dd>

此交談的識別碼。

</dd> <dt>

*JoiningIP* 
</dt> <dd>

字串，包含要加入此交談的電腦 IP 位址。

</dd> <dt>

*JoiningUser* 
</dt> <dd>

要加入之使用者的立即訊息帳戶識別字串。

</dd> <dt>

*原因* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*MemberCount* 
</dt> <dd>

交談中的參與者計數，以及成員欄位中所定義的身分識別。

</dd> <dt>

*成員* 
</dt> <dd>

分隔的字串，包含此交談中所有目前成員的立即訊息帳戶識別字串。

</dd> <dt>

*傳送者* 
</dt> <dd>

發出要求加入交談之使用者的立即訊息帳戶識別字串。

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

 

 




