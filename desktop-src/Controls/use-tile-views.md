---
title: 如何使用磚視圖
description: 本主題將示範如何設定清單視圖控制項的圖格視圖。
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933728"
---
# <a name="how-to-use-tile-views"></a><span data-ttu-id="d2324-103">如何使用磚視圖</span><span class="sxs-lookup"><span data-stu-id="d2324-103">How to Use Tile Views</span></span>

<span data-ttu-id="d2324-104">本主題將示範如何設定清單視圖控制項的圖格視圖。</span><span class="sxs-lookup"><span data-stu-id="d2324-104">This topic demonstrates how to set the tile view for a list-view control.</span></span> <span data-ttu-id="d2324-105">在 [並排顯示] 中，每個專案都是以包含一或多行伴隨文字的大型圖示來表示。</span><span class="sxs-lookup"><span data-stu-id="d2324-105">In tile view, each item is represented by a large icon with one or more lines of accompanying text.</span></span> <span data-ttu-id="d2324-106">如需圖例，請參閱 [關於 List-View 控制項](list-view-controls-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d2324-106">For an illustration, see [About List-View Controls](list-view-controls-overview.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d2324-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d2324-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d2324-108">技術</span><span class="sxs-lookup"><span data-stu-id="d2324-108">Technologies</span></span>

-   [<span data-ttu-id="d2324-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d2324-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d2324-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="d2324-110">Prerequisites</span></span>

-   <span data-ttu-id="d2324-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d2324-111">C/C++</span></span>
-   <span data-ttu-id="d2324-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="d2324-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d2324-113">指示</span><span class="sxs-lookup"><span data-stu-id="d2324-113">Instructions</span></span>


<span data-ttu-id="d2324-114">使用 [**ListView \_ SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) 宏設定磚視圖的一般顯示參數。</span><span class="sxs-lookup"><span data-stu-id="d2324-114">Set the general display parameters for tile view by using the [**ListView\_SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) macro.</span></span> <span data-ttu-id="d2324-115">使用傳遞至這個宏的 [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) 結構，以指定文字相對於圖示的位置、每個磚的大小 (包括伴隨的文字) ，以及最大的文字行數。</span><span class="sxs-lookup"><span data-stu-id="d2324-115">Use the [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) structure that is passed to this macro to specify the position of the text in relation to the icon, the size of each tile (including accompanying text), and the maximum number of lines of text.</span></span>

<span data-ttu-id="d2324-116">如果您不想讓磚自動調整大小，您必須在 [**TILESIZE**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo)成員的 **DwFlags** 成員和 **LVTVIM \_ dwMask** 中設定 **LVTVIF \_ FIXEDSIZE** ，以及提供 **LVTILEVIEWINFO** **成員中** 的維度。</span><span class="sxs-lookup"><span data-stu-id="d2324-116">If you do not want tiles to be automatically sized, you must set **LVTVIF\_FIXEDSIZE** in the **dwFlags** member and **LVTVIM\_TILESIZE** in the **dwMask** member of [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), as well as providing the dimensions in the **sizeTile** member.</span></span>

<span data-ttu-id="d2324-117">下列 c + + 程式碼範例會設定清單視圖控制項的圖格視圖資訊，因此每個專案最多會顯示兩個子專案。</span><span class="sxs-lookup"><span data-stu-id="d2324-117">The following C++ code example sets the tile view info for a list-view control so that a maximum of two subitems are displayed for each item.</span></span> <span data-ttu-id="d2324-118">它也會設定每個磚的大小。</span><span class="sxs-lookup"><span data-stu-id="d2324-118">It also sets the size of each tile.</span></span>


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



<span data-ttu-id="d2324-119">針對清單中的每個專案，您可以在專案插入清單或更新版本時，設定進一步的參數。</span><span class="sxs-lookup"><span data-stu-id="d2324-119">For each item in the list, you can set further parameters when the item is inserted in the list, or later.</span></span> <span data-ttu-id="d2324-120">與 [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem)搭配使用的 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構包含成員，這些成員會指定要顯示在專案底下的資料行，以及其對齊方式。</span><span class="sxs-lookup"><span data-stu-id="d2324-120">The [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that is used with [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contains members that specify which columns of data to display below the item, and their alignment.</span></span> <span data-ttu-id="d2324-121">這些相同的顯示參數也可以在與 [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo)搭配使用的 [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo)結構中找到。</span><span class="sxs-lookup"><span data-stu-id="d2324-121">These same display parameters are also found in the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure used with [**ListView\_SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span></span>

> [!Note]  
> <span data-ttu-id="d2324-122">此處的「資料行」指的不是要在並排顯示中顯示資料行，而是在 [詳細資料] 視圖中顯示在資料行中的子欄位。</span><span class="sxs-lookup"><span data-stu-id="d2324-122">"Columns" here refers not to display columns in tile view but rather to subitems, which are displayed in columns in details view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d2324-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2324-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2324-124">清單視圖控制項參考</span><span class="sxs-lookup"><span data-stu-id="d2324-124">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d2324-125">關於 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="d2324-125">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="d2324-126">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="d2324-126">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




