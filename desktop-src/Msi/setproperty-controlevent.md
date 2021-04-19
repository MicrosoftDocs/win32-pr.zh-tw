---
description: SetProperty 事件的語法與其他事件名稱的語法不同，它會以方括弧括住屬性（ \[ property \_ name） \] 。
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: SetProperty ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984598"
---
# <a name="setproperty-controlevent"></a><span data-ttu-id="980f0-103">SetProperty ControlEvent</span><span class="sxs-lookup"><span data-stu-id="980f0-103">SetProperty ControlEvent</span></span>

<span data-ttu-id="980f0-104">SetProperty 事件的語法與其他事件名稱的語法不同，它會以方括弧括住屬性（ \[ property \_ name） \] 。</span><span class="sxs-lookup"><span data-stu-id="980f0-104">The syntax for the SetProperty event is different than for other ControlEvents In place of the name of the event one puts the property in square brackets: \[property\_name\].</span></span> <span data-ttu-id="980f0-105">引數是屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="980f0-105">The argument is the new value of the property.</span></span> <span data-ttu-id="980f0-106">若要取消設定屬性，引數必須是 {} 。</span><span class="sxs-lookup"><span data-stu-id="980f0-106">To unset the property, the argument must be {}.</span></span> <span data-ttu-id="980f0-107">這是必要的，因為引數是資料表中的主鍵，因此不能是 null。</span><span class="sxs-lookup"><span data-stu-id="980f0-107">This is necessary, because the argument is a primary key in the table and so cannot be null.</span></span> <span data-ttu-id="980f0-108">引數將使用 FormatText 方法進行格式化，因此引數可以包含 FormatText 方法可以處理的任何運算式。</span><span class="sxs-lookup"><span data-stu-id="980f0-108">The argument will be formatted using the FormatText method, therefore the argument can contain any expression that the FormatText method can handle.</span></span> <span data-ttu-id="980f0-109">屬性值會在 ControlEvent 時進行評估。</span><span class="sxs-lookup"><span data-stu-id="980f0-109">The property values are evaluated at the moment of the ControlEvent.</span></span>

<span data-ttu-id="980f0-110">這個事件可以透過 [按鈕控制項](pushbutton-control.md)、 [CheckBox 控制項](checkbox-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="980f0-110">This event can be published by a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="980f0-111">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="980f0-111">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="980f0-112">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="980f0-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="980f0-113">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="980f0-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="980f0-114">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="980f0-114">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="980f0-115">發佈者</span><span class="sxs-lookup"><span data-stu-id="980f0-115">Published By</span></span>

<span data-ttu-id="980f0-116">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="980f0-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="980f0-117">引數</span><span class="sxs-lookup"><span data-stu-id="980f0-117">Argument</span></span>

<span data-ttu-id="980f0-118">屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="980f0-118">The new value of the property.</span></span> <span data-ttu-id="980f0-119">{} 若為 null。</span><span class="sxs-lookup"><span data-stu-id="980f0-119">{} for null.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="980f0-120">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="980f0-120">Action on Subscribers</span></span>

<span data-ttu-id="980f0-121">無。</span><span class="sxs-lookup"><span data-stu-id="980f0-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="980f0-122">一般用法</span><span class="sxs-lookup"><span data-stu-id="980f0-122">Typical Use</span></span>

<span data-ttu-id="980f0-123">連結至這個事件之對話方塊上的 [按鈕控制項，](pushbutton-control.md) 以便在推送按鈕時變更屬性。</span><span class="sxs-lookup"><span data-stu-id="980f0-123">A [PushButton](pushbutton-control.md) control on a dialog box linked to this event so it changes a property when the button is pushed.</span></span>

 

 



