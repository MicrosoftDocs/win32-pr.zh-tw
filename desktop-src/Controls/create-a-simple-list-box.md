---
title: 如何建立簡單的清單方塊
description: 本主題將示範如何從簡單列表框初始化和取出專案。
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a037bfbdb5232cd30d3e13fbc251c22c18c71a76398a351939602301a745d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063170"
---
# <a name="how-to-create-a-simple-list-box"></a>如何建立簡單的清單方塊

本主題將示範如何從簡單列表框初始化和取出專案。

本主題中的 c + + 程式碼範例包含一個對話方塊程式，此程式會以體育團隊的玩家相關資訊填滿清單方塊。 當使用者從清單中選取播放程式的名稱時，就會在對話方塊中顯示播放程式的相關資訊。 清單方塊的視窗樣式包含 [**磅 \_ 排序**](list-box-styles.md)，這會產生排序的專案清單。 下列螢幕擷取畫面顯示對話方塊。

![對話方塊的螢幕擷取畫面，其中包含已加上標籤的清單方塊、有關選取清單方塊專案的文字，以及 [確定] 按鈕](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示


應用程式必須執行下列清單方塊相關工作：

-   初始化清單方塊
-   從清單方塊中取出使用者的選取範圍

在下列 c + + 程式碼範例中，播放程式的相關資訊會儲存在結構陣列中。 在初始化期間，對話方塊程式會使用 [**LB \_ ADDSTRING**](lb-addstring.md) 訊息，將小組成員的名稱加入至清單方塊， (**IDC \_ LISTBOX \_ 範例**) 一次一個。 它也會使用 [**LB \_ SETITEMDATA**](lb-setitemdata.md) 訊息，將播放程式的陣列索引新增至清單方塊做為專案資料。 之後，當使用者從清單方塊中選取播放程式時，對話方塊程式會使用 [**LB \_ GETITEMDATA**](lb-getitemdata.md) 訊息來取出對應的陣列索引。 然後，它會使用陣列索引來從陣列中取出 player 資訊。



```C++
typedef struct 
{ 
    TCHAR achName[MAX_PATH]; 
    TCHAR achPosition[12]; 
    int nGamesPlayed; 
    int nGoalsScored; 
} Player; 

Player Roster[] = 
{ 
    {TEXT("Haas, Jonathan"), TEXT("Midfield"), 18, 4 }, 
    {TEXT("Pai, Jyothi"), TEXT("Forward"), 36, 12 }, 
    {TEXT("Hanif, Kerim"), TEXT("Back"), 26, 0 }, 
    {TEXT("Anderberg, Michael"), TEXT("Back"), 24, 2 }, 
    {TEXT("Jelitto, Jacek"), TEXT("Midfield"), 26, 3 }, 
    {TEXT("Raposo, Rui"), TEXT("Back"), 24, 3}, 
    {TEXT("Joseph, Brad"), TEXT("Forward"), 13, 3 }, 
    {TEXT("Bouchard, Thomas"), TEXT("Forward"), 28, 5 }, 
    {TEXT("Salmre, Ivo "), TEXT("Midfield"), 27, 7 }, 
    {TEXT("Camp, David"), TEXT("Midfield"), 22, 3 }, 
    {TEXT("Kohl, Franz"), TEXT("Goalkeeper"), 17, 0 }, 
}; 


INT_PTR CALLBACK ListBoxExampleProc(HWND hDlg, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_INITDIALOG:
        {
            // Add items to list. 
            HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE);  
            for (int i = 0; i < ARRAYSIZE(Roster); i++) 
            { 
                int pos = (int)SendMessage(hwndList, LB_ADDSTRING, 0, 
                    (LPARAM) Roster[i].achName); 
                // Set the array index of the player as item data.
                // This enables us to retrieve the item from the array
                // even after the items are sorted by the list box.
                SendMessage(hwndList, LB_SETITEMDATA, pos, (LPARAM) i); 
            } 
            // Set input focus to the list box.
            SetFocus(hwndList); 
            return TRUE;               
        } 

    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case IDOK:
        case IDCANCEL:
            EndDialog(hDlg, LOWORD(wParam));
            return TRUE;

        case IDC_LISTBOX_EXAMPLE:
            {
                switch (HIWORD(wParam)) 
                { 
                case LBN_SELCHANGE:
                    {
                        HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE); 

                        // Get selected index.
                        int lbItem = (int)SendMessage(hwndList, LB_GETCURSEL, 0, 0); 

                        // Get item data.
                        int i = (int)SendMessage(hwndList, LB_GETITEMDATA, lbItem, 0);

                        // Do something with the data from Roster[i]
                        TCHAR buff[MAX_PATH];
                        StringCbPrintf (buff, ARRAYSIZE(buff),  
                            TEXT("Position: %s\nGames played: %d\nGoals: %d"), 
                            Roster[i].achPosition, Roster[i].nGamesPlayed, 
                            Roster[i].nGoalsScored);

                        SetDlgItemText(hDlg, IDC_STATISTICS, buff); 
                        return TRUE; 
                    } 
                }
            }
            return TRUE;
        }
    }
    return FALSE;
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

 

 




