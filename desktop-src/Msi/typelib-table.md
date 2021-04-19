---
description: TypeLib 資料表包含需要放在類型程式庫登錄註冊中的資訊。
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: TypeLib 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0aa8949df75162ffb7107b633ab766d276c4b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973801"
---
# <a name="typelib-table"></a><span data-ttu-id="9f925-103">TypeLib 資料表</span><span class="sxs-lookup"><span data-stu-id="9f925-103">TypeLib Table</span></span>

<span data-ttu-id="9f925-104">TypeLib 資料表包含需要放在類型程式庫登錄註冊中的資訊。</span><span class="sxs-lookup"><span data-stu-id="9f925-104">The TypeLib table contains the information that needs to be placed in the registry registration of type libraries.</span></span>

<span data-ttu-id="9f925-105">TypeLib 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="9f925-105">The TypeLib table has the following columns.</span></span>



| <span data-ttu-id="9f925-106">Column</span><span class="sxs-lookup"><span data-stu-id="9f925-106">Column</span></span>      | <span data-ttu-id="9f925-107">類型</span><span class="sxs-lookup"><span data-stu-id="9f925-107">Type</span></span>                               | <span data-ttu-id="9f925-108">答案</span><span class="sxs-lookup"><span data-stu-id="9f925-108">Key</span></span> | <span data-ttu-id="9f925-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="9f925-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="9f925-110">LibID</span><span class="sxs-lookup"><span data-stu-id="9f925-110">LibID</span></span>       | [<span data-ttu-id="9f925-111">GUID</span><span class="sxs-lookup"><span data-stu-id="9f925-111">GUID</span></span>](guid.md)                   | <span data-ttu-id="9f925-112">Y</span><span class="sxs-lookup"><span data-stu-id="9f925-112">Y</span></span>   | <span data-ttu-id="9f925-113">N</span><span class="sxs-lookup"><span data-stu-id="9f925-113">N</span></span>        |
| <span data-ttu-id="9f925-114">語言</span><span class="sxs-lookup"><span data-stu-id="9f925-114">Language</span></span>    | [<span data-ttu-id="9f925-115">整數</span><span class="sxs-lookup"><span data-stu-id="9f925-115">Integer</span></span>](integer.md)             | <span data-ttu-id="9f925-116">Y</span><span class="sxs-lookup"><span data-stu-id="9f925-116">Y</span></span>   | <span data-ttu-id="9f925-117">N</span><span class="sxs-lookup"><span data-stu-id="9f925-117">N</span></span>        |
| <span data-ttu-id="9f925-118">元件\_</span><span class="sxs-lookup"><span data-stu-id="9f925-118">Component\_</span></span> | [<span data-ttu-id="9f925-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="9f925-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9f925-120">Y</span><span class="sxs-lookup"><span data-stu-id="9f925-120">Y</span></span>   | <span data-ttu-id="9f925-121">N</span><span class="sxs-lookup"><span data-stu-id="9f925-121">N</span></span>        |
| <span data-ttu-id="9f925-122">版本</span><span class="sxs-lookup"><span data-stu-id="9f925-122">Version</span></span>     | [<span data-ttu-id="9f925-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="9f925-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9f925-124">N</span><span class="sxs-lookup"><span data-stu-id="9f925-124">N</span></span>   | <span data-ttu-id="9f925-125">Y</span><span class="sxs-lookup"><span data-stu-id="9f925-125">Y</span></span>        |
| <span data-ttu-id="9f925-126">Description</span><span class="sxs-lookup"><span data-stu-id="9f925-126">Description</span></span> | [<span data-ttu-id="9f925-127">Text</span><span class="sxs-lookup"><span data-stu-id="9f925-127">Text</span></span>](text.md)                   | <span data-ttu-id="9f925-128">N</span><span class="sxs-lookup"><span data-stu-id="9f925-128">N</span></span>   | <span data-ttu-id="9f925-129">Y</span><span class="sxs-lookup"><span data-stu-id="9f925-129">Y</span></span>        |
| <span data-ttu-id="9f925-130">目錄\_</span><span class="sxs-lookup"><span data-stu-id="9f925-130">Directory\_</span></span> | [<span data-ttu-id="9f925-131">識別碼</span><span class="sxs-lookup"><span data-stu-id="9f925-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9f925-132">N</span><span class="sxs-lookup"><span data-stu-id="9f925-132">N</span></span>   | <span data-ttu-id="9f925-133">Y</span><span class="sxs-lookup"><span data-stu-id="9f925-133">Y</span></span>        |
| <span data-ttu-id="9f925-134">功能\_</span><span class="sxs-lookup"><span data-stu-id="9f925-134">Feature\_</span></span>   | [<span data-ttu-id="9f925-135">識別碼</span><span class="sxs-lookup"><span data-stu-id="9f925-135">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9f925-136">N</span><span class="sxs-lookup"><span data-stu-id="9f925-136">N</span></span>   | <span data-ttu-id="9f925-137">N</span><span class="sxs-lookup"><span data-stu-id="9f925-137">N</span></span>        |
| <span data-ttu-id="9f925-138">成本</span><span class="sxs-lookup"><span data-stu-id="9f925-138">Cost</span></span>        | [<span data-ttu-id="9f925-139">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="9f925-139">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9f925-140">N</span><span class="sxs-lookup"><span data-stu-id="9f925-140">N</span></span>   | <span data-ttu-id="9f925-141">Y</span><span class="sxs-lookup"><span data-stu-id="9f925-141">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9f925-142">資料行</span><span class="sxs-lookup"><span data-stu-id="9f925-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9f925-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span><span class="sxs-lookup"><span data-stu-id="9f925-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span></span>
</dt> <dd>

<span data-ttu-id="9f925-144">識別程式庫的 GUID。</span><span class="sxs-lookup"><span data-stu-id="9f925-144">The GUID that identifies the library.</span></span>

</dd> <dt>

<span data-ttu-id="9f925-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言</span><span class="sxs-lookup"><span data-stu-id="9f925-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="9f925-146">類型程式庫的語言。</span><span class="sxs-lookup"><span data-stu-id="9f925-146">The language of the type library.</span></span> <span data-ttu-id="9f925-147">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="9f925-147">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="9f925-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="9f925-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="9f925-149">在 [元件資料表](component-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9f925-149">External key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="9f925-150">此資料行會識別屬於功能的元件， \_ 其金鑰檔是要註冊的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="9f925-150">This column identifies the component belonging to Feature\_ whose key file is the type library being registered.</span></span>

</dd> <dt>

<span data-ttu-id="9f925-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>版本</span><span class="sxs-lookup"><span data-stu-id="9f925-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="9f925-152">這是程式庫的版本。</span><span class="sxs-lookup"><span data-stu-id="9f925-152">This is the version of the library.</span></span> <span data-ttu-id="9f925-153">主要和次要版本會以四個位元組整數值進行編碼。</span><span class="sxs-lookup"><span data-stu-id="9f925-153">The major and minor versions are encoded in the four byte integer value.</span></span> <span data-ttu-id="9f925-154">次要版本是在較低的八位。</span><span class="sxs-lookup"><span data-stu-id="9f925-154">The minor version is in the lower eight bits.</span></span> <span data-ttu-id="9f925-155">主要版本是在中間的十六位。</span><span class="sxs-lookup"><span data-stu-id="9f925-155">The major version is in the middle sixteen bits.</span></span>

</dd> <dt>

<span data-ttu-id="9f925-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="9f925-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="9f925-157">程式庫的可當地語系化描述。</span><span class="sxs-lookup"><span data-stu-id="9f925-157">A localizable description of the library.</span></span>

</dd> <dt>

<span data-ttu-id="9f925-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>目錄\_</span><span class="sxs-lookup"><span data-stu-id="9f925-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="9f925-159">在 [目錄資料表](directory-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9f925-159">External key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="9f925-160">這個資料行會識別類型程式庫的說明路徑。</span><span class="sxs-lookup"><span data-stu-id="9f925-160">This column identifies the Help path for the type library.</span></span> <span data-ttu-id="9f925-161">在廣告期間會忽略此資料行。</span><span class="sxs-lookup"><span data-stu-id="9f925-161">This column is ignored during advertising.</span></span>

</dd> <dt>

<span data-ttu-id="9f925-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_</span><span class="sxs-lookup"><span data-stu-id="9f925-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="9f925-163">在 [功能資料表](feature-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9f925-163">External key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="9f925-164">這個資料行會指定必須安裝才能操作類型程式庫的功能。</span><span class="sxs-lookup"><span data-stu-id="9f925-164">This column specifies the feature that must be installed for the type library to be operational.</span></span>

</dd> <dt>

<span data-ttu-id="9f925-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>成本</span><span class="sxs-lookup"><span data-stu-id="9f925-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="9f925-166">與類型程式庫註冊相關聯的成本（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9f925-166">The cost associated with the registration of the type library in bytes.</span></span> <span data-ttu-id="9f925-167">這必須是非負數或 null。</span><span class="sxs-lookup"><span data-stu-id="9f925-167">This must be a non-negative number or null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f925-168">備註</span><span class="sxs-lookup"><span data-stu-id="9f925-168">Remarks</span></span>

<span data-ttu-id="9f925-169">當執行 [RegisterTypeLibraries 動作](registertypelibraries-action.md) 或 [UnregisterTypeLibraries 動作](unregistertypelibraries-action.md) 時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="9f925-169">This table is referred to when the [RegisterTypeLibraries action](registertypelibraries-action.md) or the [UnregisterTypeLibraries action](unregistertypelibraries-action.md) is executed.</span></span>

<span data-ttu-id="9f925-170">安裝程式會將所有類型程式庫註冊資訊寫入 HKEY \_ 本機 \_ 電腦 (HKLM) 登錄位置。</span><span class="sxs-lookup"><span data-stu-id="9f925-170">The installer writes all type library registration information into the HKEY\_LOCAL\_MACHINE (HKLM) registry location.</span></span> <span data-ttu-id="9f925-171">即使是針對個別使用者安裝也是如此。</span><span class="sxs-lookup"><span data-stu-id="9f925-171">This is the case even for per-user installations.</span></span> <span data-ttu-id="9f925-172">類型程式庫無法在 (HKCU) 的每個使用者位置註冊。</span><span class="sxs-lookup"><span data-stu-id="9f925-172">Type libraries cannot be registered in per-user locations (HKCU).</span></span>

<span data-ttu-id="9f925-173">使用 TypeLib 資料表時，強烈建議使用安裝套件作者。</span><span class="sxs-lookup"><span data-stu-id="9f925-173">Installation package authors are strongly advised against using the TypeLib table.</span></span> <span data-ttu-id="9f925-174">相反地，他們應該使用 [登錄表來](registry-table.md) 註冊類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="9f925-174">Instead, they should register type libraries by using the [Registry](registry-table.md) table.</span></span> <span data-ttu-id="9f925-175">避免自行註冊的原因包括：</span><span class="sxs-lookup"><span data-stu-id="9f925-175">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="9f925-176">如果使用 TypeLib 資料表的安裝失敗，而且必須回復，則回復可能不會將電腦還原到復原之前存在的相同狀態。</span><span class="sxs-lookup"><span data-stu-id="9f925-176">If an installation using the TypeLib table fails and must be rolled back, the rollback may not restore the computer to the same state that existed prior to the rollback.</span></span> <span data-ttu-id="9f925-177">復原之前註冊的類型程式庫可能不會在復原後註冊。</span><span class="sxs-lookup"><span data-stu-id="9f925-177">Type libraries registered prior to rollback may not be registered after rollback.</span></span>

## <a name="validation"></a><span data-ttu-id="9f925-178">驗證</span><span class="sxs-lookup"><span data-stu-id="9f925-178">Validation</span></span>

<dl>

[<span data-ttu-id="9f925-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="9f925-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9f925-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="9f925-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9f925-181">ICE19</span><span class="sxs-lookup"><span data-stu-id="9f925-181">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="9f925-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="9f925-182">ICE32</span></span>](ice32.md)  
</dl>

 

 



