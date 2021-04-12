---
title: 如何拖曳 Tree-View 專案
description: 本主題將示範處理樹狀檢視專案的拖放程式碼。
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cedc5f7ec750270ec5d9fb6f567bf473f8c13b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463825"
---
# <a name="how-to-drag-a-tree-view-item"></a><span data-ttu-id="cab65-103">如何拖曳 Tree-View 專案</span><span class="sxs-lookup"><span data-stu-id="cab65-103">How to Drag a Tree-View Item</span></span>

<span data-ttu-id="cab65-104">本主題將示範處理樹狀檢視專案的拖放程式碼。</span><span class="sxs-lookup"><span data-stu-id="cab65-104">This topic demonstrates code for handling dragging and dropping of tree-view items.</span></span> <span data-ttu-id="cab65-105">範例程式碼是由三個函式所組成。</span><span class="sxs-lookup"><span data-stu-id="cab65-105">The sample code consists of three functions.</span></span> <span data-ttu-id="cab65-106">第一個函式會開始拖曳作業，第二個函式會拖曳影像，而第三個函式會結束拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="cab65-106">The first function begins the drag operation, the second function drags the image, and the third function ends the drag operation.</span></span>

> [!Note]  
> <span data-ttu-id="cab65-107">拖曳樹狀檢視專案通常牽涉到處理 [izdebski \_ BEGINDRAG](tvn-begindrag.md) (或 [izdebski \_ BEGINRDRAG](tvn-beginrdrag.md)) 通知碼、 [**wm \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息，以及 [**wm \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (或 [**wm \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) 訊息。</span><span class="sxs-lookup"><span data-stu-id="cab65-107">Dragging a tree-view item typically involves processing the [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code, the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (or [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) message.</span></span> <span data-ttu-id="cab65-108">此外，它也會牽涉到使用 [影像清單](image-lists.md) 函式來繪製正在拖曳的專案。</span><span class="sxs-lookup"><span data-stu-id="cab65-108">It also involves using the [Image Lists](image-lists.md) functions to draw the item as it is being dragged.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="cab65-109">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="cab65-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cab65-110">技術</span><span class="sxs-lookup"><span data-stu-id="cab65-110">Technologies</span></span>

-   [<span data-ttu-id="cab65-111">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="cab65-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cab65-112">必要條件</span><span class="sxs-lookup"><span data-stu-id="cab65-112">Prerequisites</span></span>

-   <span data-ttu-id="cab65-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="cab65-113">C/C++</span></span>
-   <span data-ttu-id="cab65-114">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="cab65-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cab65-115">指示</span><span class="sxs-lookup"><span data-stu-id="cab65-115">Instructions</span></span>

### <a name="step-1-beginning-the-tree-view-drag-operation"></a><span data-ttu-id="cab65-116">步驟1：開始進行樹狀檢視拖曳操作</span><span class="sxs-lookup"><span data-stu-id="cab65-116">Step 1: Beginning the tree-view drag operation</span></span>

<span data-ttu-id="cab65-117">當使用者開始拖曳專案時，樹狀檢視控制項會將 [izdebski \_ BEGINDRAG](tvn-begindrag.md) (或 [izdebski \_ BEGINRDRAG](tvn-beginrdrag.md)) 通知程式碼傳送給父視窗。</span><span class="sxs-lookup"><span data-stu-id="cab65-117">A tree-view control sends the parent window a [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code whenever the user starts to drag an item.</span></span> <span data-ttu-id="cab65-118">父視窗會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式接收通知，其 *lParam* 參數是 [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="cab65-118">The parent window receives the notification in the form of a [**WM\_NOTIFY**](wm-notify.md) message whose *lParam* parameter is the address of an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="cab65-119">此結構的成員包含滑鼠指標的螢幕座標，以及包含要拖曳之專案相關資訊的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) 結構。</span><span class="sxs-lookup"><span data-stu-id="cab65-119">The members of this structure include the screen coordinates of the mouse pointer and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains information about the item to be dragged.</span></span>

<span data-ttu-id="cab65-120">下列範例顯示如何處理 [**WM \_ 通知**](wm-notify.md) 訊息，以取得 [izdebski \_ BEGINDRAG](tvn-begindrag.md)。</span><span class="sxs-lookup"><span data-stu-id="cab65-120">The following example shows how to process the [**WM\_NOTIFY**](wm-notify.md) message to obtain [TVN\_BEGINDRAG](tvn-begindrag.md).</span></span>


```C++
    case WM_NOTIFY: 
        switch (((LPNMHDR)lParam)->code) 
        {
            case TVN_BEGINDRAG:
                Main_OnBeginDrag(((LPNMHDR)lParam)->hwndFrom, (LPNMTREEVIEW)lParam);
                break;
        
            // Handle other cases here. 
        }
        break; 
```



<span data-ttu-id="cab65-121">開始拖曳作業牽涉到使用 [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) 函數。</span><span class="sxs-lookup"><span data-stu-id="cab65-121">Beginning the drag operation involves using the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function.</span></span> <span data-ttu-id="cab65-122">函式的參數包含影像清單的控制碼，其中包含要在拖曳作業期間使用的影像和影像的索引。</span><span class="sxs-lookup"><span data-stu-id="cab65-122">The function's parameters include the handle to the image list that contains the image to use during the drag operation and the index of the image.</span></span> <span data-ttu-id="cab65-123">您可以提供自己的影像清單和影像，也可以讓樹狀檢視控制項使用 [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) 訊息為您建立它們。</span><span class="sxs-lookup"><span data-stu-id="cab65-123">You can either provide your own image list and image, or you can have the tree-view control create them for you by using the [**TVM\_CREATEDRAGIMAGE**](tvm-createdragimage.md) message.</span></span>

<span data-ttu-id="cab65-124">因為拖曳影像會在拖曳作業的持續時間內取代滑鼠指標，所以 [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) 需要您在影像內指定作用點。</span><span class="sxs-lookup"><span data-stu-id="cab65-124">Because the drag image replaces the mouse pointer for the duration of the drag operation, [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requires you to specify a hot spot within the image.</span></span> <span data-ttu-id="cab65-125">作用點的座標是相對於影像的左上角。</span><span class="sxs-lookup"><span data-stu-id="cab65-125">The coordinates of the hot spot are relative to the upper left corner of the image.</span></span> <span data-ttu-id="cab65-126">**ImageList \_BeginDrag** 也會要求您指定拖曳影像的初始位置。</span><span class="sxs-lookup"><span data-stu-id="cab65-126">**ImageList\_BeginDrag** also requires you to specify the initial location of the drag image.</span></span> <span data-ttu-id="cab65-127">應用程式通常會設定初始位置，讓拖曳影像的作用點與使用者開始拖曳作業時的滑鼠指標相同。</span><span class="sxs-lookup"><span data-stu-id="cab65-127">An application typically sets the initial location so that the hot spot of the drag image corresponds to that of the mouse pointer at the time the user began the drag operation.</span></span>

<span data-ttu-id="cab65-128">下列函式示範如何開始拖曳樹狀檢視專案。</span><span class="sxs-lookup"><span data-stu-id="cab65-128">The following function demonstrates how to begin dragging a tree-view item.</span></span> <span data-ttu-id="cab65-129">它會使用由樹狀檢視控制項提供的拖曳影像，並取得專案的周框，以判斷適當的作用點點。</span><span class="sxs-lookup"><span data-stu-id="cab65-129">It uses the drag image provided by the tree-view control and obtains the bounding rectangle of the item to determine the appropriate point for the hot spot.</span></span> <span data-ttu-id="cab65-130">周框的尺寸與影像的維度相同。</span><span class="sxs-lookup"><span data-stu-id="cab65-130">The dimensions of the bounding rectangle are the same as those of the image.</span></span>

<span data-ttu-id="cab65-131">此函式會捕捉滑鼠輸入，使滑鼠訊息傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="cab65-131">The function captures mouse input, causing mouse messages to be sent to the parent window.</span></span> <span data-ttu-id="cab65-132">父視窗需要後續的 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息，以決定要拖曳影像的位置和 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 訊息，以判斷何時結束拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="cab65-132">The parent window needs the subsequent [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to determine where to drag the image and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message to determine when to end the drag operation.</span></span>


```C++
// Begin dragging an item in a tree-view control. 
// hwndTV - handle to the image list. 
// lpnmtv - address of information about the item being dragged.
//
// g_fDragging -- global BOOL that specifies whether dragging is underway.

void Main_OnBeginDrag(HWND hwndTV, LPNMTREEVIEW lpnmtv)
{ 
    HIMAGELIST himl;    // handle to image list 
    RECT rcItem;        // bounding rectangle of item 

    // Tell the tree-view control to create an image to use 
    // for dragging. 
    himl = TreeView_CreateDragImage(hwndTV, lpnmtv->itemNew.hItem); 

    // Get the bounding rectangle of the item being dragged. 
    TreeView_GetItemRect(hwndTV, lpnmtv->itemNew.hItem, &rcItem, TRUE); 

    // Start the drag operation. 
    ImageList_BeginDrag(himl, 0, 0, 0);
    ImageList_DragEnter(hwndTV, lpnmtv->ptDrag.x, lpnmtv->ptDrag.x); 

    // Hide the mouse pointer, and direct mouse input to the 
    // parent window. 
    ShowCursor(FALSE); 
    SetCapture(GetParent(hwndTV)); 
    g_fDragging = TRUE; 

    return; 

} 
```



### <a name="step-2-dragging-the-tree-view-item"></a><span data-ttu-id="cab65-133">步驟2：拖曳樹狀檢視專案</span><span class="sxs-lookup"><span data-stu-id="cab65-133">Step 2: Dragging the tree-view item</span></span>

<span data-ttu-id="cab65-134">您可以在父視窗收到 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)訊息時，藉由呼叫 [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove)函式來拖曳樹狀檢視專案，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="cab65-134">You drag a tree-view item by calling the [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function when the parent window receives a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, as the following example shows.</span></span> <span data-ttu-id="cab65-135">此範例也會示範如何在拖曳作業期間執行點擊測試，以判斷是否要將樹狀檢視中的其他專案反白顯示為拖放作業的目標。</span><span class="sxs-lookup"><span data-stu-id="cab65-135">The example also demonstrates how to perform hit testing during the drag operation to determine whether to highlight other items in the tree view as targets of a drag-and-drop operation.</span></span>


```C++
// Drag an item in a tree-view control, 
// highlighting the item that is the target. 
// hwndParent - handle to the parent window. 
// hwndTV - handle to the tree-view control.
// xCur and yCur - coordinates of the mouse pointer,
//     relative to the parent window. 
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnMouseMove(HWND hwndParent, HWND hwndTV, LONG xCur, LONG yCur) 
{ 
    HTREEITEM htiTarget;  // Handle to target item. 
    TVHITTESTINFO tvht;   // Hit test information. 

    if (g_fDragging) 
    { 
       // Drag the item to the current position of the mouse pointer. 
       // First convert the dialog coordinates to control coordinates. 
       POINT point;
       point.x = xCur;
       point.y = yCur;
       ClientToScreen(hwndParent, &point);
       ScreenToClient(hwndTV, &point);
       ImageList_DragMove(point.x, point.y);
       // Turn off the dragged image so the background can be refreshed.
       ImageList_DragShowNolock(FALSE); 
                
        // Find out if the pointer is on the item. If it is, 
        // highlight the item as a drop target. 
        tvht.pt.x = point.x; 
        tvht.pt.y = point.y; 
        if ((htiTarget = TreeView_HitTest(hwndTV, &tvht)) != NULL) 
        { 
            TreeView_SelectDropTarget(hwndTV, htiTarget); 
        } 
        ImageList_DragShowNolock(TRUE);
    } 
    return; 
}
```



### <a name="step-3-ending-the-tree-view-drag-operation"></a><span data-ttu-id="cab65-136">步驟3：結束樹狀檢視拖曳操作</span><span class="sxs-lookup"><span data-stu-id="cab65-136">Step 3: Ending the tree-view drag operation</span></span>

<span data-ttu-id="cab65-137">下列範例顯示如何結束拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="cab65-137">The following example shows how to end a drag operation.</span></span> <span data-ttu-id="cab65-138">當父視窗收到 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)訊息時，就會呼叫 [**ImageList \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag)函式。</span><span class="sxs-lookup"><span data-stu-id="cab65-138">The [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function is called when the parent window receives a [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message.</span></span> <span data-ttu-id="cab65-139">樹狀檢視控制項的控制碼會傳遞至函數。</span><span class="sxs-lookup"><span data-stu-id="cab65-139">The handle of the tree-view control is passed to the function.</span></span>


```C++
// Stops dragging a tree-view item, releases the 
// mouse capture, and shows the mouse pointer.
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnLButtonUp(HWND hwndTV) 
{ 
    if (g_fDragging) 
    { 
        // Get destination item.
        HTREEITEM htiDest = TreeView_GetDropHilight(hwndTV);
        if (htiDest != NULL)
        {
            // To do: handle the actual moving of the dragged node.
        }
        ImageList_EndDrag(); 
        TreeView_SelectDropTarget(hwndTV, NULL);
        ReleaseCapture(); 
        ShowCursor(TRUE); 
        g_fDragging = FALSE; 
    } 
    return; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="cab65-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="cab65-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cab65-141">使用 Tree-View 控制項</span><span class="sxs-lookup"><span data-stu-id="cab65-141">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="cab65-142">CustDTv 範例說明 Tree-View 控制項中的自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="cab65-142">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 