---
description: 您將 **WM_SETREDRAW** 訊息傳送至視窗，以允許重新繪製該視窗中的變更，或防止重繪該視窗中的變更。
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: 'WM_SETREDRAW 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593454"
---
# <a name="wm_setredraw-message"></a>WM_SETREDRAW 訊息

您會將 **WM \_ SETREDRAW** 訊息傳送至視窗，以允許重新繪製該視窗中的變更，或防止重繪該視窗中的變更。

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

`wParam`

重繪狀態。 如果此參數為 **TRUE**，則會在變更之後重新繪製內容。 如果此參數為 **FALSE**，則不能在變更之後重新繪製內容。

`lParam`

未使用此參數。

## <a name="return-value"></a>傳回值

如果您的應用程式處理此訊息，則應該會傳回0。

## <a name="remarks"></a>備註

如果您的應用程式必須在清單方塊中加入數個專案，這則訊息會很有用。 您的應用程式可以呼叫此訊息，並將 *wParam* 設定為 **FALSE**、新增專案，然後再呼叫 *wParam* 設定為 **TRUE** 的訊息。 最後，您的應用程式可以呼叫 [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) (*hWnd*、 **null**、 **null**、RDW \_ 清除 \| RDW \_ 框架 \| RDW \_ 使 \| RDW ALLCHILDREN) 無效，使 \_ 清單方塊重新繪製。

> [!NOTE] 
> 您應該使用 [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) 搭配指定的旗標（而不是 [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect)），因為前者對於本身具有非工作區的某些控制項是必要的，或是具有導致它們被賦予非工作區的視窗樣式 (例如 **WS_THICKFRAME**、 **WS_BORDER** 或 **WS_EX_CLIENTEDGE**) 。 如果控制項沒有非工作區，則使用這些旗標的 **RedrawWindow** 將只會執行與 **InvalidateRect** 一樣多的失效。

當 *wParam* 設定為 **FALSE** 時，將 **WM_SETREDRAW** 訊息傳遞至 **DefWindowProc** 函式會將 **WS_VISIBLE** 樣式從視窗中移除。 雖然視窗內容在螢幕上仍是可見的，但 [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) 函式會在此狀態的視窗上呼叫時傳回 **FALSE** 。 

當 *wParam* 設定為 **TRUE** 時，將 **WM_SETREDRAW** 訊息傳遞至 **DefWindowProc** 函式會將 **WS_VISIBLE** 樣式加入至視窗（如果未設定的話）。 如果您的應用程式將 *wParam* 設為 **TRUE** 的 **WM_SETREDRAW** 訊息傳送至隱藏的視窗，則視窗會變成可見。 

**Windows 10 和更新版本;Windows Server 2016 和更新版本**。 系統會在視窗中，將名為 *SysSetRedraw* 的屬性設定為視窗，其視窗程式會將 **WM_SETREDRAW** 訊息傳遞至 **DefWindowProc**。 您可以使用 [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) 函數來取得可用的屬性值。 停用重繪時， **GetProp** 會傳回非零值。 當重新啟用重繪或視窗屬性不存在時， **GetProp** 會傳回零。 

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | Windows 2000 Professional \[僅限傳統型應用程式\] |
| 最低支援的伺服器 | Windows 2000 Server \[僅限傳統型應用程式\] |
| 標頭 | <dl><dt>Winuser (包含 Windows .h) </dt></dl> |

## <a name="see-also"></a>另請參閱

* [繪製和繪製總覽](painting-and-drawing.md)
* [繪製和繪製訊息](painting-and-drawing-messages.md)
* [RedrawWindow](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
