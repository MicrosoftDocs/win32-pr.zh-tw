---
description: MsiPatchOldAssemblyFile 資料表會將 File 資料表中的檔案與 MsiPatchOldAssemblyName 資料表中的元件名稱產生關聯。 多個舊的元件名稱可以與單一檔案相關聯。
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: MsiPatchOldAssemblyFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992100"
---
# <a name="msipatcholdassemblyfile-table"></a><span data-ttu-id="03cdc-104">MsiPatchOldAssemblyFile 資料表</span><span class="sxs-lookup"><span data-stu-id="03cdc-104">MsiPatchOldAssemblyFile Table</span></span>

<span data-ttu-id="03cdc-105">MsiPatchOldAssemblyFile 資料表會將 [file 資料表](file-table.md) 中的檔案與 [MsiPatchOldAssemblyName 資料表](msipatcholdassemblyname-table.md)中的元件名稱產生關聯。</span><span class="sxs-lookup"><span data-stu-id="03cdc-105">The MsiPatchOldAssemblyFile table relates a file in the [File table](file-table.md) to an assembly name in the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md).</span></span> <span data-ttu-id="03cdc-106">多個舊的元件名稱可以與單一檔案相關聯。</span><span class="sxs-lookup"><span data-stu-id="03cdc-106">Multiple old assembly names can be associated with a single file.</span></span>

<span data-ttu-id="03cdc-107">MsiPatchOldAssemblyFile 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="03cdc-107">The MsiPatchOldAssemblyFile table has the following columns.</span></span>



| <span data-ttu-id="03cdc-108">Column</span><span class="sxs-lookup"><span data-stu-id="03cdc-108">Column</span></span>     | <span data-ttu-id="03cdc-109">類型</span><span class="sxs-lookup"><span data-stu-id="03cdc-109">Type</span></span>                         | <span data-ttu-id="03cdc-110">答案</span><span class="sxs-lookup"><span data-stu-id="03cdc-110">Key</span></span> | <span data-ttu-id="03cdc-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="03cdc-111">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="03cdc-112">檔案\_</span><span class="sxs-lookup"><span data-stu-id="03cdc-112">File\_</span></span>     | [<span data-ttu-id="03cdc-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="03cdc-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="03cdc-114">Y</span><span class="sxs-lookup"><span data-stu-id="03cdc-114">Y</span></span>   | <span data-ttu-id="03cdc-115">N</span><span class="sxs-lookup"><span data-stu-id="03cdc-115">N</span></span>        |
| <span data-ttu-id="03cdc-116">組件\_</span><span class="sxs-lookup"><span data-stu-id="03cdc-116">Assembly\_</span></span> | [<span data-ttu-id="03cdc-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="03cdc-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="03cdc-118">Y</span><span class="sxs-lookup"><span data-stu-id="03cdc-118">Y</span></span>   | <span data-ttu-id="03cdc-119">N</span><span class="sxs-lookup"><span data-stu-id="03cdc-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="03cdc-120">資料行</span><span class="sxs-lookup"><span data-stu-id="03cdc-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="03cdc-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="03cdc-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="03cdc-122">檔案 [資料表](file-table.md) 的外鍵，可指定要修補的元件。</span><span class="sxs-lookup"><span data-stu-id="03cdc-122">Foreign key to the [File table](file-table.md) that specifies the assembly to be patched.</span></span> <span data-ttu-id="03cdc-123">此資料行是主鍵的一部分。</span><span class="sxs-lookup"><span data-stu-id="03cdc-123">This column is part of the primary key.</span></span>

</dd> <dt>

<span data-ttu-id="03cdc-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>裝配\_</span><span class="sxs-lookup"><span data-stu-id="03cdc-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembly\_</span></span>
</dt> <dd>

<span data-ttu-id="03cdc-125">[MsiPatchOldAssemblyName 資料表](msipatcholdassemblyname-table.md)的外鍵，可識別元件的其中一個舊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="03cdc-125">Foreign key to the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) that identifies one of the old assembly names for the assembly.</span></span> <span data-ttu-id="03cdc-126">此資料行是主鍵的一部分。</span><span class="sxs-lookup"><span data-stu-id="03cdc-126">This column is part of the primary key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03cdc-127">備註</span><span class="sxs-lookup"><span data-stu-id="03cdc-127">Remarks</span></span>

<span data-ttu-id="03cdc-128">Windows Installer 在修補安裝至全域組件快取 (GAC) 的元件時，會使用 MsiPatchOldAssemblyFile 資料表和 [MsiPatchOldAssemblyName 資料表](msipatcholdassemblyname-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="03cdc-128">Windows Installer uses the MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="03cdc-129">發行元件的較新版本時，會變更元件的強式名稱。</span><span class="sxs-lookup"><span data-stu-id="03cdc-129">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="03cdc-130">這兩個數據表會一起識別已更新元件的舊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="03cdc-130">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="03cdc-131">這可讓安裝程式使用舊的元件名稱來尋找 GAC 中的原始檔案，並套用二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="03cdc-131">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="03cdc-132">如果沒有此資訊，安裝程式可能必須存取原始安裝來源，才能修補安裝在 GAC 中的元件。</span><span class="sxs-lookup"><span data-stu-id="03cdc-132">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="03cdc-133">[PatchWiz](patchwiz-dll.md)不會自動產生 MsiPatchOldAssemblyFile 資料表和[MsiPatchOldAssemblyName 資料表](msipatcholdassemblyname-table.md)。</span><span class="sxs-lookup"><span data-stu-id="03cdc-133">The MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="03cdc-134">[UpgradedImages 資料表](upgradedimages-table-patchwiz-dll-.md)中指定的更新封裝必須包含這些資料表，修補程式才能擁有此資訊。</span><span class="sxs-lookup"><span data-stu-id="03cdc-134">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="03cdc-135">驗證</span><span class="sxs-lookup"><span data-stu-id="03cdc-135">Validation</span></span>

<dl>

[<span data-ttu-id="03cdc-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="03cdc-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="03cdc-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="03cdc-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="03cdc-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="03cdc-138">ICE32</span></span>](ice32.md)  
</dl>

 

 



