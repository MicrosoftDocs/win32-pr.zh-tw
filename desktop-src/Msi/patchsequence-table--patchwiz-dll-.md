---
description: PatchSequence 資料表是用來產生修補程式中的 MsiPatchSequence 資料表。 資料表需要 Windows Installer&160; 3.0 提供的 PATCHWIZ.DLL 版本 \# 。
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: 'PatchSequence 資料表 (PATCHWIZ.DLL) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852731"
---
# <a name="patchsequence-table-patchwizdll"></a><span data-ttu-id="5d3ec-104">PatchSequence 資料表 (PATCHWIZ.DLL) </span><span class="sxs-lookup"><span data-stu-id="5d3ec-104">PatchSequence Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="5d3ec-105">PatchSequence 資料表是用來產生修補程式中的 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-105">The PatchSequence Table is used to generate the [MsiPatchSequence Table](msipatchsequence-table.md) in a patch.</span></span> <span data-ttu-id="5d3ec-106">資料表需要 Windows Installer 3.0 提供的 [PATCHWIZ.DLL](patchwiz-dll.md) 版本。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-106">The table requires the version of [PATCHWIZ.DLL](patchwiz-dll.md) that is available with Windows Installer 3.0.</span></span>

<span data-ttu-id="5d3ec-107">下表識別 PatchSequence 資料表的資料行。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-107">The following table identifies the columns of the PatchSequence Table.</span></span>



| <span data-ttu-id="5d3ec-108">Column</span><span class="sxs-lookup"><span data-stu-id="5d3ec-108">Column</span></span>      | <span data-ttu-id="5d3ec-109">類型</span><span class="sxs-lookup"><span data-stu-id="5d3ec-109">Type</span></span>       | <span data-ttu-id="5d3ec-110">答案</span><span class="sxs-lookup"><span data-stu-id="5d3ec-110">Key</span></span> | <span data-ttu-id="5d3ec-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="5d3ec-111">Nullable</span></span> |
|-------------|------------|-----|----------|
| <span data-ttu-id="5d3ec-112">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="5d3ec-112">PatchFamily</span></span> | <span data-ttu-id="5d3ec-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="5d3ec-113">Identifier</span></span> | <span data-ttu-id="5d3ec-114">Y</span><span class="sxs-lookup"><span data-stu-id="5d3ec-114">Y</span></span>   | <span data-ttu-id="5d3ec-115">N</span><span class="sxs-lookup"><span data-stu-id="5d3ec-115">N</span></span>        |
| <span data-ttu-id="5d3ec-116">目標</span><span class="sxs-lookup"><span data-stu-id="5d3ec-116">Target</span></span>      | <span data-ttu-id="5d3ec-117">Text</span><span class="sxs-lookup"><span data-stu-id="5d3ec-117">Text</span></span>       | <span data-ttu-id="5d3ec-118">Y</span><span class="sxs-lookup"><span data-stu-id="5d3ec-118">Y</span></span>   | <span data-ttu-id="5d3ec-119">Y</span><span class="sxs-lookup"><span data-stu-id="5d3ec-119">Y</span></span>        |
| <span data-ttu-id="5d3ec-120">順序</span><span class="sxs-lookup"><span data-stu-id="5d3ec-120">Sequence</span></span>    | <span data-ttu-id="5d3ec-121">版本</span><span class="sxs-lookup"><span data-stu-id="5d3ec-121">Version</span></span>    |     | <span data-ttu-id="5d3ec-122">Y</span><span class="sxs-lookup"><span data-stu-id="5d3ec-122">Y</span></span>        |
| <span data-ttu-id="5d3ec-123">取代</span><span class="sxs-lookup"><span data-stu-id="5d3ec-123">Supersede</span></span>   | <span data-ttu-id="5d3ec-124">整數</span><span class="sxs-lookup"><span data-stu-id="5d3ec-124">Integer</span></span>    |     | <span data-ttu-id="5d3ec-125">Y</span><span class="sxs-lookup"><span data-stu-id="5d3ec-125">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="5d3ec-126">資料行</span><span class="sxs-lookup"><span data-stu-id="5d3ec-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5d3ec-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="5d3ec-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="5d3ec-128">指出此修補程式所屬序列系列的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-128">The identifier that indicates the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="5d3ec-129">[目標] 和 [PatchFamily] 資料行中的值會一起定義資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-129">The values in the Target and PatchFamily columns together define the primary key for the table.</span></span> <span data-ttu-id="5d3ec-130">屬於多個時序系列，或有不同順序（視目標的產品代碼而定）的修補程式可以針對每個配對各有一個資料列。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-130">A patch that belongs to multiple sequence families, or has different sequences depending on the product code of the target, can have one row for each pairing.</span></span> <span data-ttu-id="5d3ec-131">這個值是用來填入屬於修補程式之 [MsiPatchSequence 資料表](msipatchsequence-table.md) 的 PatchFamily 資料行。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-131">This value is used to populate the PatchFamily column of the [MsiPatchSequence Table](msipatchsequence-table.md) that belongs to the patch.</span></span>

</dd> <dt>

<span data-ttu-id="5d3ec-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標</span><span class="sxs-lookup"><span data-stu-id="5d3ec-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="5d3ec-133">目標資料行是用來依產品代碼篩選 PatchFamily。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-133">The Target column is used to filter the PatchFamily by product code.</span></span>

<span data-ttu-id="5d3ec-134">此資料行中的 Null 值表示此 PatchFamily 適用于修補程式的所有目標。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-134">A NULL value in this column indicates that this PatchFamily applies to all targets of the patch.</span></span> <span data-ttu-id="5d3ec-135">如果此資料行包含 [TargetImages 資料表](targetimages-table-patchwiz-dll-.md)的外鍵，則會抓取指定之影像的產品代碼，並在 [MsiPatchSequence 資料表](msipatchsequence-table.md)的新修補程式資料列中，用來填入產品代碼值。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-135">If this column contains a foreign key to the [TargetImages Table](targetimages-table-patchwiz-dll-.md), the product code of the specified image is retrieved and used to populate the product code value in the new patch's row of the [MsiPatchSequence Table](msipatchsequence-table.md).</span></span> <span data-ttu-id="5d3ec-136">如果此資料行包含 GUID，則會使用 GUID 來填入 MsiPatchSequence 資料表中資料列的產品代碼值。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-136">If this column contains a GUID, the GUID is used to populate the product code value of the row in the MsiPatchSequence Table.</span></span>

</dd> <dt>

<span data-ttu-id="5d3ec-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="5d3ec-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="5d3ec-138">[順序] 資料行中的值會用來填入新修補檔案之 [MsiPatchSequence 資料表](msipatchsequence-table.md) 的 [順序] 資料行。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-138">The value in the Sequence column is used to populate the Sequence column of the [MsiPatchSequence Table](msipatchsequence-table.md) of the new patch file.</span></span>

<span data-ttu-id="5d3ec-139">如果值為 Null，則會自動產生序號。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-139">If the value is NULL, a sequence number is generated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="5d3ec-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>取代</span><span class="sxs-lookup"><span data-stu-id="5d3ec-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Supersede</span></span>
</dt> <dd>

<span data-ttu-id="5d3ec-141">此欄位中的 **msidbPatchSequenceSupersedeEarlier** 或1值表示此修補程式會取代此修補程式所屬序列系列中較早的 [小型更新](small-updates.md) 。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-141">A value of **msidbPatchSequenceSupersedeEarlier** or 1 in this field indicates that this patch supersedes earlier [small updates](small-updates.md) in the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="5d3ec-142">此資料行中的值是用來設定 [MsiPatchSequence 資料表](msipatchsequence-table.md) 中新修補程式資料列的 [屬性] 資料行。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-142">The value in this column is used to set the Attributes column of the new patch's row in the [MsiPatchSequence Table](msipatchsequence-table.md) .</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="5d3ec-143">備註</span><span class="sxs-lookup"><span data-stu-id="5d3ec-143">Remarks</span></span>

<span data-ttu-id="5d3ec-144">從 Windows Installer 3.0 開始提供。</span><span class="sxs-lookup"><span data-stu-id="5d3ec-144">Available beginning in Windows Installer 3.0.</span></span>

 

 



