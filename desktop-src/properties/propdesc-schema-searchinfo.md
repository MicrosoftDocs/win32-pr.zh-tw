---
description: 指定如何根據指定的屬性定義來設定 Windows 搜尋引擎。
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984190"
---
# <a name="searchinfo"></a>searchInfo

指定如何根據指定的屬性定義來設定 Windows 搜尋引擎。 如果未提供任何 [searchInfo]() 元素，則不會將屬性包含在 Windows 搜尋引擎中。 此元素已針對 Windows 7 變更。

## <a name="syntax-for-windows-7"></a>Windows 7 的語法


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a>Windows Vista 的語法


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
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
<td>inInvertedIndex</td>
<td>公用。 選擇性。 指出屬性值是否應該儲存在反向索引中。 這可讓終端使用者對這個屬性的值執行全文檢索查詢。 預設值為 &quot;false&quot;。</td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>公用。 選擇性。 指出屬性是否也應該以資料行的形式儲存在 Windows 搜尋資料庫中，讓獨立軟體廠商 (Isv) 可以建立以述詞為基礎的查詢 (例如 &quot; Select * Where system.string &quot; &quot; = ' qqq ' &quot;) 。 如果架構建立者想要讓使用者 (或開發人員) 在屬性上建立以述詞為基礎的查詢，則必須將此設定為 &quot; true &quot; 。 預設值為 &quot;false&quot;。</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>公用。 選擇性。 預設值為 &quot;True&quot;。 如果屬性是多重值，則這個屬性一律 &quot; 為 true &quot; 。</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>公用。 選擇性。 為了優化排序和分組，Windows 搜尋引擎可以針對具有 isColumn = true 的屬性建立次要索引 &quot; &quot; 。 只有當 Windows Vista 中的 inInvertedIndex 為 &quot; true， &quot; 或 &quot; &quot; Windows 7 中的 isColumn 為 true 時，這個屬性才有用。 如果屬性通常會依使用者排序，則應該指定此屬性。 Windows Vista 中的預設值為 &quot; NotIndexed &quot; 。 Windows 7 中的預設值為 &quot; OnDemand &quot; 。 下列是有效的值。
<ul>
<li><strong>NotIndexed</strong>：永不建立值索引。</li>
<li><strong>OnDisk</strong>：建立這個屬性的預設值索引。</li>
<li><strong>OnDiskAll</strong> (Windows 7 及更新版本僅限) ：建立這個屬性的預設值索引，如果它是向量屬性，則也是所有串連向量值的值索引。</li>
<li><strong>OnDiskVector</strong> (Windows 7 及更新版本僅) ：為串連向量值建立預設值索引。</li>
<li><strong>OnDemand</strong> (Windows 7 及更新版本僅限) ：僅依需求建立值索引，也就是只在第一次用於查詢時。</li>
</ul></td>
</tr>
<tr class="odd">
<td>maxSize</td>
<td>公用。 選擇性。 儲存在 Windows 搜尋資料庫中的特定屬性所允許的大小上限（以位元組為單位）。 預設值為：
<ul>
<li><strong>Windows Vista</strong>：128位元組</li>
<li><strong>Windows 7 和更新版本</strong>：512位元組</li>
</ul>
請注意，這個大小上限是以位元組為單位，而不是字元。 字元數目上限取決於其編碼方式。<br/></td>
</tr>
<tr class="even">
<td>助憶鍵</td>
<td><strong>Windows 7 和更新版本。</strong> 公用。 選擇性。 助憶鍵值的清單，可用來參考搜尋查詢中的屬性。 此清單會以 ' | ' 字元分隔。</td>
</tr>
</tbody>
</table>



 

 

 
