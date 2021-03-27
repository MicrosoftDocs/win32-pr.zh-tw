---
description: 您可以使用線條函數來繪製標記。
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: 繪圖示記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b725e3a266e296950394a9bb9b2b76a17cb25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691892"
---
# <a name="drawing-markers"></a><span data-ttu-id="347e6-103">繪圖示記</span><span class="sxs-lookup"><span data-stu-id="347e6-103">Drawing Markers</span></span>

<span data-ttu-id="347e6-104">您可以使用線條函數來繪製標記。</span><span class="sxs-lookup"><span data-stu-id="347e6-104">You can use the line functions to draw markers.</span></span> <span data-ttu-id="347e6-105">標記是以點為中心的符號。</span><span class="sxs-lookup"><span data-stu-id="347e6-105">A marker is a symbol centered over a point.</span></span> <span data-ttu-id="347e6-106">繪圖應用程式會使用標記來指定起始點、結束點和控制點。</span><span class="sxs-lookup"><span data-stu-id="347e6-106">Drawing applications use markers to designate starting points, ending points, and control points.</span></span> <span data-ttu-id="347e6-107">試算表應用程式會使用標記來指定圖表或圖形上的感興趣點。</span><span class="sxs-lookup"><span data-stu-id="347e6-107">Spreadsheet applications use markers to designate points of interest on a chart or graph.</span></span>

<span data-ttu-id="347e6-108">在下列程式碼範例中，應用程式定義標記函數會使用 [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) 和 [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) 函式來建立標記。</span><span class="sxs-lookup"><span data-stu-id="347e6-108">In the following code sample, the application-defined Marker function creates a marker by using the [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) and [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) functions.</span></span> <span data-ttu-id="347e6-109">這些函式會繪製兩條相交線，長度20圖元，以游標座標為中心。</span><span class="sxs-lookup"><span data-stu-id="347e6-109">These functions draw two intersecting lines, 20 pixels in length, centered over the cursor coordinates.</span></span>


```C++
void Marker(LONG x, LONG y, HWND hwnd) 
{ 
    HDC hdc; 
 
    hdc = GetDC(hwnd); 
        MoveToEx(hdc, (int) x - 10, (int) y, (LPPOINT) NULL); 
        LineTo(hdc, (int) x + 10, (int) y); 
        MoveToEx(hdc, (int) x, (int) y - 10, (LPPOINT) NULL); 
        LineTo(hdc, (int) x, (int) y + 10); 

    ReleaseDC(hwnd, hdc); 
} 
```



<span data-ttu-id="347e6-110">當使用者按下滑鼠左鍵時，系統會將資料指標的座標儲存在 [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md)訊息的 *lParam* 參數中。</span><span class="sxs-lookup"><span data-stu-id="347e6-110">The system stores the coordinates of the cursor in the *lParam* parameter of the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message when the user presses the left mouse button.</span></span> <span data-ttu-id="347e6-111">下列程式碼會示範應用程式如何取得這些座標，判斷它們是否位於其用戶端區域內，並將它們傳遞至標記函式來繪製標記。</span><span class="sxs-lookup"><span data-stu-id="347e6-111">The following code demonstrates how an application gets these coordinates, determines whether they lie within its client area, and passes them to the Marker function to draw the marker.</span></span>


```C++
// Line- and arc-drawing variables  
 
static BOOL bCollectPoints; 
static POINT ptMouseDown[32]; 
static int index; 
POINTS ptTmp; 
RECT rc; 
 
    case WM_LBUTTONDOWN: 
 
 
        if (bCollectPoints && index < 32)
        { 
            // Create the region from the client area.  
 
            GetClientRect(hwnd, &rc); 
            hrgn = CreateRectRgn(rc.left, rc.top, 
                rc.right, rc.bottom); 
 
            ptTmp = MAKEPOINTS((POINTS FAR *) lParam); 
            ptMouseDown[index].x = (LONG) ptTmp.x; 
            ptMouseDown[index].y = (LONG) ptTmp.y; 
 
            // Test for a hit in the client rectangle.  
 
            if (PtInRegion(hrgn, ptMouseDown[index].x, 
                    ptMouseDown[index].y)) 
            { 
                // If a hit occurs, record the mouse coords.  
 
                Marker(ptMouseDown[index].x, ptMouseDown[index].y, 
                    hwnd); 
                index++; 
            } 
        } 
        break; 
```



 

 
