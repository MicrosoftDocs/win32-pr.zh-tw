---
title: 如何建立單一行編輯控制項
description: 本主題將示範如何建立包含單行編輯控制項的對話方塊。
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5d39a4c9fbc806de6ca151606e770eb0cea9b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024339"
---
# <a name="how-to-create-a-single-line-edit-control"></a>如何建立單一行編輯控制項

本主題將示範如何建立包含單行編輯控制項的對話方塊。

單行編輯控制項具有 [**ES \_ 密碼**](edit-control-styles.md) 樣式。 依預設，使用此樣式編輯控制項會針對使用者輸入的每個字元顯示星號。 不過，此範例會使用 [**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md) 訊息，將預設字元從星號變更為加號 (+) 。 下列螢幕擷取畫面顯示使用者輸入密碼之後的對話方塊。

![對話方塊的螢幕擷取畫面，其中包含用於輸入密碼的編輯控制項](images/passworddlg.png)

> [!Note]  
> Comctl32.dll 第6版無法轉散發。 若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>步驟1：建立密碼對話方塊的實例。

下列 c + + 程式碼範例會使用對話方塊函數來建立強制回應對話方塊。 對話方塊範本的 **IDD \_ 密碼** 會以參數形式傳遞。 它會定義 [密碼] 對話方塊的視窗樣式、按鈕和維度等等。


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>步驟2：初始化對話方塊並處理使用者輸入。

下列範例中的視窗程式會初始化密碼對話方塊，並處理通知訊息和使用者輸入。

在初始化期間，視窗程式會將預設密碼字元變更為 **+** 正負號，並將預設的按鈕設定為 [ **取消**]。

在使用者輸入處理期間，當使用者在編輯控制項中輸入文字時，視窗程式會將預設的 [推送] 按鈕從 [ **取消** ] 變更為 **[確定]** 。 如果使用者按下 [ **確定]** 按鈕，則視窗程式會使用 [**Em \_ LINELENGTH**](em-linelength.md) 和 [**em \_ GETLINE**](em-getline.md) 訊息來取出文字。



```C++
INT_PTR CALLBACK PasswordProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    TCHAR lpszPassword[16]; 
    WORD cchPassword; 

    switch (message) 
    { 
        case WM_INITDIALOG: 
            // Set password character to a plus sign (+) 
            SendDlgItemMessage(hDlg, 
                               IDE_PASSWORDEDIT, 
                               EM_SETPASSWORDCHAR, 
                               (WPARAM) '+', 
                               (LPARAM) 0); 

            // Set the default push button to "Cancel." 
            SendMessage(hDlg, 
                        DM_SETDEFID, 
                        (WPARAM) IDCANCEL, 
                        (LPARAM) 0); 

            return TRUE; 

        case WM_COMMAND: 
            // Set the default push button to "OK" when the user enters text. 
            if(HIWORD (wParam) == EN_CHANGE && 
                                LOWORD(wParam) == IDE_PASSWORDEDIT) 
            {
                SendMessage(hDlg, 
                            DM_SETDEFID, 
                            (WPARAM) IDOK, 
                            (LPARAM) 0); 
            }
            switch(wParam) 
            { 
                case IDOK: 
                    // Get number of characters. 
                    cchPassword = (WORD) SendDlgItemMessage(hDlg, 
                                                            IDE_PASSWORDEDIT, 
                                                            EM_LINELENGTH, 
                                                            (WPARAM) 0, 
                                                            (LPARAM) 0); 
                    if (cchPassword >= 16) 
                    { 
                        MessageBox(hDlg, 
                                   L"Too many characters.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 
                    else if (cchPassword == 0) 
                    { 
                        MessageBox(hDlg, 
                                   L"No characters entered.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 

                    // Put the number of characters into first word of buffer. 
                    *((LPWORD)lpszPassword) = cchPassword; 

                    // Get the characters. 
                    SendDlgItemMessage(hDlg, 
                                       IDE_PASSWORDEDIT, 
                                       EM_GETLINE, 
                                       (WPARAM) 0,       // line 0 
                                       (LPARAM) lpszPassword); 

                    // Null-terminate the string. 
                    lpszPassword[cchPassword] = 0; 

                    MessageBox(hDlg, 
                               lpszPassword, 
                               L"Did it work?", 
                               MB_OK); 

                    // Call a local password-parsing function. 
                    ParsePassword(lpszPassword); 

                    EndDialog(hDlg, TRUE); 
                    return TRUE; 

                case IDCANCEL: 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
            } 
            return 0; 
    } 
    return FALSE; 
    
    UNREFERENCED_PARAMETER(lParam); 
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於編輯控制項](about-edit-controls.md)
</dt> <dt>

[編輯控制項參考](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[使用編輯控制項](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[編輯控制項](edit-controls.md)
</dt> </dl>

 

 