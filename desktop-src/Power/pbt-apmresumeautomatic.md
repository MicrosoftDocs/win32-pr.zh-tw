---
description: 通知應用程式系統正在從睡眠或休眠狀態繼續進行。 此事件會在每次系統繼續時傳遞，且不會指出使用者是否存在。
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: 'PBT_APMRESUMEAUTOMATIC (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849267"
---
# <a name="pbt_apmresumeautomatic-event"></a>PBT \_ APMRESUMEAUTOMATIC 事件

通知應用程式系統正在從睡眠或休眠狀態繼續進行。 此事件會在每次系統繼續時傳遞，且不會指出使用者是否存在。

視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。 *WParam* 和 *lParam* 參數的設定方式如下所述。

> [!Note]  
> 在 Windows 10 的1507系統或更新版本中，如果系統從睡眠狀態只繼續進入休眠狀態，則不會傳遞此事件。 在此情況下，不會傳送 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息。

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> <dt>*uMsg*</dt> <dd> 

| 值                                                                                                                                                                                                                                                                   | 意義                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | 訊息識別碼。<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| 值                                                                                                                                                                                                                                                   | 意義                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**PBT \_APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt> </dl> | 事件識別碼。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

保護必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果系統在廣播 PBT APMRESUMEAUTOMATIC 之後偵測到任何使用者活動 \_ ，它會廣播 [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) 事件，讓應用程式知道他們可以繼續與使用者進行完全互動。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>WinUser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[系統喚醒事件](system-wake-up-events.md)
</dt> <dt>

[電源管理事件](power-management-events.md)
</dt> <dt>

[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




