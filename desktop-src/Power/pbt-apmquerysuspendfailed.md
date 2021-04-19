---
description: 通知應用程式，暫停電腦的許可權遭到拒絕。
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: 'PBT_APMQUERYSUSPENDFAILED (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978967"
---
# <a name="pbt_apmquerysuspendfailed-event"></a>PBT \_ APMQUERYSUSPENDFAILED 事件

\[PBT \_ APMQUERYSUSPENDFAILED 可用於 [需求] 區段中指定的作業系統。 此事件的支援已在 Windows Vista 中移除。 請改用 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 。\]

通知應用程式，暫停電腦的許可權遭到拒絕。 如果有任何應用程式或驅動程式傳回「 **廣播 \_ 查詢 \_ 拒絕** 」至先前的 [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) 事件，則會廣播此事件。

視窗會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收此事件。 *WParam* 和 *lParam* 參數的設定方式如下所述。


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
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

| 值                                                                                                                                                                                                                                                          | 意義                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <dt>**PBT \_APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt> </dl> | 事件識別碼。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

保護必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

應用程式通常會藉由繼續正常操作來回應此事件。

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

[電源管理](power-management-portal.md)
</dt> <dt>

[電源管理事件](power-management-events.md)
</dt> <dt>

[PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




