---
description: <depth>元素會指定搜尋連接器的範圍是否應包含子 url。 允許的值為 Deep 和淺層。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: '搜尋連接器架構 (的深度元素) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245156088cd68fcf67103c18b987a9b459b0b760b3a04a1ced817badd25aada8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862523"
---
# <a name="depth-element-search-connector-schema"></a>搜尋連接器架構 (的深度元素) 

<depth>元素會指定搜尋連接器的範圍是否應包含子 url。 允許的值有 `Deep` 與 `Shallow`。 這個元素沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- depth -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                                   | 子元素 |
|----------------------------------------------------------------------------------|----------------|
| [scopeItem 元素 (搜尋連接器架構) ](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>備註

如果深度較深，使用者可以流覽或搜尋 scopeItem 的 URL 層級或任何子 Url 內的專案。

## <a name="example"></a>範例

下列範例顯示的搜尋範圍包含 C： \\ FolderA 及其所有的子資料夾和 C： FolderB， \\ 但不包含任何子資料夾。


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



