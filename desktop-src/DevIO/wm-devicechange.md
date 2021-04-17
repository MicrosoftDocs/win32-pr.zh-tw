---
description: 通知應用程式對裝置或電腦的硬體設定有變更。
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: 'WM_DEVICECHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385909"
---
# <a name="wm_devicechange-message"></a>WM \_ DEVICECHANGE 訊息

通知應用程式對裝置或電腦的硬體設定有變更。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> <dt>

*uMsg* 
</dt> <dd>

**WM \_ DEVICECHANGE** 識別碼。

</dd> <dt>

*wParam* 
</dt> <dd>

已發生的事件。 此參數可以是 Dbt .h 標頭檔中的下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                  | 意義                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <dt>**[DBT \_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt> </dl>             | 已取消變更目前設定 (dock 或取消停駐) 的要求。<br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <dt>**[DBT \_CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt> </dl>                                         | 目前的設定已變更，因為停駐或解除卸載。<br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <dt>**[DBT \_CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt> </dl>                                                 | 發生自訂事件。<br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <dt>**[DBT \_DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt> </dl>                                         | 已插入裝置或媒體片段，且現在已可供使用。<br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <dt>**[DBT \_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt> </dl>                         | 要求移除裝置或媒體部分的許可權。 任何應用程式都可以拒絕此要求，並取消移除。<br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <dt>**[DBT \_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt> </dl> | 移除裝置或媒體片段的要求已取消。<br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <dt>**[DBT \_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt> </dl>             | 已移除裝置或媒體片段。<br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <dt>**[DBT \_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt> </dl>                 | 即將移除的裝置或媒體片段。 無法拒絕。<br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <dt>**[DBT \_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt> </dl>                     | 發生裝置特定事件。<br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <dt>**[DBT \_DEVNODES \_ 已變更](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt> </dl>                            | 已在系統中新增或移除裝置。<br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <dt>**[DBT \_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt> </dl>                         | 已要求許可權來變更目前的設定 (dock 或移除) 。<br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <dt>**[DBT \_使用者](dbt-userdefined.md)**</dt>的 <dt>0xffff</dt> </dl>                                                 | 此訊息的意義是使用者定義的。<br/>                                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

包含事件特定資料之結構的指標。 其格式取決於 *wParam* 參數的值。 如需詳細資訊，請參閱每個事件的檔。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以授與要求。

退回 **廣播 \_ 查詢 \_ 拒絕** 以拒絕要求。

## <a name="remarks"></a>備註

針對提供軟體可控制功能的裝置（例如彈出和鎖定），系統通常會傳送 [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) 訊息，讓應用程式和設備磁碟機正常地結束其裝置的使用。 如果系統強制移除裝置，則在這麼做之前，它可能不會傳送 [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                                                             |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                                                    |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h 或 Dbt) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)
</dt> <dt>

[DBT \_ CONFIGCHANGED](dbt-configchanged.md)
</dt> <dt>

[DBT \_ CUSTOMEVENT](dbt-customevent.md)
</dt> <dt>

[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)
</dt> <dt>

[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)
</dt> <dt>

[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)
</dt> <dt>

[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)
</dt> <dt>

[DBT \_ DEVNODES \_ 已變更](dbt-devnodes-changed.md)
</dt> <dt>

[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)
</dt> <dt>

[DBT 的 \_ 使用者](dbt-userdefined.md)
</dt> </dl>

 

