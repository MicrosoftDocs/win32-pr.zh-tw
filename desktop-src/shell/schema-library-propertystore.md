---
description: <propertyStore>元素會指定這個程式庫所使用的一或多個屬性集合。 這個元素是選擇性的，且沒有任何屬性。
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: 'propertyStore 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973532"
---
# <a name="propertystore-element-library-schema"></a>propertyStore 元素 (程式庫架構) 

<propertyStore>元素會指定這個程式庫所使用的一或多個屬性集合。 這個元素是選擇性的，且沒有任何屬性。

## <a name="syntax"></a>Syntax

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>項目資訊



| Parent 項目                                                               | 子元素                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [libraryDescription 元素 (程式庫架構) ](schema-librarydescription.md) | [property 元素 (程式庫架構) ](schema-library-property.md) |



 

## <a name="remarks"></a>備註

<propertyStore>元素可以有一或多 <property> 個子項目。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式庫描述架構](library-schema-entry.md)
</dt> <dt>

[搜尋連接器描述架構](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
