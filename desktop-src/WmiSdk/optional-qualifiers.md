---
description: 選擇性的限定詞可解決所有符合 CIM 規範的執行情況，這些都不是解讀這些限定詞的必要項。
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: 選用限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996964"
---
# <a name="optional-qualifiers"></a><span data-ttu-id="fe0ed-103">選用限定詞</span><span class="sxs-lookup"><span data-stu-id="fe0ed-103">Optional Qualifiers</span></span>

<span data-ttu-id="fe0ed-104">選擇性的限定詞可解決所有符合 CIM 規範的執行情況，這些都不是解讀這些限定詞的必要項。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-104">Optional qualifiers address recurring situations not common to all CIM-compliant implementations, which are not required to interpret these qualifiers.</span></span> <span data-ttu-id="fe0ed-105">規格中提供選擇性的限定詞，以避免在這些週期性情況下可能會發生的隨機使用者定義限定詞。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-105">Optional qualifiers are provided in the specification to avoid random user-defined qualifiers that might occur in these recurring situations.</span></span>

<dt>

<span data-ttu-id="fe0ed-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**刪除**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-107">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-107">Data type: **boolean**</span></span>

<span data-ttu-id="fe0ed-108">適用于：關聯、參考</span><span class="sxs-lookup"><span data-stu-id="fe0ed-108">Applies to: associations, references</span></span>

<span data-ttu-id="fe0ed-109">針對 [關聯]，指出當關聯中參考的任何物件被刪除，以及關聯中參考的個別物件是否以 **IfDeleted** 限定時，是否必須刪除限定的關聯。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-109">For associations, indicates whether the qualified association must be deleted if any of the objects referenced in the association are deleted and if the respective object referenced in the association is qualified with **IfDeleted**.</span></span> <span data-ttu-id="fe0ed-110">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-110">The default is **FALSE**.</span></span>

<span data-ttu-id="fe0ed-111">若為參考，此辨識符號會指出是否必須刪除參考的物件（如果包含參考的關聯已刪除並以 **IfDeleted** 限定），或者如果關聯中參考的任何物件被刪除，而且關聯中參考的個別物件是以 **IfDeleted** 限定。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-111">For references, this qualifier indicates whether the referenced object must be deleted if the association containing the reference is deleted and qualified with **IfDeleted**, or if any of the objects referenced in the association are deleted and the respective object referenced in the association is qualified with **IfDeleted**.</span></span>

<span data-ttu-id="fe0ed-112">使用方式：應用程式必須追蹤以 **Delete** 限定詞標記的關聯和參考，並適當地刪除關聯或參考。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-112">Usage: Applications must track associations and references marked with the **Delete** qualifier and delete the association or reference appropriately.</span></span> <span data-ttu-id="fe0ed-113">如果關聯中的物件已經刪除，但是未標示為 **IfDeleted**，則不應該刪除關聯。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-113">If an object in the association has been deleted but is not marked with **IfDeleted**, then the association should not be deleted.</span></span>

<span data-ttu-id="fe0ed-114">此使用規則必須在定義 CIM 安全性模型時進行驗證。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-114">This usage rule must be verified when the CIM security model is defined.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**昂貴**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Expensive**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-116">Data type: **boolean**</span></span>

<span data-ttu-id="fe0ed-117">適用物件：屬性、參考、類別、關聯、方法</span><span class="sxs-lookup"><span data-stu-id="fe0ed-117">Applies to: properties, references, classes, associations, methods</span></span>

<span data-ttu-id="fe0ed-118">指出隱含的動作是否需要大量的計算。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-118">Indicates whether the implied action requires extensive computation.</span></span> <span data-ttu-id="fe0ed-119">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-119">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-121">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-121">Data type: **boolean**</span></span>

<span data-ttu-id="fe0ed-122">適用于：關聯和參考</span><span class="sxs-lookup"><span data-stu-id="fe0ed-122">Applies to: associations and references</span></span>

<span data-ttu-id="fe0ed-123">指出如果參考的物件或關聯已刪除，是否必須刪除以 **Delete** 限定之關聯內的所有物件。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-123">Indicates whether all objects within an association that is qualified by **Delete** must be deleted if the referenced object or the association is deleted.</span></span> <span data-ttu-id="fe0ed-124">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-124">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**索引**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexed**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-126">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-126">Data type: **boolean**</span></span>

<span data-ttu-id="fe0ed-127">適用物件：屬性、方法</span><span class="sxs-lookup"><span data-stu-id="fe0ed-127">Applies to: properties, methods</span></span>

<span data-ttu-id="fe0ed-128">指出是否應該為類別屬性編制索引。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-128">Indicates whether a class property should be indexed.</span></span> <span data-ttu-id="fe0ed-129">當套用至存放庫所裝載之類別中的屬性時，這只具有在建立類別時建立 (的意義) 該屬性的快速次要查詢查閱。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-129">When applied to properties in classes hosted by the repository, this only has the meaning of creating (at the time of class creation) a fast secondary query lookup for that property.</span></span>

<span data-ttu-id="fe0ed-130">只允許值 **TRUE** (預設) 。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-130">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**無形**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisible**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-132">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-132">Data type: **boolean**</span></span>

<span data-ttu-id="fe0ed-133">適用于：關聯、屬性、方法、參考、類別</span><span class="sxs-lookup"><span data-stu-id="fe0ed-133">Applies to: associations, properties, methods, references, classes</span></span>

<span data-ttu-id="fe0ed-134">指出此關聯是否僅針對內部用途而定義 (例如，相依性語義的定義) ，而且不應該顯示 (例如對應) 中。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-134">Indicates whether the association is defined only for internal purposes (for example, for definition of dependency semantics) and should not be displayed (for example, in maps).</span></span> <span data-ttu-id="fe0ed-135">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-135">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**大**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Large**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-137">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-137">Data type: **boolean**</span></span>

<span data-ttu-id="fe0ed-138">適用物件：屬性、類別</span><span class="sxs-lookup"><span data-stu-id="fe0ed-138">Applies to: properties, classes</span></span>

<span data-ttu-id="fe0ed-139">指出屬性或類別是否需要大量儲存空間。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-139">Indicates whether the property or class requires a large amount of storage space.</span></span> <span data-ttu-id="fe0ed-140">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-140">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**非 \_ Null**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-142">Data type: **boolean**</span></span>

<span data-ttu-id="fe0ed-143">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="fe0ed-143">Applies to: properties</span></span>

<span data-ttu-id="fe0ed-144">指出類別屬性是否不能採用 **Null** 值 (**VT \_ null**) 。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-144">Indicates whether a class property cannot take on a value of **NULL** (**VT\_NULL**).</span></span> <span data-ttu-id="fe0ed-145">只允許值 **TRUE** (預設) 。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-145">Only the value **TRUE** (default) is allowed.</span></span>

<span data-ttu-id="fe0ed-146">如果指定了此限定詞，則 WMI 不允許建立屬性設為 **null** 的實例，而且 **Null** 屬性會傳回 **WBEM E 不 \_ \_ 合法的 \_ Null** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-146">If this qualifier is specified, WMI does not allow creation of instances with the property set to **NULL**, and **NULL** properties return the **WBEM\_E\_ILLEGAL\_NULL** error code.</span></span>

<span data-ttu-id="fe0ed-147">請注意，索引 [**鍵**](standard-qualifiers.md) 和 **索引** 限定詞已表示此行為。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-147">Note that the [**Key**](standard-qualifiers.md) and **Indexed** qualifiers already imply this behavior.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**供應商**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-149">Data type: **string**</span></span>

<span data-ttu-id="fe0ed-150">適用于： Any</span><span class="sxs-lookup"><span data-stu-id="fe0ed-150">Applies to: Any</span></span>

<span data-ttu-id="fe0ed-151">指出架構元素是動態的，因此是由提供者填入。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-151">Indication that the schema element is dynamic and thus populated by a provider.</span></span> <span data-ttu-id="fe0ed-152">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-152">The default is **NULL**.</span></span> <span data-ttu-id="fe0ed-153">此辨識符號是檢測的特定執行控點。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-153">This qualifier is an implementation-specific handle to the instrumentation.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**實驗**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-155">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-155">Data type: **boolean**</span></span>

<span data-ttu-id="fe0ed-156">適用于： any</span><span class="sxs-lookup"><span data-stu-id="fe0ed-156">Applies to: any</span></span>

<span data-ttu-id="fe0ed-157">指出已將指定的專案建議為未來版本的 CIM 架構，但還不是標準架構的一部分。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-157">Indicates that the specified element has been proposed to be a part of a future release of the CIM Schemas, but is not yet part of the standard Schema.</span></span> <span data-ttu-id="fe0ed-158">相反地，專案可供使用者進行實驗、執行並提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-158">Instead, the element is available for users to experiment, implement, and provide feedback on.</span></span> <span data-ttu-id="fe0ed-159">根據意見反應，元素可能會新增至提供、修改或移除的標準。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-159">Based on feedback, the element may added to the standard as presented, modified, or removed.</span></span> <span data-ttu-id="fe0ed-160">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-160">The default is **FALSE**.</span></span> <span data-ttu-id="fe0ed-161">執行不需要支援具有此辨識符號的元素。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-161">An implementation does not have to support an element with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-163">Data type: **string**</span></span>

<span data-ttu-id="fe0ed-164">適用物件：屬性、參考、方法、參數</span><span class="sxs-lookup"><span data-stu-id="fe0ed-164">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="fe0ed-165">指派給資料項目的特定類型。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-165">Specific type assigned to a data item.</span></span> <span data-ttu-id="fe0ed-166">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-166">The default is **NULL**.</span></span>

<span data-ttu-id="fe0ed-167">使用方式：您必須使用 **SyntaxType** 限定詞搭配此限定詞。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-167">Usage: You must use the **SyntaxType** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-169">Data type: **string**</span></span>

<span data-ttu-id="fe0ed-170">適用物件：屬性、參考、方法、參數</span><span class="sxs-lookup"><span data-stu-id="fe0ed-170">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="fe0ed-171">**語法** 辨識符號的格式。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-171">Format of the **Syntax** qualifier.</span></span> <span data-ttu-id="fe0ed-172">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-172">The default is **NULL**.</span></span>

<span data-ttu-id="fe0ed-173">使用方式：您必須使用 **語法** 辨識符號搭配此限定詞。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-173">Usage: You must use the **Syntax** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-175">Data type: **string**</span></span>

<span data-ttu-id="fe0ed-176">適用物件：類別、屬性、方法、關聯、指示、參考</span><span class="sxs-lookup"><span data-stu-id="fe0ed-176">Applies to: classes, properties, methods, associations, indications, references</span></span>

<span data-ttu-id="fe0ed-177">引發觸發程式的情況。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-177">Circumstances under which a trigger is fired.</span></span> <span data-ttu-id="fe0ed-178">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-178">The default is **NULL**.</span></span> <span data-ttu-id="fe0ed-179">觸發程式類型會依中繼模型結構而有所不同。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-179">The trigger types vary by meta-model construct.</span></span>

<span data-ttu-id="fe0ed-180">若為類別和關聯，合法值為：</span><span class="sxs-lookup"><span data-stu-id="fe0ed-180">For classes and associations, the legal values are:</span></span>

<span data-ttu-id="fe0ed-181">建立</span><span class="sxs-lookup"><span data-stu-id="fe0ed-181">Create</span></span>

<span data-ttu-id="fe0ed-182">刪除</span><span class="sxs-lookup"><span data-stu-id="fe0ed-182">Delete</span></span>

<span data-ttu-id="fe0ed-183">更新</span><span class="sxs-lookup"><span data-stu-id="fe0ed-183">Update</span></span>

<span data-ttu-id="fe0ed-184">Access</span><span class="sxs-lookup"><span data-stu-id="fe0ed-184">Access</span></span>

<span data-ttu-id="fe0ed-185">針對屬性和參考，合法值為： Update 和 Access。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-185">For properties and references, the legal values are: Update and Access.</span></span>

<span data-ttu-id="fe0ed-186">針對方法，合法的值會在之前和之後。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-186">For methods, the legal values are Before and After.</span></span>

<span data-ttu-id="fe0ed-187">如果是指示，則會擲回合法值。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-187">For indications, the legal value is Thrown.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-189">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-189">Data type: **string array**</span></span>

<span data-ttu-id="fe0ed-190">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="fe0ed-190">Applies to: properties</span></span>

<span data-ttu-id="fe0ed-191">值的集合，表示相關聯屬性的值是未知的 (無法將屬性視為具有有效或有意義的值) 。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-191">Set of values indicating that the value of the associated property is unknown (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="fe0ed-192">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-192">The default is **NULL**.</span></span>

<span data-ttu-id="fe0ed-193">用來定義未知值的慣例和限制與適用于 [**ValueMap**](standard-qualifiers.md) 辨識符號的慣例和限制相同。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-193">The conventions and restrictions used for defining unknown values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="fe0ed-194">請注意，無法覆寫此限定詞。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-194">Note that this qualifier cannot be overridden.</span></span> <span data-ttu-id="fe0ed-195">當某個子類別視為某個父類別的未知值時，允許子類別將該值視為已知值是不合理的。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-195">It is unreasonable to permit a subclass to treat a value as a known value when it is treated as unknown by some parent class.</span></span>

</dd> <dt>

<span data-ttu-id="fe0ed-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span></span>
</dt> <dd>

<span data-ttu-id="fe0ed-197">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="fe0ed-197">Data type: **string array**</span></span>

<span data-ttu-id="fe0ed-198">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="fe0ed-198">Applies to: properties</span></span>

<span data-ttu-id="fe0ed-199">值的集合，表示不支援相關聯屬性的值 (無法將屬性視為具有有效或有意義的值) 。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-199">Set of values indicating that the value of the associated property is unsupported (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="fe0ed-200">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-200">The default is **NULL**.</span></span>

<span data-ttu-id="fe0ed-201">用來定義不支援值的慣例和限制與適用于 [**ValueMap**](standard-qualifiers.md) 辨識符號的慣例和限制相同。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-201">The conventions and restrictions used for defining unsupported values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="fe0ed-202">注意：無法覆寫此限定詞。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-202">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="fe0ed-203">允許子類別將值視為支援的值（由某些父類別視為未知）是不合理的。</span><span class="sxs-lookup"><span data-stu-id="fe0ed-203">It is unreasonable to permit a subclass to treat a value as a supported value that is treated as unknown by some parent class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe0ed-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe0ed-204">Requirements</span></span>



| <span data-ttu-id="fe0ed-205">需求</span><span class="sxs-lookup"><span data-stu-id="fe0ed-205">Requirement</span></span> | <span data-ttu-id="fe0ed-206">值</span><span class="sxs-lookup"><span data-stu-id="fe0ed-206">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fe0ed-207">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe0ed-207">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0ed-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe0ed-208">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fe0ed-209">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe0ed-209">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0ed-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe0ed-210">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe0ed-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe0ed-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0ed-212">WMI 限定詞</span><span class="sxs-lookup"><span data-stu-id="fe0ed-212">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="fe0ed-213">新增限定詞</span><span class="sxs-lookup"><span data-stu-id="fe0ed-213">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




