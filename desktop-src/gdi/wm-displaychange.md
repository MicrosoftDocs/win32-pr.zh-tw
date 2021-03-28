---
description: '\_當顯示解析度變更時，會將 WM DISPLAYCHANGE 訊息傳送到所有視窗。'
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: 'WM_DISPLAYCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192386"
---
# <a name="wm_displaychange-message"></a>WM \_ DISPLAYCHANGE 訊息

當顯示解析度變更時，會將 **WM \_ DISPLAYCHANGE** 訊息傳送到所有視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam   
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

顯示的新影像深度（以位/圖元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字組指定螢幕的水準解析度。

高序位字組指定螢幕的垂直解析度。

</dd> </dl>

## <a name="remarks"></a>備註

此訊息只會傳送至最上層視窗。 所有其他視窗則會公佈。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[繪製和繪製總覽](painting-and-drawing.md)
</dt> <dt>

[繪製和繪製訊息](painting-and-drawing-messages.md)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
