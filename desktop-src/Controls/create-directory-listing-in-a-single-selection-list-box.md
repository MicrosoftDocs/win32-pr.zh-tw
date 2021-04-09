---
title: 在清單方塊中建立目錄清單
description: 本主題將示範如何使用單一選取清單方塊來顯示和存取目錄的內容。
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03829990605271574a2030486ac5aba428867ec3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933722"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a>如何在單一選取清單方塊中建立目錄清單

本主題將示範如何使用單一選取清單方塊來顯示和存取目錄的內容。 [單一選取] 清單方塊是預設的清單方塊類型。 使用者一次只能從單一選取清單方塊中選取一個專案。

本主題中的 c + + 程式碼範例可讓使用者查看目前目錄中的檔案清單、從清單中選取檔案，並將它刪除。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


目錄清單應用程式必須執行下列清單方塊相關工作：

-   初始化清單方塊。
-   從清單方塊中取出使用者的選取專案。
-   刪除選取的檔案之後，請從清單方塊中移除檔案名。

在下列 c + + 程式碼範例中，對話方塊 \_ 程式會使用 [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) 函式來填滿目前目錄中所有檔案名稱的清單方塊，以初始化 (IDC FILELIST) 的單一挑選清單框。 當使用者選取檔案並選擇 [ **刪除** ] 按鈕時， [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) 函式會抓取所選取檔案的名稱。 程式碼會使用 [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) 函數來刪除檔案，並藉由傳送 [**LB \_ DELETESTRING**](lb-deletestring.md) 訊息來更新 [目錄] 清單方塊。



```C++
INT_PTR CALLBACK DlgDelFileProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int iLBItem; 
    int cStringsRemaining; 
    int iRet; 
    TCHAR achBuffer[MAX_PATH]; 
    TCHAR achTemp[MAX_PATH]; 
    BOOL fResult;     
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
 
           // Initialize the list box by filling it with files from 
           // the current directory. 
           pszCurDir = achBuffer; 
           GetCurrentDirectory(MAX_PATH, pszCurDir); 
           DlgDirList(hDlg, pszCurDir, IDC_FILELIST, IDS_PATHTOFILL, 0); 
           SetFocus(GetDlgItem(hDlg, IDC_FILELIST)); 
           return FALSE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
 
                    // When the user presses the DEL (IDOK) button, 
                    // first retrieve the selected file. 
                    pszFileToDelete = achBuffer; 
                    DlgDirSelectEx(hDlg, pszFileToDelete, MAX_PATH, 
                        IDC_FILELIST); 

                    // Make sure the user really wants to delete the file.
                    achTemp[MAX_PATH];
                    StringCbPrintf (achTemp, ARRAYSIZE(achTemp),  
                            TEXT("Are you sure you want to delete %s?"), 
                            pszFileToDelete);
                    iRet = MessageBox(hDlg, achTemp, L"Deleting Files", 
                        MB_YESNO | MB_ICONEXCLAMATION);
                    if (iRet == IDNO)
                        return TRUE;;

                    // Delete the file.
                    fResult = DeleteFile(pszFileToDelete); 
                    if (!fResult) 
                    { 
                        MessageBox(hDlg, L"Could not delete file.", 
                            NULL, MB_OK); 
                    } 
                    else // Remove the filename from the list box.
                    { 
                        // Get the selected item.
                        iLBItem = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_GETCURSEL, 0, 0); 
 
                        // Delete the selected item.
                        cStringsRemaining = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_DELETESTRING, iLBItem, 0); 
 
                        // If this is not the last item, set the selection to 
                        // the item immediately following the one just deleted.
                        // Otherwise, set the selection to the last item.
                         if (cStringsRemaining > iLBItem) 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, iLBItem, 0); 
                        } 
                        else 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, cStringsRemaining, 0); 
                        } 
                    } 
                    return TRUE; 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
                     EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    return FALSE; 
            } 
 
        default: 
            return FALSE; 
    } 
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[清單方塊控制項參考](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[關於清單方塊](about-list-boxes.md)
</dt> <dt>

[使用清單方塊](using-list-boxes.md)
</dt> </dl>

 

 