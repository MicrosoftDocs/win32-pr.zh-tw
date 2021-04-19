---
description: 允許作者在重新安裝期間指定驗證模式，以及在目前的對話方塊正在執行時指定模式。
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ReinstallMode ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980834"
---
# <a name="reinstallmode-controlevent"></a><span data-ttu-id="5ee67-103">ReinstallMode ControlEvent</span><span class="sxs-lookup"><span data-stu-id="5ee67-103">ReinstallMode ControlEvent</span></span>

<span data-ttu-id="5ee67-104">ReinstallMode 會 ControlEventallows 作者來指定重新安裝期間的驗證模式或模式，以及目前的對話方塊正在執行。</span><span class="sxs-lookup"><span data-stu-id="5ee67-104">The ReinstallMode ControlEventallows the author to specify the validation mode or modes during a reinstallation, and while the current dialog box is running.</span></span>

<span data-ttu-id="5ee67-105">這個事件可以透過 [按鈕控制項](pushbutton-control.md) 或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="5ee67-105">This event can be published by a [PushButton Control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="5ee67-106">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)中，而且需要在 [*完整的 UI*](f-gly.md) 層級執行使用者介面。</span><span class="sxs-lookup"><span data-stu-id="5ee67-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="5ee67-107">此事件無法搭配 [*縮減的 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)來使用。</span><span class="sxs-lookup"><span data-stu-id="5ee67-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="5ee67-108">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="5ee67-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="5ee67-109">發佈者</span><span class="sxs-lookup"><span data-stu-id="5ee67-109">Published By</span></span>

<span data-ttu-id="5ee67-110">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="5ee67-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="5ee67-111">引數</span><span class="sxs-lookup"><span data-stu-id="5ee67-111">Argument</span></span>

<span data-ttu-id="5ee67-112">字串。</span><span class="sxs-lookup"><span data-stu-id="5ee67-112">A string.</span></span> <span data-ttu-id="5ee67-113">如需可能值的清單，請參閱 [**REINSTALLMODE**](reinstallmode.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="5ee67-113">For a list of possible values, see [**REINSTALLMODE**](reinstallmode.md) property.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="5ee67-114">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="5ee67-114">Action on Subscribers</span></span>

<span data-ttu-id="5ee67-115">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="5ee67-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="5ee67-116">一般用法</span><span class="sxs-lookup"><span data-stu-id="5ee67-116">Typical Use</span></span>

<span data-ttu-id="5ee67-117">此事件會系結至強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="5ee67-117">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="5ee67-118">相同的 [按鈕](pushbutton-control.md) 控制項也應系結至 [重新安裝](reinstall-controlevent.md) ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="5ee67-118">The same [PushButton](pushbutton-control.md) control should also be tied to a [Reinstall](reinstall-controlevent.md) ControlEvent.</span></span>

 

 



