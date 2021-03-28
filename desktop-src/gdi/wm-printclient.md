---
description: 將 WM \_ PRINTCLIENT 訊息傳送至視窗，要求它在指定的裝置內容中繪製其工作區，最常見的是在印表機裝置內容中。
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: 'WM_PRINTCLIENT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973512"
---
# <a name="wm_printclient-message"></a>WM \_ PRINTCLIENT 訊息

將 **WM \_ PRINTCLIENT** 訊息傳送至視窗，要求它在指定的裝置內容中繪製其工作區，最常見的是在印表機裝置內容中。

與 [**wm \_ 列印**](wm-print.md)不同的是， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)不會處理 **wm \_ PRINTCLIENT** 。 視窗應該透過應用程式定義的 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))函式來處理 **WM \_ PRINTCLIENT** 訊息，才能正確地使用它。


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

要在其中繪製的裝置內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

繪圖選項。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                  | 意義                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ CHECKVISIBLE**</dt> </dl> | 只有當視窗可見時，才會繪製視窗。<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**PRF \_ 子系**</dt> </dl>             | 繪製所有可見的子系視窗。<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**PRF \_ 用戶端**</dt> </dl>                   | 繪製視窗的工作區。<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ ERASEBKGND**</dt> </dl>       | 在繪製視窗之前清除背景。<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF \_ 非工作區**</dt> </dl>          | 繪製視窗的非工作區。<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**\_所擁有的 PRF**</dt> </dl>                      | 繪製所有擁有的視窗。<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>備註

視窗可以用與 [**WM \_ 油漆**](./wm-paint.md)相同的方式來處理此訊息，但不需要呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 和 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) () 提供裝置內容，而且視窗應該繪製其整個工作區，而不只是不正確區域。

可以在系統中任何地方使用的視窗（例如控制項）都應該處理此訊息。 其他視窗也可能需要處理此訊息，因為它相當容易執行。

[AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow)函式要求以動畫顯示的視窗必須執行 **WM \_ PRINTCLIENT** 訊息。

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

[**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**WM \_ 油漆**](wm-paint.md)
</dt> </dl>

 

 
