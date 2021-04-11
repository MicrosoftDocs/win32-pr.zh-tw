---
description: 撰寫順序資料表是開發安裝程式封裝不可或缺的一部分，因為這些資料表會指定控制安裝程式和顯示使用者介面對話方塊之標準動作的執行順序。
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: 使用順序資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be10082aba05429a63df69444ed28bea350aa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849468"
---
# <a name="using-a-sequence-table"></a><span data-ttu-id="c2d01-103">使用順序資料表</span><span class="sxs-lookup"><span data-stu-id="c2d01-103">Using a Sequence Table</span></span>

<span data-ttu-id="c2d01-104">撰寫順序資料表是開發安裝程式封裝不可或缺的一部分，因為這些資料表會指定控制安裝程式和顯示使用者介面對話方塊之 [標準動作](standard-actions.md) 的執行順序。</span><span class="sxs-lookup"><span data-stu-id="c2d01-104">The authoring of the sequence tables is an essential part of developing an installer package because these tables specify the order of execution for the [standard actions](standard-actions.md) that control the installation process and display the user interface dialog boxes.</span></span>

<span data-ttu-id="c2d01-105">有三種模式的安裝模式，以及每個模式的順序資料表有兩種類型。</span><span class="sxs-lookup"><span data-stu-id="c2d01-105">There are three modes of installation and two types of sequence tables for each mode.</span></span>

<span data-ttu-id="c2d01-106">安裝程式目前支援的三種不同安裝模式如下：</span><span class="sxs-lookup"><span data-stu-id="c2d01-106">The three separate installation modes currently supported by the installer are:</span></span>

-   <span data-ttu-id="c2d01-107">簡單安裝</span><span class="sxs-lookup"><span data-stu-id="c2d01-107">Simple Installation</span></span>
-   <span data-ttu-id="c2d01-108">系統管理安裝</span><span class="sxs-lookup"><span data-stu-id="c2d01-108">Administrative Installation</span></span>
-   <span data-ttu-id="c2d01-109">公告安裝</span><span class="sxs-lookup"><span data-stu-id="c2d01-109">Advertisement Installation</span></span>

<span data-ttu-id="c2d01-110">順序資料表各有三個欄位： Action、Condition 和 Sequence。</span><span class="sxs-lookup"><span data-stu-id="c2d01-110">The sequence tables each have three fields: Action, Condition, and Sequence.</span></span> <span data-ttu-id="c2d01-111">[動作] 欄位的名稱是標準或自訂動作，或是使用者定義的對話方塊或安裝程式執行的順序。</span><span class="sxs-lookup"><span data-stu-id="c2d01-111">The Action field names either a standard or custom action or a user defined dialog box or sequence the installer executes.</span></span> <span data-ttu-id="c2d01-112">[條件] 欄位可讓作者指定邏輯運算式，以控制是否執行或顯示動作或使用者定義的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c2d01-112">The Condition field allows the author to specify a logical expression that controls whether an action or user-defined dialog is executed or displayed.</span></span> <span data-ttu-id="c2d01-113">如果條件欄位為空白或包含評估結果為 True 的運算式，則會執行或顯示動作或對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c2d01-113">If the Condition field is blank or contains an expression that evaluates to True, the action or dialog is executed or displayed.</span></span> <span data-ttu-id="c2d01-114">如果運算式評估為 False，則會略過動作或對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c2d01-114">The action or dialog is skipped if the expression evaluates to False.</span></span> <span data-ttu-id="c2d01-115">[順序] 欄位指定在資料表中執行每個動作或使用者定義之對話方塊的順序。</span><span class="sxs-lookup"><span data-stu-id="c2d01-115">The Sequence field specifies the order of execution of each action or user-defined dialog in the table.</span></span>

<span data-ttu-id="c2d01-116">上述每一種安裝模式都會處理使用者介面順序資料表和執行順序資料表。</span><span class="sxs-lookup"><span data-stu-id="c2d01-116">Each of these installation modes processes the user interface sequence tables and the execute sequence tables.</span></span> <span data-ttu-id="c2d01-117">只有當安裝程式是以設定為 [縮小] 或 [完整] 的使用者介面顯示層級進行初始化時，才會處理使用者介面順序資料表。</span><span class="sxs-lookup"><span data-stu-id="c2d01-117">The user interface sequence tables are only processed if the installer was initialized with the user interface display level set to Reduced or Full.</span></span> <span data-ttu-id="c2d01-118">如需使用者介面顯示層級的詳細資訊，請參閱 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) 參考。</span><span class="sxs-lookup"><span data-stu-id="c2d01-118">See the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) reference for more information about user interface display levels.</span></span>

<span data-ttu-id="c2d01-119">使用者介面順序資料表通常包含與收集系統資訊（透過使用者介面顯示給使用者的系統資訊）相關的標準動作。</span><span class="sxs-lookup"><span data-stu-id="c2d01-119">The user interface sequence tables typically contains standard actions related to collecting system information that are displayed to the user through the user interface.</span></span> <span data-ttu-id="c2d01-120">將外鍵記錄到使用者介面順序資料表之 [動作] 欄位中 [對話方塊資料表](dialog-table.md) 的對話方塊名稱，即可顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="c2d01-120">The user interface is displayed by recording the foreign keys to the names of dialog boxes in the [dialog table](dialog-table.md) in the Action field of the user interface sequence table.</span></span> <span data-ttu-id="c2d01-121">然後，使用者有機會修改或接受系統資訊，然後開始安裝，這會在執行順序表處理時發生。</span><span class="sxs-lookup"><span data-stu-id="c2d01-121">The user then has the opportunity to modify or accept the system information and begin the installation, which occurs when the execute sequence table is processed.</span></span>

<span data-ttu-id="c2d01-122">在簡單的安裝過程中，會執行 [安裝](install-action.md) 最上層動作，進而處理 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="c2d01-122">During a simple installation, the [INSTALL](install-action.md) top-level action is executed which in turn processes the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

<span data-ttu-id="c2d01-123">系統管理員通常會透過網路系統管理員起始系統管理安裝，為個別使用者和使用者群組指派及安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="c2d01-123">An Administrative Installation is typically initiated by a network administrator to assign and install applications for individual users and groups of users.</span></span> <span data-ttu-id="c2d01-124">在這種安裝類型期間，系統會執行系統 [管理員](admin-action.md) 的最上層動作來處理 [AdminUISequence 資料表](adminuisequence-table.md) 和 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="c2d01-124">During this type of installation, the [ADMIN](admin-action.md) top-level action is executed which processes the [AdminUISequence table](adminuisequence-table.md) and the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>

<span data-ttu-id="c2d01-125">若要 [通告](advertisement.md) 應用程式或功能，必須使用 [通告](advertise-action.md) 動作起始安裝程式。</span><span class="sxs-lookup"><span data-stu-id="c2d01-125">To [advertise](advertisement.md) an application or feature, the installer must be initiated with the [ADVERTISE](advertise-action.md) action.</span></span> <span data-ttu-id="c2d01-126">在這種類型的安裝過程中，會處理 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="c2d01-126">During this type of installation the [AdvtExecuteSequence table](advtexecutesequence-table.md) is processed.</span></span>

<span data-ttu-id="c2d01-127">撰寫任何順序資料表時，最好的作法是使用下列主題中建議序列的標準動作序號。</span><span class="sxs-lookup"><span data-stu-id="c2d01-127">When authoring any sequence table, it is good practice to use the sequence number for standard actions from the suggested sequences in the topics below.</span></span> <span data-ttu-id="c2d01-128">對於順序資料表（例如 [ForceReboot](forcereboot-action.md)、 [ValidateProductID](validateproductid-action.md)和 [InstallExecute](installexecute-action.md)）中沒有標準位置的標準動作，請使用為十的倍數的序號，將動作識別為標準動作。</span><span class="sxs-lookup"><span data-stu-id="c2d01-128">For standard actions which have no standard position in the sequence table such as [ForceReboot](forcereboot-action.md), [ValidateProductID](validateproductid-action.md), and [InstallExecute](installexecute-action.md), use a sequence number that is a multiple of ten to identify the action as a standard action.</span></span> <span data-ttu-id="c2d01-129">若為自訂動作，請使用不是10倍數的序號，以區別順序資料表中的標準動作。</span><span class="sxs-lookup"><span data-stu-id="c2d01-129">For custom actions, use a sequence number that is not a multiple of ten to differentiate it from standard actions in the sequence table.</span></span>

<span data-ttu-id="c2d01-130">如需每個順序資料表的建議動作順序，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="c2d01-130">For suggested action sequences for each sequence table, see the following topics:</span></span>

-   [<span data-ttu-id="c2d01-131">建議的 InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="c2d01-131">Suggested InstallUISequence</span></span>](suggested-installuisequence.md)
-   [<span data-ttu-id="c2d01-132">建議的 InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="c2d01-132">Suggested InstallExecuteSequence</span></span>](suggested-installexecutesequence.md)
-   [<span data-ttu-id="c2d01-133">建議的 AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="c2d01-133">Suggested AdminUISequence</span></span>](suggested-adminuisequence.md)
-   [<span data-ttu-id="c2d01-134">建議的 AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="c2d01-134">Suggested AdminExecuteSequence</span></span>](suggested-adminexecutesequence.md)
-   [<span data-ttu-id="c2d01-135">建議的 AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="c2d01-135">Suggested AdvtUISequence</span></span>](suggested-advtuisequence.md)
-   [<span data-ttu-id="c2d01-136">建議的 AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="c2d01-136">Suggested AdvtExecuteSequence</span></span>](suggested-advtexecutesequence.md)

<span data-ttu-id="c2d01-137">如需順序資料表以及標準動作執行方式的詳細描述，請參閱 [順序資料表詳細的範例](sequence-table-detailed-example.md)。</span><span class="sxs-lookup"><span data-stu-id="c2d01-137">For a detailed description of sequence tables and how standard actions are executed, see the [sequence table detailed example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="c2d01-138">\* \* Windows Installer 3.0 和更新版本： \* \*</span><span class="sxs-lookup"><span data-stu-id="c2d01-138">\*\*Windows Installer 3.0 and later:  \*\*</span></span>

<span data-ttu-id="c2d01-139">從 Windows Installer 3.0 開始，修補封裝可以包含 [MsiPatchSequence 資料表](msipatchsequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="c2d01-139">Beginning with Windows Installer 3.0, a patch package can contain the [MsiPatchSequence table](msipatchsequence-table.md).</span></span> <span data-ttu-id="c2d01-140">此表格包含安裝程式所需的所有資訊，以判斷相對於所有其他修補程式的小型更新修補程式順序。</span><span class="sxs-lookup"><span data-stu-id="c2d01-140">This table contains all the information the installer requires to determine the sequence of the application of a small update patch relative to all other patches.</span></span> <span data-ttu-id="c2d01-141">如需詳細資訊，請參閱 [修補和升級](patching-and-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="c2d01-141">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

> [!Note]
>
> <span data-ttu-id="c2d01-142">[合併模組](merge-modules.md) 可能包含可修改目標 .msi 檔案之動作順序資料表的 [合併模組資料庫資料表](merge-module-database-tables.md) 。</span><span class="sxs-lookup"><span data-stu-id="c2d01-142">[Merge Modules](merge-modules.md) may contain [Merge Module Database Tables](merge-module-database-tables.md) that modify the action sequence tables of the target .msi file.</span></span> <span data-ttu-id="c2d01-143">將模組合併到資料庫中可以修改 sequence 資料表中的資訊，但不會將這些資料表加入至 .msi 檔案。</span><span class="sxs-lookup"><span data-stu-id="c2d01-143">Merging the module into a database can modify the information in the sequence table, but does not add these tables to the .msi file.</span></span> <span data-ttu-id="c2d01-144">如需詳細資訊，請參閱 [撰寫合併模組順序資料表](authoring-merge-module-sequence-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="c2d01-144">For more information, see [Authoring Merge Module Sequence Tables](authoring-merge-module-sequence-tables.md).</span></span>

 

 

 



