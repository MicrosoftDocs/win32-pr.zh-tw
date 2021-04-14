---
description: ModuleExclusion 資料表會保留相同安裝程式資料庫中不相容的其他合併模組清單。
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: ModuleExclusion 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386265"
---
# <a name="moduleexclusion-table"></a><span data-ttu-id="6d127-103">ModuleExclusion 資料表</span><span class="sxs-lookup"><span data-stu-id="6d127-103">ModuleExclusion Table</span></span>

<span data-ttu-id="6d127-104">ModuleExclusion 資料表會保留相同安裝程式資料庫中不相容的其他合併模組清單。</span><span class="sxs-lookup"><span data-stu-id="6d127-104">The ModuleExclusion table keeps a list of other merge modules that are incompatible in the same installer database.</span></span> <span data-ttu-id="6d127-105">此資料表會啟用合併或驗證工具，以檢查衝突的合併模組是否未在使用者的安裝程式資料庫中合併。</span><span class="sxs-lookup"><span data-stu-id="6d127-105">This table enables a merge or verification tool to check that conflicting merge modules are not merged in the user's installer database.</span></span> <span data-ttu-id="6d127-106">此工具會在安裝程式資料庫中使用 ModuleSignature 資料表來交叉參考此資料表，以進行檢查。</span><span class="sxs-lookup"><span data-stu-id="6d127-106">The tool checks by cross-referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="6d127-107">ModuleExclusion 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="6d127-107">The ModuleExclusion table has the following columns.</span></span>



| <span data-ttu-id="6d127-108">Column</span><span class="sxs-lookup"><span data-stu-id="6d127-108">Column</span></span>             | <span data-ttu-id="6d127-109">類型</span><span class="sxs-lookup"><span data-stu-id="6d127-109">Type</span></span>                         | <span data-ttu-id="6d127-110">答案</span><span class="sxs-lookup"><span data-stu-id="6d127-110">Key</span></span> | <span data-ttu-id="6d127-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="6d127-111">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="6d127-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="6d127-112">ModuleID</span></span>           | [<span data-ttu-id="6d127-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="6d127-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="6d127-114">Y</span><span class="sxs-lookup"><span data-stu-id="6d127-114">Y</span></span>   | <span data-ttu-id="6d127-115">N</span><span class="sxs-lookup"><span data-stu-id="6d127-115">N</span></span>        |
| <span data-ttu-id="6d127-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="6d127-116">ModuleLanguage</span></span>     | [<span data-ttu-id="6d127-117">整數</span><span class="sxs-lookup"><span data-stu-id="6d127-117">Integer</span></span>](integer.md)       | <span data-ttu-id="6d127-118">Y</span><span class="sxs-lookup"><span data-stu-id="6d127-118">Y</span></span>   | <span data-ttu-id="6d127-119">N</span><span class="sxs-lookup"><span data-stu-id="6d127-119">N</span></span>        |
| <span data-ttu-id="6d127-120">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="6d127-120">ExcludedID</span></span>         | [<span data-ttu-id="6d127-121">識別碼</span><span class="sxs-lookup"><span data-stu-id="6d127-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="6d127-122">Y</span><span class="sxs-lookup"><span data-stu-id="6d127-122">Y</span></span>   | <span data-ttu-id="6d127-123">N</span><span class="sxs-lookup"><span data-stu-id="6d127-123">N</span></span>        |
| <span data-ttu-id="6d127-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="6d127-124">ExcludedLanguage</span></span>   | [<span data-ttu-id="6d127-125">整數</span><span class="sxs-lookup"><span data-stu-id="6d127-125">Integer</span></span>](integer.md)       | <span data-ttu-id="6d127-126">Y</span><span class="sxs-lookup"><span data-stu-id="6d127-126">Y</span></span>   | <span data-ttu-id="6d127-127">N</span><span class="sxs-lookup"><span data-stu-id="6d127-127">N</span></span>        |
| <span data-ttu-id="6d127-128">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="6d127-128">ExcludedMinVersion</span></span> | [<span data-ttu-id="6d127-129">版本</span><span class="sxs-lookup"><span data-stu-id="6d127-129">Version</span></span>](version.md)       |     | <span data-ttu-id="6d127-130">Y</span><span class="sxs-lookup"><span data-stu-id="6d127-130">Y</span></span>        |
| <span data-ttu-id="6d127-131">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="6d127-131">ExcludedMaxVersion</span></span> | [<span data-ttu-id="6d127-132">版本</span><span class="sxs-lookup"><span data-stu-id="6d127-132">Version</span></span>](version.md)       |     | <span data-ttu-id="6d127-133">Y</span><span class="sxs-lookup"><span data-stu-id="6d127-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6d127-134">資料行</span><span class="sxs-lookup"><span data-stu-id="6d127-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6d127-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="6d127-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="6d127-136">合併模組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d127-136">Identifier of the merge module.</span></span> <span data-ttu-id="6d127-137">這是 [ModuleSignature 資料表](modulesignature-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="6d127-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d127-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="6d127-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="6d127-139">ModuleID 中合併模組的十進位語言識別項。</span><span class="sxs-lookup"><span data-stu-id="6d127-139">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="6d127-140">這是 [ModuleSignature 資料表](modulesignature-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="6d127-140">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d127-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span><span class="sxs-lookup"><span data-stu-id="6d127-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span></span>
</dt> <dd>

<span data-ttu-id="6d127-142">已排除合併模組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d127-142">Identifier of an excluded merge module.</span></span>

</dd> <dt>

<span data-ttu-id="6d127-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="6d127-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span></span>
</dt> <dd>

<span data-ttu-id="6d127-144">ExcludedID 中合併模組的數位語言識別項。</span><span class="sxs-lookup"><span data-stu-id="6d127-144">Numeric language ID of the merge module in ExcludedID.</span></span> <span data-ttu-id="6d127-145">ExcludedLanguage 資料行可以指定單一語言的語言識別項，例如美國英文的1033，或指定語言群組的語言識別項，例如任何英文的9。</span><span class="sxs-lookup"><span data-stu-id="6d127-145">The ExcludedLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="6d127-146">ExcludedLanguage 資料行可接受負的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="6d127-146">The ExcludedLanguage column can accept negative language IDs.</span></span> <span data-ttu-id="6d127-147">ExcludedLanguage 資料行中值的意義如下所示。</span><span class="sxs-lookup"><span data-stu-id="6d127-147">The meaning of the value in the ExcludedLanguage column is as follows.</span></span>



| <span data-ttu-id="6d127-148">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="6d127-148">ExcludedLanguage</span></span> | <span data-ttu-id="6d127-149">意義</span><span class="sxs-lookup"><span data-stu-id="6d127-149">Meaning</span></span>                                                              |
|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="6d127-150">> 0</span><span class="sxs-lookup"><span data-stu-id="6d127-150">> 0</span></span>           | <span data-ttu-id="6d127-151">排除 ExcludedLanguage 所指定的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="6d127-151">Exclude the language IDs specified by ExcludedLanguage.</span></span>              |
| <span data-ttu-id="6d127-152">= 0</span><span class="sxs-lookup"><span data-stu-id="6d127-152">= 0</span></span>              | <span data-ttu-id="6d127-153">排除無語言識別項。</span><span class="sxs-lookup"><span data-stu-id="6d127-153">Exclude no language IDs.</span></span>                                             |
| <span data-ttu-id="6d127-154">< 0</span><span class="sxs-lookup"><span data-stu-id="6d127-154">< 0</span></span>           | <span data-ttu-id="6d127-155">除了 ExcludedLanguage 指定的語言識別項之外，請排除所有語言識別項。</span><span class="sxs-lookup"><span data-stu-id="6d127-155">Exclude all language IDs except those specified by ExcludedLanguage.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6d127-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="6d127-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span></span>
</dt> <dd>

<span data-ttu-id="6d127-157">從範圍中排除的最小版本。</span><span class="sxs-lookup"><span data-stu-id="6d127-157">Minimum version excluded from a range.</span></span> <span data-ttu-id="6d127-158">如果 ExcludedMinVersion 欄位為 Null，則會排除 ExcludedMaxVersion 之前的所有版本。</span><span class="sxs-lookup"><span data-stu-id="6d127-158">If the ExcludedMinVersion field is Null, all versions before ExcludedMaxVersion are excluded.</span></span> <span data-ttu-id="6d127-159">如果 ExcludedMinVersion 和 ExcludedMaxVersion 都是 Null，則不會根據版本進行排除。</span><span class="sxs-lookup"><span data-stu-id="6d127-159">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> <dt>

<span data-ttu-id="6d127-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="6d127-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="6d127-161">從範圍中排除的最大版本。</span><span class="sxs-lookup"><span data-stu-id="6d127-161">Maximum version excluded from a range.</span></span> <span data-ttu-id="6d127-162">如果 ExcludedMaxVersion 欄位為 Null，則會排除 ExcludedMinVersion 之後的所有版本。</span><span class="sxs-lookup"><span data-stu-id="6d127-162">If the ExcludedMaxVersion field is Null, all versions after ExcludedMinVersion are excluded.</span></span> <span data-ttu-id="6d127-163">如果 ExcludedMinVersion 和 ExcludedMaxVersion 都是 Null，則不會根據版本進行排除。</span><span class="sxs-lookup"><span data-stu-id="6d127-163">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="6d127-164">驗證</span><span class="sxs-lookup"><span data-stu-id="6d127-164">Validation</span></span>

<dl>

[<span data-ttu-id="6d127-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="6d127-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6d127-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="6d127-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6d127-167">ICE25</span><span class="sxs-lookup"><span data-stu-id="6d127-167">ICE25</span></span>](ice25.md)  
</dl>

 

 



