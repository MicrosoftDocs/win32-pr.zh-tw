---
description: 選擇性的布林值 <isDefaultSaveLocation> 元素會指定是否應該使用搜尋連接器中所述的位置做為預設的儲存位置。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: 'isDefaultSaveLocation 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94cfe2f620dd7c4ccac2bed27dd87511e9174861aeb74dce9ac5737263e9275
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597478"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a>isDefaultSaveLocation 元素 (搜尋連接器架構) 

選擇性的布林值 <isDefaultSaveLocation> 元素會指定是否應該使用搜尋連接器中所述的位置做為預設的儲存位置。 這個元素沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
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

當使用者選擇儲存專案時，Windows 檔案總管會將專案儲存至元素中指定的位置 <simpleLocation> 。 使用者可以使用搜尋連接器的 [屬性] 對話方塊來變更此設定。

## <a name="example"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



