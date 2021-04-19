---
description: 此事件會通知安裝程式，它必須確認選取的路徑是可寫入的。 如果無法寫入路徑，事件就會封鎖與控制項相關聯的進一步工作。
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: CheckExistingTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1117de57c5474d196da1f40da6fda3cce60b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989944"
---
# <a name="checkexistingtargetpath-controlevent"></a><span data-ttu-id="920fe-104">CheckExistingTargetPath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="920fe-104">CheckExistingTargetPath ControlEvent</span></span>

<span data-ttu-id="920fe-105">此事件會通知安裝程式，它必須確認選取的路徑是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="920fe-105">This event notifies the installer that it has to verify that the selected path is writable.</span></span> <span data-ttu-id="920fe-106">如果無法寫入路徑，事件就會封鎖與控制項相關聯的進一步工作。</span><span class="sxs-lookup"><span data-stu-id="920fe-106">If the path is cannot be written, then the event blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="920fe-107">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="920fe-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="920fe-108">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="920fe-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="920fe-109">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="920fe-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="920fe-110">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="920fe-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="920fe-111">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="920fe-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="920fe-112">發佈者</span><span class="sxs-lookup"><span data-stu-id="920fe-112">Published By</span></span>

<span data-ttu-id="920fe-113">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="920fe-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="920fe-114">引數</span><span class="sxs-lookup"><span data-stu-id="920fe-114">Argument</span></span>

<span data-ttu-id="920fe-115">包含路徑之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="920fe-115">The name of the property containing the path.</span></span> <span data-ttu-id="920fe-116">如果屬性是 indirected，則屬性名稱會以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="920fe-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="920fe-117">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="920fe-117">Action on Subscribers</span></span>

<span data-ttu-id="920fe-118">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="920fe-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="920fe-119">一般用法</span><span class="sxs-lookup"><span data-stu-id="920fe-119">Typical Use</span></span>

<span data-ttu-id="920fe-120">流覽對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以檢查選取的路徑，然後再返回選取專案對話方塊。</span><span class="sxs-lookup"><span data-stu-id="920fe-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

 

 



