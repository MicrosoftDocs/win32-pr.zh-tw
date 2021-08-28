---
description: 選擇性 &lt; 範圍 &gt; 元素會指定 scopeItem 專案的 &lt; 集合 &gt; ，這些專案會定義此特定搜尋連接器的範圍包含與排除專案。
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: '範圍元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c011eee8def80a7f1d395a7a52a72d30fb4935
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886694"
---
# <a name="scope-element-search-connector-schema"></a>範圍元素 (搜尋連接器架構) 

選擇性 &lt; 範圍 &gt; 元素會指定 scopeItem 專案的 &lt; 集合 &gt; ，這些專案會定義此特定搜尋連接器的範圍包含與排除專案。 如果 &lt; 範圍 &gt; 存在，則必須包含至少一個 &lt; scopeItem &gt; 元素。 這個元素沒有屬性。

## <a name="syntax"></a>Syntax


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
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



| Parent 項目                                                                                                   | 子元素                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [searchConnectorDescriptionType 元素 (搜尋連接器架構) ](search-schema-searchconnectordescription.md) | [ScopeItem 元素 (搜尋連接器架構) ](search-schema-sconn-scopeitem.md)。 |



 

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



 

 



