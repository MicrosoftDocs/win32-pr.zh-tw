---
description: 如果合併模組必須修改目標 .msi 檔案的動作順序資料表，請在 .msm 檔案中包含 MergeModuleSequence 資料表。 合併不會將這些資料表加入至 .msi 檔案。 這些資料表只會出現在合併模組中。
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: 撰寫合併模組順序資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b21780601e626c006967cefa0dcff5700bdec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944010"
---
# <a name="authoring-merge-module-sequence-tables"></a><span data-ttu-id="f950b-105">撰寫合併模組順序資料表</span><span class="sxs-lookup"><span data-stu-id="f950b-105">Authoring Merge Module Sequence Tables</span></span>

<span data-ttu-id="f950b-106">如果合併模組必須修改目標 .msi 檔案的動作 [*順序資料表*](s-gly.md) ，請在 .msm 檔案中包含 MergeModuleSequence 資料表。</span><span class="sxs-lookup"><span data-stu-id="f950b-106">Include the MergeModuleSequence tables in the .msm file if the merge module must modify the action [*sequence tables*](s-gly.md) of the target .msi file.</span></span> <span data-ttu-id="f950b-107">合併不會將這些資料表加入至 .msi 檔案。</span><span class="sxs-lookup"><span data-stu-id="f950b-107">Merging does not add these tables to the .msi file.</span></span> <span data-ttu-id="f950b-108">這些資料表只會出現在合併模組中。</span><span class="sxs-lookup"><span data-stu-id="f950b-108">These tables only occur in merge modules.</span></span>

<span data-ttu-id="f950b-109">如果有任何 ModuleSequence 資料表存在於 .msm 檔案中，則您也必須將對應的安裝程式順序資料表的空白複本撰寫至合併模組。</span><span class="sxs-lookup"><span data-stu-id="f950b-109">If any of the ModuleSequence tables are present in an .msm file, an empty copy of the corresponding installer sequence table must also be authored into the merge module.</span></span> <span data-ttu-id="f950b-110">例如，如果 merge 模組包含 ModuleAdminExecuteSequence 資料表，則合併模組也必須包含空的 AdminExecuteSequence 資料表。</span><span class="sxs-lookup"><span data-stu-id="f950b-110">For example, if a merge module contains a ModuleAdminExecuteSequence table, the merge module must also include an empty AdminExecuteSequence table.</span></span> <span data-ttu-id="f950b-111">在合併期間，這些空白資料表會以必要的架構指導方針提供合併工具。</span><span class="sxs-lookup"><span data-stu-id="f950b-111">During a merge, these empty tables provide the merge tool with necessary schema guidelines.</span></span>

<span data-ttu-id="f950b-112">在合併模組順序資料表中使用 [標準動作](standard-actions.md) 時，[順序] 資料行中的值應該是標準動作的建議動作序號。</span><span class="sxs-lookup"><span data-stu-id="f950b-112">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number for the standard action.</span></span> <span data-ttu-id="f950b-113">請參閱下面提供的建議動作順序，以取得每個順序資料表中的建議序號。</span><span class="sxs-lookup"><span data-stu-id="f950b-113">See the suggested action sequences given below for the recommended sequence numbers in each sequence table.</span></span> <span data-ttu-id="f950b-114">如果 merge module sequence 資料表中的序號與 .msi 檔案中相同動作的序號不同，則合併工具會在合併期間使用 .msi 檔案中的序號。</span><span class="sxs-lookup"><span data-stu-id="f950b-114">If the sequence number in the merge module sequence table differs from the sequence number for the same action in the .msi file, the merge tool uses the sequence number in the .msi file during the merge.</span></span>



| <span data-ttu-id="f950b-115">MergeModuleSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="f950b-115">MergeModuleSequence table</span></span>                                                    | <span data-ttu-id="f950b-116">建議的動作順序</span><span class="sxs-lookup"><span data-stu-id="f950b-116">Recommended action sequences</span></span>                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="f950b-117">ModuleAdminUISequence</span><span class="sxs-lookup"><span data-stu-id="f950b-117">ModuleAdminUISequence</span></span>](moduleadminuisequence-table.md)                     | [<span data-ttu-id="f950b-118">建議的 AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="f950b-118">Suggested AdminUISequence</span></span>](suggested-adminuisequence.md)               |
| [<span data-ttu-id="f950b-119">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f950b-119">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)           | [<span data-ttu-id="f950b-120">建議的 AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f950b-120">Suggested AdminExecuteSequence</span></span>](suggested-adminexecutesequence.md)     |
| [<span data-ttu-id="f950b-121">ModuleAdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="f950b-121">ModuleAdvtUISequence</span></span>](moduleadvtuisequence-table.md)                       | [<span data-ttu-id="f950b-122">建議的 AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="f950b-122">Suggested AdvtUISequence</span></span>](suggested-advtuisequence.md)                 |
| [<span data-ttu-id="f950b-123">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f950b-123">ModuleAdvtExecuteSequence</span></span>](moduleadvtexecutesequence-table.md)             | [<span data-ttu-id="f950b-124">建議的 AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f950b-124">Suggested AdvtExecuteSequence</span></span>](suggested-advtexecutesequence.md)       |
| [<span data-ttu-id="f950b-125">ModuleInstallUISequence</span><span class="sxs-lookup"><span data-stu-id="f950b-125">ModuleInstallUISequence</span></span>](moduleinstalluisequence-table.md)                 | [<span data-ttu-id="f950b-126">建議的 InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="f950b-126">Suggested InstallUISequence</span></span>](suggested-installuisequence.md)           |
| [<span data-ttu-id="f950b-127">ModuleInstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="f950b-127">ModuleInstallExecuteSequence table</span></span>](moduleinstallexecutesequence-table.md) | [<span data-ttu-id="f950b-128">建議的 InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f950b-128">Suggested InstallExecuteSequence</span></span>](suggested-installexecutesequence.md) |



 

<span data-ttu-id="f950b-129">如果在 merge module sequence 資料表的動作資料行中使用 [標準動作](standard-actions.md) ，則該記錄的 BaseAction 和 After 資料行必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="f950b-129">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be Null.</span></span>

<span data-ttu-id="f950b-130">如果自訂動作或對話方塊輸入到 [動作] 資料行中，則 [順序] 資料行必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="f950b-130">If a custom action or dialog is entered into the Action column, the Sequence column must be Null.</span></span>

<span data-ttu-id="f950b-131">如果在 [動作] 資料行中輸入傳回終止旗標的動作，[順序] 資料行應該會包含該旗標的負數值，且該記錄的 BaseAction 和 After 資料行必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="f950b-131">If an action returning a termination flag is entered into the Action column, the Sequence column should contain the negative value for that flag and the BaseAction and After columns of that record must be Null.</span></span> <span data-ttu-id="f950b-132">下列負數值表示如果安裝程式傳回終止旗標，則會呼叫動作。</span><span class="sxs-lookup"><span data-stu-id="f950b-132">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span>



| <span data-ttu-id="f950b-133">終止旗標</span><span class="sxs-lookup"><span data-stu-id="f950b-133">Termination flag</span></span>          | <span data-ttu-id="f950b-134">值</span><span class="sxs-lookup"><span data-stu-id="f950b-134">Value</span></span> | <span data-ttu-id="f950b-135">描述</span><span class="sxs-lookup"><span data-stu-id="f950b-135">Description</span></span>              |
|---------------------------|-------|--------------------------|
| <span data-ttu-id="f950b-136">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="f950b-136">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="f950b-137">-1</span><span class="sxs-lookup"><span data-stu-id="f950b-137">-1</span></span>    | <span data-ttu-id="f950b-138">順利完成。</span><span class="sxs-lookup"><span data-stu-id="f950b-138">Successful completion.</span></span>   |
| <span data-ttu-id="f950b-139">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="f950b-139">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="f950b-140">-2</span><span class="sxs-lookup"><span data-stu-id="f950b-140">-2</span></span>    | <span data-ttu-id="f950b-141">使用者終止安裝。</span><span class="sxs-lookup"><span data-stu-id="f950b-141">User terminates install.</span></span> |
| <span data-ttu-id="f950b-142">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="f950b-142">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="f950b-143">-3</span><span class="sxs-lookup"><span data-stu-id="f950b-143">-3</span></span>    | <span data-ttu-id="f950b-144">嚴重結束終止。</span><span class="sxs-lookup"><span data-stu-id="f950b-144">Fatal exit terminates.</span></span>   |
| <span data-ttu-id="f950b-145">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="f950b-145">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="f950b-146">-4</span><span class="sxs-lookup"><span data-stu-id="f950b-146">-4</span></span>    | <span data-ttu-id="f950b-147">安裝已暫停。</span><span class="sxs-lookup"><span data-stu-id="f950b-147">Install is suspended.</span></span>    |



 

<span data-ttu-id="f950b-148">BaseAction 資料行可包含標準動作、在合併模組的自訂動作資料表中指定的自訂動作，或在模組的對話方塊資料表中指定的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f950b-148">The BaseAction column can contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="f950b-149">BaseAction 資料行是此資料表之 [動作] 資料行中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f950b-149">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="f950b-150">它不能是 .msi 檔案中其他合併資料表或資料表的外鍵。</span><span class="sxs-lookup"><span data-stu-id="f950b-150">It cannot be a foreign key into another merge table or table in the .msi file.</span></span> <span data-ttu-id="f950b-151">這表示 BaseAction 資料行中所列的每個標準動作、自訂動作或對話方塊，也必須列在此資料表中另一筆記錄的 [動作] 資料行中。</span><span class="sxs-lookup"><span data-stu-id="f950b-151">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

 

 



