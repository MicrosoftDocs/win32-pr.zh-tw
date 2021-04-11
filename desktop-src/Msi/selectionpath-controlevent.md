---
description: SelectionTree 控制項會使用 SelectionPath 事件來發佈反白專案的路徑。
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944421"
---
# <a name="selectionpath-controlevent"></a><span data-ttu-id="c2562-103">SelectionPath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="c2562-103">SelectionPath ControlEvent</span></span>

<span data-ttu-id="c2562-104">[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionPath 事件來發佈反白專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c2562-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionPath event to publish the path for the highlighted item.</span></span> <span data-ttu-id="c2562-105">如果已選取要從來源執行的專案，則這是來源的路徑。</span><span class="sxs-lookup"><span data-stu-id="c2562-105">If the item is selected to run from source, then this is the path of the source.</span></span> <span data-ttu-id="c2562-106">如果選取的專案不存在，則字串會是 [UIText 資料表](uitext-table.md)中的 **AbsentPath** 字串。</span><span class="sxs-lookup"><span data-stu-id="c2562-106">If the item is selected to be absent, then the string is the **AbsentPath** string from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="c2562-107">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="c2562-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="c2562-108">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="c2562-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="c2562-109">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c2562-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="c2562-110">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="c2562-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="c2562-111">此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。</span><span class="sxs-lookup"><span data-stu-id="c2562-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="c2562-112">發佈者</span><span class="sxs-lookup"><span data-stu-id="c2562-112">Published By</span></span>

[<span data-ttu-id="c2562-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="c2562-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="c2562-114">引數</span><span class="sxs-lookup"><span data-stu-id="c2562-114">Argument</span></span>

<span data-ttu-id="c2562-115">無。</span><span class="sxs-lookup"><span data-stu-id="c2562-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c2562-116">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="c2562-116">Action on Subscribers</span></span>

<span data-ttu-id="c2562-117">無。</span><span class="sxs-lookup"><span data-stu-id="c2562-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c2562-118">一般用法</span><span class="sxs-lookup"><span data-stu-id="c2562-118">Typical Use</span></span>

<span data-ttu-id="c2562-119">在與 SelectionTree 相同的強制回應對話方塊上， [文字](text-control.md) 控制項應透過 [EventMapping 資料表](eventmapping-table.md)訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="c2562-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="c2562-120">文字控制項會顯示反白專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c2562-120">The Text Control displays the path of the highlighted item.</span></span>

 

 



