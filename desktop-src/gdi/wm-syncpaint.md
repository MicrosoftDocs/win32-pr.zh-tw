---
description: 使用 WM \_ SYNCPAINT 訊息來同步處理繪製，同時避免連結獨立的 GUI 執行緒。
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: 'WM_SYNCPAINT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991498"
---
# <a name="wm_syncpaint-message"></a>WM \_ SYNCPAINT 訊息

使用 **WM \_ SYNCPAINT** 訊息來同步處理繪製，同時避免連結獨立的 GUI 執行緒。

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

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則會傳回零。

## <a name="remarks"></a>備註

當視窗隱藏、顯示、移動或調整大小時，系統可能會判斷必須將 **WM \_ SYNCPAINT** 訊息傳送至其他執行緒的最上層視窗。 應用程式必須將 **WM \_ SYNCPAINT** 傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  進行處理。 如果必須繪製視窗框架， **DefWindowProc** 函式會將 [**wm \_ NCPAINT**](wm-ncpaint.md) 訊息傳送至視窗程式，並在視窗背景清除時傳送 [**wm \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**WM \_ 油漆**](wm-paint.md)
</dt> </dl>

 

 
