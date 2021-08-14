---
description: 在 SetWindowLong 函式已變更一個或多個視窗的樣式之後，傳送至視窗。
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: 'WM_STYLECHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc84d3df087cb8667367830998675903a83f633eba4797e64125269d0c937c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705938"
---
# <a name="wm_stylechanged-message"></a>WM \_ STYLECHANGED 訊息

在 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式已變更一個或多個視窗的樣式之後，傳送至視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指出視窗的樣式或延伸視窗樣式是否已變更。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                            | 意義                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_EXSTYLE**</dt> <dt>-20</dt> </dl> | 擴充的視窗樣式已變更。<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_樣式**</dt> <dt>-16</dt> </dl>       | 視窗樣式已變更。<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)結構的指標，其中包含視窗的新樣式。 應用程式可以檢查樣式，但無法加以變更。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回零。

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

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM \_ STYLECHANGING**](wm-stylechanging.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
