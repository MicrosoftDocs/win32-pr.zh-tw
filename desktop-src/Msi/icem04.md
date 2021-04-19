---
description: ICEM04 會確認合併模組的必要空白資料表是空的。 若無法修正 ICEM04 報表的錯誤，可能會導致合併模組的合併不正確。
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979746"
---
# <a name="icem04"></a><span data-ttu-id="1409a-104">ICEM04</span><span class="sxs-lookup"><span data-stu-id="1409a-104">ICEM04</span></span>

<span data-ttu-id="1409a-105">ICEM04 會確認合併模組的必要空白資料表是空的。</span><span class="sxs-lookup"><span data-stu-id="1409a-105">ICEM04 verifies that the merge module's required empty tables are empty.</span></span> <span data-ttu-id="1409a-106">若無法修正 ICEM04 報表的錯誤，可能會導致合併模組的合併不正確。</span><span class="sxs-lookup"><span data-stu-id="1409a-106">Failure to fix an error that ICEM04 reports can result in incorrect merging of the merge module.</span></span>

## <a name="result"></a><span data-ttu-id="1409a-107">結果</span><span class="sxs-lookup"><span data-stu-id="1409a-107">Result</span></span>

<span data-ttu-id="1409a-108">當合併模組的必要空白資料表不是空白時，ICEM04 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="1409a-108">ICEM04 posts an error when the merge module's required empty tables are not empty.</span></span>

## <a name="example"></a><span data-ttu-id="1409a-109">範例</span><span class="sxs-lookup"><span data-stu-id="1409a-109">Example</span></span>

<span data-ttu-id="1409a-110">ICEM04 會針對包含所顯示資料庫專案的模組，張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1409a-110">ICEM04 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

<span data-ttu-id="1409a-111">下表顯示部分 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="1409a-111">The following table shows you a partial [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>



| <span data-ttu-id="1409a-112">動作</span><span class="sxs-lookup"><span data-stu-id="1409a-112">Action</span></span>         | <span data-ttu-id="1409a-113">順序</span><span class="sxs-lookup"><span data-stu-id="1409a-113">Sequence</span></span> |
|----------------|----------|
| <span data-ttu-id="1409a-114">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="1409a-114">CostInitialize</span></span> | <span data-ttu-id="1409a-115">1</span><span class="sxs-lookup"><span data-stu-id="1409a-115">1</span></span>        |



 

<span data-ttu-id="1409a-116">下列清單顯示 MergeModule 的部分內容：</span><span class="sxs-lookup"><span data-stu-id="1409a-116">The following list shows you the partial contents of MergeModule:</span></span>

-   <span data-ttu-id="1409a-117">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="1409a-117">ModuleInstallExecuteSequence</span></span>
-   <span data-ttu-id="1409a-118">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="1409a-118">ModuleAdvtExecuteSequence</span></span>
-   <span data-ttu-id="1409a-119">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="1409a-119">InstallUISequence</span></span>

<span data-ttu-id="1409a-120">下列範例會顯示另一個可能的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1409a-120">The following example shows you another possible error.</span></span>

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

<span data-ttu-id="1409a-121">如果合併模組包含模組順序資料表，它必須包含對應的空白順序資料表，無論模組順序資料表是否為空白。</span><span class="sxs-lookup"><span data-stu-id="1409a-121">If a merge module contains a module sequence table, it must contain the corresponding empty sequence table, whether or not the module sequence table is empty.</span></span> <span data-ttu-id="1409a-122">例如，如果 merge 模組包含 [ModuleAdminExecuteSequence 資料表](moduleadminexecutesequence-table.md)，它也必須包含空的 AdminExecuteSequence 資料表。</span><span class="sxs-lookup"><span data-stu-id="1409a-122">For example, if the merge module contains the [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), it must also contain an empty AdminExecuteSequence table.</span></span>

<span data-ttu-id="1409a-123">[FeatureComponents 資料表](featurecomponents-table.md)在所有合併模組中都是必要的，而且必須是空的。</span><span class="sxs-lookup"><span data-stu-id="1409a-123">The [FeatureComponents Table](featurecomponents-table.md) is required in all merge modules and must be empty.</span></span>

<span data-ttu-id="1409a-124">下列程式說明如何修正錯誤。</span><span class="sxs-lookup"><span data-stu-id="1409a-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="1409a-125">**若要修正錯誤**</span><span class="sxs-lookup"><span data-stu-id="1409a-125">**To fix errors**</span></span>

1.  <span data-ttu-id="1409a-126">將空的 [FeatureComponents 資料表](featurecomponents-table.md) 加入至合併模組。</span><span class="sxs-lookup"><span data-stu-id="1409a-126">Add an empty [FeatureComponents Table](featurecomponents-table.md) to the merge module.</span></span>
2.  <span data-ttu-id="1409a-127">將空的 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 加入至合併模組。</span><span class="sxs-lookup"><span data-stu-id="1409a-127">Add an empty [InstallExecuteSequence Table](installexecutesequence-table.md) to the merge module.</span></span>
3.  <span data-ttu-id="1409a-128">從 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中移除 ' CostInitialize ' 動作。</span><span class="sxs-lookup"><span data-stu-id="1409a-128">Remove the 'CostInitialize' action from the [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="1409a-129">在合併模組中，此資料表必須是空的。</span><span class="sxs-lookup"><span data-stu-id="1409a-129">This table must be empty in a merge module.</span></span> <span data-ttu-id="1409a-130">動作只能出現在 ModuleAdvtExecuteSequence 資料表中。</span><span class="sxs-lookup"><span data-stu-id="1409a-130">Actions should only appear in the ModuleAdvtExecuteSequence table.</span></span>

     

## <a name="tables-used-during-execution"></a><span data-ttu-id="1409a-131">執行期間所使用的資料表</span><span class="sxs-lookup"><span data-stu-id="1409a-131">Tables Used During Execution</span></span>

<span data-ttu-id="1409a-132">下列清單會識別執行期間所使用的資料表：</span><span class="sxs-lookup"><span data-stu-id="1409a-132">The following list identifies the tables that are used during execution:</span></span>

-   [<span data-ttu-id="1409a-133">FeatureComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="1409a-133">FeatureComponents Table</span></span>](featurecomponents-table.md)
-   <span data-ttu-id="1409a-134">模組 \* 順序資料表和對應 \* 的順序資料表。</span><span class="sxs-lookup"><span data-stu-id="1409a-134">Module\*Sequence tables and corresponding \*Sequence tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1409a-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="1409a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1409a-136">關於合併模組</span><span class="sxs-lookup"><span data-stu-id="1409a-136">About Merge Modules</span></span>](about-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="1409a-137">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="1409a-137">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



