---
description: <property>元素指定程式庫所使用的屬性。 這些是程式庫特有的屬性，因此沒有預先定義的屬性名稱組可供使用。 這個元素是選擇性的，且沒有任何子項目。
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: 'property 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481122db633750b042172561eedace81fe1d752e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468635"
---
# <a name="property-element-library-schema"></a>property 元素 (程式庫架構) 

<property>元素指定程式庫所使用的屬性。 這些是程式庫特有的屬性，因此沒有預先定義的屬性名稱組可供使用。 這個元素是選擇性的，且沒有任何子項目。

## <a name="syntax"></a>Syntax

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>項目資訊



| Parent 項目                                                             | 子元素 |
|----------------------------------------------------------------------------|----------------|
| [propertyStore 元素 (程式庫架構) ](schema-library-propertystore.md) | 無           |



 

## <a name="attributes"></a>屬性




| 屬性 | 描述 | 值 | 
|-----------|-------------|--------|
| NAME | 公用。 必要。 屬性的顯示名稱。 | 
| 類型 | 公用。 必要。 屬性的類型。 | <ul><li>任何：預設值。 此值將不會被屬性子系統強制轉型。 GetPropertyType 會傳回 VT_Null。</li><li>Null：沒有這個屬性的值。 GetPropertyType 會傳回 VT_Null。</li><li>字串：值必須是 VT_LPWSTR。</li><li>布林值：此值必須是 VT_BOOL。</li><li>Byte：此值必須是 VT_UI1。</li><li>緩衝區：此值必須是 VT_UI1 | VT_VECTOR 位元組緩衝區。</li><li>Int16：此值必須是 VT_I2。</li><li>UInt16：此值必須是 VT_UI2。</li><li>Int32：此值必須是 VT_I4。</li><li>UInt32：此值必須是 VT_UI4。</li><li>Int64：此值必須是 VT_I8。</li><li>UInt64：此值必須是 VT_UI8。</li><li>Double：此值必須是 VT_R8。</li><li>DateTime：此值必須是 VT_FILETIME。</li><li>Guid：此值必須是 VT_CLSID。</li><li>Blob：此值必須是 VT_BLOB。</li><li>物件：此值必須是 VT_UNKNOWN。</li><li>Stream：此值必須是 VT_STREAM。</li><li>剪貼簿：此值必須是 VT_CF。</li></ul> | 




 

## <a name="remarks"></a>備註

<標準名稱> 元素的需求符合 Windows Search 和 Windows 屬性系統的需求。 字串的型別必須是標準型別。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式庫描述架構](library-schema-entry.md)
</dt> <dt>

[屬性結構描述](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[搜尋連接器描述架構](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
