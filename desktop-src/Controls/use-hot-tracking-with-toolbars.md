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
# <a name="how-to-use-hot-tracking-with-toolbars"></a>如何搭配使用 Hot-Tracking 與工具列

當滑鼠指標停留在專案上時，專案會變成經常性存取。 如果啟用熱追蹤，則會反白顯示熱專案。 使用 [**TBSTYLE \_ 平面**](toolbar-control-and-button-styles.md) 樣式建立的工具列，或使用 [視覺化樣式](themes-overview.md)的工具列，預設支援熱追蹤。

熱追蹤需要您建立映射清單;因此，您無法使用 [**TB 的 \_ ADDBITMAP**](tb-addbitmap.md) 訊息或 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) 函式來建立您的工具列。

當滑鼠停留在工具列按鈕上時，會將按鈕標示為反白顯示。 下圖顯示已啟用熱追蹤的工具列;拍攝螢幕擷取畫面時，滑鼠指標會停留在 [儲存] 按鈕上。

![包含三個專案工具列之對話方塊的螢幕擷取畫面;已列出選取的圖示](images/tb-withstyles.png)

如果您想要在控制項的狀態變更時變更工具列按鈕點陣圖，請將不同的影像儲存在 [影像清單](image-lists.md)中。 例如，有些應用程式在選取時，會有黑色和白色的工具列按鈕。 這兩個不同的影像會儲存在影像清單中。 工具列支援最多使用三個影像清單。 應用程式通常會有預設、已停用和熱追蹤的影像清單。 若要設定及抓取熱門工具列按鈕的影像清單，請使用 [**tb \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) 和 [**tb \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) 訊息。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-hot-tracking-with-a-toolbar"></a>搭配使用 Hot-Tracking 與工具列

下列程式碼範例會建立、填滿及指派熱按鈕的影像清單。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具列控制項](using-toolbar-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




