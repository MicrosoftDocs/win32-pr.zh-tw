---
description: 通知應用程式，在暫停後系統已繼續操作。
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: 'PBT_APMRESUMESUSPEND (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987533"
---
# <a name="pbt_apmresumesuspend-event"></a>PBT \_ APMRESUMESUSPEND 事件

通知應用程式，在暫停後系統已繼續操作。

視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。 *WParam* 和 *lParam* 參數的設定方式如下所述。


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
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

| 值                                                                                                                                                                                                                                           | 意義                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**PBT \_APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt> </dl> | 事件識別碼。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

保護必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

只有當應用程式在電腦暫停之前收到 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件時，才會收到此事件。 否則，應用程式將會收到 [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) 事件。

如果系統因為使用者活動而喚醒 (例如按下電源按鈕) ，或系統在實體主控台上偵測到使用者互動 (例如在喚醒的情況下使用滑鼠或鍵盤輸入) ，則系統會先廣播 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 事件，然後再廣播 PBT \_ APMRESUMESUSPEND 事件。 此外，系統也會開啟顯示器。 您的應用程式應該在系統進入睡眠狀態時重新開啟已關閉的檔案，並為使用者輸入做好準備。

如果系統因為外部喚醒信號而喚醒 (遠端喚醒) ，系統只會廣播 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 事件。 PBT \_ APMRESUMESUSPEND 事件不會傳送。

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

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




