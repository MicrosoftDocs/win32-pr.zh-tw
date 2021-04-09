---
title: 如何建立簡單的清單方塊
description: 本主題將示範如何從簡單列表框初始化和取出專案。
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024337"
---
# <a name="how-to-create-a-simple-list-box"></a><span data-ttu-id="d1b41-103">如何建立簡單的清單方塊</span><span class="sxs-lookup"><span data-stu-id="d1b41-103">How to Create a Simple List Box</span></span>

<span data-ttu-id="d1b41-104">本主題將示範如何從簡單列表框初始化和取出專案。</span><span class="sxs-lookup"><span data-stu-id="d1b41-104">This topic demonstrates how to initialize and retrieve items from a simple list box.</span></span>

<span data-ttu-id="d1b41-105">本主題中的 c + + 程式碼範例包含一個對話方塊程式，此程式會以體育團隊的玩家相關資訊填滿清單方塊。</span><span class="sxs-lookup"><span data-stu-id="d1b41-105">The C++ code example in this topic includes a dialog box procedure that fills a list box with information about players on a sports team.</span></span> <span data-ttu-id="d1b41-106">當使用者從清單中選取播放程式的名稱時，就會在對話方塊中顯示播放程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b41-106">When the user selects the name of a player from the list, information about the player is displayed in the dialog box.</span></span> <span data-ttu-id="d1b41-107">清單方塊的視窗樣式包含 [**磅 \_ 排序**](list-box-styles.md)，這會產生排序的專案清單。</span><span class="sxs-lookup"><span data-stu-id="d1b41-107">The window style for the list box includes [**LBS\_SORT**](list-box-styles.md), which results in a sorted list of items.</span></span> <span data-ttu-id="d1b41-108">下列螢幕擷取畫面顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d1b41-108">The following screen shot shows the dialog box.</span></span>

![對話方塊的螢幕擷取畫面，其中包含已加上標籤的清單方塊、有關選取清單方塊專案的文字，以及 [確定] 按鈕](images/lb-roster.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="d1b41-110">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d1b41-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d1b41-111">技術</span><span class="sxs-lookup"><span data-stu-id="d1b41-111">Technologies</span></span>

-   [<span data-ttu-id="d1b41-112">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d1b41-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d1b41-113">必要條件</span><span class="sxs-lookup"><span data-stu-id="d1b41-113">Prerequisites</span></span>

-   <span data-ttu-id="d1b41-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="d1b41-114">C/C++</span></span>
-   <span data-ttu-id="d1b41-115">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="d1b41-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d1b41-116">指示</span><span class="sxs-lookup"><span data-stu-id="d1b41-116">Instructions</span></span>


<span data-ttu-id="d1b41-117">應用程式必須執行下列清單方塊相關工作：</span><span class="sxs-lookup"><span data-stu-id="d1b41-117">The application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="d1b41-118">初始化清單方塊</span><span class="sxs-lookup"><span data-stu-id="d1b41-118">Initialize the list box</span></span>
-   <span data-ttu-id="d1b41-119">從清單方塊中取出使用者的選取範圍</span><span class="sxs-lookup"><span data-stu-id="d1b41-119">Retrieve the user's selection from the list box</span></span>

<span data-ttu-id="d1b41-120">在下列 c + + 程式碼範例中，播放程式的相關資訊會儲存在結構陣列中。</span><span class="sxs-lookup"><span data-stu-id="d1b41-120">In the following C++ code example, information about players is stored in an array of structures.</span></span> <span data-ttu-id="d1b41-121">在初始化期間，對話方塊程式會使用 [**LB \_ ADDSTRING**](lb-addstring.md) 訊息，將小組成員的名稱加入至清單方塊， (**IDC \_ LISTBOX \_ 範例**) 一次一個。</span><span class="sxs-lookup"><span data-stu-id="d1b41-121">During initialization, the dialog box procedure uses the [**LB\_ADDSTRING**](lb-addstring.md) message to add the names of team members to the list box (**IDC\_LISTBOX\_EXAMPLE**) one at a time.</span></span> <span data-ttu-id="d1b41-122">它也會使用 [**LB \_ SETITEMDATA**](lb-setitemdata.md) 訊息，將播放程式的陣列索引新增至清單方塊做為專案資料。</span><span class="sxs-lookup"><span data-stu-id="d1b41-122">It also uses the [**LB\_SETITEMDATA**](lb-setitemdata.md) message to add the array index of the player to the list box as item data.</span></span> <span data-ttu-id="d1b41-123">之後，當使用者從清單方塊中選取播放程式時，對話方塊程式會使用 [**LB \_ GETITEMDATA**](lb-getitemdata.md) 訊息來取出對應的陣列索引。</span><span class="sxs-lookup"><span data-stu-id="d1b41-123">Later, when the user selects a player from the list box, the dialog box procedure uses the [**LB\_GETITEMDATA**](lb-getitemdata.md) message to retrieve the corresponding array index.</span></span> <span data-ttu-id="d1b41-124">然後，它會使用陣列索引來從陣列中取出 player 資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b41-124">It then uses the array index to retrieve player information from the array.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="d1b41-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1b41-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1b41-126">清單方塊控制項參考</span><span class="sxs-lookup"><span data-stu-id="d1b41-126">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d1b41-127">關於清單方塊</span><span class="sxs-lookup"><span data-stu-id="d1b41-127">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="d1b41-128">使用清單方塊</span><span class="sxs-lookup"><span data-stu-id="d1b41-128">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




