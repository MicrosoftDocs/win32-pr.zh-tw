---
description: 子類別化是一種技術，可讓應用程式在視窗程式有機會進行處理之前，攔截和處理傳送或張貼至特定視窗的訊息。
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: 子類別化和自動訊息轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20147567bb4cd591d31e0da5f08b76a29d0229c9bc345b8c1827fc5350dd62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390221"
---
# <a name="subclassing-and-automatic-message-translation"></a>子類別化和自動訊息轉譯

子類別化是一種技術，可讓應用程式在視窗程式有機會進行處理之前，攔截和處理傳送或張貼至特定視窗的訊息。 作業系統會根據已對視窗程式進行子類別化的函式格式，自動將訊息轉譯成[Windows (ANSI) 字碼頁](code-pages.md)或[Unicode](unicode.md)格式。

下列對 [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式的呼叫會將與 *hWnd* 參數所識別之視窗相關聯的目前視窗程式子類別化。 或者，應用程式可以使用 [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)。 新的視窗程式 **NewWndProc** 會使用 Windows 字碼頁格式的文字來接收訊息。


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



當 **NewWndProc** 完成處理訊息時，它會使用 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) 函式，如下所示將訊息傳遞至 **OldWndProc**。


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



如果 **OldWndProc** 是以 unicode 類別樣式所建立，則會將訊息從 **NewWndProc** 接收的 Windows 字碼頁表單轉譯成 unicode。

同樣地，呼叫 [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 或 [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) 函式會以預期 Unicode 文字訊息的視窗程式子類別化目前的視窗程式。 訊息轉譯（如有必要）會在處理 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) 函式期間執行。

如需子類別化的詳細資訊，請參閱 [視窗程式](../winmsg/window-procedures.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Unicode 和字元集](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
