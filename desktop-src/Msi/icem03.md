---
description: ICEM03 會確認模組中的所有動作都是基本動作，或衍生自有效的基底動作。
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980320"
---
# <a name="icem03"></a><span data-ttu-id="b5eb6-103">ICEM03</span><span class="sxs-lookup"><span data-stu-id="b5eb6-103">ICEM03</span></span>

<span data-ttu-id="b5eb6-104">ICEM03 會確認模組中的所有動作都是基本動作，或衍生自有效的基底動作。</span><span class="sxs-lookup"><span data-stu-id="b5eb6-104">ICEM03 verifies that all actions in the module are either base actions or derive from a valid base action.</span></span>

<span data-ttu-id="b5eb6-105">Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b5eb6-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="b5eb6-106">結果</span><span class="sxs-lookup"><span data-stu-id="b5eb6-106">Result</span></span>

<span data-ttu-id="b5eb6-107">ICEM03 會張貼模組的錯誤訊息，其中包含不是基底動作或衍生自有效基底動作之順序資料表中的動作。</span><span class="sxs-lookup"><span data-stu-id="b5eb6-107">ICEM03 posts the error messages for a module containing actions in a sequence table that is not a base action or derived from a valid base action.</span></span>

## <a name="example"></a><span data-ttu-id="b5eb6-108">範例</span><span class="sxs-lookup"><span data-stu-id="b5eb6-108">Example</span></span>

<span data-ttu-id="b5eb6-109">ICEM03 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b5eb6-109">ICEM03 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[<span data-ttu-id="b5eb6-110">ModuleInstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="b5eb6-110">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="b5eb6-111">動作</span><span class="sxs-lookup"><span data-stu-id="b5eb6-111">Action</span></span>  | <span data-ttu-id="b5eb6-112">順序</span><span class="sxs-lookup"><span data-stu-id="b5eb6-112">Sequence</span></span> | <span data-ttu-id="b5eb6-113">BaseAction</span><span class="sxs-lookup"><span data-stu-id="b5eb6-113">BaseAction</span></span> | <span data-ttu-id="b5eb6-114">After</span><span class="sxs-lookup"><span data-stu-id="b5eb6-114">After</span></span> | <span data-ttu-id="b5eb6-115">條件</span><span class="sxs-lookup"><span data-stu-id="b5eb6-115">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="b5eb6-116">Action1</span><span class="sxs-lookup"><span data-stu-id="b5eb6-116">Action1</span></span> |          | <span data-ttu-id="b5eb6-117">Action2</span><span class="sxs-lookup"><span data-stu-id="b5eb6-117">Action2</span></span>    | <span data-ttu-id="b5eb6-118">0</span><span class="sxs-lookup"><span data-stu-id="b5eb6-118">0</span></span>     |           |
| <span data-ttu-id="b5eb6-119">Action2</span><span class="sxs-lookup"><span data-stu-id="b5eb6-119">Action2</span></span> |          | <span data-ttu-id="b5eb6-120">Action1</span><span class="sxs-lookup"><span data-stu-id="b5eb6-120">Action1</span></span>    | <span data-ttu-id="b5eb6-121">0</span><span class="sxs-lookup"><span data-stu-id="b5eb6-121">0</span></span>     |           |



 

<span data-ttu-id="b5eb6-122">ICEM03 會張貼這兩個動作的錯誤，因為它們會將其視為 ModuleInstallExecuteSequence 資料表中的基底動作。</span><span class="sxs-lookup"><span data-stu-id="b5eb6-122">ICEM03 posts errors for these two actions because they refer to each other as base actions in the ModuleInstallExecuteSequence table.</span></span> <span data-ttu-id="b5eb6-123">[ModuleAdminUISequence](moduleadminuisequence-table.md)、 [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)、 [ModuleAdvtUISequence](moduleadvtuisequence-table.md)、 [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)、 [ModuleInstallUISequence](moduleinstalluisequence-table.md)和[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)資料表中的所有動作都必須是基底動作，或從另一個動作和前後旗標的組合衍生其位置。</span><span class="sxs-lookup"><span data-stu-id="b5eb6-123">All actions in the [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md), and [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) tables must either be base actions or derive their position from the combination of another action and a before and after flag.</span></span>

<span data-ttu-id="b5eb6-124">若要修正這個錯誤，請判斷這兩個動作的基本動作。</span><span class="sxs-lookup"><span data-stu-id="b5eb6-124">To fix this error, determine the base actions for the two actions.</span></span> <span data-ttu-id="b5eb6-125">使用預設序號新增基底動作的記錄。</span><span class="sxs-lookup"><span data-stu-id="b5eb6-125">Add a record for the base actions with a default sequence number.</span></span> <span data-ttu-id="b5eb6-126">針對 Action1 和 Action2，請在 [BaseAction] 資料行中輸入基底動作名稱，然後在 [After] 資料行中輸入0或1。</span><span class="sxs-lookup"><span data-stu-id="b5eb6-126">For Action1 and Action2 enter the base action names in the BaseAction column and 0 or 1 in the After column.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5eb6-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5eb6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5eb6-128">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="b5eb6-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



