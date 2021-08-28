---
description: 選擇性的布林值 &lt; isIndexed &gt; 元素會指定是否使用 Windows Search 4 或更高的) ，在本機或遠端 (搜尋連接器所描述的位置進行索引。
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: 'isIndexed 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3588d451631ab8d0bb8313092b5b1ee7bb5c9dc4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881851"
---
# <a name="isindexed-element-search-connector-schema"></a>isIndexed 元素 (搜尋連接器架構) 

選擇性的布林值 &lt; isIndexed &gt; 元素會指定是否使用 Windows Search 4 或更高的) ，在本機或遠端 (搜尋連接器所描述的位置進行索引。 本機資料夾的預設值為 true。 這個元素沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                                                                   | 子元素 |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [searchConnectorDescriptionType 元素 (搜尋連接器架構) ](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



