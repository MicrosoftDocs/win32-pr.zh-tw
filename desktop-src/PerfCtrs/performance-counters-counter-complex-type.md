---
description: 定義計數器。
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: 計數器複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d591d4c23b626eaf2e2bfb10b528ff7c054507df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993136"
---
# <a name="counter-complex-type"></a><span data-ttu-id="42d70-103">計數器複雜類型</span><span class="sxs-lookup"><span data-stu-id="42d70-103">counter Complex Type</span></span>

<span data-ttu-id="42d70-104">定義計數器。</span><span class="sxs-lookup"><span data-stu-id="42d70-104">Defines a counter.</span></span>

``` syntax
<xs:complexType name="counter">
    <xs:choice
        minOccurs="0"
        maxOccurs="1"
    >
        <xs:element name="counterAttributes"
            type="man:counterAttributes"
        >
            <xs:key name="uniqueCounterAttributeName">
                <xs:selector
                    xpath="./man:counterAttribute"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="id"
        type="man:UInt32Type"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="optional"
     />
    <xs:attribute name="type"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="perf_counter_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer"
                 />
                <xs:enumeration
                    value="perf_counter_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_large_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_100ns_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_obj_time_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_bulk_count"
                 />
                <xs:enumeration
                    value="perf_counter_text"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_sample_fraction"
                 />
                <xs:enumeration
                    value="perf_sample_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer_inv"
                 />
                <xs:enumeration
                    value="perf_sample_base"
                 />
                <xs:enumeration
                    value="perf_average_timer"
                 />
                <xs:enumeration
                    value="perf_average_base"
                 />
                <xs:enumeration
                    value="perf_average_bulk"
                 />
                <xs:enumeration
                    value="perf_obj_time_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_base"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_large_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_raw_base"
                 />
                <xs:enumeration
                    value="perf_large_raw_base"
                 />
                <xs:enumeration
                    value="perf_elapsed_time"
                 />
                <xs:enumeration
                    value="perf_counter_delta"
                 />
                <xs:enumeration
                    value="perf_counter_large_delta"
                 />
                <xs:enumeration
                    value="perf_precision_system_timer"
                 />
                <xs:enumeration
                    value="perf_precision_100ns_timer"
                 />
                <xs:enumeration
                    value="perf_precision_object_timer"
                 />
                <xs:enumeration
                    value="perf_counter_composite"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="detailLevel"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="standard"
                 />
                <xs:enumeration
                    value="advanced"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale"
        use="optional"
        default="0"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:integer"
            >
                <xs:minInclusive
                    value="-10"
                 />
                <xs:maxInclusive
                    value="10"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="sum"
                 />
                <xs:enumeration
                    value="avg"
                 />
                <xs:enumeration
                    value="max"
                 />
                <xs:enumeration
                    value="min"
                 />
                <xs:enumeration
                    value="undefined"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="perfFreqID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="multiCounterID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="struct"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="field"
        type="man:CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="42d70-105">子元素</span><span class="sxs-lookup"><span data-stu-id="42d70-105">Child elements</span></span>



| <span data-ttu-id="42d70-106">元素</span><span class="sxs-lookup"><span data-stu-id="42d70-106">Element</span></span>               | <span data-ttu-id="42d70-107">類型</span><span class="sxs-lookup"><span data-stu-id="42d70-107">Type</span></span>                                                                                 | <span data-ttu-id="42d70-108">Description</span><span class="sxs-lookup"><span data-stu-id="42d70-108">Description</span></span>                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d70-109">**counterAttributes**</span><span class="sxs-lookup"><span data-stu-id="42d70-109">**counterAttributes**</span></span> | [<span data-ttu-id="42d70-110">**男人： counterAttributes**</span><span class="sxs-lookup"><span data-stu-id="42d70-110">**man:counterAttributes**</span></span>](performance-counters-counterattributes-complex-type.md) | <span data-ttu-id="42d70-111">列出指定如何在取用者應用程式中顯示計數器資料的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="42d70-111">Lists the unique attributes that specify how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="42d70-112">屬性</span><span class="sxs-lookup"><span data-stu-id="42d70-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="42d70-113">名稱</span><span class="sxs-lookup"><span data-stu-id="42d70-113">Name</span></span></th>
<th><span data-ttu-id="42d70-114">類型</span><span class="sxs-lookup"><span data-stu-id="42d70-114">Type</span></span></th>
<th><span data-ttu-id="42d70-115">Description</span><span class="sxs-lookup"><span data-stu-id="42d70-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d70-116">彙總 (aggregate)</span><span class="sxs-lookup"><span data-stu-id="42d70-116">aggregate</span></span></td>

<td><span data-ttu-id="42d70-117">如果<a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a>的<strong>實例</strong>屬性是 GlobalAggregate、multipleAggregate 或 globalAggregateHistory，則適用的彙總函式。</span><span class="sxs-lookup"><span data-stu-id="42d70-117">The aggregation function to apply if the <strong>instances</strong> attribute of <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> is globalAggregate, multipleAggregate, or globalAggregateHistory.</span></span> <span data-ttu-id="42d70-118">以下是您可以套用的可能彙總函式：</span><span class="sxs-lookup"><span data-stu-id="42d70-118">The following are the possible aggregation functions that you can apply:</span></span><br/> <dl> <span data-ttu-id="42d70-119"><dt><span id="max"></span><span id="MAX"></span>麥克斯</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-119"><dt><span id="max"></span><span id="MAX"></span>max</dt> </span></span><dd> <span data-ttu-id="42d70-120">傳回最大計數器值。</span><span class="sxs-lookup"><span data-stu-id="42d70-120">The maximum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="42d70-121"><dt><span id="min"></span><span id="MIN"></span>化</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span></span><dd> <span data-ttu-id="42d70-122">傳回最小計數器值。</span><span class="sxs-lookup"><span data-stu-id="42d70-122">The minimum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="42d70-123"><dt><span id="avg"></span><span id="AVG"></span>Avg</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-123"><dt><span id="avg"></span><span id="AVG"></span>avg</dt> </span></span><dd> <span data-ttu-id="42d70-124">傳回的平均計數器值。</span><span class="sxs-lookup"><span data-stu-id="42d70-124">The average counter value is returned.</span></span><br/> </dd> <span data-ttu-id="42d70-125"><dt><span id="sum"></span><span id="SUM"></span>和</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-125"><dt><span id="sum"></span><span id="SUM"></span>sum</dt> </span></span><dd> <span data-ttu-id="42d70-126">傳回計數器值的總和。</span><span class="sxs-lookup"><span data-stu-id="42d70-126">The sum of the counter values is returned.</span></span><br/> </dd> <span data-ttu-id="42d70-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>定義</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>undefined</dt> </span></span><dd> <span data-ttu-id="42d70-128">請勿匯總此計數器。</span><span class="sxs-lookup"><span data-stu-id="42d70-128">Do not aggregate this counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d70-129">baseID</span><span class="sxs-lookup"><span data-stu-id="42d70-129">baseID</span></span></td>
<td><span data-ttu-id="42d70-130"><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="42d70-130"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="42d70-131">相同計數器集合中另一個計數器的識別碼，其值用來計算這個計數器的值。</span><span class="sxs-lookup"><span data-stu-id="42d70-131">The identifier of another counter within the same counter set, whose value is used to calculate this counter's value.</span></span> <span data-ttu-id="42d70-132">下列計數器類型需要基底計數器：</span><span class="sxs-lookup"><span data-stu-id="42d70-132">The following counter types require a base counter:</span></span><br/> <dl> <span data-ttu-id="42d70-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span></span><dd> <span data-ttu-id="42d70-134">需要 PERF_AVERAGE_BASE 基底計數器。</span><span class="sxs-lookup"><span data-stu-id="42d70-134">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="42d70-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span></span><dd> <span data-ttu-id="42d70-136">需要 PERF_AVERAGE_BASE 基底計數器。</span><span class="sxs-lookup"><span data-stu-id="42d70-136">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="42d70-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span></span><dd> <span data-ttu-id="42d70-138">需要 PERF_COUNTER_MULTI_BASE 基底計數器。</span><span class="sxs-lookup"><span data-stu-id="42d70-138">Requires the PERF_COUNTER_MULTI_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="42d70-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="42d70-140">需要 PERF_LARGE_RAW_BASE 基底計數器。</span><span class="sxs-lookup"><span data-stu-id="42d70-140">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="42d70-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span></span><dd> <span data-ttu-id="42d70-142">需要 PERF_LARGE_RAW_BASE 基底計數器。</span><span class="sxs-lookup"><span data-stu-id="42d70-142">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="42d70-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="42d70-144">需要 PERF_RAW_BASE 基底計數器。</span><span class="sxs-lookup"><span data-stu-id="42d70-144">Requires the PERF_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="42d70-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span></span><dd> <span data-ttu-id="42d70-146">需要 PERF_SAMPLE_BASE 基底計數器。</span><span class="sxs-lookup"><span data-stu-id="42d70-146">Requires the PERF_SAMPLE_BASE base counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d70-147">defaultScale</span><span class="sxs-lookup"><span data-stu-id="42d70-147">defaultScale</span></span></td>

<td><span data-ttu-id="42d70-148">要套用至計數器值的縮放比例 (因數 \* 計數器值) 。</span><span class="sxs-lookup"><span data-stu-id="42d70-148">The scale factor to apply to the counter value (factor \* counter value).</span></span> <span data-ttu-id="42d70-149">如果未套用任何小數位數，則預設值為零。</span><span class="sxs-lookup"><span data-stu-id="42d70-149">The default is zero if no scale is applied.</span></span> <span data-ttu-id="42d70-150">有效的值範圍從10到 10 (0.0000000001 到 1000000000) 。</span><span class="sxs-lookup"><span data-stu-id="42d70-150">Valid values range from  10 to 10 (0.0000000001 to 1000000000).</span></span> <span data-ttu-id="42d70-151">如果此值為零，則小數位數值為1。如果這個值是1，則小數位數值為 10;如果這個值是1，則小數位數值為. 10;依此類推。</span><span class="sxs-lookup"><span data-stu-id="42d70-151">If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is  1, the scale value is .10; and so on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d70-152">description</span><span class="sxs-lookup"><span data-stu-id="42d70-152">description</span></span></td>
<td><span data-ttu-id="42d70-153"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="42d70-153"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="42d70-154">計數器的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="42d70-154">A short description of the counter.</span></span> <span data-ttu-id="42d70-155">如果計數器包含 <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> 屬性，您就不需要指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="42d70-155">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d70-156">detailLevel</span><span class="sxs-lookup"><span data-stu-id="42d70-156">detailLevel</span></span></td>

<td><span data-ttu-id="42d70-157">指定計數器詳細資料的目標物件。</span><span class="sxs-lookup"><span data-stu-id="42d70-157">Specifies the target audience for the counter details.</span></span> <span data-ttu-id="42d70-158">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="42d70-158">The following are the possible values:</span></span><br/> <dl> <span data-ttu-id="42d70-159"><dt><span id="standard"></span><span id="STANDARD"></span>標準</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-159"><dt><span id="standard"></span><span id="STANDARD"></span>standard</dt> </span></span><dd> <span data-ttu-id="42d70-160">顯示一般使用者可瞭解之計數器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="42d70-160">Display details about the counter that a typical user would understand.</span></span><br/> </dd> <span data-ttu-id="42d70-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>先進</dt> </span><span class="sxs-lookup"><span data-stu-id="42d70-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>advanced</dt> </span></span><dd> <span data-ttu-id="42d70-162">顯示只有 advanced user 可理解的計數器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="42d70-162">Display details about the counter that only an advanced user would understand.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d70-163">field</span><span class="sxs-lookup"><span data-stu-id="42d70-163">field</span></span></td>
<td><span data-ttu-id="42d70-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>男人： CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="42d70-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="42d70-165">結構中包含計數器值的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="42d70-165">The name of a field within the struct that contains the counter value.</span></span> <span data-ttu-id="42d70-166">使用者模式提供者不允許此屬性。</span><span class="sxs-lookup"><span data-stu-id="42d70-166">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d70-167">id</span><span class="sxs-lookup"><span data-stu-id="42d70-167">id</span></span></td>
<td><span data-ttu-id="42d70-168"><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="42d70-168"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="42d70-169">識別計數器集合內之計數器的唯一數位。</span><span class="sxs-lookup"><span data-stu-id="42d70-169">A unique number that identifies the counter within the counter set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d70-170">multiCounterID</span><span class="sxs-lookup"><span data-stu-id="42d70-170">multiCounterID</span></span></td>
<td><span data-ttu-id="42d70-171"><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="42d70-171"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="42d70-172">相同計數器集合中另一個計數器的識別碼，其乘數值會用來計算這個計數器的值。</span><span class="sxs-lookup"><span data-stu-id="42d70-172">The identifier of another counter within the same counter set, whose multiplier value is used to calculate this counter's value.</span></span> <span data-ttu-id="42d70-173">下列計數器類型需要乘數值。</span><span class="sxs-lookup"><span data-stu-id="42d70-173">The following counter types require a multiplier value.</span></span> <span data-ttu-id="42d70-174">參考的計數器必須是類型 PERF_COUNTER_RAWCOUNT。</span><span class="sxs-lookup"><span data-stu-id="42d70-174">The referenced counter must be of type PERF_COUNTER_RAWCOUNT.</span></span><br/>
<ul>
<li><span data-ttu-id="42d70-175">PERF_COUNTER_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="42d70-175">PERF_COUNTER_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="42d70-176">PERF_COUNTER_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="42d70-176">PERF_COUNTER_MULTI_TIMER_INV</span></span></li>
<li><span data-ttu-id="42d70-177">PERF_100NSEC_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="42d70-177">PERF_100NSEC_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="42d70-178">PERF_100NSEC_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="42d70-178">PERF_100NSEC_MULTI_TIMER_INV</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d70-179">NAME</span><span class="sxs-lookup"><span data-stu-id="42d70-179">name</span></span></td>

<td><span data-ttu-id="42d70-180">計數器的名稱。</span><span class="sxs-lookup"><span data-stu-id="42d70-180">The name of the counter.</span></span> <span data-ttu-id="42d70-181">名稱必須是唯一且小於1024個字元。</span><span class="sxs-lookup"><span data-stu-id="42d70-181">The name must be unique and less than 1,024 characters.</span></span> <span data-ttu-id="42d70-182">名稱區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="42d70-182">The name is case-sensitive.</span></span> <span data-ttu-id="42d70-183">如果計數器包含 <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> 屬性，您就不需要指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="42d70-183">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d70-184">perfFreqID</span><span class="sxs-lookup"><span data-stu-id="42d70-184">perfFreqID</span></span></td>
<td><span data-ttu-id="42d70-185"><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="42d70-185"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="42d70-186">相同計數器集合中另一個計數器的識別碼，其頻率值會用來計算這個計數器的值。</span><span class="sxs-lookup"><span data-stu-id="42d70-186">The identifier of another counter within the same counter set, whose frequency value is used to calculate this counter's value.</span></span> <span data-ttu-id="42d70-187">下列計數器類型需要頻率。</span><span class="sxs-lookup"><span data-stu-id="42d70-187">The following counter types require a frequency.</span></span> <span data-ttu-id="42d70-188">PERF_COUNTER_LARGE_RAWCOUNT 的計數器型別包含時間戳記值。</span><span class="sxs-lookup"><span data-stu-id="42d70-188">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="42d70-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="42d70-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="42d70-190">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="42d70-190">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="42d70-191">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="42d70-191">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="42d70-192">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="42d70-192">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d70-193">perfTimeID</span><span class="sxs-lookup"><span data-stu-id="42d70-193">perfTimeID</span></span></td>
<td><span data-ttu-id="42d70-194"><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="42d70-194"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="42d70-195">同一個計數器集合中另一個計數器的識別碼，其時間戳記值會用來計算這個計數器的值。</span><span class="sxs-lookup"><span data-stu-id="42d70-195">The identifier of another counter within the same counter set, whose time stamp value is used to calculate this counter's value.</span></span> <span data-ttu-id="42d70-196">下列計數器類型需要時間戳記。</span><span class="sxs-lookup"><span data-stu-id="42d70-196">The following counter types require a time stamp.</span></span> <span data-ttu-id="42d70-197">PERF_COUNTER_LARGE_RAWCOUNT 的計數器型別包含時間戳記值。</span><span class="sxs-lookup"><span data-stu-id="42d70-197">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="42d70-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="42d70-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="42d70-199">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="42d70-199">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="42d70-200">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="42d70-200">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="42d70-201">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="42d70-201">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d70-202">struct</span><span class="sxs-lookup"><span data-stu-id="42d70-202">struct</span></span></td>
<td><span data-ttu-id="42d70-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>男人： CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="42d70-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="42d70-204">包含此計數器值之 struct 元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="42d70-204">The name of a struct element that contains this counter value.</span></span> <span data-ttu-id="42d70-205">使用者模式提供者不允許此屬性。</span><span class="sxs-lookup"><span data-stu-id="42d70-205">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d70-206">符號</span><span class="sxs-lookup"><span data-stu-id="42d70-206">symbol</span></span></td>
<td><span data-ttu-id="42d70-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>男人： CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="42d70-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="42d70-208">識別計數器的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="42d70-208">A symbolic name that identifies the counter.</span></span> <span data-ttu-id="42d70-209"><a href="ctrpp.md">CTRPP</a>工具會建立常數，您可以在呼叫需要計數器 (識別碼的函式時使用，例如<a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="42d70-209">The <a href="ctrpp.md">CTRPP</a> tool creates a constant that you can use when calling functions that require a counter identifier (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span></span> <span data-ttu-id="42d70-210">常數的名稱是符號名稱。</span><span class="sxs-lookup"><span data-stu-id="42d70-210">The name of the constant is the symbolic name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d70-211">類型</span><span class="sxs-lookup"><span data-stu-id="42d70-211">type</span></span></td>

<td><span data-ttu-id="42d70-212">計數器類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="42d70-212">The name of the counter type.</span></span> <span data-ttu-id="42d70-213">如需可能的值，請參閱上述語法區塊。</span><span class="sxs-lookup"><span data-stu-id="42d70-213">For possible values, see the above syntax block.</span></span> <span data-ttu-id="42d70-214">如需每種類型的詳細資訊，請參閱《 Windows 2003 部署指南》中的 <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">計數器類型</a> 。</span><span class="sxs-lookup"><span data-stu-id="42d70-214">For details of each type, see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Counter Types</a> in the Windows 2003 Deployment Guide.</span></span> <span data-ttu-id="42d70-215">名稱區分大小寫，請使用小寫。</span><span class="sxs-lookup"><span data-stu-id="42d70-215">The name is case-sensitive use lowercase.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d70-216">uri</span><span class="sxs-lookup"><span data-stu-id="42d70-216">uri</span></span></td>
<td><span data-ttu-id="42d70-217"><strong>xs： anyURI</strong></span><span class="sxs-lookup"><span data-stu-id="42d70-217"><strong>xs:anyURI</strong></span></span></td>
<td><span data-ttu-id="42d70-218">唯一的統一資源識別項，可讓使用者從任何位置取得計數器值。</span><span class="sxs-lookup"><span data-stu-id="42d70-218">A unique uniform resource identifier that lets users retrieve counter values from any location.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="42d70-219">備註</span><span class="sxs-lookup"><span data-stu-id="42d70-219">Remarks</span></span>

<span data-ttu-id="42d70-220">為了提供回溯相容性，計數器集合中的每個計數器都應指定相同的 **perfFreqID** 和 **perfTimeID** 值。</span><span class="sxs-lookup"><span data-stu-id="42d70-220">To provide backwards-compatibility, each counter in the counter set should specify the same **perfFreqID** and **perfTimeID** values.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d70-221">規格需求</span><span class="sxs-lookup"><span data-stu-id="42d70-221">Requirements</span></span>



| <span data-ttu-id="42d70-222">需求</span><span class="sxs-lookup"><span data-stu-id="42d70-222">Requirement</span></span> | <span data-ttu-id="42d70-223">值</span><span class="sxs-lookup"><span data-stu-id="42d70-223">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42d70-224">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42d70-224">Minimum supported client</span></span><br/> | <span data-ttu-id="42d70-225">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42d70-225">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="42d70-226">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42d70-226">Minimum supported server</span></span><br/> | <span data-ttu-id="42d70-227">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42d70-227">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

