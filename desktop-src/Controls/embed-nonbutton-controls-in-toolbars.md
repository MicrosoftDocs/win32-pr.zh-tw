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
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a>如何在工具列中內嵌 Nonbutton 控制項

工具列僅支援按鈕;因此，如果您的應用程式需要不同類型的控制項，您必須建立子視窗。 下圖顯示具有內嵌編輯控制項的工具列。

![在工具列中具有編輯控制項之對話方塊的螢幕擷取畫面，上述三個工具列圖示](images/tb-withedit.png)

> [!Note]  
> 請考慮使用 [Rebar 控制項](rebar-controls.md) ，而不是將控制項放在工具列中。

 

任何類型的視窗都可以放在工具列上。 下列程式碼範例會將編輯控制項新增為工具列控制項視窗的子系。 因為已建立工具列，然後加入編輯控制項，所以您必須提供編輯控制項的空間。 其中一個方法是在工具列中新增分隔符號做為預留位置，將分隔符號的寬度設定為您要保留的圖元數。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a>在工具列中內嵌 Nonbutton 控制項

下列程式碼片段會建立上圖中的工具列。


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



此範例會將子視窗的維度硬式編碼;不過，若要建立更健全的應用程式，請判斷工具列的大小，並讓編輯控制項視窗符合。

您可能想要編輯控制項通知移至另一個視窗，例如工具列的父代。 若要這樣做，請將編輯控制項建立為工具列父視窗的子系。 然後，將編輯控制項的父系變更為工具列，如下所示。


```
SetParent (hWndEdit, hWndToolbar);
```



通知會移至原始父系。 因此，即使編輯視窗位於工具列視窗中，編輯控制項訊息仍會移至工具列的父系。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具列控制項](using-toolbar-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




