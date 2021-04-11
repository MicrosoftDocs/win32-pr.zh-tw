---
description: FamilyFileRanges 資料表包含已升級映射的特定檔案的相關資訊，而這些檔案的範圍絕對不應該覆寫。
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: 'FamilyFileRanges 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114561"
---
# <a name="familyfileranges-table-patchwizdll"></a><span data-ttu-id="60ac3-103">FamilyFileRanges 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="60ac3-103">FamilyFileRanges Table (Patchwiz.dll)</span></span>

<span data-ttu-id="60ac3-104">FamilyFileRanges 資料表包含已升級映射的特定檔案的相關資訊，而這些檔案的範圍絕對不應該覆寫。</span><span class="sxs-lookup"><span data-stu-id="60ac3-104">The FamilyFileRanges table contains information about particular files of an upgraded image with ranges that should never be overwritten.</span></span> <span data-ttu-id="60ac3-105">此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="60ac3-105">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="60ac3-106">FamilyFileRanges 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="60ac3-106">The FamilyFileRanges table has the following columns.</span></span>



| <span data-ttu-id="60ac3-107">Column</span><span class="sxs-lookup"><span data-stu-id="60ac3-107">Column</span></span>        | <span data-ttu-id="60ac3-108">類型</span><span class="sxs-lookup"><span data-stu-id="60ac3-108">Type</span></span> | <span data-ttu-id="60ac3-109">答案</span><span class="sxs-lookup"><span data-stu-id="60ac3-109">Key</span></span> | <span data-ttu-id="60ac3-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="60ac3-110">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="60ac3-111">系列</span><span class="sxs-lookup"><span data-stu-id="60ac3-111">Family</span></span>        | <span data-ttu-id="60ac3-112">text</span><span class="sxs-lookup"><span data-stu-id="60ac3-112">text</span></span> | <span data-ttu-id="60ac3-113">Y</span><span class="sxs-lookup"><span data-stu-id="60ac3-113">Y</span></span>   | <span data-ttu-id="60ac3-114">N</span><span class="sxs-lookup"><span data-stu-id="60ac3-114">N</span></span>        |
| <span data-ttu-id="60ac3-115">FTK</span><span class="sxs-lookup"><span data-stu-id="60ac3-115">FTK</span></span>           | <span data-ttu-id="60ac3-116">text</span><span class="sxs-lookup"><span data-stu-id="60ac3-116">text</span></span> | <span data-ttu-id="60ac3-117">Y</span><span class="sxs-lookup"><span data-stu-id="60ac3-117">Y</span></span>   | <span data-ttu-id="60ac3-118">N</span><span class="sxs-lookup"><span data-stu-id="60ac3-118">N</span></span>        |
| <span data-ttu-id="60ac3-119">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="60ac3-119">RetainOffsets</span></span> | <span data-ttu-id="60ac3-120">text</span><span class="sxs-lookup"><span data-stu-id="60ac3-120">text</span></span> |     | <span data-ttu-id="60ac3-121">N</span><span class="sxs-lookup"><span data-stu-id="60ac3-121">N</span></span>        |
| <span data-ttu-id="60ac3-122">RetainLengths</span><span class="sxs-lookup"><span data-stu-id="60ac3-122">RetainLengths</span></span> | <span data-ttu-id="60ac3-123">text</span><span class="sxs-lookup"><span data-stu-id="60ac3-123">text</span></span> |     | <span data-ttu-id="60ac3-124">N</span><span class="sxs-lookup"><span data-stu-id="60ac3-124">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="60ac3-125">資料行</span><span class="sxs-lookup"><span data-stu-id="60ac3-125">Columns</span></span>

<dl> <dt>

<span data-ttu-id="60ac3-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>家庭</span><span class="sxs-lookup"><span data-stu-id="60ac3-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="60ac3-127">ImageFamilies 資料表之 [家族] 資料行的外鍵 [ (Patchwiz.dll) ](imagefamilies-table-patchwiz-dll-.md)。</span><span class="sxs-lookup"><span data-stu-id="60ac3-127">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="60ac3-128"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="60ac3-128"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="60ac3-129">在映射系列中所有已升級影像的檔案 [資料表](file-table.md) 中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="60ac3-129">Foreign key into the [File tables](file-table.md) of all the upgraded images in the image family.</span></span>

</dd> <dt>

<span data-ttu-id="60ac3-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="60ac3-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="60ac3-131">無法覆寫之範圍的位移。</span><span class="sxs-lookup"><span data-stu-id="60ac3-131">The offset of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="60ac3-132">此欄位中的值是不會在目標檔案中覆寫之範圍的範圍位移數位清單。</span><span class="sxs-lookup"><span data-stu-id="60ac3-132">The value in this field is a list of the range offset numbers for ranges that are not to be overwritten in the target files.</span></span> <span data-ttu-id="60ac3-133">清單中的範圍順序和數目必須符合 RetainLengths 資料行中的專案。</span><span class="sxs-lookup"><span data-stu-id="60ac3-133">The order and number of the ranges in the list must match the items in the RetainLengths column.</span></span>

<span data-ttu-id="60ac3-134">這些值可以是十進位或十六進位。</span><span class="sxs-lookup"><span data-stu-id="60ac3-134">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="60ac3-135">[Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。</span><span class="sxs-lookup"><span data-stu-id="60ac3-135">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="60ac3-136">這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。</span><span class="sxs-lookup"><span data-stu-id="60ac3-136">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="60ac3-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span><span class="sxs-lookup"><span data-stu-id="60ac3-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span></span>
</dt> <dd>

<span data-ttu-id="60ac3-138">無法覆寫的範圍長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="60ac3-138">The length in bytes of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="60ac3-139">此欄位中的值是要保留于目標檔案之範圍的範圍長度數位清單。</span><span class="sxs-lookup"><span data-stu-id="60ac3-139">The value in this field is a list of range length numbers for ranges to retain in target files.</span></span> <span data-ttu-id="60ac3-140">清單中的範圍順序和數目必須符合 RetainOffsets 資料行中的專案。</span><span class="sxs-lookup"><span data-stu-id="60ac3-140">The order and number of the ranges in the list must match the items in the RetainOffsets column.</span></span>

<span data-ttu-id="60ac3-141">這些值可以是十進位或十六進位。</span><span class="sxs-lookup"><span data-stu-id="60ac3-141">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="60ac3-142">[Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。</span><span class="sxs-lookup"><span data-stu-id="60ac3-142">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="60ac3-143">這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。</span><span class="sxs-lookup"><span data-stu-id="60ac3-143">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60ac3-144">備註</span><span class="sxs-lookup"><span data-stu-id="60ac3-144">Remarks</span></span>

<span data-ttu-id="60ac3-145">RetainOffsets 和 RetainLengths 中輸入的位移和長度不得指定重迭的範圍。</span><span class="sxs-lookup"><span data-stu-id="60ac3-145">The offsets and lengths entered in RetainOffsets and RetainLengths must not specify overlapping ranges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60ac3-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="60ac3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60ac3-147">修補選取的檔案區域</span><span class="sxs-lookup"><span data-stu-id="60ac3-147">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



