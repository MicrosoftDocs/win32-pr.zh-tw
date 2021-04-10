---
title: 如何建立垂直工具列
description: 建立垂直工具列的關鍵是 \_ 在視窗樣式中包含垂直 CCS，以及為 \_ 每個按鈕設定 TBSTATE 換行樣式。
ms.assetid: C2EAB160-0D8D-4BB9-AD41-D5175FBE81AB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd32609e81196a94f4298197c33a4cc6e21d117
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103933026"
---
# <a name="how-to-create-vertical-toolbars"></a><span data-ttu-id="fb49b-103">如何建立垂直工具列</span><span class="sxs-lookup"><span data-stu-id="fb49b-103">How to Create Vertical Toolbars</span></span>

<span data-ttu-id="fb49b-104">建立垂直工具列的關鍵是在視窗樣式中 [**包含 \_ 垂直 CCS**](common-control-styles.md) ，以及為每個按鈕設定 [**TBSTATE \_ 換行**](toolbar-button-states.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="fb49b-104">The key to creating a vertical toolbar is to include [**CCS\_VERT**](common-control-styles.md) in the window style, and to set the [**TBSTATE\_WRAP**](toolbar-button-states.md) style for each button.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fb49b-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="fb49b-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fb49b-106">技術</span><span class="sxs-lookup"><span data-stu-id="fb49b-106">Technologies</span></span>

-   [<span data-ttu-id="fb49b-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="fb49b-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fb49b-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="fb49b-108">Prerequisites</span></span>

-   <span data-ttu-id="fb49b-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="fb49b-109">C/C++</span></span>
-   <span data-ttu-id="fb49b-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="fb49b-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fb49b-111">指示</span><span class="sxs-lookup"><span data-stu-id="fb49b-111">Instructions</span></span>

### <a name="create-a-vertical-toolbar"></a><span data-ttu-id="fb49b-112">建立垂直工具列</span><span class="sxs-lookup"><span data-stu-id="fb49b-112">Create a Vertical Toolbar</span></span>

<span data-ttu-id="fb49b-113">下列範例程式碼會建立如下圖所示的垂直工具列。</span><span class="sxs-lookup"><span data-stu-id="fb49b-113">The following example code creates the vertical toolbar shown in the following illustration.</span></span>

![顯示對話方塊的螢幕擷取畫面，其中有三個以垂直方式排列的工具列專案，其中每個都只有一個圖示](images/tb-vertical.png)


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateVerticalToolbar(HWND hWndParent)
{
    // Define the buttons.
    // IDM_NEW, IDM_0PEN, and IDM_SAVE are application-defined command IDs.
    
    TBBUTTON tbButtons3[numButtons] = 
    {
        {STD_FILENEW,  IDM_NEW,  TBSTATE_ENABLED | TBSTATE_WRAP, BTNS_BUTTON, {0}, 0L, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED | TBSTATE_WRAP, BTNS_BUTTON, {0}, 0L, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED | TBSTATE_WRAP, BTNS_BUTTON, {0}, 0L, 0}
    };

    // Create the toolbar window.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | WS_VISIBLE | CCS_VERT | WS_BORDER, 0, 0, 0, 0,
                                      hWndParent, NULL, g_hInst, NULL);

    // Create the image list.
    g_hImageList = ImageList_Create(24, 24,                   // Dimensions of individual bitmaps.  
                                    ILC_COLOR16 | ILC_MASK,   // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 0, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_LARGE_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add them to the toolbar.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE,       (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)&tbButtons3);

    return hWndToolbar;
} 
```



## <a name="related-topics"></a><span data-ttu-id="fb49b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb49b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb49b-116">使用工具列控制項</span><span class="sxs-lookup"><span data-stu-id="fb49b-116">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="fb49b-117">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="fb49b-117">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




