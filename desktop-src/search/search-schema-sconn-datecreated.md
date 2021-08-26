---
description: 選擇性 &lt; dateCreated &gt; 元素會使用 ISO 8601 標準來識別建立此搜尋連接器的日期和時間。 它沒有任何子項目，而且沒有任何屬性。
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: 'dateCreated 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff7c739bcad9e3a6594008597c0392398f22864
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882502"
---
# <a name="datecreated-element-search-connector-schema"></a>dateCreated 元素 (搜尋連接器架構) 

選擇性 &lt; dateCreated &gt; 元素會使用 ISO 8601 標準來識別建立此搜尋連接器的日期和時間。 它沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
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

此元素的值格式會遵循 ISO 8601 標準。 常見的用法是下列其中一項：

-   \[YYYY \] - \[ MM \] - \[ DD \] T \[ hh \] ： \[ mm \] ： \[ ss \] ± \[ hh \] ： \[ MM \] ( "1981-04-05T14：30： 30-05： 00" ) 
-   \[YYYY \] \[ mm \] \[ DD \] T \[ HH \] \[ MM \] \[ ss \] Z ( "19810405T193030Z" ) 

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



