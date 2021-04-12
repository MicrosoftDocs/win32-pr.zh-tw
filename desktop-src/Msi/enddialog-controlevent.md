---
description: 此事件會通知安裝程式移除強制回應對話方塊。 在所有情況下，安裝程式都會移除目前的對話方塊。
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193118"
---
# <a name="enddialog-controlevent"></a><span data-ttu-id="911c1-104">EndDialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="911c1-104">EndDialog ControlEvent</span></span>

<span data-ttu-id="911c1-105">此事件會通知安裝程式移除強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="911c1-105">This event notifies the installer to remove a modal dialog box.</span></span> <span data-ttu-id="911c1-106">在所有情況下，安裝程式都會移除目前的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="911c1-106">In all cases the installer removes the present dialog box.</span></span>

<span data-ttu-id="911c1-107">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="911c1-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="911c1-108">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="911c1-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="911c1-109">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="911c1-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="911c1-110">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="911c1-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="911c1-111">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="911c1-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="911c1-112">下表列出在 [ControlEvent 資料表](controlevent-table.md)中輸入不同引數所產生之事件的動作。</span><span class="sxs-lookup"><span data-stu-id="911c1-112">The following table lists the action of the event resulting from different arguments entered into the [ControlEvent table](controlevent-table.md).</span></span>



| <span data-ttu-id="911c1-113">引數</span><span class="sxs-lookup"><span data-stu-id="911c1-113">Argument</span></span> | <span data-ttu-id="911c1-114">安裝程式的動作</span><span class="sxs-lookup"><span data-stu-id="911c1-114">Action by the installer</span></span>                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="911c1-115">結束</span><span class="sxs-lookup"><span data-stu-id="911c1-115">Exit</span></span>     | <span data-ttu-id="911c1-116">Wizard 順序已關閉，而控制項會傳回具有 UserExit 值的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="911c1-116">The wizard sequence is closed and the control returns to the installer with the UserExit value.</span></span> <span data-ttu-id="911c1-117">這個引數不能用在另一個對話方塊子系的對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="911c1-117">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="911c1-118">重試</span><span class="sxs-lookup"><span data-stu-id="911c1-118">Retry</span></span>    | <span data-ttu-id="911c1-119">嚮導順序已關閉，且控制項以暫停值返回安裝程式。</span><span class="sxs-lookup"><span data-stu-id="911c1-119">The wizard sequence is closed and the control returns to the installer with the Suspend value.</span></span> <span data-ttu-id="911c1-120">這個引數不能用在另一個對話方塊子系的對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="911c1-120">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span>  |
| <span data-ttu-id="911c1-121">忽略</span><span class="sxs-lookup"><span data-stu-id="911c1-121">Ignore</span></span>   | <span data-ttu-id="911c1-122">嚮導順序已關閉，且控制項以已完成的值返回安裝程式。</span><span class="sxs-lookup"><span data-stu-id="911c1-122">The wizard sequence is closed and the control returns to the installer with the Finished value.</span></span> <span data-ttu-id="911c1-123">這個引數不能用在另一個對話方塊子系的對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="911c1-123">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="911c1-124">傳回</span><span class="sxs-lookup"><span data-stu-id="911c1-124">Return</span></span>   | <span data-ttu-id="911c1-125">控制項會回到目前對話方塊的父系，如果沒有父代，控制項會返回具有 Success 值的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="911c1-125">The control returns to the parent of the present dialog box, or if there is no parent, the control returns to the installer with the Success value.</span></span>                                 |



 

## <a name="published-by"></a><span data-ttu-id="911c1-126">發佈者</span><span class="sxs-lookup"><span data-stu-id="911c1-126">Published By</span></span>

<span data-ttu-id="911c1-127">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="911c1-127">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="911c1-128">引數</span><span class="sxs-lookup"><span data-stu-id="911c1-128">Argument</span></span>

<span data-ttu-id="911c1-129">在一般對話方塊上， [ControlEvent 資料表](controlevent-table.md) 的 Argument 資料行可以是 "Return"、"Exit"、"Retry" 或 "Ignore"。</span><span class="sxs-lookup"><span data-stu-id="911c1-129">On regular dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "Return", "Exit", "Retry", or "Ignore".</span></span>

<span data-ttu-id="911c1-130">在錯誤對話方塊中， [ControlEvent 資料表](controlevent-table.md) 的 Argument 資料行可以是 "ErrorOk"、"ErrorCancel"、"ErrorAbort"、"ErrorRetry"、"ErrorIgnore"、"ErrorYes" 或 "ErrorNo"。</span><span class="sxs-lookup"><span data-stu-id="911c1-130">On error dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes", or "ErrorNo".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="911c1-131">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="911c1-131">Action on Subscribers</span></span>

<span data-ttu-id="911c1-132">無。</span><span class="sxs-lookup"><span data-stu-id="911c1-132">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="911c1-133">一般用法</span><span class="sxs-lookup"><span data-stu-id="911c1-133">Typical Use</span></span>

<span data-ttu-id="911c1-134">強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="911c1-134">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to close a dialog box.</span></span>

 

 



