---
description: 條件資料表可以用來根據條件運算式修改特徵資料表中任何專案的選取狀態。
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: 條件資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936647"
---
# <a name="condition-table"></a><span data-ttu-id="3dbbd-103">條件資料表</span><span class="sxs-lookup"><span data-stu-id="3dbbd-103">Condition Table</span></span>

<span data-ttu-id="3dbbd-104">條件資料表可以用來根據條件運算式修改 [特徵資料表](feature-table.md) 中任何專案的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-104">The Condition table can be used to modify the selection state of any entry in the [Feature table](feature-table.md) based on a conditional expression.</span></span>

<span data-ttu-id="3dbbd-105">條件資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-105">The Condition table has the following columns.</span></span>



| <span data-ttu-id="3dbbd-106">Column</span><span class="sxs-lookup"><span data-stu-id="3dbbd-106">Column</span></span>    | <span data-ttu-id="3dbbd-107">類型</span><span class="sxs-lookup"><span data-stu-id="3dbbd-107">Type</span></span>                         | <span data-ttu-id="3dbbd-108">答案</span><span class="sxs-lookup"><span data-stu-id="3dbbd-108">Key</span></span> | <span data-ttu-id="3dbbd-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="3dbbd-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="3dbbd-110">功能\_</span><span class="sxs-lookup"><span data-stu-id="3dbbd-110">Feature\_</span></span> | [<span data-ttu-id="3dbbd-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="3dbbd-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="3dbbd-112">Y</span><span class="sxs-lookup"><span data-stu-id="3dbbd-112">Y</span></span>   | <span data-ttu-id="3dbbd-113">N</span><span class="sxs-lookup"><span data-stu-id="3dbbd-113">N</span></span>        |
| <span data-ttu-id="3dbbd-114">層級</span><span class="sxs-lookup"><span data-stu-id="3dbbd-114">Level</span></span>     | [<span data-ttu-id="3dbbd-115">整數</span><span class="sxs-lookup"><span data-stu-id="3dbbd-115">Integer</span></span>](integer.md)       | <span data-ttu-id="3dbbd-116">Y</span><span class="sxs-lookup"><span data-stu-id="3dbbd-116">Y</span></span>   | <span data-ttu-id="3dbbd-117">N</span><span class="sxs-lookup"><span data-stu-id="3dbbd-117">N</span></span>        |
| <span data-ttu-id="3dbbd-118">條件</span><span class="sxs-lookup"><span data-stu-id="3dbbd-118">Condition</span></span> | [<span data-ttu-id="3dbbd-119">Condition</span><span class="sxs-lookup"><span data-stu-id="3dbbd-119">Condition</span></span>](condition.md)   | <span data-ttu-id="3dbbd-120">N</span><span class="sxs-lookup"><span data-stu-id="3dbbd-120">N</span></span>   | <span data-ttu-id="3dbbd-121">Y</span><span class="sxs-lookup"><span data-stu-id="3dbbd-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3dbbd-122">資料行</span><span class="sxs-lookup"><span data-stu-id="3dbbd-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3dbbd-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_</span><span class="sxs-lookup"><span data-stu-id="3dbbd-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="3dbbd-124">在功能資料表的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-124">External key into column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="3dbbd-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>水準</span><span class="sxs-lookup"><span data-stu-id="3dbbd-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Level</span></span>
</dt> <dd>

<span data-ttu-id="3dbbd-126">此資料表的功能資料行中功能的條件式安裝層級 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-126">A conditional install level for the feature in the Feature\_ column of this table.</span></span> <span data-ttu-id="3dbbd-127">如果 [條件] 資料行中的運算式評估為 TRUE，則安裝程式會將這項功能的安裝層級設定為此資料行中指定的層級。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-127">The installer sets the install level of this feature to the level specified in this column if the expression in the Condition column evaluates to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="3dbbd-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="3dbbd-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="3dbbd-129">如果此條件運算式評估為 TRUE，則會將功能資料表中的層級資料行設定為條件式安裝層級。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-129">If this conditional expression evaluates to TRUE, then the Level column in the Feature table is set to the conditional install level.</span></span>

<span data-ttu-id="3dbbd-130">[條件] 資料行中的運算式不應該包含任何功能或元件之已安裝狀態的參考。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-130">The expression in the Condition column should not contain reference to the installed state of any feature or component.</span></span> <span data-ttu-id="3dbbd-131">這是因為 [條件] 資料行中的運算式會在安裝程式評估功能和元件的已安裝狀態之前評估。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-131">This is because the expressions in the Condition column are evaluated before the installer evaluates the installed states of features and components.</span></span> <span data-ttu-id="3dbbd-132">在條件資料表中嘗試檢查功能或元件之已安裝狀態的任何運算式一律會評估為 false。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-132">Any expression in the Condition table that attempts to check the installed state of a feature or component always evaluates to false.</span></span>

<span data-ttu-id="3dbbd-133">如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-133">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3dbbd-134">備註</span><span class="sxs-lookup"><span data-stu-id="3dbbd-134">Remarks</span></span>

<span data-ttu-id="3dbbd-135">將 [層級] 資料行設定為0可永久停用功能。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-135">A feature can be permanently disabled by setting the Level column to 0.</span></span>

<span data-ttu-id="3dbbd-136">層級可以根據任何條件陳述式來設定，例如平臺、作業系統或特定屬性設定的測試。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-136">The Level may be set based on any conditional statement, such as a test for platform, operating system, or a particular property setting.</span></span>

<span data-ttu-id="3dbbd-137">應謹慎選擇條件，以便在安裝時不啟用功能，然後在卸載時停用。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-137">Conditions should be carefully chosen so that a feature is not enabled on install and then disabled on uninstall.</span></span> <span data-ttu-id="3dbbd-138">這將會孤立功能，而產品將無法卸載。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-138">This will orphan the feature and the product will not be able to be uninstalled.</span></span>

<span data-ttu-id="3dbbd-139">當 [CostFinalize 動作](costfinalize-action.md) 執行時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-139">This table is referred to when the [CostFinalize action](costfinalize-action.md) is executed.</span></span>

<span data-ttu-id="3dbbd-140">如果 [**預先**](preselected.md) 選取的屬性已設定為1，安裝程式就不會評估條件資料表。</span><span class="sxs-lookup"><span data-stu-id="3dbbd-140">If the [**Preselected**](preselected.md) property has been set to 1, the installer does not evaluate the Condition table.</span></span> <span data-ttu-id="3dbbd-141">只有在未設定下列任何屬性時，條件資料表才會影響功能的安裝：</span><span class="sxs-lookup"><span data-stu-id="3dbbd-141">The Condition table affects only the installation of features when none of the following properties have been set:</span></span>

<dl>

[<span data-ttu-id="3dbbd-142">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-142">**ADDLOCAL**</span></span>](addlocal.md)  
[<span data-ttu-id="3dbbd-143">**刪除**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-143">**REMOVE**</span></span>](remove.md)  
[<span data-ttu-id="3dbbd-144">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-144">**ADDSOURCE**</span></span>](addsource.md)  
[<span data-ttu-id="3dbbd-145">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-145">**ADDDEFAULT**</span></span>](adddefault.md)  
[<span data-ttu-id="3dbbd-146">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-146">**REINSTALL**</span></span>](reinstall.md)  
[<span data-ttu-id="3dbbd-147">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-147">**ADVERTISE**</span></span>](advertise.md)  
[<span data-ttu-id="3dbbd-148">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-148">**COMPADDLOCAL**</span></span>](compaddlocal.md)  
[<span data-ttu-id="3dbbd-149">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-149">**COMPADDSOURCE**</span></span>](compaddsource.md)  
[<span data-ttu-id="3dbbd-150">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-150">**COMPADDDEFAULT**</span></span>](compadddefault.md)  
[<span data-ttu-id="3dbbd-151">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-151">**FILEADDLOCAL**</span></span>](fileaddlocal.md)  
[<span data-ttu-id="3dbbd-152">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-152">**FILEADDSOURCE**</span></span>](fileaddsource.md)  
[<span data-ttu-id="3dbbd-153">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3dbbd-153">**FILEADDDEFAULT**</span></span>](fileadddefault.md)  
</dl>

## <a name="validation"></a><span data-ttu-id="3dbbd-154">驗證</span><span class="sxs-lookup"><span data-stu-id="3dbbd-154">Validation</span></span>

<dl>

[<span data-ttu-id="3dbbd-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="3dbbd-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3dbbd-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="3dbbd-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3dbbd-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="3dbbd-157">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="3dbbd-158">ICE46</span><span class="sxs-lookup"><span data-stu-id="3dbbd-158">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="3dbbd-159">ICE79</span><span class="sxs-lookup"><span data-stu-id="3dbbd-159">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="3dbbd-160">ICE86</span><span class="sxs-lookup"><span data-stu-id="3dbbd-160">ICE86</span></span>](ice86.md)  
</dl>

 

 



