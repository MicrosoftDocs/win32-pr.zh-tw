---
description: ICEM02 會確認所有模組相依性和排除專案都與目前的模組相關。
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191698"
---
# <a name="icem02"></a><span data-ttu-id="4567a-103">ICEM02</span><span class="sxs-lookup"><span data-stu-id="4567a-103">ICEM02</span></span>

<span data-ttu-id="4567a-104">ICEM02 會確認所有模組相依性和排除專案都與目前的模組相關。</span><span class="sxs-lookup"><span data-stu-id="4567a-104">ICEM02 verifies that all the module dependencies and exclusions are related to the current module.</span></span>

<span data-ttu-id="4567a-105">Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。</span><span class="sxs-lookup"><span data-stu-id="4567a-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="4567a-106">結果</span><span class="sxs-lookup"><span data-stu-id="4567a-106">Result</span></span>

<span data-ttu-id="4567a-107">如果模組資料庫嘗試指定與目前模組無關的相依性或排除專案，ICEM02 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4567a-107">ICEM02 posts error messages if the module database attempts to specify dependencies or exclusions that do not relate to the current module.</span></span> <span data-ttu-id="4567a-108">如果模組資料庫嘗試將目前的模組指定為相依或本身排除，ICEM02 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4567a-108">ICEM02 posts an error message if the module database attempts to specify the current module as dependent or as excluded by itself.</span></span>

## <a name="example"></a><span data-ttu-id="4567a-109">範例</span><span class="sxs-lookup"><span data-stu-id="4567a-109">Example</span></span>

<span data-ttu-id="4567a-110">ICEM02 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4567a-110">ICEM02 would post the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[<span data-ttu-id="4567a-111">ModuleSignature 資料表</span><span class="sxs-lookup"><span data-stu-id="4567a-111">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="4567a-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="4567a-112">ModuleID</span></span>         | <span data-ttu-id="4567a-113">語言</span><span class="sxs-lookup"><span data-stu-id="4567a-113">Language</span></span> | <span data-ttu-id="4567a-114">版本</span><span class="sxs-lookup"><span data-stu-id="4567a-114">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="4567a-115">MyModule.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4567a-115">MyModule.*GUID1*</span></span> | <span data-ttu-id="4567a-116">1033</span><span class="sxs-lookup"><span data-stu-id="4567a-116">1033</span></span>     | <span data-ttu-id="4567a-117">1.0</span><span class="sxs-lookup"><span data-stu-id="4567a-117">1.0</span></span>     |



 

[<span data-ttu-id="4567a-118">ModuleDependency 資料表</span><span class="sxs-lookup"><span data-stu-id="4567a-118">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="4567a-119">ModuleID</span><span class="sxs-lookup"><span data-stu-id="4567a-119">ModuleID</span></span>            | <span data-ttu-id="4567a-120">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="4567a-120">ModuleLanguage</span></span> | <span data-ttu-id="4567a-121">RequiredID</span><span class="sxs-lookup"><span data-stu-id="4567a-121">RequiredID</span></span>          | <span data-ttu-id="4567a-122">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="4567a-122">RequiredLanguage</span></span> | <span data-ttu-id="4567a-123">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="4567a-123">RequiredVersion</span></span> |
|---------------------|----------------|---------------------|------------------|-----------------|
| <span data-ttu-id="4567a-124">OtherModule.*GUID2*</span><span class="sxs-lookup"><span data-stu-id="4567a-124">OtherModule.*GUID2*</span></span> | <span data-ttu-id="4567a-125">1033</span><span class="sxs-lookup"><span data-stu-id="4567a-125">1033</span></span>           | <span data-ttu-id="4567a-126">OtherModule.*GUID3*</span><span class="sxs-lookup"><span data-stu-id="4567a-126">OtherModule.*GUID3*</span></span> | <span data-ttu-id="4567a-127">0</span><span class="sxs-lookup"><span data-stu-id="4567a-127">0</span></span>                | <span data-ttu-id="4567a-128">1.0</span><span class="sxs-lookup"><span data-stu-id="4567a-128">1.0</span></span>             |
| <span data-ttu-id="4567a-129">MyModule.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4567a-129">MyModule.*GUID1*</span></span>    | <span data-ttu-id="4567a-130">1033</span><span class="sxs-lookup"><span data-stu-id="4567a-130">1033</span></span>           | <span data-ttu-id="4567a-131">MyModule.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4567a-131">MyModule.*GUID1*</span></span>    | <span data-ttu-id="4567a-132">1033</span><span class="sxs-lookup"><span data-stu-id="4567a-132">1033</span></span>             | <span data-ttu-id="4567a-133">1.2</span><span class="sxs-lookup"><span data-stu-id="4567a-133">1.2</span></span>             |



 

<span data-ttu-id="4567a-134">[ModuleExclusion 資料表](moduleexclusion-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="4567a-134">[ModuleExclusion Table](moduleexclusion-table.md) (partial)</span></span>



| <span data-ttu-id="4567a-135">ModuleID</span><span class="sxs-lookup"><span data-stu-id="4567a-135">ModuleID</span></span>            | <span data-ttu-id="4567a-136">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="4567a-136">ModuleLanguage</span></span> | <span data-ttu-id="4567a-137">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="4567a-137">ExcludedID</span></span>          | <span data-ttu-id="4567a-138">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="4567a-138">ExcludedLanguage</span></span> |
|---------------------|----------------|---------------------|------------------|
| <span data-ttu-id="4567a-139">OtherModule.*GUID2*</span><span class="sxs-lookup"><span data-stu-id="4567a-139">OtherModule.*GUID2*</span></span> | <span data-ttu-id="4567a-140">1033</span><span class="sxs-lookup"><span data-stu-id="4567a-140">1033</span></span>           | <span data-ttu-id="4567a-141">OtherModule.*GUID3*</span><span class="sxs-lookup"><span data-stu-id="4567a-141">OtherModule.*GUID3*</span></span> | <span data-ttu-id="4567a-142">0</span><span class="sxs-lookup"><span data-stu-id="4567a-142">0</span></span>                |
| <span data-ttu-id="4567a-143">MyModule.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4567a-143">MyModule.*GUID1*</span></span>    | <span data-ttu-id="4567a-144">1033</span><span class="sxs-lookup"><span data-stu-id="4567a-144">1033</span></span>           | <span data-ttu-id="4567a-145">MyModule.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4567a-145">MyModule.*GUID1*</span></span>    | <span data-ttu-id="4567a-146">1033</span><span class="sxs-lookup"><span data-stu-id="4567a-146">1033</span></span>             |



 

<span data-ttu-id="4567a-147">Merge module ICE 會張貼第一個錯誤，因為 ModuleDependency 資料表中第一個資料列的是，它並未針對 ModuleSignature 資料表中指定的目前模組指定必要的相依性。</span><span class="sxs-lookup"><span data-stu-id="4567a-147">The merge module ICE posts the first error because the of the first row in the ModuleDependency table, which does not specify a required dependency for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="4567a-148">模組的相依性只能在它自己的 ModuleDependency 資料表中指定。</span><span class="sxs-lookup"><span data-stu-id="4567a-148">The dependencies of a module can only be specified in its own ModuleDependency table.</span></span> <span data-ttu-id="4567a-149">如果為 OtherModule，則為。目前的模組需要 *GUID3* ，請使用 ModuleSignature 資料表中的資料來取代資料列的前兩個數據行。</span><span class="sxs-lookup"><span data-stu-id="4567a-149">If OtherModule.*GUID3* is required by the current module, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="4567a-150">如果為 OtherModule，則為。此模組不需要 *GUID3* ，請刪除此資料列。</span><span class="sxs-lookup"><span data-stu-id="4567a-150">If OtherModule.*GUID3* is not required by this module, delete this row.</span></span>

<span data-ttu-id="4567a-151">合併模組 ICE 會張貼第二個錯誤，因為模組無法自行指定相依性。</span><span class="sxs-lookup"><span data-stu-id="4567a-151">The merge module ICE posts the second error because a module cannot specify a dependency upon itself.</span></span>

<span data-ttu-id="4567a-152">Merge module ICE 會張貼第三個錯誤，因為 ModuleExclusion 資料表中的第一個資料列不會針對 ModuleSignature 資料表中指定的目前模組指定必要的排除。</span><span class="sxs-lookup"><span data-stu-id="4567a-152">The merge module ICE posts the third error because of the first row in the ModuleExclusion table, which does not specify a required exclusion for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="4567a-153">模組的排除專案只能在它自己的 ModuleExclusion 資料表中指定。</span><span class="sxs-lookup"><span data-stu-id="4567a-153">The exclusions of a module can only be specified in its own ModuleExclusion table.</span></span> <span data-ttu-id="4567a-154">如果目前的模組排除 OtherModule。*GUID3*，將資料列的前兩個數據行取代為 ModuleSignature 資料表中的資料。</span><span class="sxs-lookup"><span data-stu-id="4567a-154">If the current module excludes OtherModule.*GUID3*, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="4567a-155">如果目前的模組未排除 OtherModule。*GUID3*，請刪除此資料列。</span><span class="sxs-lookup"><span data-stu-id="4567a-155">If the current module does not exclude OtherModule.*GUID3*, delete this row.</span></span>

<span data-ttu-id="4567a-156">合併模組 ICE 會張貼第四個錯誤，因為模組無法指定它本身排除。</span><span class="sxs-lookup"><span data-stu-id="4567a-156">The merge module ICE posts the fourth error because a module cannot specify that it exclude itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4567a-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="4567a-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4567a-158">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="4567a-158">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



