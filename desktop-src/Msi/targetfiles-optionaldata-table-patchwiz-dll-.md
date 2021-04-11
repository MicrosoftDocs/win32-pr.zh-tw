---
description: TargetFiles \_ OptionalData 資料表包含目標映射中特定檔案的相關資訊。 此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 UiCreatePatchPackageEx 函數使用。
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: 'TargetFiles_OptionalData 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944644"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="841e2-104">TargetFiles \_ OptionalData 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="841e2-104">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="841e2-105">TargetFiles \_ OptionalData 資料表包含目標映射中特定檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="841e2-105">The TargetFiles\_OptionalData table contains information about specific files in a target image.</span></span> <span data-ttu-id="841e2-106">此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="841e2-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="841e2-107">TargetFiles \_ OptionalData 資料表有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="841e2-107">The TargetFiles\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="841e2-108">Column</span><span class="sxs-lookup"><span data-stu-id="841e2-108">Column</span></span>        | <span data-ttu-id="841e2-109">類型</span><span class="sxs-lookup"><span data-stu-id="841e2-109">Type</span></span> | <span data-ttu-id="841e2-110">答案</span><span class="sxs-lookup"><span data-stu-id="841e2-110">Key</span></span> | <span data-ttu-id="841e2-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="841e2-111">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="841e2-112">目標</span><span class="sxs-lookup"><span data-stu-id="841e2-112">Target</span></span>        | <span data-ttu-id="841e2-113">text</span><span class="sxs-lookup"><span data-stu-id="841e2-113">text</span></span> | <span data-ttu-id="841e2-114">Y</span><span class="sxs-lookup"><span data-stu-id="841e2-114">Y</span></span>   | <span data-ttu-id="841e2-115">N</span><span class="sxs-lookup"><span data-stu-id="841e2-115">N</span></span>        |
| <span data-ttu-id="841e2-116">FTK</span><span class="sxs-lookup"><span data-stu-id="841e2-116">FTK</span></span>           | <span data-ttu-id="841e2-117">text</span><span class="sxs-lookup"><span data-stu-id="841e2-117">text</span></span> | <span data-ttu-id="841e2-118">Y</span><span class="sxs-lookup"><span data-stu-id="841e2-118">Y</span></span>   | <span data-ttu-id="841e2-119">N</span><span class="sxs-lookup"><span data-stu-id="841e2-119">N</span></span>        |
| <span data-ttu-id="841e2-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="841e2-120">SymbolPaths</span></span>   | <span data-ttu-id="841e2-121">text</span><span class="sxs-lookup"><span data-stu-id="841e2-121">text</span></span> |     | <span data-ttu-id="841e2-122">Y</span><span class="sxs-lookup"><span data-stu-id="841e2-122">Y</span></span>        |
| <span data-ttu-id="841e2-123">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="841e2-123">IgnoreOffsets</span></span> | <span data-ttu-id="841e2-124">text</span><span class="sxs-lookup"><span data-stu-id="841e2-124">text</span></span> |     | <span data-ttu-id="841e2-125">Y</span><span class="sxs-lookup"><span data-stu-id="841e2-125">Y</span></span>        |
| <span data-ttu-id="841e2-126">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="841e2-126">IgnoreLengths</span></span> | <span data-ttu-id="841e2-127">text</span><span class="sxs-lookup"><span data-stu-id="841e2-127">text</span></span> |     | <span data-ttu-id="841e2-128">Y</span><span class="sxs-lookup"><span data-stu-id="841e2-128">Y</span></span>        |
| <span data-ttu-id="841e2-129">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="841e2-129">RetainOffsets</span></span> | <span data-ttu-id="841e2-130">text</span><span class="sxs-lookup"><span data-stu-id="841e2-130">text</span></span> |     | <span data-ttu-id="841e2-131">Y</span><span class="sxs-lookup"><span data-stu-id="841e2-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="841e2-132">資料行</span><span class="sxs-lookup"><span data-stu-id="841e2-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="841e2-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標</span><span class="sxs-lookup"><span data-stu-id="841e2-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="841e2-134">TargetImages 資料表的目標資料行的外鍵 [ (Patchwiz.dll) ](targetimages-table-patchwiz-dll-.md)。</span><span class="sxs-lookup"><span data-stu-id="841e2-134">Foreign key to the Target column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="841e2-135"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="841e2-135"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="841e2-136">目標影像的檔案 [資料表](file-table.md) 中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="841e2-136">Foreign key into the [File table](file-table.md) of target image.</span></span>

</dd> <dt>

<span data-ttu-id="841e2-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="841e2-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="841e2-138">此欄位中的值會加入至 [TargetImages 資料表 ](targetimages-table-patchwiz-dll-.md) 之 SymbolPaths 資料行中的分號分隔資料夾清單， (Patchwiz.dll 在產生修補程式時) ，而且可以用來新增特定檔案的符號檔。</span><span class="sxs-lookup"><span data-stu-id="841e2-138">The value in this field is added to the semicolon delimited list of folders in the SymbolPaths column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="841e2-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="841e2-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="841e2-140">此欄位中的值是以逗號分隔的範圍位移數位清單，可在目標檔案中忽略範圍。</span><span class="sxs-lookup"><span data-stu-id="841e2-140">The value in this field is a comma delimited list of range offset numbers for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="841e2-141">清單中的範圍順序和數目必須符合 IgnoreLengths 資料行中的專案。</span><span class="sxs-lookup"><span data-stu-id="841e2-141">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="841e2-142">此資料行是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="841e2-142">This column is optional.</span></span>

<span data-ttu-id="841e2-143">這些值可以是十進位或十六進位。</span><span class="sxs-lookup"><span data-stu-id="841e2-143">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="841e2-144">[Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。</span><span class="sxs-lookup"><span data-stu-id="841e2-144">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="841e2-145">這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。</span><span class="sxs-lookup"><span data-stu-id="841e2-145">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="841e2-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="841e2-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="841e2-147">此欄位中的值是以逗號分隔的範圍長度清單（以位元組為單位），可忽略目標檔案中的範圍。</span><span class="sxs-lookup"><span data-stu-id="841e2-147">The value in this field is a comma delimited list of range lengths in bytes for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="841e2-148">清單中的範圍順序和數目必須符合 IgnoreOffsets 資料行中的專案。</span><span class="sxs-lookup"><span data-stu-id="841e2-148">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="841e2-149">此資料行是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="841e2-149">This column is optional.</span></span>

<span data-ttu-id="841e2-150">這些值可以是十進位或十六進位。</span><span class="sxs-lookup"><span data-stu-id="841e2-150">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="841e2-151">[Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。</span><span class="sxs-lookup"><span data-stu-id="841e2-151">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="841e2-152">這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。</span><span class="sxs-lookup"><span data-stu-id="841e2-152">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="841e2-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="841e2-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="841e2-154">此欄位中的值是以逗號分隔的範圍位移編號清單，這些範圍是要在目標檔案中保留的範圍。</span><span class="sxs-lookup"><span data-stu-id="841e2-154">The value in this field is a comma delimited list of range offset numbers for the ranges to be retained in the Target file.</span></span> <span data-ttu-id="841e2-155">清單中的範圍順序和數目必須符合[FamilyFileRanges 資料表 (Patchwiz.dll](familyfileranges-table-patchwiz-dll-.md)中對應記錄的 RetainOffsets 資料行中的專案) </span><span class="sxs-lookup"><span data-stu-id="841e2-155">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span></span>

<span data-ttu-id="841e2-156">這些值可以是十進位或十六進位。</span><span class="sxs-lookup"><span data-stu-id="841e2-156">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="841e2-157">[Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。</span><span class="sxs-lookup"><span data-stu-id="841e2-157">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="841e2-158">這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。</span><span class="sxs-lookup"><span data-stu-id="841e2-158">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="841e2-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="841e2-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="841e2-160">修補選取的檔案區域</span><span class="sxs-lookup"><span data-stu-id="841e2-160">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



