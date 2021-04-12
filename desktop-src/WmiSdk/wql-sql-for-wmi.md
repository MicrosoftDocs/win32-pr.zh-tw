---
description: WMI 查詢語言 (WQL) 是美國國家標準局結構化查詢語言 (SQL)  (ANSI SQL) &郵件的子集， \# 但不含次要語義變更。 下表列出 WQL 關鍵字。
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL for WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192182"
---
# <a name="wql-sql-for-wmi"></a><span data-ttu-id="67395-104">WQL (SQL for WMI)</span><span class="sxs-lookup"><span data-stu-id="67395-104">WQL (SQL for WMI)</span></span>

<span data-ttu-id="67395-105">WMI 查詢語言 (WQL) 是美國國家標準局結構化查詢語言 (SQL)  (ANSI SQL) 的子集，其中包含次要語義變更。</span><span class="sxs-lookup"><span data-stu-id="67395-105">The WMI Query Language (WQL) is a subset of the American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes.</span></span> <span data-ttu-id="67395-106">下表列出 WQL 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="67395-106">The following table lists the WQL keywords.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67395-107">WQL 關鍵字</span><span class="sxs-lookup"><span data-stu-id="67395-107">WQL keyword</span></span></th>
<th><span data-ttu-id="67395-108">意義</span><span class="sxs-lookup"><span data-stu-id="67395-108">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67395-109">AND</span><span class="sxs-lookup"><span data-stu-id="67395-109">AND</span></span><br/></td>
<td><span data-ttu-id="67395-110">結合兩個布林運算式，並在兩個運算式都<strong>為 true</strong>時傳回<strong>true</strong> 。</span><span class="sxs-lookup"><span data-stu-id="67395-110">Combines two Boolean expressions, and returns <strong>TRUE</strong> when both expressions are <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67395-111"><a href="associators-of-statement.md">ASSOCIATORS OF</a></span><span class="sxs-lookup"><span data-stu-id="67395-111"><a href="associators-of-statement.md">ASSOCIATORS OF</a></span></span></td>
<td><span data-ttu-id="67395-112">抓取與來源實例相關聯的所有實例。</span><span class="sxs-lookup"><span data-stu-id="67395-112">Retrieves all instances that are associated with a source instance.</span></span><br/> <span data-ttu-id="67395-113">將此語句與架構查詢和資料查詢搭配使用。</span><span class="sxs-lookup"><span data-stu-id="67395-113">Use this statement with schema queries and data queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67395-114"><a href="--class-identifier.md">__CLASS</a></span><span class="sxs-lookup"><span data-stu-id="67395-114"><a href="--class-identifier.md">__CLASS</a></span></span></td>
<td><span data-ttu-id="67395-115">參考查詢中物件的類別。</span><span class="sxs-lookup"><span data-stu-id="67395-115">References the class of the object in a query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67395-116">FROM</span><span class="sxs-lookup"><span data-stu-id="67395-116">FROM</span></span><br/></td>
<td><span data-ttu-id="67395-117">指定包含 SELECT 語句中所列屬性的類別。</span><span class="sxs-lookup"><span data-stu-id="67395-117">Specifies the class that contains the properties listed in a SELECT statement.</span></span> <span data-ttu-id="67395-118">Windows Management Instrumentation (WMI) 一次只支援一個類別的資料查詢。</span><span class="sxs-lookup"><span data-stu-id="67395-118">Windows Management Instrumentation (WMI) supports data queries from only one class at a time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67395-119"><a href="group-clause.md">GROUP 子句</a></span><span class="sxs-lookup"><span data-stu-id="67395-119"><a href="group-clause.md">GROUP Clause</a></span></span></td>
<td><span data-ttu-id="67395-120">讓 WMI 產生一個通知來表示事件群組。</span><span class="sxs-lookup"><span data-stu-id="67395-120">Causes WMI to generate one notification to represent a group of events.</span></span><br/> <span data-ttu-id="67395-121">使用這個子句搭配事件查詢。</span><span class="sxs-lookup"><span data-stu-id="67395-121">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67395-122"><a href="having-clause.md">HAVING</a></span><span class="sxs-lookup"><span data-stu-id="67395-122"><a href="having-clause.md">HAVING</a></span></span></td>
<td><span data-ttu-id="67395-123">篩選在 in <a href="within-clause.md">子句</a>中指定的分組間隔期間所收到的事件。</span><span class="sxs-lookup"><span data-stu-id="67395-123">Filters the events that are received during the grouping interval that is specified in the <a href="within-clause.md">WITHIN clause</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67395-124"><a href="wql-operators.md">IS</a></span><span class="sxs-lookup"><span data-stu-id="67395-124"><a href="wql-operators.md">IS</a></span></span></td>
<td><span data-ttu-id="67395-125">搭配 NOT 和 <strong>Null</strong>使用的比較運算子。</span><span class="sxs-lookup"><span data-stu-id="67395-125">Comparison operator used with NOT and <strong>NULL</strong>.</span></span> <span data-ttu-id="67395-126">此語句的語法如下：</span><span class="sxs-lookup"><span data-stu-id="67395-126">The syntax for this statement is the following:</span></span><br/> <span data-ttu-id="67395-127">是 [NOT] <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="67395-127">IS [NOT] <strong>NULL</strong></span></span><br/> <span data-ttu-id="67395-128"> (，其中不是選擇性的) </span><span class="sxs-lookup"><span data-stu-id="67395-128">(where NOT is optional)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67395-129"><a href="wql-operators.md">ISA</a></span><span class="sxs-lookup"><span data-stu-id="67395-129"><a href="wql-operators.md">ISA</a></span></span></td>
<td><span data-ttu-id="67395-130">將查詢套用至指定類別之子類別的運算子。</span><span class="sxs-lookup"><span data-stu-id="67395-130">Operator that applies a query to the subclasses of a specified class.</span></span> <span data-ttu-id="67395-131">如需詳細資訊，請參閱 <a href="isa-operator-for-event-queries.md">適用于事件查詢的 Isa 操作員</a>、 <a href="isa-operator-for-data-queries.md">資料查詢的 isa 運算子</a>，以及 <a href="isa-operator-for-schema-queries.md">用於架構查詢的 isa 運算子</a>。</span><span class="sxs-lookup"><span data-stu-id="67395-131">For more information, see <a href="isa-operator-for-event-queries.md">ISA Operator for Event Queries</a>, <a href="isa-operator-for-data-queries.md">ISA Operator for Data Queries</a>, and <a href="isa-operator-for-schema-queries.md">ISA Operator for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67395-132">KEYSONLY</span><span class="sxs-lookup"><span data-stu-id="67395-132">KEYSONLY</span></span><br/></td>
<td><span data-ttu-id="67395-133">用於查詢 <a href="references-of-statement.md">的參考</a> 和 <a href="associators-of-statement.md">associators of</a> ，以確保產生的實例只會填入實例的索引鍵，進而減少呼叫的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="67395-133">Used in <a href="references-of-statement.md">REFERENCES OF</a> and <a href="associators-of-statement.md">ASSOCIATORS OF</a> queries to ensure that the resulting instances are only populated with the keys of the instances, which reduces the overhead of the call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67395-134"><a href="wql-operators.md">LIKE</a></span><span class="sxs-lookup"><span data-stu-id="67395-134"><a href="wql-operators.md">LIKE</a></span></span></td>
<td><span data-ttu-id="67395-135">判斷指定的字元字串是否符合指定之模式的運算子。</span><span class="sxs-lookup"><span data-stu-id="67395-135">Operator that determines whether or not a given character string matches a specified pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67395-136">NOT</span><span class="sxs-lookup"><span data-stu-id="67395-136">NOT</span></span><br/></td>
<td><span data-ttu-id="67395-137">在 WQL SELECT 查詢中使用的比較運算子，例如：</span><span class="sxs-lookup"><span data-stu-id="67395-137">Comparison operator that use in a WQL SELECT query, for example:</span></span><br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67395-138"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="67395-138"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="67395-139">指出物件沒有明確指派的值。</span><span class="sxs-lookup"><span data-stu-id="67395-139">Indicates an object does not have an explicitly assigned value.</span></span> <span data-ttu-id="67395-140"><strong>Null</strong> 不等於零 (0) 或空白。</span><span class="sxs-lookup"><span data-stu-id="67395-140"><strong>NULL</strong> is not equivalent to zero (0) or blank.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67395-141">OR</span><span class="sxs-lookup"><span data-stu-id="67395-141">OR</span></span><br/></td>
<td><span data-ttu-id="67395-142">結合兩個條件。</span><span class="sxs-lookup"><span data-stu-id="67395-142">Combines two conditions.</span></span><br/> <span data-ttu-id="67395-143">當在語句中使用一個以上的邏輯運算子時，OR 運算子會在 AND 運算子之後評估。</span><span class="sxs-lookup"><span data-stu-id="67395-143">When more than one logical operator is used in a statement, the OR operators are evaluated after the AND operators.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67395-144"><a href="references-of-statement.md">的參考</a></span><span class="sxs-lookup"><span data-stu-id="67395-144"><a href="references-of-statement.md">REFERENCES OF</a></span></span></td>
<td><span data-ttu-id="67395-145">抓取參考特定來源實例的所有關聯實例。</span><span class="sxs-lookup"><span data-stu-id="67395-145">Retrieves all association instances that refer to a specific source instance.</span></span> <span data-ttu-id="67395-146">將此語句與架構和資料查詢搭配使用。</span><span class="sxs-lookup"><span data-stu-id="67395-146">Use this statement with schema and data queries.</span></span> <span data-ttu-id="67395-147">語句的 <a href="references-of-statement.md">參考</a> 類似于語句的 <a href="associators-of-statement.md">associators of</a> 。</span><span class="sxs-lookup"><span data-stu-id="67395-147">The <a href="references-of-statement.md">REFERENCES OF</a> statement is similar to the <a href="associators-of-statement.md">ASSOCIATORS OF</a> statement.</span></span> <span data-ttu-id="67395-148">但是，它不會取出端點實例;它會捕獲關聯實例。</span><span class="sxs-lookup"><span data-stu-id="67395-148">However, it does not retrieve endpoint instances; it retrieves the association instances.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67395-149">SELECT</span><span class="sxs-lookup"><span data-stu-id="67395-149">SELECT</span></span><br/></td>
<td><span data-ttu-id="67395-150">指定用於查詢的屬性。</span><span class="sxs-lookup"><span data-stu-id="67395-150">Specifies the properties that are used in a query.</span></span><br/> <span data-ttu-id="67395-151">如需詳細資訊，請參閱 <a href="select-statement-for-data-queries.md">資料查詢的 Select 語句</a>、 <a href="select-statement-for-event-queries.md">事件查詢的 select 語句</a>，或 <a href="select-statement-for-schema-queries.md">架構查詢的 select 語句</a>。</span><span class="sxs-lookup"><span data-stu-id="67395-151">For more information, see <a href="select-statement-for-data-queries.md">SELECT Statement for Data Queries</a>, <a href="select-statement-for-event-queries.md">SELECT Statement for Event Queries</a>, or <a href="select-statement-for-schema-queries.md">SELECT Statement for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67395-152"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="67395-152"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="67395-153">評估為-1 (減一) 的布林運算子。</span><span class="sxs-lookup"><span data-stu-id="67395-153">Boolean operator that evaluates to -1 (minus one).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67395-154"><a href="where-clause.md">WHERE</a></span><span class="sxs-lookup"><span data-stu-id="67395-154"><a href="where-clause.md">WHERE</a></span></span></td>
<td><span data-ttu-id="67395-155">縮小資料、事件或架構查詢的範圍。</span><span class="sxs-lookup"><span data-stu-id="67395-155">Narrows the scope of a data, event, or schema query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67395-156"><a href="within-clause.md">WITHIN</a></span><span class="sxs-lookup"><span data-stu-id="67395-156"><a href="within-clause.md">WITHIN</a></span></span></td>
<td><span data-ttu-id="67395-157">指定輪詢或分組間隔。</span><span class="sxs-lookup"><span data-stu-id="67395-157">Specifies a polling or grouping interval.</span></span><br/> <span data-ttu-id="67395-158">使用這個子句搭配事件查詢。</span><span class="sxs-lookup"><span data-stu-id="67395-158">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67395-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="67395-159">FALSE</span></span><br/></td>
<td><span data-ttu-id="67395-160">判斷值為 0 (零) 的布林運算子。</span><span class="sxs-lookup"><span data-stu-id="67395-160">Boolean operator that evaluates to 0 (zero).</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="67395-161">使用 WQL 關鍵字字作為物件名稱，可能會導致無法剖析查詢，即使查詢未發生錯誤，也是如此。</span><span class="sxs-lookup"><span data-stu-id="67395-161">Using a WQL key word as an object name can result in a query that cannot be parsed even when the query compiles without error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="67395-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="67395-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67395-163">WQL 運算子</span><span class="sxs-lookup"><span data-stu-id="67395-163">WQL Operators</span></span>](wql-operators.md)
</dt> <dt>

[<span data-ttu-id="67395-164">WQL-支援的日期格式</span><span class="sxs-lookup"><span data-stu-id="67395-164">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
</dt> <dt>

[<span data-ttu-id="67395-165">WQL-支援的時間格式</span><span class="sxs-lookup"><span data-stu-id="67395-165">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)
</dt> </dl>

 

 




