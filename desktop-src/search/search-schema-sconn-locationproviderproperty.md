---
description: 選擇性 <property> 元素會指定位置提供者所使用的屬性。
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: locationProvider (搜尋連接器架構) 的 property 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623d54ef98986c603acc709bcd39ca1ac5504b89
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471554"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>locationProvider (搜尋連接器架構) 的 property 元素

選擇性 <property> 元素會指定位置提供者所使用的屬性。 這些屬性是此位置提供者特有的屬性，因此沒有預先定義的名稱組可供使用。 <property>此元素有兩個屬性，如本主題中所述。

## <a name="syntax"></a>Syntax


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><property> 元素資訊



| Parent 項目                                                                                 | 子元素                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [locationProvider 元素 (搜尋連接器架構) ](search-schema-sconn-locationprovider.md) | 屬性，如本主題中所述。 |



 


## <a name="property-attributes"></a><property> 屬性




| 屬性 | 描述 | 值 | 
|-----------|-------------|--------|
| NAME | 必要。 屬性的顯示名稱。 |   | 
| 類型 | 必要。 屬性的類型。 | 任何：預設值。 此值將不會被屬性子系統強制轉型。 GetPropertyType 會傳回 VT_Null。<ul><li>Null：沒有這個屬性的值。 GetPropertyType 會傳回 VT_Null。</li><li>字串：值必須是 VT_LPWSTR。</li><li>布林值：此值必須是 VT_BOOL。</li><li>Byte：此值必須是 VT_UI1。</li><li>緩衝區：此值必須是 VT_UI1 | VT_VECTOR 位元組緩衝區。</li><li>Int16：此值必須是 VT_I2。</li><li>UInt16：此值必須是 VT_UI2。</li><li>Int32：此值必須是 VT_I4。</li><li>UInt32：此值必須是 VT_UI4。</li><li>Int64：此值必須是 VT_I8。</li><li>UInt64：此值必須是 VT_UI8</li><li>Double：此值必須是 VT_R8。</li><li>DateTime：此值必須是 VT_FILETIME。</li><li>Guid：此值必須是 VT_CLSID。</li><li>Blob：此值必須是 VT_BLOB。</li><li>物件：此值必須是 VT_UNKNOWN。</li><li>Stream：此值必須是 VT_STREAM。</li><li>剪貼簿：此值必須是 VT_CF。</li></ul> | 




 

## <a name="remarks"></a>備註

針對 OpenSearch 提供者，會使用下列屬性：

-   OpenSearchShortName：搜尋服務的簡短名稱
-   OpenSearchQueryTemplate：以查詢服務的 OpenSearch 樣板慣例格式化的範本
-   MaximumResultCount： (number) 搜尋服務所傳回的結果數目上限
-   LinkIsFilePath： (布林值) 如果為 true，則提供者會嘗試將傳回的專案解讀為檔案，並使用其擴充功能在視圖中建立適當的 ShellItem。 如果為 false，則會將專案視為 URL 快捷方式。

 

 



