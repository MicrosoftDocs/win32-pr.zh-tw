---
description: 本章節中的範例說明如何執行與使用 windows 相關聯的工作。
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: 使用 Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851872"
---
# <a name="using-windows"></a><span data-ttu-id="0d03e-103">使用 Windows</span><span class="sxs-lookup"><span data-stu-id="0d03e-103">Using Windows</span></span>

<span data-ttu-id="0d03e-104">本節中的範例說明如何執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="0d03e-104">The examples in this section describe how to perform the following tasks:</span></span>

-   [<span data-ttu-id="0d03e-105">建立主視窗</span><span class="sxs-lookup"><span data-stu-id="0d03e-105">Creating a Main Window</span></span>](#creating-a-main-window)
-   [<span data-ttu-id="0d03e-106">建立、列舉及調整子視窗的大小</span><span class="sxs-lookup"><span data-stu-id="0d03e-106">Creating, Enumerating, and Sizing Child Windows</span></span>](#creating-enumerating-and-sizing-child-windows)
-   [<span data-ttu-id="0d03e-107">終結視窗</span><span class="sxs-lookup"><span data-stu-id="0d03e-107">Destroying a Window</span></span>](#destroying-a-window)
-   [<span data-ttu-id="0d03e-108">使用分層視窗</span><span class="sxs-lookup"><span data-stu-id="0d03e-108">Using Layered Windows</span></span>](#using-layered-windows)

## <a name="creating-a-main-window"></a><span data-ttu-id="0d03e-109">建立主視窗</span><span class="sxs-lookup"><span data-stu-id="0d03e-109">Creating a Main Window</span></span>

<span data-ttu-id="0d03e-110">應用程式所建立的第一個視窗通常是主視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-110">The first window an application creates is typically the main window.</span></span> <span data-ttu-id="0d03e-111">您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式來建立主視窗，指定視窗類別、視窗名稱、視窗樣式、大小、位置、功能表控制碼、實例控制碼和建立資料。</span><span class="sxs-lookup"><span data-stu-id="0d03e-111">You create the main window by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function, specifying the window class, window name, window styles, size, position, menu handle, instance handle, and creation data.</span></span> <span data-ttu-id="0d03e-112">主視窗屬於應用程式定義的視窗類別，因此您必須先註冊視窗類別並提供類別的視窗程式，才能建立主視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-112">A main window belongs to an application-defined window class, so you must register the window class and provide a window procedure for the class before creating the main window.</span></span>

<span data-ttu-id="0d03e-113">大部分的應用程式通常會使用 [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) 樣式來建立主視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-113">Most applications typically use the [**WS\_OVERLAPPEDWINDOW**](window-styles.md) style to create the main window.</span></span> <span data-ttu-id="0d03e-114">此樣式會為視窗提供標題列、視窗功能表、調整大小框線，以及最小化和最大化按鈕。</span><span class="sxs-lookup"><span data-stu-id="0d03e-114">This style gives the window a title bar, a window menu, a sizing border, and minimize and maximize buttons.</span></span> <span data-ttu-id="0d03e-115">[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式會傳回可唯一識別視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0d03e-115">The [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function returns a handle that uniquely identifies the window.</span></span>

<span data-ttu-id="0d03e-116">下列範例會建立一個屬於應用程式定義視窗類別的主視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-116">The following example creates a main window belonging to an application-defined window class.</span></span> <span data-ttu-id="0d03e-117">視窗名稱（ **主視窗**）將會出現在視窗的標題列中。</span><span class="sxs-lookup"><span data-stu-id="0d03e-117">The window name, **Main Window**, will appear in the window's title bar.</span></span> <span data-ttu-id="0d03e-118">藉由結合 [**ws \_ VSCROLL**](window-styles.md) 和 **Ws \_ HSCROLL** 樣式與 **Ws \_ OVERLAPPEDWINDOW** 樣式，應用程式除了 **ws \_ OVERLAPPEDWINDOW** 樣式所提供的元件之外，還會建立具有水準和垂直捲動條的主視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-118">By combining the [**WS\_VSCROLL**](window-styles.md) and **WS\_HSCROLL** styles with the **WS\_OVERLAPPEDWINDOW** style, the application creates a main window with horizontal and vertical scroll bars in addition to the components provided by the **WS\_OVERLAPPEDWINDOW** style.</span></span> <span data-ttu-id="0d03e-119">四次的 **CW \_ USEDEFAULT** 常數會將視窗的初始大小和位置設定為系統定義的預設值。</span><span class="sxs-lookup"><span data-stu-id="0d03e-119">The four occurrences of the **CW\_USEDEFAULT** constant set the initial size and position of the window to the system-defined default values.</span></span> <span data-ttu-id="0d03e-120">藉由指定 **Null** 而非功能表控點，視窗將會為視窗類別定義功能表。</span><span class="sxs-lookup"><span data-stu-id="0d03e-120">By specifying **NULL** instead of a menu handle, the window will have the menu defined for the window class.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



<span data-ttu-id="0d03e-121">請注意，上述範例會在建立主視窗之後呼叫 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式。</span><span class="sxs-lookup"><span data-stu-id="0d03e-121">Notice that the preceding example calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function after creating the main window.</span></span> <span data-ttu-id="0d03e-122">這樣做的原因是，系統不會在建立後自動顯示主視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-122">This is done because the system does not automatically display the main window after creating it.</span></span> <span data-ttu-id="0d03e-123">藉由將 **SW \_ SHOWDEFAULT** 旗標傳遞給 **ShowWindow**，應用程式可讓啟動應用程式的程式設定主視窗的初始顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="0d03e-123">By passing the **SW\_SHOWDEFAULT** flag to **ShowWindow**, the application allows the program that started the application to set the initial show state of the main window.</span></span> <span data-ttu-id="0d03e-124">[**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow)函式會將它的第一個 [**WM \_ 油漆**](../gdi/wm-paint.md)訊息傳送給視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-124">The [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) function sends the window its first [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span>

## <a name="creating-enumerating-and-sizing-child-windows"></a><span data-ttu-id="0d03e-125">建立、列舉及調整子視窗的大小</span><span class="sxs-lookup"><span data-stu-id="0d03e-125">Creating, Enumerating, and Sizing Child Windows</span></span>

<span data-ttu-id="0d03e-126">您可以使用子視窗，將視窗的工作區分割成不同的功能區域。</span><span class="sxs-lookup"><span data-stu-id="0d03e-126">You can divide a window's client area into different functional areas by using child windows.</span></span> <span data-ttu-id="0d03e-127">建立子視窗就像建立主視窗一樣，您也可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="0d03e-127">Creating a child window is like creating a main window—you use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="0d03e-128">若要建立應用程式定義視窗類別的視窗，您必須先註冊視窗類別並提供視窗程式，然後再建立子視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-128">To create a window of an application-defined window class, you must register the window class and provide a window procedure before creating the child window.</span></span> <span data-ttu-id="0d03e-129">您必須提供子視窗的 [**WS \_ 子**](window-styles.md) 系樣式，並在建立時指定子視窗的父視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-129">You must give the child window the [**WS\_CHILD**](window-styles.md) style and specify a parent window for the child window when you create it.</span></span>

<span data-ttu-id="0d03e-130">下列範例會建立三個大小相同的子視窗，將應用程式主視窗的工作區分割成三個功能區域。</span><span class="sxs-lookup"><span data-stu-id="0d03e-130">The following example divides the client area of an application's main window into three functional areas by creating three child windows of equal size.</span></span> <span data-ttu-id="0d03e-131">每個子視窗的高度與主視窗的工作區高度相同，但每一個視窗的寬度都是三分之一。</span><span class="sxs-lookup"><span data-stu-id="0d03e-131">Each child window is the same height as the main window's client area, but each is one-third its width.</span></span> <span data-ttu-id="0d03e-132">主視窗會建立子視窗來回應 [**WM \_ 建立**](wm-create.md) 訊息，而主視窗會在其本身的視窗建立程式期間收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="0d03e-132">The main window creates the child windows in response to the [**WM\_CREATE**](wm-create.md) message, which the main window receives during its own window-creation process.</span></span> <span data-ttu-id="0d03e-133">因為每個子視窗都有 [**WS \_ 框線**](window-styles.md) 樣式，所以每個都有一個細線框線。</span><span class="sxs-lookup"><span data-stu-id="0d03e-133">Because each child window has the [**WS\_BORDER**](window-styles.md) style, each has a thin line border.</span></span> <span data-ttu-id="0d03e-134">此外，因為未指定 **WS \_ VISIBLE** 樣式，所以一開始會隱藏每個子視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-134">Also, because the **WS\_VISIBLE** style is not specified, each child window is initially hidden.</span></span> <span data-ttu-id="0d03e-135">另外也請注意，每個子視窗都被指派一個子視窗識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d03e-135">Notice also that each child window is assigned a child-window identifier.</span></span>

<span data-ttu-id="0d03e-136">主視窗會調整子視窗的大小並放置子視窗，以回應其大小變更時，主視窗接收到的 [**WM \_ 大小**](wm-size.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0d03e-136">The main window sizes and positions the child windows in response to the [**WM\_SIZE**](wm-size.md) message, which the main window receives when its size changes.</span></span> <span data-ttu-id="0d03e-137">為了回應 **WM \_ 大小**，主視窗會使用 [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) 函數抓取其工作區的維度，然後將維度傳遞給 [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) 函數。</span><span class="sxs-lookup"><span data-stu-id="0d03e-137">In response to **WM\_SIZE**, the main window retrieves the dimensions of its client area by using the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function and then passes the dimensions to the [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) function.</span></span> <span data-ttu-id="0d03e-138">**EnumChildWindows** 會依次將控制碼傳遞至應用程式定義的 [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="0d03e-138">**EnumChildWindows** passes the handle to each child window, in turn, to the application-defined [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) callback function.</span></span> <span data-ttu-id="0d03e-139">此函式會藉由呼叫 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式來調整每個子視窗的大小和位置;大小和位置是以主視窗工作區的維度和子視窗的識別碼為基礎。</span><span class="sxs-lookup"><span data-stu-id="0d03e-139">This function sizes and positions each child window by calling the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function; the size and position are based on the dimensions of the main window's client area and the identifier of the child window.</span></span> <span data-ttu-id="0d03e-140">之後， **EnumChildProc** 會呼叫 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式，讓視窗可見。</span><span class="sxs-lookup"><span data-stu-id="0d03e-140">Afterward, **EnumChildProc** calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function to make the window visible.</span></span>


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a><span data-ttu-id="0d03e-141">終結視窗</span><span class="sxs-lookup"><span data-stu-id="0d03e-141">Destroying a Window</span></span>

<span data-ttu-id="0d03e-142">您可以使用 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) 函數來終結視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-142">You can use the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy a window.</span></span> <span data-ttu-id="0d03e-143">一般而言，應用程式會在終結視窗之前傳送 [**WM \_ 關閉**](wm-close.md) 訊息，讓視窗有機會在視窗終結之前提示使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d03e-143">Typically, an application sends the [**WM\_CLOSE**](wm-close.md) message before destroying a window, giving the window the opportunity to prompt the user for confirmation before the window is destroyed.</span></span> <span data-ttu-id="0d03e-144">當使用者按一下 [視窗] 功能表中的 [**關閉**] 時，包含視窗功能表的視窗會自動收到 **WM \_ 關閉** 訊息。</span><span class="sxs-lookup"><span data-stu-id="0d03e-144">A window that includes a window menu automatically receives the **WM\_CLOSE** message when the user clicks **Close** from the window menu.</span></span> <span data-ttu-id="0d03e-145">如果使用者確認應該終結視窗，應用程式會呼叫 **DestroyWindow**。</span><span class="sxs-lookup"><span data-stu-id="0d03e-145">If the user confirms that the window should be destroyed, the application calls **DestroyWindow**.</span></span> <span data-ttu-id="0d03e-146">將 [**WM \_**](wm-destroy.md) 終結訊息從螢幕中移除之後，系統會將它傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-146">The system sends the [**WM\_DESTROY**](wm-destroy.md) message to the window after removing it from the screen.</span></span> <span data-ttu-id="0d03e-147">為了回應 **WM 終結 \_**，此視窗會儲存其資料並釋出它所配置的任何資源。</span><span class="sxs-lookup"><span data-stu-id="0d03e-147">In response to **WM\_DESTROY**, the window saves its data and frees any resources it allocated.</span></span> <span data-ttu-id="0d03e-148">主視窗會藉由呼叫 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)函式來結束應用程式，以結束其對 **WM \_ 摧毀** 的處理。</span><span class="sxs-lookup"><span data-stu-id="0d03e-148">A main window concludes its processing of **WM\_DESTROY** by calling the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to quit the application.</span></span>

<span data-ttu-id="0d03e-149">下列範例顯示如何在終結視窗之前提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0d03e-149">The following example shows how to prompt for user confirmation before destroying a window.</span></span> <span data-ttu-id="0d03e-150">為了回應 [**WM \_ 關閉**](wm-close.md)，此範例會顯示一個對話方塊，其中包含 **[是**]、[ **否**] 和 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="0d03e-150">In response to [**WM\_CLOSE**](wm-close.md), the example displays a dialog box that contains **Yes**, **No**, and **Cancel** buttons.</span></span> <span data-ttu-id="0d03e-151">如果使用者按一下 **[是]**，則會呼叫 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) ;否則，不會終結視窗。</span><span class="sxs-lookup"><span data-stu-id="0d03e-151">If the user clicks **Yes**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) is called; otherwise, the window is not destroyed.</span></span> <span data-ttu-id="0d03e-152">因為被終結的視窗是主視窗，此範例會呼叫 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) 以回應 [**WM 終結 \_**](wm-destroy.md)。</span><span class="sxs-lookup"><span data-stu-id="0d03e-152">Because the window being destroyed is a main window, the example calls [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) in response to [**WM\_DESTROY**](wm-destroy.md).</span></span>


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a><span data-ttu-id="0d03e-153">使用分層視窗</span><span class="sxs-lookup"><span data-stu-id="0d03e-153">Using Layered Windows</span></span>

<span data-ttu-id="0d03e-154">若要讓對話方塊成為半透明視窗，請先照常建立對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0d03e-154">To have a dialog box come up as a translucent window, first create the dialog as usual.</span></span> <span data-ttu-id="0d03e-155">然後，在 [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)上，設定視窗擴充樣式的分層位，並使用所需的 Alpha 值來呼叫 [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) 。</span><span class="sxs-lookup"><span data-stu-id="0d03e-155">Then, on [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md), set the layered bit of the window's extended style and call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) with the desired alpha value.</span></span> <span data-ttu-id="0d03e-156">程式碼可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="0d03e-156">The code might look like this:</span></span>


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



<span data-ttu-id="0d03e-157">請注意， [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) 的第三個參數是範圍從0到255的值，其中0讓視窗完全透明，而255使其完全不透明。</span><span class="sxs-lookup"><span data-stu-id="0d03e-157">Note that the third parameter of [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) is a value that ranges from 0 to 255, with 0 making the window completely transparent and 255 making it completely opaque.</span></span> <span data-ttu-id="0d03e-158">此參數模仿 [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend)函式的更多用途 [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) 。</span><span class="sxs-lookup"><span data-stu-id="0d03e-158">This parameter mimics the more versatile [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) of the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>

<span data-ttu-id="0d03e-159">若要再次使此視窗完全不透明，請呼叫 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)來移除 **WS \_ EX \_ 分層** 位，然後要求視窗重新繪製。</span><span class="sxs-lookup"><span data-stu-id="0d03e-159">To make this window completely opaque again, remove the **WS\_EX\_LAYERED** bit by calling [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) and then ask the window to repaint.</span></span> <span data-ttu-id="0d03e-160">移除此位是為了讓系統知道它可以釋出一些與分層和重新導向相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="0d03e-160">Removing the bit is desired to let the system know that it can free up some memory associated with layering and redirection.</span></span> <span data-ttu-id="0d03e-161">程式碼可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="0d03e-161">The code might look like this:</span></span>


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



<span data-ttu-id="0d03e-162">為了使用階層式子視窗，應用程式必須在資訊清單中宣告自己的 Windows 8 感知。</span><span class="sxs-lookup"><span data-stu-id="0d03e-162">In order to use layered child windows, the application has to declare itself Windows 8-aware in the manifest.</span></span>

 

 
