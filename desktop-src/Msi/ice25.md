---
description: ICE25 會驗證 .msi 檔案是否符合其所有的內部合併模組相依性和排除專案。
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850179"
---
# <a name="ice25"></a><span data-ttu-id="7dc03-103">ICE25</span><span class="sxs-lookup"><span data-stu-id="7dc03-103">ICE25</span></span>

<span data-ttu-id="7dc03-104">ICE25 會驗證 .msi 檔案是否符合其所有的內部 [合併模組](merge-modules.md) 相依性和排除專案。</span><span class="sxs-lookup"><span data-stu-id="7dc03-104">ICE25 validates that a .msi file satisfies all of its internal [merge module](merge-modules.md) dependencies and exclusions.</span></span> <span data-ttu-id="7dc03-105">ICE 會驗證下列各項：</span><span class="sxs-lookup"><span data-stu-id="7dc03-105">ICE validates the following:</span></span>

-   <span data-ttu-id="7dc03-106">在 .msi 檔案的 [ModuleDependency 資料表](moduledependency-table.md) 中指出的所有合併模組相依性，都是由 [ModuleSignature 資料表](modulesignature-table.md)中至少列出一個合併模組所滿足。</span><span class="sxs-lookup"><span data-stu-id="7dc03-106">That all merge module dependencies indicated in the .msi file's [ModuleDependency table](moduledependency-table.md) are satisfied by at least one merge module listed in the [ModuleSignature table](modulesignature-table.md).</span></span>
-   <span data-ttu-id="7dc03-107">[ModuleExclusion 資料表](moduleexclusion-table.md)中沒有任何已排除的合併模組與[ModuleSignature 資料表](modulesignature-table.md)中所列的合併模組不相容。</span><span class="sxs-lookup"><span data-stu-id="7dc03-107">That none of the excluded merge modules in the [ModuleExclusion table](moduleexclusion-table.md) are incompatible with the merge modules listed in the [ModuleSignature table](modulesignature-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="7dc03-108">結果</span><span class="sxs-lookup"><span data-stu-id="7dc03-108">Result</span></span>

<span data-ttu-id="7dc03-109">如果 .msi 檔案先前與不相容的合併模組合併，或尚未與必要的合併模組合併，ICE25 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="7dc03-109">ICE25 posts an error message if .msi file has previously been merged with an incompatible merge module or if it has not been merged with a necessary merge module.</span></span>

## <a name="example"></a><span data-ttu-id="7dc03-110">範例</span><span class="sxs-lookup"><span data-stu-id="7dc03-110">Example</span></span>

<span data-ttu-id="7dc03-111">ICE25 會針對所顯示的範例張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="7dc03-111">ICE25 posts the following errors for the example shown.</span></span>

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[<span data-ttu-id="7dc03-112">ModuleSignature 資料表</span><span class="sxs-lookup"><span data-stu-id="7dc03-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="7dc03-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="7dc03-113">ModuleID</span></span> | <span data-ttu-id="7dc03-114">語言</span><span class="sxs-lookup"><span data-stu-id="7dc03-114">Language</span></span> | <span data-ttu-id="7dc03-115">版本</span><span class="sxs-lookup"><span data-stu-id="7dc03-115">Version</span></span> |
|----------|----------|---------|
| <span data-ttu-id="7dc03-116">ModuleA</span><span class="sxs-lookup"><span data-stu-id="7dc03-116">ModuleA</span></span>  | <span data-ttu-id="7dc03-117">0</span><span class="sxs-lookup"><span data-stu-id="7dc03-117">0</span></span>        | <span data-ttu-id="7dc03-118">1.0</span><span class="sxs-lookup"><span data-stu-id="7dc03-118">1.0</span></span>     |
| <span data-ttu-id="7dc03-119">ModuleB</span><span class="sxs-lookup"><span data-stu-id="7dc03-119">ModuleB</span></span>  | <span data-ttu-id="7dc03-120">1033</span><span class="sxs-lookup"><span data-stu-id="7dc03-120">1033</span></span>     | <span data-ttu-id="7dc03-121">1.0</span><span class="sxs-lookup"><span data-stu-id="7dc03-121">1.0</span></span>     |



 

[<span data-ttu-id="7dc03-122">ModuleDependency 資料表</span><span class="sxs-lookup"><span data-stu-id="7dc03-122">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="7dc03-123">ModuleID</span><span class="sxs-lookup"><span data-stu-id="7dc03-123">ModuleID</span></span> | <span data-ttu-id="7dc03-124">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="7dc03-124">ModuleLanguage</span></span> | <span data-ttu-id="7dc03-125">RequiredID</span><span class="sxs-lookup"><span data-stu-id="7dc03-125">RequiredID</span></span> | <span data-ttu-id="7dc03-126">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="7dc03-126">RequiredLanguage</span></span> | <span data-ttu-id="7dc03-127">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="7dc03-127">RequiredVersion</span></span> |
|----------|----------------|------------|------------------|-----------------|
| <span data-ttu-id="7dc03-128">ModuleA</span><span class="sxs-lookup"><span data-stu-id="7dc03-128">ModuleA</span></span>  | <span data-ttu-id="7dc03-129">0</span><span class="sxs-lookup"><span data-stu-id="7dc03-129">0</span></span>              | <span data-ttu-id="7dc03-130">ModuleX</span><span class="sxs-lookup"><span data-stu-id="7dc03-130">ModuleX</span></span>    | <span data-ttu-id="7dc03-131">0</span><span class="sxs-lookup"><span data-stu-id="7dc03-131">0</span></span>                | <span data-ttu-id="7dc03-132">2.0</span><span class="sxs-lookup"><span data-stu-id="7dc03-132">2.0</span></span>             |



 

[<span data-ttu-id="7dc03-133">ModuleExclusion 資料表</span><span class="sxs-lookup"><span data-stu-id="7dc03-133">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="7dc03-134">ModuleID</span><span class="sxs-lookup"><span data-stu-id="7dc03-134">ModuleID</span></span> | <span data-ttu-id="7dc03-135">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="7dc03-135">ModuleLanguage</span></span> | <span data-ttu-id="7dc03-136">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="7dc03-136">ExcludedID</span></span> | <span data-ttu-id="7dc03-137">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="7dc03-137">ExcludedLanguage</span></span> | <span data-ttu-id="7dc03-138">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="7dc03-138">ExcludedMinVersion</span></span> | <span data-ttu-id="7dc03-139">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="7dc03-139">ExcludedMaxVersion</span></span> |
|----------|----------------|------------|------------------|--------------------|--------------------|
| <span data-ttu-id="7dc03-140">ModuleA</span><span class="sxs-lookup"><span data-stu-id="7dc03-140">ModuleA</span></span>  | <span data-ttu-id="7dc03-141">0</span><span class="sxs-lookup"><span data-stu-id="7dc03-141">0</span></span>              | <span data-ttu-id="7dc03-142">ModuleB</span><span class="sxs-lookup"><span data-stu-id="7dc03-142">ModuleB</span></span>    | <span data-ttu-id="7dc03-143">1033</span><span class="sxs-lookup"><span data-stu-id="7dc03-143">1033</span></span>             |                    |                    |



 

## <a name="related-topics"></a><span data-ttu-id="7dc03-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="7dc03-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc03-145">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="7dc03-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



