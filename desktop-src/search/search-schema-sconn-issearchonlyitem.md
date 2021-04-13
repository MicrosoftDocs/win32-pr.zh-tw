---
description: 布林值 <isSearchOnlyItem> 元素會指定搜尋提供者是否除了搜尋模式之外，還支援瀏覽模式。 這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: 'isSearchOnlyItem 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511080"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>isSearchOnlyItem 元素 (搜尋連接器架構) 

布林值 <isSearchOnlyItem> 元素會指定搜尋提供者是否除了搜尋模式之外，還支援瀏覽模式。 這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
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

此值 `true` 表示使用者無法流覽搜尋連接器位置。 此值 `false` 表示使用者可以流覽搜尋連接器位置。

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



