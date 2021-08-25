---
description: 通知應用程式電腦即將進入暫停狀態。
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: 'PBT_APMSUSPEND (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb3634765e6c0f863beb0c7a1c16af29cadae18ef14796e9ef01a0c8edec36a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961668"
---
# <a name="pbt_apmsuspend-event"></a>PBT \_ APMSUSPEND 事件

通知應用程式電腦即將進入暫停狀態。 此事件通常會在所有應用程式和可安裝的驅動程式都傳回 **TRUE** 至先前的 [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) 事件時廣播。

視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。 *WParam* 和 *lParam* 參數的設定方式如下所述。


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
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

| 值                                                                                                                                                                                                                         | 意義                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**PBT \_APMSUSPEND**</dt> <dt>4 (0x4)</dt> </dl> | 事件識別碼。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

保護必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

應用程式應該藉由完成儲存資料所需的所有工作來處理這個事件。

系統大約需要兩秒鐘的時間讓應用程式處理此通知。 如果應用程式在其時間配額到期之後仍在執行作業，系統可能會中斷應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>WinUser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[系統睡眠準則](system-sleep-criteria.md)
</dt> <dt>

[系統喚醒事件](system-wake-up-events.md)
</dt> <dt>

[電源管理事件](power-management-events.md)
</dt> <dt>

[PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md)
</dt> <dt>

[**SetSystemPowerState**](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




