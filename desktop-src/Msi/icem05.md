---
description: ICEM05 會驗證合併模組是否已正確與模組中的元件相關聯。 元件與模組的關聯不正確，導致元件與目標資料庫的關聯不正確。
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026636"
---
# <a name="icem05"></a><span data-ttu-id="cf653-104">ICEM05</span><span class="sxs-lookup"><span data-stu-id="cf653-104">ICEM05</span></span>

<span data-ttu-id="cf653-105">ICEM05 會驗證合併模組是否已正確與模組中的元件相關聯。</span><span class="sxs-lookup"><span data-stu-id="cf653-105">ICEM05 verifies that the merge module is correctly associated with components in the module.</span></span> <span data-ttu-id="cf653-106">元件與模組的關聯不正確，導致元件與目標資料庫的關聯不正確。</span><span class="sxs-lookup"><span data-stu-id="cf653-106">Incorrectly associating a component with a module causes the component to be incorrectly associated with the target database.</span></span>

<span data-ttu-id="cf653-107">Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。</span><span class="sxs-lookup"><span data-stu-id="cf653-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="cf653-108">結果</span><span class="sxs-lookup"><span data-stu-id="cf653-108">Result</span></span>

<span data-ttu-id="cf653-109">如果模組資料庫不正確地關聯元件和模組，ICEM05 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="cf653-109">ICEM05 posts an error if the module database incorrectly associates components and the module.</span></span>

## <a name="example"></a><span data-ttu-id="cf653-110">範例</span><span class="sxs-lookup"><span data-stu-id="cf653-110">Example</span></span>

<span data-ttu-id="cf653-111">ICEM05 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="cf653-111">ICEM05 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[<span data-ttu-id="cf653-112">ModuleSignature 資料表</span><span class="sxs-lookup"><span data-stu-id="cf653-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="cf653-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="cf653-113">ModuleID</span></span>         | <span data-ttu-id="cf653-114">語言</span><span class="sxs-lookup"><span data-stu-id="cf653-114">Language</span></span> | <span data-ttu-id="cf653-115">版本</span><span class="sxs-lookup"><span data-stu-id="cf653-115">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="cf653-116">MyModule.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="cf653-116">MyModule.*GUID1*</span></span> | <span data-ttu-id="cf653-117">1033</span><span class="sxs-lookup"><span data-stu-id="cf653-117">1033</span></span>     | <span data-ttu-id="cf653-118">1.0</span><span class="sxs-lookup"><span data-stu-id="cf653-118">1.0</span></span>     |



 

[<span data-ttu-id="cf653-119">**ModuleComponents 資料表**</span><span class="sxs-lookup"><span data-stu-id="cf653-119">**ModuleComponents Table**</span></span>](modulecomponents-table.md)



| <span data-ttu-id="cf653-120">元件</span><span class="sxs-lookup"><span data-stu-id="cf653-120">Component</span></span>  | <span data-ttu-id="cf653-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="cf653-121">ModuleID</span></span>            | <span data-ttu-id="cf653-122">語言</span><span class="sxs-lookup"><span data-stu-id="cf653-122">Language</span></span> |
|------------|---------------------|----------|
| <span data-ttu-id="cf653-123">Component1</span><span class="sxs-lookup"><span data-stu-id="cf653-123">Component1</span></span> | <span data-ttu-id="cf653-124">MyModule.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="cf653-124">MyModule.*GUID1*</span></span>    | <span data-ttu-id="cf653-125">1033</span><span class="sxs-lookup"><span data-stu-id="cf653-125">1033</span></span>     |
| <span data-ttu-id="cf653-126">Component2</span><span class="sxs-lookup"><span data-stu-id="cf653-126">Component2</span></span> | <span data-ttu-id="cf653-127">OtherModule.*GUID2*</span><span class="sxs-lookup"><span data-stu-id="cf653-127">OtherModule.*GUID2*</span></span> | <span data-ttu-id="cf653-128">1033</span><span class="sxs-lookup"><span data-stu-id="cf653-128">1033</span></span>     |



 

<span data-ttu-id="cf653-129">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="cf653-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="cf653-130">元件</span><span class="sxs-lookup"><span data-stu-id="cf653-130">Component</span></span>  | <span data-ttu-id="cf653-131">ComponentID</span><span class="sxs-lookup"><span data-stu-id="cf653-131">ComponentID</span></span> |
|------------|-------------|
| <span data-ttu-id="cf653-132">Component3</span><span class="sxs-lookup"><span data-stu-id="cf653-132">Component3</span></span> | <span data-ttu-id="cf653-133">*GUID4*</span><span class="sxs-lookup"><span data-stu-id="cf653-133">*GUID4*</span></span>     |
| <span data-ttu-id="cf653-134">Component2</span><span class="sxs-lookup"><span data-stu-id="cf653-134">Component2</span></span> | <span data-ttu-id="cf653-135">*GUID5*</span><span class="sxs-lookup"><span data-stu-id="cf653-135">*GUID5*</span></span>     |



 

<span data-ttu-id="cf653-136">Merge module ICE 會報告第一個錯誤，因為 ModuleComponents 資料表會嘗試將元件與另一個不是 ModuleSignature 資料表中指定之模組的模組產生關聯。</span><span class="sxs-lookup"><span data-stu-id="cf653-136">The merge module ICE reports the first error because the ModuleComponents table attempts to associate a component with another module that is not the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="cf653-137">若要修正此問題，請將 Component2 的 ModuleComponents 記錄的 ModuleID 和 Language 資料行變更為目前模組 MyModule 的。*GUID1*。</span><span class="sxs-lookup"><span data-stu-id="cf653-137">To fix this, change the ModuleID and Language columns of the ModuleComponents record for Component2 to that for the current module, MyModule.*GUID1*.</span></span>

<span data-ttu-id="cf653-138">Merge module ICE 會報告第二個錯誤，因為 ModuleComponents 資料表中的第一筆記錄嘗試將 Component1 與模組產生關聯。</span><span class="sxs-lookup"><span data-stu-id="cf653-138">The merge module ICE reports the second error because the first record in the ModuleComponents table attempts to associate Component1 with the module.</span></span> <span data-ttu-id="cf653-139">此元件不存在於合併模組的元件資料表中。</span><span class="sxs-lookup"><span data-stu-id="cf653-139">This component does not exist in the Component Table of the merge module.</span></span> <span data-ttu-id="cf653-140">模組只能與存在於模組中的元件相關聯。</span><span class="sxs-lookup"><span data-stu-id="cf653-140">A module can only be associated with a component that exists in the module.</span></span> <span data-ttu-id="cf653-141">若要修正此問題，請移除不存在元件的記錄。</span><span class="sxs-lookup"><span data-stu-id="cf653-141">To fix this, remove the record for the non-existent component.</span></span>

<span data-ttu-id="cf653-142">Merge module ICE 會回報第三個錯誤，因為此模組會嘗試將 Component3 新增至目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf653-142">The merge module ICE reports the third error because the module attempts to add Component3 to the target database.</span></span> <span data-ttu-id="cf653-143">這個元件尚未與 ModuleComponents 資料表中的模組相關聯。</span><span class="sxs-lookup"><span data-stu-id="cf653-143">This component has not been associated with the module in the ModuleComponents table.</span></span> <span data-ttu-id="cf653-144">若要修正這個錯誤，請將 Component3 的記錄新增至 ModuleComponents 資料表。</span><span class="sxs-lookup"><span data-stu-id="cf653-144">To fix this error, add a record for Component3 to the ModuleComponents table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf653-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf653-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf653-146">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="cf653-146">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



