---
description: 當 SetWindowLong 函式即將變更一個或多個視窗的樣式時，傳送至視窗。
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: 'WM_STYLECHANGING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849349"
---
# <a name="wm_stylechanging-message"></a>WM \_ STYLECHANGING 訊息

當 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式即將變更一個或多個視窗的樣式時，傳送至視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指出視窗的樣式或延伸視窗樣式是否正在變更。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                            | 意義                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_EXSTYLE**</dt> <dt>-20</dt> </dl> | 擴充的視窗樣式即將變更。<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_樣式**</dt> <dt>-16</dt> </dl>       | 視窗樣式即將變更。<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)結構的指標，其中包含為視窗建議的新樣式。 應用程式可以檢查樣式，並視需要加以變更。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回零。

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

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM \_ STYLECHANGED**](wm-stylechanged.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
