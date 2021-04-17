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
# <a name="using-brushes"></a>使用筆刷

您可以使用筆刷來繪製幾乎任何圖形的內部，方法是使用圖形裝置介面 (GDI) 函式。 這包括矩形、橢圓形、多邊形和路徑的內部。 視應用程式的需求而定，您可以使用指定之色彩、股票刷、影線筆刷或模式筆刷的實心筆刷。

本章節包含的程式碼範例會示範如何建立自訂筆刷對話方塊。 此對話方塊包含表示系統用來作為筆刷之點陣圖的方格。 使用者可以使用此方格來建立模式筆刷點陣圖，然後按一下 [ **測試模式** ] 按鈕以查看自訂模式。

下圖顯示使用 [ **自訂筆刷** ] 對話方塊所建立的模式。

![[自訂筆刷] 對話方塊的螢幕擷取畫面](images/custbrush.png)

若要顯示對話方塊，您必須先建立對話方塊範本。 下列對話方塊範本會定義 [ **自訂筆刷** ] 對話方塊。


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



[**自訂筆刷**] 對話方塊包含五個控制項：點陣圖方格視窗、模式流覽視窗，以及三個按鈕，標示為 [**測試模式**]、 **[確定] 和 [****取消**]。 **測試模式** 的 [推送] 按鈕可讓使用者查看模式。 對話方塊範本會指定對話方塊視窗的整體維度、將值指派給每個控制項、指定每個控制項的位置等等。 如需詳細資訊，請參閱 [對話方塊](../dlgbox/dialog-boxes.md)。

對話方塊範本中的控制項值是在應用程式標頭檔中定義如下的常數。


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



在您建立對話方塊範本，並將它包含在應用程式的資源定義檔中之後，您必須撰寫一個對話方塊程式。 此程式會處理系統傳送至對話方塊的訊息。 下列來自應用程式原始程式碼的摘要顯示 [ **自訂筆刷** ] 對話方塊的對話方塊程式，以及它所呼叫的兩個應用程式定義函數。


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



[ **自訂筆刷** ] 對話方塊的對話方塊程式會處理四個訊息，如下表所述。



| 訊息                                          | 動作                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)   | 抓取方格視窗和模式筆刷控制項的視窗控制碼和維度、計算格線視窗控制項中單一儲存格的維度，以及初始化方格儲存格座標的陣列。                                                                                           |
| [**WM \_ 油漆**](wm-paint.md)                    | 在方格視窗控制項中繪製方格模式。                                                                                                                                                                                                                                                         |
| [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) | 決定當使用者按下滑鼠左鍵時，游標是否位於方格視窗控制項內。 如果是這樣，對話方塊程式會反轉適當的方格儲存格，並將該資料格的狀態記錄在用來建立自訂筆刷點陣圖的位陣列中。              |
| [**WM \_ 命令**](../menurc/wm-command.md)         | 處理三個推播按鈕控制項的輸入。 如果使用者按一下 [ **測試模式** ] 按鈕，對話方塊程式就會以新的自訂筆刷模式繪製測試模式控制項。 如果使用者按一下 [ **確定]** 或 [ **取消** ] 按鈕，對話方塊程式就會據以執行動作。 |



 

如需訊息和訊息處理的詳細資訊，請參閱 [訊息和訊息佇列](../winmsg/messages-and-message-queues.md)。

在您撰寫對話方塊程式之後，請將程式的函式定義包含在應用程式的標頭檔中，然後在應用程式的適當位置呼叫對話方塊程式。

下列來自應用程式標頭檔的摘錄會顯示對話方塊程式的函式定義，以及它所呼叫的兩個函數。


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



最後，下列程式碼會示範如何從應用程式的原始程式碼檔案呼叫對話方塊程式。


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



通常會進行此呼叫，以回應使用者從應用程式的功能表中選擇選項。

 

 
