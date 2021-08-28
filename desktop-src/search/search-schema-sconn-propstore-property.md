---
description: 選擇性 &lt; 屬性 &gt; 元素會指定搜尋連接器所使用的屬性。 這些是此搜尋連接器特有的屬性，因此沒有預先定義的名稱組可供使用。 這個元素沒有任何子項目。
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: propertyStore (搜尋連接器架構) 的 property 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ad97c22ac87d67fdec0d007d4333bffe16aad1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886772"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>propertyStore (搜尋連接器架構) 的 property 元素

選擇性 &lt; 屬性 &gt; 元素會指定搜尋連接器所使用的屬性。 這些是此搜尋連接器特有的屬性，因此沒有預先定義的名稱組可供使用。 這個元素沒有任何子項目。

## <a name="syntax"></a>Syntax


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                                           | 子元素 |
|------------------------------------------------------------------------------------------|----------------|
| [propertyStore 元素 (搜尋連接器架構) ](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a>屬性




| 屬性 | 說明 | 值 | 
|-----------|-------------|--------|
| NAME | 公用。 必要。 屬性的顯示名稱。 |   | 
| 類型 | 公用。 必要。 屬性的類型。 | 任何：預設值。 此值將不會被屬性子系統強制轉型。 GetPropertyType 會傳回 VT_Null。<ul><li>Null：沒有這個屬性的值。 GetPropertyType 會傳回 VT_Null。</li><li>字串：值必須是 VT_LPWSTR。</li><li>布林值：此值必須是 VT_BOOL。</li><li>Byte：此值必須是 VT_UI1。</li><li>緩衝區：此值必須是 VT_UI1 | VT_VECTOR 位元組緩衝區。</li><li>Int16：此值必須是 VT_I2。</li><li>UInt16：此值必須是 VT_UI2。</li><li>Int32：此值必須是 VT_I4。</li><li>UInt32：此值必須是 VT_UI4。</li><li>Int64：此值必須是 VT_I8。</li><li>UInt64：此值必須是 VT_UI8</li><li>Double：此值必須是 VT_R8。</li><li>DateTime：此值必須是 VT_FILETIME。</li><li>Guid：此值必須是 VT_CLSID。</li><li>Blob：此值必須是 VT_BLOB。</li><li>物件：此值必須是 VT_UNKNOWN。</li><li>Stream：此值必須是 VT_STREAM。</li><li>剪貼簿：此值必須是 VT_CF。</li></ul> | 
| schema | 公用。 選擇性。 定義屬性的架構。 |   | 




 

## <a name="remarks"></a>備註

OpenSearch 搜尋連接器可以使用 OpenSearchHTMLRolloverTemplate 屬性。 這個屬性會識別依照 OpenSearch 範本慣例格式化的範本。 當使用者按一下命令列中的 [在網站上搜尋] 按鈕時，會使用 OpenSearchHTMLRolloverTemplate 範本。

## <a name="example"></a>範例

下列範例顯示 &lt; &gt; 具有兩個 &lt; property 元素的 propertyStore 專案 &gt; 。


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



