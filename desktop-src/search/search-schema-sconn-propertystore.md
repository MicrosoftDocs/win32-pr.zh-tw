---
description: 選擇性 <propertyStore> 元素會指定以 XML 為基礎之 IPropertyStore 的位置，以儲存此搜尋連接器的開啟中繼資料。 這個元素沒有任何屬性，而且只有一個子項目。
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: 'propertyStore 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de5a9e801163bd85635b82c1915394f24c39d3dfdafcb64c81fcff0bf84a219
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351848"
---
# <a name="propertystore-element-search-connector-schema"></a>propertyStore 元素 (搜尋連接器架構) 

選擇性 <propertyStore> 元素會指定以 XML 為基礎之 IPropertyStore 的位置，以儲存此搜尋連接器的開啟中繼資料。 這個元素沒有任何屬性，而且只有一個子項目。

## <a name="syntax"></a>Syntax


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                                                                   | 子元素                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [searchConnectorDescriptionType 元素 (搜尋連接器架構) ](search-schema-searchconnectordescription.md) | [propertyStore (搜尋連接器架構) 的 property 元素 ](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>範例

下列範例顯示 <propertyStore> 具有兩個元素的元素 <property> 。


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



