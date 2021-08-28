---
description: 當計時器到期時，張貼至安裝執行緒的訊息佇列。 此訊息是由 GetMessage 或 PeekMessage 函數所張貼。
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: 'WM_TIMER 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d770d640b801849eeebe1c4ec86df8c41642c6149b89e00d82261f4e090f56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710028"
---
# <a name="wm_timer-message"></a>WM \_ 計時器訊息

當計時器到期時，張貼至安裝執行緒的訊息佇列。 此訊息是由 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函數所張貼。


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

計時器識別碼。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

應用程式定義回呼函式的指標，該函式會在安裝計時器時傳遞給 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) 函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

您可以在視窗程式中提供 **WM \_ 計時器** 案例來處理訊息。 否則， [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)會呼叫用來安裝計時器之 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)函式的呼叫中指定的 [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)回呼函數。

**WM \_ 計時器** 訊息是低優先順序的訊息。 只有當執行緒的訊息佇列中沒有其他較高優先順序的訊息時， [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 和 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函式才會張貼此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

**概念**
</dt> <dt>

[計時器](timers.md)
</dt> </dl>

 

 
