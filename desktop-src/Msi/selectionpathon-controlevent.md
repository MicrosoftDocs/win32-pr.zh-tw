---
description: SelectionTree 控制項會使用 SelectionPathOn 事件來發佈布林值，指出是否有與目前選取之功能相關聯的選取路徑。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971651"
---
# <a name="selectionpathon-controlevent"></a><span data-ttu-id="f882e-104">SelectionPathOn ControlEvent</span><span class="sxs-lookup"><span data-stu-id="f882e-104">SelectionPathOn ControlEvent</span></span>

<span data-ttu-id="f882e-105">[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionPathOn 事件來發佈布林值，指出是否有與目前選取之功能相關聯的選取路徑。</span><span class="sxs-lookup"><span data-stu-id="f882e-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionPathOn event to publish a Boolean value indicating whether there is a selection path associated with the currently selected feature.</span></span> <span data-ttu-id="f882e-106">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="f882e-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="f882e-107">此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。</span><span class="sxs-lookup"><span data-stu-id="f882e-107">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

<span data-ttu-id="f882e-108">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="f882e-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f882e-109">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="f882e-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f882e-110">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="f882e-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="f882e-111">在 [維護安裝](maintenance-installation.md)期間，SelectionPathOn ControlEvent 永遠不會發行。</span><span class="sxs-lookup"><span data-stu-id="f882e-111">The SelectionPathOn ControlEvent is never published during a [Maintenance Installation](maintenance-installation.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f882e-112">發佈者</span><span class="sxs-lookup"><span data-stu-id="f882e-112">Published By</span></span>

[<span data-ttu-id="f882e-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="f882e-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="f882e-114">引數</span><span class="sxs-lookup"><span data-stu-id="f882e-114">Argument</span></span>

<span data-ttu-id="f882e-115">無。</span><span class="sxs-lookup"><span data-stu-id="f882e-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f882e-116">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="f882e-116">Action on Subscribers</span></span>

<span data-ttu-id="f882e-117">無。</span><span class="sxs-lookup"><span data-stu-id="f882e-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f882e-118">一般用法</span><span class="sxs-lookup"><span data-stu-id="f882e-118">Typical Use</span></span>

<span data-ttu-id="f882e-119">在與 SelectionTree 相同的強制回應對話方塊上， [文字](text-control.md) 控制項應透過 [EventMapping 資料表](eventmapping-table.md)訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="f882e-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="f882e-120">文字控制項會顯示選取路徑的標題。</span><span class="sxs-lookup"><span data-stu-id="f882e-120">The Text Control displays the caption of the selection path.</span></span> <span data-ttu-id="f882e-121">此文字控制項會根據事件顯示或隱藏。</span><span class="sxs-lookup"><span data-stu-id="f882e-121">This text control is visible or hidden depending on the event.</span></span>

 

 



