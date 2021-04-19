---
description: <searchConnectorDescriptionType>元素是搜尋連接器定義的最上層容器。
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: 'searchConnectorDescriptionType 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7edb69647567b7e18e25e11dcd0fc773d0be7902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970774"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a>searchConnectorDescriptionType 元素 (搜尋連接器架構) 

<searchConnectorDescriptionType>元素是搜尋連接器定義的最上層容器。

-   [語法](#syntax)
-   [項目資訊](#element-information)
-   [屬性](#attributes)
-   [備註](#remarks)
-   [搜尋連接器描述檔案的範例](#example-of-a-search-connector-description-file)
-   [相關主題](#related-topics)

## <a name="syntax"></a>Syntax


```
<!-- searchConnectorDescriptionType -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
   <xs:complexType name="searchConnectorDescriptionType">
      <xs:all>
         <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
         <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/
         <xs:element name="description" type="xs:string" minOccurs="0"/>
         <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
         <xs:element name="imageLink" minOccurs="0">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="url" type="xs:anyURI"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="author" type="xs:string" minOccurs="0"/>
         <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
         <xs:element name="templateInfo" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="folderType" minOccurs="0"/>
               </xs:all>
            </xs:complexType>
         </xs:element>
         <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0"/>
         <xs:element name="locationProvider" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
               </xs:all>
               <xs:attribute name="clsid" use="required"/>
               <xs:attribute name="codebase" type="xs:string"/>
            </xs:complexType>
         </xs:element>
         <xs:element name="scope" minOccurs="0">
            <xs:complexType>
               <xs:sequence minOccurs="0">
                  <xs:element name="scopeItem" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:all>
                           <xs:element name="mode" default="Include">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Include"/>
                                    <xs:enumeration value="Exclude"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="depth" default="Shallow" minOccurs="0">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Shallow"/>
                                    <xs:enumeration value="Deep"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="url" type="xs:anyURI"/>
                        </xs:all>
                     </xs:complexType>
                  </xs:element>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0"/>
         <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="domain" type="xs:string" minOccurs="0"/>
         <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isIndexed" type="xs:boolean" minOccurs="0"/>
      </xs:all>
      <xs:attribute name="publisher" type="xs:string"/>
      <xs:attribute name="product" type="xs:string"/>
   </xs:complexType>
</xs:schema>
```



## <a name="element-information"></a>項目資訊



| Parent 項目 | 子元素                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [isSearchOnlyItem 元素 (搜尋連接器架構) ](search-schema-sconn-issearchonlyitem.md)                           |
|                | [isDefaultSaveLocation 元素 (搜尋連接器架構) ](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [isDefaultNonOwnerSaveLocation 元素 (搜尋連接器架構) ](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [ (搜尋連接器架構) 的 description 元素 ](search-schema-sconn-description.md)                                     |
|                | [iconReference 元素 (搜尋連接器架構) ](search-schema-sconn-iconreference.md)                                 |
|                | [imageLink 元素 (搜尋連接器架構) ](search-schema-sconn-imagelink.md)                                         |
|                | [author 元素 (搜尋連接器架構) ](search-schema-sconn-author.md)                                               |
|                | [dateCreated 元素 (搜尋連接器架構) ](search-schema-sconn-datecreated.md)                                     |
|                | [templateInfo 元素 (搜尋連接器架構) ](search-schema-sconn-templateinfo.md)                                   |
|                | [locationProvider 元素 (搜尋連接器架構) ](search-schema-sconn-locationprovider.md)                           |
|                | [範圍元素 (搜尋連接器架構) ](search-schema-sconn-scope.md)                                                 |
|                | [propertyStore 元素 (搜尋連接器架構) ](search-schema-sconn-propertystore.md)                                 |
|                | [includeInStartMenuScope 元素 (搜尋連接器架構) ](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [網域元素 (搜尋連接器架構) ](search-schema-sconn-domain.md)                                               |
|                | [supportsAdvancedQuerySyntax 元素 (搜尋連接器架構) ](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [isIndexed 元素 (搜尋連接器架構) ](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a>屬性



| 屬性 | 描述                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | 選擇性。 提供搜尋連接器之發行者的顯示名稱。      |
| product   | 選擇性。 搜尋連接器所套用之產品的顯示名稱。 |



 

## <a name="remarks"></a>備註

適用于同盟搜尋的搜尋連接器不能用在程式庫中。 程式庫搜尋連接器的架構是此處所述架構的延伸模組，並包含程式庫特定的資訊。

## <a name="example-of-a-search-connector-description-file"></a>搜尋連接器描述檔案的範例

以下是同盟搜尋 web 服務的搜尋連接器描述檔案範例。


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



以下是 MAPI 通訊協定處理常式的搜尋連接器描述檔案範例。


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[搜尋連接器描述架構的總覽](search-sconn-desc-schema-entry.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows 中的同盟搜尋](-search-federated-search-overview.md)
</dt> </dl>

 

 



