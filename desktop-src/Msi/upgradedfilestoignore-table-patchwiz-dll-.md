---
description: UpgradedFilesToIgnore 資料表會防止更新相對於目標映射之已升級映射中的特定檔案。
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: 'UpgradedFilesToIgnore 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978383"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a><span data-ttu-id="6283e-103">UpgradedFilesToIgnore 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="6283e-103">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>

<span data-ttu-id="6283e-104">UpgradedFilesToIgnore 資料表會防止更新相對於目標映射之已升級映射中的特定檔案。</span><span class="sxs-lookup"><span data-stu-id="6283e-104">The UpgradedFilesToIgnore table prevents the updating of specific files that are in fact changed in the upgraded image relative to the target images.</span></span> <span data-ttu-id="6283e-105">在某些情況下，這可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="6283e-105">It may be useful to do this in certain cases.</span></span> <span data-ttu-id="6283e-106">例如，僅供非系統管理安裝使用的修補套件，不需要包含只屬於系統管理映射一部分的修補檔案。</span><span class="sxs-lookup"><span data-stu-id="6283e-106">For example, a patch package intended only for use with non-administrative installations does not need to include patching files that are only part of administrative images.</span></span> <span data-ttu-id="6283e-107">排除只用于系統管理映射的這類檔案，可以減少修補套件的大小;不過，系統管理員應該要知道如何分別更新這些檔案。</span><span class="sxs-lookup"><span data-stu-id="6283e-107">Excluding such files used only in administrative images can reduce the size of the patch package; however, administrators should be informed on how to update these files separately.</span></span> <span data-ttu-id="6283e-108">此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="6283e-108">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="6283e-109">UpgradedFilesToIgnore 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="6283e-109">The UpgradedFilesToIgnore table has the following columns.</span></span>



| <span data-ttu-id="6283e-110">Column</span><span class="sxs-lookup"><span data-stu-id="6283e-110">Column</span></span>   | <span data-ttu-id="6283e-111">類型</span><span class="sxs-lookup"><span data-stu-id="6283e-111">Type</span></span> | <span data-ttu-id="6283e-112">答案</span><span class="sxs-lookup"><span data-stu-id="6283e-112">Key</span></span> | <span data-ttu-id="6283e-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="6283e-113">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="6283e-114">已升級</span><span class="sxs-lookup"><span data-stu-id="6283e-114">Upgraded</span></span> | <span data-ttu-id="6283e-115">text</span><span class="sxs-lookup"><span data-stu-id="6283e-115">text</span></span> | <span data-ttu-id="6283e-116">Y</span><span class="sxs-lookup"><span data-stu-id="6283e-116">Y</span></span>   | <span data-ttu-id="6283e-117">N</span><span class="sxs-lookup"><span data-stu-id="6283e-117">N</span></span>        |
| <span data-ttu-id="6283e-118">FTK</span><span class="sxs-lookup"><span data-stu-id="6283e-118">FTK</span></span>      | <span data-ttu-id="6283e-119">text</span><span class="sxs-lookup"><span data-stu-id="6283e-119">text</span></span> | <span data-ttu-id="6283e-120">Y</span><span class="sxs-lookup"><span data-stu-id="6283e-120">Y</span></span>   | <span data-ttu-id="6283e-121">N</span><span class="sxs-lookup"><span data-stu-id="6283e-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6283e-122">資料行</span><span class="sxs-lookup"><span data-stu-id="6283e-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6283e-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>升級</span><span class="sxs-lookup"><span data-stu-id="6283e-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="6283e-124">UpgradedImages 資料表的升級資料行的外鍵 [ (Patchwiz.dll) ](upgradedimages-table-patchwiz-dll-.md)。</span><span class="sxs-lookup"><span data-stu-id="6283e-124">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="6283e-125">當您將目標升級為升級欄位中指定的映射時，patch 建立工具不會更新 UpgradedFilesToIgnore 資料表之 FTK 資料行中所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="6283e-125">The patch creation tool excludes updating the file specified in the FTK column of the UpgradedFilesToIgnore table when upgrading a target to the image specified in the Upgraded field.</span></span> <span data-ttu-id="6283e-126">\*在 [已升級] 欄位中輸入 "" 的值，以排除更新所有已升級映射的檔案。</span><span class="sxs-lookup"><span data-stu-id="6283e-126">Enter a value of "\*" in the Upgraded field to exclude updating the file for all upgraded images.</span></span>

</dd> <dt>

<span data-ttu-id="6283e-127"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="6283e-127"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="6283e-128">已升級之影像的檔案 [資料表](file-table.md) 中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="6283e-128">Foreign key into the [File table](file-table.md) of the upgraded image.</span></span> <span data-ttu-id="6283e-129">格式為 "" 的值 <prefix> \* 會符合檔案資料表中以該前置詞開頭的所有檔案資料表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6283e-129">A value of the form "<prefix>\*" matches all file table keys in the File table that begin with that prefix.</span></span> <span data-ttu-id="6283e-130">星號後面不能有任何文字。</span><span class="sxs-lookup"><span data-stu-id="6283e-130">No text can follow the asterisk.</span></span>

</dd> </dl>

 

 



