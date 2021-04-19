---
description: ICE68 會檢查安裝所需的所有自訂動作類型是否有效。
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987393"
---
# <a name="ice68"></a><span data-ttu-id="c8c6d-103">ICE68</span><span class="sxs-lookup"><span data-stu-id="c8c6d-103">ICE68</span></span>

<span data-ttu-id="c8c6d-104">ICE68 會檢查安裝所需的所有自訂動作類型是否有效。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-104">ICE68 checks that all custom action types needed for an installation are valid.</span></span> <span data-ttu-id="c8c6d-105">若無法修正 ICE68 所回報的錯誤，會導致嘗試執行動作失敗的安裝。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-105">Failure to fix the error reported by ICE68 causes an installation that attempts to execute the action to fail.</span></span> <span data-ttu-id="c8c6d-106">如果設定 **msidbCustomActionTypeNoImpersonate** 屬性時未同時設定 **MSIDBCUSTOMACTIONTYPEINSCRIPT** 屬性，ICE68 會發出警告。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-106">ICE68 issues a warning if the **msidbCustomActionTypeNoImpersonate** attribute is set without also setting the **msidbCustomActionTypeInScript** attribute.</span></span>

## <a name="result"></a><span data-ttu-id="c8c6d-107">結果</span><span class="sxs-lookup"><span data-stu-id="c8c6d-107">Result</span></span>

<span data-ttu-id="c8c6d-108">如果安裝所需的動作類型無效，ICE68 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-108">ICE68 returns an error if an action type needed for an installation is invalid.</span></span>

## <a name="example"></a><span data-ttu-id="c8c6d-109">範例</span><span class="sxs-lookup"><span data-stu-id="c8c6d-109">Example</span></span>

<span data-ttu-id="c8c6d-110">如果自訂動作在 CustomAction 資料表的類型欄位中設定 **msidbCustomActionTypeNoImpersonate** 位，但未設定 **msidbCustomActionTypeInScript** ，ICE68 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-110">ICE68 posts the following warning if a custom action has the **msidbCustomActionTypeNoImpersonate** bit set in the Type field of the CustomAction table without the **msidbCustomActionTypeInScript** also set.</span></span>

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

<span data-ttu-id="c8c6d-111">若要修正此警告，請在自訂動作包含 **msidbCustomActionTypeNoImpersonate** (0x800) 時，包括 **msidbCustomActionTypeInScript** (0x400) 。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-111">To fix this warning, include **msidbCustomActionTypeInScript** (0x400) if the custom action includes **msidbCustomActionTypeNoImpersonate** (0x800).</span></span> <span data-ttu-id="c8c6d-112">否則，安裝程式會忽略 **msidbCustomActionTypeNoImpersonate** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-112">Otherwise the installer ignores the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="c8c6d-113">如需詳細資訊，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="c8c6d-114">ICE68 會針對所顯示的範例報告下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="c8c6d-114">ICE68 reports the following error for the example shown:</span></span>

``` syntax
Invalid custom action type for action 'Action1'.
```

<span data-ttu-id="c8c6d-115">1027不是有效的動作類型。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-115">1027 is not a valid action type.</span></span>

<span data-ttu-id="c8c6d-116">若要修正這個錯誤，請選擇有效的自訂動作類型。</span><span class="sxs-lookup"><span data-stu-id="c8c6d-116">To fix this error, choose a valid custom action type.</span></span>

<span data-ttu-id="c8c6d-117">[CustomAction 資料表](customaction-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="c8c6d-117">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="c8c6d-118">動作</span><span class="sxs-lookup"><span data-stu-id="c8c6d-118">Action</span></span>  | <span data-ttu-id="c8c6d-119">類型</span><span class="sxs-lookup"><span data-stu-id="c8c6d-119">Type</span></span> | <span data-ttu-id="c8c6d-120">來源</span><span class="sxs-lookup"><span data-stu-id="c8c6d-120">Source</span></span>   | <span data-ttu-id="c8c6d-121">目標</span><span class="sxs-lookup"><span data-stu-id="c8c6d-121">Target</span></span>     |
|---------|------|----------|------------|
| <span data-ttu-id="c8c6d-122">Action1</span><span class="sxs-lookup"><span data-stu-id="c8c6d-122">Action1</span></span> | <span data-ttu-id="c8c6d-123">1027</span><span class="sxs-lookup"><span data-stu-id="c8c6d-123">1027</span></span> | <span data-ttu-id="c8c6d-124">引數</span><span class="sxs-lookup"><span data-stu-id="c8c6d-124">Argument</span></span> | <span data-ttu-id="c8c6d-125">Component1</span><span class="sxs-lookup"><span data-stu-id="c8c6d-125">Component1</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c8c6d-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8c6d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8c6d-127">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="c8c6d-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



