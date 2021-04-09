---
description: 選擇性 <domain> 元素會指定此搜尋連接器所使用之搜尋服務的 URL。 它會顯示在詳細資料窗格中。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: '網域元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847805"
---
# <a name="domain-element-search-connector-schema"></a>網域元素 (搜尋連接器架構) 

選擇性 <domain> 元素會指定此搜尋連接器所使用之搜尋服務的 URL。 它會顯示在詳細資料窗格中。 這個元素沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
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

URL 應該是搜尋提供者的最上層網域。 例如： https://www.example.com 。

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



