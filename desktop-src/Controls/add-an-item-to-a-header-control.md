---
title: 如何將專案加入至標題控制項
description: 本主題示範如何將專案加入至標題控制項。
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933741"
---
# <a name="how-to-add-an-item-to-a-header-control"></a>如何將專案加入至標題控制項

本主題示範如何將專案加入至標題控制項。 標題控制項通常會有數個定義控制項資料行的標頭專案。 您可以藉由將 [**HDM \_ INSERTITEM**](hdm-insertitem.md) 訊息傳送至控制項，將專案加入至標題控制項。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


使用 [**HDM \_ INSERTITEM**](hdm-insertitem.md) 訊息，將專案加入至標題控制項。 訊息必須包含 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構的位址。 此結構會定義標頭專案的屬性，其中可包括字串、點陣圖影像、初始大小，以及應用程式定義的32位值。

下列範例說明如何使用 [**HDM \_ INSERTITEM**](hdm-insertitem.md) 訊息和 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構，將專案加入至標題控制項。 新的專案是由在專案矩形內靠左對齊的字串所組成。



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於標題控制項](header-controls.md)
</dt> <dt>

[標題控制項參考](bumper-header-control-header-control-reference.md)
</dt> <dt>

[使用標題控制項](using-header-controls.md)
</dt> </dl>

 

 




