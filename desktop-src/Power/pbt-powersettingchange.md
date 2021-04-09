---
description: 使用 WM \_ POWERBROADCAST 視窗訊息或服務的 HandlerEx 通知回呼傳送的電源設定變更事件。
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: 'PBT_POWERSETTINGCHANGE (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849266"
---
# <a name="pbt_powersettingchange-event"></a>PBT \_ POWERSETTINGCHANGE 事件

使用 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 視窗訊息或服務的 [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) 通知回呼傳送的電源設定變更事件。


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
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

| 值                                                                                                                                                                                                                                                        | 意義                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**PBT \_POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt> </dl> | 事件識別碼。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**POWERBROADCAST \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>WinUser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[電源管理事件](power-management-events.md)
</dt> <dt>

[**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> <dt>

[**POWERBROADCAST \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

