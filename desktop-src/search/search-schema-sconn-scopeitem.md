---
description: <scopeItem>元素代表排除/包含範圍資料表中的單一專案。
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: 'scopeItem 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112376"
---
# <a name="scopeitem-element-search-connector-schema"></a>scopeItem 元素 (搜尋連接器架構) 

<scopeItem>元素代表排除/包含範圍資料表中的單一專案。 <scopeItem> 藉由新增可控制資料夾包含和排除的三個新元素、控制結果的深度，以及指定範圍的位置，來擴充標準 shellLinkType 類型。 如果 <scope> 元素存在，則需要這個元素。 它有三個子項目，而且沒有任何屬性。

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

您 <scope> 可以使用和專案 <scopeItem> 來識別應該搜尋的位置，以及要從搜尋中排除哪些位置。

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



 

 



