---
description: 通知應用程式系統（通常是電池供電的個人電腦）即將進入暫停模式。
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: 'WM_POWER 訊息 (WinUser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd525b4bf229fdb04dac4c1d1492a52dad44317344f58a2f0807ba9afbdc962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143181"
---
# <a name="wm_power-message"></a>WM \_ 電源訊息

通知應用程式系統（通常是電池供電的個人電腦）即將進入暫停模式。

> [!Note]  
> **WM \_ 電源** 訊息已過時。 它僅提供給以16位 Windows 為基礎的應用程式相容。 應用程式應該使用 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息。

 

視窗會透過其 **WindowProc** 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
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

**WM \_ 電源** 訊息識別碼。

</dd> <dt>

*wParam* 
</dt> <dd>

電源事件通知。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                        | 意義                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <dt>**PWR \_ CRITICALRESUME**</dt> </dl> | 表示在進入暫停模式之後，系統會繼續作業，而不會先將 **PWR \_ SUSPENDREQUEST** 通知訊息廣播至應用程式。 應用程式應該執行任何必要的復原動作。<br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <dt>**PWR \_ SUSPENDREQUEST**</dt> </dl> | 指出系統即將進入暫停模式。<br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <dt>**PWR \_ SUSPENDRESUME**</dt> </dl>    | 表示在進入暫停模式之後，系統會繼續作業，也就是，系統會在系統暫停之前，將 **PWR \_ SUSPENDREQUEST** 通知訊息廣播至應用程式。 應用程式應該執行任何必要的復原動作。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

應用程式傳回的值取決於 *wParam* 參數的值。 如果 *wParam* 是 **PWR \_ SUSPENDREQUEST**，則傳回值為 **PWR \_ 無法** 防止系統進入暫停狀態，否則為 **PWR \_ OK**。 如果 *wParam* 是 **PWR \_ SUSPENDRESUME** 或 **PWR \_ CRITICALRESUME**，則傳回值為零。

## <a name="remarks"></a>備註

此訊息只會廣播至在系統上執行的應用程式，該應用程式符合 Advanced 電源管理 (APM) 基本輸入/輸出系統 (BIOS) 規格。 此訊息是由電源管理驅動程式廣播到 **EnumWindows** 函式所傳回的每個視窗。

暫停模式是最大量省電的狀態，但會保留所有運算元據和參數。 系統會保留隨機存取記憶體 (RAM) 內容，但許多裝置可能會關閉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>WinUser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




