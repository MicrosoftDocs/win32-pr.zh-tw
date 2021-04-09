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
# <a name="how-to-create-a-multiple-selection-list-box"></a><span data-ttu-id="85824-103">如何建立 Multiple-Selection 清單方塊</span><span class="sxs-lookup"><span data-stu-id="85824-103">How to Create a Multiple-Selection List Box</span></span>

<span data-ttu-id="85824-104">本主題示範如何在多重選取清單方塊中顯示和存取目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="85824-104">This topic demonstrates how to display and access the contents of a directory in a multiple-selection list box.</span></span> <span data-ttu-id="85824-105">在多重選取清單方塊中，使用者可以一次選取一個以上的專案。</span><span class="sxs-lookup"><span data-stu-id="85824-105">In a multiple-selection list box, the user can select more than one item at a time.</span></span>

<span data-ttu-id="85824-106">本主題中的 c + + 程式碼範例可讓使用者查看目前目錄中的檔案清單、從清單中選取一組檔案，然後將它們刪除。</span><span class="sxs-lookup"><span data-stu-id="85824-106">The C++ code example in this topic enables a user to view a list of files in the current directory, select a group of files from the list, and delete them.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="85824-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="85824-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="85824-108">技術</span><span class="sxs-lookup"><span data-stu-id="85824-108">Technologies</span></span>

-   [<span data-ttu-id="85824-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="85824-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="85824-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="85824-110">Prerequisites</span></span>

-   <span data-ttu-id="85824-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="85824-111">C/C++</span></span>
-   <span data-ttu-id="85824-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="85824-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="85824-113">指示</span><span class="sxs-lookup"><span data-stu-id="85824-113">Instructions</span></span>


<span data-ttu-id="85824-114">目錄清單應用程式必須執行下列清單方塊相關工作：</span><span class="sxs-lookup"><span data-stu-id="85824-114">The directory listing application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="85824-115">初始化清單方塊。</span><span class="sxs-lookup"><span data-stu-id="85824-115">Initialize the list box.</span></span>
-   <span data-ttu-id="85824-116">從清單方塊中取出使用者的選取專案。</span><span class="sxs-lookup"><span data-stu-id="85824-116">Retrieve the user's selections from the list box.</span></span>
-   <span data-ttu-id="85824-117">刪除選取的檔案之後，請從清單方塊中移除檔案名。</span><span class="sxs-lookup"><span data-stu-id="85824-117">Remove the file names from the list box after the selected files have been deleted.</span></span>

<span data-ttu-id="85824-118">在下列 c + + 程式碼範例中，對話方塊 \_ 程式會使用 [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) 函式來填滿目前目錄中所有檔案名稱的清單方塊， (IDC FILELIST) 初始化多重選取清單方塊。</span><span class="sxs-lookup"><span data-stu-id="85824-118">In the following C++ code example, the dialog box procedure initializes the multiple-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span>

<span data-ttu-id="85824-119">當使用者選取一組檔案，並選擇 [ **刪除** ] 按鈕時，對話方塊程式會傳送 [**LB \_ GETSELCOUNT**](lb-getselcount.md) 訊息，以抓取選取的檔案數目和 [**lb \_ GETSELITEMS**](lb-getselitems.md) 訊息，以抓取選取清單方塊專案的陣列。</span><span class="sxs-lookup"><span data-stu-id="85824-119">When the user selects a group of files and chooses the **Delete** button, the dialog box procedure sends the [**LB\_GETSELCOUNT**](lb-getselcount.md) message, to retrieve the number of files selected, and the [**LB\_GETSELITEMS**](lb-getselitems.md) message, to retrieve an array of selected list box items.</span></span> <span data-ttu-id="85824-120">刪除檔案之後，對話程式會藉由傳送 [**LB \_ DELETESTRING**](lb-deletestring.md) 訊息，從清單方塊中移除對應的專案。</span><span class="sxs-lookup"><span data-stu-id="85824-120">After deleting a file, the dialog procedure removes the corresponding item from the list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="85824-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="85824-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85824-122">清單方塊控制項參考</span><span class="sxs-lookup"><span data-stu-id="85824-122">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="85824-123">關於清單方塊</span><span class="sxs-lookup"><span data-stu-id="85824-123">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="85824-124">使用清單方塊</span><span class="sxs-lookup"><span data-stu-id="85824-124">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




