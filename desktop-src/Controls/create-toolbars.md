---
title: 如何建立工具列
description: 若要建立工具列，請使用 CreateWindowEx 函數，並指定 TOOLBARCLASSNAME 視窗類別。
ms.assetid: 5D060291-6ACF-478C-97EC-CD8BD55D1FFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69cd40338eaebc0d9de852519dce34dc9bc8aa4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683136"
---
# <a name="how-to-create-toolbars"></a><span data-ttu-id="097a2-103">如何建立工具列</span><span class="sxs-lookup"><span data-stu-id="097a2-103">How to Create Toolbars</span></span>

<span data-ttu-id="097a2-104">若要建立工具列，請使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數，並指定 [**TOOLBARCLASSNAME**](common-control-window-classes.md) 視窗類別。</span><span class="sxs-lookup"><span data-stu-id="097a2-104">To create a toolbar, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**TOOLBARCLASSNAME**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="097a2-105">產生的工具列一開始不會包含任何按鈕。</span><span class="sxs-lookup"><span data-stu-id="097a2-105">The resulting toolbar initially contains no buttons.</span></span> <span data-ttu-id="097a2-106">使用 [**tb \_ ADDBUTTONS**](tb-addbuttons.md) 或 [**tb \_ INSERTBUTTON**](tb-insertbutton.md) 訊息，將按鈕新增至工具列。</span><span class="sxs-lookup"><span data-stu-id="097a2-106">Add buttons to the toolbar by using the [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) message.</span></span> <span data-ttu-id="097a2-107">在所有專案和字串都插入控制項之後，您必須傳送 [**TB 的 \_ AUTOSIZE**](tb-autosize.md) 訊息，讓工具列根據其內容重新計算其大小。</span><span class="sxs-lookup"><span data-stu-id="097a2-107">You must send the [**TB\_AUTOSIZE**](tb-autosize.md) message after all the items and strings have been inserted into the control, to cause the toolbar to recalculate its size based on its content.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="097a2-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="097a2-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="097a2-109">技術</span><span class="sxs-lookup"><span data-stu-id="097a2-109">Technologies</span></span>

-   [<span data-ttu-id="097a2-110">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="097a2-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="097a2-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="097a2-111">Prerequisites</span></span>

-   <span data-ttu-id="097a2-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="097a2-112">C/C++</span></span>
-   <span data-ttu-id="097a2-113">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="097a2-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="097a2-114">指示</span><span class="sxs-lookup"><span data-stu-id="097a2-114">Instructions</span></span>

### <a name="create-a-toolbar"></a><span data-ttu-id="097a2-115">建立工具列</span><span class="sxs-lookup"><span data-stu-id="097a2-115">Create a Toolbar</span></span>

<span data-ttu-id="097a2-116">下列範例程式碼會使用標準系統圖示來建立圖例中所示的工具列。</span><span class="sxs-lookup"><span data-stu-id="097a2-116">The following example code creates the toolbar shown in the illustration, using standard system icons.</span></span> <span data-ttu-id="097a2-117">[ **儲存** ] 按鈕一開始是停用的。</span><span class="sxs-lookup"><span data-stu-id="097a2-117">The **Save** button is initially disabled.</span></span>

![顯示具有三個工具列專案水準排列之對話方塊的螢幕擷取畫面，其中每個專案都有一個圖示和一個文字標籤](images/tb-codesample1.png)


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateSimpleToolbar(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0, 
                                      hWndParent, NULL, g_hInst, NULL);
        
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize,   // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK,   // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, (INT_PTR)L"Save"}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



<span data-ttu-id="097a2-119">下列範例會以類似的方式建立相同的工具列，但在此情況下，會從資源讀取字串。</span><span class="sxs-lookup"><span data-stu-id="097a2-119">The following example creates the same toolbar in much the same way, but in this case, the strings are read from a resource.</span></span>


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarFromResource(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0,
                                      hWndParent, NULL, g_hInst, NULL);
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK, // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Load the text from a resource.
    
    // In the string table, the text for all buttons is a single entry that 
    // appears as "~New~Open~Save~~". The separator character is arbitrary, 
    // but it must appear as the first character of the string. The message 
    // returns the index of the first item, and the items are numbered 
    // consecutively.
    
    int iNew = SendMessage(hWndToolbar, TB_ADDSTRING, 
                           (WPARAM)g_hInst, (LPARAM)IDS_NEW); 
 
    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew + 1},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, iNew + 2}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



## <a name="related-topics"></a><span data-ttu-id="097a2-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="097a2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="097a2-121">使用工具列控制項</span><span class="sxs-lookup"><span data-stu-id="097a2-121">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="097a2-122">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="097a2-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 