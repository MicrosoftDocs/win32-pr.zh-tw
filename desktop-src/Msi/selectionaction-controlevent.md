---
description: SelectionTree 控制項會使用這個事件來發佈描述反白顯示專案的字串。 字串是 &0034 的其中一個 \# ;\* & \# UIText 資料表中的 Sel 0034; 字串。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: SelectionAction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981696"
---
# <a name="selectionaction-controlevent"></a><span data-ttu-id="41e9f-105">SelectionAction ControlEvent</span><span class="sxs-lookup"><span data-stu-id="41e9f-105">SelectionAction ControlEvent</span></span>

<span data-ttu-id="41e9f-106">[SelectionTree 控制項](selectiontree-control.md)會使用這個事件來發佈描述反白顯示專案的字串。</span><span class="sxs-lookup"><span data-stu-id="41e9f-106">The [SelectionTree control](selectiontree-control.md) uses this event to publish a string describing the highlighted item.</span></span> <span data-ttu-id="41e9f-107">字串是 \* [UIText 資料表](uitext-table.md)中的其中一個「Sel」字串。</span><span class="sxs-lookup"><span data-stu-id="41e9f-107">The string is one of the "Sel\*" strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="41e9f-108">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="41e9f-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="41e9f-109">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="41e9f-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="41e9f-110">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="41e9f-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="41e9f-111">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="41e9f-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="41e9f-112">此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。</span><span class="sxs-lookup"><span data-stu-id="41e9f-112">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="41e9f-113">發佈者</span><span class="sxs-lookup"><span data-stu-id="41e9f-113">Published By</span></span>

[<span data-ttu-id="41e9f-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="41e9f-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="41e9f-115">引數</span><span class="sxs-lookup"><span data-stu-id="41e9f-115">Argument</span></span>

<span data-ttu-id="41e9f-116">無。</span><span class="sxs-lookup"><span data-stu-id="41e9f-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="41e9f-117">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="41e9f-117">Action on Subscribers</span></span>

<span data-ttu-id="41e9f-118">無。</span><span class="sxs-lookup"><span data-stu-id="41e9f-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="41e9f-119">一般用法</span><span class="sxs-lookup"><span data-stu-id="41e9f-119">Typical Use</span></span>

<span data-ttu-id="41e9f-120">與 SelectionTree 相同的強制回應對話方塊中的 [文字](text-control.md) 控制項，應該透過 [EventMapping 資料表](eventmapping-table.md)訂閱此事件。</span><span class="sxs-lookup"><span data-stu-id="41e9f-120">A [Text](text-control.md) control in the same modal dialog box as the SelectionTree should subscribe to this event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="41e9f-121">文字控制項會顯示所選取專案的說明。</span><span class="sxs-lookup"><span data-stu-id="41e9f-121">The Text Control displays the explanation of the selected item.</span></span>

 

 



