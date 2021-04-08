---
description: 儲存在內容索引中的資料行可以有多個值，而且可以使用陣列比較述詞來比較這些多重值資料行。
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: 多重值 (陣列) 比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689864"
---
# <a name="multi-valued-array-comparisons"></a><span data-ttu-id="e8d00-103">多重值 (陣列) 比較</span><span class="sxs-lookup"><span data-stu-id="e8d00-103">Multi-Valued (ARRAY) Comparisons</span></span>

<span data-ttu-id="e8d00-104">儲存在內容索引中的資料行可以有多個值，而且可以使用陣列比較述詞來比較這些多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="e8d00-104">Columns stored in the content index can have multiple values, and those multivalued columns can be compared by using the ARRAY comparison predicate.</span></span>

<span data-ttu-id="e8d00-105">陣列比較述詞具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="e8d00-105">The ARRAY comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



<span data-ttu-id="e8d00-106">如果資料行參考不是多重值資料行，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e8d00-106">An error is returned if the column reference is not a multivalued column.</span></span> <span data-ttu-id="e8d00-107">資料行資料類型必須與比較清單的元素相容。</span><span class="sxs-lookup"><span data-stu-id="e8d00-107">The column data type must be compatible with the elements of the comparison list.</span></span> <span data-ttu-id="e8d00-108">如有必要，資料行參考可以 [轉換](-search-sql-castingdatacolumntype.md) 成另一種資料類型。</span><span class="sxs-lookup"><span data-stu-id="e8d00-108">If necessary, the column reference can be [cast](-search-sql-castingdatacolumntype.md) as another data type.</span></span>

<span data-ttu-id="e8d00-109">比較運算子 (的複合 \_ op) 可以是任何一般的比較運算子。</span><span class="sxs-lookup"><span data-stu-id="e8d00-109">The comparison operator (comp\_op) can be any of the normal comparison operators.</span></span> <span data-ttu-id="e8d00-110">在多重值比較中，比較運算子的意義會因是否使用數量詞而有些許不同。</span><span class="sxs-lookup"><span data-stu-id="e8d00-110">In a multivalued comparison, the comparison operators have slightly different meanings depending on whether a quantifier is used.</span></span> <span data-ttu-id="e8d00-111">數量詞會識別是否應針對比較清單中的所有或部分值進行比較。</span><span class="sxs-lookup"><span data-stu-id="e8d00-111">Quantifiers identify whether a comparison should be made against all or some of the values in the comparison list.</span></span> <span data-ttu-id="e8d00-112">比較運算子的函式會在描述每個數量詞 (全部的資料表中提供，本檔稍後會有一些) 。</span><span class="sxs-lookup"><span data-stu-id="e8d00-112">The functions of the comparison operators are given in the tables describing each quantifier (ALL and SOME) later in this document.</span></span>

<span data-ttu-id="e8d00-113">運算子之後的值會指定與多值資料行的所有元素比較的單一常值。</span><span class="sxs-lookup"><span data-stu-id="e8d00-113">The value after the operator specifies a single literal value that is compared against all elements of the multivalued column.</span></span> <span data-ttu-id="e8d00-114">如果有任何專案符合該值，則述詞為 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-114">If any element matches the value, the predicate is true.</span></span>

<span data-ttu-id="e8d00-115">比較清單會指定與多值資料行比較的常值陣列。</span><span class="sxs-lookup"><span data-stu-id="e8d00-115">The comparison list specifies an array of literal values that are compared against the multivalued column.</span></span> <span data-ttu-id="e8d00-116">比較清單的語法如下：</span><span class="sxs-lookup"><span data-stu-id="e8d00-116">The syntax for the comparison list follows:</span></span>


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> <span data-ttu-id="e8d00-117">請留意比較清單語法。</span><span class="sxs-lookup"><span data-stu-id="e8d00-117">Be aware of the comparison list syntax.</span></span> <span data-ttu-id="e8d00-118">組成比較清單的常值群組必須以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="e8d00-118">The group of literals that make up the comparison list must be surrounded by square brackets.</span></span> <span data-ttu-id="e8d00-119">請勿以方括弧括住比較清單的個別元素。</span><span class="sxs-lookup"><span data-stu-id="e8d00-119">Do not surround individual elements of the comparison list by square brackets.</span></span> <span data-ttu-id="e8d00-120">因此，陣列 \[ 1 \] 和陣列 \[ 1、2、3 \] 是有效的，但陣列 \[ 1 \[ 、2 \] \[ 、3 \] \] 則否。</span><span class="sxs-lookup"><span data-stu-id="e8d00-120">Therefore, ARRAY \[1\] and ARRAY \[1,2,3\] are valid, but ARRAY \[1\[,2\]\[,3\]\] is not.</span></span>

 

<span data-ttu-id="e8d00-121">用來判斷多重值比較是否傳回 true 或 false 的方法是由選擇性數量詞所指定。</span><span class="sxs-lookup"><span data-stu-id="e8d00-121">The method used to determine whether the multivalued comparison returns true or false is specified by the optional quantifier.</span></span> <span data-ttu-id="e8d00-122">下列各節描述每個數量詞，以及每個比較運算子在使用數量詞時的運作方式。</span><span class="sxs-lookup"><span data-stu-id="e8d00-122">The following sections describe each quantifier, and how each comparison operator works when the quantifier is used.</span></span>

## <a name="absent-quantifier"></a><span data-ttu-id="e8d00-123">遺漏數量詞</span><span class="sxs-lookup"><span data-stu-id="e8d00-123">Absent Quantifier</span></span>

<span data-ttu-id="e8d00-124">如果未指定數量詞，則比較左邊的每個專案都會與右邊的相同位置中的元素進行比較。</span><span class="sxs-lookup"><span data-stu-id="e8d00-124">If no quantifier is specified, each element on the left side of the comparison is compared to the element in the same position on the right side.</span></span> <span data-ttu-id="e8d00-125">比較是以陣列中的第一個元素為開頭，並進行最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="e8d00-125">The comparison begins with the first element in the arrays, and progresses through the last element.</span></span> <span data-ttu-id="e8d00-126">如果左邊的所有元素都相當於右邊的對應專案，則會使用陣列元素的數目來判斷哪個陣列較大。</span><span class="sxs-lookup"><span data-stu-id="e8d00-126">If all the elements on the left side are equivalent to the corresponding elements on the right side, the number of array elements is used to determine which array is greater.</span></span>

<span data-ttu-id="e8d00-127">下表顯示未指定數量詞時，比較運算子的作業，並提供每個量值的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="e8d00-127">The following table shows the operation of the comparison operators when no quantifier is specified and provides a brief description of each.</span></span>



| <span data-ttu-id="e8d00-128">運算子</span><span class="sxs-lookup"><span data-stu-id="e8d00-128">Operator</span></span>       | <span data-ttu-id="e8d00-129">描述</span><span class="sxs-lookup"><span data-stu-id="e8d00-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="e8d00-130">當每個左邊專案的值與對應的右邊元素相同，而且這兩個數組具有相同數目的專案時，「等於」就會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-130">'Equal to' returns true when each left-side element has the same value as the corresponding right-side element, and both arrays have the same number of elements.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="e8d00-131">！ = 或 <></span><span class="sxs-lookup"><span data-stu-id="e8d00-131">!= or <></span></span> | <span data-ttu-id="e8d00-132">當一或多個左邊專案的值與對應的右端元素不同，或左邊和右邊的陣列沒有相同數目的專案時，' Not 等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-132">'Not equal to' returns true when one or more left-side elements have values that differ from the corresponding right-side elements, or when the left-side and right-side arrays do not have the same number of elements.</span></span>                                                                                                                                                              |
| >           | <span data-ttu-id="e8d00-133">當每個左邊專案的值大於對應右邊元素的值時，' 大於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-133">'Greater than' returns true when the value of each left-side element is greater than the value of the corresponding right-side element.</span></span> <span data-ttu-id="e8d00-134">如果所有左邊的元素值完全符合對應的右端元素，而左邊的陣列有比右邊陣列更多的元素，則 ' 大於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-134">If all the left-side element values exactly match the corresponding right-side elements and the left-side array has more elements than the right-side array, 'greater than' returns true.</span></span>                                                     |
| >=          | <span data-ttu-id="e8d00-135">當每個左邊專案的值大於或等於相對應右邊元素的值時，' 大於或等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-135">'Greater than or equal to' returns true when the value of every left-side element is greater than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="e8d00-136">如果所有左邊的元素值等於或大於對應的右端元素，而且左邊的陣列具有和右邊陣列相同或更多的元素，則 ' 大於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-136">If all the left-side element values are equal to or greater than the corresponding right-side elements and the left-side array has the same or more elements than the right-side array, 'greater than' returns true.</span></span> |
| <           | <span data-ttu-id="e8d00-137">當每個左邊專案的值小於對應右邊元素的值時，' 小於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-137">'Less than' returns true when the value of each left-side element is less than the value of the corresponding right-side element.</span></span> <span data-ttu-id="e8d00-138">當左邊的元素比右邊少時，' 小於 ' 也會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-138">'Less than' also returns true when the left-side side has fewer elements than the right-side side.</span></span>                                                                                                                                                  |
| <=          | <span data-ttu-id="e8d00-139">當每個左邊專案的值小於或等於相對應右邊元素的值時，' 小於或等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-139">'Less than or equal to' returns true when the value of every left-side element is less than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="e8d00-140">如果所有左邊的元素值等於或小於對應的右端元素，而且左邊的陣列具有和右邊陣列相同或較少的元素，則 ' 大於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-140">If all the left-side element values are equal to or less than the corresponding right-side elements and the left-side array has the same or fewer elements than the right-side array, 'greater than' returns true.</span></span>         |



 

## <a name="all-quantifier"></a><span data-ttu-id="e8d00-141">所有數量詞</span><span class="sxs-lookup"><span data-stu-id="e8d00-141">ALL Quantifier</span></span>

<span data-ttu-id="e8d00-142">所有數量詞會指定左邊的每個專案都會與右邊的每個元素進行比較。</span><span class="sxs-lookup"><span data-stu-id="e8d00-142">The ALL quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="e8d00-143">若要傳回 true，相較于右邊的每個專案，比較對於左邊的每個專案都必須是 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-143">To return true, the comparison must be true for each element on the left side when compared to every element on the right side.</span></span> <span data-ttu-id="e8d00-144">左邊和右邊陣列中的元素數目不會影響結果。</span><span class="sxs-lookup"><span data-stu-id="e8d00-144">The number of elements in the left and right array sides has no effect on the result.</span></span>

<span data-ttu-id="e8d00-145">下表顯示每個比較運算子如何與所有數量詞搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e8d00-145">The following table shows how each comparison operator functions with the ALL quantifier.</span></span>



| <span data-ttu-id="e8d00-146">運算子</span><span class="sxs-lookup"><span data-stu-id="e8d00-146">Operator</span></span>       | <span data-ttu-id="e8d00-147">描述</span><span class="sxs-lookup"><span data-stu-id="e8d00-147">Description</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="e8d00-148">當每個左邊的元素值與每個右邊的元素值相同時，' 等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-148">'Equal to' returns true when each left-side element value is the same as every right-side element value.</span></span>                              |
| <span data-ttu-id="e8d00-149">！ = 或 <></span><span class="sxs-lookup"><span data-stu-id="e8d00-149">!= or <></span></span> | <span data-ttu-id="e8d00-150">當至少有一個左邊的元素值與任何右邊的元素值不同時，' Not 等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-150">'Not equal to' returns true when at least one of the left-side element values is different from any of the right-side element values.</span></span> |
| >           | <span data-ttu-id="e8d00-151">當每個左邊的元素值大於每個右邊的元素值時，' 大於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-151">'Greater than' returns true when each left-side element value is greater than every right-side element value.</span></span>                         |
| >=          | <span data-ttu-id="e8d00-152">當每個左邊的元素值大於或等於每個右邊的元素值時，' 大於或等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-152">'Greater than or equal to' returns true when each left-side element value is greater than or equal to every right-side element value.</span></span> |
| <           | <span data-ttu-id="e8d00-153">當每個左邊的元素值小於每個右邊的元素值時，' 小於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-153">'Less than' returns true when each left-side element value is less than every right-side element value.</span></span>                               |
| <=          | <span data-ttu-id="e8d00-154">當每個左邊的元素值小於或等於每個右邊的元素值時，' 小於或等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-154">'Less than or equal to' returns true when each left-side element value is less than or equal to every right-side element value.</span></span>       |



 

## <a name="some-or-any-quantifier"></a><span data-ttu-id="e8d00-155">某些 (或任何) 數量詞</span><span class="sxs-lookup"><span data-stu-id="e8d00-155">SOME (or ANY) Quantifier</span></span>

<span data-ttu-id="e8d00-156">某些數量詞和任何數量詞都可以交替使用。</span><span class="sxs-lookup"><span data-stu-id="e8d00-156">The SOME quantifier and the ANY quantifier can be used interchangeably.</span></span> <span data-ttu-id="e8d00-157">就像所有數量詞一樣，某些數量詞會指定左邊的每個專案都會與右邊的每個元素進行比較。</span><span class="sxs-lookup"><span data-stu-id="e8d00-157">Like the ALL quantifier, the SOME quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="e8d00-158">若要傳回 true，相較于右邊的任何專案，比較必須為左邊的至少一個元素。</span><span class="sxs-lookup"><span data-stu-id="e8d00-158">To return true, the comparison must be true for at least one of the elements on the left side when compared to any element on the right side.</span></span> <span data-ttu-id="e8d00-159">左邊和右邊陣列的元素數目不會影響結果。</span><span class="sxs-lookup"><span data-stu-id="e8d00-159">The number of elements on the left and right side arrays has no effect on the result.</span></span>

<span data-ttu-id="e8d00-160">下表顯示每個比較運算子如何與某個數量詞搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e8d00-160">The following table shows how each comparison operator functions with the SOME quantifier.</span></span>



| <span data-ttu-id="e8d00-161">運算子</span><span class="sxs-lookup"><span data-stu-id="e8d00-161">Operator</span></span>       | <span data-ttu-id="e8d00-162">描述</span><span class="sxs-lookup"><span data-stu-id="e8d00-162">Description</span></span>                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="e8d00-163">當至少有一個左邊的元素值與任何右邊的元素值相同時，' 等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-163">'Equal to' returns true when at least one of the left-side element values is the same as any of the right-side element values.</span></span>                                  |
| <span data-ttu-id="e8d00-164">！ = 或 <></span><span class="sxs-lookup"><span data-stu-id="e8d00-164">!= or <></span></span> | <span data-ttu-id="e8d00-165">如果沒有左邊的元素值與任何右邊的元素值相同，則「不等於」會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-165">'Not equal to' returns true when none of the left-side element values is the same as any of the right-side element values.</span></span>                                      |
| >           | <span data-ttu-id="e8d00-166">當至少有一個左邊的元素值大於任何一個右邊的元素值時，' 大於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-166">'Greater than' returns true when at least one of the left-side element values is greater than any one of the right-side element values.</span></span>                         |
| >=          | <span data-ttu-id="e8d00-167">當至少有一個左邊的元素值大於或等於任一個右邊的元素值時，' 大於或等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-167">'Greater than or equal to' returns true when at least one of the left-side element values is greater than or equal to any one of the right-side element values.</span></span> |
| <           | <span data-ttu-id="e8d00-168">當至少有一個左邊的元素值小於任何一個右邊的元素值時，' 小於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-168">'Less than' returns true when at least one of the left-side element values is less than any one of the right-side element values.</span></span>                               |
| <=          | <span data-ttu-id="e8d00-169">當至少有一個左邊的元素值小於或等於右邊的任何一個元素值時，' 小於或等於 ' 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-169">'Less than or equal to' returns true when at least one of the left-side element values is less than or equal to any one of the right-side element values.</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="e8d00-170">範例</span><span class="sxs-lookup"><span data-stu-id="e8d00-170">Examples</span></span>

<span data-ttu-id="e8d00-171">下列範例會檢查檔是否為「財務」或「規劃」類別：</span><span class="sxs-lookup"><span data-stu-id="e8d00-171">The following example checks whether documents are in the "Finance" or "Planning" categories:</span></span>


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



<span data-ttu-id="e8d00-172">下列比較全部評估為 true。</span><span class="sxs-lookup"><span data-stu-id="e8d00-172">The following comparisons all evaluate true.</span></span> <span data-ttu-id="e8d00-173">請記住，在實際使用中，搜尋查詢語法需要左邊為屬性，而不是常值。</span><span class="sxs-lookup"><span data-stu-id="e8d00-173">Remember that in actual use, the search query syntax requires the left side to be a property, not a literal value.</span></span>


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a><span data-ttu-id="e8d00-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8d00-174">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e8d00-175">**參考**</span><span class="sxs-lookup"><span data-stu-id="e8d00-175">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e8d00-176">LIKE 述詞</span><span class="sxs-lookup"><span data-stu-id="e8d00-176">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="e8d00-177">常值比較</span><span class="sxs-lookup"><span data-stu-id="e8d00-177">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="e8d00-178">Null 述詞</span><span class="sxs-lookup"><span data-stu-id="e8d00-178">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="e8d00-179">**概念**</span><span class="sxs-lookup"><span data-stu-id="e8d00-179">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e8d00-180">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="e8d00-180">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="e8d00-181">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="e8d00-181">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



