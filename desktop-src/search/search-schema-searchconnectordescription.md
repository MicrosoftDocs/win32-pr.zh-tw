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
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a><span data-ttu-id="4577a-103">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-103">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>

<span data-ttu-id="4577a-104"><searchConnectorDescriptionType>元素是搜尋連接器定義的最上層容器。</span><span class="sxs-lookup"><span data-stu-id="4577a-104">The <searchConnectorDescriptionType> element is the top level container for the search connector definition.</span></span>

-   [<span data-ttu-id="4577a-105">語法</span><span class="sxs-lookup"><span data-stu-id="4577a-105">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="4577a-106">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4577a-106">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4577a-107">屬性</span><span class="sxs-lookup"><span data-stu-id="4577a-107">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="4577a-108">備註</span><span class="sxs-lookup"><span data-stu-id="4577a-108">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="4577a-109">搜尋連接器描述檔案的範例</span><span class="sxs-lookup"><span data-stu-id="4577a-109">Example of a Search Connector Description File</span></span>](#example-of-a-search-connector-description-file)
-   [<span data-ttu-id="4577a-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="4577a-110">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="4577a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4577a-111">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="4577a-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4577a-112">Element Information</span></span>



| <span data-ttu-id="4577a-113">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="4577a-113">Parent Element</span></span> | <span data-ttu-id="4577a-114">子元素</span><span class="sxs-lookup"><span data-stu-id="4577a-114">Child Elements</span></span>                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [<span data-ttu-id="4577a-115">isSearchOnlyItem 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-115">isSearchOnlyItem Element (Search Connector Schema)</span></span>](search-schema-sconn-issearchonlyitem.md)                           |
|                | [<span data-ttu-id="4577a-116">isDefaultSaveLocation 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-116">isDefaultSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [<span data-ttu-id="4577a-117">isDefaultNonOwnerSaveLocation 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-117">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [<span data-ttu-id="4577a-118"> (搜尋連接器架構) 的 description 元素 </span><span class="sxs-lookup"><span data-stu-id="4577a-118">description Element (Search Connector Schema)</span></span>](search-schema-sconn-description.md)                                     |
|                | [<span data-ttu-id="4577a-119">iconReference 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-119">iconReference Element (Search Connector Schema)</span></span>](search-schema-sconn-iconreference.md)                                 |
|                | [<span data-ttu-id="4577a-120">imageLink 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-120">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md)                                         |
|                | [<span data-ttu-id="4577a-121">author 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-121">author Element (Search Connector Schema)</span></span>](search-schema-sconn-author.md)                                               |
|                | [<span data-ttu-id="4577a-122">dateCreated 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-122">dateCreated Element (Search Connector Schema)</span></span>](search-schema-sconn-datecreated.md)                                     |
|                | [<span data-ttu-id="4577a-123">templateInfo 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-123">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md)                                   |
|                | [<span data-ttu-id="4577a-124">locationProvider 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-124">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md)                           |
|                | [<span data-ttu-id="4577a-125">範圍元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-125">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md)                                                 |
|                | [<span data-ttu-id="4577a-126">propertyStore 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-126">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md)                                 |
|                | [<span data-ttu-id="4577a-127">includeInStartMenuScope 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-127">includeInStartMenuScope Element (Search Connector Schema)</span></span>](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [<span data-ttu-id="4577a-128">網域元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-128">domain Element (Search Connector Schema)</span></span>](search-schema-sconn-domain.md)                                               |
|                | [<span data-ttu-id="4577a-129">supportsAdvancedQuerySyntax 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-129">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [<span data-ttu-id="4577a-130">isIndexed 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="4577a-130">isIndexed Element (Search Connector Schema)</span></span>](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a><span data-ttu-id="4577a-131">屬性</span><span class="sxs-lookup"><span data-stu-id="4577a-131">Attributes</span></span>



| <span data-ttu-id="4577a-132">屬性</span><span class="sxs-lookup"><span data-stu-id="4577a-132">Attribute</span></span> | <span data-ttu-id="4577a-133">描述</span><span class="sxs-lookup"><span data-stu-id="4577a-133">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4577a-134">publisher</span><span class="sxs-lookup"><span data-stu-id="4577a-134">publisher</span></span> | <span data-ttu-id="4577a-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="4577a-135">Optional.</span></span> <span data-ttu-id="4577a-136">提供搜尋連接器之發行者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4577a-136">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="4577a-137">product</span><span class="sxs-lookup"><span data-stu-id="4577a-137">product</span></span>   | <span data-ttu-id="4577a-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="4577a-138">Optional.</span></span> <span data-ttu-id="4577a-139">搜尋連接器所套用之產品的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4577a-139">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4577a-140">備註</span><span class="sxs-lookup"><span data-stu-id="4577a-140">Remarks</span></span>

<span data-ttu-id="4577a-141">適用于同盟搜尋的搜尋連接器不能用在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="4577a-141">Search connectors for federated search cannot be used in libraries.</span></span> <span data-ttu-id="4577a-142">程式庫搜尋連接器的架構是此處所述架構的延伸模組，並包含程式庫特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="4577a-142">The schema for library search connectors is an extension of the schema described here and includes information specific to libraries.</span></span>

## <a name="example-of-a-search-connector-description-file"></a><span data-ttu-id="4577a-143">搜尋連接器描述檔案的範例</span><span class="sxs-lookup"><span data-stu-id="4577a-143">Example of a Search Connector Description File</span></span>

<span data-ttu-id="4577a-144">以下是同盟搜尋 web 服務的搜尋連接器描述檔案範例。</span><span class="sxs-lookup"><span data-stu-id="4577a-144">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


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



<span data-ttu-id="4577a-145">以下是 MAPI 通訊協定處理常式的搜尋連接器描述檔案範例。</span><span class="sxs-lookup"><span data-stu-id="4577a-145">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4577a-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="4577a-146">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4577a-147">**參考**</span><span class="sxs-lookup"><span data-stu-id="4577a-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4577a-148">搜尋連接器描述架構的總覽</span><span class="sxs-lookup"><span data-stu-id="4577a-148">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="4577a-149">**概念**</span><span class="sxs-lookup"><span data-stu-id="4577a-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4577a-150">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="4577a-150">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> </dl>

 

 



