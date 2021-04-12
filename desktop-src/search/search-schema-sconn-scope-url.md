---
description: <url>元素指定代表搜尋連接器範圍的 URL。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: 'scopeItem url 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c573308fe406fe4500f6bb8e88b3762fa0bbac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847803"
---
# <a name="scopeitem-url-element-search-connector-schema"></a>scopeItem url 元素 (搜尋連接器架構) 

<url>元素指定代表搜尋連接器範圍的 URL。 這個元素沒有任何子項目，而且沒有任何屬性。

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



 

 



