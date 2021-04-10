---
title: 如何拖曳影像
description: 本主題示範如何在螢幕上拖曳影像。 拖曳函式平滑且沒有游標閃爍地移動彩色影像。 遮罩影像和未遮罩影像都可以拖曳。
ms.assetid: 84AFA770-F495-4312-9631-3335BA8CC799
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da495ef9ee0895c04a856f456fcda3e3125f2957
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683199"
---
# <a name="how-to-drag-an-image"></a><span data-ttu-id="f01f0-105">如何拖曳影像</span><span class="sxs-lookup"><span data-stu-id="f01f0-105">How to Drag an Image</span></span>

<span data-ttu-id="f01f0-106">本主題示範如何在螢幕上拖曳影像。</span><span class="sxs-lookup"><span data-stu-id="f01f0-106">This topic demonstrates how to drag an image on the screen.</span></span> <span data-ttu-id="f01f0-107">拖曳函式平滑且沒有游標閃爍地移動彩色影像。</span><span class="sxs-lookup"><span data-stu-id="f01f0-107">The dragging functions move an image smoothly, in color, and without any flashing of the cursor.</span></span> <span data-ttu-id="f01f0-108">遮罩影像和未遮罩影像都可以拖曳。</span><span class="sxs-lookup"><span data-stu-id="f01f0-108">Both masked and unmasked images can be dragged.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f01f0-109">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="f01f0-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f01f0-110">技術</span><span class="sxs-lookup"><span data-stu-id="f01f0-110">Technologies</span></span>

-   [<span data-ttu-id="f01f0-111">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="f01f0-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f01f0-112">必要條件</span><span class="sxs-lookup"><span data-stu-id="f01f0-112">Prerequisites</span></span>

-   <span data-ttu-id="f01f0-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="f01f0-113">C/C++</span></span>
-   <span data-ttu-id="f01f0-114">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="f01f0-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f01f0-115">指示</span><span class="sxs-lookup"><span data-stu-id="f01f0-115">Instructions</span></span>

### <a name="step-1-begin-the-drag-operation"></a><span data-ttu-id="f01f0-116">步驟1：開始拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="f01f0-116">Step 1: Begin the drag operation.</span></span>

<span data-ttu-id="f01f0-117">使用 [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) 函數開始拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="f01f0-117">Use the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function to begin a drag operation.</span></span>

<span data-ttu-id="f01f0-118">下列 c + + 程式碼範例中的使用者定義函式是為了回應滑鼠按鍵的訊息（例如， [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)）而被呼叫。</span><span class="sxs-lookup"><span data-stu-id="f01f0-118">The user-defined function in the following C++ code example is intended to be called in response to a mouse button-down message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="f01f0-119">此函式會決定使用者是否已在影像的周框中按一下。</span><span class="sxs-lookup"><span data-stu-id="f01f0-119">The function determines whether the user has clicked within the bounding rectangle of the image.</span></span> <span data-ttu-id="f01f0-120">如果使用者已按一下，此函式會捕捉滑鼠輸入、從工作區中清除影像，並計算影像內作用點的位置。</span><span class="sxs-lookup"><span data-stu-id="f01f0-120">If the user has clicked, the function captures the mouse input, erases the image from the client area, and calculates the position for the hot spot within the image.</span></span> <span data-ttu-id="f01f0-121">此函式會將作用點設定為與滑鼠游標的作用點一致。</span><span class="sxs-lookup"><span data-stu-id="f01f0-121">The function sets the hot spot to coincide with the hot spot of the mouse cursor.</span></span> <span data-ttu-id="f01f0-122">然後，此函式會呼叫 [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)來開始拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="f01f0-122">Then the function begins the drag operation by calling [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).</span></span>


```C++
// StartDragging - begins dragging a bitmap. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// ptCur - coordinates of the cursor. 
// himl - handle to the image list. 
// 
// Global variables 
//     g_rcImage - bounding rectangle of the image to drag. 
//     g_nImage - index of the image. 
//     g_ptHotSpot - location of the image's hot spot. 
//     g_cxBorder and g_cyBorder - width and height of border. 
//     g_cyCaption and g_cyMenu - height of title bar and menu bar. 
extern RECT g_rcImage; 
extern int g_nImage; 
extern POINT g_ptHotSpot; 
 
BOOL StartDragging(HWND hwnd, POINT ptCur, HIMAGELIST himl) 
{ 
    // Return if the cursor is not in the bounding rectangle of 
    // the image. 
    if (!PtInRect(&g_rcImage, ptCur)) 
        return FALSE; 
 
    // Capture the mouse input. 
    SetCapture(hwnd); 
 
    // Erase the image from the client area. 
    InvalidateRect(hwnd, &g_rcImage, TRUE); 
    UpdateWindow(hwnd); 
 
    // Calculate the location of the hot spot, and save it. 
    g_ptHotSpot.x = ptCur.x - g_rcImage.left; 
    g_ptHotSpot.y = ptCur.y - g_rcImage.top; 
 
    // Begin the drag operation. 
    if (!ImageList_BeginDrag(himl, g_nImage, 
            g_ptHotSpot.x, g_ptHotSpot.y)) 
        return FALSE; 
 
    // Set the initial location of the image, and make it visible. 
    // Because the ImageList_DragEnter function expects coordinates to 
    // be relative to the upper-left corner of the given window, the 
    // width of the border, title bar, and menu bar need to be taken 
    // into account. 
    
    ImageList_DragEnter(hwnd, ptCur.x + g_cxBorder, 
        ptCur.y + g_cyBorder + g_cyCaption + g_cyMenu); 
 
    g_fDragging = TRUE; 
 
    return TRUE; 
} 
```



### <a name="step-2-move-the-image"></a><span data-ttu-id="f01f0-123">步驟2：移動影像。</span><span class="sxs-lookup"><span data-stu-id="f01f0-123">Step 2: Move the image.</span></span>

<span data-ttu-id="f01f0-124">[**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove)函式會將影像移至新的位置。</span><span class="sxs-lookup"><span data-stu-id="f01f0-124">The [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function moves the image to a new location.</span></span>

<span data-ttu-id="f01f0-125">下列 c + + 程式碼範例中的使用者定義函數是為了回應 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息而呼叫的。</span><span class="sxs-lookup"><span data-stu-id="f01f0-125">The user-defined function in the following C++ code example is intended to be called in response to the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="f01f0-126">它會將影像拖曳至新的位置。</span><span class="sxs-lookup"><span data-stu-id="f01f0-126">It drags the image to a new location.</span></span>


```C++
// MoveTheImage - drags an image to the specified coordinates. 
// Returns TRUE if successful, or FALSE otherwise. 
// ptCur - new coordinates for the image. 
BOOL MoveTheImage(POINT ptCur) 
{ 
    if (!ImageList_DragMove(ptCur.x, ptCur.y)) 
        return FALSE; 
 
    return TRUE; 
} 

```



### <a name="step-3-end-the-drag-operation"></a><span data-ttu-id="f01f0-127">步驟3：結束拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="f01f0-127">Step 3: End the drag operation.</span></span>

<span data-ttu-id="f01f0-128">下列 c + + 程式碼範例中的使用者定義函數會呼叫 [**ImageList \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) 函式來結束拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="f01f0-128">The user-defined function in the following C++ code example calls the [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function to end the drag operation.</span></span> <span data-ttu-id="f01f0-129">然後，它會呼叫 [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) 函式來解除鎖定視窗，並隱藏拖曳影像，讓視窗得以更新。</span><span class="sxs-lookup"><span data-stu-id="f01f0-129">It then calls the [**ImageList\_DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) function to unlock the window and hide the drag image, allowing the window to be updated.</span></span>


```C++
// StopDragging - ends a drag operation and draws the image 
// at its final location. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// himl - handle to the image list. 
// ptCur - coordinates of the cursor. 
// 
// Global variable 
//     g_ptHotSpot - location of the image's hot spot. 
 
extern POINT g_ptHotSpot; 
 
BOOL StopDragging(HWND hwnd, HIMAGELIST himl, POINT ptCur) 
{ 
    ImageList_EndDrag(); 
    ImageList_DragLeave(hwnd); 
 
    g_fDragging = FALSE; 
 
    DrawTheImage(hwnd, himl, ptCur.x - g_ptHotSpot.x, 
        ptCur.y - g_ptHotSpot.y); 
 
    ReleaseCapture(); 
    return TRUE; 
} 

```



## <a name="related-topics"></a><span data-ttu-id="f01f0-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="f01f0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f01f0-131">影像清單參考</span><span class="sxs-lookup"><span data-stu-id="f01f0-131">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="f01f0-132">關於影像清單</span><span class="sxs-lookup"><span data-stu-id="f01f0-132">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="f01f0-133">使用影像清單</span><span class="sxs-lookup"><span data-stu-id="f01f0-133">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 