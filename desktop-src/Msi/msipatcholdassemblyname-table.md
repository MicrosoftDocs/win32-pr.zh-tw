---
description: MsiPatchOldAssemblyName 資料表會指定元件的舊名稱。
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: MsiPatchOldAssemblyName 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319915"
---
# <a name="msipatcholdassemblyname-table"></a><span data-ttu-id="769e7-103">MsiPatchOldAssemblyName 資料表</span><span class="sxs-lookup"><span data-stu-id="769e7-103">MsiPatchOldAssemblyName Table</span></span>

<span data-ttu-id="769e7-104">MsiPatchOldAssemblyName 資料表會指定元件的舊名稱。</span><span class="sxs-lookup"><span data-stu-id="769e7-104">The MsiPatchOldAssemblyName table specifies the old name for an assembly.</span></span>

<span data-ttu-id="769e7-105">MsiPatchOldAssemblyName 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="769e7-105">The MsiPatchOldAssemblyName table has the following columns.</span></span>



| <span data-ttu-id="769e7-106">Column</span><span class="sxs-lookup"><span data-stu-id="769e7-106">Column</span></span>   | <span data-ttu-id="769e7-107">類型</span><span class="sxs-lookup"><span data-stu-id="769e7-107">Type</span></span>                         | <span data-ttu-id="769e7-108">答案</span><span class="sxs-lookup"><span data-stu-id="769e7-108">Key</span></span> | <span data-ttu-id="769e7-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="769e7-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="769e7-110">組件</span><span class="sxs-lookup"><span data-stu-id="769e7-110">Assembly</span></span> | [<span data-ttu-id="769e7-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="769e7-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="769e7-112">Y</span><span class="sxs-lookup"><span data-stu-id="769e7-112">Y</span></span>   | <span data-ttu-id="769e7-113">N</span><span class="sxs-lookup"><span data-stu-id="769e7-113">N</span></span>        |
| <span data-ttu-id="769e7-114">Name</span><span class="sxs-lookup"><span data-stu-id="769e7-114">Name</span></span>     | [<span data-ttu-id="769e7-115">Text</span><span class="sxs-lookup"><span data-stu-id="769e7-115">Text</span></span>](text.md)             | <span data-ttu-id="769e7-116">Y</span><span class="sxs-lookup"><span data-stu-id="769e7-116">Y</span></span>   | <span data-ttu-id="769e7-117">N</span><span class="sxs-lookup"><span data-stu-id="769e7-117">N</span></span>        |
| <span data-ttu-id="769e7-118">值</span><span class="sxs-lookup"><span data-stu-id="769e7-118">Value</span></span>    | [<span data-ttu-id="769e7-119">Text</span><span class="sxs-lookup"><span data-stu-id="769e7-119">Text</span></span>](text.md)             | <span data-ttu-id="769e7-120">N</span><span class="sxs-lookup"><span data-stu-id="769e7-120">N</span></span>   | <span data-ttu-id="769e7-121">N</span><span class="sxs-lookup"><span data-stu-id="769e7-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="769e7-122">資料行</span><span class="sxs-lookup"><span data-stu-id="769e7-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="769e7-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>裝配</span><span class="sxs-lookup"><span data-stu-id="769e7-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembly</span></span>
</dt> <dd>

<span data-ttu-id="769e7-124">舊元件名稱的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="769e7-124">Unique identifier for the old assembly name.</span></span> <span data-ttu-id="769e7-125">此索引鍵是用來做為此與 [MsiPatchOldAssemblyFile 資料表](msipatcholdassemblyfile-table.md)之間的對應。</span><span class="sxs-lookup"><span data-stu-id="769e7-125">This key is used as a mapping between this and the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="769e7-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="769e7-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="769e7-127">與 [值] 資料行中指定的值相關聯之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="769e7-127">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="769e7-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="769e7-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="769e7-129">與 [名稱] 資料行中指定之名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="769e7-129">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="769e7-130">備註</span><span class="sxs-lookup"><span data-stu-id="769e7-130">Remarks</span></span>

<span data-ttu-id="769e7-131">Windows Installer 在修補安裝至全域組件快取 (GAC) 的元件時，會使用 [MsiPatchOldAssemblyFile 資料表](msipatcholdassemblyfile-table.md) 和 MsiPatchOldAssemblyName 資料表。</span><span class="sxs-lookup"><span data-stu-id="769e7-131">Windows Installer uses the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="769e7-132">發行元件的較新版本時，會變更元件的強式名稱。</span><span class="sxs-lookup"><span data-stu-id="769e7-132">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="769e7-133">這兩個數據表會一起識別已更新元件的舊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="769e7-133">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="769e7-134">這可讓安裝程式使用舊的元件名稱來尋找 GAC 中的原始檔案，並套用二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="769e7-134">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="769e7-135">如果沒有此資訊，安裝程式可能必須存取原始安裝來源，才能修補安裝在 GAC 中的元件。</span><span class="sxs-lookup"><span data-stu-id="769e7-135">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="769e7-136">[PatchWiz](patchwiz-dll.md)不會自動產生[MsiPatchOldAssemblyFile 資料表](msipatcholdassemblyfile-table.md)和 MsiPatchOldAssemblyName 資料表。</span><span class="sxs-lookup"><span data-stu-id="769e7-136">The [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="769e7-137">[UpgradedImages 資料表](upgradedimages-table-patchwiz-dll-.md)中指定的更新封裝必須包含這些資料表，修補程式才能擁有此資訊。</span><span class="sxs-lookup"><span data-stu-id="769e7-137">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="769e7-138">驗證</span><span class="sxs-lookup"><span data-stu-id="769e7-138">Validation</span></span>

<dl>

[<span data-ttu-id="769e7-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="769e7-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="769e7-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="769e7-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="769e7-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="769e7-141">ICE32</span></span>](ice32.md)  
</dl>

 

 



