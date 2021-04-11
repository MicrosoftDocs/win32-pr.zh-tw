---
description: 群組開啟 .。。
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: 分組依據 .。。OVER .。。聲明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112425"
---
# <a name="group-on--over--statement"></a><span data-ttu-id="c1827-103">分組依據 .。。OVER .。。聲明</span><span class="sxs-lookup"><span data-stu-id="c1827-103">GROUP ON ... OVER ... Statement</span></span>

<span data-ttu-id="c1827-104">群組開啟 .。。OVER .。。語句會傳回階層式資料列集，其中會根據指定的資料行和選擇性的群組範圍，將搜尋結果劃分成群組。</span><span class="sxs-lookup"><span data-stu-id="c1827-104">The GROUP ON... OVER... statement returns a hierarchical rowset in which search results are divided into groups based on a specified column and optional grouping ranges.</span></span> <span data-ttu-id="c1827-105">如果您 [將 [system.string] 資料行群組](../properties/props-system-kind.md) 在一起，則結果集會分成多個群組：一個用於檔、一個用於通訊等等。</span><span class="sxs-lookup"><span data-stu-id="c1827-105">If you group on the [System.Kind](../properties/props-system-kind.md) column, the result set is divided into multiple groups: one for documents, one for communications, and so on.</span></span> <span data-ttu-id="c1827-106">如果您群組的是 [ [系統大小](../properties/props-system-size.md) ] 和 [群組範圍 100 KB]，結果集會分為三個群組：大小 < 100 KB 的專案、大小 >= 100 KB 的專案，以及沒有大小值的專案。</span><span class="sxs-lookup"><span data-stu-id="c1827-106">If you group on [System.Size](../properties/props-system-size.md) and group range 100 KB, the result set is divided into three groups: items of size < 100 KB, items of size >= 100 KB, and items with no size value.</span></span> <span data-ttu-id="c1827-107">您也可以使用函數來匯總群組。</span><span class="sxs-lookup"><span data-stu-id="c1827-107">You can also aggregate groupings with functions.</span></span>

<span data-ttu-id="c1827-108">本主題涵蓋下列主題：</span><span class="sxs-lookup"><span data-stu-id="c1827-108">This topic covers the following subjects:</span></span>

-   [<span data-ttu-id="c1827-109">語法</span><span class="sxs-lookup"><span data-stu-id="c1827-109">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="c1827-110">群組範圍</span><span class="sxs-lookup"><span data-stu-id="c1827-110">Group Ranges</span></span>](#group-ranges)
-   [<span data-ttu-id="c1827-111">標記群組</span><span class="sxs-lookup"><span data-stu-id="c1827-111">Labeling Groups</span></span>](#labeling-groups)
-   [<span data-ttu-id="c1827-112">排序群組</span><span class="sxs-lookup"><span data-stu-id="c1827-112">Ordering Groups</span></span>](#ordering-groups)
-   [<span data-ttu-id="c1827-113">嵌套群組</span><span class="sxs-lookup"><span data-stu-id="c1827-113">Nesting Groups</span></span>](#nesting-groups)
-   [<span data-ttu-id="c1827-114">向量屬性上的分組</span><span class="sxs-lookup"><span data-stu-id="c1827-114">Grouping on Vector Properties</span></span>](#grouping-on-vector-properties)
-   [<span data-ttu-id="c1827-115">更多範例</span><span class="sxs-lookup"><span data-stu-id="c1827-115">More Examples</span></span>](#more-examples)
-   [<span data-ttu-id="c1827-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1827-116">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="c1827-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1827-117">Syntax</span></span>

<span data-ttu-id="c1827-118">群組開啟 .。。OVER .。。語句具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="c1827-118">The GROUP ON ... OVER ... statement has the following syntax:</span></span>


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



<span data-ttu-id="c1827-119">群組範圍定義如下：</span><span class="sxs-lookup"><span data-stu-id="c1827-119">where grouping ranges are defined as follows:</span></span>


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



<span data-ttu-id="c1827-120">群組 <column> 可以是屬性存放區中屬性的一般或分隔的 [識別碼](-search-sql-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="c1827-120">The GROUP ON <column> can be a regular or delimited [identifier](-search-sql-identifiers.md) for a property in the property store.</span></span>

<span data-ttu-id="c1827-121">選擇性 <group ranges> 是一個或多個值的清單， (數位、日期或字串) 用來將結果分割成群組。</span><span class="sxs-lookup"><span data-stu-id="c1827-121">The optional <group ranges> is a list of one or more values (number, date, or string) used for dividing the results into groups.</span></span> <span data-ttu-id="c1827-122">會 <range limit> 識別所傳回結果集中的除法點，並 <label> 識別群組的使用者易記標籤。</span><span class="sxs-lookup"><span data-stu-id="c1827-122">The <range limit> identifies a division point in the returned result set, and the <label> identifies a user-friendly label for a group.</span></span> <span data-ttu-id="c1827-123">您可以將結果集分成多個所需的群組。</span><span class="sxs-lookup"><span data-stu-id="c1827-123">You can divide the result set into as many groups as you need.</span></span>

<span data-ttu-id="c1827-124">第一個結果群組包含的專案具有指定屬性的最小可能值，但不包括第一個範圍限制。</span><span class="sxs-lookup"><span data-stu-id="c1827-124">The first group of results includes items with the minimum possible value for the specified property up to but not including the first range limit.</span></span> <span data-ttu-id="c1827-125">您可以使用 MINVALUE 關鍵字來參考這個群組。</span><span class="sxs-lookup"><span data-stu-id="c1827-125">This group can be referred to with the MINVALUE keyword.</span></span> <span data-ttu-id="c1827-126">第二個群組可以參考範圍限制規範本身，並且包含其值為指定屬性等於或大於範圍限制的專案。</span><span class="sxs-lookup"><span data-stu-id="c1827-126">The second group can be referred to with the range limit specifier itself and includes items whose value for the specified property is equal to or greater than the range limit.</span></span> <span data-ttu-id="c1827-127">最後會傳回任何沒有指定屬性值的專案，而且可以使用 **Null** 關鍵字來參考這些專案。</span><span class="sxs-lookup"><span data-stu-id="c1827-127">Any items that do not have a value for the specified property are returned last and can be referred to with the **NULL** keyword.</span></span>

<span data-ttu-id="c1827-128">例如， [DateCreated](../properties/props-system-datecreated.md) 屬性 ' 2006-01-01 ' 的範圍限制會將結果集分割為 2006-01-01 (MINVALUE group) 、日期等於或晚于 2006-01-01 (2006-01-01 group) 的專案，以及沒有日期 (**Null** 群組) 的專案。</span><span class="sxs-lookup"><span data-stu-id="c1827-128">For example, a range limit of '2006-01-01' for the [System.DateCreated](../properties/props-system-datecreated.md) property divides the result set into items with dates before 2006-01-01 (MINVALUE group), items with dates on or after 2006-01-01 (2006-01-01 group), and items with no date (**NULL** group).</span></span>

<span data-ttu-id="c1827-129">在每個群組內，依預設會依 [群組依據] 資料行中的值來排序結果。</span><span class="sxs-lookup"><span data-stu-id="c1827-129">Within each group, the results are sorted by the values in the GROUP ON column by default.</span></span> <span data-ttu-id="c1827-130">選擇性的 [ORDER BY](-search-sql-orderby.md) 子句可以包含 ASC 的方向規範，以遞增 (低至高) 或 DESC (高至低) ，而且 [GROUP BY 子句中的順序](-search-sql-orderingroup.md) 可以使用不同的規則排序每個群組。</span><span class="sxs-lookup"><span data-stu-id="c1827-130">The optional [ORDER BY](-search-sql-orderby.md) clause can contain a direction specifier of either ASC for ascending (low to high) or DESC for descending (high to low), and the [ORDER IN GROUP BY](-search-sql-orderingroup.md) clause can order each group using different rules.</span></span> <span data-ttu-id="c1827-131">如需詳細資訊，請參閱下方的 [訂購群組](#ordering-groups) 一節。</span><span class="sxs-lookup"><span data-stu-id="c1827-131">See the [Ordering Groups](#ordering-groups) section below for more information.</span></span>

## <a name="group-ranges"></a><span data-ttu-id="c1827-132">群組範圍</span><span class="sxs-lookup"><span data-stu-id="c1827-132">Group Ranges</span></span>

<span data-ttu-id="c1827-133">下表將示範如何根據範圍限制將結果分成群組：</span><span class="sxs-lookup"><span data-stu-id="c1827-133">The following table demonstrates how results are divided into groups based the range limits:</span></span>



| <span data-ttu-id="c1827-134">範例 (<column> \[ 群組範圍 \]) </span><span class="sxs-lookup"><span data-stu-id="c1827-134">Example (<column> \[group ranges\])</span></span>        | <span data-ttu-id="c1827-135">結果</span><span class="sxs-lookup"><span data-stu-id="c1827-135">Result</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1827-136">System. Size \[ 1000、5000\]</span><span class="sxs-lookup"><span data-stu-id="c1827-136">System.Size \[1000, 5000\]</span></span>                       | <span data-ttu-id="c1827-137">結果會分成四個 bucket： **MINVALUE**： Size < 1000</span><span class="sxs-lookup"><span data-stu-id="c1827-137">Results are grouped into four buckets: **MINVALUE**: Size < 1000</span></span><br/> <span data-ttu-id="c1827-138">**1000：** 1000 <= Size < 5000</span><span class="sxs-lookup"><span data-stu-id="c1827-138">**1000:** 1000 <= Size < 5000</span></span><br/> <span data-ttu-id="c1827-139">**5000：** 大小 >= 5000</span><span class="sxs-lookup"><span data-stu-id="c1827-139">**5000:** Size >= 5000</span></span><br/> <span data-ttu-id="c1827-140">**Null：** 沒有大小的值</span><span class="sxs-lookup"><span data-stu-id="c1827-140">**NULL:** No value for Size</span></span><br/>                                                                      |
| <span data-ttu-id="c1827-141">System. Author \[ ( ' ) ，在 ( ' r ' ) \]</span><span class="sxs-lookup"><span data-stu-id="c1827-141">System.Author \[BEFORE('m'),AFTER('r')\]</span></span>         | <span data-ttu-id="c1827-142">結果會分成四個值區： **MINVALUE：** Author "m" 之前 < 字元</span><span class="sxs-lookup"><span data-stu-id="c1827-142">Results are grouped into four buckets: **MINVALUE:** Author < character before "m"</span></span><br/> <span data-ttu-id="c1827-143">**m：** "m" 之前的字元 <= "r" 之後的作者 < 字元</span><span class="sxs-lookup"><span data-stu-id="c1827-143">**m:** character before "m" <= Author < character after "r"</span></span><br/> <span data-ttu-id="c1827-144">**r：** "r" 之後的字元 <= Author</span><span class="sxs-lookup"><span data-stu-id="c1827-144">**r:** character after "r" <= Author</span></span><br/> <span data-ttu-id="c1827-145">**Null：** 沒有作者的值</span><span class="sxs-lookup"><span data-stu-id="c1827-145">**NULL:** No value for Author</span></span><br/>      |
| <span data-ttu-id="c1827-146">System. Author \[ MINVALUE/' a to l '，"m"/m 至 z '\]</span><span class="sxs-lookup"><span data-stu-id="c1827-146">System.Author \[MINVALUE/'a to l',"m"/'m to z'\]</span></span> | <span data-ttu-id="c1827-147">結果會分成三個值區： **a 到 l：** Author < "m"</span><span class="sxs-lookup"><span data-stu-id="c1827-147">Results are grouped into three buckets: **a to l:** Author < "m"</span></span><br/> <span data-ttu-id="c1827-148">**m 至 z：** "m" <= Author</span><span class="sxs-lookup"><span data-stu-id="c1827-148">**m to z:** "m" <= Author</span></span> <br/> <span data-ttu-id="c1827-149">**Null：** 沒有作者的值</span><span class="sxs-lookup"><span data-stu-id="c1827-149">**NULL:** No value for Author</span></span><br/>                                                                                                               |
| <span data-ttu-id="c1827-150">System. DateCreated \[ ' 2005-1-01 '，' 2006-6-01 '\]</span><span class="sxs-lookup"><span data-stu-id="c1827-150">System.DateCreated \['2005-1-01','2006-6-01'\]</span></span>   | <span data-ttu-id="c1827-151">結果會分成四個 bucket：</span><span class="sxs-lookup"><span data-stu-id="c1827-151">Results are grouped into four buckets:</span></span><br/> <span data-ttu-id="c1827-152">**MINVALUE：** DateCreated < 2005-1-01</span><span class="sxs-lookup"><span data-stu-id="c1827-152">**MINVALUE:** DateCreated < 2005-1-01</span></span><br/> <span data-ttu-id="c1827-153">**2005-1-01：** 2005-1-01 <= DateCreated < 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="c1827-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span></span><br/> <span data-ttu-id="c1827-154">**2006-1-01：** DateCreated >= 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="c1827-154">**2006-1-01:** DateCreated >= 2006-6-01</span></span><br/> <span data-ttu-id="c1827-155">**Null：** DateCreated 沒有任何值</span><span class="sxs-lookup"><span data-stu-id="c1827-155">**NULL:** No value for DateCreated</span></span><br/> |



 

 

> [!IMPORTANT]
>
> <span data-ttu-id="c1827-156">錯誤： `GROUP ON System.Author['m','z','a']`</span><span class="sxs-lookup"><span data-stu-id="c1827-156">Incorrect: `GROUP ON System.Author['m','z','a']`</span></span>
>
> <span data-ttu-id="c1827-157">正確： `GROUP ON System.Author['a','m','z']`</span><span class="sxs-lookup"><span data-stu-id="c1827-157">Correct: `GROUP ON System.Author['a','m','z']`</span></span>

 

 

## <a name="labeling-groups"></a><span data-ttu-id="c1827-158">標記群組</span><span class="sxs-lookup"><span data-stu-id="c1827-158">Labeling Groups</span></span>

<span data-ttu-id="c1827-159">若要改善可讀性，您可以使用下列語法來標記群組：</span><span class="sxs-lookup"><span data-stu-id="c1827-159">To improve readability, you can label groups using the following syntax:</span></span>


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



<span data-ttu-id="c1827-160">標籤會與範圍限制分隔，並以斜線標示，並以單引號括住。</span><span class="sxs-lookup"><span data-stu-id="c1827-160">The label is separated from the range limit with a slash mark and is enclosed in single quotation marks.</span></span> <span data-ttu-id="c1827-161">如果您未指定標籤，組名就是範圍限制字串。</span><span class="sxs-lookup"><span data-stu-id="c1827-161">If you do not specify a label, the group name is the range limit string.</span></span>

<span data-ttu-id="c1827-162">以下是標籤群組的範例：</span><span class="sxs-lookup"><span data-stu-id="c1827-162">The following is an example of labeling groups:</span></span>


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



<span data-ttu-id="c1827-163">在 Windows 7 或更新版本中，您也可以使用一般的 \[ 其他 \] 標籤來合併多個群組範圍。</span><span class="sxs-lookup"><span data-stu-id="c1827-163">In Windows 7 or later, you can also use a generic \[OTHER\] label to combine multiple grouping ranges.</span></span> <span data-ttu-id="c1827-164">所有使用此標籤識別的群組所產生的結果，將會合並成一個具有此標籤的群組。</span><span class="sxs-lookup"><span data-stu-id="c1827-164">Results from all groups identified with this label will be combined into one group with this label.</span></span> <span data-ttu-id="c1827-165">此結果群組會在所有其他群組之後傳回，但 **Null** 群組除外。</span><span class="sxs-lookup"><span data-stu-id="c1827-165">This group of results is returned after all other groups except for the **NULL** group.</span></span> <span data-ttu-id="c1827-166">**Null** 群組包含沒有指定屬性值之專案的結果。</span><span class="sxs-lookup"><span data-stu-id="c1827-166">The **NULL** group contains results for items that do not have a value for the specified property.</span></span> <span data-ttu-id="c1827-167">在 Windows 7 之前， \[ 其他 \] 標籤的處理方式就像任何其他群組標籤一樣。</span><span class="sxs-lookup"><span data-stu-id="c1827-167">Prior to Windows 7 the \[OTHER\] label is treated like any other group label.</span></span>

<span data-ttu-id="c1827-168">下列程式碼是 \[ \] 針對在 Windows 7 或更新版本中建立的群組使用另一個標籤的範例：</span><span class="sxs-lookup"><span data-stu-id="c1827-168">The following code is an example of using the \[OTHER\] label for groups that would be created in Windows 7 or later:</span></span>


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



<span data-ttu-id="c1827-169">下表顯示在 Windows 7 或更新版本中，先前分組程式碼所建立的群組。</span><span class="sxs-lookup"><span data-stu-id="c1827-169">The following table shows the groups that would be created by the preceding grouping code in Windows 7 or later.</span></span>



| <span data-ttu-id="c1827-170">Group</span><span class="sxs-lookup"><span data-stu-id="c1827-170">Group</span></span>     | <span data-ttu-id="c1827-171">System.Author</span><span class="sxs-lookup"><span data-stu-id="c1827-171">System.Author</span></span> | <span data-ttu-id="c1827-172">System.string</span><span class="sxs-lookup"><span data-stu-id="c1827-172">System.FileName</span></span> |
|-----------|---------------|-----------------|
| <span data-ttu-id="c1827-173">0</span><span class="sxs-lookup"><span data-stu-id="c1827-173">0</span></span>         | <span data-ttu-id="c1827-174">1Bill</span><span class="sxs-lookup"><span data-stu-id="c1827-174">1Bill</span></span>         | <span data-ttu-id="c1827-175">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-175">Lorem.docx</span></span>      |
| <span data-ttu-id="c1827-176">Q</span><span class="sxs-lookup"><span data-stu-id="c1827-176">Q</span></span>         | <span data-ttu-id="c1827-177">女王</span><span class="sxs-lookup"><span data-stu-id="c1827-177">Queen</span></span>         | <span data-ttu-id="c1827-178">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-178">Ipsum.docx</span></span>      |
|           | <span data-ttu-id="c1827-179">Robin</span><span class="sxs-lookup"><span data-stu-id="c1827-179">Robin</span></span>         | <span data-ttu-id="c1827-180">dolor.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-180">dolor.docx</span></span>      |
| <span data-ttu-id="c1827-181">Y</span><span class="sxs-lookup"><span data-stu-id="c1827-181">Y</span></span>         | <span data-ttu-id="c1827-182">Zara</span><span class="sxs-lookup"><span data-stu-id="c1827-182">Zara</span></span>          | <span data-ttu-id="c1827-183">amet.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-183">amet.docx</span></span>       |
| <span data-ttu-id="c1827-184">\[其他\]</span><span class="sxs-lookup"><span data-stu-id="c1827-184">\[OTHER\]</span></span> | <span data-ttu-id="c1827-185">Abner</span><span class="sxs-lookup"><span data-stu-id="c1827-185">Abner</span></span>         | <span data-ttu-id="c1827-186">nonummy.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-186">nonummy.docx</span></span>    |
|           | <span data-ttu-id="c1827-187">Bob</span><span class="sxs-lookup"><span data-stu-id="c1827-187">Bob</span></span>           | <span data-ttu-id="c1827-188">laoreet.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-188">laoreet.docx</span></span>    |
|           | <span data-ttu-id="c1827-189">Xaria</span><span class="sxs-lookup"><span data-stu-id="c1827-189">Xaria</span></span>         | <span data-ttu-id="c1827-190">magna.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-190">magna.docx</span></span>      |
| <span data-ttu-id="c1827-191">**NULL**</span><span class="sxs-lookup"><span data-stu-id="c1827-191">**NULL**</span></span>  |               | <span data-ttu-id="c1827-192">aliquam.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-192">aliquam.docx</span></span>    |



 

## <a name="ordering-groups"></a><span data-ttu-id="c1827-193">排序群組</span><span class="sxs-lookup"><span data-stu-id="c1827-193">Ordering Groups</span></span>

<span data-ttu-id="c1827-194">有三種方式可排序群組中的專案：</span><span class="sxs-lookup"><span data-stu-id="c1827-194">There are three ways to order items in groups:</span></span>

-   <span data-ttu-id="c1827-195">預設排序：如果未指定，則會依 [群組依據] 資料行中的值，以遞增順序來排序結果。</span><span class="sxs-lookup"><span data-stu-id="c1827-195">Default ordering: If you do not specify otherwise, the results are ordered by the values in the GROUP ON column, in ascending order.</span></span>
-   <span data-ttu-id="c1827-196">ORDER BY：您可以在 ORDER BY 子句中指定遞減順序。</span><span class="sxs-lookup"><span data-stu-id="c1827-196">ORDER BY: You can specify descending order in an ORDER BY clause.</span></span> <span data-ttu-id="c1827-197">您必須依 [群組依據] 資料行來排序結果。</span><span class="sxs-lookup"><span data-stu-id="c1827-197">You must order the results by the GROUP ON column.</span></span>
-   <span data-ttu-id="c1827-198">ORDER IN GROUP BY：您可以為每個群組指定不同的順序。</span><span class="sxs-lookup"><span data-stu-id="c1827-198">ORDER IN GROUP BY: You can specify a different order for each group.</span></span> <span data-ttu-id="c1827-199">如果您在 [[系統](../properties/props-system-kind.md)] 上分組，您可以依 [系統]、[[作者](../properties/props-system-author.md)] 和 [音樂] 將檔[排序。](../properties/props-system-music-artist.md)</span><span class="sxs-lookup"><span data-stu-id="c1827-199">If you group on [System.Kind](../properties/props-system-kind.md), you can order documents by [System.Author](../properties/props-system-author.md) and music by [System.Music.Artist](../properties/props-system-music-artist.md).</span></span>

<span data-ttu-id="c1827-200">如需排序結果的詳細資訊，請參閱 [ORDER By 子句](-search-sql-orderby.md) 和 [GROUP 子句參考頁面中的 order IN](-search-sql-orderingroup.md) 。</span><span class="sxs-lookup"><span data-stu-id="c1827-200">For more information on ordering results, see the [ORDER BY Clause](-search-sql-orderby.md) and [ORDER IN GROUP Clause](-search-sql-orderingroup.md) reference pages.</span></span>

## <a name="nesting-groups"></a><span data-ttu-id="c1827-201">嵌套群組</span><span class="sxs-lookup"><span data-stu-id="c1827-201">Nesting Groups</span></span>

<span data-ttu-id="c1827-202">您可以使用多個 GROUP ON 子句來嵌套群組。</span><span class="sxs-lookup"><span data-stu-id="c1827-202">You can nest groups with multiple GROUP ON clauses.</span></span> <span data-ttu-id="c1827-203">查詢中指定的順序會直接反映在輸出群組階層中，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="c1827-203">The order specified in the query is directly reflected in the output group hierarchy, as shown in the following example.</span></span>


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| <span data-ttu-id="c1827-204">System.string</span><span class="sxs-lookup"><span data-stu-id="c1827-204">System.Kind</span></span>    | <span data-ttu-id="c1827-205">System.Author</span><span class="sxs-lookup"><span data-stu-id="c1827-205">System.Author</span></span> | <span data-ttu-id="c1827-206">System. DateCreated</span><span class="sxs-lookup"><span data-stu-id="c1827-206">System.DateCreated</span></span> |
|----------------|---------------|--------------------|
| <span data-ttu-id="c1827-207">文件</span><span class="sxs-lookup"><span data-stu-id="c1827-207">documents</span></span>      | <span data-ttu-id="c1827-208">威拉</span><span class="sxs-lookup"><span data-stu-id="c1827-208">Willa</span></span>         | <span data-ttu-id="c1827-209">2006-01-02</span><span class="sxs-lookup"><span data-stu-id="c1827-209">2006-01-02</span></span>         |
|                |               | <span data-ttu-id="c1827-210">2006-01-05</span><span class="sxs-lookup"><span data-stu-id="c1827-210">2006-01-05</span></span>         |
|                | <span data-ttu-id="c1827-211">Zara</span><span class="sxs-lookup"><span data-stu-id="c1827-211">Zara</span></span>          | <span data-ttu-id="c1827-212">2007-06-02</span><span class="sxs-lookup"><span data-stu-id="c1827-212">2007-06-02</span></span>         |
|                |               | <span data-ttu-id="c1827-213">2007-09-10</span><span class="sxs-lookup"><span data-stu-id="c1827-213">2007-09-10</span></span>         |
| <span data-ttu-id="c1827-214">通訊</span><span class="sxs-lookup"><span data-stu-id="c1827-214">communications</span></span> | <span data-ttu-id="c1827-215">Abner</span><span class="sxs-lookup"><span data-stu-id="c1827-215">Abner</span></span>         | <span data-ttu-id="c1827-216">2006-04-16</span><span class="sxs-lookup"><span data-stu-id="c1827-216">2006-04-16</span></span>         |
|                | <span data-ttu-id="c1827-217">珍</span><span class="sxs-lookup"><span data-stu-id="c1827-217">Jean</span></span>          | <span data-ttu-id="c1827-218">2007-02-20</span><span class="sxs-lookup"><span data-stu-id="c1827-218">2007-02-20</span></span>         |
|                | <span data-ttu-id="c1827-219">威拉</span><span class="sxs-lookup"><span data-stu-id="c1827-219">Willa</span></span>         | <span data-ttu-id="c1827-220">2006-10-15</span><span class="sxs-lookup"><span data-stu-id="c1827-220">2006-10-15</span></span>         |
|                | <span data-ttu-id="c1827-221">Zara</span><span class="sxs-lookup"><span data-stu-id="c1827-221">Zara</span></span>          | <span data-ttu-id="c1827-222">2008-01-02</span><span class="sxs-lookup"><span data-stu-id="c1827-222">2008-01-02</span></span>         |



 

 

## <a name="grouping-on-vector-properties"></a><span data-ttu-id="c1827-223">向量屬性上的分組</span><span class="sxs-lookup"><span data-stu-id="c1827-223">Grouping on Vector Properties</span></span>

<span data-ttu-id="c1827-224">在向量屬性、可以同時包含一或多個值的屬性上進行分組，預設會個別比較向量值。</span><span class="sxs-lookup"><span data-stu-id="c1827-224">Grouping on vector properties, properties that can contain one or more values simultaneously, compares the vector values individually by default.</span></span> <span data-ttu-id="c1827-225">例如，如果有一份檔，Lorem.docx，並以 system.string 屬性為 "Theresa;Zara "和另一個檔，Ipsum.docx，將 Author 屬性設為" Zara "，查詢會傳回兩個群組中的結果集，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c1827-225">For example, if there is one document, Lorem.docx, with the System.Author property as "Theresa;Zara" and another document, Ipsum.docx, with the System.Author property as "Zara", the query returns the result set in two groups as shown here:</span></span>


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| <span data-ttu-id="c1827-226">System.Author</span><span class="sxs-lookup"><span data-stu-id="c1827-226">System.Author</span></span> | <span data-ttu-id="c1827-227">System.string</span><span class="sxs-lookup"><span data-stu-id="c1827-227">System.FileName</span></span> |
|---------------|-----------------|
| <span data-ttu-id="c1827-228">德蕾莎</span><span class="sxs-lookup"><span data-stu-id="c1827-228">Theresa</span></span>       | <span data-ttu-id="c1827-229">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-229">Lorem.docx</span></span>      |
| <span data-ttu-id="c1827-230">Zara</span><span class="sxs-lookup"><span data-stu-id="c1827-230">Zara</span></span>          | <span data-ttu-id="c1827-231">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-231">Lorem.docx</span></span>      |
|               | <span data-ttu-id="c1827-232">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="c1827-232">Ipsum.docx</span></span>      |



 

<span data-ttu-id="c1827-233">如您所見，vector 屬性的分組會傳回重複的資料列。</span><span class="sxs-lookup"><span data-stu-id="c1827-233">As you can see, grouping on vector properties returns duplicate rows.</span></span> <span data-ttu-id="c1827-234">Lorem.docx 會出現兩次，因為它有兩個作者。</span><span class="sxs-lookup"><span data-stu-id="c1827-234">Lorem.docx appears twice because it has two authors.</span></span>

 

## <a name="more-examples"></a><span data-ttu-id="c1827-235">更多範例</span><span class="sxs-lookup"><span data-stu-id="c1827-235">More Examples</span></span>


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a><span data-ttu-id="c1827-236">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1827-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1827-237">彙總函式</span><span class="sxs-lookup"><span data-stu-id="c1827-237">Aggregate Functions</span></span>](-search-sql-aggregates.md)
</dt> <dt>

[<span data-ttu-id="c1827-238">ORDER BY 子句</span><span class="sxs-lookup"><span data-stu-id="c1827-238">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> <dt>

[<span data-ttu-id="c1827-239">ORDER IN GROUP 子句</span><span class="sxs-lookup"><span data-stu-id="c1827-239">ORDER IN GROUP Clause</span></span>](-search-sql-orderingroup.md)
</dt> </dl>

 

 
