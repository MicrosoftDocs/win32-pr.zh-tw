---
description: 允許作者在目前的對話方塊正在執行時，起始部分或所有功能的重新安裝。
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: 重新安裝 ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974666"
---
# <a name="reinstall-controlevent"></a><span data-ttu-id="7e65f-103">重新安裝 ControlEvent</span><span class="sxs-lookup"><span data-stu-id="7e65f-103">Reinstall ControlEvent</span></span>

<span data-ttu-id="7e65f-104">重新安裝 ControlEventallows 作者，在目前的對話方塊正在執行時，起始部分或所有功能的重新安裝。</span><span class="sxs-lookup"><span data-stu-id="7e65f-104">The Reinstall ControlEventallows the author to initiate a reinstall of some or all features, while the current dialog box is running.</span></span>

<span data-ttu-id="7e65f-105">這個事件可以透過 [按鈕控制項](pushbutton-control.md) 或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="7e65f-105">This event can be published by a [PushButton control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="7e65f-106">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)中，而且需要在 [*完整的 UI*](f-gly.md) 層級執行使用者介面。</span><span class="sxs-lookup"><span data-stu-id="7e65f-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="7e65f-107">此事件無法搭配 [*縮減的 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)來使用。</span><span class="sxs-lookup"><span data-stu-id="7e65f-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="7e65f-108">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="7e65f-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="7e65f-109">發佈者</span><span class="sxs-lookup"><span data-stu-id="7e65f-109">Published By</span></span>

<span data-ttu-id="7e65f-110">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="7e65f-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="7e65f-111">引數</span><span class="sxs-lookup"><span data-stu-id="7e65f-111">Argument</span></span>

<span data-ttu-id="7e65f-112">字串，該字串為功能的名稱或 "ALL"。</span><span class="sxs-lookup"><span data-stu-id="7e65f-112">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="7e65f-113">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="7e65f-113">Action on Subscribers</span></span>

<span data-ttu-id="7e65f-114">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="7e65f-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="7e65f-115">一般用法</span><span class="sxs-lookup"><span data-stu-id="7e65f-115">Typical Use</span></span>

<span data-ttu-id="7e65f-116">此事件會系結至強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="7e65f-116">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="7e65f-117">相同的 [按鈕](pushbutton-control.md) 控制項也應系結至 [ReinstallMode](reinstallmode-controlevent.md) ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="7e65f-117">The same [PushButton](pushbutton-control.md) control should also be tied to a [ReinstallMode](reinstallmode-controlevent.md) ControlEvent.</span></span>

 

 



