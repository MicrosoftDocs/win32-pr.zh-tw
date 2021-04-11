---
description: ICEM09 會驗證合併模組是否安全地處理預先定義的目錄。
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193686"
---
# <a name="icem09"></a><span data-ttu-id="c6546-103">ICEM09</span><span class="sxs-lookup"><span data-stu-id="c6546-103">ICEM09</span></span>

<span data-ttu-id="c6546-104">ICEM09 會驗證合併模組是否安全地處理預先定義的目錄。</span><span class="sxs-lookup"><span data-stu-id="c6546-104">ICEM09 verifies the merge module safely handles predefined directories.</span></span> <span data-ttu-id="c6546-105">它是藉由確認模組中的任何元件，將目錄安裝到預先定義的系統目錄（例如 "ProgramFilesFolder" 或 "StartMenuFolder"）來完成這項工作。</span><span class="sxs-lookup"><span data-stu-id="c6546-105">It does this by verifying that no component in the module installs a directory to a predefined system directory such as "ProgramFilesFolder" or "StartMenuFolder".</span></span> <span data-ttu-id="c6546-106">相反地，模組應該使用具有唯一名稱的目錄， (使用合併模組命名慣例來建立) 並使用自訂動作將目標設為適當的目標目錄。</span><span class="sxs-lookup"><span data-stu-id="c6546-106">Instead, modules should use directories with unique names (created with the merge module naming convention) and use custom actions to target the appropriate target directory.</span></span> <span data-ttu-id="c6546-107">這種方法可防止模組與最終資料庫中現有的目錄結構衝突。</span><span class="sxs-lookup"><span data-stu-id="c6546-107">This approach prevents modules from conflicting with an existing directory structure in the final database.</span></span> <span data-ttu-id="c6546-108">ICEM09 會檢查這項技術是否 (所需的自訂動作是否存在，讓合併工具可以) 或以正確的格式 (產生這些動作，以) 的方式運作。</span><span class="sxs-lookup"><span data-stu-id="c6546-108">ICEM09 checks that the custom actions needed for this technique to work either do not exist (so that the merge tool can generate them) or exist in the correct form (so that they work as expected).</span></span>

<span data-ttu-id="c6546-109">若無法修正 ICEM09 回報的警告或錯誤，可能會導致合併模組的用戶端發生問題。</span><span class="sxs-lookup"><span data-stu-id="c6546-109">Failure to fix a warning or error reported by ICEM09 could cause problems for the clients of your merge module.</span></span> <span data-ttu-id="c6546-110">具有主鍵的目錄資料表資料列（例如 ProgramFilesFolder）通常存在於資料庫中;因此，如果您模組中的元件會直接安裝到預先定義的目錄（例如 ProgramFilesFolder），則模組中的目錄專案可能會與現有的資料列相衝突。</span><span class="sxs-lookup"><span data-stu-id="c6546-110">Directory table rows with primary keys such as ProgramFilesFolder often exist in a database; therefore, if components in your module install directly to predefined directories such as ProgramFilesFolder, the directory entries in the module may collide with already existing rows.</span></span> <span data-ttu-id="c6546-111">這種情況會要求您的模組使用者必須從您的模組分割原始程式檔，才能符合現有的來原始目錄。</span><span class="sxs-lookup"><span data-stu-id="c6546-111">This condition would require the user of your module to split the source files from your module in order to match the existing source directory.</span></span>

## <a name="result"></a><span data-ttu-id="c6546-112">結果</span><span class="sxs-lookup"><span data-stu-id="c6546-112">Result</span></span>

<span data-ttu-id="c6546-113">當模組元件將目錄安裝到預先定義的系統目錄時，ICEM09 會報告錯誤或警告，導致可能與現有目錄結構發生名稱衝突。</span><span class="sxs-lookup"><span data-stu-id="c6546-113">ICEM09 reports an error or warning when a module component installs a directory to a pre-defined system directory, causing a possible name conflict with the existing directory structure.</span></span>

## <a name="example"></a><span data-ttu-id="c6546-114">範例</span><span class="sxs-lookup"><span data-stu-id="c6546-114">Example</span></span>

<span data-ttu-id="c6546-115">ICEM09 會針對包含所顯示資料庫專案的模組張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="c6546-115">ICEM09 posts the following warnings for a module containing the database entries shown.</span></span>

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

<span data-ttu-id="c6546-116">重新命名合併模組目錄，使其不符合 Windows Installer 屬性，因此是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c6546-116">Rename the merge module directory so it does not match a Windows Installer property and therefore is unique.</span></span> <span data-ttu-id="c6546-117">然後，將相同名稱的屬性設定為 Windows Installer 目錄的值。</span><span class="sxs-lookup"><span data-stu-id="c6546-117">Then set a property of the same name to the value of the Windows Installer directory.</span></span> <span data-ttu-id="c6546-118">進行目錄解析時，目錄具有相同名稱的屬性，因此目錄的安裝位置是屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c6546-118">When directory resolution takes place, the directory has a property of the same name, so the install location of the directory is the value of the property.</span></span> <span data-ttu-id="c6546-119">檔案會從相異來源位置移至相同的目標位置。</span><span class="sxs-lookup"><span data-stu-id="c6546-119">Files move from the distinct source location to the same target location.</span></span> <span data-ttu-id="c6546-120">此程式應完全移除合併衝突。</span><span class="sxs-lookup"><span data-stu-id="c6546-120">This process should completely remove the merge conflicts.</span></span>

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

<span data-ttu-id="c6546-121">如果動作沒有序號1，它可能不會在順序中提早合併到目標資料庫，以便有效地運作。</span><span class="sxs-lookup"><span data-stu-id="c6546-121">If the action does not have sequence number 1, it may not merge in to the target database early enough in the sequence to work effectively.</span></span>

<span data-ttu-id="c6546-122">若要修正此警告，請將序號設為1。</span><span class="sxs-lookup"><span data-stu-id="c6546-122">To fix this warning, set the sequence number to 1.</span></span> <span data-ttu-id="c6546-123">請注意，最新的合併工具 (但不是某些舊版的) 將會在合併時間產生這些自訂動作，因此不一定需要明確地將動作撰寫到合併模組。</span><span class="sxs-lookup"><span data-stu-id="c6546-123">Note that most current merge tools (but not some older versions) will generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

<span data-ttu-id="c6546-124">由於 CustomAction 資料行是 CustomAction 資料表的主要索引鍵，因此某些合併工具可能會產生重複的動作，因為預先撰寫的動作名稱是不同的。</span><span class="sxs-lookup"><span data-stu-id="c6546-124">Because the CustomAction column is the primary key of CustomAction table, some merge tools may generate duplicate actions because the pre-authored action name is different.</span></span>

<span data-ttu-id="c6546-125">若要修正此警告，請將動作命名為與目標目錄相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6546-125">To fix this warning, name the action the same as the target directory.</span></span> <span data-ttu-id="c6546-126">請注意，最新的合併工具 (但不是某些較舊的版本) 在合併時間產生這些自訂動作，因此不一定需要明確地將動作撰寫到合併模組。</span><span class="sxs-lookup"><span data-stu-id="c6546-126">Note that most current merge tools (but not some older versions) generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

[<span data-ttu-id="c6546-127">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="c6546-127">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="c6546-128">目錄</span><span class="sxs-lookup"><span data-stu-id="c6546-128">Directory</span></span>          | <span data-ttu-id="c6546-129">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="c6546-129">Directory\_Parent</span></span> | <span data-ttu-id="c6546-130">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="c6546-130">DefaultDir</span></span> |
|--------------------|-------------------|------------|
| <span data-ttu-id="c6546-131">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="c6546-131">ProgramFilesFolder</span></span> | <span data-ttu-id="c6546-132">Directory1</span><span class="sxs-lookup"><span data-stu-id="c6546-132">Directory1</span></span>        | <span data-ttu-id="c6546-133">A</span><span class="sxs-lookup"><span data-stu-id="c6546-133">A</span></span>          |
| <span data-ttu-id="c6546-134">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="c6546-134">StartMenuFolder</span></span>    | <span data-ttu-id="c6546-135">Directory2</span><span class="sxs-lookup"><span data-stu-id="c6546-135">Directory2</span></span>        | <span data-ttu-id="c6546-136">B:C</span><span class="sxs-lookup"><span data-stu-id="c6546-136">B:C</span></span>        |
| <span data-ttu-id="c6546-137">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="c6546-137">AppDataFolder</span></span>      | <span data-ttu-id="c6546-138">Directory3</span><span class="sxs-lookup"><span data-stu-id="c6546-138">Directory3</span></span>        | <span data-ttu-id="c6546-139">D</span><span class="sxs-lookup"><span data-stu-id="c6546-139">D</span></span>          |
| <span data-ttu-id="c6546-140">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="c6546-140">MyPicturesFolder</span></span>   | <span data-ttu-id="c6546-141">Directory4</span><span class="sxs-lookup"><span data-stu-id="c6546-141">Directory4</span></span>        | <span data-ttu-id="c6546-142">E</span><span class="sxs-lookup"><span data-stu-id="c6546-142">E</span></span>          |



 

[<span data-ttu-id="c6546-143">元件資料表</span><span class="sxs-lookup"><span data-stu-id="c6546-143">Component Table</span></span>](component-table.md)



| <span data-ttu-id="c6546-144">元件</span><span class="sxs-lookup"><span data-stu-id="c6546-144">Component</span></span>               | <span data-ttu-id="c6546-145">目錄</span><span class="sxs-lookup"><span data-stu-id="c6546-145">Directory</span></span>          |
|-------------------------|--------------------|
| <span data-ttu-id="c6546-146">Component1.<GUID></span><span class="sxs-lookup"><span data-stu-id="c6546-146">Component1.<GUID></span></span> | <span data-ttu-id="c6546-147">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="c6546-147">ProgramFilesFolder</span></span> |
| <span data-ttu-id="c6546-148">Component2.<GUID></span><span class="sxs-lookup"><span data-stu-id="c6546-148">Component2.<GUID></span></span> | <span data-ttu-id="c6546-149">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="c6546-149">StartMenuFolder</span></span>    |
| <span data-ttu-id="c6546-150">Component3.<GUID></span><span class="sxs-lookup"><span data-stu-id="c6546-150">Component3.<GUID></span></span> | <span data-ttu-id="c6546-151">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="c6546-151">AppDataFolder</span></span>      |
| <span data-ttu-id="c6546-152">Component4.<GUID></span><span class="sxs-lookup"><span data-stu-id="c6546-152">Component4.<GUID></span></span> | <span data-ttu-id="c6546-153">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="c6546-153">MyPicturesFolder</span></span>   |



 

[<span data-ttu-id="c6546-154">CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="c6546-154">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="c6546-155">CustomAction</span><span class="sxs-lookup"><span data-stu-id="c6546-155">CustomAction</span></span>                 | <span data-ttu-id="c6546-156">類型</span><span class="sxs-lookup"><span data-stu-id="c6546-156">Type</span></span> | <span data-ttu-id="c6546-157">來源</span><span class="sxs-lookup"><span data-stu-id="c6546-157">Source</span></span>                       | <span data-ttu-id="c6546-158">目標</span><span class="sxs-lookup"><span data-stu-id="c6546-158">Target</span></span>              |
|------------------------------|------|------------------------------|---------------------|
| <span data-ttu-id="c6546-159">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="c6546-159">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="c6546-160">51</span><span class="sxs-lookup"><span data-stu-id="c6546-160">51</span></span>   | <span data-ttu-id="c6546-161">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="c6546-161">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="c6546-162">\[StartMenuFolder\]</span><span class="sxs-lookup"><span data-stu-id="c6546-162">\[StartMenuFolder\]</span></span> |
| <span data-ttu-id="c6546-163">MyAppDataFolderAction</span><span class="sxs-lookup"><span data-stu-id="c6546-163">MyAppDataFolderAction</span></span>        | <span data-ttu-id="c6546-164">51</span><span class="sxs-lookup"><span data-stu-id="c6546-164">51</span></span>   | <span data-ttu-id="c6546-165">AppDataFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="c6546-165">AppDataFolder.<GUID></span></span>   | <span data-ttu-id="c6546-166">\[AppDataFolder\]</span><span class="sxs-lookup"><span data-stu-id="c6546-166">\[AppDataFolder\]</span></span>   |



 

[<span data-ttu-id="c6546-167">ModuleInstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="c6546-167">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="c6546-168">動作</span><span class="sxs-lookup"><span data-stu-id="c6546-168">Action</span></span>                       | <span data-ttu-id="c6546-169">順序</span><span class="sxs-lookup"><span data-stu-id="c6546-169">Sequence</span></span> | <span data-ttu-id="c6546-170">BaseAction</span><span class="sxs-lookup"><span data-stu-id="c6546-170">BaseAction</span></span> | <span data-ttu-id="c6546-171">After</span><span class="sxs-lookup"><span data-stu-id="c6546-171">After</span></span> | <span data-ttu-id="c6546-172">條件</span><span class="sxs-lookup"><span data-stu-id="c6546-172">Condition</span></span> |
|------------------------------|----------|------------|-------|-----------|
| <span data-ttu-id="c6546-173">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="c6546-173">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="c6546-174">100</span><span class="sxs-lookup"><span data-stu-id="c6546-174">100</span></span>      |            |       |           |



 

## <a name="related-topics"></a><span data-ttu-id="c6546-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6546-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6546-176">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="c6546-176">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



