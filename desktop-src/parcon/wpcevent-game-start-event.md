---
description: 嘗試啟動遊戲時，系統所產生的每個使用者事件。 不同的域值是由遊戲瀏覽器系統和對應的遊戲定義檔案所提供 (GDF 受支援遊戲提供的) 中繼資料。
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: 'WPCEVENT_GAME_START (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5cc47144910f624005031573e28f5078db10ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026705"
---
# <a name="wpcevent_game_start-event"></a>WPCEVENT \_ 遊戲 \_ 開始活動

嘗試啟動遊戲時，系統所產生的每個使用者事件。 不同的域值是由遊戲瀏覽器系統和對應的遊戲定義檔案所提供 (GDF 受支援遊戲提供的) 中繼資料。


```C++
const EVENT_DESCRIPTOR WPCEVENT_GAME_START = {0x2, 0x0, 0x10, 0x4, 0x16, 0x2, 0x8000000000000030};
```



## <a name="parameters"></a>參數

<dl> <dt>

*AppID* 
</dt> <dd>

嘗試啟動之遊戲的 GUID。

</dd> <dt>

*InstanceID* 
</dt> <dd>

用來區別多個安裝的 GUID。

</dd> <dt>

*AppVersion* 
</dt> <dd>

遊戲的版本字串。

</dd> <dt>

*路徑* 
</dt> <dd>

遊戲安裝主要目錄的路徑。

</dd> <dt>

*評分* 
</dt> <dd>

識別評等系統內遊戲評等層級的字串。

</dd> <dt>

*RatingSystem* 
</dt> <dd>

GUID，可識別分級層級所套用的目前評等系統。

</dd> <dt>

*原因* 
</dt> <dd>

[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。

</dd> <dt>

*DescCount* 
</dt> <dd>

存在於描述項欄位中的描述項計數。

</dd> <dt>

*描述 符* 
</dt> <dd>

分隔的字串，其中包含針對遊戲封鎖的描述項。

</dd> <dt>

*Pid* 
</dt> <dd>

遊戲的處理序識別碼，用來與進程的填充碼關閉相互關聯。

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

 

 




