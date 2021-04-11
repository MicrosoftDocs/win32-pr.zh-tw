---
description: 只有在使用完整的 UI 層級來安裝應用程式時，安裝程式才會執行範例的安裝精靈順序。
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: 在安裝結束時新增控制項事件以執行啟動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944045"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a><span data-ttu-id="6fac5-103">在安裝結束時新增控制項事件以執行啟動</span><span class="sxs-lookup"><span data-stu-id="6fac5-103">Adding a Control Event at the End of the Installation to Run Launch</span></span>

<span data-ttu-id="6fac5-104">只有在使用 [*完整的 UI*](f-gly.md) 層級來安裝應用程式時，安裝程式才會執行範例的安裝精靈順序。</span><span class="sxs-lookup"><span data-stu-id="6fac5-104">The installer runs the sample's installation wizard sequence only if the [*full UI*](f-gly.md) level is used to install the application.</span></span> <span data-ttu-id="6fac5-105">範例對話順序的最後一個對話方塊是名為 ExitDialog 的結束 [對話](exit-dialog.md) 。</span><span class="sxs-lookup"><span data-stu-id="6fac5-105">The last dialog box of the sample dialog sequence is an [Exit Dialog](exit-dialog.md) named ExitDialog.</span></span> <span data-ttu-id="6fac5-106">當使用者與 ExitDialog 上的 [確定] 按鈕互動時，會先發佈將控制權傳回給安裝程式的 [EndDialog ControlEvent](enddialog-controlevent.md) 。</span><span class="sxs-lookup"><span data-stu-id="6fac5-106">When a user interacts with the OK button on ExitDialog, this first publishes an [EndDialog ControlEvent](enddialog-controlevent.md) that returns control to the installer.</span></span> <span data-ttu-id="6fac5-107">然後，控制項會發佈執行啟動自訂動作的 [Dataadapter.doaction ControlEvent](doaction-controlevent.md) 。</span><span class="sxs-lookup"><span data-stu-id="6fac5-107">The control then publishes a [DoAction ControlEvent](doaction-controlevent.md) that runs the Launch custom action.</span></span> <span data-ttu-id="6fac5-108">每個控制項事件都需要 [ControlEvent 資料表](controlevent-table.md)中的記錄。</span><span class="sxs-lookup"><span data-stu-id="6fac5-108">Each control event requires a record in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="6fac5-109">請參閱 [ControlEvent 總覽](controlevent-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="6fac5-109">See [ControlEvent Overview](controlevent-overview.md).</span></span>

[<span data-ttu-id="6fac5-110">ControlEvent 資料表</span><span class="sxs-lookup"><span data-stu-id="6fac5-110">ControlEvent Table</span></span>](controlevent-table.md)



| <span data-ttu-id="6fac5-111">對話</span><span class="sxs-lookup"><span data-stu-id="6fac5-111">Dialog</span></span>     | <span data-ttu-id="6fac5-112">控制項\_</span><span class="sxs-lookup"><span data-stu-id="6fac5-112">Control\_</span></span> | <span data-ttu-id="6fac5-113">事件</span><span class="sxs-lookup"><span data-stu-id="6fac5-113">Event</span></span>     | <span data-ttu-id="6fac5-114">引數</span><span class="sxs-lookup"><span data-stu-id="6fac5-114">Argument</span></span> | <span data-ttu-id="6fac5-115">條件</span><span class="sxs-lookup"><span data-stu-id="6fac5-115">Condition</span></span>                     | <span data-ttu-id="6fac5-116">排序</span><span class="sxs-lookup"><span data-stu-id="6fac5-116">Ordering</span></span> |
|------------|-----------|-----------|----------|-------------------------------|----------|
| <span data-ttu-id="6fac5-117">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="6fac5-117">ExitDialog</span></span> | <span data-ttu-id="6fac5-118">確定</span><span class="sxs-lookup"><span data-stu-id="6fac5-118">OK</span></span>        | <span data-ttu-id="6fac5-119">EndDialog</span><span class="sxs-lookup"><span data-stu-id="6fac5-119">EndDialog</span></span> | <span data-ttu-id="6fac5-120">傳回</span><span class="sxs-lookup"><span data-stu-id="6fac5-120">Return</span></span>   | <span data-ttu-id="6fac5-121">1</span><span class="sxs-lookup"><span data-stu-id="6fac5-121">1</span></span>                             | <span data-ttu-id="6fac5-122">1</span><span class="sxs-lookup"><span data-stu-id="6fac5-122">1</span></span>        |
| <span data-ttu-id="6fac5-123">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="6fac5-123">ExitDialog</span></span> | <span data-ttu-id="6fac5-124">確定</span><span class="sxs-lookup"><span data-stu-id="6fac5-124">OK</span></span>        | <span data-ttu-id="6fac5-125">Dataadapter.doaction</span><span class="sxs-lookup"><span data-stu-id="6fac5-125">DoAction</span></span>  | <span data-ttu-id="6fac5-126">啟動</span><span class="sxs-lookup"><span data-stu-id="6fac5-126">Launch</span></span>   | <span data-ttu-id="6fac5-127">未安裝且 $Tutorial = 3</span><span class="sxs-lookup"><span data-stu-id="6fac5-127">NOT Installed AND $Tutorial=3</span></span> | <span data-ttu-id="6fac5-128">2</span><span class="sxs-lookup"><span data-stu-id="6fac5-128">2</span></span>        |



 

<span data-ttu-id="6fac5-129">Dataadapter.doaction 控制項上的條件可確保自訂動作只會在第一次安裝應用程式時執行，而且會安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="6fac5-129">The condition on the DoAction control ensures the custom action only runs during the first installation of the application and that it is being installed locally.</span></span> <span data-ttu-id="6fac5-130">片語 $Tutorial = 3 表示教學課程元件的動作狀態是設定為 [本機]。</span><span class="sxs-lookup"><span data-stu-id="6fac5-130">The phrase $Tutorial=3 means the action state of the Tutorial component is set to local.</span></span> <span data-ttu-id="6fac5-131">請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="6fac5-131">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="6fac5-132">這會完成範例。</span><span class="sxs-lookup"><span data-stu-id="6fac5-132">This completes the sample.</span></span>

 

 



