---
title: 使用對話方塊
description: 您可以使用對話方塊來顯示資訊，並提示使用者輸入。
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Windows消費者介面、視窗化
- Windows消費者介面，對話方塊
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
ms.openlocfilehash: 32ec5e97060697388224ac92f60b6043a188d4259520aaf151fb188c43f6bb64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720789"
---
# <a name="using-dialog-boxes"></a>使用對話方塊

您可以使用對話方塊來顯示資訊，並提示使用者輸入。 您的應用程式會載入並初始化對話方塊、處理使用者輸入，並在使用者完成工作時終結對話方塊。 處理對話方塊的處理常式會根據對話方塊為強制回應或非模式而有所不同。 強制回應對話方塊需要使用者先關閉對話方塊，再啟用應用程式中的另一個視窗。 不過，使用者可以在不同的應用程式中啟動 windows。 非強制回應對話方塊不需要使用者立即回應。 它類似于包含控制項的主視窗。

下列各節將討論如何使用這兩種類型的對話方塊。

-   [顯示訊息方塊](#displaying-a-message-box)
-   [建立強制回應對話方塊](#creating-a-modal-dialog-box)
-   [建立非強制回應對話方塊](#creating-a-modeless-dialog-box)
-   [初始化對話方塊](#initializing-a-dialog-box)
-   [在記憶體中建立範本](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a>顯示訊息方塊

強制回應對話方塊最簡單的形式就是訊息方塊。 大部分的應用程式會使用訊息方塊來警告使用者的錯誤，並提示您如何在發生錯誤之後繼續進行。 您可以使用 [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) 或 [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) 函式來建立訊息方塊，並指定訊息以及要顯示的按鈕數目和類型。 系統會建立強制回應對話方塊，並提供自己的對話方塊範本和程式。 在使用者關閉訊息方塊之後， **MessageBox** 或 **MessageBoxEx** 會傳回值，指出使用者選擇關閉訊息方塊的按鈕。

在下列範例中，應用程式會顯示訊息方塊，以在發生錯誤狀況時提示使用者輸入動作。 訊息方塊會顯示描述錯誤狀況的訊息，以及如何解決此問題。 **MB \_ YESNO** 樣式會指示 [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox)提供兩個按鈕，讓使用者可以選擇如何繼續：


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



下圖顯示上述程式碼範例的輸出：

![訊息方塊](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a>建立強制回應對話方塊

您可以使用 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 函數來建立強制回應對話方塊。 您必須指定對話方塊範本資源的識別碼或名稱，以及對話方塊程式的指標。 **對話方塊** 函式會載入範本、顯示對話方塊，並處理所有使用者輸入，直到使用者關閉對話方塊為止。

在下列範例中，當使用者按一下應用程式功能表中的 [ **刪除專案** ] 時，應用程式會顯示模式對話方塊。 對話方塊中包含編輯控制項 (使用者在其中輸入專案的名稱) 和 **[確定] 和 [** **取消** ] 按鈕。 這些控制項的控制項識別碼分別為 ID \_ ：//IDOK 和 IDCANCEL。

此範例的第一個部分是由建立強制回應對話方塊的語句所組成。 這些語句（在應用程式主視窗的視窗程式中）會在系統收到具有 IDM DELETEITEM 功能表識別碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息時建立對話方塊 \_ 。 範例的第二個部分是對話方塊程式，它會抓取編輯控制項的內容，並在收到 **WM \_ 命令** 訊息時關閉對話方塊。

下列語句會建立強制回應對話方塊。 對話方塊範本是應用程式可執行檔中的資源，且資源識別碼為 d \_ DELETEITEM。


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



在此範例中，應用程式會將其主視窗指定為對話方塊的擁有者視窗。 當系統一開始顯示對話方塊時，它的位置是相對於擁有者視窗工作區的左上角。 應用程式會使用來自 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 的傳回值，以判斷是否要繼續操作或取消作業。 下列語句會定義對話方塊程式。


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



在此範例中，程式會使用 [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) ，從 ID 的使用者識別碼所識別的編輯控制項中取出目前的文字 \_ 。 程式接著會呼叫 [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) 函式，將對話方塊的傳回值設定為 IDOK 或 IDCANCEL，視收到的訊息而定，然後開始關閉對話方塊的進程。 IDOK 和 IDCANCEL 識別碼會對應至 [ **確定]** 和 [ **取消** ] 按鈕。 在程式呼叫 **EndDialog** 之後，系統會將其他訊息傳送至程式以終結對話方塊，並將對話方塊的傳回值傳回給建立對話方塊的函式。

## <a name="creating-a-modeless-dialog-box"></a>建立非強制回應對話方塊

您可以使用 [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) 函式來建立非強制回應對話方塊，指定對話方塊範本資源的識別碼或名稱，以及對話方塊程式的指標。 **CreateDialog** 會載入範本、建立對話方塊，並選擇性地顯示此對話方塊。 您的應用程式會負責將使用者輸入訊息取出並分派至對話方塊程式。

在下列範例中，當使用者按一下應用程式功能表中的 [ **移至** ] 時，應用程式會顯示非強制回應對話方塊（如果尚未顯示）。 對話方塊中包含編輯控制項、核取方塊和 **[確定] 和 [** **取消** ] 按鈕。 對話方塊範本是應用程式可執行檔中的資源，且資源識別碼為 DLG \_ GOTO。 使用者在編輯控制項中輸入行號，並核取核取方塊，以指定行號相對於目前的行號。 控制項識別碼是識別碼 \_ 行、識別碼 \_ ABSREL、IDOK 和 IDCANCEL。

範例第一個部分中的語句會建立非強制回應對話方塊。 這些語句（在應用程式主視窗的視窗程式中）會在視窗程式收到具有 IDM GOTO 功能表識別碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息時建立對話方塊 \_ ，但只有在全域變數尚未包含有效的控制碼時。 此範例的第二個部分是應用程式的主要訊息迴圈。 迴圈包含 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函式，以確保使用者可以在這個非強制回應對話方塊中使用對話方塊鍵盤介面。 此範例的第三個部分是對話方塊程式。 當使用者按一下 [ **確定]** 按鈕時，此程式會抓取編輯控制項的內容，並選取核取方塊。 當使用者按一下 [ **取消** ] 按鈕時，此程式會終結對話方塊。


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



在上述語句中， [](/windows/desktop/api/Winuser/nf-winuser-createdialoga)只有在不 `hwndGoto` 包含有效的視窗控制碼時，才會呼叫 CreateDialog。 這可確保應用程式不會同時顯示兩個對話方塊。 若要支援這種檢查方法，當它終結對話方塊時，對話程式必須設定為 **Null** 。

應用程式的訊息迴圈是由下列語句所組成。


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



迴圈會將視窗控制碼的有效性檢查至對話方塊，而且只有在控制碼有效時，才會呼叫 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函數。 **IsDialogMessage** 只會處理屬於對話方塊的訊息。 否則，它會傳回 **FALSE** ，而迴圈會將訊息分派至適當的視窗。

下列語句會定義對話方塊程式。


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



在上述語句中，此程式會處理 [**wm \_ INITDIALOG**](wm-initdialog.md) 和 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。 在進行 **WM \_ INITDIALOG** 處理時，程式會將全域變數的目前值傳遞至 [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx)，以初始化此核取方塊。 然後，此程式會傳回 **TRUE** ，以指示系統設定預設的輸入焦點。

在 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 處理過程中，只有當使用者按一下 [ **取消** ] 按鈕（也就是具有 IDCANCEL 識別碼的按鈕）時，程式才會關閉對話方塊。 程式必須呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 來關閉非強制回應對話方塊。 請注意，此程式也會將變數設為 **Null** ，以確保相依于這個變數的其他語句會正確運作。

如果使用者按一下 [ **確定]** 按鈕，程式就會抓取該核取方塊的目前狀態，並將它指派給 **fRelative** 變數。 然後，它會使用變數來從編輯控制項取出行號。 [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) 會將編輯控制項中的文字轉譯為整數。 **FRelative** 的值會決定函式是否會將數位解讀為帶正負號或不帶正負號的值。 如果編輯控制項文字不是有效的數位， **GetDlgItemInt** 會將 **fError** 變數的值設定為非零。 此程式會檢查此值，以判斷是否要顯示錯誤訊息或執行工作。 發生錯誤時，對話方塊程式會將訊息傳送至編輯控制項，並將它導向以選取控制項中的文字，讓使用者可以輕鬆地加以取代。 如果 **GetDlgItemInt** 未傳回錯誤，則程式可以執行要求的工作本身，或將訊息傳送至主控視窗，將它導向以執行作業。

## <a name="initializing-a-dialog-box"></a>初始化對話方塊

您可以在處理 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息時，初始化對話方塊及其內容。 最常見的工作是將控制項初始化，以反映目前的對話方塊設定。 另一項常見的工作是在螢幕上或其擁有者視窗內置中對話方塊。 某些對話方塊的實用工作是將輸入焦點設定為指定的控制項，而不接受預設的輸入焦點。

在下列範例中，對話方塊程式會將對話方塊置中，並在處理 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息時設定輸入焦點。 為了將對話方塊置中，此程式會抓取對話方塊和主控視窗的視窗矩形，並計算對話方塊的新位置。 若要設定輸入焦點，程式會檢查 *wParam* 參數，以判斷預設輸入焦點的識別碼。


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



在上述語句中，此程式會使用 [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) 函式，將擁有者視窗控制碼取出至對話方塊。 函式會將擁有者視窗控制碼傳回至對話方塊，並將父視窗控制碼傳回至子視窗。 因為應用程式可以建立沒有擁有者的對話方塊，程式會檢查傳回的控制碼，並視需要使用 [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) 函式來取出桌面視窗控制碼。 在計算新的位置之後，程式會使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函式來移動對話方塊，並指定 HWND \_ TOP 值，以確保對話方塊維持在主控視窗的最上方。

設定輸入焦點之前，程式會檢查預設輸入焦點的控制項識別碼。 系統會在 *wParam* 參數中傳遞預設輸入焦點的視窗控制碼。 [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid)函式會傳回視窗控制碼所識別之控制項的識別碼。 如果識別碼不符合正確的識別碼，則程式會使用 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數來設定輸入焦點。 需要 [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) 函式才能取得所需控制項的視窗控制碼。

## <a name="creating-a-template-in-memory"></a>在記憶體中建立範本

應用程式有時會根據正在處理之資料的目前狀態，來調整或修改對話方塊的內容。 在這種情況下，提供所有可能的對話方塊範本做為應用程式可執行檔中的資源並不實用。 但在記憶體中建立範本可讓應用程式更有彈性地適應任何情況。

在下列範例中，應用程式會在記憶體中為包含 **[訊息] 和 [確定** ] 和 [說明] **按鈕的** 強制回應對話方塊建立範本。

在對話方塊範本中，所有的字元字串（例如對話方塊和按鈕標題）都必須是 Unicode 字串。 這個範例會使用 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) 函數來產生這些 Unicode 字串。

對話方塊範本中的 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 結構必須對齊 **DWORD** 界限。 為了對齊這些結構，此範例會使用接受輸入指標的 helper 常式，並傳回對齊 **DWORD** 界限的最接近指標。


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



 

 