---
title: 如何使用狀態影像索引
description: 通常會對如何在樹狀檢視控制項中設定和取出狀態影像索引產生混淆。
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04504019f79a388b6c21f940724de884d8516263daf6d410a841a96fc2e557b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059298"
---
# <a name="how-to-work-with-state-image-indexes"></a>如何使用狀態影像索引

通常會對如何在樹狀檢視控制項中設定和取出狀態影像索引產生混淆。 下列範例示範設定和抓取狀態影像索引的適當方法。 這些範例假設樹狀檢視控制項中只有兩個狀態影像索引，未核取並核取。 如果您的應用程式包含兩個以上的應用程式，則必須修改這些函式來處理該案例。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="set-a-tree-view-items-check-state"></a>設定 Tree-View 專案的檢查狀態

下列範例示範如何設定樹狀檢視專案的檢查狀態。


```C++
  BOOL TreeView_SetCheckState(HWND hwndTreeView, HTREEITEM hItem, BOOL fCheck)
  {
      TVITEM tvItem;

      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Image 1 in the tree-view check box image list is the unchecked box. 
      // Image 2 is the checked box.

      tvItem.state = INDEXTOSTATEIMAGEMASK((fCheck ? 2 : 1));

      return TreeView_SetItem(hwndTreeView, &tvItem);
  }
```



### <a name="retrieve-a-tree-view-items-check-state"></a>取得 Tree-View 專案的檢查狀態

下列範例示範如何取出樹狀檢視專案的檢查狀態。


```C++
  BOOL TreeView_GetCheckState(HWND hwndTreeView, HTREEITEM hItem)
  {
      TVITEM tvItem;

      // Prepare to receive the desired information.
      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Request the information.
      TreeView_GetItem(hwndTreeView, &tvItem);

      // Return zero if it's not checked, or nonzero otherwise.
      return ((BOOL)(tvItem.state >> 12) - 1);
  }
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Tree-View 控制項](using-treeview.md)
</dt> <dt>

[CustDTv 範例說明 Tree-View 控制項中的自訂繪圖](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




