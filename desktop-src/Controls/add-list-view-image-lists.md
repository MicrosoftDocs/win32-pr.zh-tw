---
title: 如何新增 List-View 的影像清單
description: 本主題示範如何將影像清單新增至清單視圖控制項。
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f6f5b483ea80b412ab7638c9aceafcac4c5e6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316783"
---
# <a name="how-to-add-list-view-image-lists"></a><span data-ttu-id="ba3ad-103">如何新增 List-View 的影像清單</span><span class="sxs-lookup"><span data-stu-id="ba3ad-103">How to Add List-View Image Lists</span></span>

<span data-ttu-id="ba3ad-104">本主題示範如何將影像清單新增至清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="ba3ad-104">This topic demonstrates how to add image lists to a list-view control.</span></span>

<span data-ttu-id="ba3ad-105">您只會建立控制項使用的影像清單。</span><span class="sxs-lookup"><span data-stu-id="ba3ad-105">You create only the image lists that the control uses.</span></span> <span data-ttu-id="ba3ad-106">例如，如果您的應用程式不允許使用者切換至圖示視圖，您就不需要建立並指派大型圖示清單。</span><span class="sxs-lookup"><span data-stu-id="ba3ad-106">For example, if your application does not allow the user to switch to icon view, you do not need to create and assign a large icon list.</span></span> <span data-ttu-id="ba3ad-107">如果您同時建立大型和小型影像清單，則必須以相同的順序包含相同的影像，因為單一值會用來識別兩個影像清單中的清單視圖專案圖示。</span><span class="sxs-lookup"><span data-stu-id="ba3ad-107">If you create both large and small image lists, they must contain the same images in the same order, because a single value is used to identify a list-view item's icon in both image lists.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ba3ad-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="ba3ad-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ba3ad-109">技術</span><span class="sxs-lookup"><span data-stu-id="ba3ad-109">Technologies</span></span>

-   [<span data-ttu-id="ba3ad-110">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="ba3ad-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ba3ad-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="ba3ad-111">Prerequisites</span></span>

-   <span data-ttu-id="ba3ad-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="ba3ad-112">C/C++</span></span>
-   <span data-ttu-id="ba3ad-113">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="ba3ad-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ba3ad-114">指示</span><span class="sxs-lookup"><span data-stu-id="ba3ad-114">Instructions</span></span>


<span data-ttu-id="ba3ad-115">若要顯示專案影像，您必須將影像清單指派給清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="ba3ad-115">To display item images, you must assign an image list to the list-view control.</span></span> <span data-ttu-id="ba3ad-116">若要這樣做，請使用 [**LVM \_ SETIMAGELIST**](lvm-setimagelist.md) 訊息或對應的宏 [**ListView \_ SETIMAGELIST**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist)，指定影像清單是否包含完整大小的圖示、小圖示或狀態影像。</span><span class="sxs-lookup"><span data-stu-id="ba3ad-116">To do this, use the [**LVM\_SETIMAGELIST**](lvm-setimagelist.md) message or the corresponding macro [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist), specifying whether the image list contains full-sized icons, small icons, or state images.</span></span> <span data-ttu-id="ba3ad-117">若要取得目前指派給清單視圖控制項的影像清單控制碼，請使用 [**LVM \_ GETIMAGELIST**](lvm-getimagelist.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="ba3ad-117">To retrieve the handle to an image list that is currently assigned to a list-view control, use the [**LVM\_GETIMAGELIST**](lvm-getimagelist.md) message.</span></span> <span data-ttu-id="ba3ad-118">您可以使用 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式來判斷完整大小和小圖示的適當維度。</span><span class="sxs-lookup"><span data-stu-id="ba3ad-118">You can use the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function to determine appropriate dimensions for the full-sized and small icons.</span></span>

<span data-ttu-id="ba3ad-119">在下列 c + + 程式碼範例中，應用程式定義函式會先建立影像清單，然後將它們指派給清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="ba3ad-119">In the following C++ code example, the application-defined function first creates image lists and then assigns them to a list-view control.</span></span>


```C++
// InitListViewImageLists: Creates image lists for a list-view control.
// This function only creates image lists. It does not insert the items into
// the control, which is necessary for the control to be visible.   
//
// Returns TRUE if successful, or FALSE otherwise. 
//
// hWndListView: Handle to the list-view control. 
// global variable g_hInst: The handle to the module of either a 
// dynamic-link library (DLL) or executable (.exe) that contains
// the image to be loaded. If loading a standard or system
// icon, set g_hInst to NULL.
//
BOOL InitListViewImageLists(HWND hWndListView) 
{ 
    HICON hiconItem;     // Icon for list-view items.
    HIMAGELIST hLarge;   // Image list for icon view.
    HIMAGELIST hSmall;   // Image list for other views.

    // Create the full-sized icon image lists. 
    hLarge = ImageList_Create(GetSystemMetrics(SM_CXICON), 
                              GetSystemMetrics(SM_CYICON), 
                              ILC_MASK, 1, 1); 

    hSmall = ImageList_Create(GetSystemMetrics(SM_CXSMICON), 
                              GetSystemMetrics(SM_CYSMICON), 
                              ILC_MASK, 1, 1); 
    
    // Add an icon to each image list.  
    hiconItem = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ITEM));

    ImageList_AddIcon(hLarge, hiconItem);
    ImageList_AddIcon(hSmall, hiconItem);

    DestroyIcon(hiconItem);
 
// When you are dealing with multiple icons, you can use the previous four lines of 
// code inside a loop. The following code shows such a loop. The 
// icons are defined in the application's header file as resources, which 
// are numbered consecutively starting with IDS_FIRSTICON. The number of 
// icons is defined in the header file as C_ICONS.
/*    
    for(index = 0; index < C_ICONS; index++)
    {
        hIconItem = LoadIcon (g_hinst, MAKEINTRESOURCE(IDS_FIRSTICON + index));
        ImageList_AddIcon(hSmall, hIconItem);
        ImageList_AddIcon(hLarge, hIconItem);
        Destroy(hIconItem);
    }
*/
    
    // Assign the image lists to the list-view control. 
    ListView_SetImageList(hWndListView, hLarge, LVSIL_NORMAL); 
    ListView_SetImageList(hWndListView, hSmall, LVSIL_SMALL); 
    
    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="ba3ad-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba3ad-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba3ad-121">清單視圖控制項參考</span><span class="sxs-lookup"><span data-stu-id="ba3ad-121">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ba3ad-122">關於 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="ba3ad-122">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="ba3ad-123">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="ba3ad-123">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 