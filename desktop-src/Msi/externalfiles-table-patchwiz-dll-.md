---
description: ExternalFiles 資料表包含不屬於一般目標映射的特定檔案的相關資訊。
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: 'ExternalFiles 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512792"
---
# <a name="externalfiles-table-patchwizdll"></a><span data-ttu-id="1db0e-103">ExternalFiles 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="1db0e-103">ExternalFiles Table (Patchwiz.dll)</span></span>

<span data-ttu-id="1db0e-104">ExternalFiles 資料表包含不屬於一般目標映射的特定檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1db0e-104">The ExternalFiles table contains information about specific files that are not part of a regular target image.</span></span> <span data-ttu-id="1db0e-105">這些檔案可能存在於其他產品、升級或修補程式已更新的產品中。</span><span class="sxs-lookup"><span data-stu-id="1db0e-105">These files may exist in products that have been updated by another product, upgrade, or patch.</span></span> <span data-ttu-id="1db0e-106">此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="1db0e-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="1db0e-107">ExternalFiles 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="1db0e-107">The ExternalFiles table has the following columns.</span></span>



| <span data-ttu-id="1db0e-108">Column</span><span class="sxs-lookup"><span data-stu-id="1db0e-108">Column</span></span>        | <span data-ttu-id="1db0e-109">類型</span><span class="sxs-lookup"><span data-stu-id="1db0e-109">Type</span></span>    | <span data-ttu-id="1db0e-110">答案</span><span class="sxs-lookup"><span data-stu-id="1db0e-110">Key</span></span> | <span data-ttu-id="1db0e-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="1db0e-111">Nullable</span></span> |
|---------------|---------|-----|----------|
| <span data-ttu-id="1db0e-112">系列</span><span class="sxs-lookup"><span data-stu-id="1db0e-112">Family</span></span>        | <span data-ttu-id="1db0e-113">text</span><span class="sxs-lookup"><span data-stu-id="1db0e-113">text</span></span>    | <span data-ttu-id="1db0e-114">Y</span><span class="sxs-lookup"><span data-stu-id="1db0e-114">Y</span></span>   | <span data-ttu-id="1db0e-115">N</span><span class="sxs-lookup"><span data-stu-id="1db0e-115">N</span></span>        |
| <span data-ttu-id="1db0e-116">FTK</span><span class="sxs-lookup"><span data-stu-id="1db0e-116">FTK</span></span>           | <span data-ttu-id="1db0e-117">text</span><span class="sxs-lookup"><span data-stu-id="1db0e-117">text</span></span>    | <span data-ttu-id="1db0e-118">Y</span><span class="sxs-lookup"><span data-stu-id="1db0e-118">Y</span></span>   | <span data-ttu-id="1db0e-119">N</span><span class="sxs-lookup"><span data-stu-id="1db0e-119">N</span></span>        |
| <span data-ttu-id="1db0e-120">FilePath</span><span class="sxs-lookup"><span data-stu-id="1db0e-120">FilePath</span></span>      | <span data-ttu-id="1db0e-121">text</span><span class="sxs-lookup"><span data-stu-id="1db0e-121">text</span></span>    | <span data-ttu-id="1db0e-122">Y</span><span class="sxs-lookup"><span data-stu-id="1db0e-122">Y</span></span>   | <span data-ttu-id="1db0e-123">N</span><span class="sxs-lookup"><span data-stu-id="1db0e-123">N</span></span>        |
| <span data-ttu-id="1db0e-124">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="1db0e-124">SymbolPaths</span></span>   | <span data-ttu-id="1db0e-125">text</span><span class="sxs-lookup"><span data-stu-id="1db0e-125">text</span></span>    |     | <span data-ttu-id="1db0e-126">Y</span><span class="sxs-lookup"><span data-stu-id="1db0e-126">Y</span></span>        |
| <span data-ttu-id="1db0e-127">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="1db0e-127">IgnoreOffsets</span></span> | <span data-ttu-id="1db0e-128">text</span><span class="sxs-lookup"><span data-stu-id="1db0e-128">text</span></span>    |     | <span data-ttu-id="1db0e-129">Y</span><span class="sxs-lookup"><span data-stu-id="1db0e-129">Y</span></span>        |
| <span data-ttu-id="1db0e-130">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="1db0e-130">IgnoreLengths</span></span> | <span data-ttu-id="1db0e-131">text</span><span class="sxs-lookup"><span data-stu-id="1db0e-131">text</span></span>    |     | <span data-ttu-id="1db0e-132">Y</span><span class="sxs-lookup"><span data-stu-id="1db0e-132">Y</span></span>        |
| <span data-ttu-id="1db0e-133">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="1db0e-133">RetainOffsets</span></span> | <span data-ttu-id="1db0e-134">text</span><span class="sxs-lookup"><span data-stu-id="1db0e-134">text</span></span>    |     | <span data-ttu-id="1db0e-135">N</span><span class="sxs-lookup"><span data-stu-id="1db0e-135">N</span></span>        |
| <span data-ttu-id="1db0e-136">單</span><span class="sxs-lookup"><span data-stu-id="1db0e-136">Order</span></span>         | <span data-ttu-id="1db0e-137">整數</span><span class="sxs-lookup"><span data-stu-id="1db0e-137">integer</span></span> |     | <span data-ttu-id="1db0e-138">Y</span><span class="sxs-lookup"><span data-stu-id="1db0e-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1db0e-139">資料行</span><span class="sxs-lookup"><span data-stu-id="1db0e-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1db0e-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>家庭</span><span class="sxs-lookup"><span data-stu-id="1db0e-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="1db0e-141">ImageFamilies 資料表之 [家族] 資料行的外鍵 [ (Patchwiz.dll) ](imagefamilies-table-patchwiz-dll-.md)。</span><span class="sxs-lookup"><span data-stu-id="1db0e-141">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="1db0e-142"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="1db0e-142"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="1db0e-143">已升級映射之 .msi 檔案的檔案 [資料表](file-table.md) 中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="1db0e-143">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="1db0e-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span><span class="sxs-lookup"><span data-stu-id="1db0e-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span></span>
</dt> <dd>

<span data-ttu-id="1db0e-145">外部檔案的完整路徑，包括檔案名。</span><span class="sxs-lookup"><span data-stu-id="1db0e-145">Full path of the external file including the file name.</span></span> <span data-ttu-id="1db0e-146">FilePath 欄位是用來尋找 FTK 資料行中指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="1db0e-146">FilePath field is used to locate the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="1db0e-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="1db0e-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="1db0e-148">搜尋 FTK 資料行中所指定檔案之符號檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="1db0e-148">Full path searched for symbol files of the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="1db0e-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="1db0e-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="1db0e-150">此欄位中的值是以逗號分隔的範圍位移數位清單，可在外部檔案中忽略範圍。</span><span class="sxs-lookup"><span data-stu-id="1db0e-150">The value in this field is a comma-delimited list of range offset numbers for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="1db0e-151">清單中的範圍順序和數目必須符合 IgnoreLengths 資料行中的專案。</span><span class="sxs-lookup"><span data-stu-id="1db0e-151">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="1db0e-152">此資料行是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="1db0e-152">This column is optional.</span></span>

<span data-ttu-id="1db0e-153">這些值可以是十進位或十六進位。</span><span class="sxs-lookup"><span data-stu-id="1db0e-153">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="1db0e-154">[Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。</span><span class="sxs-lookup"><span data-stu-id="1db0e-154">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="1db0e-155">這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。</span><span class="sxs-lookup"><span data-stu-id="1db0e-155">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="1db0e-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="1db0e-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="1db0e-157">此欄位中的值是以逗號分隔的範圍長度清單（以位元組為單位），可忽略外部檔案中的範圍。</span><span class="sxs-lookup"><span data-stu-id="1db0e-157">The value in this field is a comma-delimited list of range lengths in bytes for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="1db0e-158">清單中的範圍順序和數目必須符合 IgnoreOffsets 資料行中的專案。</span><span class="sxs-lookup"><span data-stu-id="1db0e-158">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="1db0e-159">此資料行是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="1db0e-159">This column is optional.</span></span>

<span data-ttu-id="1db0e-160">這些值可以是十進位或十六進位。</span><span class="sxs-lookup"><span data-stu-id="1db0e-160">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="1db0e-161">[Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。</span><span class="sxs-lookup"><span data-stu-id="1db0e-161">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="1db0e-162">這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。</span><span class="sxs-lookup"><span data-stu-id="1db0e-162">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="1db0e-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="1db0e-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="1db0e-164">此欄位中的值是以逗號分隔的範圍位移數位清單，這些範圍是要保留在外部檔案中的範圍。</span><span class="sxs-lookup"><span data-stu-id="1db0e-164">The value in this field is a comma-delimited list of range offset numbers for the ranges to be retained in the External file.</span></span> <span data-ttu-id="1db0e-165">清單中的範圍順序和數目必須符合 FamilyFileRanges 資料表中對應記錄的 RetainOffsets 資料行中的專案 [ (Patchwiz.dll) ](familyfileranges-table-patchwiz-dll-.md)。</span><span class="sxs-lookup"><span data-stu-id="1db0e-165">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span></span>

<span data-ttu-id="1db0e-166">這些值可以是十進位或十六進位。</span><span class="sxs-lookup"><span data-stu-id="1db0e-166">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="1db0e-167">[Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。</span><span class="sxs-lookup"><span data-stu-id="1db0e-167">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="1db0e-168">這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。</span><span class="sxs-lookup"><span data-stu-id="1db0e-168">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="1db0e-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>以</span><span class="sxs-lookup"><span data-stu-id="1db0e-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="1db0e-170">如果為相同的外部檔案指定了兩個以上的版本，資料表可能會包含 FTK 和數列欄位中具有相符值的多個記錄。</span><span class="sxs-lookup"><span data-stu-id="1db0e-170">If two or more versions are specified for the same external file, the table may contain multiple records with matching values in the FTK and Family fields.</span></span> <span data-ttu-id="1db0e-171">在此情況下，Order 欄位可能會指定建立修補程式時要使用的外部檔案順序。</span><span class="sxs-lookup"><span data-stu-id="1db0e-171">In this case, the Order field may specify the order of external files to use when creating the patch.</span></span> <span data-ttu-id="1db0e-172">順序是從最舊到最新版本。</span><span class="sxs-lookup"><span data-stu-id="1db0e-172">The order is from the oldest to the most recent version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1db0e-173">備註</span><span class="sxs-lookup"><span data-stu-id="1db0e-173">Remarks</span></span>

<span data-ttu-id="1db0e-174">此資料表接受環境變數作為從4.0 版 Patchwiz.dll 開始的路徑。</span><span class="sxs-lookup"><span data-stu-id="1db0e-174">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1db0e-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="1db0e-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1db0e-176">修補選取的檔案區域</span><span class="sxs-lookup"><span data-stu-id="1db0e-176">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



