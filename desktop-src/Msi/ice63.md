---
description: ICE63 會檢查是否有適當的 RemoveExistingProducts 動作順序。
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850603"
---
# <a name="ice63"></a><span data-ttu-id="b488e-103">ICE63</span><span class="sxs-lookup"><span data-stu-id="b488e-103">ICE63</span></span>

<span data-ttu-id="b488e-104">ICE63 會檢查是否有適當的 [RemoveExistingProducts 動作](removeexistingproducts-action.md)順序。</span><span class="sxs-lookup"><span data-stu-id="b488e-104">ICE63 checks for proper sequencing of the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="b488e-105">可能會放置 RemoveExistingProducts 動作：</span><span class="sxs-lookup"><span data-stu-id="b488e-105">The RemoveExistingProducts action may be placed:</span></span>

1.  <span data-ttu-id="b488e-106">介於 InstallValidate 和 InstallInitialize 之間</span><span class="sxs-lookup"><span data-stu-id="b488e-106">Between InstallValidate and InstallInitialize</span></span>
2.  <span data-ttu-id="b488e-107">緊接在 InstallInitialize 之後，或在 InstallInitialize 之後，如果 InstallInitialize 和 RemoveExistingProducts 之間的動作未產生任何腳本動作。</span><span class="sxs-lookup"><span data-stu-id="b488e-107">Immediately after InstallInitialize, or after InstallInitialize if the actions between InstallInitialize and RemoveExistingProducts do not generate any script actions.</span></span>
3.  <span data-ttu-id="b488e-108">緊接在 InstallExecute 或 InstallExecuteAgain 之後，以及 InstallFinalize 之前 (上述的相同限制適用于) 。</span><span class="sxs-lookup"><span data-stu-id="b488e-108">Immediately after InstallExecute or InstallExecuteAgain and before InstallFinalize (the same restriction as above applies).</span></span>
4.  <span data-ttu-id="b488e-109">InstallFinalize 之後。</span><span class="sxs-lookup"><span data-stu-id="b488e-109">After InstallFinalize.</span></span>

<span data-ttu-id="b488e-110">若無法修正 ICE63 回報的警告或錯誤，會導致升級失敗。</span><span class="sxs-lookup"><span data-stu-id="b488e-110">Failure to fix a warning or error reported by ICE63 leads to failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="b488e-111">結果</span><span class="sxs-lookup"><span data-stu-id="b488e-111">Result</span></span>

<span data-ttu-id="b488e-112">如果 RemoveExistingProducts 動作的排序不正確，ICE63 會張貼警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="b488e-112">ICE63 posts a warning or error if the sequencing of the RemoveExistingProducts action is not correct.</span></span>

## <a name="example"></a><span data-ttu-id="b488e-113">範例</span><span class="sxs-lookup"><span data-stu-id="b488e-113">Example</span></span>

<span data-ttu-id="b488e-114">ICE63 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="b488e-114">ICE63 reports the following error for the example shown.</span></span>

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

<span data-ttu-id="b488e-115">' MyCustomAction ' 動作發生于 InstallInitialize 和 RemoveExistingProducts 之間。</span><span class="sxs-lookup"><span data-stu-id="b488e-115">The action 'MyCustomAction' occurs between InstallInitialize and RemoveExistingProducts.</span></span> <span data-ttu-id="b488e-116">如果 MyCustomAction 在腳本中產生任何動作，這會造成安裝中的問題。</span><span class="sxs-lookup"><span data-stu-id="b488e-116">If MyCustomAction generates any actions in the script, this causes problems in the installation.</span></span>

<span data-ttu-id="b488e-117">若要修正這個錯誤，請確認 MyCustomAction 不會產生任何腳本動作或重新排序動作。</span><span class="sxs-lookup"><span data-stu-id="b488e-117">To fix this error, verify that MyCustomAction does not generate any script actions or resequence the actions.</span></span>

[<span data-ttu-id="b488e-118">InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="b488e-118">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="b488e-119">動作</span><span class="sxs-lookup"><span data-stu-id="b488e-119">Action</span></span>                 | <span data-ttu-id="b488e-120">條件</span><span class="sxs-lookup"><span data-stu-id="b488e-120">Condition</span></span> | <span data-ttu-id="b488e-121">順序</span><span class="sxs-lookup"><span data-stu-id="b488e-121">Sequence</span></span> |
|------------------------|-----------|----------|
| <span data-ttu-id="b488e-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="b488e-122">InstallInitialize</span></span>      |           | <span data-ttu-id="b488e-123">1000</span><span class="sxs-lookup"><span data-stu-id="b488e-123">1000</span></span>     |
| <span data-ttu-id="b488e-124">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="b488e-124">MyCustomAction</span></span>         |           | <span data-ttu-id="b488e-125">1010</span><span class="sxs-lookup"><span data-stu-id="b488e-125">1010</span></span>     |
| <span data-ttu-id="b488e-126">RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="b488e-126">RemoveExistingProducts</span></span> |           | <span data-ttu-id="b488e-127">1020</span><span class="sxs-lookup"><span data-stu-id="b488e-127">1020</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="b488e-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="b488e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b488e-129">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="b488e-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



