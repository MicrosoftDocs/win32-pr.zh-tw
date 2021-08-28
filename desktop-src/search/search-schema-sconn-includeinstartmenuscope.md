---
description: 選擇性的布林值 &lt; includeInStartMenuScope &gt; 元素指定此搜尋連接器是否應包含在 [開始] 功能表搜尋範圍內。
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: 'includeInStartMenuScope 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20696dc6d2bc41b3f693e771a59541204e376e7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882391"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>includeInStartMenuScope 元素 (搜尋連接器架構) 

選擇性的布林值 &lt; includeInStartMenuScope &gt; 元素指定此搜尋連接器是否應包含在 [開始] 功能表搜尋範圍內。 使用檔案系統作為資料來源之搜尋連接器的預設值是 true，而針對屬性處理常式所使用的搜尋連接器，則預設值為 false。 這個元素沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
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

如果您在 [開始] 功能表範圍中包含搜尋連接器，使用者可以從 [開始] 功能表的 [搜尋] 方塊中搜尋您的位置。

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



