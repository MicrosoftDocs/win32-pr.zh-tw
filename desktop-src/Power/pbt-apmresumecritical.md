---
description: 通知應用程式系統已繼續操作。
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: 'PBT_APMRESUMECRITICAL (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983632"
---
# <a name="pbt_apmresumecritical-event"></a>PBT \_ APMRESUMECRITICAL 事件

\[PBT \_ APMRESUMECRITICAL 可用於 [需求] 區段中指定的作業系統。 此事件的支援已在 Windows Vista 中移除。 請改用 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 。\]

通知應用程式系統已繼續操作。 此事件可能表示部分或所有應用程式未收到 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件。 例如，此事件可以在失敗的電池造成重大暫停之後廣播。

視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。 *WParam* 和 *lParam* 參數的設定方式如下所述。


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
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

| 值                                                                                                                                                                                                                                              | 意義                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <dt>**PBT \_APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt> </dl> | 事件識別碼。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

保護必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

由於未事先通知就緊急暫停，因此先前可用的資源和資料在應用程式收到此事件時可能不存在。 應用程式應該嘗試將其狀態還原成其最佳能力。 在重大的暫止中，系統會維護 DRAM 和本機硬碟的狀態，但可能不會維護網路連接。 應用程式可能需要針對在重大暫停前于網路上開啟的檔案採取行動。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                                    |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                                           |
| 標頭<br/>                   | <dl> <dt>WinUser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[系統喚醒事件](system-wake-up-events.md)
</dt> <dt>

[電源管理事件](power-management-events.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




