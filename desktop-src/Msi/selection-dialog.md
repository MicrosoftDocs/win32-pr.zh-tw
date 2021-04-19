---
description: 這個強制回應對話方塊可讓使用者選取特定的專案。
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: 選取對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989083"
---
# <a name="selection-dialog"></a><span data-ttu-id="c750c-103">選取對話方塊</span><span class="sxs-lookup"><span data-stu-id="c750c-103">Selection Dialog</span></span>

<span data-ttu-id="c750c-104">這個強制回應對話方塊可讓使用者選取特定的專案。</span><span class="sxs-lookup"><span data-stu-id="c750c-104">This modal dialog box enables users to select particular items.</span></span>

<span data-ttu-id="c750c-105">[選取範圍] 對話方塊包含發佈數個事件的 [SelectionTree 控制項](selectiontree-control.md) 。</span><span class="sxs-lookup"><span data-stu-id="c750c-105">A Selection Dialog box contains a [SelectionTree control](selectiontree-control.md) that publishes several ControlEvents.</span></span> <span data-ttu-id="c750c-106">這些工作通常是由 [文字](text-control.md)、 [圖示](icon-control.md)或 [點陣圖](bitmap-control.md) 控制項所訂閱，這些控制項會顯示描述、大小、路徑，以及反白顯示專案的圖示。</span><span class="sxs-lookup"><span data-stu-id="c750c-106">Commonly these ControlEvents are subscribed to by [Text](text-control.md), [Icon](icon-control.md), or [Bitmap](bitmap-control.md) controls that display a description, the size, the path, and the icon of the highlighted item.</span></span>

<span data-ttu-id="c750c-107">對話方塊上有一個可發佈[SelectionBrowse ControlEvent](selectionbrowse-controlevent.md)並產生[流覽對話方塊](browse-dialog.md)的[按鈕控制項](pushbutton-control.md)。</span><span class="sxs-lookup"><span data-stu-id="c750c-107">There is a [PushButton control](pushbutton-control.md) on the dialog box that publishes the [SelectionBrowse ControlEvent](selectionbrowse-controlevent.md) and spawns a [Browse Dialog](browse-dialog.md).</span></span> <span data-ttu-id="c750c-108">流覽控制項可讓使用者選取目錄。</span><span class="sxs-lookup"><span data-stu-id="c750c-108">The Browse control enables the user to select a directory.</span></span>

<span data-ttu-id="c750c-109">只有在呼叫 [CostInitialize 動作](costinitialize-action.md) 和 [CostFinalize 動作](costfinalize-action.md) 之後，才會填入選取樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="c750c-109">The selection tree is populated only after the [CostInitialize action](costinitialize-action.md) and [CostFinalize action](costfinalize-action.md) are called.</span></span>

<span data-ttu-id="c750c-110">選取專案對話方塊通常用來選取功能。</span><span class="sxs-lookup"><span data-stu-id="c750c-110">A Selection dialog box is commonly used to select features.</span></span> <span data-ttu-id="c750c-111">這些功能會列為 SelectionTree 控制項中的專案，並使用 [功能資料表](feature-table.md)的 [標題] 資料行中顯示的簡短文字字串標示。</span><span class="sxs-lookup"><span data-stu-id="c750c-111">The features are listed as items in a SelectionTree control and labeled with the short string of text appearing in the Title column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="c750c-112">功能資料表的 [描述] 資料行中的文字字串會以 [SelectionDescription ControlEvent](selectiondescription-controlevent.md) 的形式發佈，並由 [選取範圍] 對話方塊中的 [文字控制項](text-control.md) 顯示。</span><span class="sxs-lookup"><span data-stu-id="c750c-112">The text string in the Description column of the Feature table is published as a [SelectionDescription ControlEvent](selectiondescription-controlevent.md) and displayed by a [Text control](text-control.md) in the Selection Dialog box.</span></span> <span data-ttu-id="c750c-113">選取樹狀結構控制項也會將控制碼發佈至反白專案的圖示。</span><span class="sxs-lookup"><span data-stu-id="c750c-113">The Selection tree control also publishes the handle to the icon of the highlighted item.</span></span>

 

 



