---
title: 如何處理下拉按鈕
description: 下拉式按鈕可以提供選項清單給使用者。
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103681601"
---
# <a name="how-to-handle-drop-down-buttons"></a><span data-ttu-id="addb7-103">如何處理下拉按鈕</span><span class="sxs-lookup"><span data-stu-id="addb7-103">How to Handle Drop-down Buttons</span></span>

<span data-ttu-id="addb7-104">下拉式按鈕可以提供選項清單給使用者。</span><span class="sxs-lookup"><span data-stu-id="addb7-104">A drop-down button can present users with a list of options.</span></span> <span data-ttu-id="addb7-105">若要建立此按鈕樣式，請指定 [ [**BTNS \_ ] 下拉式**](toolbar-control-and-button-styles.md) 樣式 (也稱為 [ [**TBSTYLE \_ ] 下拉式清單**](toolbar-control-and-button-styles.md) ，以相容于舊版的通用控制項) 。</span><span class="sxs-lookup"><span data-stu-id="addb7-105">To create this style of button, specify the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style (also called [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) for compatibility with previous versions of the common controls).</span></span> <span data-ttu-id="addb7-106">若要以箭號顯示下拉式按鈕，您也必須透過傳送 [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)訊息來設定 [**TBSTYLE \_ EX \_ DRAWDDARROWS**](toolbar-extended-styles.md)工具列樣式。</span><span class="sxs-lookup"><span data-stu-id="addb7-106">To show a drop-down button with an arrow, you must also set the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) toolbar style by sending a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span>

<span data-ttu-id="addb7-107">下圖顯示下拉式清單 [開啟] 按鈕，並開啟內容功能表，並顯示檔案清單。</span><span class="sxs-lookup"><span data-stu-id="addb7-107">The following illustration shows a drop-down "Open" button with the context menu open and showing a list of files.</span></span> <span data-ttu-id="addb7-108">在此範例中，工具列具有 [**TBSTYLE \_ EX \_ DRAWDDARROWS**](toolbar-extended-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="addb7-108">In this example, the toolbar has the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![對話方塊的螢幕擷取畫面，其中包含三個以圖示表示的工具列專案;其中一個具有展開的下拉箭號和三個專案的內容功能表](images/tb-dropdown.png)

<span data-ttu-id="addb7-110">下圖顯示相同的工具列，這次不含 [**TBSTYLE \_ EX \_ DRAWDDARROWS**](toolbar-extended-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="addb7-110">The following illustration shows the same toolbar, this time without the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![上一個對話方塊的螢幕擷取畫面，但內容功能表的圖示沒有下拉式箭號](images/tb-dropdown2.png)

<span data-ttu-id="addb7-112">當使用者按一下使用 [ [**BTNS \_ ] 下拉式**](toolbar-control-and-button-styles.md) 樣式的工具列按鈕時，工具列控制項會將 [TBN 的 \_ 下拉式](tbn-dropdown.md) 通知程式碼傳送給它的父視窗。</span><span class="sxs-lookup"><span data-stu-id="addb7-112">When users click a toolbar button that uses the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style, the toolbar control sends its parent window a [TBN\_DROPDOWN](tbn-dropdown.md) notification code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="addb7-113">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="addb7-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="addb7-114">技術</span><span class="sxs-lookup"><span data-stu-id="addb7-114">Technologies</span></span>

-   [<span data-ttu-id="addb7-115">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="addb7-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="addb7-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="addb7-116">Prerequisites</span></span>

-   <span data-ttu-id="addb7-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="addb7-117">C/C++</span></span>
-   <span data-ttu-id="addb7-118">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="addb7-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="addb7-119">指示</span><span class="sxs-lookup"><span data-stu-id="addb7-119">Instructions</span></span>

### <a name="handle-a-drop-down-button"></a><span data-ttu-id="addb7-120">處理下拉式按鈕</span><span class="sxs-lookup"><span data-stu-id="addb7-120">Handle a Drop-down Button</span></span>

<span data-ttu-id="addb7-121">下列程式碼範例會示範應用程式如何支援工具列控制項中的下拉式按鈕。</span><span class="sxs-lookup"><span data-stu-id="addb7-121">The following code example demonstrates how an application can support a drop-down button in a toolbar control.</span></span>


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="addb7-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="addb7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="addb7-123">使用工具列控制項</span><span class="sxs-lookup"><span data-stu-id="addb7-123">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="addb7-124">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="addb7-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




