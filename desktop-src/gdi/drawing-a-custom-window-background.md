---
description: 您可以繪製自己的視窗背景，而不是讓系統為您繪製。
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: 繪製自訂視窗背景
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972697"
---
# <a name="drawing-a-custom-window-background"></a><span data-ttu-id="ba750-103">繪製自訂視窗背景</span><span class="sxs-lookup"><span data-stu-id="ba750-103">Drawing a Custom Window Background</span></span>

<span data-ttu-id="ba750-104">您可以繪製自己的視窗背景，而不是讓系統為您繪製。</span><span class="sxs-lookup"><span data-stu-id="ba750-104">You can draw your own window background rather than having the system draw it for you.</span></span> <span data-ttu-id="ba750-105">大部分的應用程式會在註冊視窗類別時，指定類別背景筆刷的筆刷控制碼或系統色彩值;系統會使用筆刷或色彩來繪製背景。</span><span class="sxs-lookup"><span data-stu-id="ba750-105">Most applications specify a brush handle or system color value for the class background brush when registering the window class; the system uses the brush or color to draw the background.</span></span> <span data-ttu-id="ba750-106">但是，如果您將類別背景筆刷設定為 **Null**，系統就會在每次必須繪製視窗背景時，將 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息傳送至您的視窗程式，讓您繪製自訂背景。</span><span class="sxs-lookup"><span data-stu-id="ba750-106">If you set the class background brush to **NULL**, however, the system sends a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to your window procedure whenever the window background must be drawn, letting you draw a custom background.</span></span>

<span data-ttu-id="ba750-107">在下列範例中，視窗程式會繪製一個在視窗中整齊的大型棋盤圖樣。</span><span class="sxs-lookup"><span data-stu-id="ba750-107">In the following example, the window procedure draws a large checkerboard pattern that fits neatly in the window.</span></span> <span data-ttu-id="ba750-108">此程式會使用白色筆刷來填滿工作區，然後使用灰色筆刷繪製 13 20 到20個矩形。</span><span class="sxs-lookup"><span data-stu-id="ba750-108">The procedure fills the client area with a white brush and then draws thirteen 20-by-20 rectangles using a gray brush.</span></span> <span data-ttu-id="ba750-109">繪製背景時要使用的顯示裝置內容，是在訊息的 *wParam* 參數中指定。</span><span class="sxs-lookup"><span data-stu-id="ba750-109">The display device context to use when drawing the background is specified in the *wParam* parameter for the message.</span></span>


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



<span data-ttu-id="ba750-110">如果應用程式繪製自己的最小化視窗，系統也會將 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息傳送至視窗程式，以繪製最小化視窗的背景。</span><span class="sxs-lookup"><span data-stu-id="ba750-110">If the application draws its own minimized window, the system also sends the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to the window procedure to draw the background for the minimized window.</span></span> <span data-ttu-id="ba750-111">您可以使用 [**WM \_ 油漆**](wm-paint.md) 所使用的相同技術來判斷視窗是否最小化，也就是呼叫 [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) 函式，並檢查傳回值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ba750-111">You can use the same technique used by [**WM\_PAINT**](wm-paint.md) to determine whether the window is minimized that is, call the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function and check for the return value **TRUE**.</span></span>

 

 
