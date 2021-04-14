---
title: 如何新增 Tree-View 專案
description: 您可以藉由將 TVM INSERTITEM 訊息傳送至控制項，將專案加入至樹狀檢視控制項 \_ 。
ms.assetid: CD6376F4-8B1A-489D-8538-6C1620E98F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7da0846b57f422de83984b197df0770286882
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374578"
---
# <a name="how-to-add-tree-view-items"></a><span data-ttu-id="a83ea-103">如何新增 Tree-View 專案</span><span class="sxs-lookup"><span data-stu-id="a83ea-103">How to Add Tree-View Items</span></span>

<span data-ttu-id="a83ea-104">您可以藉由將 [**TVM \_ INSERTITEM**](tvm-insertitem.md) 訊息傳送至控制項，將專案加入至樹狀檢視控制項。</span><span class="sxs-lookup"><span data-stu-id="a83ea-104">You add an item to a tree-view control by sending the [**TVM\_INSERTITEM**](tvm-insertitem.md) message to the control.</span></span> <span data-ttu-id="a83ea-105">訊息包含 [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) 結構的位址，指定父專案、插入新專案之後的專案，以及定義專案屬性的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) 結構。</span><span class="sxs-lookup"><span data-stu-id="a83ea-105">The message includes the address of a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure, specifying the parent item, the item after which the new item is inserted, and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that defines the attributes of the item.</span></span> <span data-ttu-id="a83ea-106">這些屬性包括專案的標籤、其選取的和 nonselected 的影像，以及32位的應用程式定義值。</span><span class="sxs-lookup"><span data-stu-id="a83ea-106">The attributes include the item's label, its selected and nonselected images, and a 32-bit application-defined value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a83ea-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="a83ea-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a83ea-108">技術</span><span class="sxs-lookup"><span data-stu-id="a83ea-108">Technologies</span></span>

-   [<span data-ttu-id="a83ea-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="a83ea-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a83ea-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="a83ea-110">Prerequisites</span></span>

-   <span data-ttu-id="a83ea-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="a83ea-111">C/C++</span></span>
-   <span data-ttu-id="a83ea-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="a83ea-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a83ea-113">指示</span><span class="sxs-lookup"><span data-stu-id="a83ea-113">Instructions</span></span>

### <a name="add-items-to-the-tree-view"></a><span data-ttu-id="a83ea-114">將專案新增至 Tree-View</span><span class="sxs-lookup"><span data-stu-id="a83ea-114">Add Items to the Tree-View</span></span>

<span data-ttu-id="a83ea-115">本節中的範例會示範如何根據應用程式定義陣列中提供的檔標題資訊來建立目錄。</span><span class="sxs-lookup"><span data-stu-id="a83ea-115">The example in this section demonstrates how to create a table of contents based on document heading information that is provided in an application-defined array.</span></span> <span data-ttu-id="a83ea-116">每個陣列元素都包含一個標頭字串，以及一個指出標題層級的整數。</span><span class="sxs-lookup"><span data-stu-id="a83ea-116">Each array element consists of a heading string and an integer that indicates the heading level.</span></span> <span data-ttu-id="a83ea-117">此範例支援三個標題層級 (1、2和 3) 。</span><span class="sxs-lookup"><span data-stu-id="a83ea-117">The example supports three heading levels (1, 2, and 3).</span></span>

<span data-ttu-id="a83ea-118">此範例包含兩個函數。</span><span class="sxs-lookup"><span data-stu-id="a83ea-118">The example includes two functions.</span></span> <span data-ttu-id="a83ea-119">第一個函式會將每個標題和伴隨的標題層級解壓縮，然後將它們傳遞給第二個函式。</span><span class="sxs-lookup"><span data-stu-id="a83ea-119">The first function extracts each heading and accompanying heading level and then passes them to the second function.</span></span>

<span data-ttu-id="a83ea-120">第二個函式會將專案加入至樹狀檢視控制項。</span><span class="sxs-lookup"><span data-stu-id="a83ea-120">The second function adds an item to a tree-view control.</span></span> <span data-ttu-id="a83ea-121">它使用標題文字作為專案的標籤，並使用標題層級來決定新專案的父專案。</span><span class="sxs-lookup"><span data-stu-id="a83ea-121">It uses the heading text as the item's label, and it uses the heading level to determine the parent item for the new item.</span></span> <span data-ttu-id="a83ea-122">層級的一個標題會加入至樹狀檢視控制項的根目錄中，層級二標題會加入為前一個層級專案的子專案，依此類推。</span><span class="sxs-lookup"><span data-stu-id="a83ea-122">A level one heading is added to the root of the tree-view control, a level two heading is added as a child item of the previous level one item, and so on.</span></span> <span data-ttu-id="a83ea-123">函數會根據專案是否有子專案，將影像指派給專案。</span><span class="sxs-lookup"><span data-stu-id="a83ea-123">The function assigns an image to an item based on whether it has child items.</span></span> <span data-ttu-id="a83ea-124">如果專案有子專案，則會取得代表已關閉資料夾的影像。</span><span class="sxs-lookup"><span data-stu-id="a83ea-124">If an item has child items, it gets an image that represents a closed folder.</span></span> <span data-ttu-id="a83ea-125">否則，它會取得代表檔的影像。</span><span class="sxs-lookup"><span data-stu-id="a83ea-125">Otherwise, it gets an image that represents a document.</span></span> <span data-ttu-id="a83ea-126">專案會針對選取的和 nonselected 狀態使用相同的影像。</span><span class="sxs-lookup"><span data-stu-id="a83ea-126">An item uses the same image for both the selected and nonselected states.</span></span>


```C++
// Adds items to a tree-view control. 
// Returns the handle to the newly added item. 
// hwndTV - handle to the tree-view control. 
// lpszItem - text of the item to add. 
// nLevel - level at which to add the item. 
//
// g_nClosed, and g_nDocument - global indexes of the images.

HTREEITEM AddItemToTree(HWND hwndTV, LPTSTR lpszItem, int nLevel)
{ 
    TVITEM tvi; 
    TVINSERTSTRUCT tvins; 
    static HTREEITEM hPrev = (HTREEITEM)TVI_FIRST; 
    static HTREEITEM hPrevRootItem = NULL; 
    static HTREEITEM hPrevLev2Item = NULL; 
    HTREEITEM hti; 

    tvi.mask = TVIF_TEXT | TVIF_IMAGE 
               | TVIF_SELECTEDIMAGE | TVIF_PARAM; 

    // Set the text of the item. 
    tvi.pszText = lpszItem; 
    tvi.cchTextMax = sizeof(tvi.pszText)/sizeof(tvi.pszText[0]); 

    // Assume the item is not a parent item, so give it a 
    // document image. 
    tvi.iImage = g_nDocument; 
    tvi.iSelectedImage = g_nDocument; 

    // Save the heading level in the item's application-defined 
    // data area. 
    tvi.lParam = (LPARAM)nLevel; 
    tvins.item = tvi; 
    tvins.hInsertAfter = hPrev; 

    // Set the parent item based on the specified level. 
    if (nLevel == 1) 
        tvins.hParent = TVI_ROOT; 
    else if (nLevel == 2) 
        tvins.hParent = hPrevRootItem; 
    else 
        tvins.hParent = hPrevLev2Item; 

    // Add the item to the tree-view control. 
    hPrev = (HTREEITEM)SendMessage(hwndTV, TVM_INSERTITEM, 
        0, (LPARAM)(LPTVINSERTSTRUCT)&tvins); 

    if (hPrev == NULL)
        return NULL;

    // Save the handle to the item. 
    if (nLevel == 1) 
        hPrevRootItem = hPrev; 
    else if (nLevel == 2) 
        hPrevLev2Item = hPrev; 

    // The new item is a child item. Give the parent item a 
    // closed folder bitmap to indicate it now has child items. 
    if (nLevel > 1)
    { 
        hti = TreeView_GetParent(hwndTV, hPrev); 
        tvi.mask = TVIF_IMAGE | TVIF_SELECTEDIMAGE; 
        tvi.hItem = hti; 
        tvi.iImage = g_nClosed; 
        tvi.iSelectedImage = g_nClosed; 
        TreeView_SetItem(hwndTV, &tvi); 
    } 

    return hPrev; 
} 

// Extracts heading text and heading levels from a global 
// array and passes them to a function that adds them as
// parent and child items to a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 

BOOL InitTreeViewItems(HWND hwndTV)
{ 
    HTREEITEM hti;

    // g_rgDocHeadings is an application-defined global array of 
    // the following structures: 
    //     typedef struct 
    //       { 
    //         TCHAR tchHeading[MAX_HEADING_LEN]; 
    //         int tchLevel; 
    //     } Heading; 
    for (int i = 0; i < ARRAYSIZE(g_rgDocHeadings); i++) 
    { 
        // Add the item to the tree-view control. 
        hti = AddItemToTree(hwndTV, g_rgDocHeadings[i].tchHeading, 
            g_rgDocHeadings[i].tchLevel); 

        if (hti == NULL)
            return FALSE;
    } 
           
    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="a83ea-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="a83ea-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a83ea-128">使用 Tree-View 控制項</span><span class="sxs-lookup"><span data-stu-id="a83ea-128">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="a83ea-129">CustDTv 範例說明 Tree-View 控制項中的自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="a83ea-129">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




