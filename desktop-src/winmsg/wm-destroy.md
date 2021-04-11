---
description: 在終結視窗時傳送。 它會傳送至視窗從螢幕中移除之後終結的視窗程式。
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: 'WM_DESTROY 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193704"
---
# <a name="wm_destroy-message"></a>WM 損 \_ 毀訊息

在終結視窗時傳送。 它會傳送至視窗從螢幕中移除之後終結的視窗程式。

這則訊息會先傳送至被終結的視窗，然後再傳送至子視窗 (是否有任何) 終結。 在訊息處理期間，可以假設所有子視窗仍然存在。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

如果終結的視窗是剪貼簿檢視器鏈的一部分 (藉由呼叫 [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) 函式來設定) ，則在從 WM 終結訊息傳回之前，視窗必須先處理 [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) 函 **式 \_** ，以從鏈中移除本身。

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

[**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**WM \_ 關閉**](wm-close.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
