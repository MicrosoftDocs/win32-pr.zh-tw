---
description: Web 內容篩選器因嘗試存取 URL 而產生的每個使用者事件。
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: 'WPCEVENT_WEB_URLVISIT (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9524909ee78d14395e2f208fe265b3abc31240d2036788b8b84c4fea05aac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112698"
---
# <a name="wpcevent_web_urlvisit-event"></a>WPCEVENT \_ WEB \_ URLVISIT 事件

Web 內容篩選器因嘗試存取 URL 而產生的每個使用者事件。


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_URLVISIT = {0x3, 0x0, 0x10, 0x4, 0x18, 0x3, 0x8000000000000010};
```



## <a name="parameters"></a>參數

<dl> <dt>

*URL* 
</dt> <dd>

嘗試開啟的 URL。

</dd> <dt>

*應用程式* 
</dt> <dd>

產生事件的應用程式。

</dd> <dt>

*版本* 
</dt> <dd>

應用程式的版本字串。

</dd> <dt>

*原因* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*RatingSystemID* 
</dt> <dd>

識別目前評等系統的 GUID。

</dd> <dt>

*CatCount* 
</dt> <dd>

[類別目錄] 欄位中封鎖的專案計數。

</dd> <dt>

*類別* 
</dt> <dd>

已封鎖之類別識別碼的分隔字串。

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

 

 




