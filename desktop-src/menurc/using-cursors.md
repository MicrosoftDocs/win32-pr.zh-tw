---
title: 使用資料指標
description: 本節提供的程式碼範例會示範如何執行與資料指標相關的工作。
ms.assetid: eab7b781-783e-4fc5-868d-6ff773c40a21
keywords:
- 資源，資料指標
- 資料指標，自訂
- 自訂資料指標
- 沙漏游標
- 資料指標，建立
- 資料指標，沙漏
- 建立資料指標
- 終結資料指標
- 顯示資料指標
- 將資料指標
- 資料指標，終結
- 資料指標，顯示
- 資料指標，將
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cf681fd17f3e79e4559e9936be232ae09f8453
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327123"
---
# <a name="using-cursors"></a><span data-ttu-id="311d9-116">使用資料指標</span><span class="sxs-lookup"><span data-stu-id="311d9-116">Using Cursors</span></span>

<span data-ttu-id="311d9-117">本節將討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="311d9-117">This section discusses the following topics.</span></span>

-   [<span data-ttu-id="311d9-118">建立資料指標</span><span class="sxs-lookup"><span data-stu-id="311d9-118">Creating a Cursor</span></span>](#creating-a-cursor)
-   [<span data-ttu-id="311d9-119">顯示資料指標</span><span class="sxs-lookup"><span data-stu-id="311d9-119">Displaying a Cursor</span></span>](#displaying-a-cursor)
-   [<span data-ttu-id="311d9-120">將資料指標</span><span class="sxs-lookup"><span data-stu-id="311d9-120">Confining a Cursor</span></span>](#confining-a-cursor)
-   [<span data-ttu-id="311d9-121">使用資料指標函數建立 Mousetrap</span><span class="sxs-lookup"><span data-stu-id="311d9-121">Using Cursor Functions to Create a Mousetrap</span></span>](#using-cursor-functions-to-create-a-mousetrap)
-   [<span data-ttu-id="311d9-122">使用鍵盤移動游標</span><span class="sxs-lookup"><span data-stu-id="311d9-122">Using the Keyboard to Move the Cursor</span></span>](#using-the-keyboard-to-move-the-cursor)

## <a name="creating-a-cursor"></a><span data-ttu-id="311d9-123">建立資料指標</span><span class="sxs-lookup"><span data-stu-id="311d9-123">Creating a Cursor</span></span>

<span data-ttu-id="311d9-124">下列範例會建立兩個數據指標控制碼：一個適用于標準沙漏游標，另一個用於自訂資料指標，其中包含做為應用程式資源定義檔中的資源。</span><span class="sxs-lookup"><span data-stu-id="311d9-124">The following example creates two cursor handles: one for the standard hourglass cursor and one for a custom cursor included as a resource in the application's resource-definition file.</span></span>


```
HINSTANCE hinst;            // handle to current instance 
HCURSOR hCurs1, hCurs2;     // cursor handles 
 
// Create a standard hourglass cursor. 
 
hCurs1 = LoadCursor(NULL, IDC_WAIT); 
 
// Create a custom cursor based on a resource. 
 
hCurs2 = LoadCursor(hinst, MAKEINTRESOURCE(240)); 
```



<span data-ttu-id="311d9-125">您應該將自訂資料指標作為資源來執行。</span><span class="sxs-lookup"><span data-stu-id="311d9-125">You should implement custom cursors as resources.</span></span> <span data-ttu-id="311d9-126">您可以使用 [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)、 [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)或 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) 函數來避免裝置的相依性，以簡化當地語系化，並讓應用程式共用資料指標設計，而不是在執行時間建立資料指標。</span><span class="sxs-lookup"><span data-stu-id="311d9-126">Rather than create the cursors at run time, use the [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea), or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function to avoid device dependence, to simplify localization, and to enable applications to share cursor designs.</span></span>

<span data-ttu-id="311d9-127">下列範例會在執行時間使用 [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) 函式來建立自訂資料指標。</span><span class="sxs-lookup"><span data-stu-id="311d9-127">The following example uses the [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) function to create a custom cursor at run time.</span></span> <span data-ttu-id="311d9-128">此範例包含在此範例中，以說明系統解釋資料指標遮罩的方式。</span><span class="sxs-lookup"><span data-stu-id="311d9-128">The example is included here to illustrate how the system interprets cursor masks.</span></span>


```
HINSTANCE hinst;            // handle to current instance  
HCURSOR hCurs1, hCurs2;     // cursor handles 
 
HCURSOR hCurs3;             // cursor handle 
 
// Yin-shaped cursor AND mask 
 
BYTE ANDmaskCursor[] = 
{ 
    0xFF, 0xFC, 0x3F, 0xFF,   // line 1 
    0xFF, 0xC0, 0x1F, 0xFF,   // line 2 
    0xFF, 0x00, 0x3F, 0xFF,   // line 3 
    0xFE, 0x00, 0xFF, 0xFF,   // line 4 
 
    0xF7, 0x01, 0xFF, 0xFF,   // line 5 
    0xF0, 0x03, 0xFF, 0xFF,   // line 6 
    0xF0, 0x03, 0xFF, 0xFF,   // line 7 
    0xE0, 0x07, 0xFF, 0xFF,   // line 8 
 
    0xC0, 0x07, 0xFF, 0xFF,   // line 9 
    0xC0, 0x0F, 0xFF, 0xFF,   // line 10 
    0x80, 0x0F, 0xFF, 0xFF,   // line 11 
    0x80, 0x0F, 0xFF, 0xFF,   // line 12 
 
    0x80, 0x07, 0xFF, 0xFF,   // line 13 
    0x00, 0x07, 0xFF, 0xFF,   // line 14 
    0x00, 0x03, 0xFF, 0xFF,   // line 15 
    0x00, 0x00, 0xFF, 0xFF,   // line 16 
 
    0x00, 0x00, 0x7F, 0xFF,   // line 17 
    0x00, 0x00, 0x1F, 0xFF,   // line 18 
    0x00, 0x00, 0x0F, 0xFF,   // line 19 
    0x80, 0x00, 0x0F, 0xFF,   // line 20 
 
    0x80, 0x00, 0x07, 0xFF,   // line 21 
    0x80, 0x00, 0x07, 0xFF,   // line 22 
    0xC0, 0x00, 0x07, 0xFF,   // line 23 
    0xC0, 0x00, 0x0F, 0xFF,   // line 24 
 
    0xE0, 0x00, 0x0F, 0xFF,   // line 25 
    0xF0, 0x00, 0x1F, 0xFF,   // line 26 
    0xF0, 0x00, 0x1F, 0xFF,   // line 27 
    0xF8, 0x00, 0x3F, 0xFF,   // line 28 
 
    0xFE, 0x00, 0x7F, 0xFF,   // line 29 
    0xFF, 0x00, 0xFF, 0xFF,   // line 30 
    0xFF, 0xC3, 0xFF, 0xFF,   // line 31 
    0xFF, 0xFF, 0xFF, 0xFF    // line 32 
};
 
// Yin-shaped cursor XOR mask 
 
BYTE XORmaskCursor[] = 
{ 
    0x00, 0x00, 0x00, 0x00,   // line 1 
    0x00, 0x03, 0xC0, 0x00,   // line 2 
    0x00, 0x3F, 0x00, 0x00,   // line 3 
    0x00, 0xFE, 0x00, 0x00,   // line 4 
 
    0x0E, 0xFC, 0x00, 0x00,   // line 5 
    0x07, 0xF8, 0x00, 0x00,   // line 6 
    0x07, 0xF8, 0x00, 0x00,   // line 7 
    0x0F, 0xF0, 0x00, 0x00,   // line 8 
 
    0x1F, 0xF0, 0x00, 0x00,   // line 9 
    0x1F, 0xE0, 0x00, 0x00,   // line 10 
    0x3F, 0xE0, 0x00, 0x00,   // line 11 
    0x3F, 0xE0, 0x00, 0x00,   // line 12 
 
    0x3F, 0xF0, 0x00, 0x00,   // line 13 
    0x7F, 0xF0, 0x00, 0x00,   // line 14 
    0x7F, 0xF8, 0x00, 0x00,   // line 15 
    0x7F, 0xFC, 0x00, 0x00,   // line 16 
 
    0x7F, 0xFF, 0x00, 0x00,   // line 17 
    0x7F, 0xFF, 0x80, 0x00,   // line 18 
    0x7F, 0xFF, 0xE0, 0x00,   // line 19 
    0x3F, 0xFF, 0xE0, 0x00,   // line 20 
 
    0x3F, 0xC7, 0xF0, 0x00,   // line 21 
    0x3F, 0x83, 0xF0, 0x00,   // line 22 
    0x1F, 0x83, 0xF0, 0x00,   // line 23 
    0x1F, 0x83, 0xE0, 0x00,   // line 24 
 
    0x0F, 0xC7, 0xE0, 0x00,   // line 25 
    0x07, 0xFF, 0xC0, 0x00,   // line 26 
    0x07, 0xFF, 0xC0, 0x00,   // line 27 
    0x01, 0xFF, 0x80, 0x00,   // line 28 
 
    0x00, 0xFF, 0x00, 0x00,   // line 29 
    0x00, 0x3C, 0x00, 0x00,   // line 30 
    0x00, 0x00, 0x00, 0x00,   // line 31 
    0x00, 0x00, 0x00, 0x00    // line 32 
};
 
// Create a custom cursor at run time. 
 
hCurs3 = CreateCursor( hinst,   // app. instance 
             19,                // horizontal position of hot spot 
             2,                 // vertical position of hot spot 
             32,                // cursor width 
             32,                // cursor height 
             ANDmaskCursor,     // AND mask 
             XORmaskCursor );   // XOR mask 
```



<span data-ttu-id="311d9-129">若要建立資料指標， [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) 會將下列事實資料表套用至 **and** 和 **XOR** 遮罩。</span><span class="sxs-lookup"><span data-stu-id="311d9-129">To create the cursor, [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) applies the following truth table to the **AND** and **XOR** masks.</span></span>



| <span data-ttu-id="311d9-130">和 mask</span><span class="sxs-lookup"><span data-stu-id="311d9-130">AND mask</span></span> | <span data-ttu-id="311d9-131">XOR 遮罩</span><span class="sxs-lookup"><span data-stu-id="311d9-131">XOR mask</span></span> | <span data-ttu-id="311d9-132">顯示</span><span class="sxs-lookup"><span data-stu-id="311d9-132">Display</span></span>        |
|----------|----------|----------------|
| <span data-ttu-id="311d9-133">0</span><span class="sxs-lookup"><span data-stu-id="311d9-133">0</span></span>        | <span data-ttu-id="311d9-134">0</span><span class="sxs-lookup"><span data-stu-id="311d9-134">0</span></span>        | <span data-ttu-id="311d9-135">黑色</span><span class="sxs-lookup"><span data-stu-id="311d9-135">Black</span></span>          |
| <span data-ttu-id="311d9-136">0</span><span class="sxs-lookup"><span data-stu-id="311d9-136">0</span></span>        | <span data-ttu-id="311d9-137">1</span><span class="sxs-lookup"><span data-stu-id="311d9-137">1</span></span>        | <span data-ttu-id="311d9-138">白色</span><span class="sxs-lookup"><span data-stu-id="311d9-138">White</span></span>          |
| <span data-ttu-id="311d9-139">1</span><span class="sxs-lookup"><span data-stu-id="311d9-139">1</span></span>        | <span data-ttu-id="311d9-140">0</span><span class="sxs-lookup"><span data-stu-id="311d9-140">0</span></span>        | <span data-ttu-id="311d9-141">畫面</span><span class="sxs-lookup"><span data-stu-id="311d9-141">Screen</span></span>         |
| <span data-ttu-id="311d9-142">1</span><span class="sxs-lookup"><span data-stu-id="311d9-142">1</span></span>        | <span data-ttu-id="311d9-143">1</span><span class="sxs-lookup"><span data-stu-id="311d9-143">1</span></span>        | <span data-ttu-id="311d9-144">反向畫面</span><span class="sxs-lookup"><span data-stu-id="311d9-144">Reverse screen</span></span> |



 

<span data-ttu-id="311d9-145">如需詳細資訊，請參閱 [點陣圖](/windows/desktop/gdi/bitmaps)。</span><span class="sxs-lookup"><span data-stu-id="311d9-145">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

<span data-ttu-id="311d9-146">在關閉之前，您必須使用 [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) 函式來終結您使用 [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor)所建立的任何資料指標。</span><span class="sxs-lookup"><span data-stu-id="311d9-146">Before closing, you must use the [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) function to destroy any cursors you created with [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor).</span></span> <span data-ttu-id="311d9-147">不需要終結其他函數所建立的資料指標。</span><span class="sxs-lookup"><span data-stu-id="311d9-147">It is not necessary to destroy cursors created by other functions.</span></span>

## <a name="displaying-a-cursor"></a><span data-ttu-id="311d9-148">顯示資料指標</span><span class="sxs-lookup"><span data-stu-id="311d9-148">Displaying a Cursor</span></span>

<span data-ttu-id="311d9-149">系統會自動顯示類別游標 (與資料指標指向的視窗相關聯的資料指標) 。</span><span class="sxs-lookup"><span data-stu-id="311d9-149">The system automatically displays the class cursor (the cursor associated with the window to which the cursor is pointing).</span></span> <span data-ttu-id="311d9-150">您可以在註冊視窗類別時指派類別資料指標。</span><span class="sxs-lookup"><span data-stu-id="311d9-150">You can assign a class cursor while registering a window class.</span></span> <span data-ttu-id="311d9-151">下列範例將說明這種情況，方法是將資料指標控制碼指派給 *wc* 參數所識別之 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **hCursor** 成員。</span><span class="sxs-lookup"><span data-stu-id="311d9-151">The following example illustrates this by assigning a cursor handle to the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure identified by the *wc* parameter.</span></span>


```
WNDCLASS  wc; 
 
// Fill the window class structure with parameters that 
// describe the main window. 
 
wc.style = NULL;                        // class style(s) 
wc.lpfnWndProc = (WNDPROC) MainWndProc; // window procedure 
wc.cbClsExtra = 0;           // no per-class extra data 
wc.cbWndExtra = 0;           // no per-window extra data 
wc.hInstance = hinst;        // application that owns the class 
wc.hIcon = LoadIcon(NULL, IDI_APPLICATION);     // class icon 
wc.hCursor = LoadCursor(hinst, MAKEINTRESOURCE(230)); // class cursor 
wc.hbrBackground = GetStockObject(WHITE_BRUSH); // class background 
wc.lpszMenuName =  "GenericMenu";               // class menu 
wc.lpszClassName = "GenericWClass"              // class name 
 
// Register the window class. 
 
return RegisterClass(&wc); 
```



<span data-ttu-id="311d9-152">註冊視窗類別之後，在應用程式的資源定義檔中，230所識別的資料指標就是所有以類別為基礎之視窗的預設資料指標。</span><span class="sxs-lookup"><span data-stu-id="311d9-152">When the window class is registered, the cursor identified by 230 in the application's resource-definition file is the default cursor for all windows based on the class.</span></span>

<span data-ttu-id="311d9-153">您的應用程式可以使用 [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) 函數並指定不同的資料指標控制碼，來變更資料指標的設計。</span><span class="sxs-lookup"><span data-stu-id="311d9-153">Your application can change the design of the cursor by using the [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) function and specifying a different cursor handle.</span></span> <span data-ttu-id="311d9-154">不過，當游標移動時，系統會在新位置重新繪製類別游標。</span><span class="sxs-lookup"><span data-stu-id="311d9-154">However, when the cursor moves, the system redraws the class cursor at the new location.</span></span> <span data-ttu-id="311d9-155">若要避免重新繪製類別資料指標，您必須處理 [**WM \_ SETCURSOR**](wm-setcursor.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="311d9-155">To prevent the class cursor from being redrawn, you must process the [**WM\_SETCURSOR**](wm-setcursor.md) message.</span></span> <span data-ttu-id="311d9-156">每次資料指標移動和滑鼠輸入都未被捕捉時，系統就會將此訊息傳送至游標移動所在的視窗。</span><span class="sxs-lookup"><span data-stu-id="311d9-156">Each time the cursor moves and mouse input is not captured, the system sends this message to the window in which the cursor is moving.</span></span>

<span data-ttu-id="311d9-157">處理 [**WM \_ SETCURSOR**](wm-setcursor.md)時，您可以為不同的條件指定不同的資料指標。</span><span class="sxs-lookup"><span data-stu-id="311d9-157">You can specify different cursors for different conditions while processing [**WM\_SETCURSOR**](wm-setcursor.md).</span></span> <span data-ttu-id="311d9-158">例如，下列範例顯示如何在游標移至最小化應用程式的圖示上時，顯示游標。</span><span class="sxs-lookup"><span data-stu-id="311d9-158">For example, the following example shows how to display the cursor whenever the cursor moves over the icon of a minimized application.</span></span>


```
case WM_SETCURSOR: 
 
    // If the window is minimized, draw the hCurs3 cursor. 
    // If the window is not minimized, draw the default 
    // cursor (class cursor). 
 
    if (IsIconic(hwnd)) 
    { 
        SetCursor(hCurs3); 
        break; 
    } 
```



<span data-ttu-id="311d9-159">當視窗未最小化時，系統會顯示類別游標。</span><span class="sxs-lookup"><span data-stu-id="311d9-159">When the window is not minimized, the system displays the class cursor.</span></span>

<span data-ttu-id="311d9-160">您可以使用 [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) 函數來取代類別資料指標。</span><span class="sxs-lookup"><span data-stu-id="311d9-160">You can replace a class cursor by using the [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) function.</span></span> <span data-ttu-id="311d9-161">此函式會變更指定類別之所有視窗的預設視窗設定。</span><span class="sxs-lookup"><span data-stu-id="311d9-161">This function changes the default window settings for all windows of a specified class.</span></span> <span data-ttu-id="311d9-162">下列範例會以資料指標取代現有的類別資料指標 `hCurs2` 。</span><span class="sxs-lookup"><span data-stu-id="311d9-162">The following example replaces the existing class cursor with the `hCurs2` cursor.</span></span>


```
// Change the cursor for window class represented by hwnd. 
 
SetClassLongPtr(hwnd,    // window handle 
    GCLP_HCURSOR,        // change cursor 
    (LONG_PTR) hCurs2);  // new cursor 
```



<span data-ttu-id="311d9-163">如需詳細資訊，請參閱 [視窗類別](/windows/desktop/winmsg/window-classes) 和 [滑鼠輸入](/windows/desktop/inputdev/mouse-input)。</span><span class="sxs-lookup"><span data-stu-id="311d9-163">For more information, see [Window Classes](/windows/desktop/winmsg/window-classes) and [Mouse Input](/windows/desktop/inputdev/mouse-input).</span></span>

## <a name="confining-a-cursor"></a><span data-ttu-id="311d9-164">將資料指標</span><span class="sxs-lookup"><span data-stu-id="311d9-164">Confining a Cursor</span></span>

<span data-ttu-id="311d9-165">下列範例會將資料指標設為應用程式的視窗，然後將游標還原到先前的視窗。</span><span class="sxs-lookup"><span data-stu-id="311d9-165">The following example confines the cursor to the application's window and then restores the cursor to its previous window.</span></span> <span data-ttu-id="311d9-166">此範例會使用 [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) 函數來記錄資料指標可以移動的區域，以及 [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) 函數來限制和還原資料指標。</span><span class="sxs-lookup"><span data-stu-id="311d9-166">The example uses the [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) function to record the area in which the cursor can move and the [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) function to confine and restore the cursor.</span></span>


```
RECT rcClip;           // new area for ClipCursor
RECT rcOldClip;        // previous area for ClipCursor
 
// Record the area in which the cursor can move. 
 
GetClipCursor(&rcOldClip); 
 
// Get the dimensions of the application's window. 
 
GetWindowRect(hwnd, &rcClip); 
 
// Confine the cursor to the application's window. 
 
ClipCursor(&rcClip); 
 
   // 
   // Process input from the confined cursor. 
   // 
 
// Restore the cursor to its previous area. 
 
ClipCursor(&rcOldClip); 
```



<span data-ttu-id="311d9-167">因為系統中有一次只能有一個資料指標，所以必須先將資料指標的應用程式還原到另一個視窗，才能將放棄控制項移至另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="311d9-167">Because there is only one cursor at a time available in the system, an application that confines the cursor must restore the cursor before relinquishing control to another window.</span></span>

## <a name="using-cursor-functions-to-create-a-mousetrap"></a><span data-ttu-id="311d9-168">使用資料指標函數建立 Mousetrap</span><span class="sxs-lookup"><span data-stu-id="311d9-168">Using Cursor Functions to Create a Mousetrap</span></span>

<span data-ttu-id="311d9-169">下列範例會使用 [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)、 [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)、 [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor)、 [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)和 [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) 函數來建立簡單的 mousetrap。</span><span class="sxs-lookup"><span data-stu-id="311d9-169">The following example uses the [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos), [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos), [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor), [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), and [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) functions to create a simple mousetrap.</span></span> <span data-ttu-id="311d9-170">它也會使用 cursor 和 timer 函式，每10秒監視資料指標的位置。</span><span class="sxs-lookup"><span data-stu-id="311d9-170">It also uses cursor and timer functions to monitor the cursor's position every 10 seconds.</span></span> <span data-ttu-id="311d9-171">如果過去10秒內的資料指標位置未變更，而且應用程式的主視窗最小化，則應用程式會變更資料指標，並將其移至 mousetrap 圖示。</span><span class="sxs-lookup"><span data-stu-id="311d9-171">If the cursor position has not changed in the last 10 seconds and the application's main window is minimized, the application changes the cursor and moves it to the mousetrap icon.</span></span>

<span data-ttu-id="311d9-172">[圖示](icons.md)中包含類似 mousetrap 的範例。</span><span class="sxs-lookup"><span data-stu-id="311d9-172">An example for a similar mousetrap is included in [Icons](icons.md).</span></span> <span data-ttu-id="311d9-173">它會使用 [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) 和 [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) 函式，而不是與裝置相關的 [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) 和 [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) 函式。</span><span class="sxs-lookup"><span data-stu-id="311d9-173">It uses the [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) and [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) functions instead of the more device-dependent [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) and [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) functions.</span></span>


```
HICON hIcon1;               // icon handles 
POINT ptOld;                // previous cursor location 
HCURSOR hCurs1;             // cursor handle 
 
 
// The following cursor masks are defined in a code 
// example that appears earlier in this section. 
 
// Yin-shaped cursor AND and XOR masks 
 
BYTE ANDmaskCursor[] = ... 
BYTE XORmaskCursor[] = ... 
 
// Yang-shaped icon AND mask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,  // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,  // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,  // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,  // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,  // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,  // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,  // line 7 
                      0xFF, 0xF0, 0x00, 0x07,  // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,  // line 9 
                      0xFF, 0xE0, 0x00, 0x03,  // line 10 
                      0xFF, 0xE0, 0x00, 0x01,  // line 11 
                      0xFF, 0xE0, 0x00, 0x01,  // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,  // line 13 
                      0xFF, 0xF0, 0x00, 0x00,  // line 14 
                      0xFF, 0xF8, 0x00, 0x00,  // line 15 
                      0xFF, 0xFC, 0x00, 0x00,  // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,  // line 17 
                      0xFF, 0xFF, 0x80, 0x00,  // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,  // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,  // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,  // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,  // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,  // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,  // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,  // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,  // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,  // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,  // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,  // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,  // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,  // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF}; // line 32 
 
// Yang-shaped icon XOR mask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,  // line 1 
                      0x00, 0x00, 0x00, 0x00,  // line 2 
                      0x00, 0x00, 0x00, 0x00,  // line 3 
                      0x00, 0x00, 0x00, 0x00,  // line 4 
 
                      0x00, 0x00, 0x00, 0x00,  // line 5 
                      0x00, 0x00, 0x00, 0x00,  // line 6 
                      0x00, 0x00, 0x00, 0x00,  // line 7 
                      0x00, 0x00, 0x38, 0x00,  // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,  // line 9 
                      0x00, 0x00, 0x7C, 0x00,  // line 10 
                      0x00, 0x00, 0x7C, 0x00,  // line 11  
                      0x00, 0x00, 0x38, 0x00,  // line 12 
 
                      0x00, 0x00, 0x00, 0x00,  // line 13 
                      0x00, 0x00, 0x00, 0x00,  // line 14 
                      0x00, 0x00, 0x00, 0x00,  // line 15 
                      0x00, 0x00, 0x00, 0x00,  // line 16 
 
                      0x00, 0x00, 0x00, 0x00,  // line 17 
                      0x00, 0x00, 0x00, 0x00,  // line 18 
                      0x00, 0x00, 0x00, 0x00,  // line 19 
                      0x00, 0x00, 0x00, 0x00,  // line 20 
 
                      0x00, 0x00, 0x00, 0x00,  // line 21 
                      0x00, 0x00, 0x00, 0x00,  // line 22 
                      0x00, 0x00, 0x00, 0x00,  // line 23 
                      0x00, 0x00, 0x00, 0x00,  // line 24 
 
                      0x00, 0x00, 0x00, 0x00,  // line 25 
                      0x00, 0x00, 0x00, 0x00,  // line 26 
                      0x00, 0x00, 0x00, 0x00,  // line 27 
                      0x00, 0x00, 0x00, 0x00,  // line 28 
 
                      0x00, 0x00, 0x00, 0x00,  // line 29 
                      0x00, 0x00, 0x00, 0x00,  // line 30 
                      0x00, 0x00, 0x00, 0x00,  // line 31 
                      0x00, 0x00, 0x00, 0x00}; // line 32 
 
hIcon1 = CreateIcon(hinst, // handle to app. instance 
             32,           // icon width 
             32,           // icon height 
             1,            // number of XOR planes 
             1,            // number of bits per pixel 
             ANDmaskIcon,  // AND mask 
             XORmaskIcon); // XOR mask 
 
hCurs1 = CreateCursor(hinst, // handle to app. instance
             19,             // horizontal position of hot spot 
             2,              // vertical position of hot spot 
             32,             // cursor width 
             32,             // cursor height 
             ANDmaskCursor,  // AND mask 
             XORmaskCursor); // XOR mask 
 
// Fill in the window class structure. 
 
WNDCLASS  wc; 
 
wc.hIcon = hIcon1;                        // class icon 
wc.hCursor = LoadCursor(NULL, IDC_ARROW); // class cursor 
 
//
// Register the window class and perform 
// other application initialization. 
//
 
// Set a timer for the mousetrap. 
 
GetCursorPos(&ptOld); 
 
SetTimer(hwnd, IDT_CURSOR, 10000, (TIMERPROC) NULL); 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // window handle 
    UINT message,       // type of message 
    UINT wParam,        // additional information 
    LONG lParam)        // additional information 
{ 
 
    HDC hdc;            // handle to device context 
    POINT pt;           // current cursor location 
    RECT rc;            // minimized window location 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
        case WM_TIMER: 
        // If the window is minimized, compare the 
        // current cursor position with the one 10 
        // seconds before. If the cursor position has 
        // not changed, move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left + 20, rc.top + 4); 
 
                    // Note that the additional constants 
                    // (20 and 4) are application-specific 
                    // values to align the yin-shaped cursor 
                    // and the yang-shaped icon. 
 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_SETCURSOR: 
        // If the window is minimized, draw hCurs1. 
        // If the window is not minimized, draw the 
        // default cursor (class cursor). 
 
            if (IsIconic(hwnd)) 
            { 
                SetCursor(hCurs1); 
                break; 
            } 
 
        case WM_DESTROY: 
        // Destroy timer. 
 
            KillTimer(hwnd, IDT_CURSOR); 
 
            PostQuitMessage(0); 
            break; 
    } 
} 
```



## <a name="using-the-keyboard-to-move-the-cursor"></a><span data-ttu-id="311d9-174">使用鍵盤移動游標</span><span class="sxs-lookup"><span data-stu-id="311d9-174">Using the Keyboard to Move the Cursor</span></span>

<span data-ttu-id="311d9-175">由於系統不需要滑鼠，因此應用程式應該能夠使用鍵盤模擬滑鼠動作。</span><span class="sxs-lookup"><span data-stu-id="311d9-175">Because the system does not require a mouse, an application should be able to simulate mouse actions with the keyboard.</span></span> <span data-ttu-id="311d9-176">下列範例示範如何使用 [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) 和 [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) 函式，以及從方向鍵處理輸入來達成此目的。</span><span class="sxs-lookup"><span data-stu-id="311d9-176">The following example shows how to achieve this by using the [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) and [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) functions and by processing input from the arrow keys.</span></span>


```
HCURSOR hCurs1, hCurs2;    // cursor handles 
 
POINT pt;                  // cursor location  
RECT rc;                   // client area coordinates 
static int repeat = 1;     // repeat key counter 
 
// 
// Other declarations and initialization. 
// 
 
switch (message) 
{ 
// 
// Process other messages. 
// 
 
    case WM_KEYDOWN: 
 
        if (wParam != VK_LEFT && wParam != VK_RIGHT && 
        wParam != VK_UP && wParam != VK_DOWN) 
        { 
            break; 
        } 
 
        GetCursorPos(&pt); 
 
        // Convert screen coordinates to client coordinates. 
 
        ScreenToClient(hwnd, &pt); 
 
        switch (wParam) 
        { 
        // Move the cursor to reflect which 
        // arrow keys are pressed. 
 
            case VK_LEFT:               // left arrow 
                pt.x -= repeat; 
                break; 
 
            case VK_RIGHT:              // right arrow 
                pt.x += repeat; 
                break; 
 
            case VK_UP:                 // up arrow 
                pt.y -= repeat; 
                break; 
 
            case VK_DOWN:               // down arrow 
                pt.y += repeat; 
                break; 
 
            default: 
                return 0; 
        } 
 
        repeat++;           // Increment repeat count. 
 
        // Keep the cursor in the client area. 
 
        GetClientRect(hwnd, &rc); 
 
        if (pt.x >= rc.right) 
        { 
            pt.x = rc.right - 1; 
        } 
        else 
        { 
            if (pt.x < rc.left) 
            { 
                pt.x = rc.left; 
            } 
        } 
 
        if (pt.y >= rc.bottom) 
            pt.y = rc.bottom - 1; 
        else 
            if (pt.y < rc.top) 
                pt.y = rc.top; 
 
        // Convert client coordinates to screen coordinates. 
 
        ClientToScreen(hwnd, &pt); 
        SetCursorPos(pt.x, pt.y); 
        return 0; 

 
    case WM_KEYUP: 
 
        repeat = 1;            // Clear repeat count. 
        return 0; 
 
} 
```



 

 
