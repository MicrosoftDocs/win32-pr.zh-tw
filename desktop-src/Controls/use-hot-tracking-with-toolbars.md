---
title: 如何搭配使用 Hot-Tracking 與工具列
description: 當滑鼠指標停留在專案上時，專案會變成經常性存取。 如果啟用熱追蹤，則會反白顯示熱專案。 使用 TBSTYLE 平面樣式建立的工具列 \_ ，或使用視覺化樣式的工具列，預設支援熱追蹤。
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "104023194"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a><span data-ttu-id="c7717-105">如何搭配使用 Hot-Tracking 與工具列</span><span class="sxs-lookup"><span data-stu-id="c7717-105">How to Use Hot-Tracking with Toolbars</span></span>

<span data-ttu-id="c7717-106">當滑鼠指標停留在專案上時，專案會變成經常性存取。</span><span class="sxs-lookup"><span data-stu-id="c7717-106">When a mouse pointer hovers over an item, the item becomes hot.</span></span> <span data-ttu-id="c7717-107">如果啟用熱追蹤，則會反白顯示熱專案。</span><span class="sxs-lookup"><span data-stu-id="c7717-107">If hot-tracking is enabled, the hot item is highlighted.</span></span> <span data-ttu-id="c7717-108">使用 [**TBSTYLE \_ 平面**](toolbar-control-and-button-styles.md) 樣式建立的工具列，或使用 [視覺化樣式](themes-overview.md)的工具列，預設支援熱追蹤。</span><span class="sxs-lookup"><span data-stu-id="c7717-108">A toolbar that is created with the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style, or one that uses [Visual Styles](themes-overview.md), supports hot-tracking by default.</span></span>

<span data-ttu-id="c7717-109">熱追蹤需要您建立映射清單;因此，您無法使用 [**TB 的 \_ ADDBITMAP**](tb-addbitmap.md) 訊息或 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) 函式來建立您的工具列。</span><span class="sxs-lookup"><span data-stu-id="c7717-109">Hot-tracking requires that you create image lists; therefore, you cannot use the [**TB\_ADDBITMAP**](tb-addbitmap.md) message or the [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function to create your toolbar.</span></span>

<span data-ttu-id="c7717-110">當滑鼠停留在工具列按鈕上時，會將按鈕標示為反白顯示。</span><span class="sxs-lookup"><span data-stu-id="c7717-110">When the mouse hovers over a toolbar button, the button is outlined to highlight it.</span></span> <span data-ttu-id="c7717-111">下圖顯示已啟用熱追蹤的工具列;拍攝螢幕擷取畫面時，滑鼠指標會停留在 [儲存] 按鈕上。</span><span class="sxs-lookup"><span data-stu-id="c7717-111">The following illustration shows a toolbar with hot-tracking enabled; the mouse pointer was hovering on the Save button when the screen shot was taken.</span></span>

![包含三個專案工具列之對話方塊的螢幕擷取畫面;已列出選取的圖示](images/tb-withstyles.png)

<span data-ttu-id="c7717-113">如果您想要在控制項的狀態變更時變更工具列按鈕點陣圖，請將不同的影像儲存在 [影像清單](image-lists.md)中。</span><span class="sxs-lookup"><span data-stu-id="c7717-113">If you want a toolbar button bitmap to change when the state of the control changes, store the different images in [image lists](image-lists.md).</span></span> <span data-ttu-id="c7717-114">例如，有些應用程式在選取時，會有黑色和白色的工具列按鈕。</span><span class="sxs-lookup"><span data-stu-id="c7717-114">For example, some applications have black and white toolbar buttons that become colored when they are selected.</span></span> <span data-ttu-id="c7717-115">這兩個不同的影像會儲存在影像清單中。</span><span class="sxs-lookup"><span data-stu-id="c7717-115">The two different images are stored in image lists.</span></span> <span data-ttu-id="c7717-116">工具列支援最多使用三個影像清單。</span><span class="sxs-lookup"><span data-stu-id="c7717-116">Toolbars support using up to three image lists.</span></span> <span data-ttu-id="c7717-117">應用程式通常會有預設、已停用和熱追蹤的影像清單。</span><span class="sxs-lookup"><span data-stu-id="c7717-117">Typically an application has a default, disabled, and hot-tracking list of images.</span></span> <span data-ttu-id="c7717-118">若要設定及抓取熱門工具列按鈕的影像清單，請使用 [**tb \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) 和 [**tb \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="c7717-118">To set and retrieve image lists for hot toolbar buttons, use the [**TB\_SETHOTIMAGELIST**](tb-sethotimagelist.md) and [**TB\_GETHOTIMAGELIST**](tb-gethotimagelist.md) messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c7717-119">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="c7717-119">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c7717-120">技術</span><span class="sxs-lookup"><span data-stu-id="c7717-120">Technologies</span></span>

-   [<span data-ttu-id="c7717-121">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="c7717-121">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c7717-122">必要條件</span><span class="sxs-lookup"><span data-stu-id="c7717-122">Prerequisites</span></span>

-   <span data-ttu-id="c7717-123">C/C++</span><span class="sxs-lookup"><span data-stu-id="c7717-123">C/C++</span></span>
-   <span data-ttu-id="c7717-124">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="c7717-124">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c7717-125">指示</span><span class="sxs-lookup"><span data-stu-id="c7717-125">Instructions</span></span>

### <a name="use-hot-tracking-with-a-toolbar"></a><span data-ttu-id="c7717-126">搭配使用 Hot-Tracking 與工具列</span><span class="sxs-lookup"><span data-stu-id="c7717-126">Use Hot-Tracking with a Toolbar</span></span>

<span data-ttu-id="c7717-127">下列程式碼範例會建立、填滿及指派熱按鈕的影像清單。</span><span class="sxs-lookup"><span data-stu-id="c7717-127">The following code example creates, fills, and assigns an image list for hot buttons.</span></span>


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a><span data-ttu-id="c7717-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7717-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7717-129">使用工具列控制項</span><span class="sxs-lookup"><span data-stu-id="c7717-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="c7717-130">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="c7717-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




