---
title: 使用滑鼠輸入
description: 本節涵蓋與滑鼠輸入相關聯的工作。
ms.assetid: b96d0046-a507-4733-bcf3-fcf757beec7f
keywords:
- 使用者輸入、滑鼠輸入
- 捕獲使用者輸入、滑鼠輸入
- 滑鼠輸入
- 游標、滑鼠輸入
- 滑鼠游標
- 按兩下 [訊息處理]
- 滑鼠滾輪
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38105da1fbbe3bee1be9ca280f1f5573dbb41ba4b7b6aa2013d9c600b8ad00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829968"
---
# <a name="using-mouse-input"></a>使用滑鼠輸入

本節涵蓋與滑鼠輸入相關聯的工作。

-   [追蹤滑鼠游標](#tracking-the-mouse-cursor)
-   [使用滑鼠繪製線條](#drawing-lines-with-the-mouse)
-   [處理按兩下訊息](#processing-a-double-click-message)
-   [選取文字行](#selecting-a-line-of-text)
-   [在具有内嵌物件的檔中使用滑鼠滾輪](#using-a-mouse-wheel-in-a-document-with-embedded-objects)
-   [取出滑鼠滾輪捲軸的數目](#retrieving-the-number-of-mouse-wheel-scroll-lines)

## <a name="tracking-the-mouse-cursor"></a>追蹤滑鼠游標

應用程式通常會執行牽涉到追蹤滑鼠游標位置的工作。 例如，大部分的繪圖應用程式都會在繪圖作業期間追蹤滑鼠游標的位置，讓使用者藉由拖曳滑鼠在視窗的工作區中繪製。 文書處理應用程式也會追蹤游標，讓使用者可以藉由按一下並拖曳滑鼠，來選取文字或文字區塊。

追蹤資料指標通常牽涉到處理 [**wm \_ LBUTTONDOWN**](wm-lbuttondown.md)、 [**WM \_ MOUSEMOVE**](wm-mousemove.md)和 [**wm \_ LBUTTONUP**](wm-lbuttonup.md) 訊息。 視窗會藉由檢查在 **WM \_ LBUTTONDOWN** 訊息的 *lParam* 參數中提供的游標位置，來決定何時開始追蹤資料指標。 例如，文字處理應用程式只會在資料指標是在文字行上時，才開始追蹤資料指標，但如果它超過檔結尾 **，則不 \_** 會開始追蹤資料指標。

視窗會藉由處理在滑鼠移動時張貼至視窗的 [**WM \_ MOUSEMOVE**](wm-mousemove.md) 訊息串流，來追蹤游標的位置。 處理 **WM \_ MOUSEMOVE** 訊息通常需要在工作區中進行重複的繪圖或繪圖操作。 例如，繪製應用程式可能會在滑鼠移動時重複重新繪製線條。 視窗會使用 [**WM \_ LBUTTONUP**](wm-lbuttonup.md) 訊息作為停止追蹤資料指標的信號。

此外，應用程式可以呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) 函數，讓系統傳送其他有助於追蹤資料指標的訊息。 當游標停留在某段時間內的工作區時，系統會張貼 [**WM \_ MOUSEHOVER**](wm-mousehover.md) 訊息。 當資料指標離開工作區時，它會張貼 [**WM \_ MOUSELEAVE**](wm-mouseleave.md) 訊息。 [**Wm \_ NCMOUSEHOVER**](wm-ncmousehover.md)和 [**wm \_ NCMOUSELEAVE**](wm-ncmouseleave.md)訊息是非工作區的對應訊息。

## <a name="drawing-lines-with-the-mouse"></a>使用滑鼠繪製線條

本節中的範例示範如何追蹤滑鼠游標。 它包含部分的視窗程式，可讓使用者藉由拖曳滑鼠，在視窗的工作區中繪製線條。

當視窗程式收到 [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md) 訊息時，它會捕捉滑鼠並儲存游標的座標，並使用座標做為線條的起點。 它也會使用 [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) 函式，將資料指標限制在程式列繪圖作業期間的工作區。

在第一個 [**WM \_ MOUSEMOVE**](wm-mousemove.md) 訊息期間，視窗程式會從起始點繪製一行到游標目前的位置。 在後續的 **WM \_ MOUSEMOVE** 訊息中，視窗程式會使用反轉的畫筆色彩來進行繪製，藉以清除前一行。 然後，它會從起始點繪製新的一行到游標的新位置。

[**WM \_ LBUTTONUP**](wm-lbuttonup.md)訊息表示繪圖作業結束。 視窗程式會釋放滑鼠捕捉，並從工作區釋放滑鼠。


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                       // handle to device context 
    RECT rcClient;                 // client area rectangle 
    POINT ptClientUL;              // client upper left corner 
    POINT ptClientLR;              // client lower right corner 
    static POINTS ptsBegin;        // beginning point 
    static POINTS ptsEnd;          // new endpoint 
    static POINTS ptsPrevEnd;      // previous endpoint 
    static BOOL fPrevLine = FALSE; // previous line flag 
 
    switch (uMsg) 
    { 
       case WM_LBUTTONDOWN: 
 
            // Capture mouse input. 
 
            SetCapture(hwndMain); 
 
            // Retrieve the screen coordinates of the client area, 
            // and convert them into client coordinates. 
 
            GetClientRect(hwndMain, &rcClient); 
            ptClientUL.x = rcClient.left; 
            ptClientUL.y = rcClient.top; 
 
            // Add one to the right and bottom sides, because the 
            // coordinates retrieved by GetClientRect do not 
            // include the far left and lowermost pixels. 
 
            ptClientLR.x = rcClient.right + 1; 
            ptClientLR.y = rcClient.bottom + 1; 
            ClientToScreen(hwndMain, &ptClientUL); 
            ClientToScreen(hwndMain, &ptClientLR); 
 
            // Copy the client coordinates of the client area 
            // to the rcClient structure. Confine the mouse cursor 
            // to the client area by passing the rcClient structure 
            // to the ClipCursor function. 
 
            SetRect(&rcClient, ptClientUL.x, ptClientUL.y, 
                ptClientLR.x, ptClientLR.y); 
            ClipCursor(&rcClient); 
 
            // Convert the cursor coordinates into a POINTS 
            // structure, which defines the beginning point of the 
            // line drawn during a WM_MOUSEMOVE message. 
 
            ptsBegin = MAKEPOINTS(lParam); 
            return 0; 
 
        case WM_MOUSEMOVE: 
 
            // When moving the mouse, the user must hold down 
            // the left mouse button to draw lines. 
 
            if (wParam & MK_LBUTTON) 
            { 
 
                // Retrieve a device context (DC) for the client area. 
 
                hdc = GetDC(hwndMain); 
 
                // The following function ensures that pixels of 
                // the previously drawn line are set to white and 
                // those of the new line are set to black. 
 
                SetROP2(hdc, R2_NOTXORPEN); 
 
                // If a line was drawn during an earlier WM_MOUSEMOVE 
                // message, draw over it. This erases the line by 
                // setting the color of its pixels to white. 
 
                if (fPrevLine) 
                { 
                    MoveToEx(hdc, ptsBegin.x, ptsBegin.y, 
                        (LPPOINT) NULL); 
                    LineTo(hdc, ptsPrevEnd.x, ptsPrevEnd.y); 
                } 
 
                // Convert the current cursor coordinates to a 
                // POINTS structure, and then draw a new line. 
 
                ptsEnd = MAKEPOINTS(lParam); 
                MoveToEx(hdc, ptsBegin.x, ptsBegin.y, (LPPOINT) NULL); 
                LineTo(hdc, ptsEnd.x, ptsEnd.y); 
 
                // Set the previous line flag, save the ending 
                // point of the new line, and then release the DC. 
 
                fPrevLine = TRUE; 
                ptsPrevEnd = ptsEnd; 
                ReleaseDC(hwndMain, hdc); 
            } 
            break; 
 
        case WM_LBUTTONUP: 
 
            // The user has finished drawing the line. Reset the 
            // previous line flag, release the mouse cursor, and 
            // release the mouse capture. 
 
            fPrevLine = FALSE; 
            ClipCursor(NULL); 
            ReleaseCapture(); 
            return 0; 
 
        case WM_DESTROY: 
            PostQuitMessage(0); 
            break; 
 
        // Process other messages. 
        
```



## <a name="processing-a-double-click-message"></a>處理按兩下訊息

若要接收按兩下訊息，視窗必須屬於具有 [**CS \_ DBLCLKS**](/windows/desktop/winmsg/about-window-classes) 類別樣式的視窗類別。 您可以在註冊視窗類別時設定此樣式，如下列範例所示。


```
BOOL InitApplication(HINSTANCE hInstance) 
{ 
    WNDCLASS wc; 
 
    wc.style = CS_DBLCLKS | CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hInstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_IBEAM); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName = "MainMenu"; 
    wc.lpszClassName = "MainWClass"; 
 
    return RegisterClass(&wc); 
} 
```



按兩下訊息的前面一律會加上按鈕下的訊息。 基於這個理由，應用程式通常會使用按兩下訊息，來擴充在按鈕的訊息期間開始的工作。

## <a name="selecting-a-line-of-text"></a>選取文字行

本節中的範例取自簡單的文字處理應用程式。 它包含的程式碼可讓使用者按一下文字行上的任何位置，以設定插入號的位置，然後按兩下行上的任何位置來選取 (反白顯示) 一行文字。


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                     // handle to device context 
    TEXTMETRIC tm;               // font size data 
    int i, j;                    // loop counters 
    int cCR = 0;                 // count of carriage returns 
    char ch;                     // character from input buffer 
    static int nBegLine;         // beginning of selected line 
    static int nCurrentLine = 0; // currently selected line 
    static int nLastLine = 0;    // last text line 
    static int nCaretPosX = 0;   // x-coordinate of caret 
    static int cch = 0;          // number of characters entered 
    static int nCharWidth = 0;   // exact width of a character 
    static char szHilite[128];   // text string to highlight 
    static DWORD dwCharX;        // average width of characters 
    static DWORD dwLineHeight;   // line height 
    static POINTS ptsCursor;     // coordinates of mouse cursor 
    static COLORREF crPrevText;  // previous text color 
    static COLORREF crPrevBk;    // previous background color 
    static PTCHAR pchInputBuf;   // pointer to input buffer 
    static BOOL fTextSelected = FALSE; // text-selection flag 
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
            dwLineHeight = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep( (UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return, and position the 
                    // caret at the beginning of the new line. 
 
                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCurrentLine += 1; 
                    break; 
 
                default:    / displayable character 
 
                    ch = (char) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width, and display the 
                    // character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, 
                        nCurrentLine * dwLineHeight, &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer. 
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the new position exceeds the maximum, 
                    // insert a carriage return and reposition the 
                    // caret at the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwMaxCharX) 
                    { 
                        nCaretPosX = 0; 
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCurrentLine; 
                    } 
 
                    ShowCaret(hwndMain); 
 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            nLastLine = max(nLastLine, nCurrentLine); 
            break; 
 
        // Process other messages. 
 
        case WM_LBUTTONDOWN: 
 
            // If a line of text is currently highlighted, redraw 
            // the text to remove the highlighting. 
 
            if (fTextSelected) 
            { 
                hdc = GetDC(hwndMain); 
                SetTextColor(hdc, crPrevText); 
                SetBkColor(hdc, crPrevBk);
                hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
                if (FAILED(hResult))
                {
                // TODO: write error handler
                } 
                TextOut(hdc, 0, nCurrentLine * dwLineHeight, 
                    szHilite, *pcch); 
                ReleaseDC(hwndMain, hdc); 
                ShowCaret(hwndMain); 
                fTextSelected = FALSE; 
            } 
 
            // Save the current mouse-cursor coordinates. 
 
            ptsCursor = MAKEPOINTS(lParam); 
 
            // Determine which line the cursor is on, and save 
            // the line number. Do not allow line numbers greater 
            // than the number of the last line of text. The 
            // line number is later multiplied by the average height 
            // of the current font. The result is used to set the 
            // y-coordinate of the caret. 
 
            nCurrentLine = min((int)(ptsCursor.y / dwLineHeight), 
                nLastLine); 
 
            // Parse the text input buffer to find the first 
            // character in the selected line of text. Each 
            // line ends with a carriage return, so it is possible 
            // to count the carriage returns to find the selected 
            // line. 
 
            cCR = 0; 
            nBegLine = 0; 
            if (nCurrentLine != 0) 
            { 
                for (i = 0; (i < cch) && 
                        (cCR < nCurrentLine); i++) 
                { 
                    if (pchInputBuf[i] == 0x0D) 
                        ++cCR; 
                } 
                nBegLine = i; 
            } 
 
            // Starting at the beginning of the selected line, 
            // measure  the width of each character, summing the 
            // width with each character measured. Stop when the 
            // sum is greater than the x-coordinate of the cursor. 
            // The sum is used to set the x-coordinate of the caret. 
 
            hdc = GetDC(hwndMain); 
            nCaretPosX = 0; 
            for (i = nBegLine; 
                (pchInputBuf[i] != 0x0D) && (i < cch); i++) 
            { 
                ch = pchInputBuf[i]; 
                GetCharWidth32(hdc, (int) ch, (int) ch, &nCharWidth); 
                if ((nCaretPosX + nCharWidth) > ptsCursor.x) break; 
                else nCaretPosX += nCharWidth; 
            } 
            ReleaseDC(hwndMain, hdc); 
 
            // Set the caret to the user-selected position. 
 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            break; 
 
        case WM_LBUTTONDBLCLK: 
 
            // Copy the selected line of text to a buffer. 
 
            for (i = nBegLine, j = 0; (pchInputBuf[i] != 0x0D) && 
                    (i < cch); i++) 
            {
                szHilite[j++] = pchInputBuf[i]; 
            }
            szHilite[j] = '\0'; 
 
            // Hide the caret, invert the background and foreground 
            // colors, and then redraw the selected line. 
 
            HideCaret(hwndMain); 
            hdc = GetDC(hwndMain); 
            crPrevText = SetTextColor(hdc, RGB(255, 255, 255)); 
            crPrevBk = SetBkColor(hdc, RGB(0, 0, 0));
            hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 0, nCurrentLine * dwLineHeight, szHilite, *pcch); 
            SetTextColor(hdc, crPrevText); 
            SetBkColor(hdc, crPrevBk); 
            ReleaseDC(hwndMain, hdc); 
 
            fTextSelected = TRUE; 
            break; 

            // Process other messages. 

        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="using-a-mouse-wheel-in-a-document-with-embedded-objects"></a>在具有内嵌物件的檔中使用滑鼠滾輪

此範例假設 Microsoft Word 檔具有各種内嵌物件：

-   Microsoft Excel 試算表
-   內嵌的清單方塊控制項，可滾動回應滾輪
-   未回應滾輪的內嵌文字方塊控制項

[MSH \_ 滑鼠滾輪](about-mouse-input.md)訊息一律會傳送至 Microsoft Word 中的主視窗。 即使內嵌的試算表為使用中，也是如此。 下表說明如何 \_ 根據焦點處理 MSH 滑鼠滾輪訊息。



| 焦點為開啟                | 處理如下所示                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Word 檔              | Word 會滾動文件視窗。                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Embedded Excel 試算表 | Word 會將訊息張貼至 Excel。 您必須決定內嵌應用程式是否應該回應訊息。                                                                                                                                                                                                                                                                                                                                                            |
| 內嵌控制項           | 應用程式會將訊息傳送至具有焦點的內嵌控制項，並檢查傳回碼以查看控制項是否處理它。 如果控制項未處理，則應用程式應該會滾動文件視窗。 例如，如果使用者按一下清單方塊，然後再滾動滾輪，該控制項就會滾動以回應滾輪旋轉。 如果使用者按一下某個文字方塊，然後旋轉滾輪，整份檔都會滾動。 |



 

下列範例會示範應用程式如何處理這兩個滾輪訊息。


```
/************************************************
* this code deals with MSH_MOUSEWHEEL
*************************************************/
#include "zmouse.h"

//
// Mouse Wheel rotation stuff, only define if we are
// on a version of the OS that does not support
// WM_MOUSEWHEEL messages.
//
#ifndef WM_MOUSEWHEEL
#define WM_MOUSEWHEEL WM_MOUSELAST+1 
    // Message ID for IntelliMouse wheel
#endif

UINT uMSH_MOUSEWHEEL = 0;   // Value returned from
                            // RegisterWindowMessage()

/**************************************************

INT WINAPI WinMain(
         HINSTANCE hInst, 
         HINSTANCE hPrevInst, 
         LPSTR lpCmdLine, 
         INT nCmdShow)
{
    MSG msg;
    BOOL bRet;

    if (!InitInstance(hInst, nCmdShow))
        return FALSE;

    //
    // The new IntelliMouse uses a Registered message to transmit
    // wheel rotation info. So register for it!
 
    uMSH_MOUSEWHEEL =
     RegisterWindowMessage(MSH_MOUSEWHEEL); 
    if ( !uMSH_MOUSEWHEEL )
    {
        MessageBox(NULL,"
                   RegisterWindowMessag Failed!",
                   "Error",MB_OK);
        return msg.wParam;
    }
    
    while (( bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            if (!TranslateAccelerator(ghwndApp,
                                      ghaccelTable,
                                      &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }

    return msg.wParam;
}

/************************************************
* this code deals with WM_MOUSEWHEEL
*************************************************/
LONG APIENTRY MainWndProc(
    HWND hwnd,
    UINT msg,
    WPARAM wParam,
    LPARAM lParam)
{
    static int nZoom = 0;
    

    switch (msg)
    {
        //
        // Handle Mouse Wheel messages generated
        // by the operating systems that have built-in
        // support for the WM_MOUSEWHEEL message.
        //

        case WM_MOUSEWHEEL:
            ((short) HIWORD(wParam)< 0) ? nZoom-- : nZoom++;

            //
            // Do other wheel stuff...
            //

            break;

        default:
            //
            // uMSH_MOUSEWHEEL is a message registered by
            // the mswheel dll on versions of Windows that
            // do not support the new message in the OS.

            if( msg == uMSH_MOUSEWHEEL )
            {
               ((int)wParam < 0) ? nZoom-- : nZoom++;

                //
                // Do other wheel stuff...
                //
                break;
            }

            return DefWindowProc(hwnd,
                                 msg,
                                 wParam,
                                 lParam);
    }

    return 0L;
}
```



## <a name="retrieving-the-number-of-mouse-wheel-scroll-lines"></a>取出滑鼠滾輪捲軸的數目

下列程式碼可讓應用程式使用 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取出捲軸的數目。


```
#ifndef SPI_GETWHEELSCROLLLINES
#define SPI_GETWHEELSCROLLLINES   104
#endif

#include "zmouse.h"

/*********************************************************
* FUNCTION: GetNumScrollLines
* Purpose : An OS independent method to retrieve the 
*           number of wheel scroll lines
* Params  : none
* Returns : UINT:  Number of scroll lines where WHEEL_PAGESCROLL 
*           indicates to scroll a page at a time.
*********************************************************/
UINT GetNumScrollLines(void)
{
   HWND hdlMsWheel;
   UINT ucNumLines=3;  // 3 is the default
   OSVERSIONINFO osversion;
   UINT uiMsh_MsgScrollLines;
   

   memset(&osversion, 0, sizeof(osversion));
   osversion.dwOSVersionInfoSize =sizeof(osversion);
   GetVersionEx(&osversion);

   if ((osversion.dwPlatformId == VER_PLATFORM_WIN32_WINDOWS) ||
       ( (osversion.dwPlatformId == VER_PLATFORM_WIN32_NT) && 
         (osversion.dwMajorVersion < 4) )   )
   {
        hdlMsWheel = FindWindow(MSH_WHEELMODULE_CLASS, 
                                MSH_WHEELMODULE_TITLE);
        if (hdlMsWheel)
        {
           uiMsh_MsgScrollLines = RegisterWindowMessage
                                     (MSH_SCROLL_LINES);
           if (uiMsh_MsgScrollLines)
                ucNumLines = (int)SendMessage(hdlMsWheel,
                                    uiMsh_MsgScrollLines, 
                                                       0, 
                                                       0);
        }
   }
   else if ( (osversion.dwPlatformId ==
                         VER_PLATFORM_WIN32_NT) &&
             (osversion.dwMajorVersion >= 4) )
   {
      SystemParametersInfo(SPI_GETWHEELSCROLLLINES,
                                          0,
                                    &ucNumLines, 0);
   }
   return(ucNumLines);
}
```



 

 