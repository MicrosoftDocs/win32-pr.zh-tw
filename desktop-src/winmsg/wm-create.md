---
description: 當應用程式要求透過呼叫 CreateWindowEx 或 CreateWindow 函數來建立視窗時傳送。
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: 'WM_CREATE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997828"
---
# <a name="wm_create-message"></a>WM \_ 建立訊息

當應用程式要求透過呼叫 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 或 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數來建立視窗時傳送。  (在函式傳回前傳送訊息。 ) 新視窗的視窗程式會在視窗建立之後，但視窗變成可見之前收到此訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構的指標，其中包含所要建立之視窗的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回零以繼續建立視窗。 如果應用程式傳回-1，則會終結視窗，且 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 或 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數會傳回 **Null** 控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**WM \_ NCCREATE**](wm-nccreate.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
