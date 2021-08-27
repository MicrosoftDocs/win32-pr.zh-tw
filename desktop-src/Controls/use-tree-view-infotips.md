---
title: 如何使用 Tree-View 提示
description: 當您將電視資料提示 \_ 樣式套用至樹狀檢視控制項時， \_ 當游標位於樹狀檢視中的專案上方時，它會產生 izdebski GETINFOTIP 通知。 藉由回應此通知，您可以設定出現在提示中的文字。
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff9273b28b614e7935f6ac507288a5733271fb455a6be1e85b52c5b0ba8bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132028"
---
# <a name="how-to-use-tree-view-infotips"></a>如何使用 Tree-View 提示

當您將 [**電視資料 \_**](tree-view-control-window-styles.md) 提示樣式套用至樹狀檢視控制項時，當游標位於樹狀檢視中的專案上方時，它會產生 [izdebski \_ GETINFOTIP](tvn-getinfotip.md) 通知。 藉由回應此通知，您可以設定出現在提示中的文字。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-tree-view-infotips"></a>使用 Tree-View 提示

下列範例程式碼顯示應用程式可能會如何回應通知。 為了簡單起見，此範例只會將專案的文字複製到提示。


```
  case WM_NOTIFY:
    switch (((LPNMHDR) lParam)->code)
    {
    case TVN_GETINFOTIP:
        {
          LPNMTVGETINFOTIP pTip = (LPNMTVGETINFOTIP)lParam;
          HWND hTree            = GetDlgItem(hDlg, IDC_TREE1);
          HTREEITEM item        = pTip->hItem;

          // Get the text for the item.
          TVITEM tvitem;
          tvitem.mask       = TVIF_TEXT;
          tvitem.hItem      = item;
          TCHAR temp[1024];
          tvitem.pszText    = infoTipBuf;
          tvitem.cchTextMax = sizeof(temp) / sizeof(TCHAR);
          TreeView_GetItem(hTree, &tvitem);

          // Copy the text to the infotip.
          wcscpy_s(pTip->pszText, pTip->cchTextMax, tvitem.pszText);
          break;
        }
      }
      return TRUE;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Tree-View 控制項](using-treeview.md)
</dt> <dt>

[CustDTv 範例說明 Tree-View 控制項中的自訂繪圖](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




