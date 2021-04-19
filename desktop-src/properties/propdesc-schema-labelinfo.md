---
description: 指定如何顯示內容的標籤。
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974384"
---
# <a name="labelinfo"></a>labelInfo

指定如何顯示內容的標籤。 每個[propertyDescription](./propdesc-schema-propertydescription.md)專案都只能有一個[labelInfo]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [labelInfo]() 元素，則不會顯示內容的標籤;不過，這通常是一個瑕疵。

## <a name="syntax"></a>Syntax


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
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
<td>label</td>
<td>公用。 選擇性。 顯示在 UI 中的標籤 (例如，[詳細資料] 資料行標籤或 [預覽] 窗格) 。 語法允許直接顯示字串或間接顯示字串參考。 使用間接顯示字串，因為它可以當地語系化。 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription：： GetDisplayName</strong></a> 會傳回已解析的顯示名稱。</td>
</tr>
<tr class="even">
<td>sortDescription</td>
<td>選擇性。 指定以排序選項提供的字串。 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription：： GetSortDescription</strong></a> 會傳回此排序描述。 下列值提供對應的 UI 字串。
<ul>
<li>一般： &quot; 排序向上 &quot;  /  &quot; 排序下移&quot;</li>
<li>AToZ：頂端 &quot; &quot;  /  &quot; Z 頂端的&quot;</li>
<li>LowestHighest：頂端 &quot; &quot;  /  &quot; 最高的最高&quot;</li>
<li>OldestNewest：最舊的最 &quot; &quot;  /  &quot; 新頂端&quot;</li>
<li>SmallestLargest：頂端最 &quot; &quot;  /  &quot; 大的最小值&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>invitationText</td>
<td>選擇性。 顯示為控制項或工具提示 (使用者之指示的說明字串文字，請 &quot; 輸入作者名稱。 &quot;) 。 語法允許直接顯示字串或間接顯示字串參考。 使用間接顯示字串，因為它可以當地語系化。 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription：： GetEditInvitation</strong></a> 會傳回已解析的邀請文字。</td>
</tr>
<tr class="even">
<td>hideLabel</td>
<td>選擇性。 預設值為 &quot;false&quot;。 指出標籤是否隱藏。</td>
</tr>
</tbody>
</table>



 

 

 
