---
description: '&lt;ScopeItem &gt; 元素代表排除/包含範圍資料表中的單一專案。'
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: 'scopeItem 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a585acd065efcbc58091d4c8bebce733ed2c73
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880444"
---
# <a name="scopeitem-element-search-connector-schema"></a>scopeItem 元素 (搜尋連接器架構) 

&lt;ScopeItem &gt; 元素代表排除/包含範圍資料表中的單一專案。 &lt;scopeItem 藉 &gt; 由新增三個可控制資料夾包含和排除的元素、控制結果的深度，以及指定範圍的位置，來擴充標準 shellLinkType 類型。 如果 &lt; 範圍 &gt; 元素存在，則需要這個元素。 它有三個子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
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



| Parent 項目                                                           | 子元素                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [範圍元素 (搜尋連接器架構) ](search-schema-sconn-scope.md) | [範圍元素 (搜尋連接器架構) ](search-schema-sconn-scope-mode.md)。        |
|                                                                          | [範圍元素 (搜尋連接器架構) ](search-schema-sconn-scope-depth.md)。       |
|                                                                          | [scopeItem Url 元素 (搜尋連接器架構) ](search-schema-sconn-scope-url.md)。 |



 

## <a name="remarks"></a>備註

使用 &lt; 範圍 &gt; 和 scopeItem &lt; 專案 &gt; 來識別應該搜尋的位置，以及要從搜尋中排除哪些位置。

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



 

 



