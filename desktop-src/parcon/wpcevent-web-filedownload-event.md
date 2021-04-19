---
description: 嘗試從 web 下載檔案時所產生的每個使用者事件。 此事件是由家長監護提示的應用程式所產生。
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: 'WPCEVENT_WEB_FILEDOWNLOAD (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66bb04a53589a1cae41e2ba7d7a9c00835452e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997963"
---
# <a name="wpcevent_web_filedownload-event"></a>WPCEVENT \_ WEB \_ FILEDOWNLOAD 事件

嘗試從 web 下載檔案時所產生的每個使用者事件。 此事件是由家長監護提示的應用程式所產生。


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_FILEDOWNLOAD = {0xa, 0x0, 0x10, 0x4, 0x18, 0xa, 0x8000000000000030};
```



## <a name="parameters"></a>參數

<dl> <dt>

*URL* 
</dt> <dd>

嘗試下載的 URL 來源。

</dd> <dt>

*AppName* 
</dt> <dd>

產生事件的應用程式名稱。

</dd> <dt>

*版本* 
</dt> <dd>

產生事件之應用程式的版本。

</dd> <dt>

*封鎖* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*路徑* 
</dt> <dd>

檔案的目的地路徑。

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

 

 




