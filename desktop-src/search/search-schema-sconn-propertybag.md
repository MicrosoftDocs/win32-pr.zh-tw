---
description: 必要的 <propertyBag> 元素會指定這個位置提供者所使用的一或多個屬性集合。
ms.assetid: 63f8f2e4-3b52-4d6e-8d3a-2e133aac0e86
title: 'propertyBag 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb9e80691e929f7fcceaff3dded4b99a242e92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026108"
---
# <a name="propertybag-element-search-connector-schema"></a><span data-ttu-id="c7e8c-103">propertyBag 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="c7e8c-103">propertyBag Element (Search Connector Schema)</span></span>

<span data-ttu-id="c7e8c-104">必要的 <propertyBag> 元素會指定這個位置提供者所使用的一或多個屬性集合。</span><span class="sxs-lookup"><span data-stu-id="c7e8c-104">The required <propertyBag> element specifies a set of one or more properties used by this location provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e8c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7e8c-105">Syntax</span></span>


```
<!-- propertyBag -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
                            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
                        </xs:element>
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



## <a name="element-information"></a><span data-ttu-id="c7e8c-106">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c7e8c-106">Element Information</span></span>



| <span data-ttu-id="c7e8c-107">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c7e8c-107">Parent Element</span></span>                                                                                 | <span data-ttu-id="c7e8c-108">子元素</span><span class="sxs-lookup"><span data-stu-id="c7e8c-108">Child Elements</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7e8c-109">locationProvider 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="c7e8c-109">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md) | [<span data-ttu-id="c7e8c-110"> (搜尋連接器架構) 的 property 元素 </span><span class="sxs-lookup"><span data-stu-id="c7e8c-110">property Element (Search Connector Schema)</span></span>](search-schema-sconn-locationproviderproperty.md) |



 

## <a name="example-of-a-propertybag-element-and-property-elements"></a><span data-ttu-id="c7e8c-111">PropertyBag 元素和 property 元素的範例</span><span class="sxs-lookup"><span data-stu-id="c7e8c-111">Example of a PropertyBag Element and property Elements</span></span>


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



