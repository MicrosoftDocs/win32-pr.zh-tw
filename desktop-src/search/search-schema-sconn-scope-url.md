---
description: '&lt;Url &gt; 元素會指定代表搜尋連接器範圍的 url。 這個元素沒有任何子項目，而且沒有任何屬性。'
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: 'scopeItem url 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a1db669f7365f04bed49c769ab695ab674b20b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886709"
---
# <a name="scopeitem-url-element-search-connector-schema"></a>scopeItem url 元素 (搜尋連接器架構) 

&lt;Url &gt; 元素會指定代表搜尋連接器範圍的 url。 這個元素沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
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

值可以是本機檔案系統路徑或 URL。

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
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



