---
title: 如何建立 Multiple-Selection 清單方塊
description: 本主題示範如何在多重選取清單方塊中顯示和存取目錄的內容。
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd47b1d582d53a66bc77284927aef4230043e92
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024343"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a>如何建立 Multiple-Selection 清單方塊

本主題示範如何在多重選取清單方塊中顯示和存取目錄的內容。 在多重選取清單方塊中，使用者可以一次選取一個以上的專案。

本主題中的 c + + 程式碼範例可讓使用者查看目前目錄中的檔案清單、從清單中選取一組檔案，然後將它們刪除。

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

在下列 c + + 程式碼範例中，對話方塊 \_ 程式會使用 [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) 函式來填滿目前目錄中所有檔案名稱的清單方塊， (IDC FILELIST) 初始化多重選取清單方塊。

當使用者選取一組檔案，並選擇 [ **刪除** ] 按鈕時，對話方塊程式會傳送 [**LB \_ GETSELCOUNT**](lb-getselcount.md) 訊息，以抓取選取的檔案數目和 [**lb \_ GETSELITEMS**](lb-getselitems.md) 訊息，以抓取選取清單方塊專案的陣列。 刪除檔案之後，對話程式會藉由傳送 [**LB \_ DELETESTRING**](lb-deletestring.md) 訊息，從清單方塊中移除對應的專案。



```C++
#define BIGBUFF 8192 
 
INT_PTR CALLBACK DlgDelFilesProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int cSelItems; 
    int cSelItemsInBuffer; 
    TCHAR achBuffer[MAX_PATH]; 
    int aSelItems[BIGBUFF]; 
    int i; 
    BOOL fResult; 
    HWND hListBox;
    int iRet;
 
    switch (message) { 
 
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
                    // first retrieve the list of selected files. 
                    pszFileToDelete = achBuffer; 
                    hListBox = GetDlgItem(hDlg, IDC_FILELIST); 
                    cSelItems = SendMessage(hListBox, 
                            LB_GETSELCOUNT, 0, 0); 
 
                    cSelItemsInBuffer = SendMessage(hListBox, 
                            LB_GETSELITEMS, 512, (LPARAM) aSelItems); 
 
                    if (cSelItems > cSelItemsInBuffer) 
                    { 
                        MessageBox(hDlg, L"Too many items selected.", 
                                NULL, MB_OK); 
                    } 
                    else 
                    { 

                        // Make sure the user really wants to delete the files.
                        iRet = MessageBox(hDlg, 
                            L"Are you sure you want to delete these files?", 
                            L"Deleting Files", MB_YESNO | MB_ICONEXCLAMATION);
                        if (iRet == IDNO)
                            return TRUE;

                        // Go through the list backward because after deleting
                        // an item the indices change for every subsequent 
                        // item. By going backward, the indices are never 
                        // invalidated. 
                        for (i = cSelItemsInBuffer - 1; i >= 0; i--) 
                        { 
                            SendMessage(hListBox, LB_GETTEXT, 
                                        aSelItems[i], 
                                        (LPARAM) pszFileToDelete); 
 
                            fResult = DeleteFile(pszFileToDelete); 
                            if (!fResult) 
                            {                     
                                MessageBox(hDlg, L"Could not delete file.", 
                                    NULL, MB_OK);     
                            } 
                            else 
                            { 
                                SendMessage(hListBox, LB_DELETESTRING, 
                                        aSelItems[i], 0); 
                            } 
                        } 
                        SendMessage(hListBox, LB_SETCARETINDEX, 0, 0); 
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

 

 




