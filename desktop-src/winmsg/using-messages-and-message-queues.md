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
# <a name="using-messages-and-message-queues"></a>使用訊息和訊息佇列

下列程式碼範例示範如何執行與 Windows 訊息和訊息佇列相關聯的下列工作。

-   [建立訊息迴圈](#creating-a-message-loop)
-   [檢查訊息佇列](#examining-a-message-queue)
-   [張貼訊息](#posting-a-message)
-   [傳送訊息](#sending-a-message)

## <a name="creating-a-message-loop"></a>建立訊息迴圈

系統不會自動為每個執行緒建立訊息佇列。 相反地，系統只會針對執行需要訊息佇列之作業的執行緒建立訊息佇列。 如果執行緒建立一或多個視窗，則必須提供訊息迴圈;此訊息迴圈會從執行緒的訊息佇列取出訊息，並將訊息分派至適當的視窗程式。

因為系統會將訊息導向至應用程式中的個別視窗，所以執行緒必須在啟動其訊息迴圈之前，至少建立一個視窗。 大部分的應用程式都包含一個建立 windows 的執行緒。 一般的應用程式會針對其主視窗註冊視窗類別、建立並顯示主視窗，然後啟動其訊息迴圈，全都在 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式中。

您可以使用 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 和 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 函數來建立訊息迴圈。 如果您的應用程式必須從使用者取得字元輸入，請在迴圈中包含 [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) 函數。 **TranslateMessage** 會將虛擬金鑰訊息轉譯為字元訊息。 下列範例顯示簡單 Windows 應用程式之 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式中的訊息迴圈。


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



下列範例顯示使用快速鍵之執行緒的訊息迴圈，並顯示非強制回應對話方塊。 當 [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) 或 [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) 傳回 **TRUE** (表示訊息已處理) ，則不會呼叫 [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) 和 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 。 這是因為 **TranslateAccelerator** 和 **IsDialogMessage** 會執行所有必要的訊息轉譯和分派。


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



## <a name="examining-a-message-queue"></a>檢查訊息佇列

有時候，應用程式需要從執行緒的訊息迴圈外部檢查執行緒訊息佇列的內容。 例如，如果應用程式的視窗程式執行冗長的繪圖作業，您可能會想要讓使用者能夠中斷作業。 除非您的應用程式會在操作滑鼠和鍵盤訊息時定期檢查訊息佇列，否則在作業完成之前，它將不會回應使用者輸入。 原因是，在視窗程式完成處理訊息之前，執行緒的訊息迴圈中的 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 函式不會傳回。

您可以使用 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函數，在冗長的作業期間檢查訊息佇列。 **PeekMessage** 類似于 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)函數;這兩者都會檢查訊息佇列中是否有符合篩選準則的訊息，然後將訊息複製到 [**訊息結構。**](/windows/win32/api/winuser/ns-winuser-msg) 這兩個函式的主要差異在於， **GetMessage** 不會傳回，直到符合篩選準則的訊息放置在佇列中，而 **PeekMessage** 則會立即傳回，無論訊息是否在佇列中。

下列範例示範如何使用 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 來檢查訊息佇列，以在長時間執行的滑鼠點擊和鍵盤輸入。


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



其他函式（包括 [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) 和 [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate)）也可讓您檢查執行緒訊息佇列的內容。 **GetQueueStatus** 會傳回旗標陣列，指出佇列中的訊息類型。使用它是探索佇列是否包含任何訊息的最快方式。 如果佇列包含滑鼠或鍵盤訊息， **GetInputState** 會傳回 **TRUE** 。 這兩個函式都可以用來判斷佇列是否包含需要處理的訊息。

## <a name="posting-a-message"></a>張貼訊息

您可以使用 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式，將訊息張貼到訊息佇列。 **PostMessage** 會將訊息放線上程訊息佇列的結尾，並立即傳回，而不需等待中的執行緒處理訊息。 函數的參數包含視窗控制碼、訊息識別碼和兩個訊息參數。 系統會將這些參數複製到 [**訊息結構，**](/windows/win32/api/winuser/ns-winuser-msg) 填滿結構的 **時間** 和 **pt** 成員，然後將結構放在訊息佇列中。

系統會使用與 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式一起傳遞的視窗控制碼，判斷哪個執行緒訊息佇列應該接收訊息。 如果控制碼是 **HWND \_ 最上層** 的，系統會將訊息張貼至所有最上層視窗的執行緒訊息佇列。

您可以使用 [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) 函式，將訊息張貼至特定的執行緒訊息佇列。 **PostThreadMessage** 與 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)類似，但第一個參數是執行緒識別碼而非視窗控制碼。 您可以藉由呼叫 [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) 函數來取出執行緒識別碼。

使用 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) 函式來結束訊息迴圈。 **PostQuitMessage** 會將 [**WM \_**](wm-quit.md) 結束訊息張貼至目前執行中的執行緒。 執行緒的訊息迴圈會終止，並在遇到 **WM \_** 結束訊息時將控制權傳回給系統。 應用程式通常會呼叫 **PostQuitMessage** 來回應 [**WM \_ 摧毀**](wm-destroy.md) 訊息，如下列範例所示。


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a>傳送訊息

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)函式是用來將訊息直接傳送至視窗程式。 **SendMessage** 會呼叫視窗程式，並等候該程式處理訊息並傳回結果。

訊息可以傳送至系統中的任何視窗;所有必要的都是視窗控制碼。 系統會使用此控制碼來判斷應該接收訊息的視窗程式。

在處理可能已經從其他執行緒傳送的訊息之前，視窗程式應該先呼叫 [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) 函式。 如果此函式傳回 **TRUE**，則視窗程式應該在任何導致執行緒產生控制權的函式之前呼叫 [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) ，如下列範例所示。


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



您可以將數個訊息傳送至對話方塊中的控制項。 這些控制訊息會設定控制項的外觀、行為和內容，或取得控制項的相關資訊。 例如， [**CB \_ ADDSTRING**](../controls/cb-addstring.md) 訊息可以將字串新增至下拉式方塊，而 [**BM \_ SETCHECK**](../controls/bm-setcheck.md) 訊息可以設定核取方塊或選項按鈕的核取狀態。

您可以使用 [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) 函式來傳送訊息給控制項，並指定控制項的識別碼，以及包含控制項之對話方塊視窗的控制碼。 下列範例取自對話方塊程式，會將字串從下拉式方塊的編輯控制項複製到其清單方塊中。 此範例會使用 **SendDlgItemMessage** 將 [**CB \_ ADDSTRING**](../controls/cb-addstring.md) 訊息傳送至下拉式方塊。


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



 

 
