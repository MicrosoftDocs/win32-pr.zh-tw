---
description: 您可以使用筆刷來繪製幾乎任何圖形的內部，方法是使用圖形裝置介面 (GDI) 函式。
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: 使用筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65ad4b14ba445642f224b0002eb1e7517c1008b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513208"
---
# <a name="using-brushes"></a><span data-ttu-id="ae936-103">使用筆刷</span><span class="sxs-lookup"><span data-stu-id="ae936-103">Using Brushes</span></span>

<span data-ttu-id="ae936-104">您可以使用筆刷來繪製幾乎任何圖形的內部，方法是使用圖形裝置介面 (GDI) 函式。</span><span class="sxs-lookup"><span data-stu-id="ae936-104">You can use a brush to paint the interior of virtually any shape by using a graphics device interface (GDI) function.</span></span> <span data-ttu-id="ae936-105">這包括矩形、橢圓形、多邊形和路徑的內部。</span><span class="sxs-lookup"><span data-stu-id="ae936-105">This includes the interiors of rectangles, ellipses, polygons, and paths.</span></span> <span data-ttu-id="ae936-106">視應用程式的需求而定，您可以使用指定之色彩、股票刷、影線筆刷或模式筆刷的實心筆刷。</span><span class="sxs-lookup"><span data-stu-id="ae936-106">Depending on the requirements of your application, you can use a solid brush of a specified color, a stock brush, a hatch brush, or a pattern brush.</span></span>

<span data-ttu-id="ae936-107">本章節包含的程式碼範例會示範如何建立自訂筆刷對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ae936-107">This section contains code samples that demonstrate the creation of a custom brush dialog box.</span></span> <span data-ttu-id="ae936-108">此對話方塊包含表示系統用來作為筆刷之點陣圖的方格。</span><span class="sxs-lookup"><span data-stu-id="ae936-108">The dialog box contains a grid that represents the bitmap the system uses as a brush.</span></span> <span data-ttu-id="ae936-109">使用者可以使用此方格來建立模式筆刷點陣圖，然後按一下 [ **測試模式** ] 按鈕以查看自訂模式。</span><span class="sxs-lookup"><span data-stu-id="ae936-109">A user can use this grid to create a pattern-brush bitmap and then view the custom pattern by clicking the **Test Pattern** button.</span></span>

<span data-ttu-id="ae936-110">下圖顯示使用 [ **自訂筆刷** ] 對話方塊所建立的模式。</span><span class="sxs-lookup"><span data-stu-id="ae936-110">The following illustration shows a pattern created by using the **Custom Brush** dialog box.</span></span>

![[自訂筆刷] 對話方塊的螢幕擷取畫面](images/custbrush.png)

<span data-ttu-id="ae936-112">若要顯示對話方塊，您必須先建立對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="ae936-112">To display a dialog box, you must first create a dialog box template.</span></span> <span data-ttu-id="ae936-113">下列對話方塊範本會定義 [ **自訂筆刷** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ae936-113">The following dialog box template defines the **Custom Brush** dialog box.</span></span>


```C++
CustBrush DIALOG 6, 18, 160, 118 
STYLE WS_DLGFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Custom Brush" 
FONT 8, "MS Sans Serif" 
BEGIN 
    CONTROL         "", IDD_GRID, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 3, 2, 83, 79 
    CONTROL         "", IDD_RECT, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 96, 11, 57, 28 
    PUSHBUTTON      "Test Pattern", IDD_PAINTRECT, 96, 47, 57, 14 
    PUSHBUTTON      "OK", IDD_OK, 29, 98, 40, 14 
    PUSHBUTTON      "Cancel", IDD_CANCEL, 92, 98, 40, 14 
END 
```



<span data-ttu-id="ae936-114">[**自訂筆刷**] 對話方塊包含五個控制項：點陣圖方格視窗、模式流覽視窗，以及三個按鈕，標示為 [**測試模式**]、 **[確定] 和 [\*\*\*\*取消**]。</span><span class="sxs-lookup"><span data-stu-id="ae936-114">The **Custom Brush** dialog box contains five controls: a bitmap-grid window, a pattern-viewing window, and three push buttons, labeled **Test Pattern**, **OK**, and **Cancel**.</span></span> <span data-ttu-id="ae936-115">**測試模式** 的 [推送] 按鈕可讓使用者查看模式。</span><span class="sxs-lookup"><span data-stu-id="ae936-115">The **Test Pattern** push button enables the user to view the pattern.</span></span> <span data-ttu-id="ae936-116">對話方塊範本會指定對話方塊視窗的整體維度、將值指派給每個控制項、指定每個控制項的位置等等。</span><span class="sxs-lookup"><span data-stu-id="ae936-116">The dialog box template specifies the overall dimensions of the dialog box window, assigns a value to each control, specifies the location of each control, and so forth.</span></span> <span data-ttu-id="ae936-117">如需詳細資訊，請參閱 [對話方塊](../dlgbox/dialog-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="ae936-117">For more information, see [Dialog Boxes](../dlgbox/dialog-boxes.md).</span></span>

<span data-ttu-id="ae936-118">對話方塊範本中的控制項值是在應用程式標頭檔中定義如下的常數。</span><span class="sxs-lookup"><span data-stu-id="ae936-118">The control values in the dialog box template are constants that have been defined as follows in the application's header file.</span></span>


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



<span data-ttu-id="ae936-119">在您建立對話方塊範本，並將它包含在應用程式的資源定義檔中之後，您必須撰寫一個對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="ae936-119">After you create a dialog box template and include it in the application's resource-definition file, you must write a dialog procedure.</span></span> <span data-ttu-id="ae936-120">此程式會處理系統傳送至對話方塊的訊息。</span><span class="sxs-lookup"><span data-stu-id="ae936-120">This procedure processes messages that the system sends to the dialog box.</span></span> <span data-ttu-id="ae936-121">下列來自應用程式原始程式碼的摘要顯示 [ **自訂筆刷** ] 對話方塊的對話方塊程式，以及它所呼叫的兩個應用程式定義函數。</span><span class="sxs-lookup"><span data-stu-id="ae936-121">The following excerpt from an application's source code shows the dialog box procedure for the **Custom Brush** dialog box and the two application-defined functions it calls.</span></span>


```C++
BOOL CALLBACK BrushDlgProc( HWND hdlg, UINT message, LONG wParam, 
                            LONG lParam) 
{ 
    static HWND hwndGrid;       // grid-window control  
    static HWND hwndBrush;      // pattern-brush control  
    static RECT rctGrid;        // grid-window rectangle  
    static RECT rctBrush;       // pattern-brush rectangle  
    static UINT bBrushBits[8];  // bitmap bits  
    static RECT rect[64];       // grid-cell array  
    static HBITMAP hbm;         // bitmap handle  
    HBRUSH hbrush;              // current brush  
    HBRUSH hbrushOld;           // default brush  
    HRGN hrgnCell;              // test-region handle  
    HDC hdc;                    // device context (DC) handle  
    int x, y, deltaX, deltaY;   // drawing coordinates  
    POINTS ptlHit;              // mouse coordinates  
    int i;                      // count variable  
 
    switch (message) 
        { 
        case WM_INITDIALOG: 
 
            // Retrieve a window handle for the grid-window and  
            // pattern-brush controls.  
 
            hwndGrid = GetDlgItem(hdlg, IDD_GRID); 
            hwndBrush = GetDlgItem(hdlg, IDD_RECT); 
 
            // Initialize the array of bits that defines the  
            // custom brush pattern with the value 1 to produce a  
            // solid white brush.  

            for (i=0; i<8; i++) 
                bBrushBits[i] = 0xFF; 
 
            // Retrieve dimensions for the grid-window and pattern- 
            // brush controls.  
 
            GetClientRect(hwndGrid, &rctGrid); 
            GetClientRect(hwndBrush, &rctBrush); 
 
            // Determine the width and height of a single cell.  
 
            deltaX = (rctGrid.right - rctGrid.left)/8; 
            deltaY = (rctGrid.bottom - rctGrid.top)/8; 
 
            // Initialize the array of cell rectangles.  
 
            for (y=rctGrid.top, i=0; y < rctGrid.bottom; y += deltaY)
            { 
                for(x=rctGrid.left; x < (rctGrid.right - 8) && i < 64; 
                        x += deltaX, i++) 
                { 
                    rect[i].left = x; rect[i].top = y; 
                    rect[i].right = x + deltaX; 
                    rect[i].bottom = y + deltaY; 
                } 
            } 
            return FALSE; 
 
 
        case WM_PAINT: 

            // Draw the grid.  
 
            hdc = GetDC(hwndGrid); 
 
            for (i=rctGrid.left; i<rctGrid.right; 
                 i+=(rctGrid.right - rctGrid.left)/8)
            { 
                 MoveToEx(hdc, i, rctGrid.top, NULL); 
                 LineTo(hdc, i, rctGrid.bottom); 
            } 
            for (i=rctGrid.top; i<rctGrid.bottom; 
                 i+=(rctGrid.bottom - rctGrid.top)/8)
            { 
                 MoveToEx(hdc, rctGrid.left, i, NULL); 
                 LineTo(hdc, rctGrid.right, i); 
            } 
            ReleaseDC(hwndGrid, hdc); 
            return FALSE; 
 
 
        case WM_LBUTTONDOWN: 
 
            // Store the mouse coordinates in a POINT structure.  
 
            ptlHit = MAKEPOINTS((POINTS FAR *)lParam); 
 
            // Create a rectangular region with dimensions and  
            // coordinates that correspond to those of the grid  
            // window.  
 
            hrgnCell = CreateRectRgn(rctGrid.left, rctGrid.top, 
                        rctGrid.right, rctGrid.bottom); 
 
            // Retrieve a window DC for the grid window.  
 
            hdc = GetDC(hwndGrid); 
 
            // Select the region into the DC.  
 
            SelectObject(hdc, hrgnCell); 
 
            // Test for a button click in the grid-window rectangle.  
 
            if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
            { 
                // A button click occurred in the grid-window  
                // rectangle; isolate the cell in which it occurred.  
 
                for(i=0; i<64; i++)
                { 
                    DeleteObject(hrgnCell); 
 
                    hrgnCell = CreateRectRgn(rect[i].left,  
                               rect[i].top, 
                               rect[i].right, rect[i].bottom); 
 
                    if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
                    { 
                        InvertRgn(hdc, hrgnCell); 
 
                        // Set the appropriate brush bits.  
 
                         if (i % 8 == 0) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x80; 
                         else if (i % 8 == 1) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x40; 
                         else if (i % 8 == 2) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x20; 
                         else if (i % 8 == 3) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x10; 
                         else if (i % 8 == 4) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x08; 
                         else if (i % 8 == 5) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x04; 
                         else if (i % 8 == 6) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x02; 
                         else if (i % 8 == 7) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x01; 
 
                      // Exit the "for" loop after the bit is set.  
 
                         break; 
                    } // end if  
 
                } // end for  
 
            } // end if  
 
            // Release the DC for the control.  
 
            ReleaseDC(hwndGrid, hdc); 
            return TRUE; 
 
 
        case WM_COMMAND: 
            switch (wParam)
            { 
               case IDD_PAINTRECT: 
 
                    hdc = GetDC(hwndBrush); 
 
                    // Create a monochrome bitmap.  
 
                    hbm = CreateBitmap(8, 8, 1, 1, 
                          (LPBYTE)bBrushBits); 
 
                    // Select the custom brush into the DC.  
 
                    hbrush = CreatePatternBrush(hbm); 
 
                    hbrushOld = SelectObject(hdc, hbrush); 
 
                    // Use the custom brush to fill the rectangle.  
 
                    Rectangle(hdc, rctBrush.left, rctBrush.top, 
                              rctBrush.right, rctBrush.bottom); 
 
                    // Clean up memory.  
                    SelectObject(hdc, hbrushOld); 
                    DeleteObject(hbrush); 
                    DeleteObject(hbm); 
 
                    ReleaseDC(hwndBrush, hdc); 
                    return TRUE; 
 
                case IDD_OK: 
 
                case IDD_CANCEL: 
                    EndDialog(hdlg, TRUE); 
                    return TRUE; 
 
            } // end switch  
            break; 
        default: 
            return FALSE; 
        } 
} 
 
 
int GetStrLngth(LPTSTR cArray) 
{ 
    int i = 0; 
 
    while (cArray[i++] != 0); 
    return i-1; 
 
} 
 
DWORD RetrieveWidth(LPTSTR cArray, int iLength) 
{ 
    int i, iTmp; 
    double dVal, dCount; 
 
    dVal = 0.0; 
    dCount = (double)(iLength-1); 
    for (i=0; i<iLength; i++)
    { 
        iTmp = cArray[i] - 0x30; 
        dVal = dVal + (((double)iTmp) * pow(10.0, dCount--)); 
    } 
 
    return (DWORD)dVal; 
} 
```



<span data-ttu-id="ae936-122">[ **自訂筆刷** ] 對話方塊的對話方塊程式會處理四個訊息，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="ae936-122">The dialog box procedure for the **Custom Brush** dialog box processes four messages, as described in the following table.</span></span>



| <span data-ttu-id="ae936-123">訊息</span><span class="sxs-lookup"><span data-stu-id="ae936-123">Message</span></span>                                          | <span data-ttu-id="ae936-124">動作</span><span class="sxs-lookup"><span data-stu-id="ae936-124">Action</span></span>                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae936-125">**WM \_ INITDIALOG**</span><span class="sxs-lookup"><span data-stu-id="ae936-125">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)   | <span data-ttu-id="ae936-126">抓取方格視窗和模式筆刷控制項的視窗控制碼和維度、計算格線視窗控制項中單一儲存格的維度，以及初始化方格儲存格座標的陣列。</span><span class="sxs-lookup"><span data-stu-id="ae936-126">Retrieves a window handle and dimensions for the grid-window and pattern-brush controls, computes the dimensions of a single cell in the grid-window control, and initializes an array of grid-cell coordinates.</span></span>                                                                                           |
| [<span data-ttu-id="ae936-127">**WM \_ 油漆**</span><span class="sxs-lookup"><span data-stu-id="ae936-127">**WM\_PAINT**</span></span>](wm-paint.md)                    | <span data-ttu-id="ae936-128">在方格視窗控制項中繪製方格模式。</span><span class="sxs-lookup"><span data-stu-id="ae936-128">Draws the grid pattern in the grid-window control.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="ae936-129">**WM \_ LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="ae936-129">**WM\_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md) | <span data-ttu-id="ae936-130">決定當使用者按下滑鼠左鍵時，游標是否位於方格視窗控制項內。</span><span class="sxs-lookup"><span data-stu-id="ae936-130">Determines whether the cursor is within the grid-window control when the user presses the left mouse button.</span></span> <span data-ttu-id="ae936-131">如果是這樣，對話方塊程式會反轉適當的方格儲存格，並將該資料格的狀態記錄在用來建立自訂筆刷點陣圖的位陣列中。</span><span class="sxs-lookup"><span data-stu-id="ae936-131">If so, the dialog box procedure inverts the appropriate grid cell and records the state of that cell in an array of bits that is used to create the bitmap for the custom brush.</span></span>              |
| [<span data-ttu-id="ae936-132">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="ae936-132">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)         | <span data-ttu-id="ae936-133">處理三個推播按鈕控制項的輸入。</span><span class="sxs-lookup"><span data-stu-id="ae936-133">Processes input for the three push button controls.</span></span> <span data-ttu-id="ae936-134">如果使用者按一下 [ **測試模式** ] 按鈕，對話方塊程式就會以新的自訂筆刷模式繪製測試模式控制項。</span><span class="sxs-lookup"><span data-stu-id="ae936-134">If the user clicks the **Test Pattern** button, the dialog box procedure paints the Test Pattern control with the new custom brush pattern.</span></span> <span data-ttu-id="ae936-135">如果使用者按一下 [ **確定]** 或 [ **取消** ] 按鈕，對話方塊程式就會據以執行動作。</span><span class="sxs-lookup"><span data-stu-id="ae936-135">If the user clicks the **OK** or **Cancel** button, the dialog box procedure performs actions accordingly.</span></span> |



 

<span data-ttu-id="ae936-136">如需訊息和訊息處理的詳細資訊，請參閱 [訊息和訊息佇列](../winmsg/messages-and-message-queues.md)。</span><span class="sxs-lookup"><span data-stu-id="ae936-136">For more information about messages and message processing, see [Messages and Message Queues](../winmsg/messages-and-message-queues.md).</span></span>

<span data-ttu-id="ae936-137">在您撰寫對話方塊程式之後，請將程式的函式定義包含在應用程式的標頭檔中，然後在應用程式的適當位置呼叫對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="ae936-137">After you write the dialog box procedure, include the function definition for the procedure in the application's header file and then call the dialog box procedure at the appropriate point in the application.</span></span>

<span data-ttu-id="ae936-138">下列來自應用程式標頭檔的摘錄會顯示對話方塊程式的函式定義，以及它所呼叫的兩個函數。</span><span class="sxs-lookup"><span data-stu-id="ae936-138">The following excerpt from the application's header file shows the function definition for the dialog box procedure and the two functions it calls.</span></span>


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



<span data-ttu-id="ae936-139">最後，下列程式碼會示範如何從應用程式的原始程式碼檔案呼叫對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="ae936-139">Finally, the following code shows how the dialog box procedure is called from the application's source-code file.</span></span>


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



<span data-ttu-id="ae936-140">通常會進行此呼叫，以回應使用者從應用程式的功能表中選擇選項。</span><span class="sxs-lookup"><span data-stu-id="ae936-140">This call is usually made in response to the user choosing an option from the application's menu.</span></span>

 

 
