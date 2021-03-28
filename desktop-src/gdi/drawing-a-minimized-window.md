---
description: 您可以繪製自己的最小化視窗，而不是讓系統為您繪製。
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: 繪製最小化視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced1f3205243ea098856517590d58caee851329a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386175"
---
# <a name="drawing-a-minimized-window"></a><span data-ttu-id="73c46-103">繪製最小化視窗</span><span class="sxs-lookup"><span data-stu-id="73c46-103">Drawing a Minimized Window</span></span>

<span data-ttu-id="73c46-104">您可以繪製自己的最小化視窗，而不是讓系統為您繪製。</span><span class="sxs-lookup"><span data-stu-id="73c46-104">You can draw your own minimized windows rather than having the system draw them for you.</span></span> <span data-ttu-id="73c46-105">大部分的應用程式會在註冊視窗的視窗類別時定義類別圖示，而系統則會在視窗最小化時繪製圖示。</span><span class="sxs-lookup"><span data-stu-id="73c46-105">Most applications define a class icon when registering the window class for the window, and the system draws the icon when the window is minimized.</span></span> <span data-ttu-id="73c46-106">但是，如果您將類別圖示設定為 **Null**，系統會在視窗最小化時，將 [**WM \_ 油漆**](wm-paint.md) 訊息傳送至您的視窗程式，讓視窗程式在最小化視窗中繪製。</span><span class="sxs-lookup"><span data-stu-id="73c46-106">If you set the class icon to **NULL**, however, the system sends a [**WM\_PAINT**](wm-paint.md) message to your window procedure whenever the window is minimized, enabling the window procedure to draw in the minimized window.</span></span>

<span data-ttu-id="73c46-107">在下列範例中，視窗程式會在最小化的視窗中繪製星形。</span><span class="sxs-lookup"><span data-stu-id="73c46-107">In the following example, the window procedure draws a star in the minimized window.</span></span> <span data-ttu-id="73c46-108">此程式會使用 [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) 函式來判斷何時最小化視窗。</span><span class="sxs-lookup"><span data-stu-id="73c46-108">The procedure uses the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function to determine when the window is minimized.</span></span> <span data-ttu-id="73c46-109">這可確保只有在視窗最小化時，才會繪製星號。</span><span class="sxs-lookup"><span data-stu-id="73c46-109">This ensures that the star is drawn only when the window is minimized.</span></span>


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



<span data-ttu-id="73c46-110">您可以藉由將 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **hIcon** 成員設定為 **null** ，然後再呼叫 window 類別的 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)函式，將類別圖示設定為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="73c46-110">You set the class icon to **NULL** by setting the **hIcon** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to **NULL** before calling the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function for the window class.</span></span>

 

 
