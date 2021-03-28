---
description: 系統不是 WM 油漆訊息的唯一來源 \_ 。 InvalidateRect 或 InvalidateRgn 函式可以間接產生 \_ 您視窗的 WM 油漆訊息。 這些函式會將一部分或部分的工作區標示為不正確 (，必須重新繪製) 。
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: 使工作區失效
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76fb02be44f600b80f87ec8f05c022fa3c35d827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991203"
---
# <a name="invalidating-the-client-area"></a><span data-ttu-id="f4f3b-105">使工作區失效</span><span class="sxs-lookup"><span data-stu-id="f4f3b-105">Invalidating the Client Area</span></span>

<span data-ttu-id="f4f3b-106">系統不是 [**WM \_ 油漆**](wm-paint.md) 訊息的唯一來源。</span><span class="sxs-lookup"><span data-stu-id="f4f3b-106">The system is not the only source of [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="f4f3b-107">[**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)或 [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)函式可以間接產生您視窗的 **WM \_ 油漆** 訊息。</span><span class="sxs-lookup"><span data-stu-id="f4f3b-107">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function can indirectly generate **WM\_PAINT** messages for your windows.</span></span> <span data-ttu-id="f4f3b-108">這些函式會將一部分或部分的工作區標示為不正確 (，必須重新繪製) 。</span><span class="sxs-lookup"><span data-stu-id="f4f3b-108">These functions mark all or part of a client area as invalid (that must be redrawn).</span></span>

<span data-ttu-id="f4f3b-109">在下列範例中，當處理 [**WM \_ 字元**](../inputdev/wm-char.md) 訊息時，視窗程式會使整個工作區失效。</span><span class="sxs-lookup"><span data-stu-id="f4f3b-109">In the following example, the window procedure invalidates the entire client area when processing [**WM\_CHAR**](../inputdev/wm-char.md) messages.</span></span> <span data-ttu-id="f4f3b-110">這可讓使用者藉由輸入數位並查看結果來變更圖形;當應用程式訊息佇列中沒有其他訊息時，就會繪製這些結果。</span><span class="sxs-lookup"><span data-stu-id="f4f3b-110">This allows the user to change the figure by typing a number and view the results; these results are drawn as soon as there are no other messages in the application's message queue.</span></span>


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



<span data-ttu-id="f4f3b-111">在此範例中， [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)所使用的 **Null** 引數會指定整個工作區;**TRUE** 引數會使背景清除。</span><span class="sxs-lookup"><span data-stu-id="f4f3b-111">In this example, the **NULL** argument used by [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) specifies the entire client area; the **TRUE** argument causes the background to be erased.</span></span> <span data-ttu-id="f4f3b-112">如果您不想讓應用程式等到應用程式訊息佇列沒有其他訊息，請使用 [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) 函式強制立即傳送 [**WM \_ 油漆**](wm-paint.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="f4f3b-112">If you do not want the application to wait until the application's message queue has no other messages, use the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) function to force the [**WM\_PAINT**](wm-paint.md) message to be sent immediately.</span></span> <span data-ttu-id="f4f3b-113">如果工作區有任何不正確部分， **UpdateWindow** 會將指定視窗的 **WM \_ 油漆** 訊息直接傳送至視窗程式。</span><span class="sxs-lookup"><span data-stu-id="f4f3b-113">If there is any invalid part of the client area, **UpdateWindow** sends the **WM\_PAINT** message for the specified window directly to the window procedure.</span></span>

 

 
