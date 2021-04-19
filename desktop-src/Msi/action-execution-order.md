---
description: 動作執行的順序取決於已撰寫至順序資料表的動作順序，以及安裝程式執行順序資料表的順序。
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: 動作執行順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954c44f6e2525deb3375cb9ea72d0320df3a5f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979108"
---
# <a name="action-execution-order"></a><span data-ttu-id="72264-103">動作執行順序</span><span class="sxs-lookup"><span data-stu-id="72264-103">Action Execution Order</span></span>

<span data-ttu-id="72264-104">動作執行的順序取決於已撰寫至 [*順序資料表*](s-gly.md) 的動作順序，以及安裝程式執行順序資料表的順序。</span><span class="sxs-lookup"><span data-stu-id="72264-104">The order of action execution is determined by the sequence of actions that have been authored into the [*sequence tables*](s-gly.md) and by the order in which the installer runs the sequence tables.</span></span> <span data-ttu-id="72264-105">如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)中的建議動作順序。</span><span class="sxs-lookup"><span data-stu-id="72264-105">For details, see the suggested action sequences in [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="72264-106">安裝程式會執行順序表格，以回應安裝、 [通告](advertisement.md)或系統 [管理安裝](administrative-installation.md)的要求。</span><span class="sxs-lookup"><span data-stu-id="72264-106">The installer runs sequence tables in response to a request for an installation, [advertisement](advertisement.md), or an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="72264-107">例如，回應使用/I、/J 或/A [命令列選項](command-line-options.md)時，不會從動作順序內呼叫 [安裝](install-action.md)、 [公告](advertise-action.md)和系統 [管理](admin-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="72264-107">For example, in response to using the /I, /J, or /A [command line options](command-line-options.md), the [INSTALL](install-action.md), [ADVERTISE](advertise-action.md), and [ADMIN](admin-action.md) actions are not called from within the action sequence.</span></span> <span data-ttu-id="72264-108">當安裝程式初始化時，這些高階動作會改傳遞給安裝程式。</span><span class="sxs-lookup"><span data-stu-id="72264-108">These high-level actions are instead passed to the installer when the installer is initialized.</span></span>

<span data-ttu-id="72264-109">如果安裝程式已通過安裝動作，且已使用使用者介面撰寫安裝套件，則安裝程式會先在 [InstallUISequence 資料表](installuisequence-table.md) 中執行動作，然後依序執行 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 中的動作。</span><span class="sxs-lookup"><span data-stu-id="72264-109">If the installer is passed the INSTALL action and the installation package has been authored with a user interface, the installer first runs the actions in [InstallUISequence table](installuisequence-table.md) and then executes the actions in the [InstallExecuteSequence table](installexecutesequence-table.md) in order.</span></span> <span data-ttu-id="72264-110">如果封裝沒有使用者介面，則安裝程式會依序執行 InstallExecuteSequence 資料表中的動作。</span><span class="sxs-lookup"><span data-stu-id="72264-110">If the package has no user interface, the installer executes the actions in the InstallExecuteSequence table in order.</span></span>

<span data-ttu-id="72264-111">如果已將系統管理員動作傳遞給安裝程式，而且已使用使用者介面來撰寫安裝套件，則安裝程式會先執行 [AdminUISequence 資料表](adminuisequence-table.md) ，然後執行 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="72264-111">If the installer is passed the ADMIN action, and the installation package has been authored with a user interface, the installer first runs the [AdminUISequence table](adminuisequence-table.md) and then runs the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="72264-112">如果封裝沒有使用者介面，則安裝程式會執行 AdminExecute 資料表。</span><span class="sxs-lookup"><span data-stu-id="72264-112">If the package has no user interface, the installer runs the AdminExecute table.</span></span>

<span data-ttu-id="72264-113">如果將公告動作傳遞給安裝程式，安裝程式就會執行 [AdvtExecuteSequence](advtexecutesequence-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="72264-113">If the installer is passed the ADVERTISE action, the installer runs the [AdvtExecuteSequence](advtexecutesequence-table.md) table.</span></span>

> [!Note]  
> <span data-ttu-id="72264-114">安裝程式不會使用 [AdvtUISequence](advtuisequence-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="72264-114">The installer does not use the [AdvtUISequence](advtuisequence-table.md) table.</span></span> <span data-ttu-id="72264-115">AdvtUISequence 資料表不應該存在於安裝資料庫中，也不應該保留空白。</span><span class="sxs-lookup"><span data-stu-id="72264-115">The AdvtUISequence table should not exist in the installation database or it should be left empty.</span></span>

 

<span data-ttu-id="72264-116">當安裝程式執行順序資料表時，它會依照 Sequence 資料行中所列序號的順序來執行動作。</span><span class="sxs-lookup"><span data-stu-id="72264-116">When the installer runs a sequence table, it executes actions in the order of the sequence numbers listed in the Sequence column.</span></span> <span data-ttu-id="72264-117">動作順序一律為線性，沒有分支或迴圈。</span><span class="sxs-lookup"><span data-stu-id="72264-117">The action order is always linear with no branching or looping.</span></span> <span data-ttu-id="72264-118">封裝開發人員可以藉由在 [條件] 資料行中撰寫邏輯運算式，有條件地防止執行特定動作。</span><span class="sxs-lookup"><span data-stu-id="72264-118">Package developers can conditionally prevent a particular action from being executed by authoring a logical expression into the Condition column.</span></span> <span data-ttu-id="72264-119">當條件評估為 False 時，安裝程式會略過動作。</span><span class="sxs-lookup"><span data-stu-id="72264-119">The installer skips the action whenever the condition evaluates to False.</span></span> <span data-ttu-id="72264-120">請參閱 [使用順序資料表](using-a-sequence-table.md) 和 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="72264-120">See [Using a Sequence Table](using-a-sequence-table.md) and [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="72264-121">所有順序資料表都有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="72264-121">All sequence tables have the following columns.</span></span>



| <span data-ttu-id="72264-122">Column</span><span class="sxs-lookup"><span data-stu-id="72264-122">Column</span></span>    | <span data-ttu-id="72264-123">描述</span><span class="sxs-lookup"><span data-stu-id="72264-123">Description</span></span>                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72264-124">動作</span><span class="sxs-lookup"><span data-stu-id="72264-124">Action</span></span>    | <span data-ttu-id="72264-125">資料表的主鍵;動作名稱必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="72264-125">The primary key for the table; the action name must be unique.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="72264-126">條件</span><span class="sxs-lookup"><span data-stu-id="72264-126">Condition</span></span> | <span data-ttu-id="72264-127">用來判斷是否要執行動作的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="72264-127">A Boolean expression used to determine whether to perform the action.</span></span> <span data-ttu-id="72264-128">如果此欄位為空白或包含評估結果為 True 的運算式，則會執行此動作。</span><span class="sxs-lookup"><span data-stu-id="72264-128">The action is executed if this field is either blank or contains an expression that evaluates to True.</span></span> <span data-ttu-id="72264-129">如果運算式評估為 False，則不會執行動作。</span><span class="sxs-lookup"><span data-stu-id="72264-129">The action is not executed if the expression evaluates to False.</span></span> |
| <span data-ttu-id="72264-130">順序</span><span class="sxs-lookup"><span data-stu-id="72264-130">Sequence</span></span>  | <span data-ttu-id="72264-131">用來決定執行動作之順序的相對序號。</span><span class="sxs-lookup"><span data-stu-id="72264-131">A relative sequence number used to determine the order in which actions are executed.</span></span>                                                                                                                                                         |



 

 

 



