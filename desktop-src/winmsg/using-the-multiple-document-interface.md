---
description: 本節說明如何執行與多個檔介面相關聯的工作。
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: 使用多重文件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980027"
---
# <a name="using-the-multiple-document-interface"></a><span data-ttu-id="81aa9-103">使用多重文件介面</span><span class="sxs-lookup"><span data-stu-id="81aa9-103">Using the Multiple Document Interface</span></span>

<span data-ttu-id="81aa9-104">本節說明如何執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="81aa9-104">This section explains how to perform the following tasks:</span></span>

-   [<span data-ttu-id="81aa9-105">註冊子系和框架視窗類別</span><span class="sxs-lookup"><span data-stu-id="81aa9-105">Registering Child and Frame Window Classes</span></span>](#registering-child-and-frame-window-classes)
-   [<span data-ttu-id="81aa9-106">建立框架和子視窗</span><span class="sxs-lookup"><span data-stu-id="81aa9-106">Creating Frame and Child Windows</span></span>](#creating-frame-and-child-windows)
-   [<span data-ttu-id="81aa9-107">寫入主要訊息迴圈</span><span class="sxs-lookup"><span data-stu-id="81aa9-107">Writing the Main Message Loop</span></span>](#writing-the-main-message-loop)
-   [<span data-ttu-id="81aa9-108">撰寫框架視窗程式</span><span class="sxs-lookup"><span data-stu-id="81aa9-108">Writing the Frame Window Procedure</span></span>](#writing-the-frame-window-procedure)
-   [<span data-ttu-id="81aa9-109">撰寫子視窗程式</span><span class="sxs-lookup"><span data-stu-id="81aa9-109">Writing the Child Window Procedure</span></span>](#writing-the-child-window-procedure)
-   [<span data-ttu-id="81aa9-110">建立子視窗</span><span class="sxs-lookup"><span data-stu-id="81aa9-110">Creating a Child Window</span></span>](#creating-a-child-window)

<span data-ttu-id="81aa9-111">為了說明這些工作，本節包含 Multipad 的範例， (MDI) 應用程式的一般多重文件介面。</span><span class="sxs-lookup"><span data-stu-id="81aa9-111">To illustrate these tasks, this section includes examples from Multipad, a typical multiple-document interface (MDI) application.</span></span>

## <a name="registering-child-and-frame-window-classes"></a><span data-ttu-id="81aa9-112">註冊子系和框架視窗類別</span><span class="sxs-lookup"><span data-stu-id="81aa9-112">Registering Child and Frame Window Classes</span></span>

<span data-ttu-id="81aa9-113">一般的 MDI 應用程式必須註冊兩個視窗類別：一個用於框架視窗，另一個用於其子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-113">A typical MDI application must register two window classes: one for its frame window and one for its child windows.</span></span> <span data-ttu-id="81aa9-114">如果應用程式支援多個檔案類型 (例如，試算表和圖表) ，則必須為每個類型註冊視窗類別。</span><span class="sxs-lookup"><span data-stu-id="81aa9-114">If an application supports more than one type of document (for example, a spreadsheet and a chart), it must register a window class for each type.</span></span>

<span data-ttu-id="81aa9-115">框架視窗的類別結構類似于非 MDI 應用程式中主視窗的類別結構。</span><span class="sxs-lookup"><span data-stu-id="81aa9-115">The class structure for the frame window is similar to the class structure for the main window in non–MDI applications.</span></span> <span data-ttu-id="81aa9-116">MDI 子視窗的類別結構與非 MDI 應用程式中的子視窗結構稍有不同，如下所示：</span><span class="sxs-lookup"><span data-stu-id="81aa9-116">The class structure for the MDI child windows differs slightly from the structure for child windows in non–MDI applications as follows:</span></span>

-   <span data-ttu-id="81aa9-117">類別結構應該要有一個圖示，因為使用者可以將 MDI 子視窗的最小化，如同一般的應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-117">The class structure should have an icon, because the user can minimize an MDI child window as if it were a normal application window.</span></span>
-   <span data-ttu-id="81aa9-118">由於 MDI 子視窗不能有自己的功能表，因此功能表名稱應為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="81aa9-118">The menu name should be **NULL**, because an MDI child window cannot have its own menu.</span></span>
-   <span data-ttu-id="81aa9-119">類別結構應該在視窗結構中保留額外的空間。</span><span class="sxs-lookup"><span data-stu-id="81aa9-119">The class structure should reserve extra space in the window structure.</span></span> <span data-ttu-id="81aa9-120">使用這個空間，應用程式可以將資料（例如檔案名）與特定的子視窗建立關聯。</span><span class="sxs-lookup"><span data-stu-id="81aa9-120">With this space, the application can associate data, such as a filename, with a particular child window.</span></span>

<span data-ttu-id="81aa9-121">下列範例顯示 Multipad 如何註冊其框架和子視窗類別。</span><span class="sxs-lookup"><span data-stu-id="81aa9-121">The following example shows how Multipad registers its frame and child window classes.</span></span>


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a><span data-ttu-id="81aa9-122">建立框架和子視窗</span><span class="sxs-lookup"><span data-stu-id="81aa9-122">Creating Frame and Child Windows</span></span>

<span data-ttu-id="81aa9-123">在註冊其視窗類別之後，MDI 應用程式即可建立其視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-123">After registering its window classes, an MDI application can create its windows.</span></span> <span data-ttu-id="81aa9-124">首先，它會使用 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數來建立框架視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-124">First, it creates its frame window by using the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="81aa9-125">在建立框架視窗之後，應用程式會使用 **CreateWindow** 或 **CreateWindowEx** 再次建立其用戶端視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-125">After creating its frame window, the application creates its client window, again by using **CreateWindow** or **CreateWindowEx**.</span></span> <span data-ttu-id="81aa9-126">應用程式應該將 MDICLIENT 指定為用戶端視窗的類別名稱; **MDICLIENT** 是系統定義的預先註冊視窗類別。</span><span class="sxs-lookup"><span data-stu-id="81aa9-126">The application should specify MDICLIENT as the client window's class name; **MDICLIENT** is a preregistered window class defined by the system.</span></span> <span data-ttu-id="81aa9-127">**CreateWindow** 或 **CreateWindowEx** 的 *lpvParam* 參數應指向 [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct)結構。</span><span class="sxs-lookup"><span data-stu-id="81aa9-127">The *lpvParam* parameter of **CreateWindow** or **CreateWindowEx** should point to a [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) structure.</span></span> <span data-ttu-id="81aa9-128">此結構包含下表中描述的成員：</span><span class="sxs-lookup"><span data-stu-id="81aa9-128">This structure contains the members described in the following table:</span></span>



| <span data-ttu-id="81aa9-129">member</span><span class="sxs-lookup"><span data-stu-id="81aa9-129">Member</span></span>           | <span data-ttu-id="81aa9-130">描述</span><span class="sxs-lookup"><span data-stu-id="81aa9-130">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81aa9-131">**hWindowMenu**</span><span class="sxs-lookup"><span data-stu-id="81aa9-131">**hWindowMenu**</span></span>  | <span data-ttu-id="81aa9-132">用來控制 MDI 子視窗的視窗功能表控制碼。</span><span class="sxs-lookup"><span data-stu-id="81aa9-132">Handle to the window menu used for controlling MDI child windows.</span></span> <span data-ttu-id="81aa9-133">當建立子視窗時，應用程式會將其標題以功能表項目的形式加入至 [視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="81aa9-133">As child windows are created, the application adds their titles to the window menu as menu items.</span></span> <span data-ttu-id="81aa9-134">然後，使用者可以按一下 [視窗] 功能表上的標題，以啟用子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-134">The user can then activate a child window by clicking its title on the window menu.</span></span>                                                               |
| <span data-ttu-id="81aa9-135">**idFirstChild**</span><span class="sxs-lookup"><span data-stu-id="81aa9-135">**idFirstChild**</span></span> | <span data-ttu-id="81aa9-136">指定第一個 MDI 子視窗的識別碼。</span><span class="sxs-lookup"><span data-stu-id="81aa9-136">Specifies the identifier of the first MDI child window.</span></span> <span data-ttu-id="81aa9-137">第一個建立的 MDI 子視窗會指派此識別碼。</span><span class="sxs-lookup"><span data-stu-id="81aa9-137">The first MDI child window created is assigned this identifier.</span></span> <span data-ttu-id="81aa9-138">其他視窗則會以遞增的視窗識別碼來建立。</span><span class="sxs-lookup"><span data-stu-id="81aa9-138">Additional windows are created with incremented window identifiers.</span></span> <span data-ttu-id="81aa9-139">當子視窗損毀時，系統會立即重新指派視窗識別碼，讓其範圍保持連續。</span><span class="sxs-lookup"><span data-stu-id="81aa9-139">When a child window is destroyed, the system immediately reassigns the window identifiers to keep their range contiguous.</span></span> |



 

<span data-ttu-id="81aa9-140">將子視窗的標題新增至 [視窗] 功能表時，系統會將識別碼指派給子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-140">When a child window's title is added to the window menu, the system assigns an identifier to the child window.</span></span> <span data-ttu-id="81aa9-141">當使用者按一下子視窗的標題時，框架視窗會在 *wParam* 參數中收到含有識別碼的 [**WM \_ 命令**](../menurc/wm-command.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="81aa9-141">When the user clicks a child window's title, the frame window receives a [**WM\_COMMAND**](../menurc/wm-command.md) message with the identifier in the *wParam* parameter.</span></span> <span data-ttu-id="81aa9-142">您應指定 **idFirstChild** 成員的值，此值不會與框架視窗功能表中的功能表項目識別碼衝突。</span><span class="sxs-lookup"><span data-stu-id="81aa9-142">You should specify a value for the **idFirstChild** member that does not conflict with menu-item identifiers in the frame window's menu.</span></span>

<span data-ttu-id="81aa9-143">Multipad 的框架視窗程式會在處理 [**WM \_ 建立**](wm-create.md) 訊息時建立 MDI 用戶端視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-143">Multipad's frame window procedure creates the MDI client window while processing the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="81aa9-144">下列範例顯示如何建立用戶端視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-144">The following example shows how the client window is created.</span></span>


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



<span data-ttu-id="81aa9-145">子視窗的標題會新增至 [視窗] 功能表的底部。</span><span class="sxs-lookup"><span data-stu-id="81aa9-145">Titles of child windows are added to the bottom of the window menu.</span></span> <span data-ttu-id="81aa9-146">如果應用程式使用 [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) 函式將字串加入至 [視窗] 功能表，當 (子視窗建立或終結) 時，子視窗的標題就可以覆寫這些字串。</span><span class="sxs-lookup"><span data-stu-id="81aa9-146">If the application adds strings to the window menu by using the [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function, these strings can be overwritten by the titles of the child windows when the window menu is repainted (whenever a child window is created or destroyed).</span></span> <span data-ttu-id="81aa9-147">將字串加入至其視窗功能表的 MDI 應用程式應該使用 [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) 函式，並確認子視窗的標題尚未覆寫這些新的字串。</span><span class="sxs-lookup"><span data-stu-id="81aa9-147">An MDI application that adds strings to its window menu should use the [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) function and verify that the titles of child windows have not overwritten these new strings.</span></span>

<span data-ttu-id="81aa9-148">使用 **WS \_ CLIPCHILDREN** 樣式來建立 MDI 用戶端視窗，以防止視窗繪製在其子視窗上。</span><span class="sxs-lookup"><span data-stu-id="81aa9-148">Use the **WS\_CLIPCHILDREN** style to create the MDI client window to prevent the window from painting over its child windows.</span></span>

## <a name="writing-the-main-message-loop"></a><span data-ttu-id="81aa9-149">寫入主要訊息迴圈</span><span class="sxs-lookup"><span data-stu-id="81aa9-149">Writing the Main Message Loop</span></span>

<span data-ttu-id="81aa9-150">MDI 應用程式的主要訊息迴圈類似于非 MDI 應用程式處理快速鍵的訊息。</span><span class="sxs-lookup"><span data-stu-id="81aa9-150">The main message loop of an MDI application is similar to that of a non-MDI application handling accelerator keys.</span></span> <span data-ttu-id="81aa9-151">不同之處在于，MDI 訊息迴圈會先呼叫 [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) 函式，再檢查應用程式定義的快速鍵或分派訊息。</span><span class="sxs-lookup"><span data-stu-id="81aa9-151">The difference is that the MDI message loop calls the [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function before checking for application-defined accelerator keys or before dispatching the message.</span></span>

<span data-ttu-id="81aa9-152">下列範例顯示一般 MDI 應用程式的訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="81aa9-152">The following example shows the message loop of a typical MDI application.</span></span> <span data-ttu-id="81aa9-153">請注意，如果發生錯誤， [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 可以傳回-1。</span><span class="sxs-lookup"><span data-stu-id="81aa9-153">Note that [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) can return -1 if there is an error.</span></span>


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



<span data-ttu-id="81aa9-154">[**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel)函式會將 [**wm 的 \_ KEYDOWN**](../inputdev/wm-keydown.md)訊息轉譯成 [**wm \_ SYSCOMMAND**](../menurc/wm-syscommand.md)訊息，並將它們傳送至作用中的 MDI 子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-154">The [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function translates [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) messages into [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) messages and sends them to the active MDI child window.</span></span> <span data-ttu-id="81aa9-155">如果訊息不是 MDI 快速鍵訊息，則函式會傳回 **FALSE**，在此情況下，應用程式會使用 [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) 函式來判斷是否已按下任何應用程式定義的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="81aa9-155">If the message is not an MDI accelerator message, the function returns **FALSE**, in which case the application uses the [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function to determine whether any of the application-defined accelerator keys were pressed.</span></span> <span data-ttu-id="81aa9-156">如果沒有，迴圈會將訊息分派至適當的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="81aa9-156">If not, the loop dispatches the message to the appropriate window procedure.</span></span>

## <a name="writing-the-frame-window-procedure"></a><span data-ttu-id="81aa9-157">撰寫框架視窗程式</span><span class="sxs-lookup"><span data-stu-id="81aa9-157">Writing the Frame Window Procedure</span></span>

<span data-ttu-id="81aa9-158">MDI 框架視窗的視窗程式與非 MDI 應用程式主視窗的程式類似。</span><span class="sxs-lookup"><span data-stu-id="81aa9-158">The window procedure for an MDI frame window is similar to that of a non–MDI application's main window.</span></span> <span data-ttu-id="81aa9-159">差別在於框架視窗程式會將它未處理的所有訊息傳遞至 [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) 函式，而不是 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。</span><span class="sxs-lookup"><span data-stu-id="81aa9-159">The difference is that a frame window procedure passes all messages it does not handle to the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="81aa9-160">此外，框架視窗程式也必須傳遞其處理的訊息，包括下表所列的訊息。</span><span class="sxs-lookup"><span data-stu-id="81aa9-160">In addition, the frame window procedure must also pass some messages that it does handle, including those listed in the following table.</span></span>



| <span data-ttu-id="81aa9-161">訊息</span><span class="sxs-lookup"><span data-stu-id="81aa9-161">Message</span></span>                                  | <span data-ttu-id="81aa9-162">回應</span><span class="sxs-lookup"><span data-stu-id="81aa9-162">Response</span></span>                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81aa9-163">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="81aa9-163">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)     | <span data-ttu-id="81aa9-164">啟用使用者選擇的 MDI 子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-164">Activates the MDI child window that the user chooses.</span></span> <span data-ttu-id="81aa9-165">當使用者從 MDI 框架視窗的 [視窗] 功能表選擇 MDI 子視窗時，就會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="81aa9-165">This message is sent when the user chooses an MDI child window from the window menu of the MDI frame window.</span></span> <span data-ttu-id="81aa9-166">伴隨此訊息的視窗識別碼會識別要啟用的 MDI 子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-166">The window identifier accompanying this message identifies the MDI child window to be activated.</span></span> |
| [<span data-ttu-id="81aa9-167">**WM \_ MENUCHAR**</span><span class="sxs-lookup"><span data-stu-id="81aa9-167">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)   | <span data-ttu-id="81aa9-168">當使用者按下 ALT + – (減號) 按鍵組合時，開啟現用 MDI 子視窗的 [視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="81aa9-168">Opens the window menu of the active MDI child window when the user presses the ALT+ – (minus) key combination.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="81aa9-169">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="81aa9-169">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md) | <span data-ttu-id="81aa9-170">將鍵盤焦點傳遞至 MDI 用戶端視窗，然後將它傳遞給使用中的 MDI 子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-170">Passes the keyboard focus to the MDI client window, which in turn passes it to the active MDI child window.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="81aa9-171">**WM \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="81aa9-171">**WM\_SIZE**</span></span>](wm-size.md)              | <span data-ttu-id="81aa9-172">調整 MDI 用戶端視窗的大小，使其符合新框架視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="81aa9-172">Resizes the MDI client window to fit in the new frame window's client area.</span></span> <span data-ttu-id="81aa9-173">如果框架視窗程式將 MDI 用戶端視窗的大小調整為不同的大小，則不應將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。</span><span class="sxs-lookup"><span data-stu-id="81aa9-173">If the frame window procedure sizes the MDI client window to a different size, it should not pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>                   |



 

<span data-ttu-id="81aa9-174">Multipad 中的框架視窗程式稱為 MPFrameWndProc。</span><span class="sxs-lookup"><span data-stu-id="81aa9-174">The frame window procedure in Multipad is called MPFrameWndProc.</span></span> <span data-ttu-id="81aa9-175">MPFrameWndProc 處理其他訊息的方式，與非 MDI 應用程式的處理方式類似。</span><span class="sxs-lookup"><span data-stu-id="81aa9-175">The handling of other messages by MPFrameWndProc is similar to that of non–MDI applications.</span></span> <span data-ttu-id="81aa9-176">[**WM \_**](../menurc/wm-command.md)Multipad 中的命令訊息是由本機定義的 CommandHandler 函數所處理。</span><span class="sxs-lookup"><span data-stu-id="81aa9-176">[**WM\_COMMAND**](../menurc/wm-command.md) messages in Multipad are handled by the locally defined CommandHandler function.</span></span> <span data-ttu-id="81aa9-177">針對 Multipad 未處理的命令訊息，CommandHandler 會呼叫 [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) 函數。</span><span class="sxs-lookup"><span data-stu-id="81aa9-177">For command messages Multipad does not handle, CommandHandler calls the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function.</span></span> <span data-ttu-id="81aa9-178">如果 Multipad 預設不使用 **DefFrameProc** ，則使用者無法從 [視窗] 功能表啟動子視窗，因為按一下視窗的功能表項目所傳送的 **WM \_ 命令** 訊息將會遺失。</span><span class="sxs-lookup"><span data-stu-id="81aa9-178">If Multipad does not use **DefFrameProc** by default, the user can't activate a child window from the window menu, because the **WM\_COMMAND** message sent by clicking the window's menu item would be lost.</span></span>

## <a name="writing-the-child-window-procedure"></a><span data-ttu-id="81aa9-179">撰寫子視窗程式</span><span class="sxs-lookup"><span data-stu-id="81aa9-179">Writing the Child Window Procedure</span></span>

<span data-ttu-id="81aa9-180">如同框架視窗程式，MDI 子視窗程式預設會使用特殊函式來處理訊息。</span><span class="sxs-lookup"><span data-stu-id="81aa9-180">Like the frame window procedure, an MDI child window procedure uses a special function for processing messages by default.</span></span> <span data-ttu-id="81aa9-181">子視窗程式未處理的所有訊息都必須傳遞至 [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) 函式，而不是傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。</span><span class="sxs-lookup"><span data-stu-id="81aa9-181">All messages that the child window procedure does not handle must be passed to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="81aa9-182">此外，某些視窗管理訊息必須傳遞至 **DefMDIChildProc**，即使應用程式處理訊息，MDI 才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="81aa9-182">In addition, some window-management messages must be passed to **DefMDIChildProc**, even if the application handles the message, in order for MDI to function correctly.</span></span> <span data-ttu-id="81aa9-183">以下是應用程式必須傳遞給 **DefMDIChildProc** 的訊息。</span><span class="sxs-lookup"><span data-stu-id="81aa9-183">Following are the messages the application must pass to **DefMDIChildProc**.</span></span>



| <span data-ttu-id="81aa9-184">訊息</span><span class="sxs-lookup"><span data-stu-id="81aa9-184">Message</span></span>                                       | <span data-ttu-id="81aa9-185">回應</span><span class="sxs-lookup"><span data-stu-id="81aa9-185">Response</span></span>                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81aa9-186">**WM \_ CHILDACTI加值稅E**</span><span class="sxs-lookup"><span data-stu-id="81aa9-186">**WM\_CHILDACTIVATE**</span></span>](wm-childactivate.md) | <span data-ttu-id="81aa9-187">當 MDI 子視窗調整大小、移動或顯示時，執行啟用處理。</span><span class="sxs-lookup"><span data-stu-id="81aa9-187">Performs activation processing when MDI child windows are sized, moved, or displayed.</span></span> <span data-ttu-id="81aa9-188">必須傳遞此訊息。</span><span class="sxs-lookup"><span data-stu-id="81aa9-188">This message must be passed.</span></span>                                                                                                                                        |
| [<span data-ttu-id="81aa9-189">**WM \_ GETMINMAXINFO**</span><span class="sxs-lookup"><span data-stu-id="81aa9-189">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md) | <span data-ttu-id="81aa9-190">根據 MDI 用戶端視窗目前的大小，計算最大化的 MDI 子視窗大小。</span><span class="sxs-lookup"><span data-stu-id="81aa9-190">Calculates the size of a maximized MDI child window, based on the current size of the MDI client window.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="81aa9-191">**WM \_ MENUCHAR**</span><span class="sxs-lookup"><span data-stu-id="81aa9-191">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)        | <span data-ttu-id="81aa9-192">將訊息傳遞至 MDI 框架視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-192">Passes the message to the MDI frame window.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="81aa9-193">**WM \_ 移動**</span><span class="sxs-lookup"><span data-stu-id="81aa9-193">**WM\_MOVE**</span></span>](wm-move.md)                   | <span data-ttu-id="81aa9-194">重新計算 MDI 用戶端捲軸（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="81aa9-194">Recalculates MDI client scroll bars, if they are present.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="81aa9-195">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="81aa9-195">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)      | <span data-ttu-id="81aa9-196">啟動子視窗（如果它不是作用中的 MDI 子視窗）。</span><span class="sxs-lookup"><span data-stu-id="81aa9-196">Activates the child window, if it is not the active MDI child window.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="81aa9-197">**WM \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="81aa9-197">**WM\_SIZE**</span></span>](wm-size.md)                   | <span data-ttu-id="81aa9-198">執行變更視窗大小所需的作業，尤其是為了最大化或還原 MDI 子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-198">Performs operations necessary for changing the size of a window, especially for maximizing or restoring an MDI child window.</span></span> <span data-ttu-id="81aa9-199">無法將此訊息傳遞至 [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) 函式會產生高度不當的結果。</span><span class="sxs-lookup"><span data-stu-id="81aa9-199">Failing to pass this message to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function produces highly undesirable results.</span></span> |
| [<span data-ttu-id="81aa9-200">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="81aa9-200">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)    | <span data-ttu-id="81aa9-201">處理視窗 (先前稱為系統) 功能表命令： **sc \_ NEXTWINDOW**、 **sc \_ PREVWINDOW**、 **sc \_ MOVE**、 **sc \_ SIZE** 和 **sc \_ 最大化**。</span><span class="sxs-lookup"><span data-stu-id="81aa9-201">Handles window (formerly known as system) menu commands: **SC\_NEXTWINDOW**, **SC\_PREVWINDOW**, **SC\_MOVE**, **SC\_SIZE**, and **SC\_MAXIMIZE**.</span></span>                                                                                                        |



 

## <a name="creating-a-child-window"></a><span data-ttu-id="81aa9-202">建立子視窗</span><span class="sxs-lookup"><span data-stu-id="81aa9-202">Creating a Child Window</span></span>

<span data-ttu-id="81aa9-203">若要建立 MDI 子視窗，應用程式可以呼叫 [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) 函式，或將 [**WM \_ MDICREATE**](wm-mdicreate.md) 訊息傳送至 MDI 用戶端視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-203">To create an MDI child window, an application can either call the [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) function or send an [**WM\_MDICREATE**](wm-mdicreate.md) message to the MDI client window.</span></span> <span data-ttu-id="81aa9-204"> (應用程式可使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式搭配 **WS \_ EX \_ MDICHILD** 樣式來建立 MDI 子視窗。 ) 單一執行緒的 MDI 應用程式可以使用任一種方法來建立子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-204">(The application can use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function with the **WS\_EX\_MDICHILD** style to create MDI child windows.) A single-threaded MDI application can use either method to create a child window.</span></span> <span data-ttu-id="81aa9-205">多執行緒 MDI 應用程式中的執行緒必須使用 **CreateMDIWindow** 或 **CreateWindowEx** 函數，在不同的執行緒中建立子視窗。</span><span class="sxs-lookup"><span data-stu-id="81aa9-205">A thread in a multithreaded MDI application must use the **CreateMDIWindow** or **CreateWindowEx** function to create a child window in a different thread.</span></span>

<span data-ttu-id="81aa9-206">[**WM \_ MDICREATE**](wm-mdicreate.md)訊息的 *lParam* 參數是 [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)結構的最遠指標。</span><span class="sxs-lookup"><span data-stu-id="81aa9-206">The *lParam* parameter of a [**WM\_MDICREATE**](wm-mdicreate.md) message is a far pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="81aa9-207">結構包含四個維度成員： **x** 和 **y**，表示視窗的水準和垂直位置，以及 **cx** 和 **cy**（表示視窗的水準和垂直範圍）。</span><span class="sxs-lookup"><span data-stu-id="81aa9-207">The structure includes four dimension members: **x** and **y**, which indicate the horizontal and vertical positions of the window, and **cx** and **cy**, which indicate the horizontal and vertical extents of the window.</span></span> <span data-ttu-id="81aa9-208">這些成員都可以由應用程式明確指派，也可以設定為 **CW \_ USEDEFAULT**，在此情況下，系統會根據串聯演算法來選取位置、大小或兩者。</span><span class="sxs-lookup"><span data-stu-id="81aa9-208">Any of these members may be assigned explicitly by the application, or they may be set to **CW\_USEDEFAULT**, in which case the system selects a position, size, or both, according to a cascading algorithm.</span></span> <span data-ttu-id="81aa9-209">在任何情況下，全部四個成員都必須初始化。</span><span class="sxs-lookup"><span data-stu-id="81aa9-209">In any case, all four members must be initialized.</span></span> <span data-ttu-id="81aa9-210">Multipad 使用所有維度的 **CW \_ USEDEFAULT** 。</span><span class="sxs-lookup"><span data-stu-id="81aa9-210">Multipad uses **CW\_USEDEFAULT** for all dimensions.</span></span>

<span data-ttu-id="81aa9-211">[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)結構的最後一個成員是 **樣式** 成員，它可能包含視窗的樣式位。</span><span class="sxs-lookup"><span data-stu-id="81aa9-211">The last member of the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure is the **style** member, which may contain style bits for the window.</span></span> <span data-ttu-id="81aa9-212">若要建立可以有視窗樣式組合的 MDI 子視窗，請指定 [ **mdi \_ ALLCHILDSTYLES** ] 視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="81aa9-212">To create an MDI child window that can have any combination of window styles, specify the **MDIS\_ALLCHILDSTYLES** window style.</span></span> <span data-ttu-id="81aa9-213">未指定此樣式時，MDI 子視窗會將 **ws \_ 最小化**、 **ws \_ 最大化**、 **ws \_ HSCROLL** 和 **ws \_ VSCROLL** 樣式設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="81aa9-213">When this style is not specified, an MDI child window has the **WS\_MINIMIZE**, **WS\_MAXIMIZE**, **WS\_HSCROLL**, and **WS\_VSCROLL** styles as default settings.</span></span>

<span data-ttu-id="81aa9-214">Multipad 會使用位於原始程式檔 MPFILE 的本機定義 AddFile 函式 (，建立其 MDI 子視窗。C) 。</span><span class="sxs-lookup"><span data-stu-id="81aa9-214">Multipad creates its MDI child windows by using its locally defined AddFile function (located in the source file MPFILE.C).</span></span> <span data-ttu-id="81aa9-215">AddFile 函式會將視窗 [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)結構的 **szTitle** 成員指派給要編輯的檔案名稱或「未命名」，以設定子視窗的標題。</span><span class="sxs-lookup"><span data-stu-id="81aa9-215">The AddFile function sets the title of the child window by assigning the **szTitle** member of the window's [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure to either the name of the file being edited or to "Untitled."</span></span> <span data-ttu-id="81aa9-216">**SzClass** 成員會設定為 Multipad 的 InitializeApplication 函式中所註冊的 MDI 子視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="81aa9-216">The **szClass** member is set to the name of the MDI child window class registered in Multipad's InitializeApplication function.</span></span> <span data-ttu-id="81aa9-217">**HOwner** 成員會設定為應用程式的實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="81aa9-217">The **hOwner** member is set to the application's instance handle.</span></span>

<span data-ttu-id="81aa9-218">下列範例會顯示 Multipad 中的 AddFile 函數。</span><span class="sxs-lookup"><span data-stu-id="81aa9-218">The following example shows the AddFile function in Multipad.</span></span>


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



<span data-ttu-id="81aa9-219">在 [**wm \_ MDICREATE**](wm-mdicreate.md)訊息的 *lParam* 參數中傳遞的指標會傳遞給 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)函數，並顯示為 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構中傳遞給 [**WM \_ 建立**](wm-create.md)訊息的第一個成員。</span><span class="sxs-lookup"><span data-stu-id="81aa9-219">The pointer passed in the *lParam* parameter of the [**WM\_MDICREATE**](wm-mdicreate.md) message is passed to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function and appears as the first member in the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure, passed in the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="81aa9-220">在 Multipad 中，子視窗會在 **WM \_ 建立** 訊息處理期間，藉由在其額外的資料中初始化檔變數，以及藉由建立編輯控制項的子視窗，來初始化本身。</span><span class="sxs-lookup"><span data-stu-id="81aa9-220">In Multipad, the child window initializes itself during **WM\_CREATE** message processing by initializing document variables in its extra data and by creating the edit control's child window.</span></span>

 

 
