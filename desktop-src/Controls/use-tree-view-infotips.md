---
title: 如何使用 Tree-View 提示
description: 當您將電視資料提示 \_ 樣式套用至樹狀檢視控制項時， \_ 當游標位於樹狀檢視中的專案上方時，它會產生 izdebski GETINFOTIP 通知。 藉由回應此通知，您可以設定出現在提示中的文字。
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0ef862d68cfd9f6ac5a97e82c80622e9c02121
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "106968482"
---
# <a name="how-to-use-tree-view-infotips"></a><span data-ttu-id="ac7ea-104">如何使用 Tree-View 提示</span><span class="sxs-lookup"><span data-stu-id="ac7ea-104">How to Use Tree-View Infotips</span></span>

<span data-ttu-id="ac7ea-105">當您將 [**電視資料 \_**](tree-view-control-window-styles.md) 提示樣式套用至樹狀檢視控制項時，當游標位於樹狀檢視中的專案上方時，它會產生 [izdebski \_ GETINFOTIP](tvn-getinfotip.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="ac7ea-105">When you apply the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style to a tree-view control, it generates [TVN\_GETINFOTIP](tvn-getinfotip.md) notifications when the cursor is over an item in the tree view.</span></span> <span data-ttu-id="ac7ea-106">藉由回應此通知，您可以設定出現在提示中的文字。</span><span class="sxs-lookup"><span data-stu-id="ac7ea-106">By responding to this notification, you can set the text that appears in the infotip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ac7ea-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="ac7ea-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ac7ea-108">技術</span><span class="sxs-lookup"><span data-stu-id="ac7ea-108">Technologies</span></span>

-   [<span data-ttu-id="ac7ea-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="ac7ea-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ac7ea-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="ac7ea-110">Prerequisites</span></span>

-   <span data-ttu-id="ac7ea-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="ac7ea-111">C/C++</span></span>
-   <span data-ttu-id="ac7ea-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="ac7ea-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ac7ea-113">指示</span><span class="sxs-lookup"><span data-stu-id="ac7ea-113">Instructions</span></span>

### <a name="use-tree-view-infotips"></a><span data-ttu-id="ac7ea-114">使用 Tree-View 提示</span><span class="sxs-lookup"><span data-stu-id="ac7ea-114">Use Tree-View Infotips</span></span>

<span data-ttu-id="ac7ea-115">下列範例程式碼顯示應用程式可能會如何回應通知。</span><span class="sxs-lookup"><span data-stu-id="ac7ea-115">The following example code shows how an application might respond to the notification.</span></span> <span data-ttu-id="ac7ea-116">為了簡單起見，此範例只會將專案的文字複製到提示。</span><span class="sxs-lookup"><span data-stu-id="ac7ea-116">For simplicity, the example just copies the text for the item to the infotip.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ac7ea-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac7ea-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac7ea-118">使用 Tree-View 控制項</span><span class="sxs-lookup"><span data-stu-id="ac7ea-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="ac7ea-119">CustDTv 範例說明 Tree-View 控制項中的自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="ac7ea-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




