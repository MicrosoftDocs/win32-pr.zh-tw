---
description: 選擇性 <description> 元素指定此搜尋連接器的描述。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: " (搜尋連接器架構) 的 description 元素"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d82fd6ad3ae45c4a8c3700c4822387a81880d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318144"
---
# <a name="description-element-search-connector-schema"></a> (搜尋連接器架構) 的 description 元素

選擇性 <description> 元素指定此搜尋連接器的描述。 這個元素沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
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



 

## <a name="remarks"></a>備註

描述應該很容易使用，因為它可以在工具提示中使用。

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 



