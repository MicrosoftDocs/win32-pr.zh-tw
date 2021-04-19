---
description: 會重設此對話方塊。 換句話說，會呼叫對話方塊上的所有控制項，以復原它們所執行的屬性變更。 此事件會將所有屬性值重設為建立對話方塊時的值。
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: 重設 ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987638"
---
# <a name="reset-controlevent"></a><span data-ttu-id="a078e-105">重設 ControlEvent</span><span class="sxs-lookup"><span data-stu-id="a078e-105">Reset ControlEvent</span></span>

<span data-ttu-id="a078e-106">會重設此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a078e-106">The dialog box is reset.</span></span> <span data-ttu-id="a078e-107">換句話說，會呼叫對話方塊上的所有控制項，以復原它們所執行的屬性變更。</span><span class="sxs-lookup"><span data-stu-id="a078e-107">In other words, all the controls on the dialog box are called to undo the property changes they have performed.</span></span> <span data-ttu-id="a078e-108">此事件會將所有屬性值重設為建立對話方塊時的值。</span><span class="sxs-lookup"><span data-stu-id="a078e-108">This event resets all the property values to what they were when the dialog box was created.</span></span>

<span data-ttu-id="a078e-109">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="a078e-109">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="a078e-110">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="a078e-110">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="a078e-111">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="a078e-111">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="a078e-112">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a078e-112">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="a078e-113">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="a078e-113">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="a078e-114">在某些情況下，這種情況應該很少發生，此 ControlEvent 並不會正確處理。</span><span class="sxs-lookup"><span data-stu-id="a078e-114">There is a case, which should occur rarely in practice, that is not handled properly by this ControlEvent.</span></span> <span data-ttu-id="a078e-115">如果相同對話方塊上有兩個或多個控制項連結到相同的屬性，且至少其中一個控制項開始有其他屬性，則這個屬性值有時會重設為其第二個值。</span><span class="sxs-lookup"><span data-stu-id="a078e-115">If there are two or more controls on the same dialog box linked indirectly to the same property and at least one of them started having some other property, then this property value will sometimes be reset to its second value.</span></span>

## <a name="published-by"></a><span data-ttu-id="a078e-116">發佈者</span><span class="sxs-lookup"><span data-stu-id="a078e-116">Published By</span></span>

<span data-ttu-id="a078e-117">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="a078e-117">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="a078e-118">引數</span><span class="sxs-lookup"><span data-stu-id="a078e-118">Argument</span></span>

<span data-ttu-id="a078e-119">無。</span><span class="sxs-lookup"><span data-stu-id="a078e-119">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="a078e-120">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="a078e-120">Action on Subscribers</span></span>

<span data-ttu-id="a078e-121">無。</span><span class="sxs-lookup"><span data-stu-id="a078e-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="a078e-122">一般用法</span><span class="sxs-lookup"><span data-stu-id="a078e-122">Typical Use</span></span>

<span data-ttu-id="a078e-123">強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項可用來重設對話方塊上的所有值，以及取消頁面上的所有變更。</span><span class="sxs-lookup"><span data-stu-id="a078e-123">A [PushButton](pushbutton-control.md) control on a modal dialog box is used to reset all the values on the dialog box and to cancel all the changes on the page.</span></span>

 

 



