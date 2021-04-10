---
description: 當在家長監護中使用定義的功能時，立即訊息用戶端所產生的每個使用者事件。
ms.assetid: 45e80314-90b1-4fcf-9c8f-c9840ae1775b
title: 'WPCEVENT_IM_FEATURE (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee28f004560ed287bc3cb94cbee1bda876355834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944124"
---
# <a name="wpcevent_im_feature-event"></a>WPCEVENT \_ IM \_ 功能事件

當在家長監護中使用定義的功能時，立即訊息用戶端所產生的每個使用者事件。


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_FEATURE = {0xb, 0x0, 0x10, 0x4, 0x16, 0xb, 0x8000000000000030};
```



## <a name="parameters"></a>參數

<dl> <dt>

*AppName* 
</dt> <dd>

立即訊息應用程式的名稱。

</dd> <dt>

*AppVersion* 
</dt> <dd>

應用程式的版本字串。

</dd> <dt>

*AccountName* 
</dt> <dd>

此使用者的立即訊息帳戶名稱。

</dd> <dt>

*ConvID* 
</dt> <dd>

此交談的識別碼。

</dd> <dt>

*MediaType* 
</dt> <dd>

[**WPCFLAG \_ IM \_ 功能**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_feature)列舉的值，指出在立即訊息互動期間存取之功能的相關資訊。

</dd> <dt>

*原因* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*RecipCount* 
</dt> <dd>

接收功能的立即訊息使用者計數，以及在 [收件者] 欄位中定義的身分識別。

</dd> <dt>

*收件者* 
</dt> <dd>

分隔的字串，其中包含所有接收功能之使用者的立即訊息帳戶身分識別。

</dd> <dt>

*傳送者* 
</dt> <dd>

為其來源的使用者提供立即訊息帳戶名稱。

</dd> <dt>

*SenderIP* 
</dt> <dd>

寄件者的電腦 IP 位址。

</dd> <dt>

*資料* 
</dt> <dd>

功能中資料的描述。

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

 

 




