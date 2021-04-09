---
title: 如何使用 List-View 工作區
description: 本主題將示範如何使用清單視圖的工作區域。 工作區域是可以用來排列清單檢視控制項中專案的矩形虛擬區域。
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021280"
---
# <a name="how-to-use-list-view-working-areas"></a><span data-ttu-id="37db2-104">如何使用 List-View 工作區</span><span class="sxs-lookup"><span data-stu-id="37db2-104">How to Use List-View Working Areas</span></span>

<span data-ttu-id="37db2-105">本主題將示範如何使用清單視圖的工作區域。</span><span class="sxs-lookup"><span data-stu-id="37db2-105">This topic demonstrates how to work with list-view working areas.</span></span> <span data-ttu-id="37db2-106">工作區域是可以用來排列清單檢視控制項中專案的矩形虛擬區域。</span><span class="sxs-lookup"><span data-stu-id="37db2-106">Working areas are rectangular virtual areas that can be used to arrange items in a list-vew control.</span></span> <span data-ttu-id="37db2-107">工作區域不是視窗，且不能有可見的框線。</span><span class="sxs-lookup"><span data-stu-id="37db2-107">A working area is not a window and cannot have a visible border.</span></span> <span data-ttu-id="37db2-108">依預設，清單視圖控制項沒有任何工作區域。</span><span class="sxs-lookup"><span data-stu-id="37db2-108">By default, the list-view control has no working areas.</span></span> <span data-ttu-id="37db2-109">藉由建立工作區，您可以在專案的左邊、頂端或右邊建立空白框線，或在正常情況下，顯示水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="37db2-109">By creating a working area, you can create an empty border on the left, top, or right of the items or cause a horizontal scroll bar to be displayed when there normally would not be one.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="37db2-110">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="37db2-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="37db2-111">技術</span><span class="sxs-lookup"><span data-stu-id="37db2-111">Technologies</span></span>

-   [<span data-ttu-id="37db2-112">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="37db2-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="37db2-113">必要條件</span><span class="sxs-lookup"><span data-stu-id="37db2-113">Prerequisites</span></span>

-   <span data-ttu-id="37db2-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="37db2-114">C/C++</span></span>
-   <span data-ttu-id="37db2-115">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="37db2-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="37db2-116">指示</span><span class="sxs-lookup"><span data-stu-id="37db2-116">Instructions</span></span>

### <a name="create-a-working-area"></a><span data-ttu-id="37db2-117">建立工作區</span><span class="sxs-lookup"><span data-stu-id="37db2-117">Create a Working Area</span></span>

<span data-ttu-id="37db2-118">下列 c + + 程式碼範例示範如何在其頂端、左方和右邊建立具有25圖元空白框線的工作區域。</span><span class="sxs-lookup"><span data-stu-id="37db2-118">The following C++ code example demonstrates how to create a working area with a 25-pixel empty border on its top, left, and right sides.</span></span>


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a><span data-ttu-id="37db2-119">建立多個工作區</span><span class="sxs-lookup"><span data-stu-id="37db2-119">Create Multiple Working Areas</span></span>

<span data-ttu-id="37db2-120">下列 c + + 程式碼範例示範如何在控制項中建立兩個工作區。</span><span class="sxs-lookup"><span data-stu-id="37db2-120">The following C++ code example demonstrates how to create two working areas in a control.</span></span> <span data-ttu-id="37db2-121">每個工作區都會使用大約一半的工作區，並以25圖元的空白框線括住。</span><span class="sxs-lookup"><span data-stu-id="37db2-121">Each working area uses about half of the client area, and is surrounded by a 25-pixel empty border.</span></span>


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a><span data-ttu-id="37db2-122">判斷專案所屬的工作區域</span><span class="sxs-lookup"><span data-stu-id="37db2-122">Determine the Working Area to Which an Item Belongs</span></span>

<span data-ttu-id="37db2-123">判斷專案所屬工作區域的其中一種方式是執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="37db2-123">One way to determine which working area an item belongs is to do the following:</span></span>

-   <span data-ttu-id="37db2-124">取得清單視圖控制項中所有工作區域的座標清單。</span><span class="sxs-lookup"><span data-stu-id="37db2-124">Retrieve the list of coordinates of all of the working areas in the list-view control.</span></span>
-   <span data-ttu-id="37db2-125">取出專案的座標。</span><span class="sxs-lookup"><span data-stu-id="37db2-125">Retrieve the coordinates of the item.</span></span>
-   <span data-ttu-id="37db2-126">判斷專案座標是否位於其中一個工作區域的座標內。</span><span class="sxs-lookup"><span data-stu-id="37db2-126">Determine whether the item coordinates lie within the coordinates of one of the working areas.</span></span>

<span data-ttu-id="37db2-127">下列 c + + 程式碼範例中的應用程式定義函數會傳回專案所屬之工作區域的索引。</span><span class="sxs-lookup"><span data-stu-id="37db2-127">The application-defined function in the following C++ code example returns the index of the working area to which the item belongs.</span></span> <span data-ttu-id="37db2-128">如果函式失敗，則會傳回–1。</span><span class="sxs-lookup"><span data-stu-id="37db2-128">If the function fails, it returns –1.</span></span> <span data-ttu-id="37db2-129">如果函式成功，但專案不在任何工作區域內，則函式會傳回0，因為不在工作區域內的所有專案都會自動成為工作區域零的成員。</span><span class="sxs-lookup"><span data-stu-id="37db2-129">If the function succeeds, but the item is not inside any of the working areas, the function returns 0, because all items that are not inside a working area automatically become a member of working area zero.</span></span>


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a><span data-ttu-id="37db2-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="37db2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37db2-131">清單視圖控制項參考</span><span class="sxs-lookup"><span data-stu-id="37db2-131">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="37db2-132">關於 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="37db2-132">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="37db2-133">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="37db2-133">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




