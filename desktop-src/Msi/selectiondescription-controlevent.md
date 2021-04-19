---
description: SelectionTree 控制項會使用 SelectionDescription 事件來發行包含反白專案之描述的字串。 此字串是功能資料表的描述欄位。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: SelectionDescription ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979197"
---
# <a name="selectiondescription-controlevent"></a><span data-ttu-id="a9044-105">SelectionDescription ControlEvent</span><span class="sxs-lookup"><span data-stu-id="a9044-105">SelectionDescription ControlEvent</span></span>

<span data-ttu-id="a9044-106">[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionDescription 事件來發行包含反白專案之描述的字串。</span><span class="sxs-lookup"><span data-stu-id="a9044-106">The [SelectionTree control](selectiontree-control.md) uses the SelectionDescription event to publish a string that contains the description for the highlighted item.</span></span> <span data-ttu-id="a9044-107">此字串是 [功能資料表](feature-table.md)的 **描述** 欄位。</span><span class="sxs-lookup"><span data-stu-id="a9044-107">This string is the **Description** field of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="a9044-108">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="a9044-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="a9044-109">此事件只會影響與 [SelectionTree 控制項](selectiontree-control.md)位於相同對話方塊的控制項。</span><span class="sxs-lookup"><span data-stu-id="a9044-109">This event can only affect controls that are located on the same dialog box as the [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="a9044-110">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="a9044-110">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="a9044-111">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a9044-111">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="a9044-112">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="a9044-112">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="a9044-113">發佈者</span><span class="sxs-lookup"><span data-stu-id="a9044-113">Published By</span></span>

[<span data-ttu-id="a9044-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="a9044-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="a9044-115">引數</span><span class="sxs-lookup"><span data-stu-id="a9044-115">Argument</span></span>

<span data-ttu-id="a9044-116">無。</span><span class="sxs-lookup"><span data-stu-id="a9044-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="a9044-117">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="a9044-117">Action on Subscribers</span></span>

<span data-ttu-id="a9044-118">無。</span><span class="sxs-lookup"><span data-stu-id="a9044-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="a9044-119">一般用法</span><span class="sxs-lookup"><span data-stu-id="a9044-119">Typical Use</span></span>

<span data-ttu-id="a9044-120">與 SelectionTree 透過[EventMapping 資料表](eventmapping-table.md)訂閱這個 ControlEvent 的相同強制回應對話方塊上的[文字](text-control.md)控制項。</span><span class="sxs-lookup"><span data-stu-id="a9044-120">A [Text](text-control.md) control on the same modal dialog as the SelectionTree subscribes to this ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="a9044-121">文字控制項會使用此事件來顯示反白專案的描述。</span><span class="sxs-lookup"><span data-stu-id="a9044-121">The Text Control uses this event to display the description of the highlighted item.</span></span>

 

 



