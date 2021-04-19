---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型19。
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: 自訂動作類型19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982777"
---
# <a name="custom-action-type-19"></a><span data-ttu-id="9f87a-103">自訂動作類型19</span><span class="sxs-lookup"><span data-stu-id="9f87a-103">Custom Action Type 19</span></span>

<span data-ttu-id="9f87a-104">此自訂動作會顯示指定的錯誤訊息、傳回失敗，然後結束安裝。</span><span class="sxs-lookup"><span data-stu-id="9f87a-104">This custom action displays a specified error message, returns failure, and then terminates the installation.</span></span> <span data-ttu-id="9f87a-105">顯示的錯誤訊息可提供為字串或 [錯誤資料表](error-table.md)中的索引。</span><span class="sxs-lookup"><span data-stu-id="9f87a-105">The error message displayed can be supplied as a string or as an index into the [Error table](error-table.md).</span></span>

## <a name="source"></a><span data-ttu-id="9f87a-106">來源</span><span class="sxs-lookup"><span data-stu-id="9f87a-106">Source</span></span>

<span data-ttu-id="9f87a-107">將 [CustomAction 資料表](customaction-table.md) 的來源資料行保留空白。</span><span class="sxs-lookup"><span data-stu-id="9f87a-107">Leave the Source column of the [CustomAction table](customaction-table.md) blank.</span></span>

## <a name="type-value"></a><span data-ttu-id="9f87a-108">類型值</span><span class="sxs-lookup"><span data-stu-id="9f87a-108">Type Value</span></span>

<span data-ttu-id="9f87a-109">在 CustomAction 資料表的 Type 資料行中包含下列值，以指定基本的數數值型別。</span><span class="sxs-lookup"><span data-stu-id="9f87a-109">Include the following value in the Type column of the CustomAction table to specify the basic numeric type.</span></span>



| <span data-ttu-id="9f87a-110">常數</span><span class="sxs-lookup"><span data-stu-id="9f87a-110">Constants</span></span>                                                               | <span data-ttu-id="9f87a-111">十六進位</span><span class="sxs-lookup"><span data-stu-id="9f87a-111">Hexadecimal</span></span> | <span data-ttu-id="9f87a-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="9f87a-112">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9f87a-113">**msidbCustomActionTypeTextData**  + **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="9f87a-113">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="9f87a-114">0x013</span><span class="sxs-lookup"><span data-stu-id="9f87a-114">0x013</span></span>       | <span data-ttu-id="9f87a-115">19</span><span class="sxs-lookup"><span data-stu-id="9f87a-115">19</span></span>      |



 

## <a name="target"></a><span data-ttu-id="9f87a-116">目標</span><span class="sxs-lookup"><span data-stu-id="9f87a-116">Target</span></span>

<span data-ttu-id="9f87a-117">[CustomAction 資料表](customaction-table.md)的目標資料行包含使用 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (中指定的功能來格式化的文字字串，而不含數值欄位規範) 。</span><span class="sxs-lookup"><span data-stu-id="9f87a-117">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="9f87a-118">要取代的參數會以方括弧（...）括住， \[ \] 而且可能是屬性、環境變數 (% prefix) 、檔案路徑 (\# 首碼) 或元件目錄路徑 ($ prefix) 。</span><span class="sxs-lookup"><span data-stu-id="9f87a-118">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="9f87a-119">如果將字串格式化為整數，則會使用該整數做為 [錯誤資料表](error-table.md) 的索引，以取得要顯示的訊息。</span><span class="sxs-lookup"><span data-stu-id="9f87a-119">If after formatting the string evaluates to an integer, that integer is used as an index into the [Error table](error-table.md) to retrieve the message to display.</span></span> <span data-ttu-id="9f87a-120">如果在格式化字串之後包含非數位字元，則字串本身會顯示為訊息。</span><span class="sxs-lookup"><span data-stu-id="9f87a-120">If after formatting the string contains non-numeric characters, the string itself is displayed as the message.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="9f87a-121">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="9f87a-121">Return Processing Options</span></span>

<span data-ttu-id="9f87a-122">自訂動作不會使用任何選項。</span><span class="sxs-lookup"><span data-stu-id="9f87a-122">The custom action does not use any options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="9f87a-123">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="9f87a-123">Execution Scheduling Options</span></span>

<span data-ttu-id="9f87a-124">自訂動作不會使用任何選項。</span><span class="sxs-lookup"><span data-stu-id="9f87a-124">The custom action does not use any options.</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="9f87a-125">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="9f87a-125">In-Script Execution Options</span></span>

<span data-ttu-id="9f87a-126">自訂動作不會使用任何選項。</span><span class="sxs-lookup"><span data-stu-id="9f87a-126">The custom action does not use any options.</span></span>

## <a name="return-values"></a><span data-ttu-id="9f87a-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f87a-127">Return Values</span></span>

<span data-ttu-id="9f87a-128">請參閱 [自訂動作傳回值](custom-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="9f87a-128">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f87a-129">備註</span><span class="sxs-lookup"><span data-stu-id="9f87a-129">Remarks</span></span>

<span data-ttu-id="9f87a-130">例如，自訂動作 CAError1、CAError2、CAError3 和 CAError4 會傳回這些訊息。</span><span class="sxs-lookup"><span data-stu-id="9f87a-130">For example, the custom actions CAError1, CAError2, CAError3, and CAError4 return these messages.</span></span>

[<span data-ttu-id="9f87a-131">CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="9f87a-131">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="9f87a-132">動作</span><span class="sxs-lookup"><span data-stu-id="9f87a-132">Action</span></span>   | <span data-ttu-id="9f87a-133">類型</span><span class="sxs-lookup"><span data-stu-id="9f87a-133">Type</span></span> | <span data-ttu-id="9f87a-134">來源</span><span class="sxs-lookup"><span data-stu-id="9f87a-134">Source</span></span> | <span data-ttu-id="9f87a-135">目標</span><span class="sxs-lookup"><span data-stu-id="9f87a-135">Target</span></span>                              |
|----------|------|--------|-------------------------------------|
| <span data-ttu-id="9f87a-136">CAError1</span><span class="sxs-lookup"><span data-stu-id="9f87a-136">CAError1</span></span> | <span data-ttu-id="9f87a-137">19</span><span class="sxs-lookup"><span data-stu-id="9f87a-137">19</span></span>   |        | <span data-ttu-id="9f87a-138">\[Prop1\]</span><span class="sxs-lookup"><span data-stu-id="9f87a-138">\[Prop1\]</span></span>                           |
| <span data-ttu-id="9f87a-139">CAError2</span><span class="sxs-lookup"><span data-stu-id="9f87a-139">CAError2</span></span> | <span data-ttu-id="9f87a-140">19</span><span class="sxs-lookup"><span data-stu-id="9f87a-140">19</span></span>   |        | <span data-ttu-id="9f87a-141">因為 Error2，所以安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="9f87a-141">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="9f87a-142">CAError3</span><span class="sxs-lookup"><span data-stu-id="9f87a-142">CAError3</span></span> | <span data-ttu-id="9f87a-143">19</span><span class="sxs-lookup"><span data-stu-id="9f87a-143">19</span></span>   |        | <span data-ttu-id="9f87a-144">25000</span><span class="sxs-lookup"><span data-stu-id="9f87a-144">25000</span></span>                               |
| <span data-ttu-id="9f87a-145">CAError4</span><span class="sxs-lookup"><span data-stu-id="9f87a-145">CAError4</span></span> | <span data-ttu-id="9f87a-146">19</span><span class="sxs-lookup"><span data-stu-id="9f87a-146">19</span></span>   |        | <span data-ttu-id="9f87a-147">\[This.prop2\]</span><span class="sxs-lookup"><span data-stu-id="9f87a-147">\[Prop2\]</span></span>                           |



 

[<span data-ttu-id="9f87a-148">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="9f87a-148">Property Table</span></span>](property-table.md)



| <span data-ttu-id="9f87a-149">屬性</span><span class="sxs-lookup"><span data-stu-id="9f87a-149">Property</span></span> | <span data-ttu-id="9f87a-150">值</span><span class="sxs-lookup"><span data-stu-id="9f87a-150">Value</span></span>                                 |
|----------|---------------------------------------|
| <span data-ttu-id="9f87a-151">Prop1</span><span class="sxs-lookup"><span data-stu-id="9f87a-151">Prop1</span></span>    | <span data-ttu-id="9f87a-152">「由於 Error1 的安裝失敗。」</span><span class="sxs-lookup"><span data-stu-id="9f87a-152">"Installation failure due to Error1."</span></span> |
| <span data-ttu-id="9f87a-153">This.prop2</span><span class="sxs-lookup"><span data-stu-id="9f87a-153">Prop2</span></span>    | <span data-ttu-id="9f87a-154">"25100"</span><span class="sxs-lookup"><span data-stu-id="9f87a-154">"25100"</span></span>                               |



 

[<span data-ttu-id="9f87a-155">錯誤資料表</span><span class="sxs-lookup"><span data-stu-id="9f87a-155">Error Table</span></span>](error-table.md)



| <span data-ttu-id="9f87a-156">程式碼</span><span class="sxs-lookup"><span data-stu-id="9f87a-156">Code</span></span>  | <span data-ttu-id="9f87a-157">訊息</span><span class="sxs-lookup"><span data-stu-id="9f87a-157">Message</span></span>                             |
|-------|-------------------------------------|
| <span data-ttu-id="9f87a-158">25000</span><span class="sxs-lookup"><span data-stu-id="9f87a-158">25000</span></span> | <span data-ttu-id="9f87a-159">因為 Error3，所以安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="9f87a-159">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="9f87a-160">25100</span><span class="sxs-lookup"><span data-stu-id="9f87a-160">25100</span></span> | <span data-ttu-id="9f87a-161">因為 Error4，所以安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="9f87a-161">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="9f87a-162">這些自訂動作會傳回下列錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="9f87a-162">These custom actions return the following error messages:</span></span>



| <span data-ttu-id="9f87a-163">自訂動作</span><span class="sxs-lookup"><span data-stu-id="9f87a-163">Custom action</span></span> | <span data-ttu-id="9f87a-164">傳回的訊息字串</span><span class="sxs-lookup"><span data-stu-id="9f87a-164">Returned message string</span></span>             |
|---------------|-------------------------------------|
| <span data-ttu-id="9f87a-165">CAError1</span><span class="sxs-lookup"><span data-stu-id="9f87a-165">CAError1</span></span>      | <span data-ttu-id="9f87a-166">因為 Error1，所以安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="9f87a-166">Installation failure due to Error1.</span></span> |
| <span data-ttu-id="9f87a-167">CAError2</span><span class="sxs-lookup"><span data-stu-id="9f87a-167">CAError2</span></span>      | <span data-ttu-id="9f87a-168">因為 Error2，所以安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="9f87a-168">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="9f87a-169">CAError3</span><span class="sxs-lookup"><span data-stu-id="9f87a-169">CAError3</span></span>      | <span data-ttu-id="9f87a-170">因為 Error3，所以安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="9f87a-170">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="9f87a-171">CAError4</span><span class="sxs-lookup"><span data-stu-id="9f87a-171">CAError4</span></span>      | <span data-ttu-id="9f87a-172">因為 Error4，所以安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="9f87a-172">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="9f87a-173">請注意，因為撰寫 [LaunchCondition 資料表](launchcondition-table.md)無法保證啟動狀況的評估順序，所以您應該在安裝中使用自訂動作類型19個自訂動作，以特定順序來評估條件。</span><span class="sxs-lookup"><span data-stu-id="9f87a-173">Note that because the order of evaluation of launch conditions cannot be guaranteed by authoring the [LaunchCondition table](launchcondition-table.md), you should use Custom Action Type 19 custom actions in your installation to evaluate conditions in a specific order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f87a-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f87a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f87a-175">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="9f87a-175">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



