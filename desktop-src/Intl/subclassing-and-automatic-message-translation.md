---
description: 子類別化是一種技術，可讓應用程式在視窗程式有機會進行處理之前，攔截和處理傳送或張貼至特定視窗的訊息。
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: 子類別化和自動訊息轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7f0aebabe4bde259a982152327ce61a14de915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977071"
---
# <a name="subclassing-and-automatic-message-translation"></a><span data-ttu-id="6d51e-103">子類別化和自動訊息轉譯</span><span class="sxs-lookup"><span data-stu-id="6d51e-103">Subclassing and Automatic Message Translation</span></span>

<span data-ttu-id="6d51e-104">子類別化是一種技術，可讓應用程式在視窗程式有機會進行處理之前，攔截和處理傳送或張貼至特定視窗的訊息。</span><span class="sxs-lookup"><span data-stu-id="6d51e-104">Subclassing is a technique that allows an application to intercept and process messages sent or posted to a particular window before a window procedure has a chance to process them.</span></span> <span data-ttu-id="6d51e-105">作業系統會根據已對視窗程式進行子類別化的函式格式，自動將訊息轉譯成 [Windows (ANSI) 字碼頁](code-pages.md) 或 [Unicode](unicode.md) 格式。</span><span class="sxs-lookup"><span data-stu-id="6d51e-105">The operating system automatically translates messages into [Windows (ANSI) code page](code-pages.md) or [Unicode](unicode.md) form, depending on the form of the function that has subclassed the window procedure.</span></span>

<span data-ttu-id="6d51e-106">下列對 [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式的呼叫會將與 *hWnd* 參數所識別之視窗相關聯的目前視窗程式子類別化。</span><span class="sxs-lookup"><span data-stu-id="6d51e-106">The following call to the [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function subclasses the current window procedure associated with the window identified by the *hWnd* parameter.</span></span> <span data-ttu-id="6d51e-107">或者，應用程式可以使用 [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)。</span><span class="sxs-lookup"><span data-stu-id="6d51e-107">Alternatively, an application can use [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span></span> <span data-ttu-id="6d51e-108">新的視窗程式 **NewWndProc** 會收到訊息，其中包含 Windows 字碼頁格式的文字。</span><span class="sxs-lookup"><span data-stu-id="6d51e-108">The new window procedure **NewWndProc**, will receive messages with text in Windows code page format.</span></span>


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



<span data-ttu-id="6d51e-109">當 **NewWndProc** 完成處理訊息時，它會使用 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) 函式，如下所示將訊息傳遞至 **OldWndProc**。</span><span class="sxs-lookup"><span data-stu-id="6d51e-109">When **NewWndProc** has finished processing a message, it uses the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function as follows to pass the message to **OldWndProc**.</span></span>


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



<span data-ttu-id="6d51e-110">如果 **OldWndProc** 是以 unicode 類別樣式所建立，則會將訊息從 **NewWndProc** 接收的 Windows 字碼頁表單轉譯成 unicode。</span><span class="sxs-lookup"><span data-stu-id="6d51e-110">If **OldWndProc** was created with a class style of UNICODE, messages are translated from the Windows code page form received by **NewWndProc** into Unicode.</span></span>

<span data-ttu-id="6d51e-111">同樣地，呼叫 [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 或 [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) 函式會以預期 Unicode 文字訊息的視窗程式子類別化目前的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="6d51e-111">Similarly, a call to the [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function subclasses the current window procedure with a window procedure that expects Unicode text messages.</span></span> <span data-ttu-id="6d51e-112">訊息轉譯（如有必要）會在處理 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) 函式期間執行。</span><span class="sxs-lookup"><span data-stu-id="6d51e-112">Message translation, if necessary, is performed during the processing of the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function.</span></span>

<span data-ttu-id="6d51e-113">如需子類別化的詳細資訊，請參閱 [視窗程式](../winmsg/window-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="6d51e-113">For more information about subclassing, see [Window Procedures](../winmsg/window-procedures.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d51e-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d51e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d51e-115">使用 Unicode 和字元集</span><span class="sxs-lookup"><span data-stu-id="6d51e-115">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
