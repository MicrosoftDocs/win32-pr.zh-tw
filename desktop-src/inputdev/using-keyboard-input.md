---
title: 使用鍵盤輸入
description: 本節涵蓋與鍵盤輸入相關聯的工作。
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- 使用者輸入，鍵盤輸入
- 捕獲使用者輸入，鍵盤輸入
- 鍵盤輸入
- 按鍵訊息
- 字元訊息
- 游標，鍵盤輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1be8753ec6a5f920f09f6e5376b7988a88de0f9a49551492408e84908bb0c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248270"
---
# <a name="using-keyboard-input"></a>使用鍵盤輸入

視窗會以擊鍵訊息和字元訊息的形式接收鍵盤輸入。 附加至視窗的訊息迴圈必須包含程式碼，以將按鍵訊息轉譯成對應的字元訊息。 如果視窗在其工作區中顯示鍵盤輸入，則應該建立並顯示插入號，以指出將輸入下一個字元的位置。 下列各節說明接收、處理及顯示鍵盤輸入的相關程式碼：

-   [處理按鍵訊息](#processing-keystroke-messages)
-   [轉譯字元訊息](#translating-character-messages)
-   [處理字元訊息](#processing-character-messages)
-   [使用插入號](#using-the-caret)
-   [顯示鍵盤輸入](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a>處理按鍵訊息

當使用者在鍵盤上輸入時，具有鍵盤焦點之視窗的視窗程式會收到按鍵訊息。 擊鍵訊息為 [**wm \_ KEYDOWN**](wm-keydown.md)、 [**wm \_ KEYUP**](wm-keyup.md)、 [**wm \_ SYSKEYDOWN**](wm-syskeydown.md)和 [**wm \_ SYSKEYUP**](wm-syskeyup.md)。 一般的視窗程式會忽略除了 **WM \_ KEYDOWN** 以外的所有擊鍵訊息。 當使用者按下按鍵時，系統會張貼 **WM 的 \_ KEYDOWN** 訊息。

當視窗程式收到 WM 的 [**\_ KEYDOWN**](wm-keydown.md) 訊息時，它應該會檢查訊息隨附的虛擬機器碼，以決定如何處理按鍵。 虛擬金鑰程式碼位於訊息的 *wParam* 參數中。 一般來說，應用程式只會處理由非字元按鍵產生的按鍵，包括函式索引鍵、游標移動索引鍵，以及特殊用途的按鍵，例如 INS、DEL、HOME 和 END。

下列範例顯示一般應用程式用來接收和處理按鍵訊息的視窗程式架構。


```
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT: 
                    
                    // Process the LEFT ARROW key. 
                     
                    break; 
 
                case VK_RIGHT: 
                    
                    // Process the RIGHT ARROW key. 
                     
                    break; 
 
                case VK_UP: 
                    
                    // Process the UP ARROW key. 
                     
                    break; 
 
                case VK_DOWN: 
                    
                    // Process the DOWN ARROW key. 
                     
                    break; 
 
                case VK_HOME: 
                    
                    // Process the HOME key. 
                     
                    break; 
 
                case VK_END: 
                    
                    // Process the END key. 
                     
                    break; 
 
                case VK_INSERT: 
                    
                    // Process the INS key. 
                     
                    break; 
 
                case VK_DELETE: 
                    
                    // Process the DEL key. 
                     
                    break; 
 
                case VK_F2: 
                    
                    // Process the F2 key. 
                    
                    break; 
 
                
                // Process other non-character keystrokes. 
                 
                default: 
                    break; 
            } 
```



## <a name="translating-character-messages"></a>轉譯字元訊息

任何接收使用者字元輸入的執行緒，都必須在其訊息迴圈中包含 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 函數。 此函式會檢查擊鍵訊息的虛擬按鍵程式碼，如果程式碼對應到字元，則會將字元訊息放入訊息佇列。 訊息迴圈的下一個反復專案會移除並分派字元訊息;訊息的 *wParam* 參數包含字元碼。

一般而言，執行緒的訊息迴圈應該使用 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 函式來轉譯每個訊息，而不只是虛擬索引鍵訊息。 雖然 **TranslateMessage** 不會影響其他類型的訊息，但它保證鍵盤輸入正確轉譯。 下列範例示範如何在一般執行緒訊息迴圈中包含 **TranslateMessage** 函數。


```
MSG msg;
BOOL bRet;

while (( bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0) 
{
    if (bRet == -1);
    {
        // handle the error and possibly exit
    }
    else
    { 
        if (TranslateAccelerator(hwndMain, haccl, &msg) == 0) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



## <a name="processing-character-messages"></a>處理字元訊息

當 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 函式轉譯對應于字元索引鍵的虛擬機器碼程式碼時，視窗程式會收到字元訊息。 字元訊息為 [**wm \_ CHAR**](wm-char.md)、 [**wm \_ DEADCHAR**](wm-deadchar.md)、 [**wm \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)和 [**wm \_ SYSDEADCHAR**](wm-sysdeadchar.md)。 一般的視窗程式會忽略 **WM \_ 字元** 以外的所有字元訊息。 當使用者按下下列任何鍵時， **TranslateMessage** 函式會產生 **WM \_ 字元** 訊息：

-   任何字元索引鍵
-   退格鍵
-   輸入 (的回車鍵) 
-   ESC
-   SHIFT + ENTER (換行字元) 
-   TAB

當視窗程式收到 [**WM \_ 字元**](wm-char.md) 訊息時，它應該會檢查伴隨于訊息的字元碼，以決定如何處理該字元。 字元碼位於訊息的 *wParam* 參數中。

下列範例顯示一般應用程式用來接收和處理字元訊息的視窗程式架構。


```
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08: 
                    
                    // Process a backspace. 
                     
                    break; 
 
                case 0x0A: 
                    
                    // Process a linefeed. 
                     
                    break; 
 
                case 0x1B: 
                    
                    // Process an escape. 
                    
                    break; 
 
                case 0x09: 
                    
                    // Process a tab. 
                     
                    break; 
 
                case 0x0D: 
                    
                    // Process a carriage return. 
                     
                    break; 
 
                default: 
                    
                    // Process displayable characters. 
                     
                    break; 
            } 
```



## <a name="using-the-caret"></a>使用插入號

接收鍵盤輸入的視窗通常會顯示使用者在視窗的工作區中鍵入的字元。 視窗應該使用插入號來指出用戶端區域中會出現下一個字元的位置。 視窗也應該在收到鍵盤焦點時建立並顯示插入號，並在其失去焦點時隱藏和終結插入號。 視窗可以在處理 [**WM \_ SETFOCUS**](wm-setfocus.md) 和 [**wm \_ KILLFOCUS**](wm-killfocus.md) 訊息時執行這些作業。 如需游標的詳細資訊，請參閱 [游標](/windows/desktop/menurc/carets)。

## <a name="displaying-keyboard-input"></a>顯示鍵盤輸入

本章節中的範例會示範應用程式如何接收鍵盤的字元、將其顯示在視窗的工作區中，以及使用每個輸入的字元更新插入號的位置。 它也會示範如何移動插入號以回應向左箭號、向右箭號、HOME 和 END 按鍵，並示範如何將選取的文字反白顯示，以回應 SHIFT + 向右鍵的按鍵組合。

在處理 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息期間，範例中顯示的視窗程式會配置一個64k 緩衝區來儲存鍵盤輸入。 它也會抓取目前載入字型的度量，並在字型中儲存字元的高度和平均寬度。 高度和寬度會用來處理 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 的訊息，以根據工作區的大小來計算行長度和最大行數。

處理 [**WM \_ SETFOCUS**](wm-setfocus.md) 訊息時，視窗程式會建立並顯示插入號。 它會在處理 [**WM \_ KILLFOCUS**](wm-killfocus.md) 訊息時隱藏和刪除插入號。

處理 [**WM \_ CHAR**](wm-char.md) 訊息時，視窗程式會顯示字元、將它們儲存在輸入緩衝區中，並更新插入號位置。 視窗程式也會將 tab 字元轉換成四個連續的空白字元。 倒退鍵、換行字元和 escape 字元會產生嗶聲，但不會進行處理。

在處理 [**WM \_ KEYDOWN**](wm-keydown.md) 訊息時，視窗程式會執行左、右、結束和主插入號的移動。 處理向右鍵的動作時，視窗程式會檢查 SHIFT 鍵的狀態，如果已關閉，則會選取插入號右邊的字元，以移動插入號。

請注意，會撰寫下列程式碼，讓它可以編譯成 Unicode 或 ANSI。 如果原始程式碼定義 UNICODE，則會將字串視為 Unicode 字元來處理;否則，它們會以 ANSI 字元的形式處理。


```
#define BUFSIZE 65535 
#define SHIFTED 0x8000 
 
LONG APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                   // handle to device context 
    TEXTMETRIC tm;             // structure for text metrics 
    static DWORD dwCharX;      // average width of characters 
    static DWORD dwCharY;      // height of characters 
    static DWORD dwClientX;    // width of client area 
    static DWORD dwClientY;    // height of client area 
    static DWORD dwLineLen;    // line length 
    static DWORD dwLines;      // text lines in client area 
    static int nCaretPosX = 0; // horizontal position of caret 
    static int nCaretPosY = 0; // vertical position of caret 
    static int nCharWidth = 0; // width of a character 
    static int cch = 0;        // characters in buffer 
    static int nCurChar = 0;   // index of current character 
    static PTCHAR pchInputBuf; // input buffer 
    int i, j;                  // loop counters 
    int cCR = 0;               // count of carriage returns 
    int nCRIndex = 0;          // index of last carriage return 
    int nVirtKey;              // virtual-key code 
    TCHAR szBuf[128];          // temporary buffer 
    TCHAR ch;                  // current character 
    PAINTSTRUCT ps;            // required by BeginPaint 
    RECT rc;                   // output rectangle for DrawText 
    SIZE sz;                   // string dimensions 
    COLORREF crPrevText;       // previous text color 
    COLORREF crPrevBk;         // previous background color
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Get the metrics of the current font. 
 
            hdc = GetDC(hwndMain); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwndMain, hdc); 
 
            // Save the average character width and height. 
 
            dwCharX = tm.tmAveCharWidth; 
            dwCharY = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPTSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
            return 0; 
 
        case WM_SIZE: 
 
            // Save the new width and height of the client area. 
 
            dwClientX = LOWORD(lParam); 
            dwClientY = HIWORD(lParam); 
 
            // Calculate the maximum width of a line and the 
            // maximum number of lines in the client area. 
            
            dwLineLen = dwClientX - dwCharX; 
            dwLines = dwClientY / dwCharY; 
            break; 
 
 
        case WM_SETFOCUS: 
 
            // Create, position, and display the caret when the 
            // window receives the keyboard focus. 
 
            CreateCaret(hwndMain, (HBITMAP) 1, 0, dwCharY); 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            ShowCaret(hwndMain); 
            break; 
 
        case WM_KILLFOCUS: 
 
            // Hide and destroy the caret when the window loses the 
            // keyboard focus. 
 
            HideCaret(hwndMain); 
            DestroyCaret(); 
            break; 
 
        case WM_CHAR:
        // check if current location is close enough to the
        // end of the buffer that a buffer overflow may
        // occur. If so, add null and display contents. 
    if (cch > BUFSIZE-5)
    {
        pchInputBuf[cch] = 0x00;
        SendMessage(hwndMain, WM_PAINT, 0, 0);
    } 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return and position the 
                    // caret at the beginning of the new line.

                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCaretPosY += 1; 
                    break; 
 
                default:    // displayable character 
 
                    ch = (TCHAR) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width and output 
                    // the character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, nCaretPosY * dwCharY, 
                        &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer.
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the position exceeds the maximum, 
                    // insert a carriage return and move the caret 
                    // to the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwLineLen) 
                    { 
                        nCaretPosX = 0;
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCaretPosY; 
                    } 
                    nCurChar = cch; 
                    ShowCaret(hwndMain); 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT:   // LEFT ARROW 
 
                    // The caret can move only to the beginning of 
                    // the current line. 
 
                    if (nCaretPosX > 0) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the left of 
                        // the caret, calculate the character's 
                        // width, then subtract the width from the 
                        // current horizontal position of the caret 
                        // to obtain the new position. 
 
                        ch = pchInputBuf[--nCurChar]; 
                        hdc = GetDC(hwndMain); 
                        GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                        ReleaseDC(hwndMain, hdc); 
                        nCaretPosX = max(nCaretPosX - nCharWidth, 
                            0); 
                        ShowCaret(hwndMain); 
                    } 
                    break; 
 
                case VK_RIGHT:  // RIGHT ARROW 
 
                    // Caret moves to the right or, when a carriage 
                    // return is encountered, to the beginning of 
                    // the next line. 
 
                    if (nCurChar < cch) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the right of 
                        // the caret. If it's a carriage return, 
                        // position the caret at the beginning of 
                        // the next line. 
 
                        ch = pchInputBuf[nCurChar]; 
                        if (ch == 0x0D) 
                        { 
                            nCaretPosX = 0; 
                            nCaretPosY++; 
                        } 
 
                        // If the character isn't a carriage 
                        // return, check to see whether the SHIFT 
                        // key is down. If it is, invert the text 
                        // colors and output the character. 
 
                        else 
                        { 
                            hdc = GetDC(hwndMain); 
                            nVirtKey = GetKeyState(VK_SHIFT); 
                            if (nVirtKey & SHIFTED) 
                            { 
                                crPrevText = SetTextColor(hdc, 
                                    RGB(255, 255, 255)); 
                                crPrevBk = SetBkColor(hdc, 
                                    RGB(0,0,0)); 
                                TextOut(hdc, nCaretPosX, 
                                    nCaretPosY * dwCharY, 
                                    &ch, 1); 
                                SetTextColor(hdc, crPrevText); 
                                SetBkColor(hdc, crPrevBk); 
                            } 
 
                            // Get the width of the character and 
                            // calculate the new horizontal 
                            // position of the caret. 
 
                            GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                            ReleaseDC(hwndMain, hdc); 
                            nCaretPosX = nCaretPosX + nCharWidth; 
                        } 
                        nCurChar++; 
                        ShowCaret(hwndMain); 
                        break; 
                    } 
                    break; 
 
                case VK_UP:     // UP ARROW 
                case VK_DOWN:   // DOWN ARROW 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case VK_HOME:   // HOME 
 
                    // Set the caret's position to the upper left 
                    // corner of the client area. 
 
                    nCaretPosX = nCaretPosY = 0; 
                    nCurChar = 0; 
                    break; 
 
                case VK_END:    // END  
 
                    // Move the caret to the end of the text. 
 
                    for (i=0; i < cch; i++) 
                    { 
                        // Count the carriage returns and save the 
                        // index of the last one. 
 
                        if (pchInputBuf[i] == 0x0D) 
                        { 
                            cCR++; 
                            nCRIndex = i + 1; 
                        } 
                    } 
                    nCaretPosY = cCR; 
 
                    // Copy all text between the last carriage 
                    // return and the end of the keyboard input 
                    // buffer to a temporary buffer. 
 
                    for (i = nCRIndex, j = 0; i < cch; i++, j++) 
                        szBuf[j] = pchInputBuf[i]; 
                    szBuf[j] = TEXT('\0'); 
 
                    // Retrieve the text extent and use it 
                    // to set the horizontal position of the 
                    // caret. 
 
                    hdc = GetDC(hwndMain);
                    hResult = StringCchLength(szBuf, 128, pcch);
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    GetTextExtentPoint32(hdc, szBuf, *pcch, 
                        &sz); 
                    nCaretPosX = sz.cx; 
                    ReleaseDC(hwndMain, hdc); 
                    nCurChar = cch; 
                    break; 
 
                default: 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_PAINT: 
            if (cch == 0)       // nothing in input buffer 
                break; 
 
            hdc = BeginPaint(hwndMain, &ps); 
            HideCaret(hwndMain); 
 
            // Set the clipping rectangle, and then draw the text 
            // into it. 
 
            SetRect(&rc, 0, 0, dwLineLen, dwClientY); 
            DrawText(hdc, pchInputBuf, -1, &rc, DT_LEFT); 
 
            ShowCaret(hwndMain); 
            EndPaint(hwndMain, &ps); 
            break; 
        
        // Process other messages. 
        
        case WM_DESTROY: 
            PostQuitMessage(0); 
 
            // Free the input buffer. 
 
            GlobalFree((HGLOBAL) pchInputBuf); 
            UnregisterHotKey(hwndMain, 0xAAAA); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



 

 