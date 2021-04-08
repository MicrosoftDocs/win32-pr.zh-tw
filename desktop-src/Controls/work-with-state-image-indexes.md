---
title: 如何使用狀態影像索引
description: 通常會對如何在樹狀檢視控制項中設定和取出狀態影像索引產生混淆。
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103681455"
---
# <a name="how-to-work-with-state-image-indexes"></a><span data-ttu-id="32760-103">如何使用狀態影像索引</span><span class="sxs-lookup"><span data-stu-id="32760-103">How to Work With State Image Indexes</span></span>

<span data-ttu-id="32760-104">通常會對如何在樹狀檢視控制項中設定和取出狀態影像索引產生混淆。</span><span class="sxs-lookup"><span data-stu-id="32760-104">There is often confusion about how to set and retrieve the state image index in a tree-view control.</span></span> <span data-ttu-id="32760-105">下列範例示範設定和抓取狀態影像索引的適當方法。</span><span class="sxs-lookup"><span data-stu-id="32760-105">The following examples demonstrate the proper method for setting and retrieving the state image index.</span></span> <span data-ttu-id="32760-106">這些範例假設樹狀檢視控制項中只有兩個狀態影像索引，未核取並核取。</span><span class="sxs-lookup"><span data-stu-id="32760-106">The examples assume that there are only two state image indexes in the tree-view control, unchecked and checked.</span></span> <span data-ttu-id="32760-107">如果您的應用程式包含兩個以上的應用程式，則必須修改這些函式來處理該案例。</span><span class="sxs-lookup"><span data-stu-id="32760-107">If your application contains more than two, these functions will need to be modified to handle that case.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="32760-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="32760-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="32760-109">技術</span><span class="sxs-lookup"><span data-stu-id="32760-109">Technologies</span></span>

-   [<span data-ttu-id="32760-110">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="32760-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="32760-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="32760-111">Prerequisites</span></span>

-   <span data-ttu-id="32760-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="32760-112">C/C++</span></span>
-   <span data-ttu-id="32760-113">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="32760-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="32760-114">指示</span><span class="sxs-lookup"><span data-stu-id="32760-114">Instructions</span></span>

### <a name="set-a-tree-view-items-check-state"></a><span data-ttu-id="32760-115">設定 Tree-View 專案的檢查狀態</span><span class="sxs-lookup"><span data-stu-id="32760-115">Set a Tree-View Item's Check State</span></span>

<span data-ttu-id="32760-116">下列範例示範如何設定樹狀檢視專案的檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="32760-116">The following example demonstrates how to set a tree-view item's check state.</span></span>


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



### <a name="retrieve-a-tree-view-items-check-state"></a><span data-ttu-id="32760-117">取得 Tree-View 專案的檢查狀態</span><span class="sxs-lookup"><span data-stu-id="32760-117">Retrieve a Tree-View Item's Check State</span></span>

<span data-ttu-id="32760-118">下列範例示範如何取出樹狀檢視專案的檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="32760-118">The following example demonstrates how to retrieve a tree-view item's check state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="32760-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="32760-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32760-120">使用 Tree-View 控制項</span><span class="sxs-lookup"><span data-stu-id="32760-120">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="32760-121">CustDTv 範例說明 Tree-View 控制項中的自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="32760-121">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




