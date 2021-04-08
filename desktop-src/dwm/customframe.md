---
title: 使用 DWM 的自訂視窗框架
description: 本主題示範如何使用桌面視窗管理員 (DWM) Api 來為您的應用程式建立自訂視窗框架。
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- 桌面視窗管理員 (DWM) 自訂視窗框架
- DWM (桌面視窗管理員) 、自訂視窗框架
- 自訂視窗框架
- 移除標準框架
- 擴充用戶端框架
- 桌面視窗管理員 (DWM) ，擴充用戶端框架
- DWM (桌面視窗管理員) ，擴充用戶端框架
- 桌面視窗管理員 (DWM) ，移除標準框架
- DWM (桌面視窗管理員) ，移除標準框架
- 桌面視窗管理員 (DWM) ，在擴充的框架中繪製
- DWM (桌面視窗管理員) ，在擴充的框架中繪製
- 在擴充框架中繪圖
- 點擊測試
- 桌面視窗管理員 (DWM) 、點擊測試
- DWM (桌面視窗管理員) 、點擊測試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024061"
---
# <a name="custom-window-frame-using-dwm"></a>使用 DWM 的自訂視窗框架

本主題示範如何使用桌面視窗管理員 (DWM) Api 來為您的應用程式建立自訂視窗框架。

-   [簡介](#introduction)
-   [擴充用戶端框架](#extending-the-client-frame)
-   [移除標準框架](#removing-the-standard-frame)
-   [展開框架視窗中的繪圖](#drawing-in-the-extended-frame-window)
-   [啟用自訂框架的點擊測試](#enabling-hit-testing-for-the-custom-frame)
-   [附錄 A：範例視窗程式](#appendix-a-sample-window-procedure)
-   [附錄 B：繪製標題標題](#appendix-b-painting-the-caption-title)
-   [附錄 C： HitTestNCA 函數](#appendix-c-hittestnca-function)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

在 Windows Vista （含）以後版本中，應用程式視窗的非工作區的外觀 (標題列、圖示、視窗框線和標題按鈕) 由 DWM 控制。 使用 DWM Api，您可以變更 DWM 呈現視窗框架的方式。

DWM Api 的其中一項功能，就是將應用程式框架擴充到工作區的能力。 這可讓您將用戶端 UI 元素（例如工具列）整合到框架中，讓 UI 控制項在應用程式 UI 中有更顯著的位置。 例如，windows Vista 上的 Windows Internet Explorer 7 藉由擴充框架頂端來將導覽列整合到視窗框架，如下列螢幕擷取畫面所示。

![整合至視窗框架的導覽列。](images/ie7-extendedborder-boxed.png)

延伸視窗框架的功能也可讓您建立自訂框架，同時維持視窗的外觀和操作。 例如，在提供標準的最小化、最大化和關閉標題按鈕時，Microsoft Office Word 2007 會在自訂框架內繪製 Office 按鈕和快速存取工具列，如下列螢幕擷取畫面所示。

![word 2007 中的 office 按鈕和快速存取工具列](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a>擴充用戶端框架

[**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea)函式會公開將框架擴充至工作區的功能。 若要擴充框架，請將目標視窗的控制碼以及邊界內凹值傳遞給 **DwmExtendFrameIntoClientArea**。 邊界內凹值決定在視窗的四邊擴充框架的距離。

下列程式碼示範如何使用 [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) 來擴充框架。


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



請注意，框架延伸是在 [**wm \_ 啟動**](/windows/desktop/inputdev/wm-activate) 訊息內進行，而不是在 [**wm \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息中。 這可確保當視窗處於預設大小且最大化時，會適當地處理框架延伸。

下圖顯示左) 的標準視窗框架 (，以及右邊)  (擴充的相同視窗框架。 使用先前的程式碼範例和預設的 Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)背景 (色彩 \_ 視窗 + 1) 來擴充框架。

![標準 (左) 的螢幕擷取畫面，以及白色背景的擴充框架 (右) ](images/white-sidebyside.png)

這兩個視窗之間的視覺化差異很微妙。 兩者之間唯一的差異在於右邊的視窗中遺漏了左邊視窗中用戶端區域的黑色黑色線條框線。 遺漏框線的原因是它會併入擴充框架中，但用戶端區域的其餘部分則否。 若要顯示擴充的框架，每個延伸框架邊的基礎區域都必須有 Alpha 值為0的圖元資料。 用戶端區域周圍的黑色框線具有圖元資料，其中所有色彩值 (紅色、綠色、藍色和 Alpha) 都會設定為0。 背景的其餘部分未將 Alpha 值設定為0，因此不會顯示擴充框架的其餘部分。

確保擴充框架可見的最簡單方式，就是將整個用戶端區域繪製為黑色。 若要完成此動作，請將 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)或 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 *HBRBACKGROUND* 成員初始化為股票黑色筆刷的控點 \_ 。 下圖顯示相同的標準框架 (左) 和延伸框架 () 先前顯示的。 不過這次， *hbrBackground* 會設定為 \_ 從 [**GETSTOCKOBJECT**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) 函數取得的黑色筆刷控制碼。

![標準 (左) 的螢幕擷取畫面，以及黑色背景的擴充框架 (右) ](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a>移除標準框架

擴充應用程式的框架並使其顯示之後，您就可以移除標準框架。 移除標準框架可讓您控制框架各側邊的寬度，而不只是擴充標準框架。

若要移除標準視窗框架，您必須處理 [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) 訊息（特別是當其 *wParam* 值為 **TRUE** ，且傳回值為0時）。 如此一來，您的應用程式就會使用整個視窗區域做為工作區，以移除標準框架。

在需要調整用戶端區域的大小時，才看不到處理 [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) 訊息的結果。 在這段時間內，視窗的初始視圖會顯示標準框架和延伸框線。 若要解決此情況，您必須調整視窗的大小，或執行在建立視窗時起始 **WM \_ NCCALCSIZE** 訊息的動作。 您可以使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函式來移動視窗並調整其大小，以達成此目的。 下列程式碼示範如何呼叫 **SetWindowPos** ，以強制使用目前的視窗矩形屬性和 SWP FRAMECHANGED 旗標來傳送 **WM \_ NCCALCSIZE** 訊息 \_ 。


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



下圖顯示標準框架 (左) ，以及不含標準框架的新擴充框架 (右) 。

![標準框架的螢幕擷取畫面 (左) 和自訂框架 (right) ](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a>展開框架視窗中的繪圖

藉由移除標準框架，您會失去應用程式圖示和標題的自動繪製。 若要將這些專案加回您的應用程式，您必須自行繪製。 若要這樣做，請先查看您的工作區發生的變更。

移除標準框架之後，您的工作區現在會包含整個視窗，包括延伸框架。 這包括繪製標題按鈕的區域。 在下列並排比較中，標準框架和自訂延伸框架的工作區會以紅色反白顯示。 標準框架視窗的工作區 (左) 是黑色區域。 在擴充框架視窗上 (右) ，工作區是整個視窗。

![標準和自訂框架上紅色反白顯示用戶端區域的螢幕擷取畫面](images/clientarea-sidebyside.png)

因為整個視窗是您的工作區，所以您可以直接在擴充框架中繪製您想要的內容。 若要將標題加入至您的應用程式，只需在適當的區域中繪製文字。 下圖顯示在自訂標題框上繪製的主題文字。 標題是使用 [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) 函式來繪製。 若要查看繪製標題的程式碼，請參閱 [附錄 B：繪製標題標題](#appendix-b-painting-the-caption-title)。

![具有標題的自訂框架螢幕擷取畫面](images/custom-caption-title.png)

> [!Note]  
> 在自訂框架中繪圖時，請小心放置 UI 控制項。 由於整個視窗是您的用戶端區域，因此，如果您不想要讓 UI 控制項在擴充框架中出現，您必須調整每個畫面格寬度的 UI 控制項位置。

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a>啟用自訂框架的點擊測試

移除標準框架的副作用是，會失去預設的調整大小和移動行為。 為了讓您的應用程式正確地模擬標準視窗行為，您必須執行邏輯來處理標題按鈕的點擊測試和框架調整大小/移動。

針對標題按鈕點擊測試，DWM 提供 [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) 函數。 若要在自訂框架案例中適當地點擊測試標題按鈕，應先將訊息傳遞至 **DwmDefWindowProc** 進行處理。 如果處理訊息， **DwmDefWindowProc** 會傳回 **TRUE** ，否則傳回 **FALSE** 。 如果訊息不是由 **DwmDefWindowProc** 處理，則您的應用程式應該處理訊息本身，或將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。

針對調整大小和移動的框架，您的應用程式必須提供點擊測試邏輯，並處理框架點擊測試訊息。 框架點擊測試訊息會透過 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 訊息傳送給您，即使您的應用程式在不使用標準框架的情況下，也會建立自訂框架。 下列程式碼示範在 [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc)不處理 **WM \_ NCHITTEST** 訊息時，如何處理該訊息。 若要查看所呼叫函式的程式碼 `HitTestNCA` ，請參閱 [附錄 C： HitTestNCA 函數](#appendix-c-hittestnca-function)。


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a>附錄 A：範例視窗程式

下列程式碼範例示範視窗程式和其支援的背景工作函式，用來建立自訂的框架應用程式。


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a>附錄 B：繪製標題標題

下列程式碼示範如何在擴充框架上繪製標題標題。 您必須從 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) 和 [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) 呼叫中呼叫此函式。


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a>附錄 C： HitTestNCA 函數

下列程式碼顯示 `HitTestNCA` 用於 [啟用自訂框架之點擊測試](#enabling-hit-testing-for-the-custom-frame)的函數。 當 [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc)未處理訊息時，此函式會處理 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest)的點擊測試邏輯。


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[桌面視窗管理員概觀](dwm-overview.md)
</dt> </dl>

 

 