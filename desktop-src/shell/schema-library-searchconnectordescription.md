---
description: <searchConnectorDescription>元素是搜尋連接器定義的最上層容器元素。
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: 'searchConnectorDescription 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa6c213d43a648ebea51b58b4c3103a0ee42f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973608"
---
# <a name="searchconnectordescription-element-library-schema"></a><span data-ttu-id="37be8-103">searchConnectorDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="37be8-103">searchConnectorDescription Element (Library Schema)</span></span>

<span data-ttu-id="37be8-104"><searchConnectorDescription>元素是搜尋連接器定義的最上層容器元素。</span><span class="sxs-lookup"><span data-stu-id="37be8-104">The <searchConnectorDescription> element is the top level container element of a search connector definition.</span></span> <span data-ttu-id="37be8-105">專案 <searchConnectorDescription> 是 <searchConnectorDescriptionType> 與 Windows 同盟搜尋連接器相關聯之專案類型的延伸; 不過，您無法在程式庫中包含 Windows 同盟搜尋或通訊協定處理常式的搜尋連接器。</span><span class="sxs-lookup"><span data-stu-id="37be8-105">The <searchConnectorDescription> element is an extension of the <searchConnectorDescriptionType> element type associated with Windows Federated Search connectors; however, you cannot include search connectors for Windows Federated Search or protocol handlers in a library.</span></span>

## <a name="syntax"></a><span data-ttu-id="37be8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="37be8-106">Syntax</span></span>

``` syntax
<!-- searchConnectorDescription -->
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

## <a name="element-information"></a><span data-ttu-id="37be8-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="37be8-107">Element Information</span></span>

<span data-ttu-id="37be8-108">請參閱[Windows Search](/previous-versions/bb268030(v=msdn.10))中的架構檔</span><span class="sxs-lookup"><span data-stu-id="37be8-108">Refer to the schema documentation in [Windows Search](/previous-versions/bb268030(v=msdn.10))</span></span>



| <span data-ttu-id="37be8-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="37be8-109">Parent Element</span></span>                                                                                               | <span data-ttu-id="37be8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="37be8-110">Child Elements</span></span>                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="37be8-111">searchConnectorDescriptionList 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="37be8-111">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md) | <span data-ttu-id="37be8-112"><isSearchOnlyI. tem></span><span class="sxs-lookup"><span data-stu-id="37be8-112"><isSearchOnlyI.tem></span></span>             |
|                                                                                                              | <description>                   |
|                                                                                                              | <iconReference>                 |
|                                                                                                              | <imageLink>                     |
|                                                                                                              | <author>                        |
|                                                                                                              | <dateCreated>                   |
|                                                                                                              | <templateInfo>                  |
|                                                                                                              | <locationProvider>              |
|                                                                                                              | <scope>                         |
|                                                                                                              | <propertyStore>                 |
|                                                                                                              | <domain>                        |
|                                                                                                              | <supportsAdvancedQuerySyntax>   |
|                                                                                                              | <isDefaultSaveLocation>         |
|                                                                                                              | <isDefaultNonOwnerSaveLocation> |
|                                                                                                              | <isIndexed>                     |
|                                                                                                              | <simpleLocation>                |
|                                                                                                              | <includeInStartMenu>            |



 

## <a name="attributes"></a><span data-ttu-id="37be8-113">屬性</span><span class="sxs-lookup"><span data-stu-id="37be8-113">Attributes</span></span>



| <span data-ttu-id="37be8-114">屬性</span><span class="sxs-lookup"><span data-stu-id="37be8-114">Attribute</span></span> | <span data-ttu-id="37be8-115">描述</span><span class="sxs-lookup"><span data-stu-id="37be8-115">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="37be8-116">publisher</span><span class="sxs-lookup"><span data-stu-id="37be8-116">publisher</span></span> | <span data-ttu-id="37be8-117">選擇性。</span><span class="sxs-lookup"><span data-stu-id="37be8-117">Optional.</span></span> <span data-ttu-id="37be8-118">提供搜尋連接器之發行者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="37be8-118">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="37be8-119">product</span><span class="sxs-lookup"><span data-stu-id="37be8-119">product</span></span>   | <span data-ttu-id="37be8-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="37be8-120">Optional.</span></span> <span data-ttu-id="37be8-121">搜尋連接器所套用之產品的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="37be8-121">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="37be8-122">備註</span><span class="sxs-lookup"><span data-stu-id="37be8-122">Remarks</span></span>

<span data-ttu-id="37be8-123">連結 <searchConnectorDescription> 庫的元素使用與 Windows 同盟搜尋相同的架構定義 <searchConnectorDescription> 。</span><span class="sxs-lookup"><span data-stu-id="37be8-123">The <searchConnectorDescription> element of a library uses the same schema definition as the <searchConnectorDescription> for Windows Federated Search.</span></span> <span data-ttu-id="37be8-124">雖然它們使用相同的架構，但 Windows 同盟搜尋的搜尋連接器不能包含在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="37be8-124">Although they use the same schemas, search connectors for Windows Federated search cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37be8-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="37be8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37be8-126">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="37be8-126">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="37be8-127">搜尋連接器描述架構</span><span class="sxs-lookup"><span data-stu-id="37be8-127">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
