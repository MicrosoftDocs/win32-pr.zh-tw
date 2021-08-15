---
description: 選擇性 <iconReference> 元素會指定這個位置的自訂圖示。 此元素沒有屬性和子項目。
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: 'iconReference 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76391eb7079414abe13c4e45696ee3eacb3b968eb93b342b1b9e67825fac85c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862580"
---
# <a name="iconreference-element-search-connector-schema"></a>iconReference 元素 (搜尋連接器架構) 

選擇性 <iconReference> 元素會指定這個位置的自訂圖示。 此元素沒有屬性和子項目。

## <a name="syntax"></a>Syntax


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
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

參考的格式必須以適合 [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) 函式的形式指定： (例如， <dll file name> <icon index>) 。

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
