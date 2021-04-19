---
description: 通知應用程式 APM BIOS 已發出 APM OEM 事件的信號。
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: 'PBT_APMOEMEVENT (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a99b99bdaf69b1a53a24ad33cd898fd1c806694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977051"
---
# <a name="pbt_apmoemevent-event"></a>PBT \_ APMOEMEVENT 事件

\[PBT \_ APMOEMEVENT 可用於 [需求] 區段中指定的作業系統。 此事件的支援已在 Windows Vista 中移除。\]

通知應用程式 APM BIOS 已發出 APM OEM 事件的信號。

視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。 *WParam* 和 *lParam* 參數的設定方式如下所述。


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
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

| 值                                                                                                                                                                                                                             | 意義                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <dt>**PBT \_APMOEMEVENT**</dt> <dt>11 (0xB)</dt> </dl> | 事件識別碼。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

由系統 APM BIOS 發出信號的 OEM 定義事件代碼。 OEM 事件碼位於 0200h-02FFh 的範圍內。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

因為並非所有 APM BIOS 都提供 OEM 事件通知，所以在某些電腦上可能永遠不會廣播此事件。

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

[電源管理事件](power-management-events.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




