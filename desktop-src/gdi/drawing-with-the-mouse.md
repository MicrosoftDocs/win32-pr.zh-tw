---
description: 您可以允許使用者在處理 WM MOUSEMOVE 訊息時，讓您的視窗程式繪製，以利用滑鼠來繪製線條 \_ 。
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: 使用滑鼠繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ad38e7ef8af5c39918bac7231aea4dde285caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026462"
---
# <a name="drawing-with-the-mouse"></a><span data-ttu-id="89102-103">使用滑鼠繪圖</span><span class="sxs-lookup"><span data-stu-id="89102-103">Drawing with the Mouse</span></span>

<span data-ttu-id="89102-104">您可以允許使用者在處理 [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) 訊息時，讓您的視窗程式繪製，以利用滑鼠來繪製線條。</span><span class="sxs-lookup"><span data-stu-id="89102-104">You can permit the user to draw lines with the mouse by having your window procedure draw while processing the [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) message.</span></span> <span data-ttu-id="89102-105">當使用者在視窗內移動資料指標時，系統會將 **WM \_ MOUSEMOVE** 訊息傳送至視窗程式。</span><span class="sxs-lookup"><span data-stu-id="89102-105">The system sends the **WM\_MOUSEMOVE** message to the window procedure whenever the user moves the cursor within the window.</span></span> <span data-ttu-id="89102-106">若要繪製線條，視窗程式可以取出顯示裝置內容，並在視窗中的目前和先前的游標位置之間繪製線條。</span><span class="sxs-lookup"><span data-stu-id="89102-106">To draw lines, the window procedure can retrieve a display device context and draw a line in the window between the current and previous cursor positions.</span></span>

<span data-ttu-id="89102-107">在下列範例中，當使用者按下滑鼠左鍵並按住滑鼠左鍵 (傳送 [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) 訊息) 時，視窗程式會準備進行繪製。</span><span class="sxs-lookup"><span data-stu-id="89102-107">In the following example, the window procedure prepares for drawing when the user presses and holds the left mouse button (sending the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message).</span></span> <span data-ttu-id="89102-108">當使用者將游標移到視窗內時，視窗程式會收到一連串的 [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="89102-108">As the user moves the cursor within the window, the window procedure receives a series of [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages.</span></span> <span data-ttu-id="89102-109">針對每個訊息，視窗程式會繪製一條連接先前位置和目前位置的線。</span><span class="sxs-lookup"><span data-stu-id="89102-109">For each message, the window procedure draws a line connecting the previous position and the current position.</span></span> <span data-ttu-id="89102-110">為了繪製這一行，程式會使用 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 來取出顯示裝置內容;然後，只要繪製完成，而且在從訊息傳回之前，程式就會使用 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式來釋放顯示裝置內容。</span><span class="sxs-lookup"><span data-stu-id="89102-110">To draw the line, the procedure uses [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) to retrieve a display device context; then, as soon as drawing is complete and before returning from the message, the procedure uses the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function to release the display device context.</span></span> <span data-ttu-id="89102-111">當使用者放開滑鼠按鍵時，視窗程式就會清除旗標，而繪圖會停止 (傳送 [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) 訊息) 。</span><span class="sxs-lookup"><span data-stu-id="89102-111">As soon as the user releases the mouse button, the window procedure clears the flag, and the drawing stops (which sends the [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) message).</span></span>


```C++
BOOL fDraw = FALSE; 
POINT ptPrevious; 
 
  . 
  . 
  . 
 
case WM_LBUTTONDOWN: 
    fDraw = TRUE; 
    ptPrevious.x = LOWORD(lParam); 
    ptPrevious.y = HIWORD(lParam); 
    return 0L; 
 
case WM_LBUTTONUP: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, LOWORD(lParam), HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    fDraw = FALSE; 
    return 0L; 
 
case WM_MOUSEMOVE: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, ptPrevious.x = LOWORD(lParam), 
          ptPrevious.y = HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    return 0L; 
```



<span data-ttu-id="89102-112">啟用繪圖的應用程式（如這個範例所示）通常會記錄點或線條，讓您可以在視窗更新時重新繪製線條。</span><span class="sxs-lookup"><span data-stu-id="89102-112">An application that enables drawing, as in this example, typically records either the points or lines so that the lines can be redrawn whenever the window is updated.</span></span> <span data-ttu-id="89102-113">繪圖應用程式通常會使用記憶體裝置內容和相關聯的點陣圖來儲存使用滑鼠繪製的線條。</span><span class="sxs-lookup"><span data-stu-id="89102-113">Drawing applications often use a memory device context and an associated bitmap to store lines that were drawn by using a mouse.</span></span>

 

 
