---
description: '&lt;Mode &gt; 元素會指定是否應將 URL 包含或排除在搜尋連接器的範圍內。 允許的值包括和排除。 這個元素沒有任何子項目，而且沒有任何屬性。'
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: " (搜尋連接器架構) 的模式元素"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e096bb21d634da6107359c014b82f1b367aba1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886747"
---
# <a name="mode-element-search-connector-schema"></a> (搜尋連接器架構) 的模式元素

&lt;Mode &gt; 元素會指定是否應將 URL 包含或排除在搜尋連接器的範圍內。 允許的值有 `Include` 與 `Exclude`。 這個元素沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- mode -->
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
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
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

無法搜尋或流覽排除的範圍。 您可以嵌套 scopeItem Url。 例如，您可以包含父範圍及其所有子系（除了一個之外），方法是新增包含的父 URL、深度的深度值，以及排除子 URL。

## <a name="example"></a>範例

下列範例顯示的搜尋範圍包含 C： \\ ExampleFolder 及其所有的子資料夾（c： \\ ExampleFolder ExcludeMe 除外） \\ 。


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



