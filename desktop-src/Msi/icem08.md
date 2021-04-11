---
description: ICEM08 可確保模組不會排除其相依的另一個模組。
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193687"
---
# <a name="icem08"></a><span data-ttu-id="3eaf9-103">ICEM08</span><span class="sxs-lookup"><span data-stu-id="3eaf9-103">ICEM08</span></span>

<span data-ttu-id="3eaf9-104">ICEM08 可確保模組不會排除其相依的另一個模組。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-104">ICEM08 ensures that a module does not exclude another module that it depends on.</span></span>

## <a name="result"></a><span data-ttu-id="3eaf9-105">結果</span><span class="sxs-lookup"><span data-stu-id="3eaf9-105">Result</span></span>

<span data-ttu-id="3eaf9-106">當模組排除相依的另一個模組時，ICEM08 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-106">ICEM08 posts an error when a module excludes another module that it depends on.</span></span>

## <a name="example"></a><span data-ttu-id="3eaf9-107">範例</span><span class="sxs-lookup"><span data-stu-id="3eaf9-107">Example</span></span>

<span data-ttu-id="3eaf9-108">ICEM08 會針對包含範例中所示資料庫專案的模組，張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-108">ICEM08 posts the following error message for a module containing the database entries shown in the example.</span></span>

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[<span data-ttu-id="3eaf9-109">ModuleDependency 資料表</span><span class="sxs-lookup"><span data-stu-id="3eaf9-109">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="3eaf9-110">ModuleID</span><span class="sxs-lookup"><span data-stu-id="3eaf9-110">ModuleID</span></span>             | <span data-ttu-id="3eaf9-111">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="3eaf9-111">ModuleLanguage</span></span> | <span data-ttu-id="3eaf9-112">RequiredID</span><span class="sxs-lookup"><span data-stu-id="3eaf9-112">RequiredID</span></span>           | <span data-ttu-id="3eaf9-113">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="3eaf9-113">RequiredLanguage</span></span> | <span data-ttu-id="3eaf9-114">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="3eaf9-114">RequiredVersion</span></span> |
|----------------------|----------------|----------------------|------------------|-----------------|
| <span data-ttu-id="3eaf9-115">ModuleA.<GUID></span><span class="sxs-lookup"><span data-stu-id="3eaf9-115">ModuleA.<GUID></span></span> | <span data-ttu-id="3eaf9-116">1033</span><span class="sxs-lookup"><span data-stu-id="3eaf9-116">1033</span></span>           | <span data-ttu-id="3eaf9-117">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="3eaf9-117">ModuleB.<GUID></span></span> | <span data-ttu-id="3eaf9-118">1033</span><span class="sxs-lookup"><span data-stu-id="3eaf9-118">1033</span></span>             | <span data-ttu-id="3eaf9-119">1.0</span><span class="sxs-lookup"><span data-stu-id="3eaf9-119">1.0</span></span>             |



 

[<span data-ttu-id="3eaf9-120">ModuleExclusion 資料表</span><span class="sxs-lookup"><span data-stu-id="3eaf9-120">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="3eaf9-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="3eaf9-121">ModuleID</span></span>             | <span data-ttu-id="3eaf9-122">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="3eaf9-122">ModuleLanguage</span></span> | <span data-ttu-id="3eaf9-123">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="3eaf9-123">ExcludedID</span></span>           | <span data-ttu-id="3eaf9-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="3eaf9-124">ExcludedLanguage</span></span> | <span data-ttu-id="3eaf9-125">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="3eaf9-125">ExcludedMinVersion</span></span> | <span data-ttu-id="3eaf9-126">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="3eaf9-126">ExcludedMaxVersion</span></span> |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| <span data-ttu-id="3eaf9-127">ModuleA.<GUID></span><span class="sxs-lookup"><span data-stu-id="3eaf9-127">ModuleA.<GUID></span></span> | <span data-ttu-id="3eaf9-128">1033</span><span class="sxs-lookup"><span data-stu-id="3eaf9-128">1033</span></span>           | <span data-ttu-id="3eaf9-129">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="3eaf9-129">ModuleB.<GUID></span></span> | <span data-ttu-id="3eaf9-130">1033</span><span class="sxs-lookup"><span data-stu-id="3eaf9-130">1033</span></span>             |                    | <span data-ttu-id="3eaf9-131">1.0</span><span class="sxs-lookup"><span data-stu-id="3eaf9-131">1.0</span></span>                |



 

<span data-ttu-id="3eaf9-132">若要修正錯誤，請移除相依性或排除。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-132">To fix the error, remove either the dependency or the exclusion.</span></span> <span data-ttu-id="3eaf9-133">如果 ModuleB 是 (RequiredID) 的相依性，您就無法將它排除 (如 ModuleExclusion 資料表) 的 ExludedID 資料行所示。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-133">If ModuleB is a dependency (RequiredID) of ModuleA, you cannot exclude it (as shown in the ExludedID column of the ModuleExclusion table).</span></span> <span data-ttu-id="3eaf9-134">如果您必須排除 ModuleB，則必須移除 ModuleA 的相依性。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-134">If you must exclude ModuleB, then you must remove ModuleA's dependency on it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3eaf9-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="3eaf9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eaf9-136">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="3eaf9-136">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



