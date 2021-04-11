---
title: 如何新增 List-View 資料行
description: 本主題示範如何將資料行加入至清單視圖控制項。
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e478c57a31fdd7ad91e0089106e93c24c47d5c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024345"
---
# <a name="how-to-add-list-view-columns"></a><span data-ttu-id="fea79-103">如何新增 List-View 資料行</span><span class="sxs-lookup"><span data-stu-id="fea79-103">How to Add List-View Columns</span></span>

<span data-ttu-id="fea79-104">本主題示範如何將資料行加入至清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="fea79-104">This topic demonstrates how to add columns to a list-view control.</span></span> <span data-ttu-id="fea79-105">當清單視圖控制項位於報表 (詳細資料) 視圖時，會使用資料行來顯示專案和子專案。</span><span class="sxs-lookup"><span data-stu-id="fea79-105">Columns are used to display the items and subitems when a list-view control is in report (details) view.</span></span> <span data-ttu-id="fea79-106">選取之資料行中的文字也可以顯示在磚視圖中。</span><span class="sxs-lookup"><span data-stu-id="fea79-106">Text from selected columns can also be displayed in tile view.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fea79-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="fea79-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fea79-108">技術</span><span class="sxs-lookup"><span data-stu-id="fea79-108">Technologies</span></span>

-   [<span data-ttu-id="fea79-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="fea79-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fea79-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="fea79-110">Prerequisites</span></span>

-   <span data-ttu-id="fea79-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="fea79-111">C/C++</span></span>
-   <span data-ttu-id="fea79-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="fea79-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fea79-113">指示</span><span class="sxs-lookup"><span data-stu-id="fea79-113">Instructions</span></span>


<span data-ttu-id="fea79-114">若要將資料行新增至清單視圖控制項，請傳送 [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) 訊息或使用 [**ListView \_ INSERTCOLUMN**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) 宏。</span><span class="sxs-lookup"><span data-stu-id="fea79-114">To add a column to a list-view control, send the [**LVM\_INSERTCOLUMN**](lvm-insertcolumn.md) message or use the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span> <span data-ttu-id="fea79-115">若要刪除資料行，請使用 [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="fea79-115">To delete a column, use the [**LVM\_DELETECOLUMN**](lvm-deletecolumn.md) message.</span></span>

<span data-ttu-id="fea79-116">下列 c + + 程式碼範例會呼叫 [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) 宏，以將資料行加入至清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="fea79-116">The following C++ code example calls the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro to add columns to a list-view control.</span></span> <span data-ttu-id="fea79-117">欄位標題會在應用程式的標頭檔中定義為字串資源，這些資源會從識別碼 FIRSTCOLUMN 開始連續編號 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fea79-117">The column headings are defined in the application's header file as string resources, which are numbered consecutively starting with IDS\_FIRSTCOLUMN.</span></span> <span data-ttu-id="fea79-118">在標頭檔中，將資料行數目定義為 **C 資料 \_ 行**。</span><span class="sxs-lookup"><span data-stu-id="fea79-118">The number of columns is defined in the header file as **C\_COLUMNS**.</span></span>


```C++
// InitListViewColumns: Adds columns to a list-view control.
// hWndListView:        Handle to the list-view control. 
// Returns TRUE if successful, and FALSE otherwise. 
BOOL InitListViewColumns(HWND hWndListView) 
{ 
    WCHAR szText[256];     // Temporary buffer.
    LVCOLUMN lvc;
    int iCol;

    // Initialize the LVCOLUMN structure.
    // The mask specifies that the format, width, text,
    // and subitem members of the structure are valid.
    lvc.mask = LVCF_FMT | LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM;

    // Add the columns.
    for (iCol = 0; iCol < C_COLUMNS; iCol++)
    {
        lvc.iSubItem = iCol;
        lvc.pszText = szText;
        lvc.cx = 100;               // Width of column in pixels.

        if ( iCol < 2 )
            lvc.fmt = LVCFMT_LEFT;  // Left-aligned column.
        else
            lvc.fmt = LVCFMT_RIGHT; // Right-aligned column.

        // Load the names of the column headings from the string resources.
        LoadString(g_hInst,
                   IDS_FIRSTCOLUMN + iCol,
                   szText,
                   sizeof(szText)/sizeof(szText[0]));

        // Insert the columns into the list view.
        if (ListView_InsertColumn(hWndListView, iCol, &lvc) == -1)
            return FALSE;
    }
    
    return TRUE;
} 
```



## <a name="related-topics"></a><span data-ttu-id="fea79-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="fea79-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fea79-120">清單視圖控制項參考</span><span class="sxs-lookup"><span data-stu-id="fea79-120">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="fea79-121">關於 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="fea79-121">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="fea79-122">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="fea79-122">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




