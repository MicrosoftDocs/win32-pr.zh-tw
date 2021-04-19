---
description: SelectionTree 控制項會使用 SelectionNoItems 事件來刪除過時的專案描述文字，或停用變成無用的按鈕。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983934"
---
# <a name="selectionnoitems-controlevent"></a><span data-ttu-id="427c5-104">SelectionNoItems ControlEvent</span><span class="sxs-lookup"><span data-stu-id="427c5-104">SelectionNoItems ControlEvent</span></span>

<span data-ttu-id="427c5-105">[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionNoItems 事件來刪除過時的專案描述文字，或停用變成無用的按鈕。</span><span class="sxs-lookup"><span data-stu-id="427c5-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionNoItems event to delete obsolete item description text or to disable buttons that have become useless.</span></span> <span data-ttu-id="427c5-106">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="427c5-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="427c5-107">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="427c5-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="427c5-108">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="427c5-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="427c5-109">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="427c5-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="427c5-110">此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。</span><span class="sxs-lookup"><span data-stu-id="427c5-110">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="427c5-111">發佈者</span><span class="sxs-lookup"><span data-stu-id="427c5-111">Published By</span></span>

<span data-ttu-id="427c5-112">如果選取專案沒有節點，則為[SelectionTree 控制項](selectiontree-control.md)。</span><span class="sxs-lookup"><span data-stu-id="427c5-112">[SelectionTree control](selectiontree-control.md) if the selection has no nodes.</span></span>

## <a name="argument"></a><span data-ttu-id="427c5-113">引數</span><span class="sxs-lookup"><span data-stu-id="427c5-113">Argument</span></span>

<span data-ttu-id="427c5-114">無。</span><span class="sxs-lookup"><span data-stu-id="427c5-114">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="427c5-115">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="427c5-115">Action on Subscribers</span></span>

<span data-ttu-id="427c5-116">刪除過時的專案描述文字或停用已淘汰的按鈕。</span><span class="sxs-lookup"><span data-stu-id="427c5-116">Deletes obsolete item description text or disables obsolete buttons.</span></span>

## <a name="typical-use"></a><span data-ttu-id="427c5-117">一般用法</span><span class="sxs-lookup"><span data-stu-id="427c5-117">Typical Use</span></span>

<span data-ttu-id="427c5-118">可用來停用選取專案對話方塊上的 [下一步]、[重設] 和 [DiskCost []](selection-dialog.md) 按鈕。</span><span class="sxs-lookup"><span data-stu-id="427c5-118">May be used to disable the Next, Reset, and DiskCost buttons on the [Selection Dialog](selection-dialog.md) when a selection has no nodes and these buttons become useless.</span></span>

 

 



