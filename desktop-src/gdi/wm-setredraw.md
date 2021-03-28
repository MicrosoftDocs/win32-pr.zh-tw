---
description: 應用程式會將 WM \_ SETREDRAW 訊息傳送至視窗，以允許重新繪製該視窗中的變更，或防止重繪該視窗中的變更。
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: 'WM_SETREDRAW 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193783"
---
# <a name="wm_setredraw-message"></a>WM \_ SETREDRAW 訊息

應用程式會將 **WM \_ SETREDRAW** 訊息傳送至視窗，以允許重新繪製該視窗中的變更，或防止重繪該視窗中的變更。

若要傳送此訊息，請使用下列參數呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數。


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

重繪狀態。 如果此參數為 **TRUE**，則會在變更之後重新繪製內容。 如果此參數為 **FALSE**，則不能在變更之後重新繪製內容。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則會傳回零。

## <a name="remarks"></a>備註

如果應用程式必須在清單方塊中加入數個專案，則此訊息會很有用。 應用程式可以呼叫此訊息，並將 *wParam* 設定為 **FALSE**、新增專案，然後再呼叫 *wParam* 設定為 **TRUE** 的訊息。 最後，應用程式可以呼叫 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) (*hWnd*、 **null**、 **null**、RDW \_ 清除 \| RDW \_ 框架 \| RDW \_ 使 \| RDW \_ ALLCHILDREN) 無效，使清單方塊重新繪製。

> [!Note]  
> 使用指定之旗標的 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) ，而不是 [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ，因為前者對於本身具有非工作區的某些控制項而言是必要的，或是具有導致它們被賦予非工作區 (例如 **ws \_ THICKFRAME**、 **ws \_ BORDER** 或 **ws \_ EX \_ CLIENTEDGE**) 的視窗樣式。 如果控制項沒有非工作區，則使用這些旗標的 **RedrawWindow** 只會執行與 **InvalidateRect** 一樣多的失效。

 

如果應用程式將 **WM \_ SETREDRAW** 訊息傳送至隱藏的視窗，該視窗就會變成可見的 (也就是說，作業系統會將 **WS \_ visible** 樣式加入視窗) 。

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

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
