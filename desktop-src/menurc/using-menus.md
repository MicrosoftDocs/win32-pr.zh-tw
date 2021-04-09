---
title: 使用功能表
description: 本節提供與功能表相關之工作的程式碼範例。
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- 資源、功能表
- 功能表，建立
- 功能表-範本資源
- 資源，功能表範本
- 擴充功能表範本格式
- 舊功能表範本格式
- 正在載入功能表範本資源
- 功能表、類別
- 功能表、快捷方式
- 建立功能表
- 類別功能表
- 捷徑功能表
- 功能表項目點陣圖
- 功能表，已繪製的擁有者
- 擁有者繪製功能表
- 自訂核取記號點陣圖
- 功能表、核取方塊
- 功能表、字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d216b5fe5e6c25a98b5bdf3abe9d55b4bb0b34f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682220"
---
# <a name="using-menus"></a><span data-ttu-id="71cb7-121">使用功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-121">Using Menus</span></span>

<span data-ttu-id="71cb7-122">本節將說明下列工作：</span><span class="sxs-lookup"><span data-stu-id="71cb7-122">This section describes the following tasks:</span></span>

-   [<span data-ttu-id="71cb7-123">使用 Menu-Template 資源</span><span class="sxs-lookup"><span data-stu-id="71cb7-123">Using a Menu-Template Resource</span></span>](#using-a-menu-template-resource)
    -   [<span data-ttu-id="71cb7-124">擴充的 Menu-Template 格式</span><span class="sxs-lookup"><span data-stu-id="71cb7-124">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
    -   [<span data-ttu-id="71cb7-125">舊的 Menu-Template 格式</span><span class="sxs-lookup"><span data-stu-id="71cb7-125">Old Menu-Template Format</span></span>](#old-menu-template-format)
    -   [<span data-ttu-id="71cb7-126">載入 Menu-Template 資源</span><span class="sxs-lookup"><span data-stu-id="71cb7-126">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
    -   [<span data-ttu-id="71cb7-127">建立類別功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-127">Creating a Class Menu</span></span>](#creating-a-class-menu)
-   [<span data-ttu-id="71cb7-128">建立快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-128">Creating a Shortcut Menu</span></span>](#creating-a-shortcut-menu)
    -   [<span data-ttu-id="71cb7-129">處理 WM \_ CONTEXTMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-129">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
    -   [<span data-ttu-id="71cb7-130">建立快捷方式 Font-Attributes 功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-130">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
    -   [<span data-ttu-id="71cb7-131">顯示快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-131">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)
-   [<span data-ttu-id="71cb7-132">使用 Menu-Item 點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-132">Using Menu-Item Bitmaps</span></span>](#using-menu-item-bitmaps)
    -   [<span data-ttu-id="71cb7-133">設定點陣圖類型旗標</span><span class="sxs-lookup"><span data-stu-id="71cb7-133">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
    -   [<span data-ttu-id="71cb7-134">建立點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-134">Creating the Bitmap</span></span>](#creating-the-bitmap)
    -   [<span data-ttu-id="71cb7-135">將線條和圖形新增至功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-135">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
    -   [<span data-ttu-id="71cb7-136">Menu-Item 點陣圖範例</span><span class="sxs-lookup"><span data-stu-id="71cb7-136">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)
-   [<span data-ttu-id="71cb7-137">建立 Owner-Drawn 功能表項目</span><span class="sxs-lookup"><span data-stu-id="71cb7-137">Creating Owner-Drawn Menu Items</span></span>](#creating-owner-drawn-menu-items)
    -   [<span data-ttu-id="71cb7-138">設定 Owner-Drawn 旗標</span><span class="sxs-lookup"><span data-stu-id="71cb7-138">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
    -   [<span data-ttu-id="71cb7-139">擁有者繪製的功能表和 WM \_ MEASUREITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-139">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="71cb7-140">擁有者繪製的功能表和 WM \_ DRAWITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-140">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="71cb7-141">擁有者繪製的功能表和 WM \_ MENUCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-141">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
    -   [<span data-ttu-id="71cb7-142">設定 Menu-Item 文字字串的字型</span><span class="sxs-lookup"><span data-stu-id="71cb7-142">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
    -   [<span data-ttu-id="71cb7-143">Owner-Drawn 功能表項目的範例</span><span class="sxs-lookup"><span data-stu-id="71cb7-143">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)
-   [<span data-ttu-id="71cb7-144">使用自訂核取記號點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-144">Using Custom Check Mark Bitmaps</span></span>](#using-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="71cb7-145">建立自訂的核取記號點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-145">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="71cb7-146">建立點陣圖與功能表項目的關聯</span><span class="sxs-lookup"><span data-stu-id="71cb7-146">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
    -   [<span data-ttu-id="71cb7-147">設定核取記號屬性</span><span class="sxs-lookup"><span data-stu-id="71cb7-147">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
    -   [<span data-ttu-id="71cb7-148">模擬功能表中的核取方塊</span><span class="sxs-lookup"><span data-stu-id="71cb7-148">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
    -   [<span data-ttu-id="71cb7-149">使用自訂核取記號點陣圖的範例</span><span class="sxs-lookup"><span data-stu-id="71cb7-149">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a><span data-ttu-id="71cb7-150">使用 Menu-Template 資源</span><span class="sxs-lookup"><span data-stu-id="71cb7-150">Using a Menu-Template Resource</span></span>

<span data-ttu-id="71cb7-151">您通常會在應用程式中包含功能表，方法是建立功能表範本資源，然後在執行時間載入功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-151">You typically include a menu in an application by creating a menu-template resource and then loading the menu at run time.</span></span> <span data-ttu-id="71cb7-152">本節說明功能表範本的格式，並說明如何載入功能表範本資源，並在您的應用程式中使用它。</span><span class="sxs-lookup"><span data-stu-id="71cb7-152">This section describes the format of a menu template, and explains how to load a menu-template resource and use it in your application.</span></span> <span data-ttu-id="71cb7-153">如需建立功能表範本資源的詳細資訊，請參閱您的開發工具隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="71cb7-153">For information about creating a menu-template resource, see the documentation included with your development tools.</span></span>

-   [<span data-ttu-id="71cb7-154">擴充的 Menu-Template 格式</span><span class="sxs-lookup"><span data-stu-id="71cb7-154">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
-   [<span data-ttu-id="71cb7-155">舊的 Menu-Template 格式</span><span class="sxs-lookup"><span data-stu-id="71cb7-155">Old Menu-Template Format</span></span>](#old-menu-template-format)
-   [<span data-ttu-id="71cb7-156">載入 Menu-Template 資源</span><span class="sxs-lookup"><span data-stu-id="71cb7-156">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
-   [<span data-ttu-id="71cb7-157">建立類別功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-157">Creating a Class Menu</span></span>](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a><span data-ttu-id="71cb7-158">擴充的 Menu-Template 格式</span><span class="sxs-lookup"><span data-stu-id="71cb7-158">Extended Menu-Template Format</span></span>

<span data-ttu-id="71cb7-159">擴充的功能表範本格式支援其他功能表功能。</span><span class="sxs-lookup"><span data-stu-id="71cb7-159">The extended menu-template format supports additional menu functionality.</span></span> <span data-ttu-id="71cb7-160">如同標準功能表-範本資源，擴充功能表-範本資源具有 **RT \_ 功能表** 資源類型。</span><span class="sxs-lookup"><span data-stu-id="71cb7-160">Like standard menu-template resources, extended menu-template resources have the **RT\_MENU** resource type.</span></span> <span data-ttu-id="71cb7-161">系統會根據版本號碼來區分這兩種資源格式，也就是資源標頭的第一個成員。</span><span class="sxs-lookup"><span data-stu-id="71cb7-161">The system distinguishes the two resource formats by the version number, which is the first member of the resource header.</span></span>

<span data-ttu-id="71cb7-162">擴充功能表範本是由 [**MENUEX \_ 範本 \_ 標頭**](menuex-template-header.md) 結構所組成，後面接著一個 [**MENUEX 的 \_ 範本 \_ 專案**](menuex-template-item.md) 專案定義結構。</span><span class="sxs-lookup"><span data-stu-id="71cb7-162">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one more [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) item definition structures.</span></span>

### <a name="old-menu-template-format"></a><span data-ttu-id="71cb7-163">舊的 Menu-Template 格式</span><span class="sxs-lookup"><span data-stu-id="71cb7-163">Old Menu-Template Format</span></span>

<span data-ttu-id="71cb7-164">舊版功能表範本 (Microsoft Windows NT 3.51 及更早版本的) 定義功能表，但不支援新的功能表功能。</span><span class="sxs-lookup"><span data-stu-id="71cb7-164">An old menu template (Microsoft Windows NT 3.51 and earlier) defines a menu, but does not support the new menu functionality.</span></span> <span data-ttu-id="71cb7-165">舊的功能表範本資源具有 **RT \_ 功能表** 資源類型。</span><span class="sxs-lookup"><span data-stu-id="71cb7-165">An old menu-template resource has the **RT\_MENU** resource type.</span></span>

<span data-ttu-id="71cb7-166">舊的功能表範本包含 [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) 結構，後面接著一或多個 [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) 結構。</span><span class="sxs-lookup"><span data-stu-id="71cb7-166">An old menu template consists of a [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) structure followed by one or more [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) structures.</span></span>

### <a name="loading-a-menu-template-resource"></a><span data-ttu-id="71cb7-167">載入 Menu-Template 資源</span><span class="sxs-lookup"><span data-stu-id="71cb7-167">Loading a Menu-Template Resource</span></span>

<span data-ttu-id="71cb7-168">若要載入功能表範本資源，請使用 [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) 函式，指定包含資源的模組控制碼和功能表範本的識別碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-168">To load a menu-template resource, use the [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) function, specifying a handle to the module that contains the resource and the menu template's identifier.</span></span> <span data-ttu-id="71cb7-169">**LoadMenu** 函式會傳回功能表控制碼，您可以用它來將功能表指派給視窗。</span><span class="sxs-lookup"><span data-stu-id="71cb7-169">The **LoadMenu** function returns a menu handle that you can use to assign the menu to a window.</span></span> <span data-ttu-id="71cb7-170">此視窗會成為功能表的擁有者視窗，並接收功能表所產生的所有訊息。</span><span class="sxs-lookup"><span data-stu-id="71cb7-170">This window becomes the menu's owner window, receiving all the messages generated by the menu.</span></span>

<span data-ttu-id="71cb7-171">若要從已在記憶體中的功能表範本建立功能表，請使用 [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) 函數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-171">To create a menu from a menu template that is already in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span> <span data-ttu-id="71cb7-172">如果您的應用程式會以動態方式產生功能表範本，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="71cb7-172">This is useful if your application generates menu templates dynamically.</span></span>

<span data-ttu-id="71cb7-173">若要將功能表指派給視窗，請使用 [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu)函數，或在建立視窗時，于 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)函式的 *hMenu* 參數中指定功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-173">To assign a menu to a window, use the [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) function or specify the menu's handle in the *hMenu* parameter of the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function when creating a window.</span></span> <span data-ttu-id="71cb7-174">您可以將功能表指派給視窗的另一種方式是在註冊視窗類別時指定功能表範本;範本會將指定的功能表識別為該視窗類別的類別功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-174">Another way you can assign a menu to a window is to specify a menu template when you register a window class; the template identifies the specified menu as the class menu for that window class.</span></span>

<span data-ttu-id="71cb7-175">若要讓系統自動將特定功能表指派給視窗，請在註冊視窗的類別時，指定功能表的範本。</span><span class="sxs-lookup"><span data-stu-id="71cb7-175">To have the system automatically assign a specific menu to a window, specify the menu's template when you register the window's class.</span></span> <span data-ttu-id="71cb7-176">範本會將指定的功能表識別為該視窗類別的類別功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-176">The template identifies the specified menu as the class menu for that window class.</span></span> <span data-ttu-id="71cb7-177">然後，當您建立指定類別的視窗時，系統會自動將指定的功能表指派給視窗。</span><span class="sxs-lookup"><span data-stu-id="71cb7-177">Then, when you create a window of the specified class, the system automatically assigns the specified menu to the window.</span></span>

<span data-ttu-id="71cb7-178">您無法將功能表指派給做為子視窗的視窗。</span><span class="sxs-lookup"><span data-stu-id="71cb7-178">You cannot assign a menu to a window that is a child window.</span></span>

<span data-ttu-id="71cb7-179">若要建立類別功能表，請將功能表範本資源的識別碼包含為 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **lpszMenuName** 成員，然後將結構的指標傳遞至 [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa)函式。</span><span class="sxs-lookup"><span data-stu-id="71cb7-179">To create a class menu, include the identifier of the menu-template resource as the **lpszMenuName** member of a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure and then pass a pointer to the structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span>

### <a name="creating-a-class-menu"></a><span data-ttu-id="71cb7-180">建立類別功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-180">Creating a Class Menu</span></span>

<span data-ttu-id="71cb7-181">下列範例示範如何建立應用程式的類別功能表、建立使用 [類別] 功能表的視窗，以及處理視窗程式中的功能表命令。</span><span class="sxs-lookup"><span data-stu-id="71cb7-181">The following example shows how to create a class menu for an application, create a window that uses the class menu, and process menu commands in the window procedure.</span></span>

<span data-ttu-id="71cb7-182">以下是應用程式標頭檔的相關部分：</span><span class="sxs-lookup"><span data-stu-id="71cb7-182">Following is the relevant portion of the application's header file:</span></span>


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



<span data-ttu-id="71cb7-183">以下是應用程式本身的相關部分：</span><span class="sxs-lookup"><span data-stu-id="71cb7-183">Following are the relevant portions of the application itself:</span></span>


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a><span data-ttu-id="71cb7-184">建立快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-184">Creating a Shortcut Menu</span></span>

<span data-ttu-id="71cb7-185">若要使用應用程式中的快捷方式功能表，請將其控制碼傳遞至 [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) 函式。</span><span class="sxs-lookup"><span data-stu-id="71cb7-185">To use a shortcut menu in an application, pass its handle to the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="71cb7-186">應用程式通常會在視窗程式中呼叫 **TrackPopupMenuEx** ，以回應使用者產生的訊息，例如 [**Wm \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 或 [**wm \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)。</span><span class="sxs-lookup"><span data-stu-id="71cb7-186">An application typically calls **TrackPopupMenuEx** in a window procedure in response to a user-generated message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown).</span></span>

<span data-ttu-id="71cb7-187">除了快顯功能表控點之外， [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) 還會要求您指定主控視窗的控制碼、螢幕座標中的快捷方式功能表 (的位置) ，以及使用者可以用來選擇專案的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="71cb7-187">In addition to the pop-up menu handle, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) requires that you specify a handle to the owner window, the position of the shortcut menu (in screen coordinates), and the mouse button that the user can use to choose an item.</span></span>

<span data-ttu-id="71cb7-188">仍然支援較舊的 [**trackpopupmenu 讓**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) 函式，但新的應用程式應該使用 [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) 函數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-188">The older [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function is still supported, but new applications should use the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="71cb7-189">**TrackPopupMenuEx** 函式需要與 **trackpopupmenu 讓** 相同的參數，但也可讓您指定功能表不應遮蔽的部分畫面。</span><span class="sxs-lookup"><span data-stu-id="71cb7-189">The **TrackPopupMenuEx** function requires the same parameters as **TrackPopupMenu**, but also lets you specify a portion of the screen that the menu should not obscure.</span></span> <span data-ttu-id="71cb7-190">應用程式通常會在處理 [**WM \_ CONTEXTMENU**](wm-contextmenu.md) 訊息時，于視窗程式中呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="71cb7-190">An application typically calls these functions in a window procedure when processing the [**WM\_CONTEXTMENU**](wm-contextmenu.md) message.</span></span>

<span data-ttu-id="71cb7-191">您可以藉由提供 x 和 y 座標以及 **tpm \_ CENTERALIGN**、 **tpm \_ LEFTALIGN** 或 **tpm \_ RIGHTALIGN** 旗標，來指定快捷方式功能表的位置。</span><span class="sxs-lookup"><span data-stu-id="71cb7-191">You can specify the position of a shortcut menu by providing x- and y-coordinates along with the **TPM\_CENTERALIGN**, **TPM\_LEFTALIGN**, or **TPM\_RIGHTALIGN** flag.</span></span> <span data-ttu-id="71cb7-192">旗標會指定相對於 x 和 y 座標之快捷方式功能表的位置。</span><span class="sxs-lookup"><span data-stu-id="71cb7-192">The flag specifies the position of the shortcut menu relative to the x- and y-coordinates.</span></span>

<span data-ttu-id="71cb7-193">您應允許使用者使用用來顯示功能表的相同滑鼠按鍵，從快捷方式功能表中選擇專案。</span><span class="sxs-lookup"><span data-stu-id="71cb7-193">You should permit the user to choose an item from a shortcut menu by using the same mouse button used to display the menu.</span></span> <span data-ttu-id="71cb7-194">若要這樣做，請指定 **tpm \_ LEFTBUTTON** 或 **tpm \_ RIGHTBUTTON** 旗標，以指出使用者可以使用哪一個滑鼠按鍵來選擇功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-194">To do this, specify either **TPM\_LEFTBUTTON** or **TPM\_RIGHTBUTTON** flag to indicate which mouse button the user can use to choose a menu item.</span></span>

-   [<span data-ttu-id="71cb7-195">處理 WM \_ CONTEXTMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-195">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
-   [<span data-ttu-id="71cb7-196">建立快捷方式 Font-Attributes 功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-196">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
-   [<span data-ttu-id="71cb7-197">顯示快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-197">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a><span data-ttu-id="71cb7-198">處理 WM \_ CONTEXTMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-198">Processing the WM\_CONTEXTMENU Message</span></span>

<span data-ttu-id="71cb7-199">當應用程式的視窗程式將 [**wm \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)或 [**wm \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup)訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函數時，就會產生 [**WM \_ CONTEXTMENU**](wm-contextmenu.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="71cb7-199">The [**WM\_CONTEXTMENU**](wm-contextmenu.md) message is generated when an application's window procedure passes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="71cb7-200">應用程式可處理此訊息，以顯示適合其螢幕特定部分的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-200">The application can process this message to display a shortcut menu appropriate to a specific portion of its screen.</span></span> <span data-ttu-id="71cb7-201">如果應用程式未顯示快捷方式功能表，則應該將訊息傳遞至 **DefWindowProc** 以進行預設處理。</span><span class="sxs-lookup"><span data-stu-id="71cb7-201">If the application does not display a shortcut menu, it should pass the message to **DefWindowProc** for default handling.</span></span>

<span data-ttu-id="71cb7-202">以下是在應用程式的視窗程式中可能出現的 [**WM \_ CONTEXTMENU**](wm-contextmenu.md) 訊息處理範例。</span><span class="sxs-lookup"><span data-stu-id="71cb7-202">Following is an example of [**WM\_CONTEXTMENU**](wm-contextmenu.md) message processing as it might appear in an application's window procedure.</span></span> <span data-ttu-id="71cb7-203">*LParam* 參數的低序位和高序位字組會在放開滑鼠右鍵時指定滑鼠的螢幕座標 (請注意，在具有多個監視器) 的系統上，這些座標可能會採用負數值。</span><span class="sxs-lookup"><span data-stu-id="71cb7-203">The low-order and high-order words of the *lParam* parameter specify the screen coordinates of the mouse when the right mouse button is released (note that these coordinates can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="71cb7-204">如果應用程式定義的 **OnCoNtextMenu** 函式顯示操作功能表，則會傳回 **TRUE** ; 否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="71cb7-204">The application-defined **OnContextMenu** function returns **TRUE** if it displays a context menu, or **FALSE** if it does not.</span></span>


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



<span data-ttu-id="71cb7-205">下列應用程式定義的 OnCoNtextMenu 函式會在指定的滑鼠位置位於視窗的工作區中時，顯示快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-205">The following application-defined OnContextMenu function displays a shortcut menu if the specified mouse position is within the window's client area.</span></span> <span data-ttu-id="71cb7-206">較複雜的函式可能會根據指定的工作區的部分，顯示數個不同功能表中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="71cb7-206">A more sophisticated function might display one of several different menus, depending on which portion of the client area is specified.</span></span> <span data-ttu-id="71cb7-207">為了實際顯示快捷方式功能表，此範例會呼叫名為 DisplayCoNtextMenu 的應用程式定義函數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-207">To actually display the shortcut menu, this example calls an application-defined function called DisplayContextMenu.</span></span> <span data-ttu-id="71cb7-208">如需此功能的描述，請參閱 [顯示快捷方式功能表](#displaying-a-shortcut-menu)。</span><span class="sxs-lookup"><span data-stu-id="71cb7-208">For a description of this function, see [Displaying a Shortcut Menu](#displaying-a-shortcut-menu).</span></span>


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a><span data-ttu-id="71cb7-209">建立快捷方式 Font-Attributes 功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-209">Creating a Shortcut Font-Attributes Menu</span></span>

<span data-ttu-id="71cb7-210">本章節中的範例包含應用程式中建立及顯示快捷方式功能表的部分程式碼，可讓使用者設定字型和字型屬性。</span><span class="sxs-lookup"><span data-stu-id="71cb7-210">The example in this section contains portions of code from an application that creates and displays a shortcut menu that enables the user to set fonts and font attributes.</span></span> <span data-ttu-id="71cb7-211">當使用者按下滑鼠左鍵時，應用程式會在主視窗的工作區中顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-211">The application displays the menu in the client area of its main window whenever the user clicks the left mouse button.</span></span>

<span data-ttu-id="71cb7-212">以下是應用程式資源定義檔中所提供快捷方式功能表的功能表範本。</span><span class="sxs-lookup"><span data-stu-id="71cb7-212">Here is the menu template for the shortcut menu that is provided in the application's resource-definition file.</span></span>


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



<span data-ttu-id="71cb7-213">下列範例會提供視窗程式和支援函式，用來建立和顯示快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-213">The following example gives the window procedure and supporting functions used to create and display the shortcut menu.</span></span>


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a><span data-ttu-id="71cb7-214">顯示快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-214">Displaying a Shortcut Menu</span></span>

<span data-ttu-id="71cb7-215">下列範例所示的函式會顯示快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-215">The function shown in the following example displays a shortcut menu.</span></span>

<span data-ttu-id="71cb7-216">應用程式包含以 "ShortcutExample" 字串識別的功能表資源。</span><span class="sxs-lookup"><span data-stu-id="71cb7-216">The application includes a menu resource identified by the string "ShortcutExample."</span></span> <span data-ttu-id="71cb7-217">功能表列只包含一個功能表名稱。</span><span class="sxs-lookup"><span data-stu-id="71cb7-217">The menu bar simply contains a menu name.</span></span> <span data-ttu-id="71cb7-218">應用程式會使用 [**trackpopupmenu 讓**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) 函式來顯示與這個功能表項目相關聯的功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-218">The application uses the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function to display the menu associated with this menu item.</span></span> <span data-ttu-id="71cb7-219">因為 **trackpopupmenu 讓** 需要功能表、子功能表或快捷方式功能表的控制碼，所以不會顯示功能表列本身。 )  (</span><span class="sxs-lookup"><span data-stu-id="71cb7-219">(The menu bar itself is not displayed because **TrackPopupMenu** requires a handle to a menu, submenu, or shortcut menu.)</span></span>


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a><span data-ttu-id="71cb7-220">使用 Menu-Item 點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-220">Using Menu-Item Bitmaps</span></span>

<span data-ttu-id="71cb7-221">系統可以使用點陣圖而非文字字串來顯示功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-221">The system can use a bitmap instead of a text string to display a menu item.</span></span> <span data-ttu-id="71cb7-222">若要使用點陣圖，您必須為功能表項目設定 **MIIM \_ 點陣圖** 旗標，並指定系統應該針對 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)結構的 **hbmpItem** 成員中的功能表項目顯示之點陣圖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-222">To use a bitmap, you must set the **MIIM\_BITMAP** flag for the menu item and specify a handle to the bitmap that the system should display for the menu item in the **hbmpItem** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="71cb7-223">本節說明如何使用功能表項目的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-223">This section describes how to use bitmaps for menu items.</span></span>

-   [<span data-ttu-id="71cb7-224">設定點陣圖類型旗標</span><span class="sxs-lookup"><span data-stu-id="71cb7-224">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
-   [<span data-ttu-id="71cb7-225">建立點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-225">Creating the Bitmap</span></span>](#creating-the-bitmap)
-   [<span data-ttu-id="71cb7-226">將線條和圖形新增至功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-226">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
-   [<span data-ttu-id="71cb7-227">Menu-Item 點陣圖範例</span><span class="sxs-lookup"><span data-stu-id="71cb7-227">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a><span data-ttu-id="71cb7-228">設定點陣圖類型旗標</span><span class="sxs-lookup"><span data-stu-id="71cb7-228">Setting the Bitmap Type Flag</span></span>

<span data-ttu-id="71cb7-229">**MIIM \_ 點陣圖** 或 **MF \_ 點陣圖** 旗標會指示系統使用點陣圖，而不是文字字串來顯示功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-229">The **MIIM\_BITMAP** or **MF\_BITMAP** flag tells the system to use a bitmap rather than a text string to display a menu item.</span></span> <span data-ttu-id="71cb7-230">您必須在執行時間設定功能表項目的 **MIIM \_ 點陣圖** 或 **MF \_ 點陣圖** 旗標; 您無法在資源定義檔中設定它。</span><span class="sxs-lookup"><span data-stu-id="71cb7-230">A menu item's **MIIM\_BITMAP** or **MF\_BITMAP** flag must be set at run time; you cannot set it in the resource-definition file.</span></span>

<span data-ttu-id="71cb7-231">針對新的應用程式，您可以使用 [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) 或 [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) 函數來設定 **MIIM \_ 點陣圖** 類型旗標。</span><span class="sxs-lookup"><span data-stu-id="71cb7-231">For new applications, you can use the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) or [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) function to set the **MIIM\_BITMAP** type flag.</span></span> <span data-ttu-id="71cb7-232">若要將功能表項目從文字專案變更為點陣圖專案，請使用 **SetMenuItemInfo**。</span><span class="sxs-lookup"><span data-stu-id="71cb7-232">To change a menu item from a text item to a bitmap item, use **SetMenuItemInfo**.</span></span> <span data-ttu-id="71cb7-233">若要將新的點陣圖專案加入至功能表，請使用 **InsertMenuItem** 函數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-233">To add a new bitmap item to a menu, use the **InsertMenuItem** function.</span></span>

<span data-ttu-id="71cb7-234">針對較舊版本的系統所撰寫的應用程式可以繼續使用 [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)、 [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)或 [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) 函數來設定 **MF \_ 點陣圖** 旗標。</span><span class="sxs-lookup"><span data-stu-id="71cb7-234">Applications written for earlier versions of the system can continue to use the [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to set the **MF\_BITMAP** flag.</span></span> <span data-ttu-id="71cb7-235">若要將功能表項目從文字字串專案變更為點陣圖專案，請使用 **ModifyMenu**。</span><span class="sxs-lookup"><span data-stu-id="71cb7-235">To change a menu item from a text string item to a bitmap item, use **ModifyMenu**.</span></span> <span data-ttu-id="71cb7-236">若要將新的點陣圖專案加入至功能表，請搭配 **InsertMenu** 或 **AppendMenu** 函數使用 **MF \_ 點陣圖** 旗標。</span><span class="sxs-lookup"><span data-stu-id="71cb7-236">To add a new bitmap item to a menu, use the **MF\_BITMAP** flag with the **InsertMenu** or **AppendMenu** function.</span></span>

### <a name="creating-the-bitmap"></a><span data-ttu-id="71cb7-237">建立點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-237">Creating the Bitmap</span></span>

<span data-ttu-id="71cb7-238">當您為功能表項目設定 **MIIM \_ 點陣圖** 或 **MF \_ 點陣圖** 類型旗標時，您也必須指定系統應該針對功能表項目顯示之點陣圖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-238">When you set the **MIIM\_BITMAP** or **MF\_BITMAP** type flag for a menu item, you must also specify a handle to the bitmap that the system should display for the menu item.</span></span> <span data-ttu-id="71cb7-239">您可以將點陣圖提供為點陣圖資源，或在執行時間建立點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-239">You can provide the bitmap as a bitmap resource or create the bitmap at run time.</span></span> <span data-ttu-id="71cb7-240">如果您使用點陣圖資源，您可以使用 [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) 函式來載入點陣圖，並取得其控制碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-240">If you use a bitmap resource, you can use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap and obtain its handle.</span></span>

<span data-ttu-id="71cb7-241">若要在執行時間建立點陣圖，請使用 Windows 圖形裝置介面 (GDI) 函數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-241">To create the bitmap at run time, use Windows Graphics Device Interface (GDI) functions.</span></span> <span data-ttu-id="71cb7-242">GDI 提供數種方式在執行時間建立點陣圖，但開發人員通常會使用下列方法：</span><span class="sxs-lookup"><span data-stu-id="71cb7-242">GDI provides several ways to create a bitmap at run time, but developers typically use the following method:</span></span>

1.  <span data-ttu-id="71cb7-243">使用 [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) 函式來建立與應用程式主視窗所用裝置內容相容的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="71cb7-243">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the device context used by the application's main window.</span></span>
2.  <span data-ttu-id="71cb7-244">您可以使用 [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) 函式來建立與應用程式主視窗相容的點陣圖，或使用 [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) 函式來建立單色點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-244">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window or use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>
3.  <span data-ttu-id="71cb7-245">使用 [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) 函式，在相容的裝置內容中選取點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-245">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="71cb7-246">使用 GDI 繪圖函式（例如 [**橢圓形**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) 和 [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto)），將影像繪製到點陣圖中。</span><span class="sxs-lookup"><span data-stu-id="71cb7-246">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap.</span></span>

<span data-ttu-id="71cb7-247">如需詳細資訊，請參閱 [點陣圖](/windows/desktop/gdi/bitmaps)。</span><span class="sxs-lookup"><span data-stu-id="71cb7-247">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="adding-lines-and-graphs-to-a-menu"></a><span data-ttu-id="71cb7-248">將線條和圖形新增至功能表</span><span class="sxs-lookup"><span data-stu-id="71cb7-248">Adding Lines and Graphs to a Menu</span></span>

<span data-ttu-id="71cb7-249">下列程式碼範例顯示如何建立包含功能表項目點陣圖的功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-249">The following code sample shows how to create a menu that contains menu-item bitmaps.</span></span> <span data-ttu-id="71cb7-250">它會建立兩個功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-250">It creates two menus.</span></span> <span data-ttu-id="71cb7-251">第一個是包含三個功能表項目點陣圖的圖表功能表：圓形圖、折線圖和橫條圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-251">The first is a Chart menu that contains three menu-item bitmaps: a pie chart, a line chart, and a bar chart.</span></span> <span data-ttu-id="71cb7-252">此範例示範如何從應用程式的資源檔載入這些點陣圖，然後使用 [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) 和 [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) 函式來建立功能表和功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-252">The example demonstrates how to load these bitmaps from the application's resource file, and then use the [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) and [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to create the menu and menu items.</span></span>

<span data-ttu-id="71cb7-253">第二個功能表是行功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-253">The second menu is a Lines menu.</span></span> <span data-ttu-id="71cb7-254">它包含的點陣圖會顯示系統中預先定義的畫筆所提供的線條樣式。</span><span class="sxs-lookup"><span data-stu-id="71cb7-254">It contains bitmaps showing the line styles provided by the predefined pen in the system.</span></span> <span data-ttu-id="71cb7-255">線條樣式點陣圖是在執行時間使用 GDI 函數所建立。</span><span class="sxs-lookup"><span data-stu-id="71cb7-255">The line-style bitmaps are created at run time by using GDI functions.</span></span>

<span data-ttu-id="71cb7-256">以下是應用程式資源定義檔中點陣圖資源的定義。</span><span class="sxs-lookup"><span data-stu-id="71cb7-256">Here are the definitions of the bitmap resources in the application's resource-definition file.</span></span>


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



<span data-ttu-id="71cb7-257">以下是應用程式標頭檔的相關部分。</span><span class="sxs-lookup"><span data-stu-id="71cb7-257">Here are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



<span data-ttu-id="71cb7-258">下列範例顯示如何在應用程式中建立功能表和功能表項目點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-258">The following example shows how menus and menu-item bitmaps are created in an application.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a><span data-ttu-id="71cb7-259">Menu-Item 點陣圖範例</span><span class="sxs-lookup"><span data-stu-id="71cb7-259">Example of Menu-Item Bitmaps</span></span>

<span data-ttu-id="71cb7-260">本主題中的範例會建立兩個功能表，每個都包含數個位圖功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-260">The example in this topic creates two menus, each containing several bitmap menu items.</span></span> <span data-ttu-id="71cb7-261">應用程式會針對每個功能表，將對應的功能表名稱新增至主視窗的功能表列。</span><span class="sxs-lookup"><span data-stu-id="71cb7-261">For each menu, the application adds a corresponding menu name to the main window's menu bar.</span></span>

<span data-ttu-id="71cb7-262">第一個功能表包含顯示三種圖表類型的功能表項目：圓形圖、線條和橫條圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-262">The first menu contains menu items showing each of three chart types: pie, line, and bar.</span></span> <span data-ttu-id="71cb7-263">這些功能表項目的點陣圖會定義為資源，並使用 [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) 函數載入。</span><span class="sxs-lookup"><span data-stu-id="71cb7-263">The bitmaps for these menu items are defined as resources and are loaded by using the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function.</span></span> <span data-ttu-id="71cb7-264">與此功能表相關聯的是功能表列上的 [圖表] 功能表名稱。</span><span class="sxs-lookup"><span data-stu-id="71cb7-264">Associated with this menu is a "Chart" menu name on the menu bar.</span></span>

<span data-ttu-id="71cb7-265">第二個功能表包含的功能表項目，會顯示與 [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) 函式搭配使用的五個線條樣式： **PS \_ 固態**、 **ps \_ 虛線**、 **ps \_ 點**、 **ps \_ 點** 和 **ps \_ DASHDOTDOT**。</span><span class="sxs-lookup"><span data-stu-id="71cb7-265">The second menu contains menu items showing each of the five line styles used with the [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) function: **PS\_SOLID**, **PS\_DASH**, **PS\_DOT**, **PS\_DASHDOT**, and **PS\_DASHDOTDOT**.</span></span> <span data-ttu-id="71cb7-266">應用程式會在執行時間使用 GDI 繪圖函式建立這些功能表項目的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-266">The application creates the bitmaps for these menu items at run time using GDI drawing functions.</span></span> <span data-ttu-id="71cb7-267">與此功能表相關聯的是功能表列上的 **線條** 功能表名稱。</span><span class="sxs-lookup"><span data-stu-id="71cb7-267">Associated with this menu is a **Lines** menu name on the menu bar.</span></span>

<span data-ttu-id="71cb7-268">在應用程式的視窗程式中定義的是兩個位圖控制碼的靜態陣列。</span><span class="sxs-lookup"><span data-stu-id="71cb7-268">Defined in the application's window procedure are two static arrays of bitmap handles.</span></span> <span data-ttu-id="71cb7-269">一個陣列包含用於 **圖表** 功能表的三個位圖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-269">One array contains the handles of the three bitmaps used for the **Chart** menu.</span></span> <span data-ttu-id="71cb7-270">另一個則包含用於 **線條** 功能表的五個位圖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-270">The other contains the handles of the five bitmaps used for the **Lines** menu.</span></span> <span data-ttu-id="71cb7-271">處理 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息時，視窗程式會載入圖表點陣圖、建立行點陣圖，然後加入對應的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-271">When processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure loads the chart bitmaps, creates the line bitmaps, and then adds the corresponding menu items.</span></span> <span data-ttu-id="71cb7-272">處理 WM 損 [**\_ 毀**](/windows/desktop/winmsg/wm-destroy) 訊息時，視窗程式會刪除所有點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-272">When processing the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the window procedure deletes all of the bitmaps.</span></span>

<span data-ttu-id="71cb7-273">以下是應用程式標頭檔的相關部分。</span><span class="sxs-lookup"><span data-stu-id="71cb7-273">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



<span data-ttu-id="71cb7-274">以下是視窗程式的相關部分。</span><span class="sxs-lookup"><span data-stu-id="71cb7-274">Following are the relevant portions of the window procedure.</span></span> <span data-ttu-id="71cb7-275">視窗程式會藉由呼叫應用程式定義的 LoadChartBitmaps、CreateLineBitmaps 和 AddBitmapMenu 函式來執行大部分的初始化，本主題稍後會加以說明。</span><span class="sxs-lookup"><span data-stu-id="71cb7-275">The window procedure performs most of its initialization by calling the application-defined LoadChartBitmaps, CreateLineBitmaps, and AddBitmapMenu functions, described later in this topic.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



<span data-ttu-id="71cb7-276">應用程式定義的 LoadChartBitmaps 函式會藉由呼叫 [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) 函式來載入圖表功能表的點陣圖資源，如下所示。</span><span class="sxs-lookup"><span data-stu-id="71cb7-276">The application-defined LoadChartBitmaps function loads the bitmap resources for the chart menu by calling the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, as follows.</span></span>


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



<span data-ttu-id="71cb7-277">應用程式定義的 CreateLineBitmaps 函式會使用 GDI 繪圖函式來建立線條功能表的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-277">The application-defined CreateLineBitmaps function creates the bitmaps for the Lines menu by using GDI drawing functions.</span></span> <span data-ttu-id="71cb7-278">此函式會使用與桌面視窗 DC 相同的屬性，建立 (DC) 的記憶體裝置內容。</span><span class="sxs-lookup"><span data-stu-id="71cb7-278">The function creates a memory device context (DC) with the same properties as the desktop window's DC.</span></span> <span data-ttu-id="71cb7-279">針對每個線條樣式，此函式會建立點陣圖、將其選取至記憶體 DC，然後在其中繪製。</span><span class="sxs-lookup"><span data-stu-id="71cb7-279">For each line style, the function creates a bitmap, selects it into the memory DC, and draws in it.</span></span>


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



<span data-ttu-id="71cb7-280">應用程式定義的 AddBitmapMenu 函式會建立功能表，並在其中加入指定的點陣圖功能表項目數目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-280">The application-defined AddBitmapMenu function creates a menu and adds the specified number of bitmap menu items to it.</span></span> <span data-ttu-id="71cb7-281">然後，它會將對應的功能表名稱新增至指定之視窗的功能表列。</span><span class="sxs-lookup"><span data-stu-id="71cb7-281">Then it adds a corresponding menu name to the specified window's menu bar.</span></span>


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a><span data-ttu-id="71cb7-282">建立 Owner-Drawn 功能表項目</span><span class="sxs-lookup"><span data-stu-id="71cb7-282">Creating Owner-Drawn Menu Items</span></span>

<span data-ttu-id="71cb7-283">如果您需要完全掌控功能表項目的外觀，您可以在應用程式中使用主控描繪功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-283">If you need complete control over the appearance of a menu item, you can use an owner-drawn menu item in your application.</span></span> <span data-ttu-id="71cb7-284">本節說明建立和使用主控描繪功能表項目所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="71cb7-284">This section describes the steps involved in creating and using an owner-drawn menu item.</span></span>

-   [<span data-ttu-id="71cb7-285">設定 Owner-Drawn 旗標</span><span class="sxs-lookup"><span data-stu-id="71cb7-285">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
-   [<span data-ttu-id="71cb7-286">擁有者繪製的功能表和 WM \_ MEASUREITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-286">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
-   [<span data-ttu-id="71cb7-287">擁有者繪製的功能表和 WM \_ DRAWITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-287">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
-   [<span data-ttu-id="71cb7-288">擁有者繪製的功能表和 WM \_ MENUCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-288">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
-   [<span data-ttu-id="71cb7-289">設定 Menu-Item 文字字串的字型</span><span class="sxs-lookup"><span data-stu-id="71cb7-289">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
-   [<span data-ttu-id="71cb7-290">Owner-Drawn 功能表項目的範例</span><span class="sxs-lookup"><span data-stu-id="71cb7-290">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a><span data-ttu-id="71cb7-291">設定 Owner-Drawn 旗標</span><span class="sxs-lookup"><span data-stu-id="71cb7-291">Setting the Owner-Drawn Flag</span></span>

<span data-ttu-id="71cb7-292">您無法在應用程式的資源定義檔中定義主控描繪功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-292">You cannot define an owner-drawn menu item in your application's resource-definition file.</span></span> <span data-ttu-id="71cb7-293">相反地，您必須使用 [ **MFT \_ OWNERDRAW** ] 功能表旗標建立新的功能表項目，或修改現有的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-293">Instead, you must create a new menu item or modify an existing one by using the **MFT\_OWNERDRAW** menu flag.</span></span>

<span data-ttu-id="71cb7-294">您可以使用 [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) 或 [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) 函數來指定主控描繪功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-294">You can use the [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) or [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function to specify an owner-drawn menu item.</span></span> <span data-ttu-id="71cb7-295">使用 **InsertMenuItem** 在功能表列或功能表中的指定位置插入新的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-295">Use **InsertMenuItem** to insert a new menu item at the specified position in a menu bar or menu.</span></span> <span data-ttu-id="71cb7-296">使用 **SetMenuItemInfo** 來變更功能表的內容。</span><span class="sxs-lookup"><span data-stu-id="71cb7-296">Use **SetMenuItemInfo** to change the contents of a menu.</span></span>

<span data-ttu-id="71cb7-297">呼叫這兩個函式時，您必須指定 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) 結構的指標，以指定新功能表項目的屬性，或您想要變更現有功能表項目的屬性。</span><span class="sxs-lookup"><span data-stu-id="71cb7-297">When calling these two functions, you must specify a pointer to a [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, which specifies the properties of the new menu item or the properties you want to change for an existing menu item.</span></span> <span data-ttu-id="71cb7-298">若要將專案設為主控描繪專案，請為 **fMask** 成員指定 **MIIM \_ FTYPE** 值，並為 **FTYPE** 成員指定 **MFT \_ OWNERDRAW** 值。</span><span class="sxs-lookup"><span data-stu-id="71cb7-298">To make an item an owner-drawn item, specify the **MIIM\_FTYPE** value for the **fMask** member and the **MFT\_OWNERDRAW** value for the **fType** member.</span></span>

<span data-ttu-id="71cb7-299">藉由設定 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) 結構的適當成員，您可以將應用程式定義的值（稱為 **專案資料**）與每個功能表項目產生關聯。</span><span class="sxs-lookup"><span data-stu-id="71cb7-299">By setting the appropriate members of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, you can associate an application-defined value, which is called **item data**, with each menu item.</span></span> <span data-ttu-id="71cb7-300">若要這樣做，請指定 **fMask** 成員的 **MIIM \_ 資料** 值，以及 **dwItemData** 成員的應用程式定義值。</span><span class="sxs-lookup"><span data-stu-id="71cb7-300">To do so, specify the **MIIM\_DATA** value for the **fMask** member and the application-defined value for the **dwItemData** member.</span></span>

<span data-ttu-id="71cb7-301">您可以使用專案資料與任何類型的功能表項目，但對於主控描繪的專案特別有用。</span><span class="sxs-lookup"><span data-stu-id="71cb7-301">You can use item data with any type of menu item, but it is particularly useful for owner-drawn items.</span></span> <span data-ttu-id="71cb7-302">例如，假設結構包含用來繪製功能表項目的資訊。</span><span class="sxs-lookup"><span data-stu-id="71cb7-302">For example, suppose a structure contains information used to draw a menu item.</span></span> <span data-ttu-id="71cb7-303">應用程式可能會使用功能表項目的專案資料來儲存結構的指標。</span><span class="sxs-lookup"><span data-stu-id="71cb7-303">An application might use the item data for a menu item to store a pointer to the structure.</span></span> <span data-ttu-id="71cb7-304">專案資料會以 [**wm \_ MEASUREITEM**](../controls/wm-measureitem.md) 和 [**wm \_ DRAWITEM**](../controls/wm-drawitem.md) 訊息傳送至功能表的擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="71cb7-304">The item data is sent to the menu's owner window with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages.</span></span> <span data-ttu-id="71cb7-305">若要隨時取出功能表的專案資料，請使用 [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) 函數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-305">To retrieve the item data for a menu at any time, use the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function.</span></span>

<span data-ttu-id="71cb7-306">針對舊版系統所撰寫的應用程式可以繼續呼叫 [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)、 [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)或 [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) ，將 **MF \_ OWNERDRAW** 旗標指派給主控描繪的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-306">Applications written for earlier versions of the system can continue to call [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) to assign the **MF\_OWNERDRAW** flag to an owner-drawn menu item.</span></span>

<span data-ttu-id="71cb7-307">當您呼叫這三個函式中的任一個時，您可以傳遞值作為 *lpNewItem* 參數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-307">When you call any of these three functions, you can pass a value as the *lpNewItem* parameter.</span></span> <span data-ttu-id="71cb7-308">這個值可以代表對您的應用程式有意義的任何資訊，而且當專案顯示時，將可供您的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="71cb7-308">This value can represent any information that is meaningful to your application, and that will be available to your application when the item is to be displayed.</span></span> <span data-ttu-id="71cb7-309">例如，值可能包含結構的指標;結構接著可能包含文字字串，以及您的應用程式將用來繪製字串的邏輯字型控制碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-309">For example, the value could contain a pointer to a structure; the structure, in turn, might contain a text string and a handle to the logical font your application will use to draw the string.</span></span>

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a><span data-ttu-id="71cb7-310">Owner-Drawn 功能表和 WM \_ MEASUREITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-310">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>

<span data-ttu-id="71cb7-311">在系統第一次顯示主控描繪功能表項目之前，它會將 [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) 訊息傳送到擁有專案功能表之視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="71cb7-311">Before the system displays an owner-drawn menu item for the first time, it sends the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message to the window procedure of the window that owns the item's menu.</span></span> <span data-ttu-id="71cb7-312">此訊息包含 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) 結構的指標，此結構會識別專案並包含應用程式可能已指派給它的專案資料。</span><span class="sxs-lookup"><span data-stu-id="71cb7-312">This message contains a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the item and contains the item data that an application may have assigned to it.</span></span> <span data-ttu-id="71cb7-313">視窗程式必須填滿結構的 **itemWidth** 和 **itemHeight** 成員，才能從處理訊息傳回。</span><span class="sxs-lookup"><span data-stu-id="71cb7-313">The window procedure must fill the **itemWidth** and **itemHeight** members of the structure before returning from processing the message.</span></span> <span data-ttu-id="71cb7-314">當建立應用程式繪製功能表項目的周框時，系統會使用這些成員中的資訊。</span><span class="sxs-lookup"><span data-stu-id="71cb7-314">The system uses the information in these members when creating the bounding rectangle in which an application draws the menu item.</span></span> <span data-ttu-id="71cb7-315">它也會使用此資訊來偵測使用者選擇此專案的時間。</span><span class="sxs-lookup"><span data-stu-id="71cb7-315">It also uses the information to detect when the user chooses the item.</span></span>

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a><span data-ttu-id="71cb7-316">Owner-Drawn 功能表和 WM \_ DRAWITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-316">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>

<span data-ttu-id="71cb7-317">每次必須繪製專案時 (例如，第一次顯示時，或當使用者選取) 時，系統會將 [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) 訊息傳送至功能表的擁有者視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="71cb7-317">Whenever the item must be drawn (for example, when it is first displayed or when the user selects it), the system sends the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message to the window procedure of the menu's owner window.</span></span> <span data-ttu-id="71cb7-318">此訊息包含 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構的指標，其中包含專案的相關資訊，包括應用程式可能已指派給它的專案資料。</span><span class="sxs-lookup"><span data-stu-id="71cb7-318">This message contains a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure, which contains information about the item, including the item data that an application may have assigned to it.</span></span> <span data-ttu-id="71cb7-319">此外， **DRAWITEMSTRUCT** 包含旗標，指出專案的狀態 (例如它是灰色還是選取的) ，以及應用程式用來繪製專案的周框和裝置內容。</span><span class="sxs-lookup"><span data-stu-id="71cb7-319">In addition, **DRAWITEMSTRUCT** contains flags that indicate the state of the item (such as whether it is grayed or selected) as well as a bounding rectangle and a device context that the application uses to draw the item.</span></span>

<span data-ttu-id="71cb7-320">處理 [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) 訊息時，應用程式必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="71cb7-320">An application must do the following while processing the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message:</span></span>

-   <span data-ttu-id="71cb7-321">判斷所需的繪圖類型。</span><span class="sxs-lookup"><span data-stu-id="71cb7-321">Determine the type of drawing that is necessary.</span></span> <span data-ttu-id="71cb7-322">若要這樣做，請檢查 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 **itemAction** 成員。</span><span class="sxs-lookup"><span data-stu-id="71cb7-322">To do so, check the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span>
-   <span data-ttu-id="71cb7-323">使用從 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構取得的周框和裝置內容，適當地繪製功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-323">Draw the menu item appropriately, using the bounding rectangle and device context obtained from the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="71cb7-324">應用程式必須只在周框中繪製。</span><span class="sxs-lookup"><span data-stu-id="71cb7-324">The application must draw only within the bounding rectangle.</span></span> <span data-ttu-id="71cb7-325">基於效能的考慮，系統不會裁剪在矩形之外繪製的影像部分。</span><span class="sxs-lookup"><span data-stu-id="71cb7-325">For performance reasons, the system does not clip portions of the image that are drawn outside the rectangle.</span></span>
-   <span data-ttu-id="71cb7-326">還原為功能表項目的裝置內容選取的所有 GDI 物件。</span><span class="sxs-lookup"><span data-stu-id="71cb7-326">Restore all GDI objects selected for the menu item's device context.</span></span>

<span data-ttu-id="71cb7-327">如果使用者選取功能表項目，系統會將 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 **itemAction** 成員設定為 **ODA \_ SELECT** 值，並在 **itemState** 成員中設定 **ODS \_ 選取** 的值。</span><span class="sxs-lookup"><span data-stu-id="71cb7-327">If the user selects the menu item, the system sets the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure to the **ODA\_SELECT** value and sets the **ODS\_SELECTED** value in the **itemState** member.</span></span> <span data-ttu-id="71cb7-328">這是應用程式用來重繪功能表項目的提示，表示已選取該功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-328">This is an application's cue to redraw the menu item to indicate that it is selected.</span></span>

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a><span data-ttu-id="71cb7-329">Owner-Drawn 功能表和 WM \_ MENUCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="71cb7-329">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>

<span data-ttu-id="71cb7-330">主控描繪功能表以外的功能表，可以藉由在功能表字串中的字元旁插入底線來指定功能表助憶鍵。</span><span class="sxs-lookup"><span data-stu-id="71cb7-330">Menus other than owner-drawn menus can specify a menu mnemonic by inserting an underscore next to a character in the menu string.</span></span> <span data-ttu-id="71cb7-331">這可讓使用者按下 ALT 鍵，然後按下功能表的助憶鍵字元，以選取功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-331">This allows the user to select the menu by pressing ALT and pressing the menu mnemonic character.</span></span> <span data-ttu-id="71cb7-332">不過，在主控描繪的功能表中，您無法以這種方式指定功能表助憶鍵。</span><span class="sxs-lookup"><span data-stu-id="71cb7-332">In owner-drawn menus, however, you cannot specify a menu mnemonic in this manner.</span></span> <span data-ttu-id="71cb7-333">相反地，您的應用程式必須處理 [**WM \_ MENUCHAR**](wm-menuchar.md) 訊息，以提供擁有者繪製的功能表與功能表的助憶鍵。</span><span class="sxs-lookup"><span data-stu-id="71cb7-333">Instead, your application must process the [**WM\_MENUCHAR**](wm-menuchar.md) message to provide owner-drawn menus with menu mnemonics.</span></span>

<span data-ttu-id="71cb7-334">當使用者輸入的功能表助憶鍵不符合目前功能表的任何預先定義的助憶鍵時，就會傳送 [**WM \_ MENUCHAR**](wm-menuchar.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="71cb7-334">The [**WM\_MENUCHAR**](wm-menuchar.md) message is sent when the user types a menu mnemonic that does not match any of the predefined mnemonics of the current menu.</span></span> <span data-ttu-id="71cb7-335">*WParam* 中所含的值會指定與使用者按下 ALT 鍵時所按下之按鍵對應的 ASCII 字元。</span><span class="sxs-lookup"><span data-stu-id="71cb7-335">The value contained in *wParam* specifies the ASCII character that corresponds to the key the user pressed with the ALT key.</span></span> <span data-ttu-id="71cb7-336">*WParam* 的低序位文字會指定所選功能表的類型，而且可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="71cb7-336">The low-order word of *wParam* specifies the type of the selected menu and can be one of the following values:</span></span>

-   <span data-ttu-id="71cb7-337">**MF \_** 如果目前的功能表是子功能表，則為快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="71cb7-337">**MF\_POPUP** if the current menu is a submenu.</span></span>
-   <span data-ttu-id="71cb7-338">**MF \_SYSMENU** ：如果功能表是 [系統] 功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-338">**MF\_SYSMENU** if the menu is the system menu.</span></span>

<span data-ttu-id="71cb7-339">*WParam* 的高序位字包含目前功能表的功能表控點。</span><span class="sxs-lookup"><span data-stu-id="71cb7-339">The high-order word of *wParam* contains the menu handle to the current menu.</span></span> <span data-ttu-id="71cb7-340">具有主控描繪功能表的視窗可以處理 [**WM \_ MENUCHAR**](wm-menuchar.md) ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="71cb7-340">The window with the owner-drawn menus can process [**WM\_MENUCHAR**](wm-menuchar.md) as follows:</span></span>


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



<span data-ttu-id="71cb7-341">傳回值的高序位字組中的兩個會通知系統，傳回值的低序位文字包含要選取之功能表項目的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="71cb7-341">The two in the high-order word of the return value informs the system that the low-order word of the return value contains the zero-based index of the menu item to be selected.</span></span>

<span data-ttu-id="71cb7-342">下列常數對應至來自 [**WM \_ MENUCHAR**](wm-menuchar.md) 訊息的可能傳回值。</span><span class="sxs-lookup"><span data-stu-id="71cb7-342">The following constants correspond to the possible return values from the [**WM\_MENUCHAR**](wm-menuchar.md) message.</span></span>



| <span data-ttu-id="71cb7-343">常數</span><span class="sxs-lookup"><span data-stu-id="71cb7-343">Constant</span></span>         | <span data-ttu-id="71cb7-344">值</span><span class="sxs-lookup"><span data-stu-id="71cb7-344">Value</span></span> | <span data-ttu-id="71cb7-345">意義</span><span class="sxs-lookup"><span data-stu-id="71cb7-345">Meaning</span></span>                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71cb7-346">**MNC \_ IGNORE**</span><span class="sxs-lookup"><span data-stu-id="71cb7-346">**MNC\_IGNORE**</span></span>  | <span data-ttu-id="71cb7-347">0</span><span class="sxs-lookup"><span data-stu-id="71cb7-347">0</span></span>     | <span data-ttu-id="71cb7-348">系統應該捨棄使用者所按下的字元，並在系統喇叭上建立短暫的嗶聲。</span><span class="sxs-lookup"><span data-stu-id="71cb7-348">The system should discard the character the user pressed and create a short beep on the system speaker.</span></span>                                                       |
| <span data-ttu-id="71cb7-349">**MNC \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="71cb7-349">**MNC\_CLOSE**</span></span>   | <span data-ttu-id="71cb7-350">1</span><span class="sxs-lookup"><span data-stu-id="71cb7-350">1</span></span>     | <span data-ttu-id="71cb7-351">系統應該關閉使用中的功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-351">The system should close the active menu.</span></span>                                                                                                                      |
| <span data-ttu-id="71cb7-352">**MNC \_ EXECUTE**</span><span class="sxs-lookup"><span data-stu-id="71cb7-352">**MNC\_EXECUTE**</span></span> | <span data-ttu-id="71cb7-353">2</span><span class="sxs-lookup"><span data-stu-id="71cb7-353">2</span></span>     | <span data-ttu-id="71cb7-354">系統應選擇傳回值的低序位字組中指定的專案。</span><span class="sxs-lookup"><span data-stu-id="71cb7-354">The system should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="71cb7-355">擁有者視窗會收到 [**WM \_ 命令**](wm-command.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="71cb7-355">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span> |
| <span data-ttu-id="71cb7-356">**MNC \_ SELECT**</span><span class="sxs-lookup"><span data-stu-id="71cb7-356">**MNC\_SELECT**</span></span>  | <span data-ttu-id="71cb7-357">3</span><span class="sxs-lookup"><span data-stu-id="71cb7-357">3</span></span>     | <span data-ttu-id="71cb7-358">系統應選取傳回值的低序位字組中指定的專案。</span><span class="sxs-lookup"><span data-stu-id="71cb7-358">The system should select the item specified in the low-order word of the return value.</span></span>                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a><span data-ttu-id="71cb7-359">設定 Menu-Item 文字字串的字型</span><span class="sxs-lookup"><span data-stu-id="71cb7-359">Setting Fonts for Menu-Item Text Strings</span></span>

<span data-ttu-id="71cb7-360">本主題包含在功能表中使用主控描繪功能表項目的應用程式範例。</span><span class="sxs-lookup"><span data-stu-id="71cb7-360">This topic contains an example from an application that uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="71cb7-361">功能表中包含的專案會設定目前字型的屬性，而且會使用適當的字型屬性來顯示專案。</span><span class="sxs-lookup"><span data-stu-id="71cb7-361">The menu contains items that set the attributes of the current font, and the items are displayed using the appropriate font attribute.</span></span>

<span data-ttu-id="71cb7-362">以下是在資源定義檔中定義功能表的方式。</span><span class="sxs-lookup"><span data-stu-id="71cb7-362">Here is how the menu is defined in the resource-definition file.</span></span> <span data-ttu-id="71cb7-363">請注意，一般、粗體、斜體和底線功能表項目的字串會在執行時間指派，因此其在資源定義檔中的字串是空的。</span><span class="sxs-lookup"><span data-stu-id="71cb7-363">Note that the strings for the Regular, Bold, Italic, and Underline menu items are assigned at run time, so their strings are empty in the resource-definition file.</span></span>


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



<span data-ttu-id="71cb7-364">應用程式的視窗程式會處理有關使用主控描繪功能表項目的訊息。</span><span class="sxs-lookup"><span data-stu-id="71cb7-364">The application's window procedure processes the messages involved in using owner-drawn menu items.</span></span> <span data-ttu-id="71cb7-365">應用程式會使用 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息來執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="71cb7-365">The application uses the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to do the following:</span></span>

-   <span data-ttu-id="71cb7-366">設定功能表項目的 **MF \_ OWNERDRAW** 旗標。</span><span class="sxs-lookup"><span data-stu-id="71cb7-366">Set the **MF\_OWNERDRAW** flag for the menu items.</span></span>
-   <span data-ttu-id="71cb7-367">設定功能表項目的文字字串。</span><span class="sxs-lookup"><span data-stu-id="71cb7-367">Set the text strings for the menu items.</span></span>
-   <span data-ttu-id="71cb7-368">取得用來繪製專案之字型的控制碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-368">Obtain handles of the fonts used to draw the items.</span></span>
-   <span data-ttu-id="71cb7-369">取得選定功能表項目的文字和背景色彩值。</span><span class="sxs-lookup"><span data-stu-id="71cb7-369">Obtain the text and background color values for selected menu items.</span></span>

<span data-ttu-id="71cb7-370">文字字串和字型控制碼會儲存在應用程式定義 MYITEM 結構的陣列中。</span><span class="sxs-lookup"><span data-stu-id="71cb7-370">The text strings and font handles are stored in an array of application-defined MYITEM structures.</span></span> <span data-ttu-id="71cb7-371">應用程式定義的 GetAFont 函式會建立對應至指定字型屬性的字型，並將控制碼傳回給字型。</span><span class="sxs-lookup"><span data-stu-id="71cb7-371">The application-defined GetAFont function creates a font that corresponds to the specified font attribute and returns a handle to the font.</span></span> <span data-ttu-id="71cb7-372">處理 [**WM \_**](/windows/desktop/winmsg/wm-destroy) 終結訊息時，會終結控制碼。</span><span class="sxs-lookup"><span data-stu-id="71cb7-372">The handles are destroyed during the processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>

<span data-ttu-id="71cb7-373">在處理 [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) 訊息期間，範例會取得功能表項目字串的寬度和高度，並將這些值複製到 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) 結構中。</span><span class="sxs-lookup"><span data-stu-id="71cb7-373">During the processing of the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message, the example gets the width and height of a menu-item string and copies these values into the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure.</span></span> <span data-ttu-id="71cb7-374">系統會使用 [寬度] 和 [高度] 值來計算功能表的大小。</span><span class="sxs-lookup"><span data-stu-id="71cb7-374">The system uses the width and height values to calculate the size of the menu.</span></span>

<span data-ttu-id="71cb7-375">在處理 [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) 訊息期間，會繪製功能表項目的字串，並在核取記號點陣圖的字串旁邊留下空間。</span><span class="sxs-lookup"><span data-stu-id="71cb7-375">During the processing of the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message, the menu item's string is drawn with room left next to the string for the check-mark bitmap.</span></span> <span data-ttu-id="71cb7-376">如果使用者選取該專案，則會使用選取的文字和背景色彩來繪製專案。</span><span class="sxs-lookup"><span data-stu-id="71cb7-376">If the user selects the item, the selected text and background colors are used to draw the item.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a><span data-ttu-id="71cb7-377">Owner-Drawn 功能表項目的範例</span><span class="sxs-lookup"><span data-stu-id="71cb7-377">Example of Owner-Drawn Menu Items</span></span>

<span data-ttu-id="71cb7-378">本主題中的範例會使用功能表中的主控描繪功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-378">The example in this topic uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="71cb7-379">功能表項目會選取特定的字型屬性，而應用程式會使用具有對應屬性的字型來顯示每個功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-379">The menu items select specific font attributes, and the application displays each menu item using a font that has the corresponding attribute.</span></span> <span data-ttu-id="71cb7-380">例如， **斜體** 功能表項目會以斜體字型顯示。</span><span class="sxs-lookup"><span data-stu-id="71cb7-380">For example, the **Italic** menu item is displayed in an italic font.</span></span> <span data-ttu-id="71cb7-381">功能表列上的 **字元** 功能表名稱會開啟功能表。</span><span class="sxs-lookup"><span data-stu-id="71cb7-381">The **Character** menu name on the menu bar opens the menu.</span></span>

<span data-ttu-id="71cb7-382">功能表列和下拉式功能表最初是由擴充功能表範本資源所定義。</span><span class="sxs-lookup"><span data-stu-id="71cb7-382">The menu bar and drop-down menu are defined initially by an extended menu-template resource.</span></span> <span data-ttu-id="71cb7-383">因為功能表範本無法指定主控描繪的專案，所以功能表一開始會包含四個具有下列字串的文字功能表項目：「一般」、「粗體」、「斜體」和「底線」。</span><span class="sxs-lookup"><span data-stu-id="71cb7-383">Because a menu template cannot specify owner-drawn items, the menu initially contains four text menu items with the following strings: "Regular," "Bold," "Italic," and "Underline."</span></span> <span data-ttu-id="71cb7-384">應用程式的視窗程式在處理 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息時，會將這些專案變更為主控描繪專案。</span><span class="sxs-lookup"><span data-stu-id="71cb7-384">The application's window procedure changes these to owner-drawn items when it processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="71cb7-385">當它收到 **WM \_ 建立** 訊息時，視窗程式會呼叫應用程式定義的 >oncreate 函式，此函式會針對每個功能表項目執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="71cb7-385">When it receives the **WM\_CREATE** message, the window procedure calls the application-defined OnCreate function, which performs the following steps for each menu item:</span></span>

-   <span data-ttu-id="71cb7-386">配置應用程式定義的 MYITEM 結構。</span><span class="sxs-lookup"><span data-stu-id="71cb7-386">Allocates an application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="71cb7-387">取得功能表項目的文字，並將它儲存在應用程式定義的 MYITEM 結構中。</span><span class="sxs-lookup"><span data-stu-id="71cb7-387">Gets the text of the menu item and saves it in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="71cb7-388">建立用來顯示功能表項目的字型，並將其控制碼儲存在應用程式定義的 MYITEM 結構中。</span><span class="sxs-lookup"><span data-stu-id="71cb7-388">Creates the font used to display the menu item and saves its handle in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="71cb7-389">將功能表項目類型變更為 **MFT \_ OWNERDRAW** ，並將應用程式定義的 MYITEM 結構指標儲存為專案資料。</span><span class="sxs-lookup"><span data-stu-id="71cb7-389">Changes the menu item type to **MFT\_OWNERDRAW** and saves a pointer to the application-defined MYITEM structure as item data.</span></span>

<span data-ttu-id="71cb7-390">由於每個應用程式定義的 MYITEM 結構的指標都會儲存為專案資料，因此會將它傳遞給視窗程式，並結合了 [**wm \_ MEASUREITEM**](../controls/wm-measureitem.md) 和 [**wm \_ DRAWITEM**](../controls/wm-drawitem.md) 訊息來取得對應的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-390">Because a pointer to each application-defined MYITEM structure is saved as item data, it is passed to the window procedure in conjunction with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages for the corresponding menu item.</span></span> <span data-ttu-id="71cb7-391">指標包含在 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)和 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 **itemData** 成員中。</span><span class="sxs-lookup"><span data-stu-id="71cb7-391">The pointer is contained in the **itemData** member of both the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) and [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structures.</span></span>

<span data-ttu-id="71cb7-392">第一次顯示每個主控描繪功能表項目時，會傳送一個 [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="71cb7-392">A [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message is sent for each owner-drawn menu item the first time it is displayed.</span></span> <span data-ttu-id="71cb7-393">應用程式會藉由選取功能表項目的字型至裝置內容，然後判斷在該字型中顯示功能表項目文字所需的空間，來處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="71cb7-393">The application processes this message by selecting the font for the menu item into a device context and then determining the space required to display the menu item text in that font.</span></span> <span data-ttu-id="71cb7-394">字型和功能表項目文字都是由功能表項目的結構所指定， `MYITEM` (應用程式) 所定義的結構。</span><span class="sxs-lookup"><span data-stu-id="71cb7-394">The font and menu item text are both specified by the menu item's `MYITEM` structure (the structure defined by the application).</span></span> <span data-ttu-id="71cb7-395">應用程式會使用 [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) 函數來判斷文字的大小。</span><span class="sxs-lookup"><span data-stu-id="71cb7-395">The application determines the size of the text by using the [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) function.</span></span>

<span data-ttu-id="71cb7-396">視窗程式會藉由顯示適當字型中的功能表項目文字來處理 [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="71cb7-396">The window procedure processes the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message by displaying the menu item text in the appropriate font.</span></span> <span data-ttu-id="71cb7-397">字型和功能表項目文字都是由功能表項目的結構所指定 `MYITEM` 。</span><span class="sxs-lookup"><span data-stu-id="71cb7-397">The font and menu item text are both specified by the menu item's `MYITEM` structure.</span></span> <span data-ttu-id="71cb7-398">應用程式會選取適合功能表項目狀態的文字和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="71cb7-398">The application selects text and background colors appropriate to the menu item's state.</span></span>

<span data-ttu-id="71cb7-399">視窗程式會處理 [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy) 訊息，以終結字型和可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="71cb7-399">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message to destroy fonts and free memory.</span></span> <span data-ttu-id="71cb7-400">應用程式會刪除字型，並釋出每個功能表項目的應用程式定義 MYITEM 結構。</span><span class="sxs-lookup"><span data-stu-id="71cb7-400">The application deletes the font and frees the application-defined MYITEM structure for each menu item.</span></span>

<span data-ttu-id="71cb7-401">以下是應用程式標頭檔的相關部分。</span><span class="sxs-lookup"><span data-stu-id="71cb7-401">The following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



<span data-ttu-id="71cb7-402">以下是應用程式的視窗程式及其相關聯的函式的相關部分。</span><span class="sxs-lookup"><span data-stu-id="71cb7-402">The following are the relevant portions of the application's window procedure and its associated functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a><span data-ttu-id="71cb7-403">使用自訂核取記號點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-403">Using Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="71cb7-404">系統會提供預設的核取記號點陣圖，以便在選取的功能表項目旁邊顯示。</span><span class="sxs-lookup"><span data-stu-id="71cb7-404">The system provides a default check-mark bitmap for displaying next to a menu item that is selected.</span></span> <span data-ttu-id="71cb7-405">您可以提供一組點陣圖來取代預設的核取記號點陣圖，以自訂個別的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-405">You can customize an individual menu item by providing a pair of bitmaps to replace the default check-mark bitmap.</span></span> <span data-ttu-id="71cb7-406">當選取專案時，系統會顯示一個點陣圖，另一個則是清除時。</span><span class="sxs-lookup"><span data-stu-id="71cb7-406">The system displays one bitmap when the item is selected and the other when it is clear.</span></span> <span data-ttu-id="71cb7-407">本節說明建立和使用自訂核取記號點陣圖時所牽涉到的步驟。</span><span class="sxs-lookup"><span data-stu-id="71cb7-407">This section describes the steps involved in creating and using custom check-mark bitmaps.</span></span>

-   [<span data-ttu-id="71cb7-408">建立自訂的核取記號點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-408">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
-   [<span data-ttu-id="71cb7-409">建立點陣圖與功能表項目的關聯</span><span class="sxs-lookup"><span data-stu-id="71cb7-409">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
-   [<span data-ttu-id="71cb7-410">設定核取記號屬性</span><span class="sxs-lookup"><span data-stu-id="71cb7-410">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
-   [<span data-ttu-id="71cb7-411">模擬功能表中的核取方塊</span><span class="sxs-lookup"><span data-stu-id="71cb7-411">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
-   [<span data-ttu-id="71cb7-412">使用自訂核取記號點陣圖的範例</span><span class="sxs-lookup"><span data-stu-id="71cb7-412">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a><span data-ttu-id="71cb7-413">建立自訂的核取記號點陣圖</span><span class="sxs-lookup"><span data-stu-id="71cb7-413">Creating Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="71cb7-414">自訂核取記號點陣圖的大小必須與預設的核取記號點陣圖相同。</span><span class="sxs-lookup"><span data-stu-id="71cb7-414">A custom check-mark bitmap must be the same size as the default check-mark bitmap.</span></span> <span data-ttu-id="71cb7-415">您可以藉由呼叫 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式來取出點陣圖的預設核取記號大小。</span><span class="sxs-lookup"><span data-stu-id="71cb7-415">You can retrieve the default check-mark size of the bitmap by calling the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="71cb7-416">此函式傳回值的低序位字組會指定寬度;高序位字組指定高度。</span><span class="sxs-lookup"><span data-stu-id="71cb7-416">The low-order word of this function's return value specifies the width; the high-order word specifies the height.</span></span>

<span data-ttu-id="71cb7-417">您可以使用點陣圖資源來提供核取記號點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-417">You can use bitmap resources to provide check-mark bitmaps.</span></span> <span data-ttu-id="71cb7-418">不過，由於所需的點陣圖大小會隨著顯示類型而有所不同，因此您可能需要使用 [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) 函式，在執行時間調整點陣圖的大小。</span><span class="sxs-lookup"><span data-stu-id="71cb7-418">However, because the required bitmap size varies depending on the display type, you may need to resize the bitmap at run time by using the [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) function.</span></span> <span data-ttu-id="71cb7-419">根據點陣圖，調整大小所造成的扭曲可能會產生無法接受的結果。</span><span class="sxs-lookup"><span data-stu-id="71cb7-419">Depending on the bitmap, the distortion caused by sizing could produce unacceptable results.</span></span>

<span data-ttu-id="71cb7-420">您可以使用 GDI 函數，在執行時間建立點陣圖，而不是使用點陣圖資源。</span><span class="sxs-lookup"><span data-stu-id="71cb7-420">Instead of using a bitmap resource, you can create a bitmap at run time by using GDI functions.</span></span>

<span data-ttu-id="71cb7-421">**若要在執行時間建立點陣圖**</span><span class="sxs-lookup"><span data-stu-id="71cb7-421">**To create a bitmap at run time**</span></span>

1.  <span data-ttu-id="71cb7-422">使用 [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) 函式來建立與應用程式主視窗所使用的裝置內容相容的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="71cb7-422">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the one used by the application's main window.</span></span>

    <span data-ttu-id="71cb7-423">函數的 *hdc* 參數可以指定函式的 **Null** 或傳回值。</span><span class="sxs-lookup"><span data-stu-id="71cb7-423">The function's *hdc* parameter can specify either **NULL** or the return value from the function.</span></span> <span data-ttu-id="71cb7-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) 會將控制碼傳回相容的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="71cb7-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) returns a handle to the compatible device context.</span></span>

2.  <span data-ttu-id="71cb7-425">您可以使用 [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) 函式來建立與應用程式主視窗相容的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-425">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window.</span></span>

    <span data-ttu-id="71cb7-426">這個函式的 *nWidth* 和 *nHeight* 參數會設定點陣圖的大小;它們應該指定 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式所傳回的寬度和高度資訊。</span><span class="sxs-lookup"><span data-stu-id="71cb7-426">This function's *nWidth* and *nHeight* parameters set the size of the bitmap; they should specify the width and height information returned by the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span>

    > [!Note]  
    > <span data-ttu-id="71cb7-427">您也可以使用 [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) 函式來建立單色點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-427">You can also use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>

     

3.  <span data-ttu-id="71cb7-428">使用 [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) 函式，在相容的裝置內容中選取點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-428">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="71cb7-429">使用 GDI 繪圖函式（例如 [**橢圓形**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) 和 [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto)）將影像繪製到點陣圖中，或使用 [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) 和 [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) 等函數將影像複製到點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-429">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap, or use functions such as [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) and [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) to copy an image into the bitmap.</span></span>

<span data-ttu-id="71cb7-430">如需詳細資訊，請參閱 [點陣圖](/windows/desktop/gdi/bitmaps)。</span><span class="sxs-lookup"><span data-stu-id="71cb7-430">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="associating-bitmaps-with-a-menu-item"></a><span data-ttu-id="71cb7-431">建立點陣圖與功能表項目的關聯</span><span class="sxs-lookup"><span data-stu-id="71cb7-431">Associating Bitmaps with a Menu Item</span></span>

<span data-ttu-id="71cb7-432">您可以藉由將點陣圖的控制碼傳遞至 [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) 函式，來建立一對核取記號點陣圖與功能表項目的關聯。</span><span class="sxs-lookup"><span data-stu-id="71cb7-432">You associate a pair of check-mark bitmaps with a menu item by passing the handles of the bitmaps to the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span> <span data-ttu-id="71cb7-433">*HBitmapUnchecked* 參數可識別 clear 點陣圖，而 *hBitmapChecked* 參數會識別選取的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-433">The *hBitmapUnchecked* parameter identifies the clear bitmap, and the *hBitmapChecked* parameter identifies the selected bitmap.</span></span> <span data-ttu-id="71cb7-434">如果您想要從功能表項目中移除一個或兩個核取記號，可以將 *hBitmapUnchecked* 或 *hBitmapChecked* 參數（或兩者）設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="71cb7-434">If you want to remove one or both check marks from a menu item, you can set the *hBitmapUnchecked* or *hBitmapChecked* parameter, or both, to **NULL**.</span></span>

### <a name="setting-the-check-mark-attribute"></a><span data-ttu-id="71cb7-435">設定核取記號屬性</span><span class="sxs-lookup"><span data-stu-id="71cb7-435">Setting the Check-mark Attribute</span></span>

<span data-ttu-id="71cb7-436">[**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)函式會將功能表項目的核取記號屬性設定為選取或清除。</span><span class="sxs-lookup"><span data-stu-id="71cb7-436">The [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) function sets a menu item's check-mark attribute to either selected or cleared.</span></span> <span data-ttu-id="71cb7-437">您可以指定 [ **mf \_ 已核** 取] 值，將核取記號屬性設定為 [已選取]，並將 [ **mf \_ 未** 核取值] 設定為 [清除]。</span><span class="sxs-lookup"><span data-stu-id="71cb7-437">You can specify the **MF\_CHECKED** value to set the check-mark attribute to selected and the **MF\_UNCHECKED** value to set it to clear.</span></span>

<span data-ttu-id="71cb7-438">您也可以使用 [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) 函數來設定功能表項目的檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="71cb7-438">You can also set the check state of a menu item by using the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="71cb7-439">有時一組功能表項目代表一組互斥的選項。</span><span class="sxs-lookup"><span data-stu-id="71cb7-439">Sometimes a group of menu items represents a set of mutually exclusive options.</span></span> <span data-ttu-id="71cb7-440">藉由使用 [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) 函式，您可以檢查一個功能表項目，同時從群組中的所有其他功能表項目中移除核取記號。</span><span class="sxs-lookup"><span data-stu-id="71cb7-440">By using the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function, you can check one menu item while simultaneously removing the check mark from all other menu items in the group.</span></span>

### <a name="simulating-check-boxes-in-a-menu"></a><span data-ttu-id="71cb7-441">模擬功能表中的核取方塊</span><span class="sxs-lookup"><span data-stu-id="71cb7-441">Simulating Check Boxes in a Menu</span></span>

<span data-ttu-id="71cb7-442">本主題包含的範例會示範如何模擬功能表中的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="71cb7-442">This topic contains an example that shows how to simulate check boxes in a menu.</span></span> <span data-ttu-id="71cb7-443">此範例包含的字元功能表，其專案可讓使用者設定目前字型的粗體、斜體和底線屬性。</span><span class="sxs-lookup"><span data-stu-id="71cb7-443">The example contains a Character menu whose items allow the user to set the bold, italic, and underline attributes of the current font.</span></span> <span data-ttu-id="71cb7-444">當字型屬性作用時，核取記號會顯示在對應功能表項目旁的核取方塊中;否則，專案旁邊會顯示空白的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="71cb7-444">When a font attribute is in effect, a check mark is displayed in the check box next to the corresponding menu item; otherwise, an empty check box is displayed next to the item.</span></span>

<span data-ttu-id="71cb7-445">此範例會使用兩個位圖來取代預設的核取記號點陣圖：具有已選取核取方塊的點陣圖和帶有空白方塊的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-445">The example replaces the default check-mark bitmap with two bitmaps: a bitmap with a selected check box and the bitmap with an empty box.</span></span> <span data-ttu-id="71cb7-446">當專案的核取記號屬性設定為 [ **MF \_ 已核** 取] 時，會在粗體、斜體或底線功能表項目旁邊顯示選取的核取方塊點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-446">The selected check box bitmap is displayed next to the Bold, Italic, or Underline menu item when the item's check-mark attribute is set to **MF\_CHECKED**.</span></span> <span data-ttu-id="71cb7-447">當核取記號屬性設定為 **\_ 未** 核取時，就會顯示清除或空白核取方塊點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-447">The clear or empty check box bitmap is displayed when the check-mark attribute is set to **MF\_UNCHECKED**.</span></span>

<span data-ttu-id="71cb7-448">系統會提供預先定義的點陣圖，其中包含用於核取方塊和選項按鈕的影像。</span><span class="sxs-lookup"><span data-stu-id="71cb7-448">The system provides a predefined bitmap that contains the images used for check boxes and radio buttons.</span></span> <span data-ttu-id="71cb7-449">此範例會隔離選取的和空白的核取方塊，將它們複製到兩個不同的點陣圖，然後將它們作為 **字元** 功能表中專案的已選取和清除點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-449">The example isolates the selected and empty check boxes, copies them to two separate bitmaps, and then uses them as the selected and cleared bitmaps for items in the **Character** menu.</span></span>

<span data-ttu-id="71cb7-450">為了取得系統定義之核取方塊點陣圖的控制碼，此範例會呼叫 [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) 函式，並將 **Null** 指定為 *HInstance* 參數，並以 **OBM \_ 複選** 框作為 *lpBitmapName* 參數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-450">To retrieve a handle to the system-defined check box bitmap, the example calls the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, specifying **NULL** as the *hInstance* parameter and **OBM\_CHECKBOXES** as the *lpBitmapName* parameter.</span></span> <span data-ttu-id="71cb7-451">由於點陣圖中的影像大小都相同，因此，此範例可以將點陣圖寬度和高度除以其資料列和資料行中的影像數目來加以隔離。</span><span class="sxs-lookup"><span data-stu-id="71cb7-451">Because the images in the bitmap are all the same size, the example can isolate them by dividing the bitmap width and height by the number of images in its rows and columns.</span></span>

<span data-ttu-id="71cb7-452">資源定義檔的下列部分會顯示如何定義 **字元** 功能表中的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-452">The following portion of a resource-definition file shows how the menu items in the **Character** menu are defined.</span></span> <span data-ttu-id="71cb7-453">請注意，一開始沒有任何字型屬性，因此 **一般** 專案的核取記號屬性會設定為 [已選取]，而其餘專案的 [核取記號] 屬性預設會設定為 [清除]。</span><span class="sxs-lookup"><span data-stu-id="71cb7-453">Note that no font attributes are in effect initially, so the check-mark attribute for the **Regular** item is set to selected and, by default, the check-mark attribute of the remaining items is set to clear.</span></span>


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



<span data-ttu-id="71cb7-454">以下是應用程式標頭檔的相關內容。</span><span class="sxs-lookup"><span data-stu-id="71cb7-454">Here are the relevant contents of the application's header file.</span></span>


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



<span data-ttu-id="71cb7-455">下列範例顯示建立核取記號點陣圖的視窗程式部分。設定 **粗體**、 **斜體** 和 **底線功能表項目** 的核取記號屬性;並損毀核取記號點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-455">The following example shows the portions of the window procedure that create the check-mark bitmaps; set the check-mark attribute of the **Bold**, **Italic**, and **Underline** menu items; and destroy check-mark bitmaps.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a><span data-ttu-id="71cb7-456">使用自訂核取記號點陣圖的範例</span><span class="sxs-lookup"><span data-stu-id="71cb7-456">Example of Using Custom Check-mark Bitmaps</span></span>

<span data-ttu-id="71cb7-457">本主題中的範例會在兩個功能表中將自訂的核取記號點陣圖指派給功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-457">The example in this topic assigns custom check-mark bitmaps to menu items in two menus.</span></span> <span data-ttu-id="71cb7-458">第一個功能表中的功能表項目會指定字元屬性：粗體、斜體和底線。</span><span class="sxs-lookup"><span data-stu-id="71cb7-458">The menu items in the first menu specify character attributes: bold, italic, and underline.</span></span> <span data-ttu-id="71cb7-459">您可以選取或清除每個功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-459">Each menu item can be either selected or cleared.</span></span> <span data-ttu-id="71cb7-460">針對這些功能表項目，此範例會使用類似核取方塊控制項之選取和清除狀態的核取記號點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-460">For these menu items, the example uses check-mark bitmaps that resemble the selected and cleared states of a check box control.</span></span>

<span data-ttu-id="71cb7-461">第二個功能表中的功能表項目會指定段落對齊設定：靠左、置中、靠右。</span><span class="sxs-lookup"><span data-stu-id="71cb7-461">The menu items in the second menu specify paragraph alignment settings: left, centered, and right.</span></span> <span data-ttu-id="71cb7-462">任何時候都只會選取其中一個功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-462">Only one of these menu items is selected at any time.</span></span> <span data-ttu-id="71cb7-463">針對這些功能表項目，此範例會使用類似選項按鈕控制項選取和清除狀態的核取記號點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71cb7-463">For these menu items, the example uses check-mark bitmaps that resemble the selected and clear states of a radio button control.</span></span>

<span data-ttu-id="71cb7-464">視窗程式會藉由呼叫應用程式定義的 >oncreate 函數來處理 [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) message。</span><span class="sxs-lookup"><span data-stu-id="71cb7-464">The window procedure processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message by calling the application-defined OnCreate function.</span></span> <span data-ttu-id="71cb7-465">`OnCreate` 建立四個核取記號點陣圖，然後使用 [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) 函式將它們指派給其適當的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="71cb7-465">`OnCreate` creates the four check-mark bitmaps and then assigns them to their appropriate menu items by using the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span>

<span data-ttu-id="71cb7-466">若要建立每個點陣圖，>oncreate 會呼叫應用程式定義的 CreateMenuBitmaps 函式，並指定點陣圖特定繪圖函式的指標。</span><span class="sxs-lookup"><span data-stu-id="71cb7-466">To create each bitmap, OnCreate calls the application-defined CreateMenuBitmaps function, specifying a pointer to a bitmap-specific drawing function.</span></span> <span data-ttu-id="71cb7-467">CreateMenuBitmaps 會建立所需大小的單色點陣圖，並將其選取為記憶體裝置內容，並清除背景。</span><span class="sxs-lookup"><span data-stu-id="71cb7-467">CreateMenuBitmaps creates a monochrome bitmap of the required size, selects it into a memory device context, and erases the background.</span></span> <span data-ttu-id="71cb7-468">然後，它會呼叫指定的繪圖函式來填滿前景。</span><span class="sxs-lookup"><span data-stu-id="71cb7-468">Then it calls the specified drawing function to fill in the foreground.</span></span>

<span data-ttu-id="71cb7-469">四個應用程式定義的繪圖函數為 DrawCheck、DrawUncheck、 **DrawRadioCheck** 和 DrawRadioUncheck。</span><span class="sxs-lookup"><span data-stu-id="71cb7-469">The four application-defined drawing functions are DrawCheck, DrawUncheck, **DrawRadioCheck**, and DrawRadioUncheck.</span></span> <span data-ttu-id="71cb7-470">它們會繪製一個矩形，其中包含 X、一個空白矩形、一個橢圓形，其中包含較小的填滿橢圓形和一個空白橢圓形。</span><span class="sxs-lookup"><span data-stu-id="71cb7-470">They draw a rectangle with an X, an empty rectangle, an ellipse containing a smaller filled ellipse, and an empty ellipse, respectively.</span></span>

<span data-ttu-id="71cb7-471">視窗程式會藉由刪除核取記號點陣圖來處理 [**WM \_**](/windows/desktop/winmsg/wm-destroy) 終結訊息。</span><span class="sxs-lookup"><span data-stu-id="71cb7-471">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message by deleting the check-mark bitmaps.</span></span> <span data-ttu-id="71cb7-472">它會使用 [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) 函式來抓取每個點陣圖控制碼，然後將控制碼傳遞給函式。</span><span class="sxs-lookup"><span data-stu-id="71cb7-472">It retrieves each bitmap handle by using the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function and then passes a handle to the function.</span></span>

<span data-ttu-id="71cb7-473">當使用者選擇功能表項目時，會將 [**WM \_ 命令**](wm-command.md) 訊息傳送至主控視窗。</span><span class="sxs-lookup"><span data-stu-id="71cb7-473">When the user chooses a menu item, a [**WM\_COMMAND**](wm-command.md) message is sent to the owner window.</span></span> <span data-ttu-id="71cb7-474">如果是 [ **字元** ] 功能表上的功能表項目，則視窗程式會呼叫應用程式定義的 CheckCharacterItem 函式。</span><span class="sxs-lookup"><span data-stu-id="71cb7-474">For menu items on the **Character** menu, the window procedure calls the application-defined CheckCharacterItem function.</span></span> <span data-ttu-id="71cb7-475">針對 **段落** 功能表上的專案，視窗程式會呼叫應用程式定義的 CheckParagraphItem 函數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-475">For items on the **Paragraph** menu, the window procedure calls the application-defined CheckParagraphItem function.</span></span>

<span data-ttu-id="71cb7-476">**字元** 功能表上的每個專案都可以單獨選取和清除。</span><span class="sxs-lookup"><span data-stu-id="71cb7-476">Each item on the **Character** menu can be selected and cleared independently.</span></span> <span data-ttu-id="71cb7-477">因此，CheckCharacterItem 只會切換指定的功能表項目的檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="71cb7-477">Therefore, CheckCharacterItem simply switches the specified menu item's check state.</span></span> <span data-ttu-id="71cb7-478">首先，此函式會呼叫 [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) 函數來取得目前的功能表項目狀態。</span><span class="sxs-lookup"><span data-stu-id="71cb7-478">First, the function calls the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function to get the current menu item state.</span></span> <span data-ttu-id="71cb7-479">然後，它會切換 **MFS \_ CHECKED** 狀態旗標，並藉由呼叫 [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) 函式來設定新的狀態。</span><span class="sxs-lookup"><span data-stu-id="71cb7-479">Then it switches the **MFS\_CHECKED** state flag and sets the new state by calling the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="71cb7-480">和字元屬性不同的是，一次只能選取一個段落對齊。</span><span class="sxs-lookup"><span data-stu-id="71cb7-480">Unlike character attributes, only one paragraph alignment can be selected at a time.</span></span> <span data-ttu-id="71cb7-481">因此，CheckParagraphItem 會檢查指定的功能表項目，並從功能表上的所有其他專案中移除核取記號。</span><span class="sxs-lookup"><span data-stu-id="71cb7-481">Therefore, CheckParagraphItem checks the specified menu item and removes the check mark from all other items on the menu.</span></span> <span data-ttu-id="71cb7-482">若要這樣做，它會呼叫 [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) 函數。</span><span class="sxs-lookup"><span data-stu-id="71cb7-482">To do so, it calls the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function.</span></span>

<span data-ttu-id="71cb7-483">以下是應用程式標頭檔的相關部分。</span><span class="sxs-lookup"><span data-stu-id="71cb7-483">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



<span data-ttu-id="71cb7-484">以下是應用程式的視窗程式和相關功能的相關部分。</span><span class="sxs-lookup"><span data-stu-id="71cb7-484">The following are the relevant portions of the application's window procedure and related functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 