---
description: 彙總函式會對一組值執行計算，並傳回值。 這麼做可讓您產生多層級群組的摘要統計資料，而不會產生太多負荷。
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: 彙總函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563534"
---
# <a name="aggregate-functions"></a><span data-ttu-id="6c7ac-104">彙總函式</span><span class="sxs-lookup"><span data-stu-id="6c7ac-104">Aggregate Functions</span></span>

<span data-ttu-id="6c7ac-105">彙總函式會對一組值執行計算，並傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-105">An aggregate function performs a calculation on a set of values and returns a value.</span></span> <span data-ttu-id="6c7ac-106">這麼做可讓您產生多層級群組的摘要統計資料，而不會產生太多負荷。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-106">Doing so makes it possible to generate summary statistics for multi-level groups with little overhead.</span></span>

## <a name="about-aggregate-functions"></a><span data-ttu-id="6c7ac-107">關於彙總函式</span><span class="sxs-lookup"><span data-stu-id="6c7ac-107">About Aggregate Functions</span></span>

<span data-ttu-id="6c7ac-108">Windows Search 結構化查詢語言 (SQL)  (SQL) 中的彙總函式具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="6c7ac-108">Aggregate functions in Windows Search Structured Query Language (SQL) have the following syntax:</span></span>


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



<span data-ttu-id="6c7ac-109">函數部分可以包含下列任何函數和語法：</span><span class="sxs-lookup"><span data-stu-id="6c7ac-109">The function portion can include any of the following functions and syntax:</span></span>



| <span data-ttu-id="6c7ac-110">函式</span><span class="sxs-lookup"><span data-stu-id="6c7ac-110">Function</span></span>                                                              | <span data-ttu-id="6c7ac-111">描述</span><span class="sxs-lookup"><span data-stu-id="6c7ac-111">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7ac-112">平均 (<column>) </span><span class="sxs-lookup"><span data-stu-id="6c7ac-112">AVG(<column>)</span></span>                                                   | <span data-ttu-id="6c7ac-113">傳回群組中的值的平均值。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-113">Returns the average of the values in a group.</span></span> <span data-ttu-id="6c7ac-114">只適用于數位。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-114">Applies only to numbers.</span></span>                                                                                                                                      |
| <span data-ttu-id="6c7ac-115">BYFREQUENCY (<column> ， <N>) </span><span class="sxs-lookup"><span data-stu-id="6c7ac-115">BYFREQUENCY(<column>, <N>)</span></span>                                | <span data-ttu-id="6c7ac-116">從群組中的結果傳回最常出現的 N 個數據行值。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-116">Returns the most frequent N column values from the results in the group.</span></span> <span data-ttu-id="6c7ac-117">也包含每個值發生次數的計數，以及包含每個傳回值之結果的檔識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-117">Also includes a count of how many times each value occurred and document identifiers for results that contain each returned value.</span></span> |
| <span data-ttu-id="6c7ac-118">CHILDCOUNT () </span><span class="sxs-lookup"><span data-stu-id="6c7ac-118">CHILDCOUNT()</span></span>                                                          | <span data-ttu-id="6c7ac-119">傳回群組中的專案數 (排除子群組) 。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-119">Returns the number of items in a group (excluding subgroups).</span></span> <span data-ttu-id="6c7ac-120">如果有多個群組層級，這會傳回直屬子群組的數目。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-120">If there are multiple levels of grouping, this returns the number of immediate child groups.</span></span>                                                  |
| <span data-ttu-id="6c7ac-121">計數 () </span><span class="sxs-lookup"><span data-stu-id="6c7ac-121">COUNT()</span></span>                                                               | <span data-ttu-id="6c7ac-122">傳回群組和所有子群組中的專案數。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-122">Returns the number of items in a group and all subgroups.</span></span>                                                                                                                                                   |
| <span data-ttu-id="6c7ac-123">DATERANGE (<column>) </span><span class="sxs-lookup"><span data-stu-id="6c7ac-123">DATERANGE(<column>)</span></span>                                             | <span data-ttu-id="6c7ac-124">傳回在群組結果群組中找到之資料行值的下限和上限。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-124">Returns the lower and upper bounds of the column values found in the group results group.</span></span> <span data-ttu-id="6c7ac-125">只有 filetime 屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-125">Valid only for filetime properties.</span></span>                                                                               |
| <span data-ttu-id="6c7ac-126">第一個 (<column> ， <N>) </span><span class="sxs-lookup"><span data-stu-id="6c7ac-126">FIRST(<column>, <N>)</span></span>                                      | <span data-ttu-id="6c7ac-127">從群組中找到的分葉結果傳回前 N 個數據行值。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-127">Returns the first N column values from leaf results found in a group.</span></span>                                                                                                                                       |
| <span data-ttu-id="6c7ac-128">最大 (<column>) </span><span class="sxs-lookup"><span data-stu-id="6c7ac-128">MAX(<column>)</span></span>                                                   | <span data-ttu-id="6c7ac-129">傳回運算式中的最大值。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-129">Returns the maximum value in the expression.</span></span> <span data-ttu-id="6c7ac-130">只適用于數位或日期。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-130">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="6c7ac-131">最小 (<column>) </span><span class="sxs-lookup"><span data-stu-id="6c7ac-131">MIN(<column>)</span></span>                                                   | <span data-ttu-id="6c7ac-132">傳回運算式中的最小值。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-132">Returns the minimum value in the expression.</span></span> <span data-ttu-id="6c7ac-133">只適用于數位或日期。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-133">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="6c7ac-134">REPRESENTATIVEOF (<column> 、 <idRepresentative> <N>) </span><span class="sxs-lookup"><span data-stu-id="6c7ac-134">REPRESENTATIVEOF(<column>, <idRepresentative>, <N>)</span></span> | <span data-ttu-id="6c7ac-135">傳回 N 個 idRepresentative 值，每個值都是從具有唯一資料行值的其中一個結果子集選取。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-135">Returns N idRepresentative values, each selected from one of the result subsets that has a unique column value.</span></span> <span data-ttu-id="6c7ac-136">每個值也會以具有 idRepresentative 值的檔識別碼傳回。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-136">Each value is also returned with a document identifier that has the idRepresentative value.</span></span> |
| <span data-ttu-id="6c7ac-137">SUM (<column>) </span><span class="sxs-lookup"><span data-stu-id="6c7ac-137">SUM(<column>)</span></span>                                                   | <span data-ttu-id="6c7ac-138">傳回群組中值的總和。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-138">Returns the sum of the values in a group.</span></span> <span data-ttu-id="6c7ac-139">只適用于數位。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-139">Applies only to numbers.</span></span>                                                                                                                                          |



 

 

> [!Note]  
> <span data-ttu-id="6c7ac-140">匯總會以個別資料行傳回。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-140">Aggregates are returned as individual columns.</span></span> <span data-ttu-id="6c7ac-141">它們大多是簡單類型，除了 ByFrequency、First、DateRange 和 RepresentativeOf，會以複合類型傳回。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-141">They are mostly simple types except for ByFrequency, First, DateRange, and RepresentativeOf which are returned as compound types.</span></span>

 

<span data-ttu-id="6c7ac-142">您可以針對匯總使用任何數值或日期資料行，而不只是 SELECT 子句中的資料行。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-142">You can use any numeric or date column for aggregations, and not only those that are in the SELECT clause.</span></span> <span data-ttu-id="6c7ac-143">不過，您無法將匯總分組。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-143">However, you cannot group on aggregates.</span></span> <span data-ttu-id="6c7ac-144">如果傳入的資料行引數不是數值或日期類型，就會傳回語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-144">A syntax error is returned if the column argument passed in is not either a numeric or date type.</span></span>

<span data-ttu-id="6c7ac-145">標籤部分是選擇性的，並為標籤提供更容易讀取的別名。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-145">The label portion is optional and provides a more readable alias for the label.</span></span> <span data-ttu-id="6c7ac-146">如果您未包含別名標籤，則 Windows Search 會將函式和資料行名稱轉換成標籤。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-146">If you do not include an alias label, then Windows Search transforms the function and column name into a label.</span></span> <span data-ttu-id="6c7ac-147">例如，MAX (System.Doc>ument。WordCount) 會變成 MAX \_ SystemDocumentWordCount。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-147">For example, MAX(System.Document.WordCount) becomes MAX\_SystemDocumentWordCount.</span></span>

## <a name="multi-level-groups-and-counting"></a><span data-ttu-id="6c7ac-148">多層級群組和計數</span><span class="sxs-lookup"><span data-stu-id="6c7ac-148">Multi-level Groups and Counting</span></span>

<span data-ttu-id="6c7ac-149">匯總是定義在葉上，並且會重複。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-149">Aggregates are defined over leaves and are duplicated.</span></span> <span data-ttu-id="6c7ac-150">匯總會以群組的形式來輸入群組，將它定義 (檔) ，而非其子群組的子群組。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-150">An aggregate takes as input the leaves of the group that defines it (documents), rather than the subgroups of its children.</span></span> <span data-ttu-id="6c7ac-151">這項功能稱為多重層級群組。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-151">This functionality is referred to as multi-level grouping.</span></span>

<span data-ttu-id="6c7ac-152">除了定義于保留和重複的匯總外，這些匯總只會計算一次。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-152">In addition to aggregates being defined over leaves and duplicated, they are counted only once.</span></span> <span data-ttu-id="6c7ac-153">雖然同一份檔可能會在一個群組下表示多次，但匯總只會考慮一次。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-153">While the same document might be represented multiple times under one group, aggregates would only consider it once.</span></span> <span data-ttu-id="6c7ac-154">下圖說明這個概念。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-154">The following graphic illustrates this concept.</span></span>

![圖表顯示匯總是定義于保留和重複的，而且只會計算一次](images/aggregates.png)

## <a name="aggregate-examples"></a><span data-ttu-id="6c7ac-156">匯總範例</span><span class="sxs-lookup"><span data-stu-id="6c7ac-156">Aggregate Examples</span></span>

<span data-ttu-id="6c7ac-157">以下是 GROUP ON 子句內的彙總函式範例：</span><span class="sxs-lookup"><span data-stu-id="6c7ac-157">The following are examples of aggregate functions within the GROUP ON clause:</span></span>


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a><span data-ttu-id="6c7ac-158">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c7ac-158">Return Value</span></span>

<span data-ttu-id="6c7ac-159">傳回值是在資料列集上找到作為自訂屬性的 variant，可作為指定的別名，如果未指定別名標籤，則為「匯總」。</span><span class="sxs-lookup"><span data-stu-id="6c7ac-159">The return value is a variant found on the rowset as a custom property, either as the specified aliases or as "Aggregates" if no alias label is specified.</span></span>

 

 



