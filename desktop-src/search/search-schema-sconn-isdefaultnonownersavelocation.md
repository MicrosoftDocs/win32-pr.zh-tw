---
description: 選擇性的布林值 <isDefaultNonOwnerSaveLocation> 元素會指定當來自家庭電腦上另一部電腦的使用者選擇儲存專案時，是否應使用搜尋連接器中所述的位置做為預設的儲存位置。
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: 'isDefaultNonOwnerSaveLocation 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966681"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>isDefaultNonOwnerSaveLocation 元素 (搜尋連接器架構) 

選擇性的布林值 <isDefaultNonOwnerSaveLocation> 元素會指定當來自家庭電腦上另一部電腦的使用者選擇儲存專案時，是否應使用搜尋連接器中所述的位置做為預設的儲存位置。 這個元素沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
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

若為 true，當使用者從家用電腦中的另一部電腦選擇儲存專案時，Windows 檔案總管會將專案儲存至專案中指定的位置 <simpleLocation> 。

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



