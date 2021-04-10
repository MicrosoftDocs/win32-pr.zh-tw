---
title: 如何滾動文字
description: 本節說明您可以對應用程式的主視窗程式進行的變更，讓使用者能夠滾動文字。
ms.assetid: ACB4FF34-38EF-4F3D-9395-D48D58A72C0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ef9a2eea9490beac7b6ff5048b70de61eb635f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842747"
---
# <a name="how-to-scroll-text"></a><span data-ttu-id="b5b07-103">如何滾動文字</span><span class="sxs-lookup"><span data-stu-id="b5b07-103">How to Scroll Text</span></span>

<span data-ttu-id="b5b07-104">本節說明您可以對應用程式的主視窗程式進行的變更，讓使用者能夠滾動文字。</span><span class="sxs-lookup"><span data-stu-id="b5b07-104">This section describes the changes you can make to an application's main window procedure to enable a user to scroll text.</span></span> <span data-ttu-id="b5b07-105">本節中的範例會建立並顯示文字字串的陣列，並處理 [**wm \_ HSCROLL**](wm-hscroll.md) 和 [**WM \_ VSCROLL**](wm-vscroll.md) 捲軸訊息，讓使用者可以垂直和水準滾動文字。</span><span class="sxs-lookup"><span data-stu-id="b5b07-105">The example in this section creates and displays an array of text strings, and processes [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) scroll bar messages so that the user can scroll text both vertically and horizontally.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b5b07-106">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="b5b07-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b5b07-107">技術</span><span class="sxs-lookup"><span data-stu-id="b5b07-107">Technologies</span></span>

-   [<span data-ttu-id="b5b07-108">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="b5b07-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b5b07-109">必要條件</span><span class="sxs-lookup"><span data-stu-id="b5b07-109">Prerequisites</span></span>

-   <span data-ttu-id="b5b07-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="b5b07-110">C/C++</span></span>
-   <span data-ttu-id="b5b07-111">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="b5b07-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b5b07-112">指示</span><span class="sxs-lookup"><span data-stu-id="b5b07-112">Instructions</span></span>

### <a name="processing-the-wm_create-message"></a><span data-ttu-id="b5b07-113">處理 WM \_ 建立訊息</span><span class="sxs-lookup"><span data-stu-id="b5b07-113">Processing the WM\_CREATE Message</span></span>

<span data-ttu-id="b5b07-114">滾動單元通常會在處理 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息時設定。</span><span class="sxs-lookup"><span data-stu-id="b5b07-114">Scrolling units are typically set while processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="b5b07-115">以與視窗的裝置內容相關聯的字型尺寸作為滾動單元的基礎， (DC) 很方便。</span><span class="sxs-lookup"><span data-stu-id="b5b07-115">It is convenient to base the scrolling units on the dimensions of the font associated with the window's device context (DC).</span></span> <span data-ttu-id="b5b07-116">若要取得特定 DC 的字型維度，請使用 [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) 函數。</span><span class="sxs-lookup"><span data-stu-id="b5b07-116">To retrieve the font dimensions for a specific DC, use the [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) function.</span></span>

<span data-ttu-id="b5b07-117">在本節的範例中，一個垂直捲動單元相當於字元資料格的高度，加上外部前置。</span><span class="sxs-lookup"><span data-stu-id="b5b07-117">In the example in this section, one vertical scrolling unit is equivalent to the height of a character cell, plus external leading.</span></span> <span data-ttu-id="b5b07-118">一個水準滾動單元相當於字元資料格的平均寬度。</span><span class="sxs-lookup"><span data-stu-id="b5b07-118">One horizontal scrolling unit is equivalent to the average width of a character cell.</span></span> <span data-ttu-id="b5b07-119">因此，除非螢幕字型為固定寬度，否則水準滾動位置不會對應到實際的字元。</span><span class="sxs-lookup"><span data-stu-id="b5b07-119">The horizontal scrolling positions, therefore, do not correspond to actual characters, unless the screen font is fixed-width.</span></span>

### <a name="processing-the-wm_size-message"></a><span data-ttu-id="b5b07-120">處理 WM \_ 大小訊息</span><span class="sxs-lookup"><span data-stu-id="b5b07-120">Processing the WM\_SIZE Message</span></span>

<span data-ttu-id="b5b07-121">處理 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息時，調整滾動範圍和滾動位置以反映工作區的維度以及將顯示的文字行數，是很方便的。</span><span class="sxs-lookup"><span data-stu-id="b5b07-121">When processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, it is convenient to adjust the scrolling range and scrolling position to reflect the dimensions of the client area as well as the number of lines of text that will be displayed.</span></span>

<span data-ttu-id="b5b07-122">[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)函式會設定捲軸的最小和最大位置值、頁面大小和滾動位置。</span><span class="sxs-lookup"><span data-stu-id="b5b07-122">The [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function sets the minimum and maximum position values, the page size, and the scrolling position for a scroll bar.</span></span>

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a><span data-ttu-id="b5b07-123">處理 WM \_ HSCROLL 和 WM \_ VSCROLL 訊息</span><span class="sxs-lookup"><span data-stu-id="b5b07-123">Processing the WM\_HSCROLL and WM\_VSCROLL Messages</span></span>

<span data-ttu-id="b5b07-124">每當使用者按一下捲軸或拖曳捲動方塊時，捲軸就會將 [**wm \_ HSCROLL**](wm-hscroll.md) 和 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送至視窗程式。</span><span class="sxs-lookup"><span data-stu-id="b5b07-124">The scroll bar sends [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to the window procedure whenever the user clicks the scroll bar or drags the scroll box.</span></span> <span data-ttu-id="b5b07-125">**Wm \_ VSCROLL** 和 **wm \_ HSCROLL** 的低序位單字各包含一個要求碼，指出滾動動作的方向和幅度。</span><span class="sxs-lookup"><span data-stu-id="b5b07-125">The low-order words of **WM\_VSCROLL** and **WM\_HSCROLL** each contain a request code that indicates the direction and magnitude of the scrolling action.</span></span>

<span data-ttu-id="b5b07-126">處理 [**wm \_ HSCROLL**](wm-hscroll.md) 和 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息時，會檢查捲軸要求碼並計算滾動遞增。</span><span class="sxs-lookup"><span data-stu-id="b5b07-126">When the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages are processed, the scroll bar request code is examined and the scrolling increment is calculated.</span></span> <span data-ttu-id="b5b07-127">將遞增套用至目前的滾動位置之後，會使用 [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) 函式將視窗滾動至新的位置，並使用 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) 函數來調整捲動方塊的位置。</span><span class="sxs-lookup"><span data-stu-id="b5b07-127">After the increment is applied to the current scrolling position, the window is scrolled to the new position by using the [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) function, and the position of the scroll box is adjusted by using the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span>

<span data-ttu-id="b5b07-128">滾動視窗之後，部分的工作區會成為無效。</span><span class="sxs-lookup"><span data-stu-id="b5b07-128">After a window is scrolled, part of its client area is made invalid.</span></span> <span data-ttu-id="b5b07-129">為了確保更新的區域無效，會使用 [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) 函式來產生 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息。</span><span class="sxs-lookup"><span data-stu-id="b5b07-129">To ensure that the invalid region is updated, the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function is used to generate a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

### <a name="processing-the-wm_paint-message"></a><span data-ttu-id="b5b07-130">處理 WM \_ 油漆訊息</span><span class="sxs-lookup"><span data-stu-id="b5b07-130">Processing the WM\_PAINT Message</span></span>

<span data-ttu-id="b5b07-131">處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時，繪製您想要顯示在視窗的無效部分的文字行是很方便的。</span><span class="sxs-lookup"><span data-stu-id="b5b07-131">When processing the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, it is convenient to draw the lines of text that you want to appear in the invalid portion of the window.</span></span> <span data-ttu-id="b5b07-132">下列範例會使用目前的滾動位置和無效區域的維度來判斷無效區域內的線條範圍，以便顯示它們。</span><span class="sxs-lookup"><span data-stu-id="b5b07-132">The following example uses the current scrolling position and the dimensions of the invalid region to determine the range of lines within the invalid region in order to display them.</span></span>

## <a name="example-of-scrolling-text"></a><span data-ttu-id="b5b07-133">滾動文字的範例</span><span class="sxs-lookup"><span data-stu-id="b5b07-133">Example of Scrolling Text</span></span>

<span data-ttu-id="b5b07-134">下列範例是視窗的視窗程式，可在其工作區中顯示文字。</span><span class="sxs-lookup"><span data-stu-id="b5b07-134">The following example is a window procedure for a window that displays text in its client area.</span></span> <span data-ttu-id="b5b07-135">此範例示範如何從水準和垂直捲動條的輸入中滾動文字以回應輸入。</span><span class="sxs-lookup"><span data-stu-id="b5b07-135">The example demonstrates how to scroll the text in response to input from the horizontal and vertical scroll bars.</span></span>


```C++
#include "strsafe.h"

LRESULT CALLBACK MyTextWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
HDC hdc; 
PAINTSTRUCT ps; 
TEXTMETRIC tm; 
SCROLLINFO si; 
 
// These variables are required to display text. 
static int xClient;     // width of client area 
static int yClient;     // height of client area 
static int xClientMax;  // maximum width of client area 
 
static int xChar;       // horizontal scrolling unit 
static int yChar;       // vertical scrolling unit 
static int xUpper;      // average width of uppercase letters 
 
static int xPos;        // current horizontal scrolling position 
static int yPos;        // current vertical scrolling position 
 
int i;                  // loop counter 
int x, y;               // horizontal and vertical coordinates
 
int FirstLine;          // first line in the invalidated area 
int LastLine;           // last line in the invalidated area 
HRESULT hr;
size_t abcLength;        // length of an abc[] item 

// Create an array of lines to display. 
#define LINES 28 
static TCHAR *abc[] = { 
       TEXT("anteater"),  TEXT("bear"),      TEXT("cougar"), 
       TEXT("dingo"),     TEXT("elephant"),  TEXT("falcon"), 
       TEXT("gazelle"),   TEXT("hyena"),     TEXT("iguana"), 
       TEXT("jackal"),    TEXT("kangaroo"),  TEXT("llama"), 
       TEXT("moose"),     TEXT("newt"),      TEXT("octopus"), 
       TEXT("penguin"),   TEXT("quail"),     TEXT("rat"), 
       TEXT("squid"),     TEXT("tortoise"),  TEXT("urus"), 
       TEXT("vole"),      TEXT("walrus"),    TEXT("xylophone"), 
       TEXT("yak"),       TEXT("zebra"),
       TEXT("This line contains words, but no character. Go figure."),
       TEXT("")
     }; 
 
switch (uMsg) 
{ 
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hwnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hwnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0; 
 
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
        return 0; 
    case WM_HSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;

        // Save the position for comparison later on.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;
        switch (LOWORD (wParam))
        {
        // User clicked the left arrow.
        case SB_LINELEFT: 
            si.nPos -= 1;
            break;
              
        // User clicked the right arrow.
        case SB_LINERIGHT: 
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft left of the scroll box.
        case SB_PAGELEFT:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft right of the scroll box.
        case SB_PAGERIGHT:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK: 
            si.nPos = si.nTrackPos;
            break;
              
        default :
            break;
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_HORZ, &si, TRUE);
        GetScrollInfo (hwnd, SB_HORZ, &si);
         
        // If the position has changed, scroll the window.
        if (si.nPos != xPos)
        {
            ScrollWindow(hwnd, xChar * (xPos - si.nPos), 0, NULL, NULL);
        }

        return 0;
         
    case WM_VSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hwnd, SB_VERT, &si);

        // Save the position for comparison later on.
        yPos = si.nPos;
        switch (LOWORD (wParam))
        {

        // User clicked the HOME keyboard key.
        case SB_TOP:
            si.nPos = si.nMin;
            break;
              
        // User clicked the END keyboard key.
        case SB_BOTTOM:
            si.nPos = si.nMax;
            break;
              
        // User clicked the top arrow.
        case SB_LINEUP:
            si.nPos -= 1;
            break;
              
        // User clicked the bottom arrow.
        case SB_LINEDOWN:
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft above the scroll box.
        case SB_PAGEUP:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft below the scroll box.
        case SB_PAGEDOWN:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK:
            si.nPos = si.nTrackPos;
            break;
              
        default:
            break; 
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_VERT, &si, TRUE);
        GetScrollInfo (hwnd, SB_VERT, &si);

        // If the position has changed, scroll window and update it.
        if (si.nPos != yPos)
        {                    
            ScrollWindow(hwnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
            UpdateWindow (hwnd);
        }

        return 0;
         
    case WM_PAINT :
        // Prepare the window for painting.
        hdc = BeginPaint (hwnd, &ps);

        // Get vertical scroll bar position.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_POS;
        GetScrollInfo (hwnd, SB_VERT, &si);
        yPos = si.nPos;

        // Get horizontal scroll bar position.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;

        // Find painting limits.
        FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
        LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
        for (i = FirstLine; i <= LastLine; i++)
        {
            x = xChar * (1 - xPos);
            y = yChar * (i - yPos);
              
            // Note that "55" in the following depends on the 
            // maximum size of an abc[] item. Also, you must include
            // strsafe.h to use the StringCchLength function.
            hr = StringCchLength(abc[i], 55, &abcLength);
            if ((FAILED(hr))|(abcLength == NULL))
            {
                //
                // TODO: write error handler
                //
            }

            // Write a line of text to the client area.
            TextOut(hdc, x, y, abc[i], abcLength); 
        }

        // Indicate that painting is finished.
        EndPaint (hwnd, &ps);
        return 0;
         
    case WM_DESTROY :
        PostQuitMessage (0);
        return 0;
    }

    return DefWindowProc (hwnd, uMsg, wParam, lParam);
}
```



## <a name="related-topics"></a><span data-ttu-id="b5b07-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5b07-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5b07-137">使用捲軸</span><span class="sxs-lookup"><span data-stu-id="b5b07-137">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="b5b07-138">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="b5b07-138">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 