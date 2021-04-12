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
# <a name="how-to-drag-a-tree-view-item"></a>如何拖曳 Tree-View 專案

本主題將示範處理樹狀檢視專案的拖放程式碼。 範例程式碼是由三個函式所組成。 第一個函式會開始拖曳作業，第二個函式會拖曳影像，而第三個函式會結束拖曳作業。

> [!Note]  
> 拖曳樹狀檢視專案通常牽涉到處理 [izdebski \_ BEGINDRAG](tvn-begindrag.md) (或 [izdebski \_ BEGINRDRAG](tvn-beginrdrag.md)) 通知碼、 [**wm \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息，以及 [**wm \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (或 [**wm \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) 訊息。 此外，它也會牽涉到使用 [影像清單](image-lists.md) 函式來繪製正在拖曳的專案。

 

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>步驟1：開始進行樹狀檢視拖曳操作

當使用者開始拖曳專案時，樹狀檢視控制項會將 [izdebski \_ BEGINDRAG](tvn-begindrag.md) (或 [izdebski \_ BEGINRDRAG](tvn-beginrdrag.md)) 通知程式碼傳送給父視窗。 父視窗會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式接收通知，其 *lParam* 參數是 [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) 結構的位址。 此結構的成員包含滑鼠指標的螢幕座標，以及包含要拖曳之專案相關資訊的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) 結構。

下列範例顯示如何處理 [**WM \_ 通知**](wm-notify.md) 訊息，以取得 [izdebski \_ BEGINDRAG](tvn-begindrag.md)。


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



開始拖曳作業牽涉到使用 [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) 函數。 函式的參數包含影像清單的控制碼，其中包含要在拖曳作業期間使用的影像和影像的索引。 您可以提供自己的影像清單和影像，也可以讓樹狀檢視控制項使用 [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) 訊息為您建立它們。

因為拖曳影像會在拖曳作業的持續時間內取代滑鼠指標，所以 [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) 需要您在影像內指定作用點。 作用點的座標是相對於影像的左上角。 **ImageList \_BeginDrag** 也會要求您指定拖曳影像的初始位置。 應用程式通常會設定初始位置，讓拖曳影像的作用點與使用者開始拖曳作業時的滑鼠指標相同。

下列函式示範如何開始拖曳樹狀檢視專案。 它會使用由樹狀檢視控制項提供的拖曳影像，並取得專案的周框，以判斷適當的作用點點。 周框的尺寸與影像的維度相同。

此函式會捕捉滑鼠輸入，使滑鼠訊息傳送至父視窗。 父視窗需要後續的 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息，以決定要拖曳影像的位置和 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 訊息，以判斷何時結束拖曳作業。


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



### <a name="step-2-dragging-the-tree-view-item"></a>步驟2：拖曳樹狀檢視專案

您可以在父視窗收到 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)訊息時，藉由呼叫 [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove)函式來拖曳樹狀檢視專案，如下列範例所示。 此範例也會示範如何在拖曳作業期間執行點擊測試，以判斷是否要將樹狀檢視中的其他專案反白顯示為拖放作業的目標。


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a>步驟3：結束樹狀檢視拖曳操作

下列範例顯示如何結束拖曳作業。 當父視窗收到 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)訊息時，就會呼叫 [**ImageList \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag)函式。 樹狀檢視控制項的控制碼會傳遞至函數。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Tree-View 控制項](using-treeview.md)
</dt> <dt>

[CustDTv 範例說明 Tree-View 控制項中的自訂繪圖](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 