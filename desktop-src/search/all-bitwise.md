---
description: 所有位 and 部分位關鍵字都是用來測試整數型別中的位。
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: 全部位 and 部分位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511086"
---
# <a name="all-bitwise-and-some-bitwise"></a><span data-ttu-id="9f286-103">全部位 and 部分位</span><span class="sxs-lookup"><span data-stu-id="9f286-103">ALL BITWISE and SOME BITWISE</span></span>

<span data-ttu-id="9f286-104">**所有位** AND **部分位** 關鍵字都是用來測試整數型別中的位。</span><span class="sxs-lookup"><span data-stu-id="9f286-104">The **ALL BITWISE** and **SOME BITWISE** keywords are used for testing the bits in an integral type.</span></span> <span data-ttu-id="9f286-105">如果屬性中的所有設定位都符合遮罩，則 **所有位** 都是 true。</span><span class="sxs-lookup"><span data-stu-id="9f286-105">If all of the set bits in a property match the mask, **ALL BITWISE** is true.</span></span> <span data-ttu-id="9f286-106">如果屬性中至少有一個設定位符合遮罩，則 **某些位** 為 true。</span><span class="sxs-lookup"><span data-stu-id="9f286-106">If at least one of the set bits in a property matches the mask, **SOME BITWISE** is true.</span></span>

<span data-ttu-id="9f286-107">您可以將運算子套用至純量 (單一值) 屬性和向量 (多重值) 屬性。</span><span class="sxs-lookup"><span data-stu-id="9f286-107">Operators can be applied to both scalar (single-value) properties and vector (multiple-value) properties.</span></span> <span data-ttu-id="9f286-108">下列程式碼範例示範如何使用 **所有位** And 和 **SOME 位** 來測試屬性值。</span><span class="sxs-lookup"><span data-stu-id="9f286-108">The following code example shows how to test property values with **ALL BITWISE** and **SOME BITWISE**.</span></span>


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a><span data-ttu-id="9f286-109">比較運算子</span><span class="sxs-lookup"><span data-stu-id="9f286-109">Comparison Operators</span></span>

<span data-ttu-id="9f286-110">下表列出支援的位測試比較運算子。</span><span class="sxs-lookup"><span data-stu-id="9f286-110">The supported comparison operators for BITWISE tests are listed in the following table.</span></span>



| <span data-ttu-id="9f286-111">比較運算子</span><span class="sxs-lookup"><span data-stu-id="9f286-111">Comparison operator</span></span> | <span data-ttu-id="9f286-112">描述</span><span class="sxs-lookup"><span data-stu-id="9f286-112">Description</span></span>  |
|---------------------|--------------|
| =                   | <span data-ttu-id="9f286-113">等於</span><span class="sxs-lookup"><span data-stu-id="9f286-113">Equal to</span></span>     |
| <span data-ttu-id="9f286-114">！ = 或 <></span><span class="sxs-lookup"><span data-stu-id="9f286-114">!= or <></span></span>      | <span data-ttu-id="9f286-115">不等於</span><span class="sxs-lookup"><span data-stu-id="9f286-115">Not equal to</span></span> |



 

<span data-ttu-id="9f286-116">下表列出位測試的邏輯。</span><span class="sxs-lookup"><span data-stu-id="9f286-116">The logic of BITWISE tests is listed in the following table.</span></span>



| <span data-ttu-id="9f286-117">位測試和比較運算子</span><span class="sxs-lookup"><span data-stu-id="9f286-117">BITWISE test and comparison operator</span></span> | <span data-ttu-id="9f286-118">邏輯</span><span class="sxs-lookup"><span data-stu-id="9f286-118">Logic</span></span>                   |
|--------------------------------------|-------------------------|
| <span data-ttu-id="9f286-119">= 全部位</span><span class="sxs-lookup"><span data-stu-id="9f286-119">= ALL BITWISE</span></span>                        | <span data-ttu-id="9f286-120">屬性 & Mask = Mask</span><span class="sxs-lookup"><span data-stu-id="9f286-120">Property & Mask = Mask</span></span>  |
| <span data-ttu-id="9f286-121">= 部分位</span><span class="sxs-lookup"><span data-stu-id="9f286-121">= SOME BITWISE</span></span>                       | <span data-ttu-id="9f286-122">屬性 & Mask！ = 0</span><span class="sxs-lookup"><span data-stu-id="9f286-122">Property & Mask != 0</span></span>    |
| <span data-ttu-id="9f286-123"><> 全部位</span><span class="sxs-lookup"><span data-stu-id="9f286-123"><> ALL BITWISE</span></span>                 | <span data-ttu-id="9f286-124">屬性 & Mask！ = Mask</span><span class="sxs-lookup"><span data-stu-id="9f286-124">Property & Mask != Mask</span></span> |
| <span data-ttu-id="9f286-125"><> 部分位</span><span class="sxs-lookup"><span data-stu-id="9f286-125"><> SOME BITWISE</span></span>                | <span data-ttu-id="9f286-126">屬性 & Mask = 0</span><span class="sxs-lookup"><span data-stu-id="9f286-126">Property & Mask = 0</span></span>     |



 

<span data-ttu-id="9f286-127">下列事實資料表使用範例二進位和十六進位值來示範位測試的邏輯。</span><span class="sxs-lookup"><span data-stu-id="9f286-127">The following truth table uses example binary and hex values to demonstate the logic of BITWISE tests.</span></span>



| <span data-ttu-id="9f286-128">Binary (hex) 中的屬性</span><span class="sxs-lookup"><span data-stu-id="9f286-128">Property in binary (hex)</span></span> | <span data-ttu-id="9f286-129">Binary 中的遮罩 (hex) </span><span class="sxs-lookup"><span data-stu-id="9f286-129">Mask in binary (hex)</span></span> | <span data-ttu-id="9f286-130">屬性 & Mask = binary (hex) </span><span class="sxs-lookup"><span data-stu-id="9f286-130">Property & Mask = binary (hex)</span></span> | <span data-ttu-id="9f286-131">= 部分位</span><span class="sxs-lookup"><span data-stu-id="9f286-131">= SOME BITWISE</span></span> | <span data-ttu-id="9f286-132">= 全部位</span><span class="sxs-lookup"><span data-stu-id="9f286-132">= ALL BITWISE</span></span> |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| <span data-ttu-id="9f286-133">0001 (0x1) </span><span class="sxs-lookup"><span data-stu-id="9f286-133">0001 (0x1)</span></span>               | <span data-ttu-id="9f286-134">0001 (0x1) </span><span class="sxs-lookup"><span data-stu-id="9f286-134">0001 (0x1)</span></span>           | <span data-ttu-id="9f286-135">0001 (0x1) </span><span class="sxs-lookup"><span data-stu-id="9f286-135">0001 (0x1)</span></span>                     | <span data-ttu-id="9f286-136">True</span><span class="sxs-lookup"><span data-stu-id="9f286-136">True</span></span>           | <span data-ttu-id="9f286-137">True</span><span class="sxs-lookup"><span data-stu-id="9f286-137">True</span></span>          |
| <span data-ttu-id="9f286-138">0001 (0x1) </span><span class="sxs-lookup"><span data-stu-id="9f286-138">0001 (0x1)</span></span>               | <span data-ttu-id="9f286-139">0011 (0x3) </span><span class="sxs-lookup"><span data-stu-id="9f286-139">0011 (0x3)</span></span>           | <span data-ttu-id="9f286-140">0001 (0x1) </span><span class="sxs-lookup"><span data-stu-id="9f286-140">0001 (0x1)</span></span>                     | <span data-ttu-id="9f286-141">是</span><span class="sxs-lookup"><span data-stu-id="9f286-141">True</span></span>           | <span data-ttu-id="9f286-142">否</span><span class="sxs-lookup"><span data-stu-id="9f286-142">False</span></span>         |
| <span data-ttu-id="9f286-143">0011 (0x3) </span><span class="sxs-lookup"><span data-stu-id="9f286-143">0011 (0x3)</span></span>               | <span data-ttu-id="9f286-144">0001 (0x1) </span><span class="sxs-lookup"><span data-stu-id="9f286-144">0001 (0x1)</span></span>           | <span data-ttu-id="9f286-145">0001 (0x1) </span><span class="sxs-lookup"><span data-stu-id="9f286-145">0001 (0x1)</span></span>                     | <span data-ttu-id="9f286-146">True</span><span class="sxs-lookup"><span data-stu-id="9f286-146">True</span></span>           | <span data-ttu-id="9f286-147">True</span><span class="sxs-lookup"><span data-stu-id="9f286-147">True</span></span>          |
| <span data-ttu-id="9f286-148">0010 (0x2) </span><span class="sxs-lookup"><span data-stu-id="9f286-148">0010 (0x2)</span></span>               | <span data-ttu-id="9f286-149">0001 (0x1) </span><span class="sxs-lookup"><span data-stu-id="9f286-149">0001 (0x1)</span></span>           | <span data-ttu-id="9f286-150">0000 (0x0) </span><span class="sxs-lookup"><span data-stu-id="9f286-150">0000 (0x0)</span></span>                     | <span data-ttu-id="9f286-151">False</span><span class="sxs-lookup"><span data-stu-id="9f286-151">False</span></span>          | <span data-ttu-id="9f286-152">False</span><span class="sxs-lookup"><span data-stu-id="9f286-152">False</span></span>         |
| <span data-ttu-id="9f286-153">11110000 (0xF0) </span><span class="sxs-lookup"><span data-stu-id="9f286-153">11110000 (0xF0)</span></span>          | <span data-ttu-id="9f286-154">00000011 (0x03) </span><span class="sxs-lookup"><span data-stu-id="9f286-154">00000011 (0x03)</span></span>      | <span data-ttu-id="9f286-155">00000000 (0x00) </span><span class="sxs-lookup"><span data-stu-id="9f286-155">00000000 (0x00)</span></span>                | <span data-ttu-id="9f286-156">False</span><span class="sxs-lookup"><span data-stu-id="9f286-156">False</span></span>          | <span data-ttu-id="9f286-157">False</span><span class="sxs-lookup"><span data-stu-id="9f286-157">False</span></span>         |
| <span data-ttu-id="9f286-158">11110010 (0xF2) </span><span class="sxs-lookup"><span data-stu-id="9f286-158">11110010 (0xF2)</span></span>          | <span data-ttu-id="9f286-159">11110010 (0xF2) </span><span class="sxs-lookup"><span data-stu-id="9f286-159">11110010 (0xF2)</span></span>      | <span data-ttu-id="9f286-160">11110010 (0xF2) </span><span class="sxs-lookup"><span data-stu-id="9f286-160">11110010 (0xF2)</span></span>                | <span data-ttu-id="9f286-161">True</span><span class="sxs-lookup"><span data-stu-id="9f286-161">True</span></span>           | <span data-ttu-id="9f286-162">True</span><span class="sxs-lookup"><span data-stu-id="9f286-162">True</span></span>          |
| <span data-ttu-id="9f286-163">11110010 (0xF2) </span><span class="sxs-lookup"><span data-stu-id="9f286-163">11110010 (0xF2)</span></span>          | <span data-ttu-id="9f286-164">00000011 (0x03) </span><span class="sxs-lookup"><span data-stu-id="9f286-164">00000011 (0x03)</span></span>      | <span data-ttu-id="9f286-165">00000010 (0x02) </span><span class="sxs-lookup"><span data-stu-id="9f286-165">00000010 (0x02)</span></span>                | <span data-ttu-id="9f286-166">是</span><span class="sxs-lookup"><span data-stu-id="9f286-166">True</span></span>           | <span data-ttu-id="9f286-167">否</span><span class="sxs-lookup"><span data-stu-id="9f286-167">False</span></span>         |



 

## <a name="example"></a><span data-ttu-id="9f286-168">範例</span><span class="sxs-lookup"><span data-stu-id="9f286-168">Example</span></span>

<span data-ttu-id="9f286-169">以下是 **所有位** 述詞的範例。</span><span class="sxs-lookup"><span data-stu-id="9f286-169">The following is an example of the **ALL BITWISE** predicate.</span></span>


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a><span data-ttu-id="9f286-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f286-170">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9f286-171">**概念**</span><span class="sxs-lookup"><span data-stu-id="9f286-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9f286-172">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="9f286-172">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="9f286-173">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="9f286-173">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



