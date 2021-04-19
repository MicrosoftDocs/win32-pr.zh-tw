---
description: ModuleDependency 資料表會保留此合併模組正常運作所需的其他合併模組清單。
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: ModuleDependency 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971871"
---
# <a name="moduledependency-table"></a><span data-ttu-id="54d5c-103">ModuleDependency 資料表</span><span class="sxs-lookup"><span data-stu-id="54d5c-103">ModuleDependency Table</span></span>

<span data-ttu-id="54d5c-104">ModuleDependency 資料表會保留此合併模組正常運作所需的其他合併模組清單。</span><span class="sxs-lookup"><span data-stu-id="54d5c-104">The ModuleDependency table keeps a list of other merge modules that are required for this merge module to operate properly.</span></span> <span data-ttu-id="54d5c-105">下表啟用合併或驗證工具，以確保所需的合併模組實際上包含在使用者的安裝程式資料庫中。</span><span class="sxs-lookup"><span data-stu-id="54d5c-105">This table enables a merge or verification tool to ensure that the necessary merge modules are in fact included in the user's installer database.</span></span> <span data-ttu-id="54d5c-106">此工具會在安裝程式資料庫中，透過參考此資料表與 ModuleSignature 資料表的方式進行檢查。</span><span class="sxs-lookup"><span data-stu-id="54d5c-106">The tool checks by cross referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="54d5c-107">ModuleDependency 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="54d5c-107">The ModuleDependency table has the following columns.</span></span>



| <span data-ttu-id="54d5c-108">Column</span><span class="sxs-lookup"><span data-stu-id="54d5c-108">Column</span></span>           | <span data-ttu-id="54d5c-109">類型</span><span class="sxs-lookup"><span data-stu-id="54d5c-109">Type</span></span>                         | <span data-ttu-id="54d5c-110">答案</span><span class="sxs-lookup"><span data-stu-id="54d5c-110">Key</span></span> | <span data-ttu-id="54d5c-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="54d5c-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="54d5c-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="54d5c-112">ModuleID</span></span>         | [<span data-ttu-id="54d5c-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="54d5c-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="54d5c-114">Y</span><span class="sxs-lookup"><span data-stu-id="54d5c-114">Y</span></span>   | <span data-ttu-id="54d5c-115">N</span><span class="sxs-lookup"><span data-stu-id="54d5c-115">N</span></span>        |
| <span data-ttu-id="54d5c-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="54d5c-116">ModuleLanguage</span></span>   | [<span data-ttu-id="54d5c-117">整數</span><span class="sxs-lookup"><span data-stu-id="54d5c-117">Integer</span></span>](integer.md)       | <span data-ttu-id="54d5c-118">Y</span><span class="sxs-lookup"><span data-stu-id="54d5c-118">Y</span></span>   | <span data-ttu-id="54d5c-119">N</span><span class="sxs-lookup"><span data-stu-id="54d5c-119">N</span></span>        |
| <span data-ttu-id="54d5c-120">RequiredID</span><span class="sxs-lookup"><span data-stu-id="54d5c-120">RequiredID</span></span>       | [<span data-ttu-id="54d5c-121">識別碼</span><span class="sxs-lookup"><span data-stu-id="54d5c-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="54d5c-122">Y</span><span class="sxs-lookup"><span data-stu-id="54d5c-122">Y</span></span>   | <span data-ttu-id="54d5c-123">N</span><span class="sxs-lookup"><span data-stu-id="54d5c-123">N</span></span>        |
| <span data-ttu-id="54d5c-124">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="54d5c-124">RequiredLanguage</span></span> | [<span data-ttu-id="54d5c-125">整數</span><span class="sxs-lookup"><span data-stu-id="54d5c-125">Integer</span></span>](integer.md)       | <span data-ttu-id="54d5c-126">Y</span><span class="sxs-lookup"><span data-stu-id="54d5c-126">Y</span></span>   | <span data-ttu-id="54d5c-127">N</span><span class="sxs-lookup"><span data-stu-id="54d5c-127">N</span></span>        |
| <span data-ttu-id="54d5c-128">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="54d5c-128">RequiredVersion</span></span>  | [<span data-ttu-id="54d5c-129">版本</span><span class="sxs-lookup"><span data-stu-id="54d5c-129">Version</span></span>](version.md)       |     | <span data-ttu-id="54d5c-130">Y</span><span class="sxs-lookup"><span data-stu-id="54d5c-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="54d5c-131">資料行</span><span class="sxs-lookup"><span data-stu-id="54d5c-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="54d5c-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="54d5c-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="54d5c-133">合併模組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="54d5c-133">Identifier of the merge module.</span></span> <span data-ttu-id="54d5c-134">這是 [ModuleSignature 資料表](modulesignature-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="54d5c-134">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="54d5c-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="54d5c-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="54d5c-136">ModuleID 中合併模組的十進位語言識別項。</span><span class="sxs-lookup"><span data-stu-id="54d5c-136">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="54d5c-137">這是 [ModuleSignature 資料表](modulesignature-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="54d5c-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="54d5c-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span><span class="sxs-lookup"><span data-stu-id="54d5c-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span></span>
</dt> <dd>

<span data-ttu-id="54d5c-139">ModuleID 中 merge 模組所需之合併模組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="54d5c-139">Identifier of the merge module required by the merge module in ModuleID.</span></span>

</dd> <dt>

<span data-ttu-id="54d5c-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="54d5c-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span></span>
</dt> <dd>

<span data-ttu-id="54d5c-141">RequiredID 中合併模組的數位語言識別項。</span><span class="sxs-lookup"><span data-stu-id="54d5c-141">Numeric language ID of the merge module in RequiredID.</span></span> <span data-ttu-id="54d5c-142">RequiredLanguage 資料行可以指定單一語言的語言識別項，例如美國英文的1033，或指定語言群組的語言識別項，例如任何英文的9。</span><span class="sxs-lookup"><span data-stu-id="54d5c-142">The RequiredLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="54d5c-143">如果欄位包含群組語言識別項，則在該群組中具有語言代碼的任何合併模組都會滿足相依性。</span><span class="sxs-lookup"><span data-stu-id="54d5c-143">If the field contains a group language ID, any merge module with having a language code in that group satisfies the dependency.</span></span> <span data-ttu-id="54d5c-144">如果 RequiredLanguage 設定為0，則任何填入其他需求的合併模組都會滿足相依性。</span><span class="sxs-lookup"><span data-stu-id="54d5c-144">If the RequiredLanguage is set to 0, any merge module filling the other requirements satisfies the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="54d5c-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="54d5c-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span></span>
</dt> <dd>

<span data-ttu-id="54d5c-146">RequiredID 中的合併模組版本。</span><span class="sxs-lookup"><span data-stu-id="54d5c-146">Version of the merge module in RequiredID.</span></span> <span data-ttu-id="54d5c-147">如果此欄位為 Null，任何版本都會填滿相依性。</span><span class="sxs-lookup"><span data-stu-id="54d5c-147">If this field is Null, any version fills the dependency.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="54d5c-148">驗證</span><span class="sxs-lookup"><span data-stu-id="54d5c-148">Validation</span></span>

<dl>

[<span data-ttu-id="54d5c-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="54d5c-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="54d5c-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="54d5c-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="54d5c-151">ICE25</span><span class="sxs-lookup"><span data-stu-id="54d5c-151">ICE25</span></span>](ice25.md)  
</dl>

 

 



