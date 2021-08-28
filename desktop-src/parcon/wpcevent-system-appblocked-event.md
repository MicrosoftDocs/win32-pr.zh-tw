---
description: 軟體限制原則所產生的系統層級事件 (SRP) 當應用程式被更安全的規則封鎖時。
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: 'WPCEVENT_SYSTEM_APPBLOCKED (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0444cee0a2844ae868923b5cf51923e0024c9de9a2a12ad51e20d8db9fa3b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112718"
---
# <a name="wpcevent_system_appblocked-event"></a>WPCEVENT \_ 系統 \_ APPBLOCKED 事件

軟體限制原則所產生的系統層級事件 (SRP) 當應用程式被更安全的規則封鎖時。


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>參數

<dl> <dt>

*時間 戳* 
</dt> <dd>

發生區塊的時間。

</dd> <dt>

*UserID* 
</dt> <dd>

嘗試啟動應用程式之使用者的安全識別碼。

</dd> <dt>

*路徑* 
</dt> <dd>

使用者嘗試啟動之應用程式的路徑。

</dd> <dt>

*RuleID* 
</dt> <dd>

在一組家長中，規則的識別碼會控制封鎖執行的更安全規則。

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

 

 




