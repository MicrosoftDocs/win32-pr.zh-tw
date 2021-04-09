---
description: 要求暫停電腦的許可權。 授與使用權限的應用程式在回傳之前應該要執行暫停的準備。
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: 'PBT_APMQUERYSUSPEND (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849268"
---
# <a name="pbt_apmquerysuspend-event"></a>PBT \_ APMQUERYSUSPEND 事件

\[PBT \_ APMQUERYSUSPEND 可用於 [需求] 區段中指定的作業系統。 此事件的支援已在 Windows Vista 中移除。 請改用 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 。\]

要求暫停電腦的許可權。 授與使用權限的應用程式在回傳之前應該要執行暫停的準備。

視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。 *WParam* 和 *lParam* 參數的設定方式如下所述。


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
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

| 值                                                                                                                                                                                                                                        | 意義                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <dt>**PBT \_APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt> </dl> | 事件識別碼。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

動作旗標。 如果位0是1，則應用程式可以提示使用者如何準備暫停的指示;否則，應用程式必須在沒有使用者互動的情況下做好準備。 所有其他位值都是保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以授與暫止的要求。 若要拒絕要求，請退回 **廣播 \_ 查詢 \_ 拒絕**。

## <a name="remarks"></a>備註

應用程式應該儘快處理這個事件。 只有在已設定 *Flags* 參數中的位0時，應用程式才會提示使用者提供如何準備暫停的指示。 但是，如果此訊息是因為使用者正在關閉膝上型電腦而發出的，則無法提示使用者。 當應用程式關閉膝上型電腦蓋或按下電源按鈕並允許轉換成功時，應用程式應該遵守特定的行為。

系統大約需要20秒的時間，應用程式才能移除從應用程式訊息佇列傳送 PBT APMQUERYSUSPEND 事件的 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息 \_ 。 如果應用程式未在20秒內從佇列中移除訊息，系統會假設應用程式處於沒有回應的狀態，而且應用程式會同意睡眠要求。 未處理其訊息佇列的應用程式可能會中斷其作業。 從訊息佇列中移除訊息之後，應用程式可能需要花費太多時間才能在進入睡眠狀態之前執行任何必要的作業。 這次可能需要花費較長20秒的作業，因為系統只允許20秒的時間讓作業在 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 處理期間完成。

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

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




