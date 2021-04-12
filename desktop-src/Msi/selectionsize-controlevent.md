---
description: SelectionTree 控制項會使用 SelectionSize 事件來發佈反白專案的大小。
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193097"
---
# <a name="selectionsize-controlevent"></a><span data-ttu-id="5c92c-103">SelectionSize ControlEvent</span><span class="sxs-lookup"><span data-stu-id="5c92c-103">SelectionSize ControlEvent</span></span>

<span data-ttu-id="5c92c-104">[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionSize 事件來發佈反白專案的大小。</span><span class="sxs-lookup"><span data-stu-id="5c92c-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionSize event to publish the size of the highlighted item.</span></span> <span data-ttu-id="5c92c-105">如果它是父代專案，則也會一併發行選取的子係數目。</span><span class="sxs-lookup"><span data-stu-id="5c92c-105">If it is a parent item, then the number of children selected is also published.</span></span> <span data-ttu-id="5c92c-106">字串是 [SelParentCostNegPos 資料表](uitext-table.md)中的其中一個 **SelChildCostPos**、 **SelChildCostNeg**、 **SelParentCostPosPos**、 **SelParentCostPosNeg**、 **SelParentCostNegNeg** 或 **UIText** 字串。</span><span class="sxs-lookup"><span data-stu-id="5c92c-106">The string is one of the **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** or **SelParentCostNegNeg** strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="5c92c-107">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="5c92c-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="5c92c-108">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="5c92c-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="5c92c-109">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="5c92c-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="5c92c-110">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="5c92c-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="5c92c-111">此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。</span><span class="sxs-lookup"><span data-stu-id="5c92c-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="5c92c-112">發佈者</span><span class="sxs-lookup"><span data-stu-id="5c92c-112">Published By</span></span>

[<span data-ttu-id="5c92c-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="5c92c-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="5c92c-114">引數</span><span class="sxs-lookup"><span data-stu-id="5c92c-114">Argument</span></span>

<span data-ttu-id="5c92c-115">無。</span><span class="sxs-lookup"><span data-stu-id="5c92c-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="5c92c-116">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="5c92c-116">Action on Subscribers</span></span>

<span data-ttu-id="5c92c-117">無。</span><span class="sxs-lookup"><span data-stu-id="5c92c-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="5c92c-118">一般用法</span><span class="sxs-lookup"><span data-stu-id="5c92c-118">Typical Use</span></span>

<span data-ttu-id="5c92c-119">在與 SelectionTree 控制項相同的強制回應對話方塊上，透過[EventMapping 資料表](eventmapping-table.md)的[文字](text-control.md)控制項。</span><span class="sxs-lookup"><span data-stu-id="5c92c-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree Control via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="5c92c-120">文字控制項會使用此事件來顯示反白專案的大小。</span><span class="sxs-lookup"><span data-stu-id="5c92c-120">The Text Control uses this event to display the size of the highlighted item.</span></span>

 

 



