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
# <a name="counter-complex-type"></a>計數器複雜類型

定義計數器。

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

## <a name="child-elements"></a>子元素



| 元素               | 類型                                                                                 | Description                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **counterAttributes** | [**男人： counterAttributes**](performance-counters-counterattributes-complex-type.md) | 列出指定如何在取用者應用程式中顯示計數器資料的唯一屬性。<br/> |



## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>名稱</th>
<th>類型</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>彙總 (aggregate)</td>

<td>如果<a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a>的<strong>實例</strong>屬性是 GlobalAggregate、multipleAggregate 或 globalAggregateHistory，則適用的彙總函式。 以下是您可以套用的可能彙總函式：<br/> <dl> <dt><span id="max"></span><span id="MAX"></span>麥克斯</dt> <dd> 傳回最大計數器值。<br/> </dd> <dt><span id="min"></span><span id="MIN"></span>化</dt> <dd> 傳回最小計數器值。<br/> </dd> <dt><span id="avg"></span><span id="AVG"></span>Avg</dt> <dd> 傳回的平均計數器值。<br/> </dd> <dt><span id="sum"></span><span id="SUM"></span>和</dt> <dd> 傳回計數器值的總和。<br/> </dd> <dt><span id="undefined"></span><span id="UNDEFINED"></span>定義</dt> <dd> 請勿匯總此計數器。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>baseID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></td>
<td>相同計數器集合中另一個計數器的識別碼，其值用來計算這個計數器的值。 下列計數器類型需要基底計數器：<br/> <dl> <dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> <dd> 需要 PERF_AVERAGE_BASE 基底計數器。<br/> </dd> <dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> <dd> 需要 PERF_AVERAGE_BASE 基底計數器。<br/> </dd> <dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> <dd> 需要 PERF_COUNTER_MULTI_BASE 基底計數器。<br/> </dd> <dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> <dd> 需要 PERF_LARGE_RAW_BASE 基底計數器。<br/> </dd> <dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> <dd> 需要 PERF_LARGE_RAW_BASE 基底計數器。<br/> </dd> <dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> <dd> 需要 PERF_RAW_BASE 基底計數器。<br/> </dd> <dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> <dd> 需要 PERF_SAMPLE_BASE 基底計數器。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td>defaultScale</td>

<td>要套用至計數器值的縮放比例 (因數 * 計數器值) 。 如果未套用任何小數位數，則預設值為零。 有效的值範圍從10到 10 (0.0000000001 到 1000000000) 。 如果此值為零，則小數位數值為1。如果這個值是1，則小數位數值為 10;如果這個值是1，則小數位數值為. 10;依此類推。<br/></td>
</tr>
<tr class="even">
<td>description</td>
<td><strong>xs:string</strong></td>
<td>計數器的簡短描述。 如果計數器包含 <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> 屬性，您就不需要指定此屬性。<br/></td>
</tr>
<tr class="odd">
<td>detailLevel</td>

<td>指定計數器詳細資料的目標物件。 以下是可能的值：<br/> <dl> <dt><span id="standard"></span><span id="STANDARD"></span>標準</dt> <dd> 顯示一般使用者可瞭解之計數器的詳細資料。<br/> </dd> <dt><span id="advanced"></span><span id="ADVANCED"></span>先進</dt> <dd> 顯示只有 advanced user 可理解的計數器詳細資料。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>field</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>男人： CSymbolType</strong></a></td>
<td>結構中包含計數器值的功能變數名稱。 使用者模式提供者不允許此屬性。<br/></td>
</tr>
<tr class="odd">
<td>id</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></td>
<td>識別計數器集合內之計數器的唯一數位。<br/></td>
</tr>
<tr class="even">
<td>multiCounterID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></td>
<td>相同計數器集合中另一個計數器的識別碼，其乘數值會用來計算這個計數器的值。 下列計數器類型需要乘數值。 參考的計數器必須是類型 PERF_COUNTER_RAWCOUNT。<br/>
<ul>
<li>PERF_COUNTER_MULTI_TIMER</li>
<li>PERF_COUNTER_MULTI_TIMER_INV</li>
<li>PERF_100NSEC_MULTI_TIMER</li>
<li>PERF_100NSEC_MULTI_TIMER_INV</li>
</ul></td>
</tr>
<tr class="odd">
<td>NAME</td>

<td>計數器的名稱。 名稱必須是唯一且小於1024個字元。 名稱區分大小寫。 如果計數器包含 <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> 屬性，您就不需要指定此屬性。<br/></td>
</tr>
<tr class="even">
<td>perfFreqID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></td>
<td>相同計數器集合中另一個計數器的識別碼，其頻率值會用來計算這個計數器的值。 下列計數器類型需要頻率。 PERF_COUNTER_LARGE_RAWCOUNT 的計數器型別包含時間戳記值。<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="odd">
<td>perfTimeID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></td>
<td>同一個計數器集合中另一個計數器的識別碼，其時間戳記值會用來計算這個計數器的值。 下列計數器類型需要時間戳記。 PERF_COUNTER_LARGE_RAWCOUNT 的計數器型別包含時間戳記值。<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="even">
<td>struct</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>男人： CSymbolType</strong></a></td>
<td>包含此計數器值之 struct 元素的名稱。 使用者模式提供者不允許此屬性。<br/></td>
</tr>
<tr class="odd">
<td>符號</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>男人： CSymbolType</strong></a></td>
<td>識別計數器的符號名稱。 <a href="ctrpp.md">CTRPP</a>工具會建立常數，您可以在呼叫需要計數器 (識別碼的函式時使用，例如<a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>) 。 常數的名稱是符號名稱。<br/></td>
</tr>
<tr class="even">
<td>類型</td>

<td>計數器類型的名稱。 如需可能的值，請參閱上述語法區塊。 如需每種類型的詳細資訊，請參閱《 Windows 2003 部署指南》中的 <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">計數器類型</a> 。 名稱區分大小寫，請使用小寫。 <br/></td>
</tr>
<tr class="odd">
<td>uri</td>
<td><strong>xs： anyURI</strong></td>
<td>唯一的統一資源識別項，可讓使用者從任何位置取得計數器值。<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

為了提供回溯相容性，計數器集合中的每個計數器都應指定相同的 **perfFreqID** 和 **perfTimeID** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

