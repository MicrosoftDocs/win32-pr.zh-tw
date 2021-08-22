---
title: 使用游標
description: 本節提供的程式碼範例會示範如何執行與游標相關的工作。
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- 資源，游標
- 游標，建立
- 游標，顯示
- 游標，終結
- 游標，隱藏
- 游標，閃爍時間
- 閃爍線
- 閃爍的區塊
- 閃爍的點陣圖
- 建立游標
- 顯示游標
- 隱藏游標
- 終結游標
- 閃爍時間
- 使用者輸入，鍵盤輸入
- 捕獲使用者輸入，鍵盤輸入
- 鍵盤輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c930931df8ce401fbed8cc9af16db3cb52de08ebe9cf539109b426497318d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472644"
---
# <a name="using-carets"></a>使用游標

本節包含下列工作的程式碼範例：

-   [建立及顯示插入號](#creating-and-displaying-a-caret)
-   [隱藏插入號](#hiding-a-caret)
-   [終結插入號](#destroying-a-caret)
-   [調整閃爍時間](#adjusting-the-blink-time)
-   [處理鍵盤輸入](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a>建立及顯示插入號

收到鍵盤焦點時，視窗應該建立並顯示插入號。 使用 [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) 函式在指定的視窗中建立插入號。 然後，您可以呼叫 [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) 來設定插入號和 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) 的目前位置，使插入號變成可見。

系統會將 [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) 訊息傳送至接收鍵盤焦點的視窗; 因此，應用程式應該在處理此訊息時建立並顯示插入號。


```
HWND hwnd,       // window handle 
int x;           // horizontal coordinate of cursor 
int y;           // vertical coordinate of cursor 
int nWidth;      // width of cursor 
int nHeight;     // height of cursor 
char *lpszChar;  // pointer to character 
 
    case WM_SETFOCUS: 
 
    // Create a solid black caret. 
        CreateCaret(hwnd, (HBITMAP) NULL, nWidth, nHeight); 
 
    // Adjust the caret position, in client coordinates. 
        SetCaretPos(x, y); 
 
    // Display the caret. 
        ShowCaret(hwnd); 
 
        break; 
```



若要根據點陣圖建立插入點，您必須在使用 [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)時指定點陣圖控制碼。 您可以使用圖形應用程式來建立點陣圖，並使用資源編譯器將點陣圖新增至您的應用程式資源。 然後，您的應用程式就可以使用 [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) 函式來載入點陣圖控制碼。 例如，您可以使用下列幾行來取代上述範例中的 **CreateCaret** 行，以建立點陣圖插入號。


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



或者，您可以使用 [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) 或 [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) 函式來取出插入號點陣圖的控制碼。 如需點陣圖的詳細資訊，請參閱 [點陣圖](/windows/desktop/gdi/bitmaps)。

如果您的應用程式指定點陣圖控制碼， [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) 會忽略寬度和高度參數。 點陣圖會定義插入號的大小。

## <a name="hiding-a-caret"></a>隱藏插入號

每當您的應用程式在處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)以外的訊息時重繪畫面時，就必須使用 [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) 函式來隱藏插入號。 當您的應用程式完成繪圖時，請使用 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) 函數重新顯示插入號。 如果您的應用程式處理 **WM \_ 油漆** 訊息，則不需要隱藏並重新顯示插入號，因為此函式會自動執行這項工作。

下列程式碼範例示範如何讓您的應用程式在螢幕上繪製字元時，以及處理 [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) 訊息時，隱藏插入號。


```
HWND hwnd,   // window handle 
HDC hdc;     // device context 
 
    case WM_CHAR: 
        switch (wParam) 
        { 
            case 0x08: 
             
             // Process a backspace. 
             
                break; 
 
            case 0x09: 
             
             // Process a tab.  
             
                break; 
 
            case 0x0D: 
             
             // Process a carriage return. 
             
                break; 
 
            case 0x1B: 
             
             // Process an escape. 
             
                break; 
 
            case 0x0A: 
             
             // Process a linefeed. 
             
                break; 
 
            default: 
                // Hide the caret. 
                HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                hdc = GetDC(hwnd); 
                SelectObject(hdc, 
                    GetStockObject(SYSTEM_FIXED_FONT)); 
 
                TextOut(hdc, x, y, lpszChar, 1); 
 
                ReleaseDC(hwnd, hdc); 
 
                // Display the caret. 
 
                ShowCaret(hwnd); 
 
        } 
```



如果您的應用程式多次呼叫 [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) 函式，但未呼叫 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)，將不會顯示插入號，除非應用程式也會呼叫相同次數的 **ShowCaret** 。

## <a name="destroying-a-caret"></a>終結插入號

當視窗失去鍵盤焦點時，系統會將 [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) 訊息傳送至視窗。 您的應用程式應該使用 [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) 函式，在處理此訊息時終結插入號。 下列程式碼示範如何在不再具有鍵盤焦點的視窗中終結插入號。


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a>調整閃爍時間

在16位 Windows 中，以 Windows 為基礎的應用程式可以呼叫 [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime)函式來儲存目前的閃爍時間，然後呼叫 [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime)函式以調整在其處理 [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)訊息時的閃爍時間。 應用程式會在處理 [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)訊息時呼叫 **SetCaretBlinkTime** ，以還原使用其他應用程式的已儲存閃爍時間。 不過，這項技術無法在多執行緒環境中運作。 具體而言，停用某個應用程式並不會與啟用另一個應用程式同步處理，因此，如果某個應用程式停止回應，仍然可以啟動另一個應用程式。

應用程式應該遵守使用者所選擇的閃爍時間。 [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime)函式只能由允許使用者設定閃爍時間的應用程式呼叫。

## <a name="processing-keyboard-input"></a>處理鍵盤輸入

下列範例示範如何在簡單的文字編輯器中使用插入號。 此範例會在使用者輸入可列印的字元時，更新插入號位置，並使用各種按鍵來移動整個工作區。


```
#define TEXTMATRIX(x, y) *(pTextMatrix + (y * nWindowCharsX) + x) 
// Global variables.
HINSTANCE hinst;                  // current instance 
HBITMAP hCaret;                   // caret bitmap 
HDC hdc;                          // device context  
PAINTSTRUCT ps;                   // client area paint info 
static char *pTextMatrix = NULL;  // points to text matrix 
static int  nCharX,               // width of char. in logical units 
            nCharY,               // height of char. in logical units 
            nWindowX,             // width of client area 
            nWindowY,             // height of client area 
            nWindowCharsX,        // width of client area 
            nWindowCharsY,        // height of client area 
            nCaretPosX,           // x-position of caret 
            nCaretPosY;           // y-position of caret 
static UINT uOldBlink;            // previous blink rate 
int x, y;                         // coordinates for text matrix 
TEXTMETRIC tm;                    // font information 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,            // window handle 
    UINT message,         // type of message 
    UINT wParam,          // additional information 
    LONG lParam)          // additional information 
{ 
 
    switch (message) 
    { 
        case WM_CREATE: 
        // Select a fixed-width system font, and get its text metrics.
 
            hdc = GetDC(hwnd); 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwnd, hdc); 
 
        // Save the avg. width and height of characters. 
 
            nCharX = tm.tmAveCharWidth; 
            nCharY = tm.tmHeight; 
 
            return 0; 
 
        case WM_SIZE: 
        // Determine the width of the client area, in pixels 
        // and in number of characters. 
 
            nWindowX = LOWORD(lParam); 
            nWindowCharsX = max(1, nWindowX/nCharX); 
 
            // Determine the height of the client area, in 
            // pixels and in number of characters. 
 
            nWindowY = HIWORD(lParam); 
            nWindowCharsY = max(1, nWindowY/nCharY); 
 
            // Clear the buffer that holds the text input. 
 
            if (pTextMatrix != NULL) 
                free(pTextMatrix); 
 
            // If there is enough memory, allocate space for the 
            // text input buffer. 
 
            pTextMatrix = malloc(nWindowCharsX * nWindowCharsY); 
 
            if (pTextMatrix == NULL) 
                ErrorHandler("Not enough memory."); 
            else 
                for (y = 0; y < nWindowCharsY; y++) 
                    for (x = 0; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, y) = ' '; 
 
            // Move the caret to the origin. 
 
            SetCaretPos(0, 0); 
 
            return 0; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_HOME:       // Home 
                    nCaretPosX = 0; 
                    break; 
 
                case VK_END:        // End 
                    nCaretPosX = nWindowCharsX - 1; 
                    break; 
 
                case VK_PRIOR:      // Page Up 
                    nCaretPosY = 0; 
                    break; 
 
                case VK_NEXT:       // Page Down 
                    nCaretPosY = nWindowCharsY -1; 
                    break; 
 
                case VK_LEFT:       // Left arrow 
                    nCaretPosX = max(nCaretPosX - 1, 0); 
                    break; 
 
                case VK_RIGHT:      // Right arrow 
                    nCaretPosX = min(nCaretPosX + 1, 
                        nWindowCharsX - 1); 
                    break; 
 
                case VK_UP:         // Up arrow 
                    nCaretPosY = max(nCaretPosY - 1, 0); 
                    break; 
 
                case VK_DOWN:       // Down arrow 
                    nCaretPosY = min(nCaretPosY + 1, 
                        nWindowCharsY - 1); 
                    break; 
 
                case VK_DELETE:     // Delete 
 
                // Move all the characters that followed the 
                // deleted character (on the same line) one 
                // space back (to the left) in the matrix. 
 
                    for (x = nCaretPosX; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, nCaretPosY) = 
                            TEXTMATRIX(x + 1, nCaretPosY); 
 
                    // Replace the last character on the 
                    // line with a space. 
 
                    TEXTMATRIX(nWindowCharsX - 1, 
                        nCaretPosY) = ' '; 
 
                    // The application will draw outside the 
                    // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                    // Redraw the line, adjusted for the 
                    // deleted character. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 
                        nWindowCharsX - nCaretPosX); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // virtual-key processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:          // Backspace 
                // Move the caret back one space, and then 
                // process this like the DEL key. 
 
                    if (nCaretPosX > 0) 
                    { 
                        nCaretPosX--; 
                        SendMessage(hwnd, WM_KEYDOWN, 
                            VK_DELETE, 1L); 
                    } 
                    break; 
 
                case 0x09:          // Tab 
                // Tab stops exist every four spaces, so add 
                // spaces until the user hits the next tab. 
 
                    do 
                    { 
                        SendMessage(hwnd, WM_CHAR, ' ', 1L); 
                    } while (nCaretPosX % 4 != 0); 
                    break; 
 
                case 0x0D:          // Carriage return 
                // Go to the beginning of the next line. 
                // The bottom line wraps around to the top. 
 
                    nCaretPosX = 0; 
 
                    if (++nCaretPosY == nWindowCharsY) 
                        nCaretPosY = 0; 
                    break; 
 
                case 0x1B:        // Escape 
                case 0x0A:        // Linefeed 
                    MessageBeep((UINT) -1); 
                    break; 
 
                default: 
                // Add the character to the text buffer. 
 
                    TEXTMATRIX(nCaretPosX, nCaretPosY) = 
                        (char) wParam; 
 
                // The application will draw outside the 
                // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 1); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    // Prepare to wrap around if you reached the 
                    // end of the line. 
 
                    if (++nCaretPosX == nWindowCharsX) 
                    { 
                        nCaretPosX = 0; 
                        if (++nCaretPosY == nWindowCharsY) 
                            nCaretPosY = 0; 
                    } 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // character processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_PAINT: 
        // Draw all the characters in the buffer, line by line. 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
 
            for (y = 0; y < nWindowCharsY; y++) 
                TextOut(hdc, 0, y * nCharY, &TEXTMATRIX(0, y), 
                    nWindowCharsX); 
 
            EndPaint(hwnd, &ps); 
 
        case WM_SETFOCUS: 
        // The window has the input focus. Load the 
        // application-defined caret resource. 
 
            hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
            // Create the caret. 
 
            CreateCaret(hwnd, hCaret, 0, 0); 
 
            // Adjust the caret position. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            // Display the caret. 
 
            ShowCaret(hwnd); 
 
            break; 
 
        case WM_KILLFOCUS: 
        // The window is losing the input focus, 
        // so destroy the caret. 
 
            DestroyCaret(); 
 
            break; 
 
        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
    } 
 
    return NULL; 
} 
```



 

 