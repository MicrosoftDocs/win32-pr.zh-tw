---
description: ModuleConfiguration 資料表會識別模組的可設定屬性。 這個資料表不會合並到資料庫中。
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: ModuleConfiguration 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193310"
---
# <a name="moduleconfiguration-table"></a><span data-ttu-id="a6608-104">ModuleConfiguration 資料表</span><span class="sxs-lookup"><span data-stu-id="a6608-104">ModuleConfiguration Table</span></span>

<span data-ttu-id="a6608-105">ModuleConfiguration 資料表會識別模組的可設定屬性。</span><span class="sxs-lookup"><span data-stu-id="a6608-105">The ModuleConfiguration table identifies the configurable attributes of the module.</span></span> <span data-ttu-id="a6608-106">這個資料表不會合並到資料庫中。</span><span class="sxs-lookup"><span data-stu-id="a6608-106">This table is not merged into the database.</span></span>

<span data-ttu-id="a6608-107">ModuleConfiguration 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="a6608-107">The ModuleConfiguration table has the following columns.</span></span>



| <span data-ttu-id="a6608-108">Column</span><span class="sxs-lookup"><span data-stu-id="a6608-108">Column</span></span>       | <span data-ttu-id="a6608-109">類型</span><span class="sxs-lookup"><span data-stu-id="a6608-109">Type</span></span>                         | <span data-ttu-id="a6608-110">答案</span><span class="sxs-lookup"><span data-stu-id="a6608-110">Key</span></span> | <span data-ttu-id="a6608-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="a6608-111">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="a6608-112">Name</span><span class="sxs-lookup"><span data-stu-id="a6608-112">Name</span></span>         | [<span data-ttu-id="a6608-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="a6608-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="a6608-114">Y</span><span class="sxs-lookup"><span data-stu-id="a6608-114">Y</span></span>   | <span data-ttu-id="a6608-115">N</span><span class="sxs-lookup"><span data-stu-id="a6608-115">N</span></span>        |
| <span data-ttu-id="a6608-116">格式</span><span class="sxs-lookup"><span data-stu-id="a6608-116">Format</span></span>       | [<span data-ttu-id="a6608-117">整數</span><span class="sxs-lookup"><span data-stu-id="a6608-117">Integer</span></span>](integer.md)       | <span data-ttu-id="a6608-118">N</span><span class="sxs-lookup"><span data-stu-id="a6608-118">N</span></span>   | <span data-ttu-id="a6608-119">N</span><span class="sxs-lookup"><span data-stu-id="a6608-119">N</span></span>        |
| <span data-ttu-id="a6608-120">類型</span><span class="sxs-lookup"><span data-stu-id="a6608-120">Type</span></span>         | [<span data-ttu-id="a6608-121">Text</span><span class="sxs-lookup"><span data-stu-id="a6608-121">Text</span></span>](text.md)             | <span data-ttu-id="a6608-122">N</span><span class="sxs-lookup"><span data-stu-id="a6608-122">N</span></span>   | <span data-ttu-id="a6608-123">Y</span><span class="sxs-lookup"><span data-stu-id="a6608-123">Y</span></span>        |
| <span data-ttu-id="a6608-124">CoNtextData</span><span class="sxs-lookup"><span data-stu-id="a6608-124">ContextData</span></span>  | [<span data-ttu-id="a6608-125">Text</span><span class="sxs-lookup"><span data-stu-id="a6608-125">Text</span></span>](text.md)             | <span data-ttu-id="a6608-126">N</span><span class="sxs-lookup"><span data-stu-id="a6608-126">N</span></span>   | <span data-ttu-id="a6608-127">Y</span><span class="sxs-lookup"><span data-stu-id="a6608-127">Y</span></span>        |
| <span data-ttu-id="a6608-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a6608-128">DefaultValue</span></span> | [<span data-ttu-id="a6608-129">Text</span><span class="sxs-lookup"><span data-stu-id="a6608-129">Text</span></span>](text.md)             | <span data-ttu-id="a6608-130">N</span><span class="sxs-lookup"><span data-stu-id="a6608-130">N</span></span>   | <span data-ttu-id="a6608-131">Y</span><span class="sxs-lookup"><span data-stu-id="a6608-131">Y</span></span>        |
| <span data-ttu-id="a6608-132">屬性</span><span class="sxs-lookup"><span data-stu-id="a6608-132">Attributes</span></span>   | [<span data-ttu-id="a6608-133">整數</span><span class="sxs-lookup"><span data-stu-id="a6608-133">Integer</span></span>](integer.md)       | <span data-ttu-id="a6608-134">N</span><span class="sxs-lookup"><span data-stu-id="a6608-134">N</span></span>   | <span data-ttu-id="a6608-135">Y</span><span class="sxs-lookup"><span data-stu-id="a6608-135">Y</span></span>        |
| <span data-ttu-id="a6608-136">DisplayName</span><span class="sxs-lookup"><span data-stu-id="a6608-136">DisplayName</span></span>  | [<span data-ttu-id="a6608-137">Text</span><span class="sxs-lookup"><span data-stu-id="a6608-137">Text</span></span>](text.md)             | <span data-ttu-id="a6608-138">N</span><span class="sxs-lookup"><span data-stu-id="a6608-138">N</span></span>   | <span data-ttu-id="a6608-139">Y</span><span class="sxs-lookup"><span data-stu-id="a6608-139">Y</span></span>        |
| <span data-ttu-id="a6608-140">Description</span><span class="sxs-lookup"><span data-stu-id="a6608-140">Description</span></span>  | [<span data-ttu-id="a6608-141">Text</span><span class="sxs-lookup"><span data-stu-id="a6608-141">Text</span></span>](text.md)             | <span data-ttu-id="a6608-142">N</span><span class="sxs-lookup"><span data-stu-id="a6608-142">N</span></span>   | <span data-ttu-id="a6608-143">Y</span><span class="sxs-lookup"><span data-stu-id="a6608-143">Y</span></span>        |
| <span data-ttu-id="a6608-144">HelpLocation</span><span class="sxs-lookup"><span data-stu-id="a6608-144">HelpLocation</span></span> | [<span data-ttu-id="a6608-145">Text</span><span class="sxs-lookup"><span data-stu-id="a6608-145">Text</span></span>](text.md)             | <span data-ttu-id="a6608-146">N</span><span class="sxs-lookup"><span data-stu-id="a6608-146">N</span></span>   | <span data-ttu-id="a6608-147">Y</span><span class="sxs-lookup"><span data-stu-id="a6608-147">Y</span></span>        |
| <span data-ttu-id="a6608-148">HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="a6608-148">HelpKeyword</span></span>  | [<span data-ttu-id="a6608-149">Text</span><span class="sxs-lookup"><span data-stu-id="a6608-149">Text</span></span>](text.md)             | <span data-ttu-id="a6608-150">N</span><span class="sxs-lookup"><span data-stu-id="a6608-150">N</span></span>   | <span data-ttu-id="a6608-151">Y</span><span class="sxs-lookup"><span data-stu-id="a6608-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a6608-152">資料行</span><span class="sxs-lookup"><span data-stu-id="a6608-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a6608-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="a6608-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a6608-154">此欄位定義可設定專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6608-154">This field defines the name of the configurable item.</span></span> <span data-ttu-id="a6608-155">這個名稱會在 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中的格式化範本中參考。</span><span class="sxs-lookup"><span data-stu-id="a6608-155">This name is referenced in the formatting template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6608-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>格式</span><span class="sxs-lookup"><span data-stu-id="a6608-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format</span></span>
</dt> <dd>

<span data-ttu-id="a6608-157">此資料行指定要變更的資料格式。</span><span class="sxs-lookup"><span data-stu-id="a6608-157">This column specifies the format of the data being changed.</span></span>



| <span data-ttu-id="a6608-158">格式</span><span class="sxs-lookup"><span data-stu-id="a6608-158">Format</span></span>                                       | <span data-ttu-id="a6608-159">值</span><span class="sxs-lookup"><span data-stu-id="a6608-159">Value</span></span> |
|----------------------------------------------|-------|
| [<span data-ttu-id="a6608-160">Text</span><span class="sxs-lookup"><span data-stu-id="a6608-160">Text</span></span>](text-format-types.md)                | <span data-ttu-id="a6608-161">0</span><span class="sxs-lookup"><span data-stu-id="a6608-161">0</span></span>     |
| [<span data-ttu-id="a6608-162">金鑰</span><span class="sxs-lookup"><span data-stu-id="a6608-162">Key</span></span>](key-format-types.md)                  | <span data-ttu-id="a6608-163">1</span><span class="sxs-lookup"><span data-stu-id="a6608-163">1</span></span>     |
| [<span data-ttu-id="a6608-164">整數</span><span class="sxs-lookup"><span data-stu-id="a6608-164">Integer</span></span>](integer-format-types.md)          | <span data-ttu-id="a6608-165">2</span><span class="sxs-lookup"><span data-stu-id="a6608-165">2</span></span>     |
| [<span data-ttu-id="a6608-166">位位格式</span><span class="sxs-lookup"><span data-stu-id="a6608-166">Bitfield Format</span></span>](bitfield-format-types.md) | <span data-ttu-id="a6608-167">3</span><span class="sxs-lookup"><span data-stu-id="a6608-167">3</span></span>     |



 

</dd> <dt>

<span data-ttu-id="a6608-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型</span><span class="sxs-lookup"><span data-stu-id="a6608-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="a6608-169">這個資料行會指定變更資料的類型。</span><span class="sxs-lookup"><span data-stu-id="a6608-169">This column specifies the type for the data being changed.</span></span> <span data-ttu-id="a6608-170">此類型是用來提供任何使用者介面的內容，而且不會用於合併進程。</span><span class="sxs-lookup"><span data-stu-id="a6608-170">This type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="a6608-171">此資料行的有效值取決於 Format 資料行中的值。</span><span class="sxs-lookup"><span data-stu-id="a6608-171">The valid values for this column depend on the value in the Format column.</span></span>

</dd> <dt>

<span data-ttu-id="a6608-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>CoNtextData</span><span class="sxs-lookup"><span data-stu-id="a6608-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span></span>
</dt> <dd>

<span data-ttu-id="a6608-173">這個資料行會指定所要求資料的語義內容。</span><span class="sxs-lookup"><span data-stu-id="a6608-173">This column specifies a semantic context for the requested data.</span></span> <span data-ttu-id="a6608-174">類型是用來提供任何使用者介面的內容，而且不會用於合併處理。</span><span class="sxs-lookup"><span data-stu-id="a6608-174">The type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="a6608-175">此資料行的有效值取決於 [格式] 和 [類型] 資料行中的值。</span><span class="sxs-lookup"><span data-stu-id="a6608-175">The valid values for this column depend on the values in the Format and Type columns.</span></span>

</dd> <dt>

<span data-ttu-id="a6608-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>值</span><span class="sxs-lookup"><span data-stu-id="a6608-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span></span>
</dt> <dd>

<span data-ttu-id="a6608-177">如果合併工具拒絕提供值，此資料行會指定此記錄中專案的預設值。</span><span class="sxs-lookup"><span data-stu-id="a6608-177">This column specifies a default value for the item in this record if the merge tool declines to provide a value.</span></span> <span data-ttu-id="a6608-178">這個值必須具有專案的格式、類型和內容。</span><span class="sxs-lookup"><span data-stu-id="a6608-178">This value must have the format, type, and context of the item.</span></span> <span data-ttu-id="a6608-179">如果這是「金鑰」格式專案，外鍵必須是模組資料表中的有效索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a6608-179">If this is a "Key" format item, the foreign key must be a valid key into the tables of the module.</span></span> <span data-ttu-id="a6608-180">根據專案而定，Null 可能是此資料行的有效值。</span><span class="sxs-lookup"><span data-stu-id="a6608-180">Null may be a valid value for this column depending on the item.</span></span> <span data-ttu-id="a6608-181">針對「金鑰」格式專案，此值採用 [CMSM 的特殊格式](cmsm-special-format.md)。</span><span class="sxs-lookup"><span data-stu-id="a6608-181">For "Key" format items, this value is in [CMSM special format](cmsm-special-format.md).</span></span> <span data-ttu-id="a6608-182">若為所有其他類型，則會將值視為字面處理。</span><span class="sxs-lookup"><span data-stu-id="a6608-182">For all other types, the value is treated literally.</span></span>

<span data-ttu-id="a6608-183">模組作者必須確保模組在其預設狀態中是有效的。</span><span class="sxs-lookup"><span data-stu-id="a6608-183">Module authors must ensure that the module is valid in its default state.</span></span> <span data-ttu-id="a6608-184">這可確保2.0 版之前的 Mergemod.dll 版本仍可使用其預設狀態中的模組。</span><span class="sxs-lookup"><span data-stu-id="a6608-184">This ensures that versions of Mergemod.dll earlier than version 2.0 can still use the module in its default state.</span></span>

</dd> <dt>

<span data-ttu-id="a6608-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="a6608-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="a6608-186">此資料行是一個位欄位，其中包含這個可設定專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="a6608-186">This column is a bit field containing attributes for this configurable item.</span></span> <span data-ttu-id="a6608-187">Null 相當於0。</span><span class="sxs-lookup"><span data-stu-id="a6608-187">Null is equivalent to 0.</span></span> <span data-ttu-id="a6608-188">此資料行中的所有其他位都保留供日後使用，且必須為0。</span><span class="sxs-lookup"><span data-stu-id="a6608-188">All other bits in this column are reserved for future use and must be 0.</span></span>



| <span data-ttu-id="a6608-189">Name</span><span class="sxs-lookup"><span data-stu-id="a6608-189">Name</span></span>                             | <span data-ttu-id="a6608-190">Decimal</span><span class="sxs-lookup"><span data-stu-id="a6608-190">Decimal</span></span> | <span data-ttu-id="a6608-191">十六進位</span><span class="sxs-lookup"><span data-stu-id="a6608-191">Hexadecimal</span></span> | <span data-ttu-id="a6608-192">Description</span><span class="sxs-lookup"><span data-stu-id="a6608-192">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6608-193">msmConfigurableOptionKeyNoOrphan</span><span class="sxs-lookup"><span data-stu-id="a6608-193">msmConfigurableOptionKeyNoOrphan</span></span> | <span data-ttu-id="a6608-194">1</span><span class="sxs-lookup"><span data-stu-id="a6608-194">1</span></span>       | <span data-ttu-id="a6608-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a6608-195">0x00000001</span></span>  | <span data-ttu-id="a6608-196">這個屬性只適用于在其 DefaultValue 欄位中列出模組資料表外鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="a6608-196">This attribute only applies to records that list a foreign key to a module table in their DefaultValue field.</span></span> <span data-ttu-id="a6608-197">合併工具會忽略索引 [鍵格式類型](key-format-types.md)以外之任何格式的屬性。</span><span class="sxs-lookup"><span data-stu-id="a6608-197">The merge tool ignores the attribute for any formats other than the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="a6608-198">下列檢查會排除未列在 [ModuleSubstitution 資料表](modulesubstitution-table.md) 中的專案。</span><span class="sxs-lookup"><span data-stu-id="a6608-198">Items not listed in the [ModuleSubstitution table](modulesubstitution-table.md) are excluded from the following check.</span></span> <span data-ttu-id="a6608-199">如果在完成所有設定選項之後滿足下列條件，則合併工具不會將 DefaultValue 資料行所參考的資料列合併到目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="a6608-199">The merge tool does not merge the row referenced by the DefaultValue column into the target database if the following conditions are satisfied after completing all configuration options.</span></span><br/> <span data-ttu-id="a6608-200">ModuleConfiguration 資料表中具有相同 DefaultValue 的每個資料列都會設定 msmConfigurationItemsKeyNoOrphan。</span><span class="sxs-lookup"><span data-stu-id="a6608-200">Every row in the ModuleConfiguration table with the same DefaultValue has the msmConfigurationItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="a6608-201">沒有任何資料列使用 DefaultValue，因為 authoring tool 已拒絕提供值。</span><span class="sxs-lookup"><span data-stu-id="a6608-201">No rows use the DefaultValue because the authoring tool declined to provide a value.</span></span><br/> <span data-ttu-id="a6608-202">如果符合下列任一條件，則合併工具會合並資料列。</span><span class="sxs-lookup"><span data-stu-id="a6608-202">The merge tool merges the row if any of the following conditions are satisfied.</span></span><br/> <span data-ttu-id="a6608-203">合併工具會尋找未設定 msmConfigItemsKeyNoOrphan 的任何資料列。</span><span class="sxs-lookup"><span data-stu-id="a6608-203">The merge tool finds any row that does not have msmConfigItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="a6608-204">如果合併工具使用 DefaultValue 找到任何資料列，因為 authoring tool 已拒絕提供值。</span><span class="sxs-lookup"><span data-stu-id="a6608-204">If the merge tool finds any row using DefaultValue because the authoring tool declined to provide a value.</span></span><br/> |
| <span data-ttu-id="a6608-205">msmConfigurableOptionNonNullable</span><span class="sxs-lookup"><span data-stu-id="a6608-205">msmConfigurableOptionNonNullable</span></span> | <span data-ttu-id="a6608-206">2</span><span class="sxs-lookup"><span data-stu-id="a6608-206">2</span></span>       | <span data-ttu-id="a6608-207">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a6608-207">0x00000002</span></span>  | <span data-ttu-id="a6608-208">當設定這個屬性時，null 不是此專案的有效回應。</span><span class="sxs-lookup"><span data-stu-id="a6608-208">When this attribute is set, null is not a valid response for this item.</span></span> <span data-ttu-id="a6608-209">這個屬性不會影響 [整數格式類型](integer-format-types.md) 或位欄位 [格式類型](bitfield-format-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a6608-209">This attribute has no effect for [Integer Format Types](integer-format-types.md) or [Bitfield Format Types](bitfield-format-types.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="a6608-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span><span class="sxs-lookup"><span data-stu-id="a6608-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="a6608-211">本資料行提供 authoring tool 可能在使用者介面中使用之這個專案的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="a6608-211">This column provides a short description of this item that the authoring tool may use in the user interface.</span></span> <span data-ttu-id="a6608-212">此資料行可能尚未當地語系化。</span><span class="sxs-lookup"><span data-stu-id="a6608-212">This column may not be localized.</span></span> <span data-ttu-id="a6608-213">將此資料行設定為 null，讓模組要求 authoring tool 不會在 UI 中公開此屬性。</span><span class="sxs-lookup"><span data-stu-id="a6608-213">Set this column to null to have the module is request that the authoring tool not expose this property in the UI.</span></span> <span data-ttu-id="a6608-214">此工具可能會忽略此欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="a6608-214">The tool may disregard the value in this field.</span></span>

</dd> <dt>

<span data-ttu-id="a6608-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="a6608-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="a6608-216">此資料行提供 authoring tool 可在 UI 元素中使用的這個專案的描述。</span><span class="sxs-lookup"><span data-stu-id="a6608-216">This column provides a description of this item that the authoring tool may use in UI elements.</span></span> <span data-ttu-id="a6608-217">這個字串可能會由模組的語言轉換所當地語系化。</span><span class="sxs-lookup"><span data-stu-id="a6608-217">This string may be localized by the module's language transform.</span></span> <span data-ttu-id="a6608-218">此資料行可以是 null。</span><span class="sxs-lookup"><span data-stu-id="a6608-218">This column may be null.</span></span>

</dd> <dt>

<span data-ttu-id="a6608-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span><span class="sxs-lookup"><span data-stu-id="a6608-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span></span>
</dt> <dd>

<span data-ttu-id="a6608-220">此資料行提供說明檔的名稱 (不含 .chm 副檔名) 或以分號分隔的說明命名空間清單。</span><span class="sxs-lookup"><span data-stu-id="a6608-220">This column provides either the name of a help file (without the .chm extension) or a semicolon delimited list of help namespaces.</span></span> <span data-ttu-id="a6608-221">如果沒有可用的說明，此資料行可以是 null。</span><span class="sxs-lookup"><span data-stu-id="a6608-221">This column can be null if no help is available.</span></span> <span data-ttu-id="a6608-222">只有當 HelpKeyword 資料行是 null 時，這個資料行才可以是 null。</span><span class="sxs-lookup"><span data-stu-id="a6608-222">This column can be null only if the HelpKeyword column is null.</span></span>

</dd> <dt>

<span data-ttu-id="a6608-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="a6608-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span></span>
</dt> <dd>

<span data-ttu-id="a6608-224">這個資料行會從 HelpLocation 資料行提供說明檔或命名空間中的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="a6608-224">This column provides a keyword into the help file or namespace from the HelpLocation column.</span></span> <span data-ttu-id="a6608-225">此關鍵字的解讀取決於 HelpLocation 資料行。</span><span class="sxs-lookup"><span data-stu-id="a6608-225">The interpretation of this keyword depends on the HelpLocation column.</span></span> <span data-ttu-id="a6608-226">此資料行可以是 null。</span><span class="sxs-lookup"><span data-stu-id="a6608-226">This column may be null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6608-227">備註</span><span class="sxs-lookup"><span data-stu-id="a6608-227">Remarks</span></span>

<span data-ttu-id="a6608-228">ModuleConfiguration 資料表是由可設定的 [合併模組](configurable-merge-modules.md)所使用。</span><span class="sxs-lookup"><span data-stu-id="a6608-228">The ModuleConfiguration table is used by [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="a6608-229">需要 Mergemod.dll 2.0 或更新版本，才能建立可設定的合併模組。</span><span class="sxs-lookup"><span data-stu-id="a6608-229">Mergemod.dll 2.0 or later is required to create a configurable merge module.</span></span>

<span data-ttu-id="a6608-230">為了確保與舊版 Mergemod.dll 的相容性，ModuleConfiguration 資料表和 [ModuleSubstitution 資料表](modulesubstitution-table.md) 應該加入至每個模組的 [ModuleIgnoreTable 資料表](moduleignoretable-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="a6608-230">To ensure compatibility with older versions of Mergemod.dll, the ModuleConfiguration table and [ModuleSubstitution table](modulesubstitution-table.md) should be added to the [ModuleIgnoreTable table](moduleignoretable-table.md) of every module.</span></span>

## <a name="validation"></a><span data-ttu-id="a6608-231">驗證</span><span class="sxs-lookup"><span data-stu-id="a6608-231">Validation</span></span>

<dl>

[<span data-ttu-id="a6608-232">ICE03</span><span class="sxs-lookup"><span data-stu-id="a6608-232">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a6608-233">ICE06</span><span class="sxs-lookup"><span data-stu-id="a6608-233">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a6608-234">ICE25</span><span class="sxs-lookup"><span data-stu-id="a6608-234">ICE25</span></span>](ice25.md)  
[<span data-ttu-id="a6608-235">ICE45</span><span class="sxs-lookup"><span data-stu-id="a6608-235">ICE45</span></span>](ice45.md)  
</dl>

 

 




