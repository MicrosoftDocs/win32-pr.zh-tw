---
description: 父控制項設定變更時產生的系統層級事件。
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: 'WPCEVENT_SYS_SETTINGCHANGE (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978375"
---
# <a name="wpcevent_sys_settingchange-event"></a>WPCEVENT \_ SYS \_ SETTINGCHANGE 事件

父控制項設定變更時產生的系統層級事件。


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a>參數

<dl> <dt>

*類別* 
</dt> <dd>

產生事件的類別。

</dd> <dt>

*設定* 
</dt> <dd>

**WPC \_ 設定** 列舉的值。

</dd> <dt>

*擁有者* 
</dt> <dd>

正在產生事件之使用者的安全識別碼。

</dd> <dt>

*OldVal* 
</dt> <dd>

此設定的先前值（如果已刪除或已變更）。

</dd> <dt>

*NewVal* 
</dt> <dd>

此設定的新值（如果已加入或已變更）。

</dd> <dt>

*原因* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*選擇性* 
</dt> <dd>

選擇性欄位。

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

 

 




