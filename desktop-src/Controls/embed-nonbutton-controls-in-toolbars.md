---
title: 如何在工具列中內嵌 Nonbutton 控制項
description: 工具列僅支援按鈕;因此，如果您的應用程式需要不同類型的控制項，您必須建立子視窗。 下圖顯示具有內嵌編輯控制項的工具列。
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841988"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a><span data-ttu-id="a3495-104">如何在工具列中內嵌 Nonbutton 控制項</span><span class="sxs-lookup"><span data-stu-id="a3495-104">How to Embed Nonbutton Controls in Toolbars</span></span>

<span data-ttu-id="a3495-105">工具列僅支援按鈕;因此，如果您的應用程式需要不同類型的控制項，您必須建立子視窗。</span><span class="sxs-lookup"><span data-stu-id="a3495-105">Toolbars support only buttons; therefore, if your application requires a different kind of control, you must create a child window.</span></span> <span data-ttu-id="a3495-106">下圖顯示具有內嵌編輯控制項的工具列。</span><span class="sxs-lookup"><span data-stu-id="a3495-106">The following illustration shows a toolbar with an embedded edit control.</span></span>

![在工具列中具有編輯控制項之對話方塊的螢幕擷取畫面，上述三個工具列圖示](images/tb-withedit.png)

> [!Note]  
> <span data-ttu-id="a3495-108">請考慮使用 [Rebar 控制項](rebar-controls.md) ，而不是將控制項放在工具列中。</span><span class="sxs-lookup"><span data-stu-id="a3495-108">Consider using [Rebar Controls](rebar-controls.md) instead of placing controls in toolbars.</span></span>

 

<span data-ttu-id="a3495-109">任何類型的視窗都可以放在工具列上。</span><span class="sxs-lookup"><span data-stu-id="a3495-109">Any type of window can be placed on a toolbar.</span></span> <span data-ttu-id="a3495-110">下列程式碼範例會將編輯控制項新增為工具列控制項視窗的子系。</span><span class="sxs-lookup"><span data-stu-id="a3495-110">The following example code adds an edit control as a child of the toolbar control window.</span></span> <span data-ttu-id="a3495-111">因為已建立工具列，然後加入編輯控制項，所以您必須提供編輯控制項的空間。</span><span class="sxs-lookup"><span data-stu-id="a3495-111">Because the toolbar is created and then the edit control added, you must provide space for the edit control.</span></span> <span data-ttu-id="a3495-112">其中一個方法是在工具列中新增分隔符號做為預留位置，將分隔符號的寬度設定為您要保留的圖元數。</span><span class="sxs-lookup"><span data-stu-id="a3495-112">One way to do this is to add a separator as a placeholder in the toolbar, setting the width of the separator to the number of pixels you want to reserve.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a3495-113">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="a3495-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a3495-114">技術</span><span class="sxs-lookup"><span data-stu-id="a3495-114">Technologies</span></span>

-   [<span data-ttu-id="a3495-115">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="a3495-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a3495-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="a3495-116">Prerequisites</span></span>

-   <span data-ttu-id="a3495-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="a3495-117">C/C++</span></span>
-   <span data-ttu-id="a3495-118">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="a3495-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a3495-119">指示</span><span class="sxs-lookup"><span data-stu-id="a3495-119">Instructions</span></span>

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a><span data-ttu-id="a3495-120">在工具列中內嵌 Nonbutton 控制項</span><span class="sxs-lookup"><span data-stu-id="a3495-120">Embed a Nonbutton Control in a Toolbar</span></span>

<span data-ttu-id="a3495-121">下列程式碼片段會建立上圖中的工具列。</span><span class="sxs-lookup"><span data-stu-id="a3495-121">The following code snippet creates the toolbar in the preceding illustration.</span></span>


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



<span data-ttu-id="a3495-122">此範例會將子視窗的維度硬式編碼;不過，若要建立更健全的應用程式，請判斷工具列的大小，並讓編輯控制項視窗符合。</span><span class="sxs-lookup"><span data-stu-id="a3495-122">This example hard-codes the dimensions of the child window; however, to make a more robust application, determine the size of the toolbar and make the edit control window to fit.</span></span>

<span data-ttu-id="a3495-123">您可能想要編輯控制項通知移至另一個視窗，例如工具列的父代。</span><span class="sxs-lookup"><span data-stu-id="a3495-123">You might want the edit control notifications to go to another window, such as the toolbar's parent.</span></span> <span data-ttu-id="a3495-124">若要這樣做，請將編輯控制項建立為工具列父視窗的子系。</span><span class="sxs-lookup"><span data-stu-id="a3495-124">To do this, create the edit control as a child of the toolbar's parent window.</span></span> <span data-ttu-id="a3495-125">然後，將編輯控制項的父系變更為工具列，如下所示。</span><span class="sxs-lookup"><span data-stu-id="a3495-125">Then change the parent of the edit control to the toolbar as follows.</span></span>


```
SetParent (hWndEdit, hWndToolbar);
```



<span data-ttu-id="a3495-126">通知會移至原始父系。</span><span class="sxs-lookup"><span data-stu-id="a3495-126">Notifications go to the original parent.</span></span> <span data-ttu-id="a3495-127">因此，即使編輯視窗位於工具列視窗中，編輯控制項訊息仍會移至工具列的父系。</span><span class="sxs-lookup"><span data-stu-id="a3495-127">Therefore, the edit control messages go to the parent of the toolbar even though the edit window resides in the toolbar window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3495-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3495-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3495-129">使用工具列控制項</span><span class="sxs-lookup"><span data-stu-id="a3495-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="a3495-130">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="a3495-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




