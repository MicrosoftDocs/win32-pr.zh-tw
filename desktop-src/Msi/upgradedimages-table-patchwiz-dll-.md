---
description: UpgradedImages 資料表包含產品升級後影像的相關資訊。
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: 'UpgradedImages 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320559"
---
# <a name="upgradedimages-table-patchwizdll"></a><span data-ttu-id="0dcad-103">UpgradedImages 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="0dcad-103">UpgradedImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="0dcad-104">UpgradedImages 資料表包含產品升級後影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0dcad-104">The UpgradedImages table contains information about the upgraded images of the product.</span></span> <span data-ttu-id="0dcad-105">升級的映射應該是產品最新版本的完全未壓縮安裝映射，例如，系統管理映射或 CD-ROM 的未壓縮安裝映射。</span><span class="sxs-lookup"><span data-stu-id="0dcad-105">The upgraded image should be a fully uncompressed setup image of the latest version of the product, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="0dcad-106">Windows Installer 修補程式套件會將目標映射更新為升級的映射。</span><span class="sxs-lookup"><span data-stu-id="0dcad-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span> <span data-ttu-id="0dcad-107">UpgradedImages 資料表在 patch 建立資料庫中是必要的， (. pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)使用。</span><span class="sxs-lookup"><span data-stu-id="0dcad-107">The UpgradedImages table is required in the patch creation database (.pcp file) and is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="0dcad-108">在每個修補程式建立資料庫中都必須包含至少一筆記錄的 UpgradedImages 資料表， ( pcp 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="0dcad-108">An UpgradedImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="0dcad-109">此資料表是由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)所使用。</span><span class="sxs-lookup"><span data-stu-id="0dcad-109">This table is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="0dcad-110">UpgradedImages 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="0dcad-110">The UpgradedImages table has the following columns.</span></span>



| <span data-ttu-id="0dcad-111">Column</span><span class="sxs-lookup"><span data-stu-id="0dcad-111">Column</span></span>       | <span data-ttu-id="0dcad-112">類型</span><span class="sxs-lookup"><span data-stu-id="0dcad-112">Type</span></span> | <span data-ttu-id="0dcad-113">答案</span><span class="sxs-lookup"><span data-stu-id="0dcad-113">Key</span></span> | <span data-ttu-id="0dcad-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="0dcad-114">Nullable</span></span> |
|--------------|------|-----|----------|
| <span data-ttu-id="0dcad-115">已升級</span><span class="sxs-lookup"><span data-stu-id="0dcad-115">Upgraded</span></span>     | <span data-ttu-id="0dcad-116">text</span><span class="sxs-lookup"><span data-stu-id="0dcad-116">text</span></span> | <span data-ttu-id="0dcad-117">Y</span><span class="sxs-lookup"><span data-stu-id="0dcad-117">Y</span></span>   | <span data-ttu-id="0dcad-118">N</span><span class="sxs-lookup"><span data-stu-id="0dcad-118">N</span></span>        |
| <span data-ttu-id="0dcad-119">MsiPath</span><span class="sxs-lookup"><span data-stu-id="0dcad-119">MsiPath</span></span>      | <span data-ttu-id="0dcad-120">text</span><span class="sxs-lookup"><span data-stu-id="0dcad-120">text</span></span> |     | <span data-ttu-id="0dcad-121">N</span><span class="sxs-lookup"><span data-stu-id="0dcad-121">N</span></span>        |
| <span data-ttu-id="0dcad-122">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="0dcad-122">PatchMsiPath</span></span> | <span data-ttu-id="0dcad-123">text</span><span class="sxs-lookup"><span data-stu-id="0dcad-123">text</span></span> |     | <span data-ttu-id="0dcad-124">Y</span><span class="sxs-lookup"><span data-stu-id="0dcad-124">Y</span></span>        |
| <span data-ttu-id="0dcad-125">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="0dcad-125">SymbolPaths</span></span>  | <span data-ttu-id="0dcad-126">text</span><span class="sxs-lookup"><span data-stu-id="0dcad-126">text</span></span> |     | <span data-ttu-id="0dcad-127">Y</span><span class="sxs-lookup"><span data-stu-id="0dcad-127">Y</span></span>        |
| <span data-ttu-id="0dcad-128">系列</span><span class="sxs-lookup"><span data-stu-id="0dcad-128">Family</span></span>       | <span data-ttu-id="0dcad-129">text</span><span class="sxs-lookup"><span data-stu-id="0dcad-129">text</span></span> |     | <span data-ttu-id="0dcad-130">N</span><span class="sxs-lookup"><span data-stu-id="0dcad-130">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0dcad-131">資料行</span><span class="sxs-lookup"><span data-stu-id="0dcad-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0dcad-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>升級</span><span class="sxs-lookup"><span data-stu-id="0dcad-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="0dcad-133">升級的欄位是任意的識別碼，可將目標映射連接到產品的升級映射。</span><span class="sxs-lookup"><span data-stu-id="0dcad-133">The Upgraded field is an arbitrary identifier to connect the target images with an upgraded image of the product.</span></span>

</dd> <dt>

<span data-ttu-id="0dcad-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span><span class="sxs-lookup"><span data-stu-id="0dcad-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="0dcad-135">此欄位會指定檔案的完整路徑（包括檔案名）至已升級之映射的 .msi 檔案位置。</span><span class="sxs-lookup"><span data-stu-id="0dcad-135">This field specifies the full path, including the file name, to the location of the .msi file for the upgraded image.</span></span> <span data-ttu-id="0dcad-136">這是已升級映射之來源檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="0dcad-136">This is the location of the source files for the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="0dcad-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="0dcad-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span></span>
</dt> <dd>

<span data-ttu-id="0dcad-138">選擇性的 patchMsiPath 會指向已升級安裝資料庫的已修改複本，其中包含修補程式安裝程式的其他專屬撰寫。</span><span class="sxs-lookup"><span data-stu-id="0dcad-138">The optional patchMsiPath points to a modified copy of the upgraded installation database that contains additional authoring specific to the patch installation process.</span></span> <span data-ttu-id="0dcad-139">例如，在 [**PATCH**](patch.md) 屬性上有條件的其他對話或自訂動作。</span><span class="sxs-lookup"><span data-stu-id="0dcad-139">For example, additional dialogs or custom actions conditioned on the [**PATCH**](patch.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="0dcad-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="0dcad-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="0dcad-141">以分號分隔的資料夾清單，這些資料夾是要搜尋的符號檔，可用於優化二進位修補程式的產生。</span><span class="sxs-lookup"><span data-stu-id="0dcad-141">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="0dcad-142">請注意，不會搜尋此欄位中指定的資料夾子目錄。</span><span class="sxs-lookup"><span data-stu-id="0dcad-142">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="0dcad-143">優化的二進位修補程式可能較小。</span><span class="sxs-lookup"><span data-stu-id="0dcad-143">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="0dcad-144">Visual C++ 必須安裝在產生修補程式的電腦上，並用來建立符號檔。</span><span class="sxs-lookup"><span data-stu-id="0dcad-144">Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="0dcad-145">這個欄位是選擇性欄位，即使未指定符號檔或符號檔無法 Patchwiz.dll，安裝程式還是會建立二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="0dcad-145">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="0dcad-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>家庭</span><span class="sxs-lookup"><span data-stu-id="0dcad-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="0dcad-147">[ImageFamilies 資料表](imagefamilies-table-patchwiz-dll-.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="0dcad-147">Foreign key into the [ImageFamilies table](imagefamilies-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="0dcad-148">每個升級的映射都只能屬於一個系列。</span><span class="sxs-lookup"><span data-stu-id="0dcad-148">Each upgraded image must belong to only one family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0dcad-149">備註</span><span class="sxs-lookup"><span data-stu-id="0dcad-149">Remarks</span></span>

<span data-ttu-id="0dcad-150">雖然每個升級的映射都可以分組為不同的映射系列，但是將共用檔案的已升級影像群組在一起，可能會使 .msp 變得較小。</span><span class="sxs-lookup"><span data-stu-id="0dcad-150">Although each upgraded image can be grouped into a separate image family, grouping upgraded images that share files together may make the .msp smaller.</span></span>

<span data-ttu-id="0dcad-151">此資料表接受環境變數作為從4.0 版 Patchwiz.dll 開始的路徑。</span><span class="sxs-lookup"><span data-stu-id="0dcad-151">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 



