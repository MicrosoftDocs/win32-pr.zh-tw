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
ms.openlocfilehash: e6450a3169588b3072d1fee271f4890a7cdeafd2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023368"
---
# <a name="using-carets"></a><span data-ttu-id="08b10-120">使用游標</span><span class="sxs-lookup"><span data-stu-id="08b10-120">Using Carets</span></span>

<span data-ttu-id="08b10-121">本節包含下列工作的程式碼範例：</span><span class="sxs-lookup"><span data-stu-id="08b10-121">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="08b10-122">建立及顯示插入號</span><span class="sxs-lookup"><span data-stu-id="08b10-122">Creating and Displaying a Caret</span></span>](#creating-and-displaying-a-caret)
-   [<span data-ttu-id="08b10-123">隱藏插入號</span><span class="sxs-lookup"><span data-stu-id="08b10-123">Hiding a Caret</span></span>](#hiding-a-caret)
-   [<span data-ttu-id="08b10-124">終結插入號</span><span class="sxs-lookup"><span data-stu-id="08b10-124">Destroying a Caret</span></span>](#destroying-a-caret)
-   [<span data-ttu-id="08b10-125">調整閃爍時間</span><span class="sxs-lookup"><span data-stu-id="08b10-125">Adjusting the Blink Time</span></span>](#adjusting-the-blink-time)
-   [<span data-ttu-id="08b10-126">處理鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="08b10-126">Processing Keyboard Input</span></span>](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a><span data-ttu-id="08b10-127">建立及顯示插入號</span><span class="sxs-lookup"><span data-stu-id="08b10-127">Creating and Displaying a Caret</span></span>

<span data-ttu-id="08b10-128">收到鍵盤焦點時，視窗應該建立並顯示插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-128">Upon receiving the keyboard focus, the window should create and display the caret.</span></span> <span data-ttu-id="08b10-129">使用 [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) 函式在指定的視窗中建立插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-129">Use the [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) function to create a caret in the given window.</span></span> <span data-ttu-id="08b10-130">然後，您可以呼叫 [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) 來設定插入號和 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) 的目前位置，使插入號變成可見。</span><span class="sxs-lookup"><span data-stu-id="08b10-130">You can then call [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) to set the current position of the caret and [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) to make the caret visible.</span></span>

<span data-ttu-id="08b10-131">系統會將 [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) 訊息傳送至接收鍵盤焦點的視窗; 因此，應用程式應該在處理此訊息時建立並顯示插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-131">The system sends the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message to the window receiving keyboard focus; therefore, an application should create and display the caret while processing this message.</span></span>


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



<span data-ttu-id="08b10-132">若要根據點陣圖建立插入點，您必須在使用 [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)時指定點陣圖控制碼。</span><span class="sxs-lookup"><span data-stu-id="08b10-132">To create a caret based on a bitmap, you must specify a bitmap handle when using [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span></span> <span data-ttu-id="08b10-133">您可以使用圖形應用程式來建立點陣圖，並使用資源編譯器將點陣圖新增至您的應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="08b10-133">You can use a graphics application to create the bitmap and a resource compiler to add the bitmap to your application's resources.</span></span> <span data-ttu-id="08b10-134">然後，您的應用程式就可以使用 [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) 函式來載入點陣圖控制碼。</span><span class="sxs-lookup"><span data-stu-id="08b10-134">Your application can then use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap handle.</span></span> <span data-ttu-id="08b10-135">例如，您可以使用下列幾行來取代上述範例中的 **CreateCaret** 行，以建立點陣圖插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-135">For example, you could replace the **CreateCaret** line in the preceding example with the following lines to create a bitmap caret.</span></span>


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



<span data-ttu-id="08b10-136">或者，您可以使用 [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) 或 [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) 函式來取出插入號點陣圖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="08b10-136">Alternatively, you can use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) or [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) function to retrieve the handle of the caret bitmap.</span></span> <span data-ttu-id="08b10-137">如需點陣圖的詳細資訊，請參閱 [點陣圖](/windows/desktop/gdi/bitmaps)。</span><span class="sxs-lookup"><span data-stu-id="08b10-137">For more information about bitmaps, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

<span data-ttu-id="08b10-138">如果您的應用程式指定點陣圖控制碼， [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) 會忽略寬度和高度參數。</span><span class="sxs-lookup"><span data-stu-id="08b10-138">If your application specifies a bitmap handle, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignores the width and height parameters.</span></span> <span data-ttu-id="08b10-139">點陣圖會定義插入號的大小。</span><span class="sxs-lookup"><span data-stu-id="08b10-139">The bitmap defines the size of the caret.</span></span>

## <a name="hiding-a-caret"></a><span data-ttu-id="08b10-140">隱藏插入號</span><span class="sxs-lookup"><span data-stu-id="08b10-140">Hiding a Caret</span></span>

<span data-ttu-id="08b10-141">每當您的應用程式在處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)以外的訊息時重繪畫面時，就必須使用 [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) 函式來隱藏插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-141">Whenever your application redraws a screen while processing a message other than [**WM\_PAINT**](/windows/desktop/gdi/wm-paint), it must make the caret invisible by using the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function.</span></span> <span data-ttu-id="08b10-142">當您的應用程式完成繪圖時，請使用 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) 函數重新顯示插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-142">When your application is finished drawing, redisplay the caret by using the [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) function.</span></span> <span data-ttu-id="08b10-143">如果您的應用程式處理 **WM \_ 油漆** 訊息，則不需要隱藏並重新顯示插入號，因為此函式會自動執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="08b10-143">If your application processes the **WM\_PAINT** message, it is not necessary to hide and redisplay the caret, because this function does this automatically.</span></span>

<span data-ttu-id="08b10-144">下列程式碼範例示範如何讓您的應用程式在螢幕上繪製字元時，以及處理 [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) 訊息時，隱藏插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-144">The following code sample shows how to have your application hide the caret while drawing a character on the screen and while processing the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


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



<span data-ttu-id="08b10-145">如果您的應用程式多次呼叫 [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) 函式，但未呼叫 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)，將不會顯示插入號，除非應用程式也會呼叫相同次數的 **ShowCaret** 。</span><span class="sxs-lookup"><span data-stu-id="08b10-145">If your application calls the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function several times without calling [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), the caret will not be displayed until the application also calls **ShowCaret** the same number of times.</span></span>

## <a name="destroying-a-caret"></a><span data-ttu-id="08b10-146">終結插入號</span><span class="sxs-lookup"><span data-stu-id="08b10-146">Destroying a Caret</span></span>

<span data-ttu-id="08b10-147">當視窗失去鍵盤焦點時，系統會將 [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="08b10-147">When a window loses the keyboard focus, the system sends the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message to the window.</span></span> <span data-ttu-id="08b10-148">您的應用程式應該使用 [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) 函式，在處理此訊息時終結插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-148">Your application should destroy the caret while processing this message by using the [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) function.</span></span> <span data-ttu-id="08b10-149">下列程式碼示範如何在不再具有鍵盤焦點的視窗中終結插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-149">The following code shows how to destroy a caret in a window that no longer has the keyboard focus.</span></span>


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a><span data-ttu-id="08b10-150">調整閃爍時間</span><span class="sxs-lookup"><span data-stu-id="08b10-150">Adjusting the Blink Time</span></span>

<span data-ttu-id="08b10-151">在16位的 Windows 中，以 Windows 為基礎的應用程式可以呼叫 [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) 函式來儲存目前的閃爍時間，然後呼叫 [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) 函式來調整在它處理 [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) 訊息時的閃爍時間。</span><span class="sxs-lookup"><span data-stu-id="08b10-151">In 16-bit Windows, a Windows-based application could call the [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) function to save the current blink time, then call the [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function to adjust the blink time during its processing of the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="08b10-152">應用程式會在處理 [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)訊息時呼叫 **SetCaretBlinkTime** ，以還原使用其他應用程式的已儲存閃爍時間。</span><span class="sxs-lookup"><span data-stu-id="08b10-152">The application would restore the saved blink time for the use of other applications by calling **SetCaretBlinkTime** during its processing of the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="08b10-153">不過，這項技術無法在多執行緒環境中運作。</span><span class="sxs-lookup"><span data-stu-id="08b10-153">However, this technique does not work in multithreaded environments.</span></span> <span data-ttu-id="08b10-154">具體而言，停用某個應用程式並不會與啟用另一個應用程式同步處理，因此，如果某個應用程式停止回應，仍然可以啟動另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="08b10-154">Specifically, the deactivation of one application is not synchronized with the activation of another application, so that if one application hangs, another application can still be activated.</span></span>

<span data-ttu-id="08b10-155">應用程式應該遵守使用者所選擇的閃爍時間。</span><span class="sxs-lookup"><span data-stu-id="08b10-155">Applications should respect the blink time chosen by the user.</span></span> <span data-ttu-id="08b10-156">[**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime)函式只能由允許使用者設定閃爍時間的應用程式呼叫。</span><span class="sxs-lookup"><span data-stu-id="08b10-156">The [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function should only be called by an application that allows the user to set the blink time.</span></span>

## <a name="processing-keyboard-input"></a><span data-ttu-id="08b10-157">處理鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="08b10-157">Processing Keyboard Input</span></span>

<span data-ttu-id="08b10-158">下列範例示範如何在簡單的文字編輯器中使用插入號。</span><span class="sxs-lookup"><span data-stu-id="08b10-158">The following example demonstrates how to use a caret in a simple text editor.</span></span> <span data-ttu-id="08b10-159">此範例會在使用者輸入可列印的字元時，更新插入號位置，並使用各種按鍵來移動整個工作區。</span><span class="sxs-lookup"><span data-stu-id="08b10-159">The example updates the caret position as the user types printable characters and uses various keys to move through the client area.</span></span>


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



 

 