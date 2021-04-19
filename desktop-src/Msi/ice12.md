---
description: ICE12 會驗證 Windows Installer 資料庫的 CustomAction、Directory、AdminExecuteSequence、AdminUISequence、AdvtExecuteSequence、InstallExecuteSequence 和 InstallUISequence 資料表。
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998125"
---
# <a name="ice12"></a><span data-ttu-id="aa656-103">ICE12</span><span class="sxs-lookup"><span data-stu-id="aa656-103">ICE12</span></span>

<span data-ttu-id="aa656-104">ICE12 會查詢 [CustomAction](customaction-table.md)、 [Directory](directory-table.md)、 [AdminExecuteSequence](adminexecutesequence-table.md)、 [AdminUISequence](adminuisequence-table.md)、 [AdvtExecuteSequence](advtexecutesequence-table.md)、 [InstallExecuteSequence](installexecutesequence-table.md)和 [InstallUISequence](installuisequence-table.md) 資料表，以驗證下列各項：</span><span class="sxs-lookup"><span data-stu-id="aa656-104">ICE12 queries the [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [InstallUISequence](installuisequence-table.md) tables to validate the following:</span></span>

-   <span data-ttu-id="aa656-105">[CostFinalize 動作](costfinalize-action.md)發生于任何順序資料表中，其中包含類型[自訂動作類型 35](custom-action-type-35.md)或[自訂動作類型 51](custom-action-type-51.md)的動作。</span><span class="sxs-lookup"><span data-stu-id="aa656-105">That the [CostFinalize action](costfinalize-action.md) occurs in any sequence table containing actions of the type [Custom Action Type 35](custom-action-type-35.md) or [Custom Action Type 51](custom-action-type-51.md).</span></span>
-   <span data-ttu-id="aa656-106">每個 [自訂動作類型 35](custom-action-type-35.md) 都是在 [CostFinalize 動作](costfinalize-action.md)之後。</span><span class="sxs-lookup"><span data-stu-id="aa656-106">That every [Custom Action Type 35](custom-action-type-35.md) comes after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="aa656-107">在順序資料表中。</span><span class="sxs-lookup"><span data-stu-id="aa656-107">in the sequence tables.</span></span>
-   <span data-ttu-id="aa656-108">針對 CustomAction 資料表之來源資料行中的目錄資料表具有外鍵的每個 [自訂動作類型 51](custom-action-type-51.md) ，都會出現在順序資料表中的 [CostFinalize 動作](costfinalize-action.md) 之前。</span><span class="sxs-lookup"><span data-stu-id="aa656-108">That every [Custom Action Type 51](custom-action-type-51.md) that has a foreign key to the Directory table in the Source column of the CustomAction table comes before the [CostFinalize action](costfinalize-action.md) in the sequence tables.</span></span>

<span data-ttu-id="aa656-109">請注意，ICE12 不會驗證 CustomAction 資料表的目標資料行中格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="aa656-109">Note that ICE12 does not validate the formatted text in the Target column of the CustomAction table.</span></span>

## <a name="result"></a><span data-ttu-id="aa656-110">結果</span><span class="sxs-lookup"><span data-stu-id="aa656-110">Result</span></span>

<span data-ttu-id="aa656-111">如果設定目錄屬性的自訂動作驗證失敗，ICE12 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="aa656-111">ICE12 posts an error message if validation of the custom actions that set a directory property fails.</span></span>

## <a name="example"></a><span data-ttu-id="aa656-112">範例</span><span class="sxs-lookup"><span data-stu-id="aa656-112">Example</span></span>

<span data-ttu-id="aa656-113">ICE12 會針對所顯示的範例張貼三個錯誤。</span><span class="sxs-lookup"><span data-stu-id="aa656-113">ICE12 would post three errors for the example shown.</span></span>

-   <span data-ttu-id="aa656-114">針對 CA1，在目錄資料表中找不到資料夾 ' MyFolder '</span><span class="sxs-lookup"><span data-stu-id="aa656-114">For CA1, Folder 'MyFolder' not found in Directory table</span></span>
-   <span data-ttu-id="aa656-115">若為 CA2，順序 ' 80 ' 會在 InstallExecuteSequence 資料表中 CostFinalize 之前出現。</span><span class="sxs-lookup"><span data-stu-id="aa656-115">For CA2, Sequence '80' comes before CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="aa656-116">它必須在 (之後 CF@100) </span><span class="sxs-lookup"><span data-stu-id="aa656-116">It must come after (CF@100)</span></span>
-   <span data-ttu-id="aa656-117">若為 CA3，序列 ' 125 ' 會出現在 InstallExecuteSequence 資料表的 CostFinalize 之後。</span><span class="sxs-lookup"><span data-stu-id="aa656-117">For CA3, Sequence '125' comes after CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="aa656-118">它必須在 (之前 CF@100) </span><span class="sxs-lookup"><span data-stu-id="aa656-118">It must come before (CF@100)</span></span>

<span data-ttu-id="aa656-119">[CustomAction 資料表](customaction-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="aa656-119">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="aa656-120">動作</span><span class="sxs-lookup"><span data-stu-id="aa656-120">Action</span></span> | <span data-ttu-id="aa656-121">類型</span><span class="sxs-lookup"><span data-stu-id="aa656-121">Type</span></span> | <span data-ttu-id="aa656-122">來源</span><span class="sxs-lookup"><span data-stu-id="aa656-122">Source</span></span>        |
|--------|------|---------------|
| <span data-ttu-id="aa656-123">CA1</span><span class="sxs-lookup"><span data-stu-id="aa656-123">CA1</span></span>    | <span data-ttu-id="aa656-124">35</span><span class="sxs-lookup"><span data-stu-id="aa656-124">35</span></span>   | <span data-ttu-id="aa656-125">MyFolder</span><span class="sxs-lookup"><span data-stu-id="aa656-125">MyFolder</span></span>      |
| <span data-ttu-id="aa656-126">CA2</span><span class="sxs-lookup"><span data-stu-id="aa656-126">CA2</span></span>    | <span data-ttu-id="aa656-127">35</span><span class="sxs-lookup"><span data-stu-id="aa656-127">35</span></span>   | <span data-ttu-id="aa656-128">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="aa656-128">WindowsFolder</span></span> |
| <span data-ttu-id="aa656-129">CA3</span><span class="sxs-lookup"><span data-stu-id="aa656-129">CA3</span></span>    | <span data-ttu-id="aa656-130">51</span><span class="sxs-lookup"><span data-stu-id="aa656-130">51</span></span>   | <span data-ttu-id="aa656-131">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="aa656-131">WindowsFolder</span></span> |



 

[<span data-ttu-id="aa656-132">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="aa656-132">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="aa656-133">目錄</span><span class="sxs-lookup"><span data-stu-id="aa656-133">Directory</span></span>     | <span data-ttu-id="aa656-134">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="aa656-134">Directory\_Parent</span></span> | <span data-ttu-id="aa656-135">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="aa656-135">DefaultDir</span></span>    |
|---------------|-------------------|---------------|
| <span data-ttu-id="aa656-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="aa656-136">TARGETDIR</span></span>     |                   | <span data-ttu-id="aa656-137">SourceDir</span><span class="sxs-lookup"><span data-stu-id="aa656-137">SourceDir</span></span>     |
| <span data-ttu-id="aa656-138">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="aa656-138">WindowsFolder</span></span> | <span data-ttu-id="aa656-139">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="aa656-139">TARGETDIR</span></span>         | <span data-ttu-id="aa656-140">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="aa656-140">WindowsFolder</span></span> |



 

<span data-ttu-id="aa656-141">[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="aa656-141">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="aa656-142">動作</span><span class="sxs-lookup"><span data-stu-id="aa656-142">Action</span></span>       | <span data-ttu-id="aa656-143">順序</span><span class="sxs-lookup"><span data-stu-id="aa656-143">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="aa656-144">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="aa656-144">CostFinalize</span></span> | <span data-ttu-id="aa656-145">100</span><span class="sxs-lookup"><span data-stu-id="aa656-145">100</span></span>      |
| <span data-ttu-id="aa656-146">CA2</span><span class="sxs-lookup"><span data-stu-id="aa656-146">CA2</span></span>          | <span data-ttu-id="aa656-147">80</span><span class="sxs-lookup"><span data-stu-id="aa656-147">80</span></span>       |
| <span data-ttu-id="aa656-148">CA3</span><span class="sxs-lookup"><span data-stu-id="aa656-148">CA3</span></span>          | <span data-ttu-id="aa656-149">125</span><span class="sxs-lookup"><span data-stu-id="aa656-149">125</span></span>      |



 

<span data-ttu-id="aa656-150">若要修正 CA1 的錯誤，請將其 CustomAction 資料表中來源資料行的專案變更為目錄資料表中的現有專案，或將 MyFolder 加入目錄資料表中。</span><span class="sxs-lookup"><span data-stu-id="aa656-150">To fix the error for CA1 change its entry in its Source column in the CustomAction table to an existing entry in the Directory table or add MyFolder to the Directory table.</span></span>

<span data-ttu-id="aa656-151">若要修正 CA2 的錯誤，請在 InstallExecuteSequence 資料表中變更其順序，使其在 CostFinalize 動作之後。</span><span class="sxs-lookup"><span data-stu-id="aa656-151">To fix the error for CA2, change its sequence in the InstallExecuteSequence table such that it comes after the CostFinalize action.</span></span>

<span data-ttu-id="aa656-152">若要修正 CA3 的錯誤，請在 InstallExecuteSequence 資料表中變更其順序，使其在 CostFinalize 動作之前。</span><span class="sxs-lookup"><span data-stu-id="aa656-152">To fix the error for CA3, change its sequence in the InstallExecuteSequence table such that it comes before the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa656-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa656-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa656-154">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="aa656-154">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



