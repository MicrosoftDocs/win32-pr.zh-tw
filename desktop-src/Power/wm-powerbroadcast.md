---
description: 通知應用程式發生電源管理事件。
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: 'WM_POWERBROADCAST 訊息 (WinUser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b205a146b731bdf8cf9adc1563621232c24c10b4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396503"
---
# <a name="wm_powerbroadcast-message"></a>WM \_ POWERBROADCAST 訊息

通知應用程式發生電源管理事件。

視窗會透過其 **WindowProc** 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> <dt>
  
*uMsg*
</dt> <dd> 

| 值                                                                                                                                                                                                                                          | 意義                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>* * * * WM \_POWERBROADCAST * *</dt> * <dt>536 (0x218) </dt> </dl> | 訊息識別碼。<br/> |



 

</dd> <dt>

*wParam* 
</dt> <dd>

電源管理事件。 此參數可以是下列其中一個事件識別碼。



| 事件                                                                                                                                                                                                                                                                                        | 意義                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**[PBT \_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt> </dl> | 電源狀態已變更。<br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**[PBT \_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt> </dl>        | 作業從低電源狀態自動繼續。 每次系統繼續時，就會傳送此訊息。<br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**[PBT \_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt> </dl>                  | 作業正在從低電源狀態繼續。 如果使用者輸入觸發繼續（例如按下某個按鍵），則會在 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 之後傳送此訊息。<br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**[PBT \_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt> </dl>                                          | 系統正在暫停操作。<br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**[PBT \_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt> </dl>   | 已收到電源設定變更事件。 <br/>                                                                                                                                                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

事件特定資料。 對於大部分的事件，此參數是保留的，而且不會使用。

如果 *wParam* 參數為 [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)，則 *lParam* 參數是 [**POWERBROADCAST \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE** 。

## <a name="remarks"></a>備註

當系統繼續時，系統一律會傳送 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 訊息。 如果系統繼續回應使用者輸入，例如按下按鍵，則系統也會在傳送 PBT APMRESUMEAUTOMATIC 之後傳送 **PBT \_ APMRESUMESUSPEND** 訊息 \_ 。

**WM \_POWERBROADCAST** 訊息不會區分不同的低電源狀態。 應用程式只能判斷系統是否進入或已從低電源狀態繼續;它無法判斷特定的電源狀態。 系統會記錄有關 Windows 系統事件記錄檔中電源狀態轉換的詳細資料。

為了防止系統轉換成 Windows Vista 的低電源狀態，應用程式必須呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 來通知系統它正在使用中。

在 [需求] 區段中指定的任何作業系統上，不支援下列訊息：

- PBT_APMQUERYSTANDBY  
- PBT_APMQUERYSTANDBYFAILED  
- PBT_APMSTANDBY  
- PBT_APMRESUMESTANDBY  

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>WinUser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WM \_ POWERBROADCAST 訊息](wm-powerbroadcast-messages.md)
</dt> <dt>

[電源管理訊息](power-management-messages.md)
</dt> </dl>

 

 




