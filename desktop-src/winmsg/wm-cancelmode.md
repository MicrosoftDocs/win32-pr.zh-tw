---
description: 傳送以取消特定模式，例如滑鼠捕捉。
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: 'WM_CANCELMODE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae26cef4919ed93bb2a1c60376ab450560cd2142cef7b3040032f791c45ab09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849297"
---
# <a name="wm_cancelmode-message"></a>WM \_ CANCELMODE 訊息

傳送以取消特定模式，例如滑鼠捕捉。 例如，當顯示對話方塊或訊息方塊時，系統會將此訊息傳送至使用中視窗。 某些函式也會將此訊息明確地傳送到指定的視窗，不論它是否為使用中視窗。 例如， [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) 函式會在停用指定的視窗時傳送此訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_CANCELMODE                   0x001F
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

傳送 **WM \_ CANCELMODE** 訊息時， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會取消標準捲軸輸入的內部處理、取消內部功能表處理，以及放開滑鼠捕捉。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
