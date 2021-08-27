---
description: 指定如何顯示內容的標籤。
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d2d358270bfdf231f990feee54d90f6f39f16fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475094"
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




| 屬性 | 描述 | 
|-----------|-------------|
| label | 公用。 選擇性。 顯示在 UI 中的標籤 (例如，[詳細資料] 資料行標籤或 [預覽] 窗格) 。 語法允許直接顯示字串或間接顯示字串參考。 使用間接顯示字串，因為它可以當地語系化。 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription：： GetDisplayName</strong></a> 會傳回已解析的顯示名稱。 | 
| sortDescription | 選擇性。 指定以排序選項提供的字串。 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription：： GetSortDescription</strong></a> 會傳回此排序描述。 下列值提供對應的 UI 字串。<ul><li>一般：「排序進行中」/「排序即將中斷」</li><li>AToZ： "A on top"/"Z on top"</li><li>LowestHighest：「最小的頂端」/「最高」</li><li>OldestNewest：「最舊的頂端」/「最新」</li><li>SmallestLargest：「最小的最小值」/「最大值」</li></ul> | 
| invitationText | 選擇性。 顯示為控制項或工具提示使用者之指示的說明字串文字 (例如「輸入作者名稱」。) 。 語法允許直接顯示字串或間接顯示字串參考。 使用間接顯示字串，因為它可以當地語系化。 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription：： GetEditInvitation</strong></a> 會傳回已解析的邀請文字。 | 
| hideLabel | 選擇性。 預設值為 "false"。 指出標籤是否隱藏。 | 




 

 

 
