---
title: 如何新增 List-View 資料行
description: 本主題示範如何將資料行加入至清單視圖控制項。
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee71065729502410d189493527af0e3e37663a4a2aaf541852454af7fa4a5aac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922078"
---
# <a name="how-to-add-list-view-columns"></a>如何新增 List-View 資料行

本主題示範如何將資料行加入至清單視圖控制項。 當清單視圖控制項位於報表 (詳細資料) 視圖時，會使用資料行來顯示專案和子專案。 選取之資料行中的文字也可以顯示在磚視圖中。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示


若要將資料行新增至清單視圖控制項，請傳送 [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) 訊息或使用 [**ListView \_ INSERTCOLUMN**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) 宏。 若要刪除資料行，請使用 [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) 訊息。

下列 c + + 程式碼範例會呼叫 [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) 宏，以將資料行加入至清單視圖控制項。 欄位標題會在應用程式的標頭檔中定義為字串資源，這些資源會從識別碼 FIRSTCOLUMN 開始連續編號 \_ 。 在標頭檔中，將資料行數目定義為 **C 資料 \_ 行**。


```C++
// InitListViewColumns: Adds columns to a list-view control.
// hWndListView:        Handle to the list-view control. 
// Returns TRUE if successful, and FALSE otherwise. 
BOOL InitListViewColumns(HWND hWndListView) 
{ 
    WCHAR szText[256];     // Temporary buffer.
    LVCOLUMN lvc;
    int iCol;

    // Initialize the LVCOLUMN structure.
    // The mask specifies that the format, width, text,
    // and subitem members of the structure are valid.
    lvc.mask = LVCF_FMT | LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM;

    // Add the columns.
    for (iCol = 0; iCol < C_COLUMNS; iCol++)
    {
        lvc.iSubItem = iCol;
        lvc.pszText = szText;
        lvc.cx = 100;               // Width of column in pixels.

        if ( iCol < 2 )
            lvc.fmt = LVCFMT_LEFT;  // Left-aligned column.
        else
            lvc.fmt = LVCFMT_RIGHT; // Right-aligned column.

        // Load the names of the column headings from the string resources.
        LoadString(g_hInst,
                   IDS_FIRSTCOLUMN + iCol,
                   szText,
                   sizeof(szText)/sizeof(szText[0]));

        // Insert the columns into the list view.
        if (ListView_InsertColumn(hWndListView, iCol, &lvc) == -1)
            return FALSE;
    }
    
    return TRUE;
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[清單視圖控制項參考](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[關於 List-View 控制項](list-view-controls-overview.md)
</dt> <dt>

[使用 List-View 控制項](using-list-view-controls.md)
</dt> </dl>

 

 




