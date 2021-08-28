---
description: 選擇性的 &lt; locationProvider 專案 &gt; 會指定 web 服務提供者搜尋連接器要使用的搜尋提供者。 這個元素包含一個強制屬性和一個選擇性的子項目。
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: 'locationProvider 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f049a01cc0c51075c147918a2f43b740000f2e36
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883371"
---
# <a name="locationprovider-element-search-connector-schema"></a>locationProvider 元素 (搜尋連接器架構) 

選擇性的 &lt; locationProvider 專案 &gt; 會指定 web 服務提供者搜尋連接器要使用的搜尋提供者。 這個元素包含一個強制屬性和一個選擇性的子項目。

## <a name="syntax"></a>Syntax


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                                                                   | 子元素                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [searchConnectorDescriptionType 元素 (搜尋連接器架構) ](search-schema-searchconnectordescription.md) | [propertyBag 元素 (搜尋連接器架構) ](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>屬性



| 屬性 | 描述                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | 必要。 搜尋提供者 (CLSID) 的類別識別碼。 |
| codebase  | 選擇性。                                                      |



 

## <a name="remarks"></a>備註

@clsidOpenSearch 提供者的屬性值為 {48E277F6-4E74-4cd6-BA6F-FA4F42898223}。

以檔案系統和通訊協定處理常式為基礎的搜尋連接器可以改用[ &lt; simpleLocation &gt; ](search-schema-sconn-simplelocation.md)元素。 如果 &lt; locationProvider &gt; 存在， &lt; &gt; 則搜尋連接器描述中不能有 simpleLocation 元素。

## <a name="example-of-a-locationprovider-element"></a>LocationProvider 元素範例


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



