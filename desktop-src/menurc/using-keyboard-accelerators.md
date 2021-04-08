---
title: 使用鍵盤加速器
description: 本節涵蓋與鍵盤快速鍵相關聯的工作。
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- 使用者輸入，鍵盤快速鍵
- 捕獲使用者輸入，鍵盤快捷
- 鍵盤加速器
- 加速器
- 快速鍵對應表
- 快速鍵-資料表資源
- 轉譯快速鍵函數
- WM_COMMAND 訊息
- WM_SYS 命令訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023463"
---
# <a name="using-keyboard-accelerators"></a><span data-ttu-id="eef66-112">使用鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="eef66-112">Using Keyboard Accelerators</span></span>

<span data-ttu-id="eef66-113">本節涵蓋與鍵盤快速鍵相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="eef66-113">This section covers tasks that are associated with keyboard accelerators.</span></span>

-   [<span data-ttu-id="eef66-114">使用快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-114">Using an Accelerator Table Resource</span></span>](#using-an-accelerator-table-resource)
    -   [<span data-ttu-id="eef66-115">建立快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-115">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
    -   [<span data-ttu-id="eef66-116">載入快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-116">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
    -   [<span data-ttu-id="eef66-117">呼叫轉譯快速鍵函數</span><span class="sxs-lookup"><span data-stu-id="eef66-117">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
    -   [<span data-ttu-id="eef66-118">處理 WM \_ 命令訊息</span><span class="sxs-lookup"><span data-stu-id="eef66-118">Processing WM\_COMMAND Messages</span></span>](/windows)
    -   [<span data-ttu-id="eef66-119">終結快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-119">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
    -   [<span data-ttu-id="eef66-120">建立字型屬性的快速鍵</span><span class="sxs-lookup"><span data-stu-id="eef66-120">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)
-   [<span data-ttu-id="eef66-121">使用在執行時間建立的快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="eef66-121">Using an Accelerator Table Created at Run Time</span></span>](#using-an-accelerator-table-created-at-run-time)
    -   [<span data-ttu-id="eef66-122">建立 Run-Time 快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="eef66-122">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
    -   [<span data-ttu-id="eef66-123">處理加速器</span><span class="sxs-lookup"><span data-stu-id="eef66-123">Processing Accelerators</span></span>](#processing-accelerators)
    -   [<span data-ttu-id="eef66-124">終結 Run-Time 的快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="eef66-124">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
    -   [<span data-ttu-id="eef66-125">建立使用者可編輯的加速器</span><span class="sxs-lookup"><span data-stu-id="eef66-125">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a><span data-ttu-id="eef66-126">使用快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-126">Using an Accelerator Table Resource</span></span>

<span data-ttu-id="eef66-127">若要將加速器支援新增至應用程式，最常見的方法是在執行時間包含具有應用程式可執行檔的快速鍵對應表資源，然後載入資源。</span><span class="sxs-lookup"><span data-stu-id="eef66-127">The most common way to add accelerator support to an application is to include an accelerator-table resource with the application's executable file and then load the resource at run time.</span></span>

<span data-ttu-id="eef66-128">本節涵蓋下列主題。</span><span class="sxs-lookup"><span data-stu-id="eef66-128">This section covers the following topics.</span></span>

-   [<span data-ttu-id="eef66-129">建立快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-129">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
-   [<span data-ttu-id="eef66-130">載入快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-130">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
-   [<span data-ttu-id="eef66-131">呼叫轉譯快速鍵函數</span><span class="sxs-lookup"><span data-stu-id="eef66-131">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
-   [<span data-ttu-id="eef66-132">處理 WM \_ 命令訊息</span><span class="sxs-lookup"><span data-stu-id="eef66-132">Processing WM\_COMMAND Messages</span></span>](/windows)
-   [<span data-ttu-id="eef66-133">終結快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-133">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
-   [<span data-ttu-id="eef66-134">建立字型屬性的快速鍵</span><span class="sxs-lookup"><span data-stu-id="eef66-134">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a><span data-ttu-id="eef66-135">建立快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-135">Creating the Accelerator Table Resource</span></span>

<span data-ttu-id="eef66-136">您可以在應用程式的資源定義檔中使用 [快速鍵](./accelerators-resource.md) 語句來建立快速鍵對應表資源。</span><span class="sxs-lookup"><span data-stu-id="eef66-136">You create an accelerator-table resource by using the [ACCELERATORS](./accelerators-resource.md) statement in your application's resource-definition file.</span></span> <span data-ttu-id="eef66-137">您必須將名稱或資源識別碼指派給快速鍵對應表，最好與任何其他資源的名稱或資源識別碼不同。</span><span class="sxs-lookup"><span data-stu-id="eef66-137">You must assign a name or resource identifier to the accelerator table, preferably unlike that of any other resource.</span></span> <span data-ttu-id="eef66-138">系統會在執行時間使用此識別碼來載入資源。</span><span class="sxs-lookup"><span data-stu-id="eef66-138">The system uses this identifier to load the resource at run time.</span></span>

<span data-ttu-id="eef66-139">您所定義的每個加速器都需要快速鍵對應表中的個別專案。</span><span class="sxs-lookup"><span data-stu-id="eef66-139">Each accelerator you define requires a separate entry in the accelerator table.</span></span> <span data-ttu-id="eef66-140">在每個專案中，您可以定義擊鍵 (可產生快速鍵的 ASCII 字元碼或虛擬按鍵程式碼) ，以及加速器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eef66-140">In each entry, you define the keystroke (either an ASCII character code or virtual-key code) that generates the accelerator and the accelerator's identifier.</span></span> <span data-ttu-id="eef66-141">您也必須指定按鍵是否必須搭配 ALT、SHIFT 或 CTRL 鍵一起使用。</span><span class="sxs-lookup"><span data-stu-id="eef66-141">You must also specify whether the keystroke must be used in some combination with the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="eef66-142">如需虛擬機器碼的詳細資訊，請參閱 [鍵盤輸入](/windows/desktop/inputdev/keyboard-input)。</span><span class="sxs-lookup"><span data-stu-id="eef66-142">For more information about virtual keys, see [Keyboard Input](/windows/desktop/inputdev/keyboard-input).</span></span>

<span data-ttu-id="eef66-143">您可以用雙引號括住 ASCII 字元，或使用字元的整數值搭配 ASCII 旗標來指定 ASCII 按鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-143">An ASCII keystroke is specified either by enclosing the ASCII character in double quotation marks or by using the integer value of the character in combination with the ASCII flag.</span></span> <span data-ttu-id="eef66-144">下列範例示範如何定義 ASCII 加速器。</span><span class="sxs-lookup"><span data-stu-id="eef66-144">The following examples show how to define ASCII accelerators.</span></span>

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

<span data-ttu-id="eef66-145">根據按鍵是英數位鍵還是非英數位鍵，以不同的方式指定虛擬按鍵程式碼按鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-145">A virtual-key code keystroke is specified differently depending on whether the keystroke is an alphanumeric key or a non-alphanumeric key.</span></span> <span data-ttu-id="eef66-146">若為英數位元，以雙引號括住的索引鍵字母或數位，會與 **VIRTKEY** 旗標合併。</span><span class="sxs-lookup"><span data-stu-id="eef66-146">For an alphanumeric key, the key's letter or number, enclosed in double quotation marks, is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="eef66-147">針對非英數位元，特定索引鍵的虛擬金鑰程式碼會與 **VIRTKEY** 旗標合併。</span><span class="sxs-lookup"><span data-stu-id="eef66-147">For a non-alphanumeric key, the virtual-key code for the specific key is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="eef66-148">下列範例示範如何定義虛擬金鑰程式碼加速器。</span><span class="sxs-lookup"><span data-stu-id="eef66-148">The following examples show how to define virtual-key code accelerators.</span></span>

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

<span data-ttu-id="eef66-149">下列範例顯示的快速鍵對應表資源會定義檔案作業的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-149">The following example shows an accelerator-table resource that defines accelerators for file operations.</span></span> <span data-ttu-id="eef66-150">資源的名稱是 *FileAccel*。</span><span class="sxs-lookup"><span data-stu-id="eef66-150">The name of the resource is *FileAccel*.</span></span>

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

<span data-ttu-id="eef66-151">如果您想要讓使用者按下 ALT、SHIFT 或 CTRL 鍵並搭配快速鍵按鍵，請在快速鍵的定義中指定 ALT、SHIFT 和 CONTROL 旗標。</span><span class="sxs-lookup"><span data-stu-id="eef66-151">If you want the user to press the ALT, SHIFT, or CTRL keys in some combination with the accelerator keystroke, specify the ALT, SHIFT, and CONTROL flags in the accelerator's definition.</span></span> <span data-ttu-id="eef66-152">以下有一些範例。</span><span class="sxs-lookup"><span data-stu-id="eef66-152">Following are some examples.</span></span>

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

<span data-ttu-id="eef66-153">依預設，當快速鍵對應至功能表項目時，系統會反白顯示功能表項目。</span><span class="sxs-lookup"><span data-stu-id="eef66-153">By default, when an accelerator key corresponds to a menu item, the system highlights the menu item.</span></span> <span data-ttu-id="eef66-154">您可以使用 **NOINVERT** 旗標來防止針對個別加速器進行反白顯示。</span><span class="sxs-lookup"><span data-stu-id="eef66-154">You can use the **NOINVERT** flag to prevent highlighting for an individual accelerator.</span></span> <span data-ttu-id="eef66-155">下列範例顯示如何使用 **NOINVERT** 旗標：</span><span class="sxs-lookup"><span data-stu-id="eef66-155">The following example shows how to use the **NOINVERT** flag:</span></span>

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

<span data-ttu-id="eef66-156">若要定義對應到應用程式中功能表項目的快速鍵，請在功能表項目的文字中包含快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-156">To define accelerators that correspond to menu items in your application, include the accelerators in the text of the menu items.</span></span> <span data-ttu-id="eef66-157">下列範例顯示如何在資源定義檔中的功能表項目文字中包含快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-157">The following example shows how to include accelerators in menu-item text in a resource-definition file.</span></span>

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a><span data-ttu-id="eef66-158">載入快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-158">Loading the Accelerator Table Resource</span></span>

<span data-ttu-id="eef66-159">應用程式會藉由呼叫 [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) 函式，並指定應用程式的實例控制碼（可執行檔包含資源和資源的名稱或識別碼），來載入快速鍵對應表資源。</span><span class="sxs-lookup"><span data-stu-id="eef66-159">An application loads an accelerator-table resource by calling the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function and specifying the instance handle to the application whose executable file contains the resource and the name or identifier of the resource.</span></span> <span data-ttu-id="eef66-160">**LoadAccelerators** 會將指定的快速鍵對應表載入至記憶體，並將控制碼傳回至快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="eef66-160">**LoadAccelerators** loads the specified accelerator table into memory and returns the handle to the accelerator table.</span></span>

<span data-ttu-id="eef66-161">應用程式可以隨時載入快速鍵對應表資源。</span><span class="sxs-lookup"><span data-stu-id="eef66-161">An application can load an accelerator-table resource at any time.</span></span> <span data-ttu-id="eef66-162">通常，單一執行緒應用程式會在輸入其主要訊息迴圈之前載入其快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="eef66-162">Usually, a single-threaded application loads its accelerator table before entering its main message loop.</span></span> <span data-ttu-id="eef66-163">使用多個執行緒的應用程式通常會在進入執行緒的訊息迴圈之前，先載入執行緒的快速鍵對應表資源。</span><span class="sxs-lookup"><span data-stu-id="eef66-163">An application that uses multiple threads typically loads the accelerator-table resource for a thread before entering the message loop for the thread.</span></span> <span data-ttu-id="eef66-164">應用程式或執行緒也可能會使用多個快速鍵對應表，每個都與應用程式中的特定視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="eef66-164">An application or thread might also use multiple accelerator tables, each associated with a particular window in the application.</span></span> <span data-ttu-id="eef66-165">這類應用程式會在每次使用者啟動視窗時載入視窗的快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="eef66-165">Such an application would load the accelerator table for the window each time the user activated the window.</span></span> <span data-ttu-id="eef66-166">如需執行緒的詳細資訊，請參閱 [進程和執行緒](/windows/desktop/ProcThread/processes-and-threads)。</span><span class="sxs-lookup"><span data-stu-id="eef66-166">For more information about threads, see [Processes and Threads](/windows/desktop/ProcThread/processes-and-threads).</span></span>

### <a name="calling-the-translate-accelerator-function"></a><span data-ttu-id="eef66-167">呼叫轉譯快速鍵函數</span><span class="sxs-lookup"><span data-stu-id="eef66-167">Calling the Translate Accelerator Function</span></span>

<span data-ttu-id="eef66-168">若要處理快速鍵，應用程式的 (或執行緒的) 訊息迴圈必須包含 [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) 函式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="eef66-168">To process accelerators, an application's (or thread's) message loop must contain a call to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function.</span></span> <span data-ttu-id="eef66-169">**TranslateAccelerator** 會比較按鍵與快速鍵對應表，如果找到相符項，則會將按鍵轉譯為 [**wm \_ 命令**](wm-command.md) (或 [**wm \_ SYSCOMMAND**](wm-syscommand.md)) 訊息。</span><span class="sxs-lookup"><span data-stu-id="eef66-169">**TranslateAccelerator** compares keystrokes to an accelerator table and, if it finds a match, translates the keystrokes into a [**WM\_COMMAND**](wm-command.md) (or [**WM\_SYSCOMMAND**](wm-syscommand.md)) message.</span></span> <span data-ttu-id="eef66-170">然後，此函式會將訊息傳送至視窗程式。</span><span class="sxs-lookup"><span data-stu-id="eef66-170">The function then sends the message to a window procedure.</span></span> <span data-ttu-id="eef66-171">**TranslateAccelerator** 函式的參數包含視窗的控制碼，此控制碼是接收 **WM \_ 命令** 訊息的視窗控制碼、用來轉譯快速鍵之快速鍵對應表的控制碼，以及包含佇列中訊息的訊息結構指標。 [](/windows/win32/api/winuser/ns-winuser-msg)</span><span class="sxs-lookup"><span data-stu-id="eef66-171">The parameters of the **TranslateAccelerator** function include the handle to the window that is to receive the **WM\_COMMAND** messages, the handle to the accelerator table used to translate accelerators, and a pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure containing a message from the queue.</span></span> <span data-ttu-id="eef66-172">下列範例顯示如何從訊息迴圈內呼叫 **TranslateAccelerator** 。</span><span class="sxs-lookup"><span data-stu-id="eef66-172">The following example shows how to call **TranslateAccelerator** from within a message loop.</span></span>


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a><span data-ttu-id="eef66-173">處理 WM \_ 命令訊息</span><span class="sxs-lookup"><span data-stu-id="eef66-173">Processing WM\_COMMAND Messages</span></span>

<span data-ttu-id="eef66-174">使用加速器時， [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) 函式中指定的視窗會收到 [**Wm \_ 命令**](wm-command.md) 或 [**wm \_ SYSCOMMAND**](wm-syscommand.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="eef66-174">When an accelerator is used, the window specified in the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function receives a [**WM\_COMMAND**](wm-command.md) or [**WM\_SYSCOMMAND**](wm-syscommand.md) message.</span></span> <span data-ttu-id="eef66-175">*WParam* 參數的低序位文字包含快速鍵的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eef66-175">The low-order word of the *wParam* parameter contains the identifier of the accelerator.</span></span> <span data-ttu-id="eef66-176">視窗程式會檢查識別碼，以判斷 **WM \_ 命令** 訊息的來源，並據以處理訊息。</span><span class="sxs-lookup"><span data-stu-id="eef66-176">The window procedure examines the identifier to determine the source of the **WM\_COMMAND** message and process the message accordingly.</span></span>

<span data-ttu-id="eef66-177">一般而言，如果快速鍵對應到應用程式中的功能表項目，則會將相同的識別碼指派給快速鍵和功能表項目。</span><span class="sxs-lookup"><span data-stu-id="eef66-177">Typically, if an accelerator corresponds to a menu item in the application, the accelerator and menu item are assigned the same identifier.</span></span> <span data-ttu-id="eef66-178">如果您需要知道是否已由加速器或功能表項目產生 [**WM \_ 命令**](wm-command.md) 訊息，您可以檢查 *wParam* 參數的高序位字組。</span><span class="sxs-lookup"><span data-stu-id="eef66-178">If you need to know whether a [**WM\_COMMAND**](wm-command.md) message was generated by an accelerator or by a menu item, you can examine the high-order word of the *wParam* parameter.</span></span> <span data-ttu-id="eef66-179">如果快速鍵產生訊息，則高序位字是 1;如果功能表項目產生訊息，則高序位字是0。</span><span class="sxs-lookup"><span data-stu-id="eef66-179">If an accelerator generated the message, the high-order word is 1; if a menu item generated the message, the high-order word is 0.</span></span>

### <a name="destroying-the-accelerator-table-resource"></a><span data-ttu-id="eef66-180">終結快速鍵對應表資源</span><span class="sxs-lookup"><span data-stu-id="eef66-180">Destroying the Accelerator Table Resource</span></span>

<span data-ttu-id="eef66-181">系統會自動終結 [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) 函式所載入的快速鍵對應表資源，並在應用程式關閉後，從記憶體中移除資源。</span><span class="sxs-lookup"><span data-stu-id="eef66-181">The system automatically destroys accelerator-table resources loaded by the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function, removing the resource from memory after the application closes.</span></span>

### <a name="creating-accelerators-for-font-attributes"></a><span data-ttu-id="eef66-182">建立字型屬性的快速鍵</span><span class="sxs-lookup"><span data-stu-id="eef66-182">Creating Accelerators for Font Attributes</span></span>

<span data-ttu-id="eef66-183">本節中的範例說明如何執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="eef66-183">The example in this section shows how to perform the following tasks:</span></span>

-   <span data-ttu-id="eef66-184">建立快速鍵對應表資源。</span><span class="sxs-lookup"><span data-stu-id="eef66-184">Create an accelerator-table resource.</span></span>
-   <span data-ttu-id="eef66-185">在執行時間載入快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="eef66-185">Load the accelerator table at run time.</span></span>
-   <span data-ttu-id="eef66-186">在訊息迴圈中轉譯快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-186">Translate accelerators in a message loop.</span></span>
-   <span data-ttu-id="eef66-187">處理加速器所產生的 [**WM \_ 命令**](wm-command.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="eef66-187">Process [**WM\_COMMAND**](wm-command.md) messages generated by the accelerators.</span></span>

<span data-ttu-id="eef66-188">這些工作會在應用程式的內容中示範，此應用程式包含 **字元** 功能表和對應的快速鍵，可讓使用者選取目前字型的屬性。</span><span class="sxs-lookup"><span data-stu-id="eef66-188">These tasks are demonstrated in the context of an application that includes a **Character** menu and corresponding accelerators that allow the user to select attributes of the current font.</span></span>

<span data-ttu-id="eef66-189">資源定義檔的下列部分會定義 **字元** 功能表和相關聯的快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="eef66-189">The following portion of a resource-definition file defines the **Character** menu and the associated accelerator table.</span></span> <span data-ttu-id="eef66-190">請注意，功能表項目會顯示快速鍵按鍵，而且每個加速器都有與其相關聯功能表項目相同的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eef66-190">Note that the menu items show the accelerator keystrokes and that each accelerator has the same identifier as its associated menu item.</span></span>


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



<span data-ttu-id="eef66-191">應用程式原始程式檔中的下列各節會示範如何執行加速器。</span><span class="sxs-lookup"><span data-stu-id="eef66-191">The following sections from the application's source file show how to implement the accelerators.</span></span>


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a><span data-ttu-id="eef66-192">使用在執行時間建立的快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="eef66-192">Using an Accelerator Table Created at Run Time</span></span>

<span data-ttu-id="eef66-193">本主題討論如何使用在執行時間建立的快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="eef66-193">This topic discusses how to use accelerator tables created at run time.</span></span>

-   [<span data-ttu-id="eef66-194">建立 Run-Time 快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="eef66-194">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
-   [<span data-ttu-id="eef66-195">處理加速器</span><span class="sxs-lookup"><span data-stu-id="eef66-195">Processing Accelerators</span></span>](#processing-accelerators)
-   [<span data-ttu-id="eef66-196">終結 Run-Time 的快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="eef66-196">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
-   [<span data-ttu-id="eef66-197">建立使用者可編輯的加速器</span><span class="sxs-lookup"><span data-stu-id="eef66-197">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a><span data-ttu-id="eef66-198">建立 Run-Time 快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="eef66-198">Creating a Run-Time Accelerator Table</span></span>

<span data-ttu-id="eef66-199">在執行時間建立快速鍵對應表的第一個步驟是填入 [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="eef66-199">The first step in creating an accelerator table at run time is filling an array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures.</span></span> <span data-ttu-id="eef66-200">陣列中的每個結構會定義資料表中的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-200">Each structure in the array defines an accelerator in the table.</span></span> <span data-ttu-id="eef66-201">加速器的定義包含其旗標、其索引鍵和識別碼。</span><span class="sxs-lookup"><span data-stu-id="eef66-201">An accelerator's definition includes its flags, its key, and its identifier.</span></span> <span data-ttu-id="eef66-202">**ACCEL** 結構具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="eef66-202">The **ACCEL** structure has the following form.</span></span>

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

<span data-ttu-id="eef66-203">您可以藉由在 [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel)結構的索引 **鍵** 成員中指定 ASCII 字元碼或虛擬機器碼，來定義加速器的按鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-203">You define an accelerator's keystroke by specifying an ASCII character code or a virtual-key code in the **key** member of the [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structure.</span></span> <span data-ttu-id="eef66-204">如果您指定虛擬金鑰程式碼，則必須先在 **fVirt** 成員中包含 **FVIRTKEY** 旗標;否則，系統會將程式碼解釋為 ASCII 字元碼。</span><span class="sxs-lookup"><span data-stu-id="eef66-204">If you specify a virtual-key code, you must first include the **FVIRTKEY** flag in the **fVirt** member; otherwise, the system interprets the code as an ASCII character code.</span></span> <span data-ttu-id="eef66-205">您可以包含 **FCONTROL**、 **FALT** 或 **FSHIFT** 旗標，或全部三個來合併 CTRL、ALT 或 SHIFT 鍵與按鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-205">You can include the **FCONTROL**, **FALT**, or **FSHIFT** flag, or all three, to combine the CTRL, ALT, or SHIFT key with the keystroke.</span></span>

<span data-ttu-id="eef66-206">若要建立快速鍵對應表，請將 [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) 結構陣列的指標傳遞至 [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) 函數。</span><span class="sxs-lookup"><span data-stu-id="eef66-206">To create the accelerator table, pass a pointer to the array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures to the [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) function.</span></span> <span data-ttu-id="eef66-207">**CreateAcceleratorTable** 會建立快速鍵對應表，並將控制碼傳回資料表。</span><span class="sxs-lookup"><span data-stu-id="eef66-207">**CreateAcceleratorTable** creates the accelerator table and returns the handle to the table.</span></span>

### <a name="processing-accelerators"></a><span data-ttu-id="eef66-208">處理加速器</span><span class="sxs-lookup"><span data-stu-id="eef66-208">Processing Accelerators</span></span>

<span data-ttu-id="eef66-209">載入和呼叫快速鍵（在執行時間所建立）所提供之快速鍵的程式，與處理快速鍵對應表資源所提供的快速鍵相同。</span><span class="sxs-lookup"><span data-stu-id="eef66-209">The process of loading and calling accelerators provided by an accelerator table created at run time is the same as processing those provided by an accelerator-table resource.</span></span> <span data-ttu-id="eef66-210">如需詳細資訊，請參閱透過[處理 WM \_ 命令訊息](/windows)來[載入快速鍵對應表資源](#loading-the-accelerator-table-resource)。</span><span class="sxs-lookup"><span data-stu-id="eef66-210">For more information, see [Loading the Accelerator Table Resource](#loading-the-accelerator-table-resource) through [Processing WM\_COMMAND Messages](/windows).</span></span>

### <a name="destroying-a-run-time-accelerator-table"></a><span data-ttu-id="eef66-211">終結 Run-Time 的快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="eef66-211">Destroying a Run-Time Accelerator Table</span></span>

<span data-ttu-id="eef66-212">系統會自動終結在執行時間建立的快速鍵對應表，並在應用程式關閉後，從記憶體中移除資源。</span><span class="sxs-lookup"><span data-stu-id="eef66-212">The system automatically destroys accelerator tables created at run time, removing the resources from memory after the application closes.</span></span> <span data-ttu-id="eef66-213">您可以終結快速鍵對應表，並將資料表的控制碼傳遞至 [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) 函式，以在先前的記憶體中將其移除。</span><span class="sxs-lookup"><span data-stu-id="eef66-213">You can destroy an accelerator table and remove it from memory earlier by passing the table's handle to the [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) function.</span></span>

### <a name="creating-user-editable-accelerators"></a><span data-ttu-id="eef66-214">建立使用者可編輯的加速器</span><span class="sxs-lookup"><span data-stu-id="eef66-214">Creating User Editable Accelerators</span></span>

<span data-ttu-id="eef66-215">這個範例示範如何建立可讓使用者變更與功能表項目相關聯之快速鍵的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="eef66-215">This example shows how to construct a dialog box that allows the user to change the accelerator associated with a menu item.</span></span> <span data-ttu-id="eef66-216">此對話方塊包含包含功能表項目的下拉式方塊、包含索引鍵名稱的下拉式方塊，以及用來選取 CTRL、ALT 和 SHIFT 鍵的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="eef66-216">The dialog box consists of a combo box containing menu items, a combo box containing the names of keys, and check boxes for selecting the CTRL, ALT, and SHIFT keys.</span></span> <span data-ttu-id="eef66-217">下圖顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="eef66-217">The following illustration shows the dialog box.</span></span>

![具有下拉式方塊和核取方塊的對話方塊](images/useredit.gif)

<span data-ttu-id="eef66-219">下列範例顯示如何在資源定義檔中定義對話方塊。</span><span class="sxs-lookup"><span data-stu-id="eef66-219">The following example shows how the dialog box is defined in the resource-definition file.</span></span>

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

<span data-ttu-id="eef66-220">應用程式的功能表列包含一個 **字元** 子功能表，其專案具有與其相關聯的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eef66-220">The application's menu bar contains a **Character** submenu whose items have accelerators associated with them.</span></span>

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

<span data-ttu-id="eef66-221">功能表範本的功能表項目值是在應用程式的標頭檔中定義如下的常數。</span><span class="sxs-lookup"><span data-stu-id="eef66-221">The menu item values for the menu template are constants defined as follows in the application's header file.</span></span>

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

<span data-ttu-id="eef66-222">對話方塊會使用應用程式定義的 VKEY 結構陣列，其中每個結構都包含按鍵文字字串和快速鍵文字字串。</span><span class="sxs-lookup"><span data-stu-id="eef66-222">The dialog box uses an array of application-defined VKEY structures, each containing a keystroke-text string and an accelerator-text string.</span></span> <span data-ttu-id="eef66-223">建立對話方塊時，它會剖析陣列，並將每個按鍵文字字串新增至 [ **選取按鍵** ] 下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="eef66-223">When the dialog box is created, it parses the array and adds each keystroke-text string to the **Select Keystroke** combo box.</span></span> <span data-ttu-id="eef66-224">當使用者按一下 [ **確定]** 按鈕時，對話方塊會查閱選取的按鍵文字字串，並抓取對應的快速鍵文字字串。</span><span class="sxs-lookup"><span data-stu-id="eef66-224">When the user clicks the **OK** button, the dialog box looks up the selected keystroke-text string and retrieves the corresponding accelerator-text string.</span></span> <span data-ttu-id="eef66-225">對話方塊會將快速鍵文字字串附加至使用者選取之功能表項目的文字。</span><span class="sxs-lookup"><span data-stu-id="eef66-225">The dialog box appends the accelerator-text string to the text of the menu item that the user selected.</span></span> <span data-ttu-id="eef66-226">下列範例顯示 VKEY 結構的陣列：</span><span class="sxs-lookup"><span data-stu-id="eef66-226">The following example shows the array of VKEY structures:</span></span>


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



<span data-ttu-id="eef66-227">對話方塊的初始化程式會填滿 **選取專案** 並 **選取擊鍵** 下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="eef66-227">The dialog box's initialization procedure fills the **Select Item** and **Select Keystroke** combo boxes.</span></span> <span data-ttu-id="eef66-228">當使用者選取功能表項目和相關聯的快速鍵之後，對話方塊會檢查對話方塊中的控制項，以取得使用者的選取專案、更新功能表項目的文字，然後建立包含使用者定義新快速鍵的新快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="eef66-228">After the user selects a menu item and associated accelerator, the dialog box examines the controls in the dialog box to get the user's selection, updates the text of the menu item, and then creates a new accelerator table that contains the user-defined new accelerator.</span></span> <span data-ttu-id="eef66-229">下列範例顯示對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="eef66-229">The following example shows the dialog-box procedure.</span></span> <span data-ttu-id="eef66-230">請注意，您必須在視窗程式中初始化。</span><span class="sxs-lookup"><span data-stu-id="eef66-230">Note that you must initialize in your window procedure.</span></span>


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 