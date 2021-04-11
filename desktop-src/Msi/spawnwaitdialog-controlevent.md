---
description: 如果 [條件] 資料行中的運算式評估為 FALSE，SpawnWaitDialog ControlEvent 就會觸發 ControlEvent 資料表的 Argument 資料行所指定的對話方塊。
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943530"
---
# <a name="spawnwaitdialog-controlevent"></a><span data-ttu-id="de48a-103">SpawnWaitDialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="de48a-103">SpawnWaitDialog ControlEvent</span></span>

<span data-ttu-id="de48a-104">如果 [條件] 資料行中的運算式評估為 FALSE，SpawnWaitDialog ControlEvent 就會觸發 [ControlEvent 資料表](controlevent-table.md)的 Argument 資料行所指定的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="de48a-104">The SpawnWaitDialog ControlEvent triggers the dialog box specified by the Argument column of the [ControlEvent table](controlevent-table.md), if the expression in the Condition column evaluates as FALSE.</span></span> <span data-ttu-id="de48a-105">只要條件運算式維持 FALSE，對話方塊就會保持開啟狀態，而且只要條件運算式評估為 TRUE，就會移除此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="de48a-105">The dialog box remains up for as long as the conditional expression remains FALSE and is removed as soon as the condition evaluates TRUE.</span></span>

<span data-ttu-id="de48a-106">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="de48a-106">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="de48a-107">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="de48a-107">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="de48a-108">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="de48a-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="de48a-109">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="de48a-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="de48a-110">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="de48a-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="de48a-111">發佈者</span><span class="sxs-lookup"><span data-stu-id="de48a-111">Published By</span></span>

<span data-ttu-id="de48a-112">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="de48a-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="de48a-113">引數</span><span class="sxs-lookup"><span data-stu-id="de48a-113">Argument</span></span>

<span data-ttu-id="de48a-114">[對話方塊資料表](dialog-table.md)中的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="de48a-114">A dialog box in the [Dialog table](dialog-table.md).</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="de48a-115">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="de48a-115">Action on Subscribers</span></span>

<span data-ttu-id="de48a-116">無。</span><span class="sxs-lookup"><span data-stu-id="de48a-116">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="de48a-117">一般用法</span><span class="sxs-lookup"><span data-stu-id="de48a-117">Typical Use</span></span>

<span data-ttu-id="de48a-118">您可以使用 SpawnWaitDialog ControlEvent 來等候任何背景工作完成，該工作可以使用條件運算式（例如屬性的狀態）進行測試。</span><span class="sxs-lookup"><span data-stu-id="de48a-118">The SpawnWaitDialog ControlEvent can be used to wait for any background task the completion of which can be tested using a conditional expression such as the state of a property.</span></span> <span data-ttu-id="de48a-119">如需使用 SpawnWaitDialog ControlEvent 的範例，請參閱 [撰寫條件式「請稍候 ...」一節。訊息方塊](authoring-a-conditional-please-wait-------message-box.md)。</span><span class="sxs-lookup"><span data-stu-id="de48a-119">For an example of using the SpawnWaitDialog ControlEvent, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

 

 



