---
title: 使用對話方塊
description: 您可以使用對話方塊來顯示資訊，並提示使用者輸入。
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Windows 消費者介面、視窗化
- Windows 消費者介面，對話方塊
- 視窗化，對話方塊
- 對話方塊，關於
- 對話方塊，顯示
- 強制回應對話方塊
- 非強制回應對話方塊
- 對話方塊，強制回應
- 對話方塊、非模式
- 對話方塊，初始化
- 對話方塊範本
- 對話方塊、範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023905"
---
# <a name="using-dialog-boxes"></a><span data-ttu-id="034d7-115">使用對話方塊</span><span class="sxs-lookup"><span data-stu-id="034d7-115">Using Dialog Boxes</span></span>

<span data-ttu-id="034d7-116">您可以使用對話方塊來顯示資訊，並提示使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="034d7-116">You use dialog boxes to display information and prompt for input from the user.</span></span> <span data-ttu-id="034d7-117">您的應用程式會載入並初始化對話方塊、處理使用者輸入，並在使用者完成工作時終結對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-117">Your application loads and initializes the dialog box, processes user input, and destroys the dialog box when the user finishes the task.</span></span> <span data-ttu-id="034d7-118">處理對話方塊的處理常式會根據對話方塊為強制回應或非模式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="034d7-118">The process for handling dialog boxes varies, depending on whether the dialog box is modal or modeless.</span></span> <span data-ttu-id="034d7-119">強制回應對話方塊需要使用者先關閉對話方塊，再啟用應用程式中的另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="034d7-119">A modal dialog box requires the user to close the dialog box before activating another window in the application.</span></span> <span data-ttu-id="034d7-120">不過，使用者可以在不同的應用程式中啟動 windows。</span><span class="sxs-lookup"><span data-stu-id="034d7-120">However, the user can activate windows in different applications.</span></span> <span data-ttu-id="034d7-121">非強制回應對話方塊不需要使用者立即回應。</span><span class="sxs-lookup"><span data-stu-id="034d7-121">A modeless dialog box does not require an immediate response from the user.</span></span> <span data-ttu-id="034d7-122">它類似于包含控制項的主視窗。</span><span class="sxs-lookup"><span data-stu-id="034d7-122">It is similar to a main window containing controls.</span></span>

<span data-ttu-id="034d7-123">下列各節將討論如何使用這兩種類型的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-123">The following sections discuss how to use both types of dialog boxes.</span></span>

-   [<span data-ttu-id="034d7-124">顯示訊息方塊</span><span class="sxs-lookup"><span data-stu-id="034d7-124">Displaying a Message Box</span></span>](#displaying-a-message-box)
-   [<span data-ttu-id="034d7-125">建立強制回應對話方塊</span><span class="sxs-lookup"><span data-stu-id="034d7-125">Creating a Modal Dialog Box</span></span>](#creating-a-modal-dialog-box)
-   [<span data-ttu-id="034d7-126">建立非強制回應對話方塊</span><span class="sxs-lookup"><span data-stu-id="034d7-126">Creating a Modeless Dialog Box</span></span>](#creating-a-modeless-dialog-box)
-   [<span data-ttu-id="034d7-127">初始化對話方塊</span><span class="sxs-lookup"><span data-stu-id="034d7-127">Initializing a Dialog Box</span></span>](#initializing-a-dialog-box)
-   [<span data-ttu-id="034d7-128">在記憶體中建立範本</span><span class="sxs-lookup"><span data-stu-id="034d7-128">Creating a Template in Memory</span></span>](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a><span data-ttu-id="034d7-129">顯示訊息方塊</span><span class="sxs-lookup"><span data-stu-id="034d7-129">Displaying a Message Box</span></span>

<span data-ttu-id="034d7-130">強制回應對話方塊最簡單的形式就是訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-130">The simplest form of modal dialog box is the message box.</span></span> <span data-ttu-id="034d7-131">大部分的應用程式會使用訊息方塊來警告使用者的錯誤，並提示您如何在發生錯誤之後繼續進行。</span><span class="sxs-lookup"><span data-stu-id="034d7-131">Most applications use message boxes to warn the user of errors and to prompt for directions on how to proceed after an error has occurred.</span></span> <span data-ttu-id="034d7-132">您可以使用 [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) 或 [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) 函式來建立訊息方塊，並指定訊息以及要顯示的按鈕數目和類型。</span><span class="sxs-lookup"><span data-stu-id="034d7-132">You create a message box by using the [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) or [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) function, specifying the message and the number and type of buttons to display.</span></span> <span data-ttu-id="034d7-133">系統會建立強制回應對話方塊，並提供自己的對話方塊範本和程式。</span><span class="sxs-lookup"><span data-stu-id="034d7-133">The system creates a modal dialog box, providing its own dialog box template and procedure.</span></span> <span data-ttu-id="034d7-134">在使用者關閉訊息方塊之後， **MessageBox** 或 **MessageBoxEx** 會傳回值，指出使用者選擇關閉訊息方塊的按鈕。</span><span class="sxs-lookup"><span data-stu-id="034d7-134">After the user closes the message box, **MessageBox** or **MessageBoxEx** returns a value identifying the button chosen by the user to close the message box.</span></span>

<span data-ttu-id="034d7-135">在下列範例中，應用程式會顯示訊息方塊，以在發生錯誤狀況時提示使用者輸入動作。</span><span class="sxs-lookup"><span data-stu-id="034d7-135">In the following example, the application displays a message box that prompts the user for an action after an error condition has occurred.</span></span> <span data-ttu-id="034d7-136">訊息方塊會顯示描述錯誤狀況的訊息，以及如何解決此問題。</span><span class="sxs-lookup"><span data-stu-id="034d7-136">The message box displays the message that describes the error condition and how to resolve it.</span></span> <span data-ttu-id="034d7-137">**MB \_ YESNO** 樣式會指示 [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox)提供兩個按鈕，讓使用者可以選擇如何繼續：</span><span class="sxs-lookup"><span data-stu-id="034d7-137">The **MB\_YESNO** style directs [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) to provide two buttons with which the user can choose how to proceed:</span></span>


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



<span data-ttu-id="034d7-138">下圖顯示上述程式碼範例的輸出：</span><span class="sxs-lookup"><span data-stu-id="034d7-138">The following image shows the output from the preceding code example:</span></span>

![訊息方塊](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a><span data-ttu-id="034d7-140">建立強制回應對話方塊</span><span class="sxs-lookup"><span data-stu-id="034d7-140">Creating a Modal Dialog Box</span></span>

<span data-ttu-id="034d7-141">您可以使用 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 函數來建立強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-141">You create a modal dialog box by using the [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) function.</span></span> <span data-ttu-id="034d7-142">您必須指定對話方塊範本資源的識別碼或名稱，以及對話方塊程式的指標。</span><span class="sxs-lookup"><span data-stu-id="034d7-142">You must specify the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="034d7-143">**對話方塊** 函式會載入範本、顯示對話方塊，並處理所有使用者輸入，直到使用者關閉對話方塊為止。</span><span class="sxs-lookup"><span data-stu-id="034d7-143">The **DialogBox** function loads the template, displays the dialog box, and processes all user input until the user closes the dialog box.</span></span>

<span data-ttu-id="034d7-144">在下列範例中，當使用者按一下應用程式功能表中的 [ **刪除專案** ] 時，應用程式會顯示模式對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-144">In the following example, the application displays a modal dialog box when the user clicks **Delete Item** from an application menu.</span></span> <span data-ttu-id="034d7-145">對話方塊中包含編輯控制項 (使用者在其中輸入專案的名稱) 和 **[確定] 和 [** **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="034d7-145">The dialog box contains an edit control (in which the user enters the name of an item) and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="034d7-146">這些控制項的控制項識別碼分別為 ID \_ ：//IDOK 和 IDCANCEL。</span><span class="sxs-lookup"><span data-stu-id="034d7-146">The control identifiers for these controls are ID\_ITEMNAME, IDOK, and IDCANCEL, respectively.</span></span>

<span data-ttu-id="034d7-147">此範例的第一個部分是由建立強制回應對話方塊的語句所組成。</span><span class="sxs-lookup"><span data-stu-id="034d7-147">The first part of the example consists of the statements that create the modal dialog box.</span></span> <span data-ttu-id="034d7-148">這些語句（在應用程式主視窗的視窗程式中）會在系統收到具有 IDM DELETEITEM 功能表識別碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息時建立對話方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="034d7-148">These statements, in the window procedure for the application's main window, create the dialog box when the system receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_DELETEITEM menu identifier.</span></span> <span data-ttu-id="034d7-149">範例的第二個部分是對話方塊程式，它會抓取編輯控制項的內容，並在收到 **WM \_ 命令** 訊息時關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-149">The second part of the example is the dialog box procedure, which retrieves the contents of the edit control and closes the dialog box upon receiving a **WM\_COMMAND** message.</span></span>

<span data-ttu-id="034d7-150">下列語句會建立強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-150">The following statements create the modal dialog box.</span></span> <span data-ttu-id="034d7-151">對話方塊範本是應用程式可執行檔中的資源，且資源識別碼為 d \_ DELETEITEM。</span><span class="sxs-lookup"><span data-stu-id="034d7-151">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_DELETEITEM.</span></span>


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="034d7-152">在此範例中，應用程式會將其主視窗指定為對話方塊的擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="034d7-152">In this example, the application specifies its main window as the owner window for the dialog box.</span></span> <span data-ttu-id="034d7-153">當系統一開始顯示對話方塊時，它的位置是相對於擁有者視窗工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="034d7-153">When the system initially displays the dialog box, its position is relative to the upper left corner of the owner window's client area.</span></span> <span data-ttu-id="034d7-154">應用程式會使用來自 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 的傳回值，以判斷是否要繼續操作或取消作業。</span><span class="sxs-lookup"><span data-stu-id="034d7-154">The application uses the return value from [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) to determine whether to proceed with the operation or cancel it.</span></span> <span data-ttu-id="034d7-155">下列語句會定義對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="034d7-155">The following statements define the dialog box procedure.</span></span>


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="034d7-156">在此範例中，程式會使用 [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) ，從 ID 的使用者識別碼所識別的編輯控制項中取出目前的文字 \_ 。</span><span class="sxs-lookup"><span data-stu-id="034d7-156">In this example, the procedure uses [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) to retrieve the current text from the edit control identified by ID\_ITEMNAME.</span></span> <span data-ttu-id="034d7-157">程式接著會呼叫 [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) 函式，將對話方塊的傳回值設定為 IDOK 或 IDCANCEL，視收到的訊息而定，然後開始關閉對話方塊的進程。</span><span class="sxs-lookup"><span data-stu-id="034d7-157">The procedure then calls the [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) function to set the dialog box's return value to either IDOK or IDCANCEL, depending on the message received, and to begin the process of closing the dialog box.</span></span> <span data-ttu-id="034d7-158">IDOK 和 IDCANCEL 識別碼會對應至 [ **確定]** 和 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="034d7-158">The IDOK and IDCANCEL identifiers correspond to the **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="034d7-159">在程式呼叫 **EndDialog** 之後，系統會將其他訊息傳送至程式以終結對話方塊，並將對話方塊的傳回值傳回給建立對話方塊的函式。</span><span class="sxs-lookup"><span data-stu-id="034d7-159">After the procedure calls **EndDialog**, the system sends additional messages to the procedure to destroy the dialog box and returns the dialog box's return value back to the function that created the dialog box.</span></span>

## <a name="creating-a-modeless-dialog-box"></a><span data-ttu-id="034d7-160">建立非強制回應對話方塊</span><span class="sxs-lookup"><span data-stu-id="034d7-160">Creating a Modeless Dialog Box</span></span>

<span data-ttu-id="034d7-161">您可以使用 [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) 函式來建立非強制回應對話方塊，指定對話方塊範本資源的識別碼或名稱，以及對話方塊程式的指標。</span><span class="sxs-lookup"><span data-stu-id="034d7-161">You create a modeless dialog box by using the [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) function, specifying the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="034d7-162">**CreateDialog** 會載入範本、建立對話方塊，並選擇性地顯示此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-162">**CreateDialog** loads the template, creates the dialog box, and optionally displays it.</span></span> <span data-ttu-id="034d7-163">您的應用程式會負責將使用者輸入訊息取出並分派至對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="034d7-163">Your application is responsible for retrieving and dispatching user input messages to the dialog box procedure.</span></span>

<span data-ttu-id="034d7-164">在下列範例中，當使用者按一下應用程式功能表中的 [ **移至** ] 時，應用程式會顯示非強制回應對話方塊（如果尚未顯示）。</span><span class="sxs-lookup"><span data-stu-id="034d7-164">In the following example, the application displays a modeless dialog box — if it is not already displayed — when the user clicks **Go To** from an application menu.</span></span> <span data-ttu-id="034d7-165">對話方塊中包含編輯控制項、核取方塊和 **[確定] 和 [** **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="034d7-165">The dialog box contains an edit control, a check box, and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="034d7-166">對話方塊範本是應用程式可執行檔中的資源，且資源識別碼為 DLG \_ GOTO。</span><span class="sxs-lookup"><span data-stu-id="034d7-166">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_GOTO.</span></span> <span data-ttu-id="034d7-167">使用者在編輯控制項中輸入行號，並核取核取方塊，以指定行號相對於目前的行號。</span><span class="sxs-lookup"><span data-stu-id="034d7-167">The user enters a line number in the edit control and checks the check box to specify that the line number is relative to the current line.</span></span> <span data-ttu-id="034d7-168">控制項識別碼是識別碼 \_ 行、識別碼 \_ ABSREL、IDOK 和 IDCANCEL。</span><span class="sxs-lookup"><span data-stu-id="034d7-168">The control identifiers are ID\_LINE, ID\_ABSREL, IDOK, and IDCANCEL.</span></span>

<span data-ttu-id="034d7-169">範例第一個部分中的語句會建立非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-169">The statements in the first part of the example create the modeless dialog box.</span></span> <span data-ttu-id="034d7-170">這些語句（在應用程式主視窗的視窗程式中）會在視窗程式收到具有 IDM GOTO 功能表識別碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息時建立對話方塊 \_ ，但只有在全域變數尚未包含有效的控制碼時。</span><span class="sxs-lookup"><span data-stu-id="034d7-170">These statements, in the window procedure for the application's main window, create the dialog box when the window procedure receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_GOTO menu identifier, but only if the global variable does not already contain a valid handle.</span></span> <span data-ttu-id="034d7-171">此範例的第二個部分是應用程式的主要訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="034d7-171">The second part of the example is the application's main message loop.</span></span> <span data-ttu-id="034d7-172">迴圈包含 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函式，以確保使用者可以在這個非強制回應對話方塊中使用對話方塊鍵盤介面。</span><span class="sxs-lookup"><span data-stu-id="034d7-172">The loop includes the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function to ensure that the user can use the dialog box keyboard interface in this modeless dialog box.</span></span> <span data-ttu-id="034d7-173">此範例的第三個部分是對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="034d7-173">The third part of the example is the dialog box procedure.</span></span> <span data-ttu-id="034d7-174">當使用者按一下 [ **確定]** 按鈕時，此程式會抓取編輯控制項的內容，並選取核取方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-174">The procedure retrieves the contents of the edit control and check box when the user clicks the **OK** button.</span></span> <span data-ttu-id="034d7-175">當使用者按一下 [ **取消** ] 按鈕時，此程式會終結對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-175">The procedure destroys the dialog box when the user clicks the **Cancel** button.</span></span>


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="034d7-176">在上述語句中， [](/windows/desktop/api/Winuser/nf-winuser-createdialoga)只有在不 `hwndGoto` 包含有效的視窗控制碼時，才會呼叫 CreateDialog。</span><span class="sxs-lookup"><span data-stu-id="034d7-176">In the preceding statements, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) is called only if `hwndGoto` does not contain a valid window handle.</span></span> <span data-ttu-id="034d7-177">這可確保應用程式不會同時顯示兩個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-177">This ensures that the application does not display two dialog boxes at the same time.</span></span> <span data-ttu-id="034d7-178">若要支援這種檢查方法，當它終結對話方塊時，對話程式必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="034d7-178">To support this method of checking, the dialog procedure must set to **NULL** when it destroys the dialog box.</span></span>

<span data-ttu-id="034d7-179">應用程式的訊息迴圈是由下列語句所組成。</span><span class="sxs-lookup"><span data-stu-id="034d7-179">The message loop for an application consists of the following statements.</span></span>


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



<span data-ttu-id="034d7-180">迴圈會將視窗控制碼的有效性檢查至對話方塊，而且只有在控制碼有效時，才會呼叫 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="034d7-180">The loop checks the validity of the window handle to the dialog box and only calls the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function if the handle is valid.</span></span> <span data-ttu-id="034d7-181">**IsDialogMessage** 只會處理屬於對話方塊的訊息。</span><span class="sxs-lookup"><span data-stu-id="034d7-181">**IsDialogMessage** only processes the message if it belongs to the dialog box.</span></span> <span data-ttu-id="034d7-182">否則，它會傳回 **FALSE** ，而迴圈會將訊息分派至適當的視窗。</span><span class="sxs-lookup"><span data-stu-id="034d7-182">Otherwise, it returns **FALSE** and the loop dispatches the message to the appropriate window.</span></span>

<span data-ttu-id="034d7-183">下列語句會定義對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="034d7-183">The following statements define the dialog box procedure.</span></span>


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="034d7-184">在上述語句中，此程式會處理 [**wm \_ INITDIALOG**](wm-initdialog.md) 和 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。</span><span class="sxs-lookup"><span data-stu-id="034d7-184">In the preceding statements, the procedure processes the [**WM\_INITDIALOG**](wm-initdialog.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="034d7-185">在進行 **WM \_ INITDIALOG** 處理時，程式會將全域變數的目前值傳遞至 [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx)，以初始化此核取方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-185">During **WM\_INITDIALOG** processing, the procedure initializes the check box by passing the current value of the global variable to [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span></span> <span data-ttu-id="034d7-186">然後，此程式會傳回 **TRUE** ，以指示系統設定預設的輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="034d7-186">The procedure then returns **TRUE** to direct the system to set the default input focus.</span></span>

<span data-ttu-id="034d7-187">在 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 處理過程中，只有當使用者按一下 [ **取消** ] 按鈕（也就是具有 IDCANCEL 識別碼的按鈕）時，程式才會關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-187">During [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) processing, the procedure closes the dialog box only if the user clicks the **Cancel** button — that is, the button having the IDCANCEL identifier.</span></span> <span data-ttu-id="034d7-188">程式必須呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 來關閉非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-188">The procedure must call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to close a modeless dialog box.</span></span> <span data-ttu-id="034d7-189">請注意，此程式也會將變數設為 **Null** ，以確保相依于這個變數的其他語句會正確運作。</span><span class="sxs-lookup"><span data-stu-id="034d7-189">Notice that the procedure also sets the variable to **NULL** to ensure that other statements that depend on this variable operate correctly.</span></span>

<span data-ttu-id="034d7-190">如果使用者按一下 [ **確定]** 按鈕，程式就會抓取該核取方塊的目前狀態，並將它指派給 **fRelative** 變數。</span><span class="sxs-lookup"><span data-stu-id="034d7-190">If the user clicks the **OK** button, the procedure retrieves the current state of the check box and assigns it to the **fRelative** variable.</span></span> <span data-ttu-id="034d7-191">然後，它會使用變數來從編輯控制項取出行號。</span><span class="sxs-lookup"><span data-stu-id="034d7-191">It then uses the variable to retrieve the line number from the edit control.</span></span> <span data-ttu-id="034d7-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) 會將編輯控制項中的文字轉譯為整數。</span><span class="sxs-lookup"><span data-stu-id="034d7-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) translates the text in the edit control into an integer.</span></span> <span data-ttu-id="034d7-193">**FRelative** 的值會決定函式是否會將數位解讀為帶正負號或不帶正負號的值。</span><span class="sxs-lookup"><span data-stu-id="034d7-193">The value of **fRelative** determines whether the function interprets the number as a signed or unsigned value.</span></span> <span data-ttu-id="034d7-194">如果編輯控制項文字不是有效的數位， **GetDlgItemInt** 會將 **fError** 變數的值設定為非零。</span><span class="sxs-lookup"><span data-stu-id="034d7-194">If the edit control text is not a valid number, **GetDlgItemInt** sets the value of the **fError** variable to nonzero.</span></span> <span data-ttu-id="034d7-195">此程式會檢查此值，以判斷是否要顯示錯誤訊息或執行工作。</span><span class="sxs-lookup"><span data-stu-id="034d7-195">The procedure checks this value to determine whether to display an error message or carry out the task.</span></span> <span data-ttu-id="034d7-196">發生錯誤時，對話方塊程式會將訊息傳送至編輯控制項，並將它導向以選取控制項中的文字，讓使用者可以輕鬆地加以取代。</span><span class="sxs-lookup"><span data-stu-id="034d7-196">In the event of an error, the dialog box procedure sends a message to the edit control, directing it to select the text in the control so that the user can easily replace it.</span></span> <span data-ttu-id="034d7-197">如果 **GetDlgItemInt** 未傳回錯誤，則程式可以執行要求的工作本身，或將訊息傳送至主控視窗，將它導向以執行作業。</span><span class="sxs-lookup"><span data-stu-id="034d7-197">If **GetDlgItemInt** does not return an error, the procedure can either carry out the requested task itself or send a message to the owner window, directing it to carry out the operation.</span></span>

## <a name="initializing-a-dialog-box"></a><span data-ttu-id="034d7-198">初始化對話方塊</span><span class="sxs-lookup"><span data-stu-id="034d7-198">Initializing a Dialog Box</span></span>

<span data-ttu-id="034d7-199">您可以在處理 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息時，初始化對話方塊及其內容。</span><span class="sxs-lookup"><span data-stu-id="034d7-199">You initialize the dialog box and its contents while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="034d7-200">最常見的工作是將控制項初始化，以反映目前的對話方塊設定。</span><span class="sxs-lookup"><span data-stu-id="034d7-200">The most common task is to initialize the controls to reflect the current dialog box settings.</span></span> <span data-ttu-id="034d7-201">另一項常見的工作是在螢幕上或其擁有者視窗內置中對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-201">Another common task is to center a dialog box on the screen or within its owner window.</span></span> <span data-ttu-id="034d7-202">某些對話方塊的實用工作是將輸入焦點設定為指定的控制項，而不接受預設的輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="034d7-202">A useful task for some dialog boxes is to set the input focus to a specified control rather than accept the default input focus.</span></span>

<span data-ttu-id="034d7-203">在下列範例中，對話方塊程式會將對話方塊置中，並在處理 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息時設定輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="034d7-203">In the following example, the dialog box procedure centers the dialog box and sets the input focus while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="034d7-204">為了將對話方塊置中，此程式會抓取對話方塊和主控視窗的視窗矩形，並計算對話方塊的新位置。</span><span class="sxs-lookup"><span data-stu-id="034d7-204">To center the dialog box, the procedure retrieves the window rectangles for the dialog box and the owner window and calculates a new position for the dialog box.</span></span> <span data-ttu-id="034d7-205">若要設定輸入焦點，程式會檢查 *wParam* 參數，以判斷預設輸入焦點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="034d7-205">To set the input focus, the procedure checks the *wParam* parameter to determine the identifier of the default input focus.</span></span>


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



<span data-ttu-id="034d7-206">在上述語句中，此程式會使用 [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) 函式，將擁有者視窗控制碼取出至對話方塊。</span><span class="sxs-lookup"><span data-stu-id="034d7-206">In the preceding statements, the procedure uses the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function to retrieve the owner window handle to a dialog box.</span></span> <span data-ttu-id="034d7-207">函式會將擁有者視窗控制碼傳回至對話方塊，並將父視窗控制碼傳回至子視窗。</span><span class="sxs-lookup"><span data-stu-id="034d7-207">The function returns the owner window handle to dialog boxes, and the parent window handle to child windows.</span></span> <span data-ttu-id="034d7-208">因為應用程式可以建立沒有擁有者的對話方塊，程式會檢查傳回的控制碼，並視需要使用 [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) 函式來取出桌面視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="034d7-208">Because an application can create a dialog box that has no owner, the procedure checks the returned handle and uses the [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) function to retrieve the desktop window handle, if necessary.</span></span> <span data-ttu-id="034d7-209">在計算新的位置之後，程式會使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函式來移動對話方塊，並指定 HWND \_ TOP 值，以確保對話方塊維持在主控視窗的最上方。</span><span class="sxs-lookup"><span data-stu-id="034d7-209">After calculating the new position, the procedure uses the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move the dialog box, specifying the HWND\_TOP value to ensure that the dialog box remains on top of the owner window.</span></span>

<span data-ttu-id="034d7-210">設定輸入焦點之前，程式會檢查預設輸入焦點的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="034d7-210">Before setting the input focus, the procedure checks the control identifier of the default input focus.</span></span> <span data-ttu-id="034d7-211">系統會在 *wParam* 參數中傳遞預設輸入焦點的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="034d7-211">The system passes the window handle of the default input focus in the *wParam* parameter.</span></span> <span data-ttu-id="034d7-212">[**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid)函式會傳回視窗控制碼所識別之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="034d7-212">The [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) function returns the identifier for the control identified by the window handle.</span></span> <span data-ttu-id="034d7-213">如果識別碼不符合正確的識別碼，則程式會使用 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數來設定輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="034d7-213">If the identifier does not match the correct identifier, the procedure uses the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function to set the input focus.</span></span> <span data-ttu-id="034d7-214">需要 [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) 函式才能取得所需控制項的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="034d7-214">The [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) function is required to retrieve the window handle of the desired control.</span></span>

## <a name="creating-a-template-in-memory"></a><span data-ttu-id="034d7-215">在記憶體中建立範本</span><span class="sxs-lookup"><span data-stu-id="034d7-215">Creating a Template in Memory</span></span>

<span data-ttu-id="034d7-216">應用程式有時會根據正在處理之資料的目前狀態，來調整或修改對話方塊的內容。</span><span class="sxs-lookup"><span data-stu-id="034d7-216">Applications sometimes adapt or modify the content of dialog boxes depending on the current state of the data being processed.</span></span> <span data-ttu-id="034d7-217">在這種情況下，提供所有可能的對話方塊範本做為應用程式可執行檔中的資源並不實用。</span><span class="sxs-lookup"><span data-stu-id="034d7-217">In such cases, it is not practical to provide all possible dialog box templates as resources in the application's executable file.</span></span> <span data-ttu-id="034d7-218">但在記憶體中建立範本可讓應用程式更有彈性地適應任何情況。</span><span class="sxs-lookup"><span data-stu-id="034d7-218">But creating templates in memory gives the application more flexibility to adapt to any circumstances.</span></span>

<span data-ttu-id="034d7-219">在下列範例中，應用程式會在記憶體中為包含 **[訊息] 和 [確定** ] 和 [說明] **按鈕的** 強制回應對話方塊建立範本。</span><span class="sxs-lookup"><span data-stu-id="034d7-219">In the following example, the application creates a template in memory for a modal dialog box that contains a message and **OK** and **Help** buttons.</span></span>

<span data-ttu-id="034d7-220">在對話方塊範本中，所有的字元字串（例如對話方塊和按鈕標題）都必須是 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="034d7-220">In a dialog template, all character strings, such as the dialog box and button titles, must be Unicode strings.</span></span> <span data-ttu-id="034d7-221">這個範例會使用 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) 函數來產生這些 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="034d7-221">This example uses the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings.</span></span>

<span data-ttu-id="034d7-222">對話方塊範本中的 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 結構必須對齊 **DWORD** 界限。</span><span class="sxs-lookup"><span data-stu-id="034d7-222">The [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures in a dialog template must be aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="034d7-223">為了對齊這些結構，此範例會使用接受輸入指標的 helper 常式，並傳回對齊 **DWORD** 界限的最接近指標。</span><span class="sxs-lookup"><span data-stu-id="034d7-223">To align these structures, this example uses a helper routine that takes an input pointer and returns the closest pointer that is aligned on a **DWORD** boundary.</span></span>


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 