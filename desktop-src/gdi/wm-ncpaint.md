---
description: 當您 \_ 必須繪製 WM NCPAINT 訊息的框架時，就會將它傳送至視窗。
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: 'WM_NCPAINT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6be5fa951d50dbaf8663e34a5d9476ecb62576c203095bed9427dcef44425690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977998"
---
# <a name="wm_ncpaint-message"></a>WM \_ NCPAINT 訊息

當您必須繪製 **WM \_ NCPAINT** 訊息的框架時，就會將它傳送至視窗。

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

視窗更新區域的控制碼。 更新區域會裁剪至視窗框架。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則會傳回零。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會繪製視窗框架。

應用程式可以攔截 **WM \_ NCPAINT** 訊息，並繪製自己的自訂視窗框架。 視窗的裁剪區域一律是矩形，即使框架的形狀改變也一樣。

*WParam* 值可以傳遞給 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) ，如下列範例所示。


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[繪製和繪製總覽](painting-and-drawing.md)
</dt> <dt>

[繪製和繪製訊息](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**WM \_ 油漆**](wm-paint.md)
</dt> <dt>

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
