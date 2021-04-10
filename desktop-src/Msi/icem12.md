---
description: ICEM12 會確認在 ModuleSequence 資料表中，標準動作具有序號和自訂動作具有 BaseAction 和之後的值。
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026358"
---
# <a name="icem12"></a><span data-ttu-id="7c8b4-103">ICEM12</span><span class="sxs-lookup"><span data-stu-id="7c8b4-103">ICEM12</span></span>

<span data-ttu-id="7c8b4-104">ICEM12 會確認在 ModuleSequence 資料表中，標準動作具有序號和自訂動作具有 BaseAction 和之後的值。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-104">ICEM12 verifies that in a ModuleSequence table, standard actions have sequence numbers and custom actions have BaseAction and After values.</span></span>

<span data-ttu-id="7c8b4-105">此 ICEM 可在 Windows Installer 2.0 SDK 和更新版本提供的 Mergemod 檔中找到。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-105">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="7c8b4-106">如需詳細資訊，請參閱 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-106">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="7c8b4-107">結果</span><span class="sxs-lookup"><span data-stu-id="7c8b4-107">Result</span></span>

<span data-ttu-id="7c8b4-108">ICEM12 會在下列情況下張貼錯誤：</span><span class="sxs-lookup"><span data-stu-id="7c8b4-108">ICEM12 posts an error in the following cases:</span></span>

-   <span data-ttu-id="7c8b4-109">它會尋找模組包含沒有序號的 [標準動作](standard-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-109">It finds the module contains a [standard action](standard-actions.md) without a sequence number.</span></span>
-   <span data-ttu-id="7c8b4-110">它會發現標準動作具有在 [ModuleAdminUISequence 資料表](moduleadminuisequence-table.md)、 [ModuleAdminExecuteSequence 資料表](moduleadminexecutesequence-table.md)、 [ModuleAdvtExecuteSequence 資料表](moduleadvtexecutesequence-table.md)、 [ModuleInstallUISequence 資料表](moduleinstalluisequence-table.md)或 [ModuleInstallExecuteSequence 資料表](moduleinstallexecutesequence-table.md)的 BaseAction 或 After 欄位中輸入的值。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-110">It finds that a standard action has values entered in the BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>
-   <span data-ttu-id="7c8b4-111">它會尋找模組包含 [自訂動作](custom-actions.md) ，而不會在 BaseAction 或 [ModuleAdminUISequence 資料表](moduleadminuisequence-table.md)、 [ModuleAdminExecuteSequence 資料表](moduleadminexecutesequence-table.md)、 [ModuleAdvtExecuteSequence 資料表](moduleadvtexecutesequence-table.md)、 [ModuleInstallUISequence 資料表](moduleinstalluisequence-table.md)或 [ModuleInstallExecuteSequence 資料表](moduleinstallexecutesequence-table.md)的欄位中輸入任何值。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-111">It finds the module contains a [custom action](custom-actions.md) without any values entered into the Sequence, BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>

<span data-ttu-id="7c8b4-112">ICEM12 會在找到指定序號的自訂動作時張貼警告，但不會在 BaseAction 或 After 欄位中提供任何值。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-112">ICEM12 posts a warning if it finds a custom action that has a Sequence number specified, but no value in the BaseAction or After fields.</span></span>

<span data-ttu-id="7c8b4-113">請注意，在 [CustomAction 資料表](customaction-table.md) 中找到的所有動作都會視為自訂動作。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-113">Note that all actions found in the [CustomAction table](customaction-table.md) are considered custom actions.</span></span> <span data-ttu-id="7c8b4-114">所有其他動作都會視為標準動作。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-114">All other action are considered standard actions.</span></span>

## <a name="example"></a><span data-ttu-id="7c8b4-115">範例</span><span class="sxs-lookup"><span data-stu-id="7c8b4-115">Example</span></span>

<span data-ttu-id="7c8b4-116">ICEM12 會針對包含如下所示之資料庫專案的模組，張貼下列錯誤和警告訊息：</span><span class="sxs-lookup"><span data-stu-id="7c8b4-116">ICEM12 posts the following error and warning messages for a module that contains the database entries shown below:</span></span>

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[<span data-ttu-id="7c8b4-117">CustomAction</span><span class="sxs-lookup"><span data-stu-id="7c8b4-117">CustomAction</span></span>](customaction-table.md)



| <span data-ttu-id="7c8b4-118">動作</span><span class="sxs-lookup"><span data-stu-id="7c8b4-118">Action</span></span>  | <span data-ttu-id="7c8b4-119">類型</span><span class="sxs-lookup"><span data-stu-id="7c8b4-119">Type</span></span> | <span data-ttu-id="7c8b4-120">來源</span><span class="sxs-lookup"><span data-stu-id="7c8b4-120">Source</span></span>  | <span data-ttu-id="7c8b4-121">目標</span><span class="sxs-lookup"><span data-stu-id="7c8b4-121">Target</span></span>  |
|---------|------|---------|---------|
| <span data-ttu-id="7c8b4-122">Action1</span><span class="sxs-lookup"><span data-stu-id="7c8b4-122">Action1</span></span> | <span data-ttu-id="7c8b4-123">30</span><span class="sxs-lookup"><span data-stu-id="7c8b4-123">30</span></span>   | <span data-ttu-id="7c8b4-124">source1.rc</span><span class="sxs-lookup"><span data-stu-id="7c8b4-124">source1</span></span> | <span data-ttu-id="7c8b4-125">target1</span><span class="sxs-lookup"><span data-stu-id="7c8b4-125">target1</span></span> |
| <span data-ttu-id="7c8b4-126">Action3</span><span class="sxs-lookup"><span data-stu-id="7c8b4-126">Action3</span></span> | <span data-ttu-id="7c8b4-127">30</span><span class="sxs-lookup"><span data-stu-id="7c8b4-127">30</span></span>   | <span data-ttu-id="7c8b4-128">source3</span><span class="sxs-lookup"><span data-stu-id="7c8b4-128">source3</span></span> | <span data-ttu-id="7c8b4-129">target3</span><span class="sxs-lookup"><span data-stu-id="7c8b4-129">target3</span></span> |



 

[<span data-ttu-id="7c8b4-130">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="7c8b4-130">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)



| <span data-ttu-id="7c8b4-131">動作</span><span class="sxs-lookup"><span data-stu-id="7c8b4-131">Action</span></span>  | <span data-ttu-id="7c8b4-132">順序</span><span class="sxs-lookup"><span data-stu-id="7c8b4-132">Sequence</span></span> | <span data-ttu-id="7c8b4-133">BaseAction</span><span class="sxs-lookup"><span data-stu-id="7c8b4-133">BaseAction</span></span> | <span data-ttu-id="7c8b4-134">After</span><span class="sxs-lookup"><span data-stu-id="7c8b4-134">After</span></span> | <span data-ttu-id="7c8b4-135">條件</span><span class="sxs-lookup"><span data-stu-id="7c8b4-135">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="7c8b4-136">Action2</span><span class="sxs-lookup"><span data-stu-id="7c8b4-136">Action2</span></span> |          | <span data-ttu-id="7c8b4-137">Action1</span><span class="sxs-lookup"><span data-stu-id="7c8b4-137">Action1</span></span>    | <span data-ttu-id="7c8b4-138">1</span><span class="sxs-lookup"><span data-stu-id="7c8b4-138">1</span></span>     | <span data-ttu-id="7c8b4-139">true</span><span class="sxs-lookup"><span data-stu-id="7c8b4-139">true</span></span>      |
| <span data-ttu-id="7c8b4-140">Action3</span><span class="sxs-lookup"><span data-stu-id="7c8b4-140">Action3</span></span> |          |            |       | <span data-ttu-id="7c8b4-141">true</span><span class="sxs-lookup"><span data-stu-id="7c8b4-141">true</span></span>      |



 

[<span data-ttu-id="7c8b4-142">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="7c8b4-142">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="7c8b4-143">動作</span><span class="sxs-lookup"><span data-stu-id="7c8b4-143">Action</span></span>  | <span data-ttu-id="7c8b4-144">順序</span><span class="sxs-lookup"><span data-stu-id="7c8b4-144">Sequence</span></span> | <span data-ttu-id="7c8b4-145">BaseAction</span><span class="sxs-lookup"><span data-stu-id="7c8b4-145">BaseAction</span></span> | <span data-ttu-id="7c8b4-146">After</span><span class="sxs-lookup"><span data-stu-id="7c8b4-146">After</span></span> | <span data-ttu-id="7c8b4-147">條件</span><span class="sxs-lookup"><span data-stu-id="7c8b4-147">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="7c8b4-148">Action1</span><span class="sxs-lookup"><span data-stu-id="7c8b4-148">Action1</span></span> | <span data-ttu-id="7c8b4-149">1</span><span class="sxs-lookup"><span data-stu-id="7c8b4-149">1</span></span>        |            |       | <span data-ttu-id="7c8b4-150">true</span><span class="sxs-lookup"><span data-stu-id="7c8b4-150">true</span></span>      |



 

<span data-ttu-id="7c8b4-151">若要修正這些錯誤，請嘗試下列動作：</span><span class="sxs-lookup"><span data-stu-id="7c8b4-151">To fix these errors try the following:</span></span>

-   <span data-ttu-id="7c8b4-152">移除自訂動作 Action1 的序號，並改為使用 BaseAction 和 After 欄位。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-152">Remove the sequence number for the custom action Action1 and use the BaseAction and After fields instead.</span></span>
-   <span data-ttu-id="7c8b4-153">在 [順序]、[BaseAction] 或 [自訂動作 Action3 的欄位] 欄位中輸入值。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-153">Enter values into the Sequence, BaseAction, or After fields for the custom action Action3.</span></span> <span data-ttu-id="7c8b4-154">將 [BaseAction] 和 [After] 欄位保留為 [標準動作 Action2]。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-154">Leave the BaseAction and After fields empty for standard action Action2.</span></span>
-   <span data-ttu-id="7c8b4-155">請勿將 [順序] 欄位保留為 [標準動作 Action2]。</span><span class="sxs-lookup"><span data-stu-id="7c8b4-155">Do not leave the Sequence field empty for standard action Action2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c8b4-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c8b4-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c8b4-157">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="7c8b4-157">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



