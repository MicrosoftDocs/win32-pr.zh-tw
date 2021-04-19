---
description: MsiPatchSequence 資料表包含安裝程式所需的所有資訊，以判斷相對於所有其他修補程式的小型更新修補程式順序。
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: MsiPatchSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979400"
---
# <a name="msipatchsequence-table"></a><span data-ttu-id="09ba2-103">MsiPatchSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="09ba2-103">MsiPatchSequence Table</span></span>

<span data-ttu-id="09ba2-104">MsiPatchSequence 資料表包含安裝程式所需的所有資訊，以判斷相對於所有其他修補程式的 [小型更新](small-updates.md) 修補程式順序。</span><span class="sxs-lookup"><span data-stu-id="09ba2-104">The MsiPatchSequence table contains all the information the installer requires to determine the sequence of application of a [small update](small-updates.md) patch relative to all other patches.</span></span> <span data-ttu-id="09ba2-105">資料表必須在 patch 檔案的資料庫中，而不是在修補程式的轉換中。</span><span class="sxs-lookup"><span data-stu-id="09ba2-105">The table must be in the database of the patch file and not in a transform in the patch.</span></span> <span data-ttu-id="09ba2-106">套用 [主要升級](major-upgrades.md) 修補程式時，安裝程式會忽略此資料表。</span><span class="sxs-lookup"><span data-stu-id="09ba2-106">The installer ignores this table when applying a [major upgrade](major-upgrades.md) patch.</span></span> <span data-ttu-id="09ba2-107">套用 [次要升級](minor-upgrades.md) 修補程式時，安裝程式只會使用此資料表來識別不得排序的已取代修補程式。</span><span class="sxs-lookup"><span data-stu-id="09ba2-107">When applying a [minor upgrade](minor-upgrades.md) patch, the installer only uses this table to identify superseded patches that must not be sequenced.</span></span>

<span data-ttu-id="09ba2-108">**MsiPatchSequence 資料表** 具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="09ba2-108">The **MsiPatchSequence table** has the following columns.</span></span>



| <span data-ttu-id="09ba2-109">Column</span><span class="sxs-lookup"><span data-stu-id="09ba2-109">Column</span></span>      | <span data-ttu-id="09ba2-110">類型</span><span class="sxs-lookup"><span data-stu-id="09ba2-110">Type</span></span>                         | <span data-ttu-id="09ba2-111">答案</span><span class="sxs-lookup"><span data-stu-id="09ba2-111">Key</span></span> | <span data-ttu-id="09ba2-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="09ba2-112">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="09ba2-113">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="09ba2-113">PatchFamily</span></span> | [<span data-ttu-id="09ba2-114">識別碼</span><span class="sxs-lookup"><span data-stu-id="09ba2-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="09ba2-115">Y</span><span class="sxs-lookup"><span data-stu-id="09ba2-115">Y</span></span>   | <span data-ttu-id="09ba2-116">N</span><span class="sxs-lookup"><span data-stu-id="09ba2-116">N</span></span>        |
| <span data-ttu-id="09ba2-117">ProductCode</span><span class="sxs-lookup"><span data-stu-id="09ba2-117">ProductCode</span></span> | [<span data-ttu-id="09ba2-118">GUID</span><span class="sxs-lookup"><span data-stu-id="09ba2-118">GUID</span></span>](guid.md)             | <span data-ttu-id="09ba2-119">Y</span><span class="sxs-lookup"><span data-stu-id="09ba2-119">Y</span></span>   | <span data-ttu-id="09ba2-120">Y</span><span class="sxs-lookup"><span data-stu-id="09ba2-120">Y</span></span>        |
| <span data-ttu-id="09ba2-121">順序</span><span class="sxs-lookup"><span data-stu-id="09ba2-121">Sequence</span></span>    | [<span data-ttu-id="09ba2-122">版本</span><span class="sxs-lookup"><span data-stu-id="09ba2-122">Version</span></span>](version.md)       | <span data-ttu-id="09ba2-123">N</span><span class="sxs-lookup"><span data-stu-id="09ba2-123">N</span></span>   | <span data-ttu-id="09ba2-124">N</span><span class="sxs-lookup"><span data-stu-id="09ba2-124">N</span></span>        |
| <span data-ttu-id="09ba2-125">屬性</span><span class="sxs-lookup"><span data-stu-id="09ba2-125">Attributes</span></span>  | [<span data-ttu-id="09ba2-126">整數</span><span class="sxs-lookup"><span data-stu-id="09ba2-126">Integer</span></span>](integer.md)       | <span data-ttu-id="09ba2-127">N</span><span class="sxs-lookup"><span data-stu-id="09ba2-127">N</span></span>   | <span data-ttu-id="09ba2-128">Y</span><span class="sxs-lookup"><span data-stu-id="09ba2-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="09ba2-129">資料行</span><span class="sxs-lookup"><span data-stu-id="09ba2-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="09ba2-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="09ba2-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="09ba2-131">指定修補程式是在此欄位中命名之修補程式系列的成員。</span><span class="sxs-lookup"><span data-stu-id="09ba2-131">Specifies that the patch is a member of the patch family named in this field.</span></span> <span data-ttu-id="09ba2-132">相同修補系列中以相同產品版本為目標的修補程式，會依 [順序] 資料行中的值進行排序。</span><span class="sxs-lookup"><span data-stu-id="09ba2-132">Patches in the same patch family that target the same product version are sorted by the values in the Sequence column.</span></span> <span data-ttu-id="09ba2-133">修補程式系列內的修補程式會依照順序遞增順序套用至目標產品。</span><span class="sxs-lookup"><span data-stu-id="09ba2-133">The patches within the patch family are applied to the target product in the order of increasing sequence.</span></span> <span data-ttu-id="09ba2-134">PatchFamily 也可用來判斷要取代的修補程式。</span><span class="sxs-lookup"><span data-stu-id="09ba2-134">The PatchFamily is also used to determine which patches are to be superseded.</span></span> <span data-ttu-id="09ba2-135">修補程式可能會在多個資料列中列出，而且如果它適用于多個產品或包含多個修正，則屬於多個修補程式系列。</span><span class="sxs-lookup"><span data-stu-id="09ba2-135">A patch may be listed in multiple rows and belong to multiple patch families if it applies to more than one product or includes multiple fixes.</span></span>

<span data-ttu-id="09ba2-136">Windows Installer 不會以任何不同的方式來解讀 PatchFamily 值，而不是比較是否等於其他 PatchFamily 值。</span><span class="sxs-lookup"><span data-stu-id="09ba2-136">The Windows Installer does not interpret the PatchFamily value in any way other than comparisons for equality against other PatchFamily values.</span></span> <span data-ttu-id="09ba2-137">PatchFamily 值在一組修補程式以目標的 ProductCode 中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="09ba2-137">A PatchFamily value must be unique within the ProductCode targeted by the set of patches.</span></span> <span data-ttu-id="09ba2-138">在複雜的修補案例中，PatchFamily 識別碼可能必須是全域唯一的。</span><span class="sxs-lookup"><span data-stu-id="09ba2-138">In the complex patching scenarios the PatchFamily identifier may need to be globally unique.</span></span>

</dd> <dt>

<span data-ttu-id="09ba2-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span><span class="sxs-lookup"><span data-stu-id="09ba2-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span></span>
</dt> <dd>

<span data-ttu-id="09ba2-140">此欄位中的值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="09ba2-140">A value in this field is optional.</span></span> <span data-ttu-id="09ba2-141">如果在此欄位中輸入 [產品代碼](product-codes.md) GUID，並將修補程式套用至指定的產品，則會將修補程式排序並套用為指定之 PatchFamily 的成員。</span><span class="sxs-lookup"><span data-stu-id="09ba2-141">If a [product code](product-codes.md) GUID is entered in this field and the patch is being applied to the specified product, the patch is sorted and applied as a member of the specified PatchFamily.</span></span> <span data-ttu-id="09ba2-142">如果在此欄位中輸入產品代碼 GUID，而修補程式未套用至 [ProductCode] 所指定的產品，則會忽略此資料列。</span><span class="sxs-lookup"><span data-stu-id="09ba2-142">If a product code GUID is entered in this field and the patch is not being applied to the product specified by ProductCode, this row is ignored.</span></span> <span data-ttu-id="09ba2-143">如果 [ProductCode] 中的值為 Null，則會將修補程式排序並套用為所有修補目標的 PatchFamily 成員，而不論產品程式碼為何。</span><span class="sxs-lookup"><span data-stu-id="09ba2-143">If the value in ProductCode is NULL, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

<span data-ttu-id="09ba2-144">修補程式可能會在相同的 PatchFamily 中有多個資料列，而修補程式的目標每個產品都有不同的 ProductCode。</span><span class="sxs-lookup"><span data-stu-id="09ba2-144">A patch can have multiple rows in the same PatchFamily and a different ProductCode for each product targeted by the patch.</span></span> <span data-ttu-id="09ba2-145">PatchFamily 的一個資料列可以針對 ProductCode 指定 Null。</span><span class="sxs-lookup"><span data-stu-id="09ba2-145">One row for the PatchFamily can specify NULL for ProductCode.</span></span> <span data-ttu-id="09ba2-146">如果目標產品符合具有非 Null 的 ProductCode 的資料列，安裝程式會使用相符的資料列，並使用 Null 的 ProductCode 來忽略該資料列。</span><span class="sxs-lookup"><span data-stu-id="09ba2-146">If the target product matches a row with a non-NULL ProductCode, the installer uses the matching row and ignores the row with the NULL ProductCode.</span></span> <span data-ttu-id="09ba2-147">如果指定的產品代碼沒有符合目標，修補程式就會排序，並套用為所有修補目標的 PatchFamily 成員，而不論產品代碼為何。</span><span class="sxs-lookup"><span data-stu-id="09ba2-147">If none of the specified product codes match the target, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

</dd> <dt>

<span data-ttu-id="09ba2-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="09ba2-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="09ba2-149">[順序] 資料行中的值會指定此修補程式在指定 PatchFamily 中的順序。</span><span class="sxs-lookup"><span data-stu-id="09ba2-149">The value in the Sequence column specifies the sequence of this patch within the specified PatchFamily.</span></span> <span data-ttu-id="09ba2-150">順序中的值是以 [版本](version.md) 資料的格式表示。</span><span class="sxs-lookup"><span data-stu-id="09ba2-150">The value in Sequence is expressed in the format of [Version](version.md) data.</span></span> <span data-ttu-id="09ba2-151">值包含1到4個欄位，且每個欄位的範圍為0到65535。</span><span class="sxs-lookup"><span data-stu-id="09ba2-151">The value contains between 1 and 4 fields and each field has a range of 0 to 65535.</span></span> <span data-ttu-id="09ba2-152">PatchFamily 的成員會依順序值的遞增順序排序並套用至目標產品。</span><span class="sxs-lookup"><span data-stu-id="09ba2-152">Members of PatchFamily are sorted and applied to the target product in the order of increasing Sequence values.</span></span> <span data-ttu-id="09ba2-153">例如，下列六個值會增加：1、1.1、1.2、2.01、2.01.1、2.01.1.1。</span><span class="sxs-lookup"><span data-stu-id="09ba2-153">For example, the following six values are increasing: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.</span></span>

</dd> <dt>

<span data-ttu-id="09ba2-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="09ba2-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="09ba2-155">如果資料列中有 **msidbPatchSequenceSupersedeEarlier** 屬性，表示 [小型更新](small-updates.md) 修補程式會取代相同 PatchFamily 中具有較小順序值的所有修補程式所提供的更新。</span><span class="sxs-lookup"><span data-stu-id="09ba2-155">The presence of the **msidbPatchSequenceSupersedeEarlier** attribute in a row indicates that the [small update](small-updates.md) patch supersedes the updates provided by all patches with lesser Sequence values in the same PatchFamily.</span></span> <span data-ttu-id="09ba2-156">此修補套裝程式含在指定的 PatchFamily 中，舊版修補程式所提供的所有修正。</span><span class="sxs-lookup"><span data-stu-id="09ba2-156">This patch contains all fixes provided by earlier patches in the specified PatchFamily.</span></span> <span data-ttu-id="09ba2-157">此屬性並不表示在所有情況下，此修補程式都會取代先前的修補程式，因為較舊的修補程式可以屬於多個修補程式系列。</span><span class="sxs-lookup"><span data-stu-id="09ba2-157">This attribute does not mean that this patch supersedes the earlier patches in all cases because the earlier patches can belong to multiple patch families.</span></span>

<span data-ttu-id="09ba2-158">在任何情況下， [小的更新](small-updates.md) 修補程式無法取代 [次要升級](minor-upgrades.md) 或 [重大升級](major-upgrades.md) 修補程式（即使已設定 **msidbPatchSequenceSupersedeEarlier** ）。</span><span class="sxs-lookup"><span data-stu-id="09ba2-158">A [small update](small-updates.md) patch cannot supersede a [minor upgrade](minor-upgrades.md) or [major upgrade](major-upgrades.md) patch under any circumstances, even if the **msidbPatchSequenceSupersedeEarlier** is set.</span></span> 

| <span data-ttu-id="09ba2-159">Name</span><span class="sxs-lookup"><span data-stu-id="09ba2-159">Name</span></span>                                   | <span data-ttu-id="09ba2-160">值</span><span class="sxs-lookup"><span data-stu-id="09ba2-160">Value</span></span> | <span data-ttu-id="09ba2-161">意義</span><span class="sxs-lookup"><span data-stu-id="09ba2-161">Meaning</span></span>                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | <span data-ttu-id="09ba2-162">0x00</span><span class="sxs-lookup"><span data-stu-id="09ba2-162">0x00</span></span>  | <span data-ttu-id="09ba2-163">指出簡單的排序值。</span><span class="sxs-lookup"><span data-stu-id="09ba2-163">Indicates a simple sequencing value.</span></span>                              |
| <span data-ttu-id="09ba2-164">**msidbPatchSequenceSupersedeEarlier**</span><span class="sxs-lookup"><span data-stu-id="09ba2-164">**msidbPatchSequenceSupersedeEarlier**</span></span> | <span data-ttu-id="09ba2-165">0x01</span><span class="sxs-lookup"><span data-stu-id="09ba2-165">0x01</span></span>  | <span data-ttu-id="09ba2-166">表示取代此系列中較早修補程式的修補程式。</span><span class="sxs-lookup"><span data-stu-id="09ba2-166">Indicates a patch that supersedes earlier patches in this family.</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="09ba2-167">驗證</span><span class="sxs-lookup"><span data-stu-id="09ba2-167">Validation</span></span>

<dl>

[<span data-ttu-id="09ba2-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="09ba2-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="09ba2-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="09ba2-169">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="09ba2-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="09ba2-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09ba2-171">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="09ba2-171">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



