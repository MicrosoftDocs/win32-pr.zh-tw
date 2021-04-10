---
description: 表示終止應用程式的要求，並在應用程式呼叫 PostQuitMessage 函數時產生。 此訊息會使 GetMessage 函式傳回零。
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: 'WM_QUIT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026777"
---
# <a name="wm_quit-message"></a>WM 結束 \_ 訊息

表示終止應用程式的要求，並在應用程式呼叫 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) 函數時產生。 此訊息會使 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 函式傳回零。


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)函式中提供的結束代碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

此訊息沒有傳回值，因為它會在訊息傳送至應用程式的視窗程式之前，讓訊息迴圈結束。

## <a name="remarks"></a>備註

**WM 結束 \_** 訊息不會與視窗相關聯，因此永遠不會透過視窗的視窗程式來接收。 只有 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函數才能抓取它。

請勿使用 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)函式張貼 **WM \_** 結束訊息; 請使用 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)。

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

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
