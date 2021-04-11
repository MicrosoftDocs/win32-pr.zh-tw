---
description: 此事件會通知安裝程式將強制回應對話方塊轉換成另一個對話方塊。 安裝程式會移除目前的對話方塊，並使用引數中指出的名稱建立新的對話方塊。
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114557"
---
# <a name="newdialog-controlevent"></a><span data-ttu-id="a2840-104">NewDialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="a2840-104">NewDialog ControlEvent</span></span>

<span data-ttu-id="a2840-105">此事件會通知安裝程式將強制回應對話方塊轉換成另一個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a2840-105">This event notifies the installer to transition a modal dialog box to another dialog box.</span></span> <span data-ttu-id="a2840-106">安裝程式會移除目前的對話方塊，並使用引數中指出的名稱建立新的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a2840-106">The installer removes the present dialog box and creates the new one with the name indicated in the argument.</span></span>

<span data-ttu-id="a2840-107">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="a2840-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="a2840-108">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="a2840-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="a2840-109">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="a2840-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="a2840-110">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a2840-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="a2840-111">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="a2840-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="a2840-112">發佈者</span><span class="sxs-lookup"><span data-stu-id="a2840-112">Published By</span></span>

<span data-ttu-id="a2840-113">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="a2840-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="a2840-114">引數</span><span class="sxs-lookup"><span data-stu-id="a2840-114">Argument</span></span>

<span data-ttu-id="a2840-115">字串，這是新對話方塊的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2840-115">A string that is the name of the new dialog.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="a2840-116">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="a2840-116">Action on Subscribers</span></span>

<span data-ttu-id="a2840-117">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="a2840-117">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="a2840-118">一般用法</span><span class="sxs-lookup"><span data-stu-id="a2840-118">Typical Use</span></span>

<span data-ttu-id="a2840-119">強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以指示轉換至相同 wizard 順序的下一個或上一個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a2840-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to signal a transition to the next or previous dialog box of the same wizard sequence.</span></span>

 

 



