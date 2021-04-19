---
description: ICE72 會確認 AdvtExecuteSequence 資料表中不會使用非內建的自訂動作。
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994464"
---
# <a name="ice72"></a><span data-ttu-id="dc0f2-103">ICE72</span><span class="sxs-lookup"><span data-stu-id="dc0f2-103">ICE72</span></span>

<span data-ttu-id="dc0f2-104">ICE72 會確認 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中不會使用非內建的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="dc0f2-104">ICE72 verifies that non-built-in custom actions are not used in the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span> <span data-ttu-id="dc0f2-105">具體而言，AdvtExecuteSequence 資料表中只允許類型19、type 35 和 type 51 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="dc0f2-105">Specifically, only type 19, type 35, and type 51 custom actions are allowed in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="dc0f2-106">如果使用其他自訂動作，則公告可能無法如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="dc0f2-106">If other custom actions are used, advertisement may not behave as expected.</span></span>

## <a name="result"></a><span data-ttu-id="dc0f2-107">結果</span><span class="sxs-lookup"><span data-stu-id="dc0f2-107">Result</span></span>

<span data-ttu-id="dc0f2-108">如果 AdvExecuteSequence 資料表使用類型35、類型51和類型19以外的自訂動作，ICE72 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc0f2-108">ICE72 returns an error if the AdvExecuteSequence table uses custom actions other than type 35, type 51, and type 19.</span></span>

## <a name="example"></a><span data-ttu-id="dc0f2-109">範例</span><span class="sxs-lookup"><span data-stu-id="dc0f2-109">Example</span></span>

<span data-ttu-id="dc0f2-110">ICE72 會針對所顯示的範例報告下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="dc0f2-110">ICE72 reports the following error for the example shown:</span></span>

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

<span data-ttu-id="dc0f2-111">若要修正錯誤，請從 AdvtExecuteSequence 資料表中移除 ' CA1 '。</span><span class="sxs-lookup"><span data-stu-id="dc0f2-111">To fix the error, remove 'CA1' from the AdvtExecuteSequence table.</span></span>

<span data-ttu-id="dc0f2-112">[AdvtExecuteSequence 資料表](advtexecutesequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="dc0f2-112">[AdvtExecuteSequence Table](advtexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="dc0f2-113">動作</span><span class="sxs-lookup"><span data-stu-id="dc0f2-113">Action</span></span> |
|--------|
| <span data-ttu-id="dc0f2-114">CA1</span><span class="sxs-lookup"><span data-stu-id="dc0f2-114">CA1</span></span>    |
| <span data-ttu-id="dc0f2-115">CA35</span><span class="sxs-lookup"><span data-stu-id="dc0f2-115">CA35</span></span>   |



 

<span data-ttu-id="dc0f2-116">[CustomAction 資料表](customaction-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="dc0f2-116">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="dc0f2-117">動作</span><span class="sxs-lookup"><span data-stu-id="dc0f2-117">Action</span></span> | <span data-ttu-id="dc0f2-118">類型</span><span class="sxs-lookup"><span data-stu-id="dc0f2-118">Type</span></span> |
|--------|------|
| <span data-ttu-id="dc0f2-119">CA1</span><span class="sxs-lookup"><span data-stu-id="dc0f2-119">CA1</span></span>    | <span data-ttu-id="dc0f2-120">1</span><span class="sxs-lookup"><span data-stu-id="dc0f2-120">1</span></span>    |
| <span data-ttu-id="dc0f2-121">CA35</span><span class="sxs-lookup"><span data-stu-id="dc0f2-121">CA35</span></span>   | <span data-ttu-id="dc0f2-122">35</span><span class="sxs-lookup"><span data-stu-id="dc0f2-122">35</span></span>   |



 

## <a name="tables-used-during-execution"></a><span data-ttu-id="dc0f2-123">執行期間所使用的資料表</span><span class="sxs-lookup"><span data-stu-id="dc0f2-123">Tables used during execution</span></span>

[<span data-ttu-id="dc0f2-124">AdvtExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="dc0f2-124">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)

[<span data-ttu-id="dc0f2-125">CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="dc0f2-125">CustomAction Table</span></span>](customaction-table.md)

## <a name="related-topics"></a><span data-ttu-id="dc0f2-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc0f2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc0f2-127">自訂動作類型19</span><span class="sxs-lookup"><span data-stu-id="dc0f2-127">Custom Action Type 19</span></span>](custom-action-type-19.md)
</dt> <dt>

[<span data-ttu-id="dc0f2-128">自訂動作類型35</span><span class="sxs-lookup"><span data-stu-id="dc0f2-128">Custom Action Type 35</span></span>](custom-action-type-35.md)
</dt> <dt>

[<span data-ttu-id="dc0f2-129">自訂動作類型51</span><span class="sxs-lookup"><span data-stu-id="dc0f2-129">Custom Action Type 51</span></span>](custom-action-type-51.md)
</dt> <dt>

[<span data-ttu-id="dc0f2-130">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="dc0f2-130">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



