---
description: 布林值 <supportsAdvancedQuerySyntax> 元素會指定搜尋提供者是否支援 Advanced 查詢語法。 預設為 false。 這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: 'supportsAdvancedQuerySyntax 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973427"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a>supportsAdvancedQuerySyntax 元素 (搜尋連接器架構) 

布林值 <supportsAdvancedQuerySyntax> 元素會指定搜尋提供者是否支援 [Advanced 查詢語法](-search-3x-advancedquerysyntax.md)。 預設為 false。 這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
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

此值 `true` 表示搜尋提供者支援在搜尋查詢中傳送的 Advanced Query 語法。

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



