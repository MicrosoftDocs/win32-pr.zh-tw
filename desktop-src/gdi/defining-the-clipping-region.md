---
description: 當使用者按一下 [定義剪輯區域] 時，系統會發出 WM \_ 命令訊息。
ms.assetid: 4b20f310-98c0-42c1-b3b3-eadf9bb2003c
title: 定義裁剪區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e49693c0e94ab9b43af817f80985af98ae2ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512913"
---
# <a name="defining-the-clipping-region"></a><span data-ttu-id="0de3d-103">定義裁剪區域</span><span class="sxs-lookup"><span data-stu-id="0de3d-103">Defining the Clipping Region</span></span>

<span data-ttu-id="0de3d-104">當使用者按一下 [定義剪輯區域] 時，系統會發出 [**WM \_ 命令**](../menurc/wm-command.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0de3d-104">When the user clicks Define Clip Region , the system issues a [**WM\_COMMAND**](../menurc/wm-command.md) message.</span></span> <span data-ttu-id="0de3d-105">此訊息的 *wParam* 參數包含應用程式定義的常數，IDM \_ 定義，表示使用者已從功能表中選取此選項。</span><span class="sxs-lookup"><span data-stu-id="0de3d-105">The *wParam* parameter of this message contains an application-defined constant, IDM\_DEFINE, that indicates that the user selected this option from the menu.</span></span> <span data-ttu-id="0de3d-106">應用程式會藉由設定布林值旗標 fDefineRegion 來處理此輸入，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="0de3d-106">The application processes this input by setting a Boolean flag, fDefineRegion, as shown in the following code sample.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
 
        case IDM_DEFINE: 
            fDefineRegion = TRUE; 
            break; 
```



<span data-ttu-id="0de3d-107">按一下 [ **定義剪下區域** ] 之後，使用者可以在游標位於應用程式的工作區中時，按一下並拖曳滑鼠來開始繪製矩形。</span><span class="sxs-lookup"><span data-stu-id="0de3d-107">After clicking **Define Clipping Region** , the user can begin drawing the rectangle by clicking and dragging the mouse while the cursor is in the application's client area.</span></span>

<span data-ttu-id="0de3d-108">當使用者按下滑鼠左鍵時，系統會發出 [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0de3d-108">When the user presses the left button, the system issues a [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message.</span></span> <span data-ttu-id="0de3d-109">此訊息的 *lParam* 參數包含游標座標，其對應至用來定義裁剪區域之矩形的左上角。</span><span class="sxs-lookup"><span data-stu-id="0de3d-109">The *lParam* parameter of this message contains the cursor coordinates, which correspond to the upper left corner of a rectangle used to define the clipping region.</span></span> <span data-ttu-id="0de3d-110">應用程式會處理 **WM \_ LBUTTONDOWN** 訊息，如下所示。</span><span class="sxs-lookup"><span data-stu-id="0de3d-110">The application processes the **WM\_LBUTTONDOWN** message, as follows.</span></span>


```C++
// These variables are required for clipping.  
 
static POINT ptUpperLeft; 
static POINT ptLowerRight; 
static POINT aptRect[5]; 
static POINT ptTmp; 
static POINTS ptsTmp; 
static BOOL fDefineRegion; 
static BOOL fRegionExists; 
static HRGN hrgn; 
static RECT rctTmp; 
int i; 
 
switch (message) 
{ 
 
    case WM_LBUTTONDOWN: 
        if (fDefineRegion) 
        { 
 
        // Retrieve the new upper left corner.  
 
            ptsTmp = MAKEPOINTS(lParam); 
            ptUpperLeft.x = (LONG) ptsTmp.x; 
            ptUpperLeft.y = (LONG) ptsTmp.y; 
        } 
 
        if (fRegionExists) 
        { 
 
            // Erase the previous rectangle.  
 
            hdc = GetDC(hwnd); 
            SetROP2(hdc, R2_NOTXORPEN); 
 
            if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
                errhandler("Polyline Failed", hwnd); 
            ReleaseDC(hwnd, hdc); 
 
            // Clear the rectangle coordinates.  
 
            for (i = 0; i < 4; i++) 
            { 
                aptRect[i].x = 0; 
                aptRect[i].y = 0; 
            } 
 
            // Clear the temporary point structure.  
 
            ptTmp.x = 0; 
            ptTmp.y = 0; 
 
            // Clear the lower right coordinates.  
 
            ptLowerRight.x = 0; 
            ptLowerRight.y = 0; 
 
            // Reset the flag.  
 
            fRegionExists = FALSE; 
            fDefineRegion = TRUE; 
 
            // Retrieve the new upper left corner.  
 
            ptsTmp = MAKEPOINTS(lParam); 
            ptUpperLeft.x = (LONG) ptsTmp.x; 
            ptUpperLeft.y = (LONG) ptsTmp.y; 
        } 
    break; 
}
```



<span data-ttu-id="0de3d-111">當使用者拖曳滑鼠時，系統會發出 [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) 訊息，並將新的資料指標座標儲存在 *lParam* 參數中。</span><span class="sxs-lookup"><span data-stu-id="0de3d-111">As the user drags the mouse, the system issues [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages and stores the new cursor coordinates in the *lParam* parameter.</span></span> <span data-ttu-id="0de3d-112">每次應用程式收到新的 **WM \_ MOUSEMOVE** 訊息時，它會清除前一個矩形 (如果有的話) ，然後藉由呼叫聚合 [**函數來**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) 繪製新的矩形，然後將矩形的四個角落的座標傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="0de3d-112">Each time the application receives a new **WM\_MOUSEMOVE** message, it erases the previous rectangle (if one exists) and draws the new rectangle by calling the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function, passing it the coordinates of the four corners of the rectangle.</span></span> <span data-ttu-id="0de3d-113">應用程式會執行下列工作。</span><span class="sxs-lookup"><span data-stu-id="0de3d-113">The application performs the following tasks.</span></span>


```C++
// These variables are required for clipping.  
 
static POINT ptUpperLeft; 
static POINT ptLowerRight; 
static POINT aptRect[5]; 
static POINT ptTmp; 
static POINTS ptsTmp; 
static BOOL fDefineRegion; 
static BOOL fRegionExists; 
static HRGN hrgn; 
static RECT rctTmp; 
int i; 
 
switch (message) 
{ 
 
    case WM_MOUSEMOVE: 
 
    if (wParam & MK_LBUTTON && fDefineRegion) 
    { 
 
        // Get a window DC.  
 
        hdc = GetDC(hwnd); 
 
        if (!SetROP2(hdc, R2_NOTXORPEN)) 
            errhandler("SetROP2 Failed", hwnd); 
 
        // If previous mouse movement occurred, store the original  
        // lower right corner coordinates in a temporary structure.  
 
        if (ptLowerRight.x) 
        { 
            ptTmp.x = ptLowerRight.x; 
            ptTmp.y = ptLowerRight.y; 
        } 
 
        // Get the new coordinates of the clipping region's lower  
        // right corner.  
 
        ptsTmp = MAKEPOINTS(lParam); 
        ptLowerRight.x = (LONG) ptsTmp.x; 
        ptLowerRight.y = (LONG) ptsTmp.y; 
 
        // If previous mouse movement occurred, erase the original  
        // rectangle.  
 
        if (ptTmp.x) 
        { 
            aptRect[0].x = ptUpperLeft.x; 
            aptRect[0].y = ptUpperLeft.y; 
            aptRect[1].x = ptTmp.x; 
            aptRect[1].y = ptUpperLeft.y; 
            aptRect[2].x = ptTmp.x; 
            aptRect[2].y = ptTmp.y; 
            aptRect[3].x = ptUpperLeft.x; 
            aptRect[3].y = ptTmp.y; 
            aptRect[4].x = aptRect[0].x; 
            aptRect[4].y = aptRect[0].y; 
 
            if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
                errhandler("Polyline Failed", hwnd); 
        } 
 
        aptRect[0].x = ptUpperLeft.x; 
        aptRect[0].y = ptUpperLeft.y; 
        aptRect[1].x = ptLowerRight.x; 
        aptRect[1].y = ptUpperLeft.y; 
        aptRect[2].x = ptLowerRight.x; 
        aptRect[2].y = ptLowerRight.y; 
        aptRect[3].x = ptUpperLeft.x; 
        aptRect[3].y = ptLowerRight.y; 
        aptRect[4].x = aptRect[0].x; 
        aptRect[4].y = aptRect[0].y; 
 
        if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
             errhandler("Polyline Failed", hwnd); 
 
        ReleaseDC(hwnd, hdc); 
    } 
    break; 
```



 

 
