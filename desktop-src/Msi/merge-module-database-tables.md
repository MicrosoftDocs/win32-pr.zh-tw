---
description: 標準合併模組中需要有下列資料表。
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: 合併模組資料庫資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977086"
---
# <a name="merge-module-database-tables"></a><span data-ttu-id="8ec5b-103">合併模組資料庫資料表</span><span class="sxs-lookup"><span data-stu-id="8ec5b-103">Merge Module Database Tables</span></span>

<span data-ttu-id="8ec5b-104">標準合併模組中需要有下列資料表。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-104">The following tables are required in a standard merge module.</span></span>



| <span data-ttu-id="8ec5b-105">資料表名稱</span><span class="sxs-lookup"><span data-stu-id="8ec5b-105">Table name</span></span>                                       | <span data-ttu-id="8ec5b-106">註解</span><span class="sxs-lookup"><span data-stu-id="8ec5b-106">Comment</span></span>                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ec5b-107">元件</span><span class="sxs-lookup"><span data-stu-id="8ec5b-107">Component</span></span>](component-table.md)                 | <span data-ttu-id="8ec5b-108">需要 () </span><span class="sxs-lookup"><span data-stu-id="8ec5b-108">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="8ec5b-109">目錄</span><span class="sxs-lookup"><span data-stu-id="8ec5b-109">Directory</span></span>](directory-table.md)                 | <span data-ttu-id="8ec5b-110">需要 () </span><span class="sxs-lookup"><span data-stu-id="8ec5b-110">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="8ec5b-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="8ec5b-111">FeatureComponents</span></span>](featurecomponents-table.md) | <span data-ttu-id="8ec5b-112">需要 () </span><span class="sxs-lookup"><span data-stu-id="8ec5b-112">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="8ec5b-113">檔案</span><span class="sxs-lookup"><span data-stu-id="8ec5b-113">File</span></span>](file-table.md)                           | <span data-ttu-id="8ec5b-114">需要 () </span><span class="sxs-lookup"><span data-stu-id="8ec5b-114">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="8ec5b-115">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="8ec5b-115">ModuleSignature</span></span>](modulesignature-table.md)     | <span data-ttu-id="8ec5b-116"> (需要合併到安裝程式資料庫) 。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-116">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="8ec5b-117">列出識別合併模組的資訊。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-117">Lists the information identifying a merge module.</span></span> |
| [<span data-ttu-id="8ec5b-118">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="8ec5b-118">ModuleComponents</span></span>](modulecomponents-table.md)   | <span data-ttu-id="8ec5b-119"> (需要合併到安裝程式資料庫) 。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-119">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="8ec5b-120">列出合併模組中的所有元件。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-120">Lists all the components in the merge module.</span></span>     |



 

<span data-ttu-id="8ec5b-121">下列資料表只會出現在合併模組或其他安裝程式資料庫（已與合併模組合併）中。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-121">The following tables only occur in merge modules or other installer databases that have already been combined with a merge module.</span></span>



| <span data-ttu-id="8ec5b-122">資料表名稱</span><span class="sxs-lookup"><span data-stu-id="8ec5b-122">Table name</span></span>                                     | <span data-ttu-id="8ec5b-123">註解</span><span class="sxs-lookup"><span data-stu-id="8ec5b-123">Comment</span></span>                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ec5b-124">ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="8ec5b-124">ModuleDependency</span></span>](moduledependency-table.md) | <span data-ttu-id="8ec5b-125">合併到安裝程式資料庫。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-125">Merged into the installer database.</span></span> <span data-ttu-id="8ec5b-126">列出此合併模組所需的其他合併模組。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-126">Lists other merge modules required by this merge module.</span></span>                |
| [<span data-ttu-id="8ec5b-127">ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="8ec5b-127">ModuleExclusion</span></span>](moduleexclusion-table.md)   | <span data-ttu-id="8ec5b-128">合併到安裝程式資料庫。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-128">Merged into the installer database.</span></span> <span data-ttu-id="8ec5b-129">列出與此合併模組不相容的其他合併模組。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-129">Lists other merge modules that are incompatible with this merge module.</span></span> |



 

<span data-ttu-id="8ec5b-130">下列 ModuleSequence 資料表只會出現在合併模組中。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-130">The following ModuleSequence tables only occur in merge modules.</span></span>



| <span data-ttu-id="8ec5b-131">資料表名稱</span><span class="sxs-lookup"><span data-stu-id="8ec5b-131">Table name</span></span>                                                             | <span data-ttu-id="8ec5b-132">註解</span><span class="sxs-lookup"><span data-stu-id="8ec5b-132">Comment</span></span>                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ec5b-133">ModuleAdminUISequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-133">ModuleAdminUISequence</span></span>](moduleadminuisequence-table.md)               | <span data-ttu-id="8ec5b-134">將動作合併至 [AdminUISequence 資料表](adminuisequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-134">Merges actions into the [AdminUISequence table](adminuisequence-table.md).</span></span>               |
| [<span data-ttu-id="8ec5b-135">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-135">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)     | <span data-ttu-id="8ec5b-136">將動作合併至 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-136">Merges actions into the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>     |
| [<span data-ttu-id="8ec5b-137">ModuleAdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-137">ModuleAdvtUISequence</span></span>](moduleadvtuisequence-table.md)                 | <span data-ttu-id="8ec5b-138">請勿使用此資料表。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-138">Do not use this table.</span></span> <span data-ttu-id="8ec5b-139">如需詳細資訊，請參閱 [AdvtUISequence 資料表](advtuisequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-139">For details, see [AdvtUISequence table](advtuisequence-table.md).</span></span> |
| [<span data-ttu-id="8ec5b-140">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-140">ModuleAdvtExecuteSequence</span></span>](moduleadvtexecutesequence-table.md)       | <span data-ttu-id="8ec5b-141">將動作合併至 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-141">Merges actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>       |
| [<span data-ttu-id="8ec5b-142">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="8ec5b-142">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)                       | <span data-ttu-id="8ec5b-143">列出模組中未合併至 .msi 檔案的資料表。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-143">Lists tables in the module that are not merged into the .msi file.</span></span>                        |
| [<span data-ttu-id="8ec5b-144">ModuleInstallUISequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-144">ModuleInstallUISequence</span></span>](moduleinstalluisequence-table.md)           | <span data-ttu-id="8ec5b-145">將動作合併至 [InstallUISequence 資料表](installuisequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-145">Merges actions into the [InstallUISequence table](installuisequence-table.md).</span></span>           |
| [<span data-ttu-id="8ec5b-146">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-146">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md) | <span data-ttu-id="8ec5b-147">將動作合併至 [InstallExecuteSequence 資料表](installexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-147">Merges actions into the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> |



 

<span data-ttu-id="8ec5b-148">每個可設定的合併模組都需要下列資料表。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-148">The following tables are required in every configurable merge module.</span></span> <span data-ttu-id="8ec5b-149">需要 Mergemod.dll 2.0 或更新版本，才能建立可設定的合併模組。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-149">Mergemod.dll 2.0 or later is required to create configurable merge module.</span></span> <span data-ttu-id="8ec5b-150">如需詳細資訊，請參閱可設定的 [合併模組](configurable-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-150">For details, see [Configurable Merge Modules](configurable-merge-modules.md).</span></span>



| <span data-ttu-id="8ec5b-151">資料表名稱</span><span class="sxs-lookup"><span data-stu-id="8ec5b-151">Table name</span></span>                                                 | <span data-ttu-id="8ec5b-152">註解</span><span class="sxs-lookup"><span data-stu-id="8ec5b-152">Comment</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ec5b-153">ModuleSubstitution 資料表</span><span class="sxs-lookup"><span data-stu-id="8ec5b-153">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)   | <span data-ttu-id="8ec5b-154"> (需要) 此資料表不會合並到目標安裝資料庫中。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-154">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="8ec5b-155">指定目標資料庫中可設定的欄位，並為每個欄位的設定提供範本。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-155">Specifies the configurable fields in the target database and provides a template for the configuration of each field.</span></span> |
| [<span data-ttu-id="8ec5b-156">ModuleConfiguration 資料表</span><span class="sxs-lookup"><span data-stu-id="8ec5b-156">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md) | <span data-ttu-id="8ec5b-157"> (需要) 此資料表不會合並到目標安裝資料庫中。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-157">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="8ec5b-158">識別模組的可設定屬性。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-158">Identifies the configurable attributes of the module.</span></span>                                                                 |



 

<span data-ttu-id="8ec5b-159">下列安裝程式資料表不能出現在標準合併模組中。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-159">The following installer tables cannot occur in a standard merge module.</span></span>

-   [<span data-ttu-id="8ec5b-160">BBControl</span><span class="sxs-lookup"><span data-stu-id="8ec5b-160">BBControl</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="8ec5b-161">廣告 牌</span><span class="sxs-lookup"><span data-stu-id="8ec5b-161">Billboard</span></span>](billboard-table.md)
-   [<span data-ttu-id="8ec5b-162">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="8ec5b-162">CCPSearch</span></span>](ccpsearch-table.md)
-   [<span data-ttu-id="8ec5b-163">錯誤</span><span class="sxs-lookup"><span data-stu-id="8ec5b-163">Error</span></span>](error-table.md)
-   [<span data-ttu-id="8ec5b-164">功能</span><span class="sxs-lookup"><span data-stu-id="8ec5b-164">Feature</span></span>](feature-table.md)
-   [<span data-ttu-id="8ec5b-165">LaunchCondition 資料表</span><span class="sxs-lookup"><span data-stu-id="8ec5b-165">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="8ec5b-166">媒體</span><span class="sxs-lookup"><span data-stu-id="8ec5b-166">Media</span></span>](media-table.md)
-   [<span data-ttu-id="8ec5b-167">修補</span><span class="sxs-lookup"><span data-stu-id="8ec5b-167">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="8ec5b-168">升級</span><span class="sxs-lookup"><span data-stu-id="8ec5b-168">Upgrade</span></span>](upgrade-table.md)

<span data-ttu-id="8ec5b-169">下列安裝程式資料表在合併模組中是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8ec5b-169">The following installer tables are optional in merge modules.</span></span>

-   [<span data-ttu-id="8ec5b-170">ActionText</span><span class="sxs-lookup"><span data-stu-id="8ec5b-170">ActionText</span></span>](actiontext-table.md)
-   [<span data-ttu-id="8ec5b-171">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-171">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="8ec5b-172">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-172">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="8ec5b-173">AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-173">AdvtExecuteSequence</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="8ec5b-174">AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-174">AdvtUISequence</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="8ec5b-175">AppId</span><span class="sxs-lookup"><span data-stu-id="8ec5b-175">AppId</span></span>](appid-table.md)
-   [<span data-ttu-id="8ec5b-176">AppSearch</span><span class="sxs-lookup"><span data-stu-id="8ec5b-176">AppSearch</span></span>](appsearch-table.md)
-   [<span data-ttu-id="8ec5b-177">BindImage</span><span class="sxs-lookup"><span data-stu-id="8ec5b-177">BindImage</span></span>](bindimage-table.md)
-   [<span data-ttu-id="8ec5b-178">CheckBox</span><span class="sxs-lookup"><span data-stu-id="8ec5b-178">CheckBox</span></span>](checkbox-table.md)
-   [<span data-ttu-id="8ec5b-179">類別</span><span class="sxs-lookup"><span data-stu-id="8ec5b-179">Class</span></span>](class-table.md)
-   [<span data-ttu-id="8ec5b-180">ComboBox</span><span class="sxs-lookup"><span data-stu-id="8ec5b-180">ComboBox</span></span>](combobox-table.md)
-   [<span data-ttu-id="8ec5b-181">CompLocator</span><span class="sxs-lookup"><span data-stu-id="8ec5b-181">CompLocator</span></span>](complocator-table.md)
-   [<span data-ttu-id="8ec5b-182">控制</span><span class="sxs-lookup"><span data-stu-id="8ec5b-182">Control</span></span>](control-table.md)
-   [<span data-ttu-id="8ec5b-183">ControlCondition</span><span class="sxs-lookup"><span data-stu-id="8ec5b-183">ControlCondition</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="8ec5b-184">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="8ec5b-184">CreateFolder</span></span>](createfolder-table.md)
-   [<span data-ttu-id="8ec5b-185">CustomAction</span><span class="sxs-lookup"><span data-stu-id="8ec5b-185">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="8ec5b-186">對話方塊</span><span class="sxs-lookup"><span data-stu-id="8ec5b-186">Dialog</span></span>](dialog-table.md)
-   [<span data-ttu-id="8ec5b-187">DrLocator</span><span class="sxs-lookup"><span data-stu-id="8ec5b-187">DrLocator</span></span>](drlocator-table.md)
-   [<span data-ttu-id="8ec5b-188">DuplicateFile</span><span class="sxs-lookup"><span data-stu-id="8ec5b-188">DuplicateFile</span></span>](duplicatefile-table.md)
-   [<span data-ttu-id="8ec5b-189">環境</span><span class="sxs-lookup"><span data-stu-id="8ec5b-189">Environment</span></span>](environment-table.md)
-   [<span data-ttu-id="8ec5b-190">EventMapping</span><span class="sxs-lookup"><span data-stu-id="8ec5b-190">EventMapping</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="8ec5b-191">分機</span><span class="sxs-lookup"><span data-stu-id="8ec5b-191">Extension</span></span>](extension-table.md)
-   [<span data-ttu-id="8ec5b-192">字型</span><span class="sxs-lookup"><span data-stu-id="8ec5b-192">Font</span></span>](font-table.md)
-   [<span data-ttu-id="8ec5b-193">圖示</span><span class="sxs-lookup"><span data-stu-id="8ec5b-193">Icon</span></span>](icon-table.md)
-   [<span data-ttu-id="8ec5b-194">IniFile</span><span class="sxs-lookup"><span data-stu-id="8ec5b-194">IniFile</span></span>](inifile-table.md)
-   [<span data-ttu-id="8ec5b-195">IniLocator</span><span class="sxs-lookup"><span data-stu-id="8ec5b-195">IniLocator</span></span>](inilocator-table.md)
-   [<span data-ttu-id="8ec5b-196">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-196">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="8ec5b-197">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="8ec5b-197">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="8ec5b-198">ListBox</span><span class="sxs-lookup"><span data-stu-id="8ec5b-198">ListBox</span></span>](listbox-table.md)
-   [<span data-ttu-id="8ec5b-199">ListView</span><span class="sxs-lookup"><span data-stu-id="8ec5b-199">ListView</span></span>](listview-table.md)
-   [<span data-ttu-id="8ec5b-200">MIME</span><span class="sxs-lookup"><span data-stu-id="8ec5b-200">MIME</span></span>](mime-table.md)
-   [<span data-ttu-id="8ec5b-201">MoveFile</span><span class="sxs-lookup"><span data-stu-id="8ec5b-201">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="8ec5b-202">ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="8ec5b-202">ODBCAttribute</span></span>](odbcattribute-table.md)
-   [<span data-ttu-id="8ec5b-203">ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="8ec5b-203">ODBCDataSource</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="8ec5b-204">ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="8ec5b-204">ODBCDriver</span></span>](odbcdriver-table.md)
-   [<span data-ttu-id="8ec5b-205">ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="8ec5b-205">ODBCSourceAttribute</span></span>](odbcsourceattribute-table.md)
-   [<span data-ttu-id="8ec5b-206">ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="8ec5b-206">ODBCTranslator</span></span>](odbctranslator-table.md)
-   [<span data-ttu-id="8ec5b-207">ProgID 資料表</span><span class="sxs-lookup"><span data-stu-id="8ec5b-207">ProgID Table</span></span>](progid-table.md)
-   [<span data-ttu-id="8ec5b-208">屬性</span><span class="sxs-lookup"><span data-stu-id="8ec5b-208">Property</span></span>](property-table.md)
-   [<span data-ttu-id="8ec5b-209">PublishComponent</span><span class="sxs-lookup"><span data-stu-id="8ec5b-209">PublishComponent</span></span>](publishcomponent-table.md)
-   [<span data-ttu-id="8ec5b-210">RadioButton</span><span class="sxs-lookup"><span data-stu-id="8ec5b-210">RadioButton</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="8ec5b-211">登錄資料表</span><span class="sxs-lookup"><span data-stu-id="8ec5b-211">Registry Table</span></span>](registry-table.md)
-   [<span data-ttu-id="8ec5b-212">RegLocator</span><span class="sxs-lookup"><span data-stu-id="8ec5b-212">RegLocator</span></span>](reglocator-table.md)
-   [<span data-ttu-id="8ec5b-213">RemoveFile</span><span class="sxs-lookup"><span data-stu-id="8ec5b-213">RemoveFile</span></span>](removefile-table.md)
-   [<span data-ttu-id="8ec5b-214">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="8ec5b-214">RemoveIniFile</span></span>](removeinifile-table.md)
-   [<span data-ttu-id="8ec5b-215">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="8ec5b-215">RemoveRegistry</span></span>](removeregistry-table.md)
-   [<span data-ttu-id="8ec5b-216">ReserveCost</span><span class="sxs-lookup"><span data-stu-id="8ec5b-216">ReserveCost</span></span>](reservecost-table.md)
-   [<span data-ttu-id="8ec5b-217">SelfReg</span><span class="sxs-lookup"><span data-stu-id="8ec5b-217">SelfReg</span></span>](selfreg-table.md)
-   [<span data-ttu-id="8ec5b-218">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="8ec5b-218">ServiceControl</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="8ec5b-219">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="8ec5b-219">ServiceInstall</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="8ec5b-220">快速鍵</span><span class="sxs-lookup"><span data-stu-id="8ec5b-220">Shortcut</span></span>](shortcut-table.md)
-   [<span data-ttu-id="8ec5b-221">簽名</span><span class="sxs-lookup"><span data-stu-id="8ec5b-221">Signature</span></span>](signature-table.md)
-   [<span data-ttu-id="8ec5b-222">文本</span><span class="sxs-lookup"><span data-stu-id="8ec5b-222">TextStyle</span></span>](textstyle-table.md)
-   [<span data-ttu-id="8ec5b-223">類型</span><span class="sxs-lookup"><span data-stu-id="8ec5b-223">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="8ec5b-224">UIText</span><span class="sxs-lookup"><span data-stu-id="8ec5b-224">UIText</span></span>](uitext-table.md)
-   [<span data-ttu-id="8ec5b-225">動詞</span><span class="sxs-lookup"><span data-stu-id="8ec5b-225">Verb</span></span>](verb-table.md)

 

 



