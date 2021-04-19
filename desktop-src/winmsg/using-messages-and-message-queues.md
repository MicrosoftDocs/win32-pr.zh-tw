---
description: 下列程式碼範例示範如何執行與 Windows 訊息和訊息佇列相關聯的下列工作。
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: 使用訊息和訊息佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a33f422a1a7c77f2c2fcd5913f931168a350a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971810"
---
# <a name="using-messages-and-message-queues"></a><span data-ttu-id="fd23b-103">使用訊息和訊息佇列</span><span class="sxs-lookup"><span data-stu-id="fd23b-103">Using Messages and Message Queues</span></span>

<span data-ttu-id="fd23b-104">下列程式碼範例示範如何執行與 Windows 訊息和訊息佇列相關聯的下列工作。</span><span class="sxs-lookup"><span data-stu-id="fd23b-104">The following code examples demonstrate how to perform the following tasks associated with Windows messages and message queues.</span></span>

-   [<span data-ttu-id="fd23b-105">建立訊息迴圈</span><span class="sxs-lookup"><span data-stu-id="fd23b-105">Creating a Message Loop</span></span>](#creating-a-message-loop)
-   [<span data-ttu-id="fd23b-106">檢查訊息佇列</span><span class="sxs-lookup"><span data-stu-id="fd23b-106">Examining a Message Queue</span></span>](#examining-a-message-queue)
-   [<span data-ttu-id="fd23b-107">張貼訊息</span><span class="sxs-lookup"><span data-stu-id="fd23b-107">Posting a Message</span></span>](#posting-a-message)
-   [<span data-ttu-id="fd23b-108">傳送訊息</span><span class="sxs-lookup"><span data-stu-id="fd23b-108">Sending a Message</span></span>](#sending-a-message)

## <a name="creating-a-message-loop"></a><span data-ttu-id="fd23b-109">建立訊息迴圈</span><span class="sxs-lookup"><span data-stu-id="fd23b-109">Creating a Message Loop</span></span>

<span data-ttu-id="fd23b-110">系統不會自動為每個執行緒建立訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="fd23b-110">The system does not automatically create a message queue for each thread.</span></span> <span data-ttu-id="fd23b-111">相反地，系統只會針對執行需要訊息佇列之作業的執行緒建立訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="fd23b-111">Instead, the system creates a message queue only for threads that perform operations which require a message queue.</span></span> <span data-ttu-id="fd23b-112">如果執行緒建立一或多個視窗，則必須提供訊息迴圈;此訊息迴圈會從執行緒的訊息佇列取出訊息，並將訊息分派至適當的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="fd23b-112">If the thread creates one or more windows, a message loop must be provided; this message loop retrieves messages from the thread's message queue and dispatches them to the appropriate window procedures.</span></span>

<span data-ttu-id="fd23b-113">因為系統會將訊息導向至應用程式中的個別視窗，所以執行緒必須在啟動其訊息迴圈之前，至少建立一個視窗。</span><span class="sxs-lookup"><span data-stu-id="fd23b-113">Because the system directs messages to individual windows in an application, a thread must create at least one window before starting its message loop.</span></span> <span data-ttu-id="fd23b-114">大部分的應用程式都包含一個建立 windows 的執行緒。</span><span class="sxs-lookup"><span data-stu-id="fd23b-114">Most applications contain a single thread that creates windows.</span></span> <span data-ttu-id="fd23b-115">一般的應用程式會針對其主視窗註冊視窗類別、建立並顯示主視窗，然後啟動其訊息迴圈，全都在 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式中。</span><span class="sxs-lookup"><span data-stu-id="fd23b-115">A typical application registers the window class for its main window, creates and shows the main window, and then starts its message loop — all in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span>

<span data-ttu-id="fd23b-116">您可以使用 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 和 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 函數來建立訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="fd23b-116">You create a message loop by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) functions.</span></span> <span data-ttu-id="fd23b-117">如果您的應用程式必須從使用者取得字元輸入，請在迴圈中包含 [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="fd23b-117">If your application must obtain character input from the user, include the [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) function in the loop.</span></span> <span data-ttu-id="fd23b-118">**TranslateMessage** 會將虛擬金鑰訊息轉譯為字元訊息。</span><span class="sxs-lookup"><span data-stu-id="fd23b-118">**TranslateMessage** translates virtual-key messages into character messages.</span></span> <span data-ttu-id="fd23b-119">下列範例顯示簡單 Windows 應用程式之 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式中的訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="fd23b-119">The following example shows the message loop in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function of a simple Windows-based application.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



<span data-ttu-id="fd23b-120">下列範例顯示使用快速鍵之執行緒的訊息迴圈，並顯示非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fd23b-120">The following example shows a message loop for a thread that uses accelerators and displays a modeless dialog box.</span></span> <span data-ttu-id="fd23b-121">當 [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) 或 [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) 傳回 **TRUE** (表示訊息已處理) ，則不會呼叫 [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) 和 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 。</span><span class="sxs-lookup"><span data-stu-id="fd23b-121">When [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) or [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) returns **TRUE** (indicating that the message has been processed), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) are not called.</span></span> <span data-ttu-id="fd23b-122">這是因為 **TranslateAccelerator** 和 **IsDialogMessage** 會執行所有必要的訊息轉譯和分派。</span><span class="sxs-lookup"><span data-stu-id="fd23b-122">The reason for this is that **TranslateAccelerator** and **IsDialogMessage** perform all necessary translating and dispatching of messages.</span></span>


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a><span data-ttu-id="fd23b-123">檢查訊息佇列</span><span class="sxs-lookup"><span data-stu-id="fd23b-123">Examining a Message Queue</span></span>

<span data-ttu-id="fd23b-124">有時候，應用程式需要從執行緒的訊息迴圈外部檢查執行緒訊息佇列的內容。</span><span class="sxs-lookup"><span data-stu-id="fd23b-124">Occasionally, an application needs to examine the contents of a thread's message queue from outside the thread's message loop.</span></span> <span data-ttu-id="fd23b-125">例如，如果應用程式的視窗程式執行冗長的繪圖作業，您可能會想要讓使用者能夠中斷作業。</span><span class="sxs-lookup"><span data-stu-id="fd23b-125">For example, if an application's window procedure performs a lengthy drawing operation, you may want the user to be able to interrupt the operation.</span></span> <span data-ttu-id="fd23b-126">除非您的應用程式會在操作滑鼠和鍵盤訊息時定期檢查訊息佇列，否則在作業完成之前，它將不會回應使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="fd23b-126">Unless your application periodically examines the message queue during the operation for mouse and keyboard messages, it will not respond to user input until after the operation has completed.</span></span> <span data-ttu-id="fd23b-127">原因是，在視窗程式完成處理訊息之前，執行緒的訊息迴圈中的 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 函式不會傳回。</span><span class="sxs-lookup"><span data-stu-id="fd23b-127">The reason for this is that the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function in the thread's message loop does not return until the window procedure finishes processing a message.</span></span>

<span data-ttu-id="fd23b-128">您可以使用 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函數，在冗長的作業期間檢查訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="fd23b-128">You can use the [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function to examine a message queue during a lengthy operation.</span></span> <span data-ttu-id="fd23b-129">**PeekMessage** 類似于 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)函數;這兩者都會檢查訊息佇列中是否有符合篩選準則的訊息，然後將訊息複製到 [**訊息結構。**](/windows/win32/api/winuser/ns-winuser-msg)</span><span class="sxs-lookup"><span data-stu-id="fd23b-129">**PeekMessage** is similar to the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function; both check a message queue for a message that matches the filter criteria and then copy the message to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure.</span></span> <span data-ttu-id="fd23b-130">這兩個函式的主要差異在於， **GetMessage** 不會傳回，直到符合篩選準則的訊息放置在佇列中，而 **PeekMessage** 則會立即傳回，無論訊息是否在佇列中。</span><span class="sxs-lookup"><span data-stu-id="fd23b-130">The main difference between the two functions is that **GetMessage** does not return until a message matching the filter criteria is placed in the queue, whereas **PeekMessage** returns immediately regardless of whether a message is in the queue.</span></span>

<span data-ttu-id="fd23b-131">下列範例示範如何使用 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 來檢查訊息佇列，以在長時間執行的滑鼠點擊和鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="fd23b-131">The following example shows how to use [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) to examine a message queue for mouse clicks and keyboard input during a lengthy operation.</span></span>


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



<span data-ttu-id="fd23b-132">其他函式（包括 [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) 和 [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate)）也可讓您檢查執行緒訊息佇列的內容。</span><span class="sxs-lookup"><span data-stu-id="fd23b-132">Other functions, including [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) and [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), also allow you to examine the contents of a thread's message queue.</span></span> <span data-ttu-id="fd23b-133">**GetQueueStatus** 會傳回旗標陣列，指出佇列中的訊息類型。使用它是探索佇列是否包含任何訊息的最快方式。</span><span class="sxs-lookup"><span data-stu-id="fd23b-133">**GetQueueStatus** returns an array of flags that indicates the types of messages in the queue; using it is the fastest way to discover whether the queue contains any messages.</span></span> <span data-ttu-id="fd23b-134">如果佇列包含滑鼠或鍵盤訊息， **GetInputState** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="fd23b-134">**GetInputState** returns **TRUE** if the queue contains mouse or keyboard messages.</span></span> <span data-ttu-id="fd23b-135">這兩個函式都可以用來判斷佇列是否包含需要處理的訊息。</span><span class="sxs-lookup"><span data-stu-id="fd23b-135">Both of these functions can be used to determine whether the queue contains messages that need to be processed.</span></span>

## <a name="posting-a-message"></a><span data-ttu-id="fd23b-136">張貼訊息</span><span class="sxs-lookup"><span data-stu-id="fd23b-136">Posting a Message</span></span>

<span data-ttu-id="fd23b-137">您可以使用 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式，將訊息張貼到訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="fd23b-137">You can post a message to a message queue by using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function.</span></span> <span data-ttu-id="fd23b-138">**PostMessage** 會將訊息放線上程訊息佇列的結尾，並立即傳回，而不需等待中的執行緒處理訊息。</span><span class="sxs-lookup"><span data-stu-id="fd23b-138">**PostMessage** places a message at the end of a thread's message queue and returns immediately, without waiting for the thread to process the message.</span></span> <span data-ttu-id="fd23b-139">函數的參數包含視窗控制碼、訊息識別碼和兩個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="fd23b-139">The function's parameters include a window handle, a message identifier, and two message parameters.</span></span> <span data-ttu-id="fd23b-140">系統會將這些參數複製到 [**訊息結構，**](/windows/win32/api/winuser/ns-winuser-msg) 填滿結構的 **時間** 和 **pt** 成員，然後將結構放在訊息佇列中。</span><span class="sxs-lookup"><span data-stu-id="fd23b-140">The system copies these parameters to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure, fills the **time** and **pt** members of the structure, and places the structure in the message queue.</span></span>

<span data-ttu-id="fd23b-141">系統會使用與 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式一起傳遞的視窗控制碼，判斷哪個執行緒訊息佇列應該接收訊息。</span><span class="sxs-lookup"><span data-stu-id="fd23b-141">The system uses the window handle passed with the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to determine which thread message queue should receive the message.</span></span> <span data-ttu-id="fd23b-142">如果控制碼是 **HWND \_ 最上層** 的，系統會將訊息張貼至所有最上層視窗的執行緒訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="fd23b-142">If the handle is **HWND\_TOPMOST**, the system posts the message to the thread message queues of all top-level windows.</span></span>

<span data-ttu-id="fd23b-143">您可以使用 [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) 函式，將訊息張貼至特定的執行緒訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="fd23b-143">You can use the [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) function to post a message to a specific thread message queue.</span></span> <span data-ttu-id="fd23b-144">**PostThreadMessage** 與 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)類似，但第一個參數是執行緒識別碼而非視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="fd23b-144">**PostThreadMessage** is similar to [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), except the first parameter is a thread identifier rather than a window handle.</span></span> <span data-ttu-id="fd23b-145">您可以藉由呼叫 [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) 函數來取出執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd23b-145">You can retrieve the thread identifier by calling the [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) function.</span></span>

<span data-ttu-id="fd23b-146">使用 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) 函式來結束訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="fd23b-146">Use the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to exit a message loop.</span></span> <span data-ttu-id="fd23b-147">**PostQuitMessage** 會將 [**WM \_**](wm-quit.md) 結束訊息張貼至目前執行中的執行緒。</span><span class="sxs-lookup"><span data-stu-id="fd23b-147">**PostQuitMessage** posts the [**WM\_QUIT**](wm-quit.md) message to the currently executing thread.</span></span> <span data-ttu-id="fd23b-148">執行緒的訊息迴圈會終止，並在遇到 **WM \_** 結束訊息時將控制權傳回給系統。</span><span class="sxs-lookup"><span data-stu-id="fd23b-148">The thread's message loop terminates and returns control to the system when it encounters the **WM\_QUIT** message.</span></span> <span data-ttu-id="fd23b-149">應用程式通常會呼叫 **PostQuitMessage** 來回應 [**WM \_ 摧毀**](wm-destroy.md) 訊息，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="fd23b-149">An application usually calls **PostQuitMessage** in response to the [**WM\_DESTROY**](wm-destroy.md) message, as shown in the following example.</span></span>


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a><span data-ttu-id="fd23b-150">傳送訊息</span><span class="sxs-lookup"><span data-stu-id="fd23b-150">Sending a Message</span></span>

<span data-ttu-id="fd23b-151">[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)函式是用來將訊息直接傳送至視窗程式。</span><span class="sxs-lookup"><span data-stu-id="fd23b-151">The [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function is used to send a message directly to a window procedure.</span></span> <span data-ttu-id="fd23b-152">**SendMessage** 會呼叫視窗程式，並等候該程式處理訊息並傳回結果。</span><span class="sxs-lookup"><span data-stu-id="fd23b-152">**SendMessage** calls a window procedure and waits for that procedure to process the message and return a result.</span></span>

<span data-ttu-id="fd23b-153">訊息可以傳送至系統中的任何視窗;所有必要的都是視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="fd23b-153">A message can be sent to any window in the system; all that is required is a window handle.</span></span> <span data-ttu-id="fd23b-154">系統會使用此控制碼來判斷應該接收訊息的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="fd23b-154">The system uses the handle to determine which window procedure should receive the message.</span></span>

<span data-ttu-id="fd23b-155">在處理可能已經從其他執行緒傳送的訊息之前，視窗程式應該先呼叫 [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) 函式。</span><span class="sxs-lookup"><span data-stu-id="fd23b-155">Before processing a message that may have been sent from another thread, a window procedure should first call the [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) function.</span></span> <span data-ttu-id="fd23b-156">如果此函式傳回 **TRUE**，則視窗程式應該在任何導致執行緒產生控制權的函式之前呼叫 [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) ，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="fd23b-156">If this function returns **TRUE**, the window procedure should call [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) before any function that causes the thread to yield control, as shown in the following example.</span></span>


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



<span data-ttu-id="fd23b-157">您可以將數個訊息傳送至對話方塊中的控制項。</span><span class="sxs-lookup"><span data-stu-id="fd23b-157">A number of messages can be sent to controls in a dialog box.</span></span> <span data-ttu-id="fd23b-158">這些控制訊息會設定控制項的外觀、行為和內容，或取得控制項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fd23b-158">These control messages set the appearance, behavior, and content of controls or retrieve information about controls.</span></span> <span data-ttu-id="fd23b-159">例如， [**CB \_ ADDSTRING**](../controls/cb-addstring.md) 訊息可以將字串新增至下拉式方塊，而 [**BM \_ SETCHECK**](../controls/bm-setcheck.md) 訊息可以設定核取方塊或選項按鈕的核取狀態。</span><span class="sxs-lookup"><span data-stu-id="fd23b-159">For example, the [**CB\_ADDSTRING**](../controls/cb-addstring.md) message can add a string to a combo box, and the [**BM\_SETCHECK**](../controls/bm-setcheck.md) message can set the check state of a check box or radio button.</span></span>

<span data-ttu-id="fd23b-160">您可以使用 [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) 函式來傳送訊息給控制項，並指定控制項的識別碼，以及包含控制項之對話方塊視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fd23b-160">Use the [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) function to send a message to a control, specifying the identifier of the control and the handle of the dialog box window that contains the control.</span></span> <span data-ttu-id="fd23b-161">下列範例取自對話方塊程式，會將字串從下拉式方塊的編輯控制項複製到其清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="fd23b-161">The following example, taken from a dialog box procedure, copies a string from a combo box's edit control into its list box.</span></span> <span data-ttu-id="fd23b-162">此範例會使用 **SendDlgItemMessage** 將 [**CB \_ ADDSTRING**](../controls/cb-addstring.md) 訊息傳送至下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="fd23b-162">The example uses **SendDlgItemMessage** to send a [**CB\_ADDSTRING**](../controls/cb-addstring.md) message to the combo box.</span></span>


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
