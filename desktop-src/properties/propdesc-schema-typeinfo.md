---
description: 指定屬性的類型資訊。
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987459"
---
# <a name="typeinfo"></a>typeInfo

指定屬性的類型資訊。 每個[propertyDescription](./propdesc-schema-propertydescription.md)只能有一個[typeInfo]()元素。 此元素已針對 Windows 7 變更。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [typeInfo]() 元素，則會將預設屬性設定套用至屬性描述。

## <a name="syntax-for-windows-7"></a>Windows 7 的語法


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                   | 子元素 |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | 無           |



 

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>type</td>
<td>公用。 選擇性。 預設值為 &quot; Any &quot; 。 指出屬性的類型。 下列是有效的類型，且其相關聯的 variant 類型會由 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription：： GetPropertyType</strong></a>抓取。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>任意</td>
<td>預設值。 屬性子系統不會強制執行或強制轉換屬性值。 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription：： GetPropertyType</strong></a> 會傳回 VT_Null。 強烈建議 (Isv) 的獨立軟體廠商提供類型，而不是改回此預設值。</td>
</tr>
<tr class="even">
<td>Null</td>
<td>這個屬性沒有值。 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription：： GetPropertyType</strong></a> 會傳回 VT_Null。</td>
</tr>
<tr class="odd">
<td>String</td>
<td>值必須是 VT_LPWSTR，也就是以 null 參考結束的 Unicode 字串。</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>值必須是 VT_BOOL，也就是布林值。</td>
</tr>
<tr class="odd">
<td>Byte</td>
<td>值必須是 VT_UI1，也就是位元組。</td>
</tr>
<tr class="even">
<td>Buffer</td>
<td>值必須是 VT_UI1 |VT_VECTOR 位元組緩衝區。</td>
</tr>
<tr class="odd">
<td>Int16</td>
<td>值必須是 VT_I2，也就是16位整數。</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>值必須是 VT_UI2，也就是16位不帶正負號的整數。</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>值必須是 VT_I4，也就是32位的整數。</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>值必須是 VT_UI4，也就是32位不帶正負號的整數。</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>值必須是 VT_I8，也就是64位的整數。</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>值必須是 VT_UI8，也就是64位不帶正負號的整數。</td>
</tr>
<tr class="odd">
<td>Double</td>
<td>值必須是 VT_R8，也就是雙精度浮點數。</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>值必須是 VT_FILETIME，也就是 <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>。</td>
</tr>
<tr class="odd">
<td>Guid</td>
<td>值必須是 VT_CLSID，也就是 (CLSID) 的類別識別碼。</td>
</tr>
<tr class="even">
<td>Blob</td>
<td>值必須是長度為首碼位元組的 VT_BLOB。</td>
</tr>
<tr class="odd">
<td>串流</td>
<td>值必須是 VT_STREAM，也就是執行 <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>的物件。</td>
</tr>
<tr class="even">
<td>剪貼簿</td>
<td>值必須是 VT_CF，也就是剪貼簿格式。</td>
</tr>
<tr class="odd">
<td>Object</td>
<td>值必須是 VT_UNKNOWN，也就是執行 <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>的物件。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>groupingRange</td>
<td>選擇性。 預設值是 &quot; 離散的 &quot; 。 指定當視圖依此屬性分組時，顯示內容的方式。 在這裡設定之後，這些值就會由 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription：： GetGroupingRange</strong></a>取出。 以下是有效的類型。

<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Discrete</td>
<td>預設值。 顯示個別的值。</td>
</tr>
<tr class="even">
<td>英數字元</td>
<td>顯示值的靜態英數位元範圍。</td>
</tr>
<tr class="odd">
<td>大小</td>
<td>顯示值的靜態大小範圍。</td>
</tr>
<tr class="even">
<td>Date</td>
<td>顯示月份/年度群組。 Type = DateTime 之屬性的預設值 &quot; &quot; 。</td>
</tr>
<tr class="odd">
<td>TimeRelative</td>
<td>以時間相對的群組顯示。</td>
</tr>
<tr class="even">
<td>動態</td>
<td>顯示動態建立的值範圍。</td>
</tr>
<tr class="odd">
<td>百分比</td>
<td>顯示百分比值區。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>isInnate</td>
<td>公用。 選擇性。 預設值為 &quot;false&quot;。 指定屬性是否視為固有。 固有屬性是從檔案內容或從其他資源或系統進行計算的屬性。 例如，System.object 是檔案系統提供的固有屬性;變更和本身的屬性值不會執行任何動作。 其他範例為 system.string 和 System.Doc>ument。PageCount，根據檔案內容的程式來計算，而不是根據使用者變更的設定。 設定 isInnate = &quot; true &quot; 表示使用者無法直接透過屬性控制項來編輯此屬性。 此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_ISINNATE 旗標。</td>
</tr>
<tr class="even">
<td>canBePurged</td>
<td><strong>Windows Vista Service Pack 1 (SP1) 和更新版本</strong>。 公用。 選擇性。 當設為 &quot; true 時 &quot; ，允許刪除固有屬性。 固有屬性（從其他屬性計算而來）是以唯讀方式定義的。 這個屬性的預設值取決於 <em>isInnate</em> 值。

<table>
<thead>
<tr class="header">
<th>isInnate</th>
<th>canBePurged 預設值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>true</td>
<td>false</td>
</tr>
<tr class="even">
<td>false</td>
<td>true</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
屬性，其 <em>isInnate</em> 值為 &quot; false &quot; (表示屬性是讀取/寫入) 也無法將 <em>canBePurged</em> 值設定為 &quot; false &quot; 。 這項限制是由作業系統強制執行。
</blockquote>
</div>
<div>
 
</div>
<p>雖然這個屬性是在 Windows Vista Service Pack 1 (SP1) 引進的，但包含這個屬性的 propdesc 檔案與 Windows Vista SP1 之前的 Windows Vista 相容。 在這種情況下，只會忽略 <em>canBePurged</em> 屬性。</p></td>
</tr>
<tr class="odd">
<td>multipleValues</td>
<td>公用。 選擇性。 預設值為 &quot;false&quot;。 指定這個屬性是否可以有多個值。 此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_MULTIPLEVALUES 旗標。 這也會影響 VT_VECTOR 是否為屬性值的 VARTYPE 或。</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>公用。 選擇性。 預設值為 &quot;false&quot;。 指定屬性是否為群組標題。 群組標題會嚴格用於 proplists 中，沒有任何值，絕對不會儲存在檔案中，也應該具有 <typeInfo type=&quot;Null&quot;> 。 系統中的某些 UI 會使用 proplists 來指出要顯示的屬性順序。 這些 proplists 可能包含群組標題的參考 (例如 PropGroup) ，它會告訴 UI 啟動新的群組區段 (例如 &quot; 相機設定 &quot;) 。 具有 isGroup = true 的屬性 &quot; 描述 &quot; 應該指定 <labelInfo label=&quot;Some localized label&quot;> ，否則它不是有用的屬性。 此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_ISGROUP 旗標。</td>
</tr>
<tr class="odd">
<td>aggregationType</td>
<td>公用。 選擇性。 預設值為預設值 &quot; &quot; 。 指定當選取多個專案時，如何顯示匯總屬性。 在這裡設定之後， <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription：： GetAggregationType</strong></a> 會以 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>的形式取出這些值。 以下是有效的類型。

<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>預設</td>
<td>預設值。 在 UI 中顯示 <strong>多個值</strong> 預留位置。 如果 <em>類型</em> 與指定的 <em>aggregationType</em>不相容，這就是預設值。</td>
</tr>
<tr class="even">
<td>First</td>
<td>顯示選取專案或集合中第一個專案的屬性值。</td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>顯示數值的總和。 適用于如 system.string 或 System. 大小等屬性。 此值與非數數值型別不相容。</td>
</tr>
<tr class="even">
<td>平均</td>
<td>顯示數值的平均值。 適用于如 System. 評等的屬性。 此值與非數數值型別不相容。</td>
</tr>
<tr class="odd">
<td>DateRange</td>
<td>顯示日期的範圍。 適用于 DateTaken 等屬性。 這個值與 type = DateTime 以外的任何值都不相容 &quot; &quot; ，而且是該類型屬性的預設值。</td>
</tr>
<tr class="even">
<td>Union</td>
<td>顯示選取範圍或集合中所有值的聯集。 值的顯示順序未定義。 此值是 type = &quot; String &quot; 和 multipleValues = true 的屬性預設值 &quot; &quot; 。</td>
</tr>
<tr class="odd">
<td>最大值</td>
<td>顯示集合中的最大值。 適用于 DateModified 之類的屬性。 與非數值或非日期類型不相容。</td>
</tr>
<tr class="even">
<td>最小值</td>
<td>顯示集合中的最小值。 與非數值或非日期類型不相容。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>isTreeProperty</td>
<td>公用。 選擇性。 預設值為 &quot;false&quot;。</td>
</tr>
<tr class="odd">
<td>isViewable</td>
<td>公用。 選擇性。 預設值為 &quot;false&quot;。 指定是否要向使用者查看此屬性。 例如，資料行選擇器 UI 只會顯示具有 isViewable = true 的 &quot; 屬性 &quot; 。 例外狀況是由 proplist 驅動的 UI，一律會顯示內容。 如果您的屬性只是要在兩個物件之間快速流覽資料，而不想讓使用者看到，則這個屬性應該是 false。 此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_ISVIEWABLE 旗標。</td>
</tr>
<tr class="even">
<td>isQueryable</td>
<td>僅限 Windows Vista。 在 Windows 7 和更新版本中不支援。 公用。 選擇性。 預設值為 &quot;false&quot;。 指定是否要在搜尋查詢產生器 UI 中提供這個屬性。 在 &quot; &quot; 遵守 isQueryable = true 之前，屬性必須有 isViewable = true &quot; &quot; 。 此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_ISQUERYABLE 旗標。</td>
</tr>
<tr class="odd">
<td>searchRawValue</td>
<td><strong>Windows 7 和更新版本。</strong> 公用。 選擇性。 預設值為 &quot;false&quot;。</td>
</tr>
<tr class="even">
<td>includeInFullTextQuery</td>
<td>僅限 Windows Vista。 在 Windows 7 和更新版本中不支援。 公用。 選擇性。 預設值為 &quot;false&quot;。</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>公用。 選擇性。 預設值是 &quot; String &quot; 。 指定搜尋查詢產生器 UI 的提示，讓它可以判斷述詞內可能條件運算子的清單。 以下是可辨識的值。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>預設值。 將會使用下列運算子：是，不是，，，，， &quot; &quot; &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; &quot; 開頭為 &quot; ， &quot; 結尾為 &quot; ， &quot; 包含 &quot; ， &quot; 不包含 &quot; ， &quot; 則類似 &quot; 。</td>
</tr>
<tr class="even">
<td>Number</td>
<td>數值屬性的預設值。 將會使用下列運算子： &quot; equals &quot; 、 &quot; 不等於、小於、大於 &quot; &quot; &quot; &quot; &quot; 、 &quot; 小於或等於 &quot; 、 &quot; 大於或等於 &quot; 。</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Type = DateTime 之屬性的預設值 &quot; &quot; 。 將會使用下列運算子： &quot; 是，不是 &quot; &quot; &quot; ， &quot; 之前是 &quot; &quot; &quot; &quot; &quot; &quot; &quot; ，在之後，但在中，但包含。</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Type = Boolean 的屬性預設 &quot; 值 &quot; 。 與數位相同。</td>
</tr>
<tr class="odd">
<td>大小</td>
<td>與數位相同。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>defaultOperation</td>
<td>公用。 選擇性。 預設值為 [ &quot; 等於] &quot; 。 指定搜尋查詢產生器工具的提示，讓它可以判斷預設運算子。 可能的值如下：

<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>等於</td>
<td>預設值。 表示對等專案。</td>
</tr>
<tr class="even">
<td>NotEqual</td>
<td>表示不相等。</td>
</tr>
<tr class="odd">
<td>LessThan</td>
<td>表示小於。</td>
</tr>
<tr class="even">
<td>GreaterThan</td>
<td>ConditionType = Size 的屬性預設 &quot; 值 &quot; 。 表示大於。</td>
</tr>
<tr class="odd">
<td>包含</td>
<td>ConditionType = String 的屬性預設 &quot; 值 &quot; 。 表示包含。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
