---
description: 每個使用者的事件，嘗試以連接到家長監護的媒體應用程式播放內容時所產生的事件。
ms.assetid: 478cc11e-afbd-411a-ab84-b8ca7c3aa503
title: 'WPCEVENT_MEDIA_PLAYBACK (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdf4e884cc0e87f579d245676f78232a5ae0177
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992638"
---
# <a name="wpcevent_media_playback-event"></a>WPCEVENT \_ MEDIA \_ 播放事件

每個使用者的事件，嘗試以連接到家長監護的媒體應用程式播放內容時所產生的事件。


```C++
const EVENT_DESCRIPTOR WPCEVENT_MEDIA_PLAYBACK = {0x6, 0x0, 0x10, 0x4, 0x16, 0x6, 0x8000000000000030};
```



## <a name="parameters"></a>參數

<dl> <dt>

*AppName* 
</dt> <dd>

產生事件的媒體應用程式名稱。

</dd> <dt>

*AppVersion* 
</dt> <dd>

產生事件之媒體應用程式的版本。

</dd> <dt>

*MediaType* 
</dt> <dd>

[**WPC \_ 媒體 \_ 類型**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_type)列舉的值，指出所存取媒體檔案類型的相關資訊。

</dd> <dt>

*路徑* 
</dt> <dd>

媒體內容來源的路徑。

</dd> <dt>

*標題* 
</dt> <dd>

內容的標題中繼資料。

</dd> <dt>

*Pml* 
</dt> <dd>

家長管理層級。

</dd> <dt>

*專輯* 
</dt> <dd>

內容的專輯中繼資料。

</dd> <dt>

*明確* 
</dt> <dd>

[**WPC \_ 媒體 \_ 明確**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_explicit)列舉的值，表示媒體檔案明確分級的相關資訊。

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

 

 




