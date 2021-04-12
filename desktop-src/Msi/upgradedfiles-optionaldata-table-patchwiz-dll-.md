---
description: UpgradedFile \_ OptionalData 資料表包含有關已升級映射中特定檔案的資訊。 此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 UiCreatePatchPackageEx 函數使用。
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: 'UpgradedFiles_OptionalData 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194946"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="e6bc2-104">UpgradedFiles \_ OptionalData 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="e6bc2-104">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="e6bc2-105">UpgradedFile \_ OptionalData 資料表包含有關已升級映射中特定檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-105">The UpgradedFile\_OptionalData table contains information about specific files in an upgraded image.</span></span> <span data-ttu-id="e6bc2-106">此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="e6bc2-107">UpgradedFile \_ OptionalData 資料表有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-107">The UpgradedFile\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="e6bc2-108">Column</span><span class="sxs-lookup"><span data-stu-id="e6bc2-108">Column</span></span>                  | <span data-ttu-id="e6bc2-109">類型</span><span class="sxs-lookup"><span data-stu-id="e6bc2-109">Type</span></span>    | <span data-ttu-id="e6bc2-110">答案</span><span class="sxs-lookup"><span data-stu-id="e6bc2-110">Key</span></span> | <span data-ttu-id="e6bc2-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="e6bc2-111">Nullable</span></span> |
|-------------------------|---------|-----|----------|
| <span data-ttu-id="e6bc2-112">已升級</span><span class="sxs-lookup"><span data-stu-id="e6bc2-112">Upgraded</span></span>                | <span data-ttu-id="e6bc2-113">text</span><span class="sxs-lookup"><span data-stu-id="e6bc2-113">text</span></span>    | <span data-ttu-id="e6bc2-114">Y</span><span class="sxs-lookup"><span data-stu-id="e6bc2-114">Y</span></span>   | <span data-ttu-id="e6bc2-115">N</span><span class="sxs-lookup"><span data-stu-id="e6bc2-115">N</span></span>        |
| <span data-ttu-id="e6bc2-116">FTK</span><span class="sxs-lookup"><span data-stu-id="e6bc2-116">FTK</span></span>                     | <span data-ttu-id="e6bc2-117">text</span><span class="sxs-lookup"><span data-stu-id="e6bc2-117">text</span></span>    | <span data-ttu-id="e6bc2-118">Y</span><span class="sxs-lookup"><span data-stu-id="e6bc2-118">Y</span></span>   | <span data-ttu-id="e6bc2-119">N</span><span class="sxs-lookup"><span data-stu-id="e6bc2-119">N</span></span>        |
| <span data-ttu-id="e6bc2-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="e6bc2-120">SymbolPaths</span></span>             | <span data-ttu-id="e6bc2-121">text</span><span class="sxs-lookup"><span data-stu-id="e6bc2-121">text</span></span>    |     | <span data-ttu-id="e6bc2-122">Y</span><span class="sxs-lookup"><span data-stu-id="e6bc2-122">Y</span></span>        |
| <span data-ttu-id="e6bc2-123">AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="e6bc2-123">AllowIgnoreOnPatchError</span></span> | <span data-ttu-id="e6bc2-124">整數</span><span class="sxs-lookup"><span data-stu-id="e6bc2-124">integer</span></span> |     | <span data-ttu-id="e6bc2-125">Y</span><span class="sxs-lookup"><span data-stu-id="e6bc2-125">Y</span></span>        |
| <span data-ttu-id="e6bc2-126">IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="e6bc2-126">IncludeWholeFile</span></span>        | <span data-ttu-id="e6bc2-127">整數</span><span class="sxs-lookup"><span data-stu-id="e6bc2-127">integer</span></span> |     | <span data-ttu-id="e6bc2-128">Y</span><span class="sxs-lookup"><span data-stu-id="e6bc2-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e6bc2-129">資料行</span><span class="sxs-lookup"><span data-stu-id="e6bc2-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e6bc2-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>升級</span><span class="sxs-lookup"><span data-stu-id="e6bc2-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="e6bc2-131">UpgradedImages 資料表的升級資料行的外鍵 [ (Patchwiz.dll) ](upgradedimages-table-patchwiz-dll-.md)。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-131">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6bc2-132"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="e6bc2-132"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="e6bc2-133">檔案資料表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-133">File table key.</span></span> <span data-ttu-id="e6bc2-134">已升級映射之 .msi 檔案的檔案 [資料表](file-table.md) 中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-134">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span> <span data-ttu-id="e6bc2-135">如果系列內的兩個或多個升級的映射具有相同的 FTK 值，則值必須參考相同的檔案。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-135">If two or more upgraded images within a family have the same FTK value, the value must refer to the same file.</span></span> <span data-ttu-id="e6bc2-136">多個升級映射所共用的檔案應該具有相同的 FTK，以將封包檔大小降到最低。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-136">Files shared by multiple upgrade images should have the same FTK to minimize cabinet file size.</span></span>

</dd> <dt>

<span data-ttu-id="e6bc2-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="e6bc2-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="e6bc2-138">此欄位中的值會加入至 [UpgradedImages 資料表 ](upgradedimages-table-patchwiz-dll-.md) 的 SymbolPaths 資料行中，以分號分隔的資料夾清單， (Patchwiz.dll 在產生修補程式時) ，而且可以用來新增特定檔案的符號檔。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-138">The value in this field is added to the semicolon-delimited list of folders in the SymbolPaths column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="e6bc2-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="e6bc2-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span></span>
</dt> <dd>

<span data-ttu-id="e6bc2-140">設定為1，表示修補程式為不重要。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-140">Set to 1 to indicate that the patch is non-vital.</span></span> <span data-ttu-id="e6bc2-141">設定為0表示修補程式很重要。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-141">Set to 0 to indicate that the patch is vital.</span></span> <span data-ttu-id="e6bc2-142">如果 Windows Installer 在將此修補程式套用至 [FTK] 資料行中指定的檔案時發生問題，則此欄位中的值會決定錯誤訊息框是否包含 [ **略** 過] 按鈕，讓使用者能夠繼續進行修補程式。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-142">If Windows Installer encounters a problem when applying this patch to the file specified in the FTK column, the value in this field determines whether the error message box includes an **Ignore** button to enable the user to continue the patching process.</span></span>

</dd> <dt>

<span data-ttu-id="e6bc2-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="e6bc2-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span></span>
</dt> <dd>

<span data-ttu-id="e6bc2-144">如果應該安裝 FTK 資料行中指定的整個檔案，而不是建立二進位修補程式，請將設定為非零值。</span><span class="sxs-lookup"><span data-stu-id="e6bc2-144">Set to a nonzero value if the entire file specified in the FTK column should be installed rather than creating a binary patch.</span></span>

</dd> </dl>

 

 



