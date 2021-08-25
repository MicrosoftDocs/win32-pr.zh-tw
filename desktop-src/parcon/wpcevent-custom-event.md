---
description: 支援最多三個欄位的每個使用者事件。
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: 'WPCEVENT_CUSTOM (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8082e03aa6dfea8cd2fd461feec093de71a1ada8051b8fb88295d0bbbf570b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951548"
---
# <a name="wpcevent_custom-event"></a>WPCEVENT \_ 自訂事件

支援最多三個欄位的每個使用者事件。

事件會顯示在 **活動檢視器** 中， **另** 一個區段具有下列階層：

1.  Publisher

2.  應用程式

3.  事件


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>參數

<dl> <dt>

*發行者* 
</dt> <dd>

事件的發行者 (例如) 的公司名稱。

</dd> <dt>

*AppName* 
</dt> <dd>

產生事件的應用程式名稱。

</dd> <dt>

*AppVersion* 
</dt> <dd>

產生事件之應用程式的版本。

</dd> <dt>

*事件* 
</dt> <dd>

事件的名稱。

</dd> <dt>

*Value1* 
</dt> <dd>

自訂欄位1。

</dd> <dt>

*Value2* 
</dt> <dd>

自訂欄位2。

</dd> <dt>

*Value3* 
</dt> <dd>

自訂欄位3。

</dd> <dt>

*封鎖* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*原因* 
</dt> <dd>

提供有關封鎖或不封鎖原因之額外資訊的自訂字串。

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

 

 




