---
title: 如何新增 List-View 專案與子專案
description: 本主題示範如何將專案和子專案加入至清單視圖控制項。
ms.assetid: B7E204DC-FD08-4639-985D-1459A1AC0ED6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b3d20008edc10fda810261427507c77e9cfe34
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104093523"
---
# <a name="how-to-add-list-view-items-and-subitems"></a><span data-ttu-id="264a9-103">如何新增 List-View 專案與子專案</span><span class="sxs-lookup"><span data-stu-id="264a9-103">How to Add List-View Items and Subitems</span></span>

<span data-ttu-id="264a9-104">本主題示範如何將專案和子專案加入至清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="264a9-104">This topic demonstrates how to add items and subitems to a list-view control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="264a9-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="264a9-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="264a9-106">技術</span><span class="sxs-lookup"><span data-stu-id="264a9-106">Technologies</span></span>

-   [<span data-ttu-id="264a9-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="264a9-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="264a9-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="264a9-108">Prerequisites</span></span>

-   <span data-ttu-id="264a9-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="264a9-109">C/C++</span></span>
-   <span data-ttu-id="264a9-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="264a9-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="264a9-111">指示</span><span class="sxs-lookup"><span data-stu-id="264a9-111">Instructions</span></span>


<span data-ttu-id="264a9-112">若要將專案加入至清單視圖控制項，應用程式必須先定義 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構，然後再傳送 [**LVM \_ INSERTITEM**](lvm-insertitem.md) 訊息，指定 **LVITEM** 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="264a9-112">To add an item to a list-view control, an application must first define an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure and then send an [**LVM\_INSERTITEM**](lvm-insertitem.md) message, specifying the address of the **LVITEM** structure.</span></span> <span data-ttu-id="264a9-113">如果應用程式使用報表檢視，則必須提供子必須文字。</span><span class="sxs-lookup"><span data-stu-id="264a9-113">If an application uses report view, subitem text must be provided.</span></span>

<span data-ttu-id="264a9-114">下列 c + + 程式碼範例會填入 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構，並使用 [**LVM \_ INSERTITEM**](lvm-insertitem.md) 訊息或對應的宏 [**ListView \_ INSERTITEM**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem)來加入清單視圖專案。</span><span class="sxs-lookup"><span data-stu-id="264a9-114">The following C++ code example fills an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure and adds the list-view items by using the [**LVM\_INSERTITEM**](lvm-insertitem.md) message or the corresponding macro [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem).</span></span> <span data-ttu-id="264a9-115">由於應用程式會儲存自己的文字，因此它會 \_ 針對 **LVITEM** 結構的 **pszText** 成員指定 LPSTR TEXTCALLBACK 值。</span><span class="sxs-lookup"><span data-stu-id="264a9-115">Because the application saves its own text, it specifies the LPSTR\_TEXTCALLBACK value for the **pszText** member of the **LVITEM** structure.</span></span> <span data-ttu-id="264a9-116">指定 LPSTR \_ TEXTCALLBACK 值會讓控制項在需要顯示專案時，將 [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) 通知程式碼傳送至其擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="264a9-116">Specifying the LPSTR\_TEXTCALLBACK value causes the control to send an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code to its owner window whenever it needs to display an item.</span></span>


```C++
// InsertListViewItems: Inserts items into a list view. 
// hWndListView:        Handle to the list-view control.
// cItems:              Number of items to insert.
// Returns TRUE if successful, and FALSE otherwise.
BOOL InsertListViewItems(HWND hWndListView, int cItems)
{
    LVITEM lvI;

    // Initialize LVITEM members that are common to all items.
    lvI.pszText   = LPSTR_TEXTCALLBACK; // Sends an LVN_GETDISPINFO message.
    lvI.mask      = LVIF_TEXT | LVIF_IMAGE |LVIF_STATE;
    lvI.stateMask = 0;
    lvI.iSubItem  = 0;
    lvI.state     = 0;

    // Initialize LVITEM members that are different for each item.
    for (int index = 0; index < cItems; index++)
    {
        lvI.iItem  = index;
        lvI.iImage = index;
    
        // Insert items into the list.
        if (ListView_InsertItem(hWndListView, &lvI) == -1)
            return FALSE;
    }

    return TRUE;
}

// HandleWM_NOTIFY - Handles the LVN_GETDISPINFO notification code that is 
//         sent in a WM_NOTIFY to the list view parent window. The function 
//        provides display strings for list view items and subitems.
//
// lParam - The LPARAM parameter passed with the WM_NOTIFY message.
// rgPetInfo - A global array of structures, defined as follows:
//         struct PETINFO
//        {
//            TCHAR szKind[10];
//            TCHAR szBreed[50];
//            TCHAR szPrice[20];
//        };
//
//        PETINFO rgPetInfo[ ] = 
//        {
//            {TEXT("Dog"),  TEXT("Poodle"),     TEXT("$300.00")},
//            {TEXT("Cat"),  TEXT("Siamese"),    TEXT("$100.00")},
//            {TEXT("Fish"), TEXT("Angel Fish"), TEXT("$10.00")},
//            {TEXT("Bird"), TEXT("Parakeet"),   TEXT("$5.00")},
//            {TEXT("Toad"), TEXT("Woodhouse"),  TEXT("$0.25")},
//        };
//
void HandleWM_NOTIFY(LPARAM lParam)
{
    NMLVDISPINFO* plvdi;

    switch (((LPNMHDR) lParam)->code)
    {
        case LVN_GETDISPINFO:

            plvdi = (NMLVDISPINFO*)lParam;

            switch (plvdi->item.iSubItem)
            {
                case 0:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szKind;
                    break;
                      
                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;
                
                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;
                
                default:
                    break;
            }

        break;

    }
    // NOTE: In addition to setting pszText to point to the item text, you could 
    // copy the item text into pszText using StringCchCopy. For example:
    //
    // StringCchCopy(plvdi->item.pszText, 
    //                         plvdi->item.cchTextMax, 
    //                         rgPetInfo[plvdi->item.iItem].szKind);

    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="264a9-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="264a9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="264a9-118">清單視圖控制項參考</span><span class="sxs-lookup"><span data-stu-id="264a9-118">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="264a9-119">關於 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="264a9-119">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="264a9-120">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="264a9-120">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




