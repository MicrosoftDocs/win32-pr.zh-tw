---
description: 本節說明如何執行與視窗程式相關聯的下列工作。
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: 使用視窗程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e0508119a2ba62c813c32e8fd0c00bd3dd1e85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851875"
---
# <a name="using-window-procedures"></a><span data-ttu-id="8e23e-103">使用視窗程式</span><span class="sxs-lookup"><span data-stu-id="8e23e-103">Using Window Procedures</span></span>

<span data-ttu-id="8e23e-104">本節說明如何執行與視窗程式相關聯的下列工作。</span><span class="sxs-lookup"><span data-stu-id="8e23e-104">This section explains how to perform the following tasks associated with window procedures.</span></span>

-   [<span data-ttu-id="8e23e-105">設計視窗程式</span><span class="sxs-lookup"><span data-stu-id="8e23e-105">Designing a Window Procedure</span></span>](#designing-a-window-procedure)
-   [<span data-ttu-id="8e23e-106">建立視窗程式與視窗類別的關聯</span><span class="sxs-lookup"><span data-stu-id="8e23e-106">Associating a Window Procedure with a Window Class</span></span>](#associating-a-window-procedure-with-a-window-class)
-   [<span data-ttu-id="8e23e-107">子類別化視窗</span><span class="sxs-lookup"><span data-stu-id="8e23e-107">Subclassing a Window</span></span>](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a><span data-ttu-id="8e23e-108">設計視窗程式</span><span class="sxs-lookup"><span data-stu-id="8e23e-108">Designing a Window Procedure</span></span>

<span data-ttu-id="8e23e-109">下列範例顯示一般視窗程式的結構。</span><span class="sxs-lookup"><span data-stu-id="8e23e-109">The following example shows the structure of a typical window procedure.</span></span> <span data-ttu-id="8e23e-110">視窗程式在 **switch** 語句中使用 message 引數，並以個別的 **case** 語句處理個別訊息。</span><span class="sxs-lookup"><span data-stu-id="8e23e-110">The window procedure uses the message argument in a **switch** statement with individual messages handled by separate **case** statements.</span></span> <span data-ttu-id="8e23e-111">請注意，每個案例都會針對每個訊息傳回特定值。</span><span class="sxs-lookup"><span data-stu-id="8e23e-111">Notice that each case returns a specific value for each message.</span></span> <span data-ttu-id="8e23e-112">針對它未處理的訊息，視窗程式會呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。</span><span class="sxs-lookup"><span data-stu-id="8e23e-112">For messages that it does not process, the window procedure calls the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



<span data-ttu-id="8e23e-113">當您建立視窗之後，就會傳送 [**WM \_ NCCREATE**](wm-nccreate.md) 訊息，但如果應用程式傳回 **FALSE** 來回應此訊息，則 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式會失敗。</span><span class="sxs-lookup"><span data-stu-id="8e23e-113">The [**WM\_NCCREATE**](wm-nccreate.md) message is sent just after your window is created, but if an application responds to this message by returning **FALSE**, [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function fails.</span></span> <span data-ttu-id="8e23e-114">在您的視窗建立之後，會傳送 [**WM \_ 建立**](wm-create.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="8e23e-114">The [**WM\_CREATE**](wm-create.md) message is sent after your window is already created.</span></span>

<span data-ttu-id="8e23e-115">當您的視窗即將終結時，會傳送 [**WM 損 \_ 毀**](wm-destroy.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="8e23e-115">The [**WM\_DESTROY**](wm-destroy.md) message is sent when your window is about to be destroyed.</span></span> <span data-ttu-id="8e23e-116">[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)函式會負責終結要終結之視窗的任何子視窗。</span><span class="sxs-lookup"><span data-stu-id="8e23e-116">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function takes care of destroying any child windows of the window being destroyed.</span></span> <span data-ttu-id="8e23e-117">在終結視窗之前，會立即傳送 [**WM \_ NCDESTROY**](wm-ncdestroy.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="8e23e-117">The [**WM\_NCDESTROY**](wm-ncdestroy.md) message is sent just before a window is destroyed.</span></span>

<span data-ttu-id="8e23e-118">視窗程式至少應該處理 [**WM \_ 繪製**](../gdi/wm-paint.md) 訊息來自行繪製。</span><span class="sxs-lookup"><span data-stu-id="8e23e-118">At the very least, a window procedure should process the [**WM\_PAINT**](../gdi/wm-paint.md) message to draw itself.</span></span> <span data-ttu-id="8e23e-119">一般來說，它也應該處理滑鼠和鍵盤訊息。</span><span class="sxs-lookup"><span data-stu-id="8e23e-119">Typically, it should handle mouse and keyboard messages as well.</span></span> <span data-ttu-id="8e23e-120">請參閱個別訊息的描述，以判斷您的視窗程式是否應該處理這些訊息。</span><span class="sxs-lookup"><span data-stu-id="8e23e-120">Consult the descriptions of individual messages to determine whether your window procedure should handle them.</span></span>

<span data-ttu-id="8e23e-121">您的應用程式可以呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數，做為訊息處理的一部分。</span><span class="sxs-lookup"><span data-stu-id="8e23e-121">Your application can call the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as part of the processing of a message.</span></span> <span data-ttu-id="8e23e-122">在這種情況下，應用程式可以先修改訊息參數，然後再將訊息傳遞至 **DefWindowProc**，或者它可以在執行自己的作業之後繼續進行預設處理。</span><span class="sxs-lookup"><span data-stu-id="8e23e-122">In such a case, the application can modify the message parameters before passing the message to **DefWindowProc**, or it can continue with the default processing after performing its own operations.</span></span>

<span data-ttu-id="8e23e-123">對話方塊程式會收到 [**wm \_ INITDIALOG**](../dlgbox/wm-initdialog.md) 訊息，而不是使用 [**wm \_ 建立**](wm-create.md) 訊息，而且不會將未處理的訊息傳遞至 [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) 函式。</span><span class="sxs-lookup"><span data-stu-id="8e23e-123">A dialog box procedure receives a [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message instead of a [**WM\_CREATE**](wm-create.md) message and does not pass unprocessed messages to the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="8e23e-124">否則，對話方塊程式與視窗程式完全相同。</span><span class="sxs-lookup"><span data-stu-id="8e23e-124">Otherwise, a dialog box procedure is exactly the same as a window procedure.</span></span>

## <a name="associating-a-window-procedure-with-a-window-class"></a><span data-ttu-id="8e23e-125">建立視窗程式與視窗類別的關聯</span><span class="sxs-lookup"><span data-stu-id="8e23e-125">Associating a Window Procedure with a Window Class</span></span>

<span data-ttu-id="8e23e-126">在註冊類別時，您會將視窗程式與視窗類別產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8e23e-126">You associate a window procedure with a window class when registering the class.</span></span> <span data-ttu-id="8e23e-127">您必須以類別的相關資訊填入 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 結構，而且 **lpfnWndProc** 成員必須指定視窗程式的位址。</span><span class="sxs-lookup"><span data-stu-id="8e23e-127">You must fill a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure with information about the class, and the **lpfnWndProc** member must specify the address of the window procedure.</span></span> <span data-ttu-id="8e23e-128">若要註冊類別，請將 **WNDCLASS** 結構的位址傳遞給 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) 函數。</span><span class="sxs-lookup"><span data-stu-id="8e23e-128">To register the class, pass the address of **WNDCLASS** structure to the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="8e23e-129">在註冊視窗類別之後，視窗程式會自動與以該類別建立的每個新視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="8e23e-129">After the window class has been registered, the window procedure is automatically associated with each new window created with that class.</span></span>

<span data-ttu-id="8e23e-130">下列範例顯示如何將上一個範例中的視窗程式與視窗類別產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8e23e-130">The following example shows how to associate the window procedure in the previous example with a window class.</span></span>


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a><span data-ttu-id="8e23e-131">子類別化視窗</span><span class="sxs-lookup"><span data-stu-id="8e23e-131">Subclassing a Window</span></span>

<span data-ttu-id="8e23e-132">若要子類別化視窗的實例，請呼叫 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式，並指定視窗的控制碼，以將 GWL \_ WNDPROC 旗標和子類別程式的指標子類別化。</span><span class="sxs-lookup"><span data-stu-id="8e23e-132">To subclass an instance of a window, call the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function and specify the handle to the window to subclass the GWL\_WNDPROC flag and a pointer to the subclass procedure.</span></span> <span data-ttu-id="8e23e-133">**SetWindowLong** 會傳回原始視窗程式的指標;使用這個指標可將訊息傳遞至原始程式。</span><span class="sxs-lookup"><span data-stu-id="8e23e-133">**SetWindowLong** returns a pointer to the original window procedure; use this pointer to pass messages to the original procedure.</span></span> <span data-ttu-id="8e23e-134">子類別視窗程式必須使用 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) 函數來呼叫原始視窗程式。</span><span class="sxs-lookup"><span data-stu-id="8e23e-134">The subclass window procedure must use the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function to call the original window procedure.</span></span>

> [!Note]  
> <span data-ttu-id="8e23e-135">若要撰寫與32位和64位版本的 Windows 相容的程式碼，請使用 [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) 函數。</span><span class="sxs-lookup"><span data-stu-id="8e23e-135">To write code that is compatible with both 32-bit and 64-bit versions of Windows, use the [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function.</span></span>

 

<span data-ttu-id="8e23e-136">下列範例顯示如何在對話方塊中子類別化編輯控制項的實例。</span><span class="sxs-lookup"><span data-stu-id="8e23e-136">The following example shows how to subclass an instance of an edit control in a dialog box.</span></span> <span data-ttu-id="8e23e-137">當控制項有輸入焦點時，子類別視窗程式可讓編輯控制項接收所有鍵盤輸入，包括 ENTER 和 TAB 鍵。</span><span class="sxs-lookup"><span data-stu-id="8e23e-137">The subclass window procedure enables the edit control to receive all keyboard input, including the ENTER and TAB keys, whenever the control has the input focus.</span></span>


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
