---
description: TargetImages 資料表包含產品目標影像的相關資訊。 Windows Installer 修補程式套件會將目標映射更新為升級的映射。
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: 'TargetImages 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852335"
---
# <a name="targetimages-table-patchwizdll"></a><span data-ttu-id="29b69-104">TargetImages 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="29b69-104">TargetImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="29b69-105">TargetImages 資料表包含產品目標影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29b69-105">The TargetImages table contains information about the target images of the product.</span></span> <span data-ttu-id="29b69-106">Windows Installer 修補程式套件會將目標映射更新為升級的映射。</span><span class="sxs-lookup"><span data-stu-id="29b69-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span>

<span data-ttu-id="29b69-107">在每個修補程式建立資料庫中都必須包含至少一筆記錄的 TargetImages 資料表， ( pcp 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="29b69-107">A TargetImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="29b69-108">此資料表是由 [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 函數所使用。</span><span class="sxs-lookup"><span data-stu-id="29b69-108">This table is used by the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="29b69-109">TargetImages 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="29b69-109">The TargetImages table has the following columns.</span></span>



| <span data-ttu-id="29b69-110">Column</span><span class="sxs-lookup"><span data-stu-id="29b69-110">Column</span></span>                | <span data-ttu-id="29b69-111">類型</span><span class="sxs-lookup"><span data-stu-id="29b69-111">Type</span></span>    | <span data-ttu-id="29b69-112">答案</span><span class="sxs-lookup"><span data-stu-id="29b69-112">Key</span></span> | <span data-ttu-id="29b69-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="29b69-113">Nullable</span></span> |
|-----------------------|---------|-----|----------|
| <span data-ttu-id="29b69-114">目標</span><span class="sxs-lookup"><span data-stu-id="29b69-114">Target</span></span>                | <span data-ttu-id="29b69-115">text</span><span class="sxs-lookup"><span data-stu-id="29b69-115">text</span></span>    | <span data-ttu-id="29b69-116">Y</span><span class="sxs-lookup"><span data-stu-id="29b69-116">Y</span></span>   | <span data-ttu-id="29b69-117">N</span><span class="sxs-lookup"><span data-stu-id="29b69-117">N</span></span>        |
| <span data-ttu-id="29b69-118">MsiPath</span><span class="sxs-lookup"><span data-stu-id="29b69-118">MsiPath</span></span>               | <span data-ttu-id="29b69-119">text</span><span class="sxs-lookup"><span data-stu-id="29b69-119">text</span></span>    |     | <span data-ttu-id="29b69-120">N</span><span class="sxs-lookup"><span data-stu-id="29b69-120">N</span></span>        |
| <span data-ttu-id="29b69-121">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="29b69-121">SymbolPaths</span></span>           | <span data-ttu-id="29b69-122">text</span><span class="sxs-lookup"><span data-stu-id="29b69-122">text</span></span>    |     | <span data-ttu-id="29b69-123">Y</span><span class="sxs-lookup"><span data-stu-id="29b69-123">Y</span></span>        |
| <span data-ttu-id="29b69-124">已升級</span><span class="sxs-lookup"><span data-stu-id="29b69-124">Upgraded</span></span>              | <span data-ttu-id="29b69-125">text</span><span class="sxs-lookup"><span data-stu-id="29b69-125">text</span></span>    |     | <span data-ttu-id="29b69-126">N</span><span class="sxs-lookup"><span data-stu-id="29b69-126">N</span></span>        |
| <span data-ttu-id="29b69-127">單</span><span class="sxs-lookup"><span data-stu-id="29b69-127">Order</span></span>                 | <span data-ttu-id="29b69-128">整數</span><span class="sxs-lookup"><span data-stu-id="29b69-128">integer</span></span> |     | <span data-ttu-id="29b69-129">N</span><span class="sxs-lookup"><span data-stu-id="29b69-129">N</span></span>        |
| <span data-ttu-id="29b69-130">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="29b69-130">ProductValidateFlags</span></span>  | <span data-ttu-id="29b69-131">text</span><span class="sxs-lookup"><span data-stu-id="29b69-131">text</span></span>    |     | <span data-ttu-id="29b69-132">Y</span><span class="sxs-lookup"><span data-stu-id="29b69-132">Y</span></span>        |
| <span data-ttu-id="29b69-133">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="29b69-133">IgnoreMissingSrcFiles</span></span> | <span data-ttu-id="29b69-134">整數</span><span class="sxs-lookup"><span data-stu-id="29b69-134">integer</span></span> |     | <span data-ttu-id="29b69-135">N</span><span class="sxs-lookup"><span data-stu-id="29b69-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="29b69-136">資料行</span><span class="sxs-lookup"><span data-stu-id="29b69-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="29b69-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標</span><span class="sxs-lookup"><span data-stu-id="29b69-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="29b69-138">目標映射的識別碼。</span><span class="sxs-lookup"><span data-stu-id="29b69-138">Identifier for a target image.</span></span> <span data-ttu-id="29b69-139">修補程式套件會將此資料行中指定的目標映射更新為升級的資料行中所指定的升級映射。</span><span class="sxs-lookup"><span data-stu-id="29b69-139">The patch package updates the target image specified in this column to the upgraded image specified in the Upgraded column.</span></span> <span data-ttu-id="29b69-140">每個升級的映射都有一個或多個目標映射。</span><span class="sxs-lookup"><span data-stu-id="29b69-140">There are one or more target images for each upgraded image.</span></span> <span data-ttu-id="29b69-141">目標映射必須是產品的完全未壓縮安裝映射，例如 CD-ROM 上的系統管理映射或未壓縮的安裝映射。</span><span class="sxs-lookup"><span data-stu-id="29b69-141">The target image must be a fully uncompressed setup image of the product, such as an administrative image or an uncompressed setup image on a CD-ROM.</span></span> <span data-ttu-id="29b69-142">請注意， [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數不會為封包中的檔案產生二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="29b69-142">Note that the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function does not generate binary patches for files in cabinets.</span></span> <span data-ttu-id="29b69-143">此欄位中的值會與 [已升級] 欄位中的值搭配使用，以產生安裝程式新增至 patch 封裝的轉換名稱。</span><span class="sxs-lookup"><span data-stu-id="29b69-143">The value in this field is used with the value in the Upgraded field to generate the names of the transforms that the installer adds to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="29b69-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span><span class="sxs-lookup"><span data-stu-id="29b69-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="29b69-145">此欄位會指定目標映射之 .msi 檔案位置的完整路徑，包括檔案名。</span><span class="sxs-lookup"><span data-stu-id="29b69-145">This field specifies the full path, including the file name, to the location of the .msi file for the target image.</span></span> <span data-ttu-id="29b69-146">這是目標映射的來源檔案位置。</span><span class="sxs-lookup"><span data-stu-id="29b69-146">This is the location of the source files for the target image.</span></span>

</dd> <dt>

<span data-ttu-id="29b69-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="29b69-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="29b69-148">以分號分隔的資料夾清單，這些資料夾是要搜尋的符號檔，可用於優化二進位修補程式的產生。</span><span class="sxs-lookup"><span data-stu-id="29b69-148">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="29b69-149">請注意，不會搜尋此欄位中指定的資料夾子目錄。</span><span class="sxs-lookup"><span data-stu-id="29b69-149">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="29b69-150">優化的二進位修補程式可能較小。</span><span class="sxs-lookup"><span data-stu-id="29b69-150">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="29b69-151">Microsoft Visual C++ 必須安裝在產生修補程式的電腦上，並用來建立符號檔。</span><span class="sxs-lookup"><span data-stu-id="29b69-151">Microsoft Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="29b69-152">這個欄位是選擇性欄位，即使未指定符號檔或符號檔無法 Patchwiz.dll，安裝程式還是會建立二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="29b69-152">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="29b69-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>升級</span><span class="sxs-lookup"><span data-stu-id="29b69-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="29b69-154">[UpgradedImages 資料表](upgradedimages-table-patchwiz-dll-.md)的升級資料行外鍵。</span><span class="sxs-lookup"><span data-stu-id="29b69-154">Foreign key to the Upgraded column of the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="29b69-155">[UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)函式會忽略至少一個 TargetImages 資料表記錄未參考的已升級影像。</span><span class="sxs-lookup"><span data-stu-id="29b69-155">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function ignores any upgraded image that is not referenced by at least one record of the TargetImages table.</span></span>

</dd> <dt>

<span data-ttu-id="29b69-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>以</span><span class="sxs-lookup"><span data-stu-id="29b69-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="29b69-157">目標影像的相對順序。</span><span class="sxs-lookup"><span data-stu-id="29b69-157">Relative order of the target image.</span></span> <span data-ttu-id="29b69-158">因為多個目標可以修補為升級的映射，所以 [順序] 欄位提供在 [修補程式轉換] 清單中排序轉換的方法。</span><span class="sxs-lookup"><span data-stu-id="29b69-158">Because multiple targets can be patched to an upgraded image, the Order field provides a means to sequence the transforms in the patch transforms list.</span></span> <span data-ttu-id="29b69-159">通常，順序是從最舊到最新的影像。</span><span class="sxs-lookup"><span data-stu-id="29b69-159">Commonly, the order is from oldest to newest image.</span></span>

</dd> <dt>

<span data-ttu-id="29b69-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="29b69-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span></span>
</dt> <dd>

<span data-ttu-id="29b69-161">ProductValidateFlags 欄位是用來指定產品檢查，以避免套用不相關的轉換。</span><span class="sxs-lookup"><span data-stu-id="29b69-161">The ProductValidateFlags field is used to specify product checking to avoid applying irrelevant transforms.</span></span> <span data-ttu-id="29b69-162">在此欄位中輸入的值必須是8位數的十六進位整數，以及 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)函數之 *iValidation* 參數的其中一個有效值。</span><span class="sxs-lookup"><span data-stu-id="29b69-162">The value entered in this field must be an 8-digit hex integer and one of the valid values for the *iValidation* parameter of the [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) function.</span></span> <span data-ttu-id="29b69-163">預設值為0x00000922，等於 **MSITRANSFORM \_ validate \_ UPDATEVERSION**  +  **MSITRANSFORM \_ validate \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ validate \_ UPGRADECODE**  +  **MSITRANSFORM \_ validate \_ PRODUCT**。</span><span class="sxs-lookup"><span data-stu-id="29b69-163">The default value is 0x00000922 which equals **MSITRANSFORM\_VALIDATE\_UPDATEVERSION** + **MSITRANSFORM\_VALIDATE\_NEWEQUALBASEVERSION** + **MSITRANSFORM\_VALIDATE\_UPGRADECODE** + **MSITRANSFORM\_VALIDATE\_PRODUCT**.</span></span>

</dd> <dt>

<span data-ttu-id="29b69-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="29b69-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span></span>
</dt> <dd>

<span data-ttu-id="29b69-165">如果此欄位設定為非零值，則安裝程式會忽略目標映射中遺失的檔案，並在修補期間保持不變。</span><span class="sxs-lookup"><span data-stu-id="29b69-165">If this field is set to a nonzero value, files missing from the target image are ignored by the installer and left unchanged during patching.</span></span> <span data-ttu-id="29b69-166">這可讓您在不需要整個映射的情況下進行修補;只有已變更的產品和 .msi 檔案的檔案是必要的。</span><span class="sxs-lookup"><span data-stu-id="29b69-166">This enables patches to be made without requiring the entire image; only the changed files of the product and the .msi file are required.</span></span> <span data-ttu-id="29b69-167">這可能會減少產生修補程式所需的時間。</span><span class="sxs-lookup"><span data-stu-id="29b69-167">This may reduce the time required to generate the patch.</span></span>

> [!Note]  
> <span data-ttu-id="29b69-168">請勿在 [Properties 資料表](properties-table-patchwiz-dll-.md)中使用 IgnoreMissingSrcFiles 值，並將 TrustMsi 設定為1。</span><span class="sxs-lookup"><span data-stu-id="29b69-168">Do not use the IgnoreMissingSrcFiles value with TrustMsi set to 1 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29b69-169">備註</span><span class="sxs-lookup"><span data-stu-id="29b69-169">Remarks</span></span>

<span data-ttu-id="29b69-170">此資料表接受環境變數作為從4.0 版 Patchwiz.dll 開始的路徑。</span><span class="sxs-lookup"><span data-stu-id="29b69-170">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 



