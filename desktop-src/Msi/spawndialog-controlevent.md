---
description: SpawnDialog ControlEvent 會通知安裝程式建立強制回應對話方塊的子系，同時讓目前的對話方塊保持執行狀態。
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: SpawnDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972376"
---
# <a name="spawndialog-controlevent"></a><span data-ttu-id="92add-103">SpawnDialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="92add-103">SpawnDialog ControlEvent</span></span>

<span data-ttu-id="92add-104">SpawnDialog ControlEvent 會通知安裝程式建立強制回應對話方塊的子系，同時讓目前的對話方塊保持執行狀態。</span><span class="sxs-lookup"><span data-stu-id="92add-104">The SpawnDialog ControlEvent notifies the installer to create a child of a modal dialog box while keeping the present dialog box running.</span></span>

<span data-ttu-id="92add-105">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="92add-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="92add-106">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="92add-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="92add-107">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="92add-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="92add-108">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="92add-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="92add-109">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="92add-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="92add-110">發佈者</span><span class="sxs-lookup"><span data-stu-id="92add-110">Published By</span></span>

<span data-ttu-id="92add-111">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="92add-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="92add-112">引數</span><span class="sxs-lookup"><span data-stu-id="92add-112">Argument</span></span>

<span data-ttu-id="92add-113">字串，這是新對話方塊的名稱。</span><span class="sxs-lookup"><span data-stu-id="92add-113">A string that is the name of the new dialog box.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="92add-114">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="92add-114">Action on Subscribers</span></span>

<span data-ttu-id="92add-115">無。</span><span class="sxs-lookup"><span data-stu-id="92add-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="92add-116">一般用法</span><span class="sxs-lookup"><span data-stu-id="92add-116">Typical Use</span></span>

<span data-ttu-id="92add-117">強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以建立子對話，例如「您確定要取消嗎？」。</span><span class="sxs-lookup"><span data-stu-id="92add-117">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to create a child dialog, such as an "Are you sure you want to cancel?"</span></span> <span data-ttu-id="92add-118">對話方塊中指定選項。</span><span class="sxs-lookup"><span data-stu-id="92add-118">dialog box.</span></span>

 

 



